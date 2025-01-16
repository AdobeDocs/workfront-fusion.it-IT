---
title: Connettere Adobe Workfront Fusion a un servizio web che utilizza l’autorizzazione del token API
description: Alcuni servizi non consentono alle soluzioni di integrazione, come Adobe Workfront Fusion, di creare un’app che puoi facilmente utilizzare nel tuo scenario.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 1%

---

# Connettere Adobe Workfront Fusion a un servizio web che utilizza l’autorizzazione del token API

Alcuni servizi non consentono alle soluzioni di integrazione, come Adobe Workfront Fusion, di creare un’app che puoi facilmente utilizzare nel tuo scenario.

Per ovviare a questa situazione, è necessario collegare il servizio desiderato (app) a Workfront Fusion tramite il modulo HTTP > Crea una richiesta.

Questo articolo spiega come connettere quasi tutti i servizi web a Workfront Fusion utilizzando un token API/chiave.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Selezionare o Prime Workfront Plan: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Ultimate Workfront: Workfront Fusion è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Connettersi a un servizio Web che utilizza un token API

La procedura di connessione del servizio tramite un token API è simile per la maggior parte dei servizi web.

1. Creare un&#39;applicazione nel sito Web del servizio Web, come descritto nella sezione [Creare una nuova applicazione e ottenere il token API](#create-a-new-application-and-obtain-the-api-token) in questo articolo.
1. Ottieni la chiave API o il token API.
1. Aggiungi HTTP di Workfront Fusion > Crea un modulo di richiesta al tuo scenario.
1. Configurare il modulo in base alla documentazione API del servizio Web ed eseguire lo scenario, come descritto nella sezione [Configurare il modulo HTTP](#set-up-the-http-module) in questo articolo.

>[!NOTE]
>
>Questo esempio si connette al servizio di notifica push.

## Creare una nuova applicazione e ottenere il token API

>[!NOTE]
>
>Esistono molti modi diversi in cui i servizi web creano e distribuiscono chiavi API o token API. Per istruzioni su come ottenere una chiave API e un token per il servizio web desiderato, visita il sito web del servizio e cerca &quot;Chiave API&quot; o &quot;Token API&quot;.
>
>Stiamo includendo istruzioni per ottenere una chiave API push solo come esempio di ciò che potresti trovare.

1. Accedi al tuo account Pushover.
1. Fai clic su **Crea un token di applicazione/API** nella parte inferiore della pagina.
1. Compila le informazioni sull&#39;applicazione e fai clic su **Crea un&#39;applicazione**.
1. Memorizza il token API fornito in un luogo sicuro. Sarà necessaria per Workfront Fusion HTTP > Creare un modulo di richiesta per connettersi al servizio web desiderato (in questo caso, Pushover).

## Configurare il modulo HTTP

Per collegare un servizio web allo scenario Workfront Fusion, devi utilizzare HTTP > Creare un modulo di richiesta nello scenario e configurarlo in base alla documentazione API del servizio web.

1. Aggiungi HTTP > Crea un modulo di richiesta allo scenario.
1. Per inviare un messaggio push tramite Workfront Fusion, imposta il modulo HTTP come segue.

   >[!NOTE]
   >
   >Queste impostazioni del modulo corrispondono alla documentazione API del servizio web push. Le impostazioni possono essere diverse per altri servizi web. Ad esempio, il token API può essere inserito nell’intestazione e non nel campo Corpo.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>Il campo URL contiene l’endpoint che puoi trovare nella documentazione API del servizio web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Metodo</td> 
      <td> <p><code>POST</code> </p> <p>Il metodo utilizzato dipende dall’endpoint corrispondente. L’endpoint Pushover per la trasmissione dei messaggi utilizza il metodo POST.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Intestazioni</p> </td> 
      <td> <p>Alcuni servizi web possono utilizzare le intestazioni per specificare l’autenticazione del token API o altri parametri. Questo non avviene nel nostro esempio, poiché l’endpoint di push dei messaggi utilizza il corpo (vedi sotto) per tutti i tipi di richiesta.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Stringa di query</p> </td> 
      <td> <p>Alcuni servizi web possono utilizzare una stringa di query per specificare altri parametri. Questo non è il caso nel nostro esempio, in quanto il servizio web push utilizza Body (vedi sotto) per tutti i tipi di richiesta.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Tipo di corpo</p> </td> 
      <td> <p><code>Raw</code> </p> <p>Questa impostazione consente di selezionare il tipo di contenuto JSON nel campo Tipo di contenuto sottostante.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Tipo di contenuto</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON è il tipo di contenuto richiesto dall’app push. Questo può differire da altri servizi web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Richiedi contenuto</p> </td> 
      <td> <p>Immetti il contenuto della richiesta Body in formato JSON. Puoi utilizzare il modulo JSON &gt; Crea JSON come spiegato in <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">Mappare il corpo del JSON utilizzando il modulo JSON &gt; Crea JSON</a> in questo articolo. Oppure puoi immettere il contenuto JSON manualmente, come spiegato in <a href="#enter-the-json-body-manually" class="MCXref xref">Inserisci il corpo JSON manualmente</a> in questo articolo.</p> <p>Per informazioni sui parametri richiesti per il servizio Web, consulta la documentazione API del servizio Web.</p> </td>

   </tr> 
    </tbody> 
   </table>

## Inserisci manualmente il corpo del codice JSON

Specifica parametri e valori nel formato JSON.

>[!BEGINSHADEBOX]

**Esempio:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

Questo esempio include le seguenti informazioni.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> utente</p> </td> 
   <td> <p>USER_KEY. Questo si trova nel dashboard di Pushover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> token </td> 
   <td> <p>Il token API/chiave API generato ha creato l'app Pushover.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> messaggio </td> 
   <td> <p>Il contenuto testuale della notifica push inviata ai dispositivi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> titolo </td> 
   <td> <p>(Facoltativo) Titolo del messaggio. Se non viene immesso alcun valore, viene utilizzato il nome dell’app. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Mappa il corpo del JSON utilizzando il modulo JSON > Crea JSON

Il modulo Crea JSON semplifica la specifica di JSON. Consente inoltre di definire i valori in modo dinamico.

Per ulteriori informazioni sui moduli JSON, vedi [Moduli JSON](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Immetti o mappa i valori da cui desideri creare il JSON.

   ![](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. Connetti il modulo JSON > Crea JSON al modulo HTTP > Crea richiesta.
1. Mappa la stringa JSON dal modulo Crea JSON al campo Contenuto richiesta in HTTP > Crea un modulo di richiesta.

Quando esegui lo scenario, la notifica push viene inviata al dispositivo registrato nel tuo account Pushover.
