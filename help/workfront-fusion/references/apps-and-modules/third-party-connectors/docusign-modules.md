---
title: Moduli DocuSign
description: I moduli  [!DNL Adobe Workfront Fusion DocuSign]  ti consentono di monitorare e recuperare lo stato della busta, cercare e recuperare le buste o scaricare e inviare un documento per accedere al tuo account [!DNL DocuSign] .
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%

---

# Moduli DocuSign

I moduli [!DNL Adobe Workfront Fusion] [!DNL DocuSign] consentono di monitorare e recuperare lo stato della busta, cercare e recuperare le buste o scaricare e inviare un documento per l&#39;accesso al proprio account [!DNL DocuSign].

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare i moduli [!DNL DocuSign], è necessario disporre di un account [!DNL DocuSign].

## Informazioni API di DocuSign

Il connettore DocuSign utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL DocuSign] a [!DNL Workfront Fusion] {#connect-docusign-to-workfront-fusion}

Per creare una connessione per i moduli [!DNL DocuSign]:

1. Fare clic su **[!UICONTROL Add]** accanto alla casella [!UICONTROL Connection] quando si inizia la configurazione del primo modulo [!DNL DocuSign].
1. Immetti quanto segue:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Immettere un nome per la nuova connessione [!DNL DocuSign]</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Seleziona se l'account a cui desideri connetterti è un account di produzione o un account demo.</td> 
     </tr> 
    </tbody> 
   </table>

1. Continuare come descritto in [Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md#connect).

## [!DNL DocuSign] moduli e relativi campi

Quando configuri [!DNL DocuSign] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL DocuSign], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Azioni](#actions)

### Triggers

#### [!UICONTROL Watch envelopes]

Questo modulo di attivazione avvia uno scenario in cui una busta viene inviata, consegnata, firmata, completata o rifiutata.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente i record che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Seleziona il tipo di evento che desideri guardare.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Output fields]</p> </td> 
   <td> <p>Selezionare i campi da includere nell'output del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di record con cui si desidera lavorare il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Add custom field]](#add-custom-field)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Send envelope]](#send-envelope)

#### [!UICONTROL Custom API Call]

