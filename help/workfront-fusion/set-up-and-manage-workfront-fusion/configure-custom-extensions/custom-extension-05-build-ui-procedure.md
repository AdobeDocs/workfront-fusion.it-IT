---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Creare l’interfaccia utente dell’estensione personalizzata
description: Creare l’interfaccia utente dell’estensione personalizzata
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 0%

---


# Creare l’interfaccia utente dell’estensione personalizzata

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Questa procedura descrive come creare la schermata che gli utenti visualizzano e completare la connessione **(&quot;handshake&quot;)** con Fusion.

Durante questo processo, è importante ricordare che l&#39;estensione viene eseguita in due frame: il frame **registration** nascosto e il frame **UI** visibile.

Per informazioni sui frame in relazione alle estensioni personalizzate, vedere [Frame inclusi in un&#39;estensione dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

Per istruzioni sulla creazione del frame di registrazione, vedere [Creare un progetto per l&#39;estendibilità dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

## Instradamento tra i due fotogrammi

Entrambi i frame caricano lo stesso `index.html`; un piccolo router front-end decide quale componente mostrare in base all&#39;URL.

1. Impostare le route in `web-src/src/components/App.js`. La parte essenziale è:

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   Questi percorsi vengono mappati alla configurazione precedente come segue:

   * La route predefinita (`index`) esegue il rendering di **`ExtensionRegistration`**, il frame nascosto che chiama `register(...)`.
   * La route `my-widget` esegue il rendering di **`DashboardWidget`**, la tua interfaccia utente visibile. Corrisponde al `url: "/index.html#/my-widget"` restituito da `getWidget()` in [la pagina precedente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

   >[!NOTE]
   >
   > **Le route e l&#39;URL `getWidget` devono essere concordi.** Se si modifica il nome della route, modificare anche `url` oppure Fusion caricherà una pagina vuota.

1. Continua con [Completa l&#39;handshake con `attach`](#complete-the-handshake-with-attach).

## Completa l&#39;handshake con `attach`

Questa è la riga più importante nell’interfaccia utente visibile. Quando Fusion apre il frame dell’interfaccia utente, attende che venga eseguito il check-in del frame. Il codice archivia chiamando `attach({ id })`.

**Se viene omesso, Fusion va in timeout** con un errore come *&quot;in attesa del messaggio iniziale dall&#39;iframe di destinazione.&quot;*

1. Aggiungi quanto segue a `web-src/src/components/DashboardWidget.js`:

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   Questo codice esegue le operazioni seguenti:

   * `attach({ id })` restituisce un **oggetto connessione** dopo che Fusion ha risposto. È consigliabile salvarlo, poiché lo utilizzerai nel passaggio successivo per leggere il contesto inviato da Fusion.
   * Fino a quando la connessione non si risolve, un breve &quot;Collegamento...&quot; viene visualizzato un messaggio.
   * Utilizza **gli stessi`extensionId`** impostati in `Constants.js`.

   A questo punto hai un’estensione di lavoro: registra, allega e mostra un messaggio. Tutto ciò che segue riguarda l’utilizzo dei dati forniti da Fusion.

1. Continua con [Leggi il contesto Condivisioni Fusion](#read-the-context-fusion-shares).

## Leggere il contesto Condivisioni Fusion

Dopo l&#39;associazione, la connessione espone un **contesto condiviso** con informazioni sull&#39;utente, l&#39;organizzazione e il team correnti. È possibile leggere singoli valori con `connection.sharedContext.get("<key>")`:

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

Questo esempio mostra un esempio completo e reattivo che viene aggiornato anche quando l’utente cambia organizzazione o team:

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

Tenere presente quanto segue:

* **Leggi i valori iniziali** da `connection.sharedContext.get(key)` subito dopo `attach`.
* **Iscriviti a`contextchange`** per rimanere sincronizzato. Fusion attiva questo evento ogni volta che l’organizzazione, il team o l’utente attivi cambia. I nuovi valori arrivano il `event.detail.context`.

Per l&#39;elenco completo delle chiavi e del contenuto di ciascuna chiave è incluso nel [Riferimento al contesto di Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Per continuare il processo di configurazione dell&#39;estensione personalizzata, passare a [Riferimento al contesto di Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
