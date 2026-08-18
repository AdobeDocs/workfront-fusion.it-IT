---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Risoluzione dei problemi relativi alle estensioni personalizzate
description: Risoluzione dei problemi relativi alle estensioni personalizzate
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# Risoluzione dei problemi relativi alle estensioni personalizzate

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Questo articolo presenta alcune soluzioni ai problemi che è più probabile incontrare durante la creazione di estensioni personalizzate, approssimativamente nell&#39;ordine in cui si verificano durante lo sviluppo.

## Elenco di controllo rapido

Se qualcosa non funziona, verifica prima quanto segue:

* Node.js è la versione 18 o 20 (`node --version`).
* Hai effettuato l&#39;accesso (`aio login`) e nell&#39;organizzazione, nel progetto o nell&#39;area di lavoro corretta (`aio console where`).
* Il nome del punto di estensione corrisponde esattamente, inclusa la versione: `fusion/nav-organization/1`.
* `url` in `getWidget()` corrisponde a un percorso nell&#39;app.
* Chiamate visibili dell&#39;interfaccia utente `attach({ id })`.
* Stai esaminando il set giusto di estensioni in Fusion:
  * Per visualizzare una build di staging, distribuisci nell’ambiente di staging e attiva lo switch Estensioni di staging nel profilo di Fusion (Impostazioni prodotto > Profilo di Fusion > Preferenze).
  * Per visualizzare un’estensione pubblicata, distribuiscila in produzione e ottieni l’approvazione.

## Errore 1060: &quot;Il punto di estensione non esiste&quot;

**Messaggio completo:** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist` durante `aio app deploy`.

**Significato:** il punto di estensione Fusion non è ancora abilitato (&quot;onboarded&quot;) per la tua organizzazione Adobe. Adobe verifica, al momento della distribuzione, che il punto di estensione esista nel catalogo della tua organizzazione. **non** è un problema con il tuo codice o YAML.

**Correzione:** Chiedi al team di Fusion di integrare i punti di estensione (`fusion/nav-organization/1` e/o `fusion/nav-team/1`) per la tua organizzazione IMS. Quando richiedi l’onboarding, includi:

* il tuo **id organizzazione IMS** (`XXXX@AdobeOrg`),
* i **punti di estensione** necessari,
* i tuoi nomi di **progetto Developer Console e area di lavoro**.

Una volta confermato l&#39;onboarding, rieseguire `aio app deploy`.


## &quot;In attesa del messaggio iniziale dall’iframe di destinazione&quot; / il pannello gira per sempre

**Significato:** Fusion ha aperto l&#39;interfaccia utente visibile ma non ha completato l&#39;handshake. Timeout di Fusion.

**Cause comuni:**

* `attach` si trova solo nel componente di registrazione, non nel widget visibile.
* `url` in `getWidget()` punta a una route che esegue il rendering del componente **registrazione** (o di una pagina vuota) al posto del widget.
* Il `id` passato a `attach` è diverso dal `id` utilizzato in `register`. Devono essere identici, quindi mantieni entrambi in `Constants.js`.

**Correzione:** Assicurarsi che il componente **visible** chiami `attach({ id })`:

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

Per ulteriori informazioni, vedere [Creare l&#39;interfaccia utente dell&#39;estensione personalizzata](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).



## Il pulsante di navigazione non viene visualizzato in Fusion

Se il pulsante di navigazione per l’estensione personalizzata non viene visualizzato in Fusion, verifica questi elementi nell’ordine:

1. **Stai cercando il set giusto di estensioni?** Per impostazione predefinita, Fusion mostra solo le estensioni pubblicate, distribuite in produzione e approvate. Se stai testando una build di Stage, attiva lo switch Estensioni di Stage nel profilo di Fusion (Impostazioni prodotto > Profilo di Fusion > Preferenze) e ricarica. Gli elementi della fase sono etichettati **(fase)**.
Per ulteriori informazioni, consulta [Pubblicare l&#39;estensione personalizzata](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. **È stato revocato o ritirato?** Un&#39;estensione revocata o ritirata non viene più visualizzata in Fusion senza alcun errore. Se un pulsante che funzionava in precedenza scompare, prima di cercare un problema di codice conferma che sia ancora attivo in Adobe Exchange.
1. **È distribuito nell&#39;area di lavoro corretta?** Distribuisci nell’area di lavoro che stai caricando, l’area di lavoro Stage quando utilizzi l’opzione Test dello stage.
1. **È distribuito nell&#39;organizzazione corretta?** Accedi a Fusion con un account nella **stessa** organizzazione IMS in cui hai eseguito la distribuzione.
1. **La sezione è corretta?** `fusion/nav-organization/1` viene visualizzato in **Organizzazione**; `fusion/nav-team/1` viene visualizzato in **Team** (è necessario selezionare prima un team).
1. **Esiste un errore di battitura del nome del punto di estensione?** Deve leggere esattamente `fusion/nav-organization/1` sia in `app.config.yaml` che nel percorso di inclusione `ext.config.yaml` della cartella.


## Il pulsante viene visualizzato ma il pannello è vuoto

Se il pulsante viene visualizzato ma il pannello è vuoto, verificare quanto segue:

* **Mancata corrispondenza percorso:** `url` da `getWidget()` (ad esempio `/index.html#/my-widget`) deve corrispondere a `<Route>` in `App.js`. Una mancata corrispondenza carica una pagina senza alcun componente.
* **Errore JavaScript:** apri la scheda Strumenti per sviluppatori (F12) > **Console** del browser e cerca gli errori provenienti dall&#39;iframe. Correggi l’errore segnalato e ridistribuiscilo.
* **Intestazione mancante/duplicata:** `hideWidgetHeader` in `getWidget()` controlla se Fusion mostra il titolo sopra l&#39;interfaccia utente. Impostalo su `true` se esegui il rendering della tua intestazione.

