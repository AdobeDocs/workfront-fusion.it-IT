---
title: Moduli AWS S3
description: I moduli S3 di  [!DNL Adobe Workfront Fusion AWS] ti consentono di eseguire operazioni sui bucket S3.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%

---

# Moduli AWS S3

I moduli S3 di [!DNL Adobe Workfront Fusion AWS] consentono di eseguire operazioni sui bucket S3.

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

Per utilizzare i moduli [!UICONTROL AWS S3], è necessario disporre di un account [!DNL Amazon Web Service].

## Informazioni sull’API di AWS S3

Il connettore AWS S3 utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://s3.{{parameters.region}}.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL AWS] a [!DNL Workfront Fusion] {#connect-aws-to-workfront-fusion}

Per connettere [!DNL AWS S3] a [!DNL Workfront Fusion] è necessario connettere l&#39;account [!DNL AWS] a [!DNL Workfront Fusion]. Per eseguire questa operazione, è innanzitutto necessario creare un utente API in [!DNL AWS] [!UICONTROL IAM].

1. Accedi al tuo account [!DNL AWS] [!UICONTROL IAM].
1. Passa a **[!UICONTROL Identity and Access Management]** > **[!UICONTROL Access Management]** > **[!UICONTROL Users]**.

1. Fare clic su **[!UICONTROL Add User]**.
1. Immettere il nome del nuovo utente e selezionare l&#39;opzione **[!UICONTROL Programmatic access]** nella sezione [!UICONTROL Access type].
1. Fare clic su **[!UICONTROL Attach existing policies directly]**, quindi cercare **[!UICONTROL AmazonS3FullAccess]** nella barra di ricerca. Fare clic su di esso quando viene visualizzato, quindi fare clic su **[!UICONTROL Next]**.

1. Passare alle altre finestre di dialogo, quindi fare clic su **[!UICONTROL Create User]**.
1. Copia **[!UICONTROL Access key ID]** e **[!UICONTROL Secret access key]** forniti.

1. Vai a [!DNL Workfront Fusion] e apri la finestra di dialogo **[!UICONTROL Create a connection]** del modulo [!DNL AWS S3].
1. Immettere [!UICONTROL Access key ID] e [!UICONTROL Secret access key] dal passaggio 7 nei rispettivi campi e fare clic su **[!UICONTROL Continue]** per stabilire la connessione.

La connessione è stata stabilita. Puoi procedere con la configurazione del modulo.

## [!DNL AWS S3] moduli e relativi campi