Questo modulo di azione ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Immettere o mappare l'account da utilizzare per accedere all'API [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Digita l’indirizzo sul server web con cui desideri che interagisca il modulo.</p> <p>È possibile digitare un URL relativo, il che significa che non è necessario includere il protocollo (ad esempio <code>http://</code>) all'inizio. Questo suggerisce al server web che l’interazione si sta verificando sul server.</p> <p>Ad esempio: <code>[!DNL /api/conversations].create</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> <p>Nota: se ricevi errori ed è difficile determinarne l'origine, puoi modificare le intestazioni in base alla documentazione di [!DNL Workfront]. Se la chiamata API personalizzata restituisce un errore di richiesta HTTP 422, prova a utilizzare un’intestazione "Content-Type":"text/plain".</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di risultati con cui lavorare durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** buste elenco
>
>La chiamata API seguente restituisce le buste dalla data specificata nell&#39;account [!DNL DocuSign]:
>
>**URL**: `/v2.1/accounts/{accountId}/envelopes/`
>
>**Metodo**: `GET`
>
>**Stringa di query**:
>
>* **Chiave**: `from_date`
>
>* **Valore**: `YYYY-MM-DD`
>
>Specifica quando la richiesta inizia il controllo delle modifiche di stato per le buste nell&#39;account.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)
>
>Il risultato si trova nell’Output del modulo in Bundle > Corpo > inviluppi.
>
>Nel nostro esempio, sono state restituite 6 buste:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

#### [!UICONTROL Download a document]

Questo modulo di azione scarica un singolo documento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente il documento che si desidera scaricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Inserisci o mappa l’ID della busta da scaricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Immettere o mappare l'ID del documento da scaricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Selezionare <strong>[!UICONTROL Yes]</strong> se si desidera includere il certificato di firma della busta nel download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Selezionare <strong>[!UICONTROL Yes]</strong> se si desidera consentire ai destinatari di recuperare i documenti in base all'ID utente. Ad esempio, se un utente è incluso in due ordini di instradamento diversi con visibilità diversa, l'utilizzo di questa opzione restituisce tutti i documenti di entrambi i cicli.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Selezionare <strong>[!UICONTROL Yes]</strong> se si desidera che i byte dei PDF restituiti nella risposta siano crittografati per tutti i gestori di chiavi configurati nell'account [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Seleziona la lingua.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Se è impostato su <strong>[!UICONTROL Yes]</strong>, tutti i campi modificati per il PDF restituito sono evidenziati in giallo e le firme o le iniziali facoltative sono evidenziate in rosso.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Selezionare <strong>[!UICONTROL No]</strong> per rimuovere la filigrana dai documenti PDF.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

Questo modulo di azione legge le informazioni su una busta in [!DNL DocuSign] utilizzando l&#39;ID busta.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente il documento da cui si desidera leggere le informazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Immettere o mappare l'ID contenente il documento da cui si desidera leggere le informazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

Questo modulo carica un file specificato in un envelope esistente in DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Seleziona l’account contenente la busta in cui desideri caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Inserisci o mappa l’ID della busta in cui desideri caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o immettere il nome e i dati del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

Questo modulo di azione crea un nuovo envelope da un modello. Restituisce l&#39;ID della nuova busta e lo stato della nuova busta.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>Per istruzioni sulla connessione dell'account DocuSign a Workfront Fusion, vedere gli articoli in <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Seleziona l’account contenente la busta in cui desideri caricare un file.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Selezionate il modello da cui desiderate creare la nuova busta. I modelli sono disponibili in base a [!UICONTROL Account] selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Seleziona se desideri salvare la busta come bozza o inviarla per la firma.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>Seleziona il destinatario della busta</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

Questo modulo di azione aggiunge uno o più destinatari a una busta esistente. Se la busta è già stata inviata, al destinatario viene inviata un’e-mail. Questo modulo non è valido per le buste già completate.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account DocuSign a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Selezionare l'account contenente la busta in cui si desidera aggiungere i destinatari.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Seleziona o mappa l’ID della busta in cui desideri aggiungere il destinatario.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Selezionare il tipo di destinatario da aggiungere alla busta.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Inserisci o mappa l’indirizzo e-mail del destinatario che desideri aggiungere alla busta.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Immettere o mappare il nome del destinatario da aggiungere alla busta.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Inserire o mappare il numero di ciclo per il destinatario. Il numero di indirizzamento determina l'ordine in cui i destinatari ricevono e firmano i documenti.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Inserisci o mappa il corpo (contenuto) dell’e-mail inviata al destinatario.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Inserisci o mappa l’oggetto dell’e-mail inviata al destinatario.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> <li> <p>Solo il destinatario selezionato visualizza il messaggio privato e il messaggio generale. Il messaggio privato può contenere un massimo di 1000 caratteri.</p> </li> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Selezionare il metodo di autenticazione da utilizzare per confermare l'identità del destinatario.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Immetti o mappa il codice di accesso.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Inserisci o mappa il numero di telefono</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Inserisci o mappa il numero di telefono</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add custom field]

Questo modulo di azione aggiunge un campo personalizzato al documento

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente il documento in cui si desidera aggiungere un campo personalizzato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Immettere o mappare l'ID della busta contenente il documento in cui si desidera aggiungere un campo personalizzato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Immettere o mappare un nome per il nuovo campo che si desidera aggiungere.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Abilita questa opzione se desideri che il campo aggiunto sia un campo obbligatorio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Abilita questa opzione se desideri che il campo sia visibile.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Immettere o mappare il valore (contenuto) del campo aggiunto. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

Questo modulo modifica un campo personalizzato utilizzando il nome del campo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente il documento in cui si desidera modificare un campo personalizzato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Immettere o mappare l'ID della busta contenente il documento in cui si desidera modificare un campo personalizzato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Immetti o mappa l’ID del campo da modificare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Immettere o mappare il nome del campo che si desidera modificare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Abilita questa opzione se desideri che il campo modificato sia un campo obbligatorio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Abilita questa opzione se desideri che il campo sia visibile.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Immettere o mappare il valore (contenuto) del campo modificato. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

Questo modulo di azione invia una bozza di busta ai destinatari.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL DocuSign] a [!DNL Workfront Fusion], vedere <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL DocuSign] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selezionare l'account contenente la bozza di busta che si desidera inviare ai destinatari.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Immettete o mappate l'ID della busta 2D da inviare ai destinatari.</p> </td> 
  </tr> 
 </tbody> 
</table>