## L’iframe è bloccato (informativa sulla sicurezza dei contenuti/&quot;rifiutato all’inquadratura&quot;)

Fusion consente solo le estensioni ospitate sulla rete CDN App Builder di Adobe (`*.adobeio-static.net`), che è dove `aio app deploy` inserisce i file per impostazione predefinita. Se ospiti l’interfaccia utente da un’altra posizione, ad esempio un dominio personalizzato, Fusion rifiuta di caricarla. Distribuisci tramite App Builder come documentato, oppure chiedi al team di Fusion se il tuo dominio può essere inserito nell&#39;elenco Consentiti.

## Il contesto è vuoto o non aggiornato

* **Vuoto subito dopo il caricamento:** Leggi il contesto **dopo** `attach` risolve, non prima. Fino ad allora, mostrare uno stato &quot;Connessione in corso...&quot;.
* **Nessun aggiornamento quando l&#39;utente cambia organizzazione o team:** Iscriviti all&#39;evento `contextchange` e rileggi le chiavi nel gestore. Per ulteriori informazioni, vedere [Leggere il contesto Condivisioni Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares) nell&#39;articolo Creare l&#39;interfaccia utente dell&#39;estensione personalizzata.
* **Le date non sono corrette:** I campi data arrivano come **stringhe** ISO, non come `Date` oggetti. Racchiudile in `new Date(...)`. Vedi [Date](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates) nell&#39;articolo Riferimento al contesto di Fusion.

## La chiamata di un’API non riesce e genera un errore CORS

**Sintomo:** La console del browser mostra *&quot;Nessuna intestazione &#39;Access-Control-Allow-Origin&#39;&quot;* (o la richiesta è bloccata) quando l&#39;interfaccia utente chiama direttamente un&#39;API Workfront/Fusion.

**Correzione:** Non chiamare tali API dal browser. Indirizza la chiamata tramite la tua **azione runtime** di App Builder (lato server, senza CORS) e fai in modo che il guest chiami l&#39;azione con un URL relativo della stessa origine. Per ulteriori informazioni, vedere [Chiamata delle API Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


## L’azione proxy restituisce 401 anche con un token valido

**Significato:** Con `require-adobe-auth: true`, il gateway di Adobe convalida la chiamata prima dell&#39;esecuzione dell&#39;azione e può rifiutarla o eliminare le intestazioni personalizzate necessarie a monte, presentandosi come `401`.

**Correzione:** Imposta `require-adobe-auth: false` sull&#39;azione **e** applica autonomamente l&#39;autorizzazione. Richiedi un portatore `Authorization` nell&#39;azione, inoltralo a monte e mantieni un rigoroso elenco Consentiti di destinazione. Vedi [require-adobe-auth: true vs. false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false).

## La fusione `GET /api/v3/hooks` restituisce 400

**Significato:** l&#39;endpoint degli hook è **con ambito team**, quindi `teamId` è un parametro di query obbligatorio.

**Correzione:** Chiamare `/api/v3/hooks?teamId=<team.id>`. Gli hook vengono restituiti solo per il team attivo. Per coprire un’organizzazione, esegui il loop dei relativi team e unisci. Gli scenari accettano invece `organizationId`. Consulta le [specifiche API di Fusion v3](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics).


## `aio` errori

* **`aio: command not found`:** CLI non installato o non installato nel PERCORSO. Rieseguire `npm install -g @adobe/aio-cli`, quindi aprire un nuovo terminale.
* **La compilazione/distribuzione non riesce in una nuova versione del nodo:** Usa il nodo **18 o 20 LTS**. Veramente nuove, versioni non LTS a volte rompono la toolchain.
* **&quot;Non sei uno sviluppatore&quot; / impossibile visualizzare l&#39;organizzazione:** L&#39;amministratore dell&#39;organizzazione di Adobe deve concederti il ruolo **Sviluppatore** e l&#39;accesso ad App Builder. Per ulteriori informazioni, vedere [Configurare gli strumenti e l&#39;account dell&#39;estensione dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
* **401 / token non valido durante la distribuzione o l&#39;individuazione:** La sessione è scaduta o si stanno combinando ambienti. Eseguire `aio logout`, quindi `aio login`, confermare `aio console where` e distribuire nell&#39;area di lavoro che si sta caricando.

## Raccolta di informazioni per il supporto

Raccogli queste informazioni per velocizzare la diagnosi:

* Comando esatto eseguito e output dell&#39;errore **full**.
* Il tuo **ID organizzazione IMS**, **progetto** e **area di lavoro**.
* Il **punto di estensione** di cui stai eseguendo il targeting.
* Indica se `aio app deploy` ha avuto esito positivo e se l&#39;estensione è **published** (oppure, per un test di staging, se l&#39;opzione Estensioni di staging è attivata).
* Eventuali errori nel browser **Console** (F12) all&#39;apertura del pannello in Fusion.
