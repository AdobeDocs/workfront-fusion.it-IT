---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Chiamata delle API Workfront e Fusion dall’estensione
description: Chiamata delle API Workfront e Fusion dall’estensione
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# Chiamata delle API Workfront e Fusion dall’estensione

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Il riferimento al contesto di Fusion ti fornisce il token IMS dell’utente connesso, quindi un naturale passaggio successivo consiste nel chiamare le API Workfront o Fusion e mostrare i dati reali. Ciò non è possibile a causa di CORS. Questo articolo mostra come aggirare tale limite utilizzando un’azione di runtime di App Builder come proxy lato server e include un esempio (il dashboard delle sottoscrizioni degli eventi).

## Perché una chiamata diretta al browser non riesce (CORS)

L&#39;interfaccia utente visibile viene eseguita in un `<iframe>` fornito dal CDN di Adobe (`https://<your-app>.adobeio-static.net`). Quando la pagina `fetch(...)` viene aggiunta a un&#39;API Workfront o Fusion su un&#39;origine **diversa**, il browser applica la condivisione CORS (Cross-Origin Resource Sharing). A meno che l&#39;API non restituisca esplicitamente `Access-Control-Allow-Origin` per l&#39;origine CDN, il browser blocca la risposta. Queste API non inseriscono nell&#39;elenco Consentiti origini di estensioni arbitrarie, pertanto le chiamate dirette dal guest non riescono.

Per informazioni su CORS, vedi [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS).

## Chiama la tua azione di runtime senza CORS

Per risolvere questo problema, devi chiamare la tua azione di runtime senza CORS.

Le app App Builder possono includere azioni di runtime, ovvero piccole funzioni senza server eseguite su Adobe I/O Runtime lato server. Le chiamate server-to-server non sono soggette al CORS del browser. Poiché l’azione fa parte dell’app, l’ospite può chiamarla con un URL relativo, che ha la stessa origine e quindi non è bloccato.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

L’azione riceve il token IMS dell’utente dall’ospite e lo inoltra a monte, pertanto le chiamate vengono ancora effettuate per conto dell’utente con le relative autorizzazioni.

## Passaggio 1: Dichiarare l’azione

Le azioni di runtime sono dichiarate in `app.config.yaml` sotto l&#39;estensione `runtimeManifest`. Aggiungi un&#39;azione `wf-proxy` accanto all&#39;estensione:

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

L’azione diventa raggiungibile in:

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`: true vs false

Questa annotazione controlla se il gateway di Adobe convalida un token IMS prima dell’esecuzione dell’azione.

* **`true`:** Il valore predefinito protetto.  Il gateway rifiuta le chiamate non autenticate. Tuttavia, la funzione di convalida è molto rigida in merito alle intestazioni previste e può rifiutare le richieste o eliminare le intestazioni personalizzate necessarie per la chiamata a monte. In questo caso, verrà visualizzato come `401` anche se il token è valido.
* **`false`:** Ignora il controllo del gateway. La tua azione è quindi richiamabile pubblicamente, quindi **devi** applicare l&#39;autorizzazione autonomamente. Richiedi un bearer `Authorization` nell&#39;azione e rifiutalo se manca, quindi inoltralo a monte, dove Workfront e Fusion lo convalidano. In combinazione con un rigoroso inserisco nell&#39;elenco Consentiti di targeting di, descritto nel passaggio 2, questo è il percorso affidabile per un proxy che deve trasmettere intestazioni personalizzate.

>[!TIP]
>
> Prova prima `true`. Se vedi un `401` che non puoi spiegare perché il token è valido e funziona altrove, passa a `false` **e** mantieni l&#39;assegno al portatore e inserisci nell&#39;elenco Consentiti l&#39;azione in modo che la sicurezza sia ancora applicata a monte.

## Passaggio 2: scrivere l&#39;azione per un proxy inserito nell&#39;elenco Consentiti

Crea `src/fusion-nav-organization-1/actions/wf-proxy/index.js`. Due regole lo mantengono sicuro: una inserisce nell&#39;elenco Consentiti di targeting a monte di cui l’azione non può essere utilizzata come relay aperto e un token bearer richiesto che viene inoltrato a monte.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse` e `checkMissingRequestInputs` provengono dai `actions/utils.js` generati, dove sono scaffollati dal modello. `getBearerToken` legge `params.__ow_headers.authorization`, che è il punto in cui il gateway inserisce l&#39;intestazione `Authorization` in ingresso.

## Passaggio 3: chiama l’azione dall’ospite

Dall’interfaccia utente, `fetch` l’azione con un URL relativo (della stessa origine) e invia il token IMS come bearer. Passa gli ID organizzazione e team necessari all’elemento a monte come parametri di query.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Ottieni `token`, `imsOrgId`, `fusionOrgId` e `teamId` dal contesto:

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

