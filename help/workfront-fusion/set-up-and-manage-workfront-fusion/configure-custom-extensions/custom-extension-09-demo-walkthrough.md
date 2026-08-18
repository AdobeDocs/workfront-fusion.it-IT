---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Procedura dettagliata per la dimostrazione di un’estensione personalizzata
description: Procedura dettagliata per la dimostrazione di un’estensione personalizzata
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 0%

---


# Procedura dettagliata sulla dimostrazione della creazione di un’estensione personalizzata in Fusion

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Questa demo illustra come creare un’estensione personalizzata, distribuirla ed eseguirla in Fusion.

Include:

* Scaffolda un’app App Builder dal modello generico Experience Cloud Shell.
* Esegui il retargeting dell’app per un punto di estensione di Fusion.
* Distribuisci l’app nell’area di lavoro dello stage.
* Attiva i test dello staging in Fusion e mostra l’app in esecuzione.

Partendo dal modello anziché da un `--standalone-app` vuoto, il bootstrap dell&#39;applicazione a pagina singola viene generato automaticamente: `index.js`, `exc-runtime.js`, `App.js` con routing e `ErrorBoundary` e un esempio di `ExtensionRegistration`. I passaggi live nella demo consistono nel retargeting della configurazione e nella modifica di due file, che è esattamente il modo in cui è stato creato l&#39;effettivo `fusion-uix-guest`.

>[!NOTE]
>
> **Tempo:** La demo live richiede circa 10 minuti dopo la configurazione degli strumenti. È necessario eseguire l&#39;installazione una tantum (Nodo 18/20, `aio` CLI, `aio login`) **prima** della demo. Per istruzioni, consulta [Configurare gli strumenti e l&#39;account dell&#39;estensione dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


## Prima di iniziare

Questa operazione deve essere eseguita una sola volta e può essere eseguita off-camera prima della dimostrazione.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

Nell’organizzazione demo devono essere vere due cose:

* Il punto di estensione `fusion/nav-organization/1` è integrato nell&#39;organizzazione. Se non è integrato nel processo di onboarding, la distribuzione non riesce e viene visualizzato l’errore 1060. Per ulteriori informazioni, vedere [Risoluzione dei problemi relativi alle estensioni personalizzate](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).
* La funzione di estensione personalizzata è abilitata nell’host Fusion. Questa funzione è attiva per impostazione predefinita. Poiché verrà eseguita una demo di una build di Stage anziché di una pubblicata, verrà attivato anche lo switch **Estensioni di Stage** nel profilo di Fusion. (Questo interruttore è illustrato al punto 7). Fusion mostra solo le estensioni pubblicate fino a quando non lo fai.

## Passaggio 1: generare l’app dal modello generico

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* Selezionare **Crea nuovo progetto** quando richiesto e accettare il nome suggerito.
* `@adobe/generator-app-excshell` è il modello generico di estensione dell&#39;interfaccia utente **Experience Cloud Shell** e non è specifico del prodotto. Scaffolds di un&#39;applicazione a pagina singola completa e funzionante in `src/dx-excshell-1/`.

>[!NOTE]
>
>Se preferisci il menu, esegui `aio app init my-fusion-extension`, scegli **Aggiungi estensioni o app autonoma** > **Modelli** e seleziona **&quot;Estensione App Builder UIX per Experience Cloud Shell&quot;**.

Riceverai un set di file, tra cui:

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## Passaggio 2: aggiungere la libreria guest di Fusion

Il modello include già React, React Spectrum ed exc-app. Aggiungi la libreria che parla con l&#39;host Fusion:

```sh
npm install @adobe/uix-guest
```

## Passaggio 3: ridestinare la configurazione a Fusion

Apri **`app.config.yaml`** e cambia **solo la chiave del punto di estensione** dal punto di Experience Cloud Shell a quello di Fusion (lascia il percorso `$include` immutato):

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

Non è necessario modificare altri elementi nella configurazione. Il nome della cartella `dx-excshell-1` è interno e non influisce su Fusion, pertanto è possibile lasciarlo. Rinominare significherebbe anche aggiornare eventuali percorsi di azione. Saltalo per la demo.

>[!NOTE]
>
>Se esegui il targeting della sezione **Team**, utilizza invece `fusion/nav-team/1`. Per spedire **sia** organizzazione che team in produzione, utilizza **due progetti separati**. Un bundle di punto di estensione per nome di registro evita un conflitto tra app condivise.

## Passaggio 4: modificare i file di registrazione e widget

Tutti i percorsi si trovano in `src/dx-excshell-1/web-src/src/components/`.