Quando configuri [!DNL AWS S3] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL AWS S3], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Ricerche](#searches)

### Azioni

* [[!UICONTROL Create Bucket]](#create-bucket)
* [[!UICONTROL Get File]](#get-file)
* [[!UICONTROL Upload File]](#upload-file)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Create Bucket]

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immetti il nome del nuovo bucket.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get File]

Scarica un file da un bucket.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Seleziona il bucket da cui desideri scaricare il file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Immettere il percorso del file. Esempio: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] (opzionale) </p> </td> 
   <td> <p>Specificare la cartella di destinazione in cui si desidera caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (opzionale)</p> </td> 
   <td> <p> Inserire le intestazioni della richiesta. Le intestazioni disponibili sono disponibili nella documentazione di <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">[!DNL AWS S3] - [!UICONTROL PUT] oggetto</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Per informazioni dettagliate sull&#39;API [!DNL Amazon S3], vedere Introduzione all&#39;API [[!DNL Amazon S3] [!UICONTROL REST]](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>URL Immettere un URL host. Il percorso deve essere relativo a <code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Selezionare il metodo di richiesta [!UICONTROL HTTP] necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] metodi di richiesta in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi un’intestazione di richiesta. Puoi utilizzare le seguenti intestazioni di richiesta comuni. Per ulteriori intestazioni di richiesta fare riferimento alla documentazione API <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3]</a>.</p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Nome intestazione</th> 
       <th> <p> Descrizione</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Lunghezza del messaggio (senza intestazioni) in base alla RFC 2616. Questa intestazione è necessaria per [!UICONTROL PUT] e le operazioni che caricano XML, ad esempio registrazione e ACL.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>Il tipo di contenuto della risorsa, nel caso in cui il contenuto della richiesta sia nel corpo. Esempio: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>Il digest MD5 a 128 bit codificato in base a base64 del messaggio (senza le intestazioni) in base alla RFC 1864. Questa intestazione può essere utilizzata come controllo di integrità del messaggio per verificare che i dati siano gli stessi dati inviati originariamente. Sebbene sia facoltativo, si consiglia di utilizzare il meccanismo [!UICONTROL Content-MD5] come controllo di integrità end-to-end. Per ulteriori informazioni sull'autenticazione della richiesta [!UICONTROL REST], passare a Autenticazione <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">[!UICONTROL REST]</a> nella Guida per gli sviluppatori del servizio di archiviazione semplice <i>[!DNL Amazon]</i>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>Data e ora correnti in base al richiedente. Esempio: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Quando si specifica l'intestazione <code>Authorization </code>, è necessario specificare l'intestazione <code>x-amz-date</code> o <code>Date </code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>Quando l'applicazione utilizza [!UICONTROL 100-continue], non invia il corpo della richiesta fino a quando non riceve una conferma. Se il messaggio viene rifiutato in base alle intestazioni, il corpo del messaggio non viene inviato. Questa intestazione può essere utilizzata solo se invii un corpo.</p> <p>Valori validi: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Per le richieste di tipo percorso, il valore è <code>s3.amazonaws.com</code>. Per le richieste in stile virtuale, il valore è <code>BucketName.s3.amazonaws.com</code>. Per ulteriori informazioni, vedere <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Virtual Hosting</a> nella <i>[!DNL Amazon] Simple Storage Service Developer Guide</i>.</p> <p>Questa intestazione è obbligatoria per HTTP 1.1 (la maggior parte dei toolkit aggiunge questa intestazione automaticamente); facoltativa per le richieste HTTP/1.0.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Quando si utilizza la firma versione 4 per autenticare la richiesta, questa intestazione fornisce un hash del payload della richiesta. Quando si carica un oggetto in blocchi, impostare il valore su <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> per indicare che la firma copre solo le intestazioni e che non è presente alcun payload. Per ulteriori informazioni, vedere <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Calcoli della firma per l'intestazione di autorizzazione: trasferimento del payload in più blocchi (caricamento a blocchi) ([!DNL AWS] firma versione 4)</a>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>Data e ora correnti in base al richiedente. Esempio: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Quando si specifica l'intestazione <code>Authorization </code>, è necessario specificare l'intestazione <code>x-amz-date</code> o <code>Date </code>. Se si specificano entrambi, il valore specificato per l'intestazione <code>x-amz-date</code> ha la precedenza.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Questa intestazione può essere utilizzata nei seguenti scenari:</p> 
        <ul> 
         <li>Fornire token di sicurezza per le operazioni [!DNL Amazon DevPay]. Ogni richiesta che utilizza [!DNL Amazon DevPay] richiede due intestazioni <code>x-amz-security-token</code>: una per il token di prodotto e una per il token utente. Quando [!DNL Amazon S3] riceve una richiesta autenticata, confronta la firma calcolata con la firma fornita. Le intestazioni con più valori formattate in modo non corretto utilizzate per calcolare una firma possono causare problemi di autenticazione.</li> 
         <li>Fornisci un token di sicurezza quando utilizzi credenziali di sicurezza temporanee. Quando effettui richieste utilizzando le credenziali di sicurezza temporanee ottenute da IAM, devi fornire un token di sicurezza utilizzando questa intestazione. Per ulteriori informazioni sulle credenziali di sicurezza temporanee, vedere Creazione di richieste.</li> 
        </ul> <p>Questa intestazione è necessaria per le richieste che utilizzano [!DNL Amazon DevPay] e per le richieste firmate utilizzando credenziali di sicurezza temporanee.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Aggiungi le stringhe di query desiderate, ad esempio parametri o campi modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:   <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL List Files]](#list-files)
* [[!UICONTROL List Folders]](#list-folders)

#### [!UICONTROL List Files]

Restituisce un elenco di file da una posizione specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selezionare il bucket [!DNL Amazon S3] in cui cercare i file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (opzionale)</p> </td> 
   <td> <p> Percorso di una cartella in cui cercare i file, ad esempio <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Folders]

Restituisce un elenco di cartelle da una posizione specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL AWS] a [!DNL Workfront Fusion], vedere <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL AWS] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta la discussione di <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html">endpoint regionali</a> nella documentazione di AWS.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selezionare il bucket [!DNL Amazon S3] in cui si desidera cercare le cartelle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (opzionale)</p> </td> 
   <td> <p> Percorso di una cartella in cui cercare le cartelle, ad esempio <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>