Per informazioni sul contesto, vedere [Riferimento al contesto di Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Specifiche API di Fusion v3

Funzionamento del dashboard rispetto a `https://fusion.adobe.com/api/v3`:

| Intestazione/parametro | Valore | Note |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | Token IMS dell’utente dal contesto. |
| `x-organization-id` | `organization.id` | ID tenant proprio di Fusion, non l’ID organizzazione IMS. Fusion identifica il tenant in base a questo. |
| `x-team-id` | `team.id` | Invia quando la chiamata ha un ambito di team. |
| `x-gw-ims-org-id` | `imsOrgId` | ID organizzazione Adobe IMS per il gateway. |

Osserva le seguenti avvertenze:

* **`GET /api/v3/hooks`con ambito team:** `teamId` è un **parametro query obbligatorio** (`/api/v3/hooks?teamId=...`). Senza di esso si ottiene un `400`. Ciò significa che gli hook tornano solo per il *team attivo*; per coprire un&#39;organizzazione, eseguire il loop dei team e unire.
* **`GET /api/v3/scenarios`** funziona con `organizationId` (`/api/v3/scenarios?organizationId=...`).

>[!NOTE]
>
> Il riferimento ufficiale è [API Workfront Fusion](https://developer.adobe.com/workfront-fusion-apis/) di Adobe. I requisiti di intestazione/autenticazione variano a seconda del gateway. Questa tabella riflette ciò di cui la demo aveva effettivamente bisogno. Se una chiamata restituisce `401`/`400`, ricontrolla prima queste intestazioni.

## Paginare i risultati dell’elenco

Gli endpoint dell&#39;elenco di Fusion v3 (hook, scenari) restituiscono una **pagina** alla volta, non l&#39;intero set. Una risposta è simile alla seguente:

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

I record si trovano in **`items`** e i metadati di impaginazione in **`_page`**. Si esegue la pagina con i parametri di query **`start`** (offset) e **`limit`** (dimensioni pagina). Il proxy di cui sopra trasmette entrambi, quindi la pagina nell’ospite effettuando un ciclo fino a quando non hai raccolto tutto:

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

Se si desidera mantenere il paging all&#39;esterno del browser, eseguire lo stesso ciclo all&#39;interno dell&#39;azione di runtime e restituire l&#39;array `items` unito in un&#39;unica risposta. In entrambi i casi, non presumere che la prima pagina sia l’intero set di risultati. In caso contrario, un team con più pagine di hook potrebbe avere l’aspetto di un team con scenari mancanti.

## Lista di controllo protezione

* **Inserisci nell&#39;elenco Consentiti a monte.** Non creare mai l’URL di destinazione dall’input del client non elaborato. Mappare una chiave `target` breve a un URL fisso, come nel passaggio 2. Questo impedisce che l’azione diventi un relè aperto.
* **Richiedi il token Bearer** nell&#39;azione e inoltralo a monte. Consenti a Workfront e Fusion di applicare le autorizzazioni dell&#39;utente.
* **Non registrare mai il token.** `imsToken` è una credenziale Tieni presente `LOG_LEVEL` sulle stampe di `stringParameters`.
* **Inoltra solo tramite HTTPS** agli host attendibili di Adobe e Workfront.

## Esempio funzionante: il dashboard delle sottoscrizioni degli eventi

Il dashboard demo si unisce a tre origini per mostrare, in base all’abbonamento a un evento Workfront, se uno scenario Fusion corrispondente è integro:

1. `fetchSubscriptions()` → sottoscrizioni di eventi Workfront (con contatori ricevuti/passati).
1. `fetchHooks(teamId)` → hook di Fusion per il team attivo (paging con `fetchAllPages`).
1. `fetchScenarios(fusionOrgId)` scenari → Fusion per l&#39;organizzazione (paging con `fetchAllPages`).

Il **join** li concatena, ma esiste un catch che vale la pena richiamare: una sottoscrizione Workfront e l&#39;hook Fusion punta a **host diversi**, pertanto i relativi campi URL non sono uguali byte per byte. Il token **alla fine dell&#39;URL del webhook** (ultimo segmento di percorso) è stabile. Corrispondenza con il token finale, non con l&#39;URL completo. Il `scenarioId` dell&#39;hook corrisponde quindi al `id` di uno scenario:

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

Lo stato è derivato dal join:

* **Interrotto**: nessun hook corrispondente oppure l&#39;hook è `gone`.
* **Filtro**: corrisponde, ma `passed < received` (gli eventi arrivano ma vengono filtrati prima dell&#39;esecuzione dello scenario).
* **Integro**: corrisponde e passa.

Poiché le forme del payload reale variano, il client mappa i campi in modo difensivo, tentando diverse chiavi candidate per campo, in modo che una differenza API minore non interrompa la tabella:

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

Questo è solo un esempio. Lo stesso modello proxy funziona per qualsiasi API Workfront o Fusion necessaria.