### **`ExtensionRegistration.js`**

Il file generato registra un esempio di Experience Cloud Shell. Sostituisci `methods` con il contratto Fusion **`dashboard.getWidget`** in modo che Fusion conosca il tuo titolo e dove si trova l&#39;interfaccia utente:

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

Se `Constants.js` non esiste accanto ad esso, crealo:

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

Crea questo file. Completa l’handshake e mostra il contesto live di Fusion:

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

Il router generato invia già `index` / `index.html` a `ExtensionRegistration`. Aggiungi una route per il widget e importala:

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> Il percorso della route (`widget`) deve corrispondere all&#39;hash in `getWidget().url` (`/index.html#/widget`). Mantieni `index.js` / `exc-runtime.js` generato e il resto di `App.js` esattamente come scaffolded, perché è l&#39;avvio che desideri che il modello fornisca.

## Passaggio 5: generare

```sh
aio app build
```

In questo modo viene compilato il front-end e viene eseguito l&#39;hook dei metadati che genera `app-metadata.json`. Correggi eventuali errori prima di continuare.

## Passaggio 6: distribuisci nell’ambiente di staging

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy` ospita la tua interfaccia utente sulla rete CDN di Adobe e registra l&#39;endpoint dell&#39;estensione nell&#39;area di lavoro di Stage, consentendo a Fusion di individuarlo. CLI stampa l&#39;URL dell&#39;endpoint, ad esempio `https://<project>-stage.adobeio-static.net`.

## Passaggio 7: attivare il test dello staging e visualizzare l’estensione in Fusion

1. Open Fusion su Experience Cloud, ha effettuato l’accesso alla stessa organizzazione in cui è stato implementato.
1. Apri il menu dell&#39;avatar utente e vai a **Impostazioni prodotto** > **Profilo Fusion** > **Preferenze**.
1. Attiva l&#39;opzione **Estensioni stage** e conferma il ricaricamento.

   Fusion ora carica le estensioni dall&#39;area di lavoro dello stage e le contrassegna come **(Stage)**.
1. Vai all&#39;area **Organizzazione** della navigazione a sinistra.

   Verrà visualizzato il pulsante **&quot;My Fusion Tool (Stage)&quot;**.
1. Fare clic sul pulsante **&quot;My Fusion Tool (Stage)&quot;**.
L’interfaccia utente viene caricata nel pannello principale e mostra l’utente, l’organizzazione e il team in tempo reale.
1. **Cambiare organizzazione o team attivo** in Fusion.

   Il pannello viene aggiornato con la dimostrazione del contesto live (`contextchange`).

>[!TIP]
>
>Se il pulsante non viene visualizzato, ricaricalo una volta, perché l’individuazione viene memorizzata nella cache per sessione. Quindi vedi [Risoluzione dei problemi relativi alle estensioni personalizzate](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).


## Iterazione durante la demo

Apporta una modifica, quindi genera e ridistribuisci.  La prossima volta che lo aprono, gli utenti visualizzano l’estensione aggiornata.

```sh
aio app build && aio app deploy
```

## Vai alla produzione dopo la demo

La fase è sufficiente per la dimostrazione. Per rilasciare l’approvazione a livello di organizzazione, passa all’area di lavoro Produzione, distribuisci e invia la richiesta di approvazione. La richiesta deve essere inviata utilizzando il ruolo Amministratore di sistema. Per informazioni sull&#39;intero processo, vedere [Versione in produzione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production).

## Demo talk-track (opzionale)

Durante la demo live potrebbe essere utile effettuare le seguenti operazioni:

* **&quot;Ho iniziato dal modello generico di Experience Cloud Shell.&quot;** Scaffold l&#39;intera shell SPA, quindi ho solo retargeting il punto di estensione e modificato due file.
* **&quot;Fusion è l&#39;host, la mia app è l&#39;ospite.&quot;** Vengono eseguiti in frame separati e parlano con l’interfaccia utente di Adobe Extensibility SDK, senza reti personalizzate.
* **&quot;Registrazione e visualizzazione&quot;** Il frame nascosto *registra* ciò che offro (`dashboard.getWidget`) e il frame visibile *allega* e legge il contesto.
* **&quot;Il test dello staging è un&#39;opzione per utente.&quot;** Per impostazione predefinita, Fusion mostra solo le estensioni pubblicate. Ho attivato le estensioni Stage nel mio profilo Fusion per caricare la build Stage, senza una versione di produzione.
* **&quot;Contesto live.&quot;** Quando si cambia organizzazione o team, viene inviato nuovamente il contesto e viene eseguito il rendering del guest.
