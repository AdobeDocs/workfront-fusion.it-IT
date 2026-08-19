---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Creare un progetto per l’estendibilità dell’interfaccia utente
description: Creare un progetto per l’estendibilità dell’interfaccia utente
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
source-wordcount: 1360
ht-degree: 0%

---

# Creare un progetto per l’estendibilità dell’interfaccia utente

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Per creare un’estensione dell’interfaccia utente personalizzata, devi creare un progetto App Builder per essa.

Questa pagina descrive come generare un progetto App Builder generico con la riga di comando `aio`. &quot;Generico&quot; significa che il progetto **non** inizia da un modello specifico per il prodotto. Partendo da un’app generica, il progetto diventa semplice e consente la connessione con Workfront Fusion.

Può essere utile acquisire familiarità con i concetti e la terminologia seguenti per quanto riguarda la creazione di un progetto da utilizzare con l’estensibilità di Adobe Fusion AI.

* **Adobe Developer Console** (<https://developer.adobe.com/console>) è il dashboard Web in cui risiede il progetto.

* **Terminologia**:

  | Termine | Che cosa significa |
  | ------ | --------------- |
  | **Organizzazione** | Organizzazione Adobe della tua azienda. La stessa organizzazione utilizzata in Fusion. |
  | **Progetto** | Contenitore per un&#39;app/estensione. Creerai un progetto per l’estensione. |
  | **Workspace** | Una copia della configurazione del progetto per una fase del lavoro. Ogni progetto ha un&#39;area di lavoro **Produzione** e in genere si utilizza anche un&#39;area di lavoro **Stage** per il test. Pensate alle aree di lavoro come &quot;ambienti&quot;. |
  | **Credenziali / Servizi** | Autorizzazioni che l&#39;app può utilizzare. I valori predefiniti creati sono sufficienti per iniziare. |

* Esistono due modi per creare un progetto:

  * **Automatico (scelta consigliata):** Il comando `aio app init` crea automaticamente il progetto e le aree di lavoro durante la generazione del codice. Questo articolo descrive questo processo.
  * **Manuale:** Il progetto viene creato in Developer Console, quindi viene impostato su `aio`. È consigliabile eseguire questa operazione solo se l’organizzazione richiede la creazione centralizzata dei progetti.

* Quando decidi quale area di lavoro utilizzare, sviluppa e distribuisci prima in **Stage**. Fusion carica una build di staging solo quando l’utente attiva il test di staging nel proprio profilo di Fusion (menu dell’avatar utente > Impostazioni prodotto > Profilo di Fusion > Preferenze > Estensioni di staging); in caso contrario, vengono visualizzate solo le estensioni di produzione pubblicate. Puoi anche visualizzare l&#39;anteprima locale con `aio app run`, quindi passare successivamente a **Produzione**.

  Per ulteriori informazioni sulla promozione in produzione, consulta [Pubblicare la tua estensione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).


## Esegui `aio app init`

1. Apri un terminale.
1. Nel terminale, sposta nella cartella in cui tieni i progetti.
1. Esegui:

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension` è il nome della cartella/app. È possibile selezionare questo nome, ma utilizzare lettere minuscole, trattini e non spazi.
   * `--standalone-app` indica all&#39;interfaccia della riga di comando di creare una **ossatura semplice dell&#39;applicazione** invece di chiedere di scegliere un modello di prodotto. Questa è la chiave per evitare il modello AEM (o qualsiasi altro).

1. Quando richiesto, **seleziona la tua organizzazione** (se appartieni a più organizzazioni).
1. Quando richiesto, selezionare **Crea nuovo progetto** e accettare il nome suggerito oppure scegliere un progetto vuoto esistente.

   Il comando imposta automaticamente le aree di lavoro **Stage** e **Produzione**.

   Il comando genera anche file nella cartella `my-fusion-extension` ed esegue `npm install`.

1. Continua con [Conferma creazione progetto](#confirm-project-creation).

>[!NOTE]
>
> **Se si preferisce il menu interattivo:** eseguire `aio app init my-fusion-extension` > (senza `--standalone-app`). Quando viene chiesto a **&quot;Quali modelli si desidera cercare?&quot;** o mostra un elenco di controllo di modelli, non selezionare un modello di prodotto come AEM. Scegliere l&#39;opzione per creare una **applicazione autonoma** / **&quot;Tutti i punti di estensione → nessuno&quot;**.

## Verifica creazione progetto

1. Nel terminale, spostarsi nella cartella creata:

   ```sh
   cd my-fusion-extension
   ```

   Dovresti vedere una struttura simile a questa (alcuni file omessi):

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   I due file più importanti sono:

   * **`app.config.yaml`**: configurazione centrale. Successivamente verrà aggiunta una sezione `extensions:` che collega l&#39;app a un punto di estensione di Fusion.
   * **`package.json`**: elenca le librerie utilizzate dall&#39;app. Aggiungere qui la libreria guest di estendibilità dell’interfaccia utente di Adobe.

1. Continua con [Aggiungi librerie richieste](#add-required-libraries).

>[!TIP]
>
> Non preoccuparti se il layout generato è leggermente diverso tra le versioni CLI. Questa procedura indica esattamente quali file creare e cosa inserirvi, in modo da poter corrispondere alla struttura prevista indipendentemente dal punto di partenza.

## Aggiungi librerie richieste

L’estensione richiede due librerie:

* **`@adobe/uix-guest`**: consente all&#39;app di comunicare con Fusion (host).
* **`@adobe/react-spectrum`**: componenti dell&#39;interfaccia utente React di Adobe, in modo che lo schermo corrisponda all&#39;aspetto di Adobe. (Facoltativo ma consigliato; puoi utilizzare al suo posto il HTML normale.)

Per installare queste librerie:

1. Nel terminale, eseguire:

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (Condizionale) Se il progetto generato non include già React, installalo anche:

   ```sh
   npm install react react-dom react-router-dom
   ```

1. Continua con [Conferma le build del progetto](#confirm-the-project-builds).

## Conferma le build del progetto

Prima di modificare qualsiasi elemento, assicurati che le build del progetto vuote vengano

1. Nel terminale, eseguire:

   ```sh
   aio app build
   ```

   Se il completamento avviene senza errori, gli strumenti e il progetto vengono configurati correttamente. È ora possibile collegare il progetto a Fusion.

   >[!TIP]
   >
   > **Se la compilazione non riesce,** la causa più comune è una versione di Node.js non supportata. Eseguire `node --version` e verificare che sia 18 o 20.
   >
   >* Per informazioni sull&#39;installazione di Node.js, consulta [Configurare gli strumenti](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
   >* Per informazioni su altri possibili errori, vedere [Risoluzione dei problemi](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

1. Continua con [Configurare il progetto per Fusion](#configure-the-project-for-fusion).

## Configurare il progetto per Fusion

Il passaggio successivo per configurare l’estensione personalizzata consiste nel collegare il progetto generico a Workfront Fusion.

Effettua le seguenti operazioni:

1. [Creare una cartella per l’estensione](#create-a-folder-for-your-extension)
1. Informare App Builder di un **punto di estensione** di Fusion (in `app.config.yaml`).
1. Descrivi i pezzi dell&#39;estensione (in `ext.config.yaml`).
1. **Registra** il widget in modo che Fusion conosca il titolo e la posizione dell&#39;interfaccia utente.

Utilizziamo `fusion/nav-organization/1` in tutto. Per eseguire il targeting della sezione Team, sostituisci in `fusion/nav-team/1` ovunque. Per supportare entrambi, ripetete il pattern per ciascuno di essi.

## Creare una cartella per l’estensione

1. Crea i file in modo che il progetto sia simile al seguente:

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   È consigliabile denominare la cartella dopo il punto di estensione (`fusion-nav-organization-1`). Il nome esatto dipende da te, ma deve corrispondere a quello a cui si fa riferimento in `app.config.yaml`.

1. Continuare a [Dichiarare il punto di estensione in `app.config.yaml`](#declare-the-extension-point-in-appconfigyaml).

## Dichiara il punto di estensione in `app.config.yaml`

1. Apri `app.config.yaml` e aggiornane il contenuto in:

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   Tali contenuti descrivono quanto segue:

   * `extensions:`: questa app implementa uno o più punti di estensione.
   * `fusion/nav-organization/1`: lo slot Fusion in cui ci si sta collegando. **Il nome deve corrispondere esattamente**, inclusa la versione `1`.
   * `$include:`: questo fa riferimento a un secondo file di configurazione (creato nel passaggio successivo) che descrive il contenuto di questa estensione. Mantenendolo in un file separato, `app.config.yaml` rimane pulito e consente di aggiungere altri punti di estensione in un secondo momento.

   >[!NOTE]
   >
   >Se esegui il targeting di entrambe le estensioni, elenca entrambe, ciascuna con la propria cartella:
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. Continua con [Descrizione dell&#39;estensione in `ext.config.yaml`](#describe-the-extension-in-extconfigyaml)

## Descrizione dell&#39;estensione in `ext.config.yaml`

1. Crea `src/fusion-nav-organization-1/ext.config.yaml` con:

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   Tali contenuti descrivono quanto segue:

   * **`operations.view`**: dichiara che l&#39;estensione fornisce una **visualizzazione** (interfaccia utente visibile), fornita da `index.html`. In questo modo l’estensione viene visualizzata una schermata anziché essere eseguita solo in background.
   * **`web: web-src`**: cartella contenente i file front-end. App Builder crea tutto qui sotto e lo ospita sulla rete CDN (Content Delivery Network) di Adobe.
   * **`hooks`**: piccoli comandi eseguiti automaticamente in fase di compilazione/esecuzione. Lo script `generate-metadata.js` viene fornito con `@adobe/uix-guest` e genera un file `app-metadata.json` necessario per il codice di registrazione (vedere il passaggio 4). Non si scrive questo script, ma si fa semplicemente riferimento ad esso.

   >[!NOTE]
   >
   > Se è necessaria anche una logica lato server, è possibile aggiungere anche `actions` senza server (piccole funzioni di back-end). Le azioni sono facoltative e non sono necessarie per eseguire il rendering di un’interfaccia utente, pertanto non sono necessarie per mantenere attiva questa guida. Se li aggiungi in un secondo momento, dichiarali una cartella `actions:` qui e una `runtimeManifest:` in `app.config.yaml`. Il motivo più comune per aggiungerne uno è quello di chiamare le API Workfront/Fusion senza premere CORS del browser.
   > Per informazioni sulla chiamata delle API, vedere [Chiamata delle API Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).
1. Continua con [Imposta un ID estensione stabile](#set-a-stable-extension-id).

## Imposta un ID di estensione stabile

L&#39;estensione richiede un ID univoco condiviso da entrambi i fotogrammi.

Per informazioni sui frame in relazione alle estensioni personalizzate, vedere [Frame inclusi in un&#39;estensione dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

1. Crea `src/fusion-nav-organization-1/web-src/src/components/Constants.js`:

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   Utilizza lo stesso valore in tutti i casi in cui il codice fa riferimento all’ID estensione.
1. Continua con [Registra widget](#register-your-widget).


## Registra il widget

Con &quot;Registrazione&quot; si intende il modo in cui il frame di sfondo nascosto comunica a Fusion le offerte della tua estensione. Dichiara un metodo `dashboard.getWidget()` che restituisce il titolo del widget e l&#39;URL della relativa interfaccia utente visibile.

1. Crea `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js`.
La parte importante è la chiamata `register(...)`:

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   Punti chiave:

   * **`title`** è l&#39;etichetta inserita da Fusion sul pulsante di navigazione. Se `hideWidgetHeader` è `false`, Fusion mostrerà anche il titolo come intestazione sopra l&#39;interfaccia utente.
   * **`url`** è il percorso per l&#39;interfaccia utente di *visible* all&#39;interno della stessa app. Questa è una route hash (`#/my-widget`) gestita dal router front-end (configurato nella pagina successiva). Deve risolversi nel componente che esegue il rendering dello schermo.
   * **`metadata`** proviene da `app-metadata.json`, che l&#39;hook `generate-metadata` crea automaticamente in fase di compilazione. Importa come mostrato.
   * Il nome del metodo `dashboard.getWidget` è il contratto concordato con le chiamate Fusion per l&#39;individuazione del widget. Mantieni lo spazio dei nomi `dashboard` e il nome `getWidget`.

Il backend dell’estensione è ora completo. Il passaggio successivo per creare l’interfaccia utente dell’estensione.

Per istruzioni sulla creazione dell&#39;interfaccia utente, vedere [Creare l&#39;interfaccia utente dell&#39;estensione personalizzata](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
