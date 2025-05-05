---
title: Servizi Adobe PDF
description: Servizi Adobe PDF
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '4125'
ht-degree: 0%

---

# [!DNL Adobe PDF Services]

Con [!DNL Adobe Workfront Fusion] [!DNL Adobe PDF Services] è possibile estrarre dati da un file PDF o generare un nuovo file PDF dai dati forniti. Inoltre, è possibile convertire diversi tipi di file in PDF o PDF in altri tipi di file. I servizi PDF consentono inoltre di combinare, comprimere o leggere i metadati di un file PDF e di controllare la protezione tramite password del file.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

Per informazioni sull&#39;API utilizzata per i servizi PDF, vedere [Adobe Document Generation API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Considerazioni sulla sicurezza durante l&#39;utilizzo di [!DNL Adobe PDF Services]

[!DNL Adobe PDF Services] può leggere, convertire o modificare i tuoi file, ma né [!DNL Adobe] né [!DNL Workfront Fusion] memorizzano i tuoi file o dati. Ciò significa che:

* L&#39;utente mantiene il controllo dei file, inclusa la protezione
* Non è necessario disporre di un account di archiviazione [!UICONTROL Adobe] o di un account di archiviazione cloud per utilizzare i servizi PDF.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per creare una connessione server-to-server OAuth, devi aggiungere l’API dei servizi Adobe PDF nella console per sviluppatori di Adobe. Quando aggiungi l’API, seleziona l’opzione OAuth Server-to-Server.

Per istruzioni, consulta [Aggiungere API al progetto utilizzando OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/) Nella documentazione per gli sviluppatori di Adobe.

## Informazioni API dei servizi Adobe PDF

Il connettore Adobe PDF Services utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Crea una connessione a [!DNL Adobe PDF Services]

Per creare una connessione per i moduli [!DNL Adobe PDF Services]:

1. In qualsiasi modulo di [!DNL Adobe PDF Services], fare clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo di connessione]</td>
          <td>
            <p>Seleziona se desideri creare una connessione server-to-server o JWT.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome connessione]</td>
          <td>
            <p>Immettere un nome per la connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]</td>
          <td>Immetti l'ID client [!DNL Adobe] . È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segreto client]</td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Technical account ID] (solo JWT)</td>
          <td>Immetti l'ID account tecnico [!DNL Adobe] . È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organization ID] (solo JWT)</td>
          <td>Immetti l'ID organizzazione [!DNL Adobe] . È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta ambiti] (solo JWT)</td>
          <td>
            Immetti i meta-ambiti necessari per la connessione.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Chiave privata]</td>
        <td>
          <p>Se hai selezionato una connessione JWT, immetti la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fare clic su <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selezionare il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Immettere la password per il file.</p>
            </li>
            <li value="5">
              <p>Fare clic su <b>[!UICONTROL Salva]</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## [!DNL Adobe PDF Services] moduli e relativi campi

Quando configuri [!DNL PDF Services], [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combina file PDF]](#combine-pdf-files)
* [[!UICONTROL Comprimi file PDF]](#compress-pdf-files)
* [[!UICONTROL Converti documento in file PDF]](#convert-document-to-pdf-file)
* [[!UICONTROL Converti HTML in file PDF]](#convert-html-to-pdf-file)
* [[!UICONTROL Converti immagine in file PDF]](#convert-image-to-pdf-file)
* [[!UICONTROL Converti PDF in documento]](#convert-pdf-to-document)
* [[!UICONTROL Converti PDF in immagine]](#convert-pdf-to-image)
* [[!UICONTROL Estrai testo/tabella]](#extract-text--table)
* [[!UICONTROL Genera documento]](#generate-document)
* [[!UICONTROL Linearizzare un file PDF]](#linearize-a-pdf-file)
* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [[!UICONTROL OCR per file PDF]](#ocr-for-pdf-file)
* [[!UICONTROL Manipolazione pagina]](#page-manipulation)
* [[!UICONTROL Tag automatico di accessibilità PDF]](#pdf-accessibility-auto-tag)
* [[!UICONTROL Proprietà file PDF]](#pdf-file-properties)
* [[!UICONTROL Proteggi file PDF]](#protect-pdf-file)
* [[!UICONTROL Rimuovere la protezione di un file PDF]](#remove-protection-of-a-pdf-file)
* [Dividere un file PDF](#split-a-pdf-file)

### [!UICONTROL Combina file PDF]

Questo modulo di azione raccoglie più file PDF e li combina in un unico file PDF. Questo modulo potrebbe ad esempio combinare tutti i documenti di un progetto [!UICONTROL Workfront] in un unico PDF al completamento del progetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documenti]</td> 
   <td> <p>È possibile utilizzare un modulo di aggregazione per raccogliere i documenti da combinare in un PDF oppure aggiungere i documenti manualmente. </p> <p>È consigliabile utilizzare un modulo [!UICONTROL Array Aggregator] per aggregare l'output di un modulo precedente. Utilizzando un aggregatore, non è necessario conoscere i nomi, le posizioni o i numeri dei file da combinare. L'utilizzo di un aggregatore è quindi molto più flessibile e scalabile rispetto all'immissione manuale dei documenti da combinare.</p> <p>Per utilizzare il modulo dei file [!UICONTROL Combine PDF] con un aggregatore, è necessario abilitare la mappatura nel campo [!UICONTROL Documents]. </p> <p>In questo esempio, il modulo [!UICONTROL Read Related Records] identifica i documenti associati a un progetto e il modulo [!UICONTROL Download Documents] scarica ciascuno di essi. Tutti i PDF vengono aggregati in un array, che viene trasmesso nel modulo dei file [!UICONTROL Combine PDF].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>È inoltre possibile immettere i documenti manualmente.</p> <p>Per ogni documento da includere nel PDF combinato:</p> 
    <ol> 
     <li value="1"> <p>Fare clic su [!UICONTROL Aggiungi documento]</p> </li> 
     <li value="2"> <p>Nel campo [!UICONTROL Source file], selezionare il modulo che restituisce il documento che si desidera includere o mappare il nome e i dati del file di origine. </p> </li> 
     <li value="3"> <p>(Facoltativo) Se si desidera includere solo determinate pagine del file di origine, per ogni intervallo di pagine che si desidera aggiungere fare clic su <strong>[!UICONTROL Add item]</strong> nel campo [!UICONTROL Pages], quindi immettere la prima e l'ultima pagina dell'intervallo di pagine da includere e fare clic su <strong>[!UICONTROL Add]</strong>. È possibile includere più intervalli di pagine da un singolo documento.</p> </li> 
     <li value="4"> <p>Fare clic su <strong>[!UICONTROL Add]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Comprimi file PDF]

Questo modulo di azione accetta un file PDF e lo comprime. Questo può essere utile per conservare la larghezza di banda o la memoria.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Livello di compressione]</td> 
   <td>Selezionare il livello di compressione che si desidera utilizzare.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti documento in file PDF]

Questo strumento converte un documento in un file PDF. Il file di origine deve essere in uno dei seguenti formati di documento:

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in uno dei seguenti formati:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Selezionare la lingua predefinita per il documento di origine. Questo consente al modulo di selezionare un font appropriato, se non è incluso nel file di origine.</p> <p>Seleziona una delle seguenti lingue:</p> 
    <ul> 
     <li> <p>en-US (predefinito): Inglese (Stati Uniti d’America)</p> </li> 
     <li> <p>ca-ES: Catalano (Spagna)</p> </li> 
     <li> <p>cs-CZ: Ceco (Repubblica ceca)</p> </li> 
     <li> <p>da-DK: Danese (Danimarca)</p> </li> 
     <li> <p>de-DE: Tedesco (Germania)</p> </li> 
     <li> <p>en-AE: Inglese (Emirati Arabi Uniti)</p> </li> 
     <li> <p>en-GB: Inglese (Regno Unito)</p> </li> 
     <li> <p>en-IL: Inglese (Israele)</p> </li> 
     <li> <p>en-US: Inglese (Stati Uniti d’America)</p> </li> 
     <li> <p>es-ES: Spagnolo (Spagna)</p> </li> 
     <li> <p>es-MX: Spagnolo (Messico)</p> </li> 
     <li> <p>eu-ES: Basco (Spagna)</p> </li> 
     <li> <p>FI-FI: Finlandese (Finlandia)</p> </li> 
     <li> <p>fr-CA: Francese (Canada)</p> </li> 
     <li> <p>fr-FR: francese (Francia)</p> </li> 
     <li> <p>fr-MA: Francese (Marocco)</p> </li> 
     <li> <p>hr-HR: croato (Croazia)</p> </li> 
     <li> <p>hu-HU: Ungherese (Ungheria)</p> </li> 
     <li> <p>it-IT: Italiano (Italia)</p> </li> 
     <li> <p>ja-JP: Giapponese (Giappone)</p> </li> 
     <li> <p>kr-KR: Coreano (Corea del Sud)</p> </li> 
     <li> <p>nb-NO: Bokmål norvegese (Norvegia)</p> </li> 
     <li> <p>nl-NL: Olandese (Paesi Bassi)</p> </li> 
     <li> <p>pl-PL: Polacco (Polonia)</p> </li> 
     <li> <p>pt-BR: Portoghese (Brasile)</p> </li> 
     <li> <p>pt-PT: Portoghese (Portogallo)</p> </li> 
     <li> <p>ro-RO: rumeno (Romania)</p> </li> 
     <li> <p>ru-RU: Russo (Russia)</p> </li> 
     <li> <p>sk-SK: Slovacco (Slovacchia)</p> </li> 
     <li> <p>sl-SI: Sloveno (Slovenia)</p> </li> 
     <li> <p>sv-SE: Svedese (Svezia)</p> </li> 
     <li> <p>tr-TR: Turco (Turchia)</p> </li> 
     <li> <p>uk-UA: Ucraino (Ucraina)</p> </li> 
     <li> <p>zh-CN: Cinese (Cina continentale)</p> </li> 
     <li> <p>zh-TW: Cinese (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti HTML in file PDF]

Questo strumento converte un file HTML in un file PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Importante: il file Source deve essere in formato HTML o ZIP. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Se il HTML fa riferimento a variabili di JavaScript, puoi includerle qui. </p> <p>Per ogni variabile, fare clic su <strong>[!UICONTROL Add item]</strong> e includere la chiave e il valore della variabile.</p> <p>Nota:   
     <ul> 
      <li> <p>Durante la creazione di un PDF da un file ZIP, il materiale collaterale di origine deve includere un elemento script come: <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>Quando si crea un PDF da un URL, il contenuto di questo oggetto JSON viene inserito nella VM del browser prima che venga eseguito il rendering della pagina. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Includi intestazione e piè di pagina]</td> 
   <td> <p>Abilitare questa opzione per creare intestazioni e piè di pagina per il documento PDF.</p> 
    <ul> 
     <li> <p>L'intestazione include una data e il titolo del documento.</p> </li> 
     <li> <p>Il piè di pagina include il nome del file e un numero di pagina.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Larghezza pagina]</td> 
   <td>Immettere la larghezza del foglio, in pollici. Il modulo utilizza queste informazioni per formattare le pagine nel file PDF creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altezza pagina]</td> 
   <td>Immettere l'altezza della carta, in pollici. Il modulo utilizza queste informazioni per formattare le pagine nel file PDF creato.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti immagine in file PDF]

Questo strumento converte un&#39;immagine in un file PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionate un file di origine da un modulo precedente o mappate il nome e il file di immagine del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti PDF in documento]

Questo strumento converte un file PDF in un documento. È possibile selezionare uno dei seguenti formati per il file di output.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato file di output]</td> 
   <td> <p>Selezionare il formato che si desidera venga utilizzato come output dei file:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Selezionare la lingua predefinita per il documento di origine. Questo consente al modulo di selezionare un font appropriato, se non è incluso nel file di origine.</p> <p>Seleziona una delle seguenti lingue:</p> 
    <ul> 
     <li> <p>en-US (predefinito): Inglese (Stati Uniti d’America)</p> </li> 
     <li> <p>ca-ES: Catalano (Spagna)</p> </li> 
     <li> <p>cs-CZ: Ceco (Repubblica ceca)</p> </li> 
     <li> <p>da-DK: Danese (Danimarca)</p> </li> 
     <li> <p>de-DE: Tedesco (Germania)</p> </li> 
     <li> <p>en-AE: Inglese (Emirati Arabi Uniti)</p> </li> 
     <li> <p>en-GB: Inglese (Regno Unito)</p> </li> 
     <li> <p>en-IL: Inglese (Israele)</p> </li> 
     <li> <p>en-US: Inglese (Stati Uniti d’America)</p> </li> 
     <li> <p>es-ES: Spagnolo (Spagna)</p> </li> 
     <li> <p>es-MX: Spagnolo (Messico)</p> </li> 
     <li> <p>eu-ES: Basco (Spagna)</p> </li> 
     <li> <p>FI-FI: Finlandese (Finlandia)</p> </li> 
     <li> <p>fr-CA: Francese (Canada)</p> </li> 
     <li> <p>fr-FR: francese (Francia)</p> </li> 
     <li> <p>fr-MA: Francese (Marocco)</p> </li> 
     <li> <p>hr-HR: croato (Croazia)</p> </li> 
     <li> <p>hu-HU: Ungherese (Ungheria)</p> </li> 
     <li> <p>it-IT: Italiano (Italia)</p> </li> 
     <li> <p>ja-JP: Giapponese (Giappone)</p> </li> 
     <li> <p>kr-KR: Coreano (Corea del Sud)</p> </li> 
     <li> <p>nb-NO: Bokmål norvegese (Norvegia)</p> </li> 
     <li> <p>nl-NL: Olandese (Paesi Bassi)</p> </li> 
     <li> <p>pl-PL: Polacco (Polonia)</p> </li> 
     <li> <p>pt-BR: Portoghese (Brasile)</p> </li> 
     <li> <p>pt-PT: Portoghese (Portogallo)</p> </li> 
     <li> <p>ro-RO: rumeno (Romania)</p> </li> 
     <li> <p>ru-RU: Russo (Russia)</p> </li> 
     <li> <p>sk-SK: Slovacco (Slovacchia)</p> </li> 
     <li> <p>sl-SI: Sloveno (Slovenia)</p> </li> 
     <li> <p>sv-SE: Svedese (Svezia)</p> </li> 
     <li> <p>tr-TR: Turco (Turchia)</p> </li> 
     <li> <p>uk-UA: Ucraino (Ucraina)</p> </li> 
     <li> <p>zh-CN: Cinese (Cina continentale)</p> </li> 
     <li> <p>zh-TW: Cinese (Taiwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti PDF in immagine]

Questo strumento converte un PDF in un&#39;immagine in formato PNG o JPEG., che viene quindi trasmessa come elenco o combinata in un file ZIP.

Se viene generato come file ZIP, il PDF viene convertito in un’immagine per pagina e ogni immagine termina con il numero della pagina. I file di immagine vengono quindi combinati in un file ZIP.

Ad esempio, un file denominato &quot;TestFile&quot; con 8 pagine produrrebbe 8 immagini, denominate da &quot;TestFile_1&quot; a &quot;TestFile_8&quot;. L’output del modulo è un file ZIP contenente le 8 immagini.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato file di output]</td> 
   <td> <p>Selezionare il formato che si desidera venga utilizzato come output dei file:</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di output]</td> 
   <td> <p>Seleziona se desideri che i file vengano restituiti come elenco di file o come file ZIP.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL Estrai testo/tabella]

Questo modulo di azione ti consente di estrarre dati da un file PDF. Il modulo restituisce singoli elementi di testo, ad esempio un paragrafo o il testo, in una singola cella di una tabella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elementi che devono essere estratti come JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tabelle]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrarre i rettangoli di selezione?]</td> 
   <td>Abilita questa opzione per estrarre i dati relativi al riquadro del testo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Includere informazioni sullo stile per l'output?]</td> 
   <td>Abilita questa opzione per aggiungere informazioni sullo stile al JSON di output.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Genera documento]

Il modulo [!UICONTROL Genera documento] è un modo potente per creare un PDF che contiene i dati selezionati. È possibile formattarlo utilizzando un modello [!DNL Microsoft Word] o fornendo dati in formato JSON.

Per ulteriori informazioni sulla funzionalità [!UICONTROL [!DNL Adobe PDF Services] Genera documento], vedere la [Panoramica sulla generazione di documenti](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) nella documentazione di [!DNL Adobe Document Services].

* [Utilizza il modulo [!UICONTROL Genera documento] con un [!DNL Microsoft Word] modello](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Usa il modulo [!UICONTROL Genera documento] con JSON](#use-the-generate-document-module-with-json)

#### Utilizza il modulo [!UICONTROL Genera documento] con un modello [!DNL Microsoft Word]


>[!NOTE]
>
>Per informazioni sui modelli di Microsoft Word, vedere [Moduli modello di Microsoft Word](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Non è necessario utilizzare i moduli modello di Microsoft Word per utilizzare un modello di Microsoft Word con il modulo documento Generazione servizi di PDF.


Per utilizzare il modulo [!UICONTROL Genera documento] con un modello [!UICONTROL Microsoft Word], è necessario innanzitutto creare il modello. Per istruzioni, cercare &quot;Crea un modello&quot; nella documentazione di [!DNL Microsoft Office].

Compila i campi del modulo [!UICONTROL Genera documento] come segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine è il modello [!DNL Microsoft Word] utilizzato dal modulo per generare il nuovo PDF.</p> <p>È consigliabile creare un progetto in [!DNL Workfront] per i modelli [!DNL Microsoft Word] utilizzati in [!DNL Workfront Fusion]. È quindi possibile utilizzare il modulo [!DNL Workfront] &gt; [!UICONTROL Download document] per richiamare il modello appropriato nello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato Di Output]</td> 
   <td> <p>Selezionare il formato per il documento generato.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dati per unione]</td> 
   <td> <p>Per ogni tag di valore nel modello che si desidera sostituire con testo, compilare il modulo seguente:</p> 
    <ul> 
     <li> <p>[!UICONTROL Key]</p> <p>Immetti una chiave. Nel modello, la chiave è il testo mostrato nel tag valore. Se ad esempio si desidera inserire del testo nel tag valore <code>&#123;&#123;name&#125;&#125;</code>, immettere <code>name </code> nel campo chiave.</p> </li> 
     <li> <p>Tipo di valore</p> <p>Seleziona se i dati nel campo valore sono un valore, un oggetto o un array di oggetti.</p> </li> 
     <li> <p>Valore </p> <p>Immettere o mappare il testo che si desidera visualizzare nel documento generato al posto del tag value.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Usa il modulo [!UICONTROL Genera documento] con JSON

Per utilizzare il modulo [!UICONTROL Genera documento] con JSON, compila i campi come segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato Di Output]</td> 
   <td> <p>Selezionare il formato per il documento generato.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dati per unione]</td> 
   <td> <p>Per utilizzare JSON in questo modulo, devi abilitare la mappatura in questo campo.</p> <p>Immetti o mappa il JSON da cui generare il documento. </p> <p>Puoi digitare JSON direttamente in questo campo, oppure mappare l’output JSON da un modulo JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearizzare un file PDF]

Questo strumento linearizza un documento PDF per creare un documento PDF ottimizzato per il web. Un documento PDF linearizzato può essere visualizzato pagina per pagina senza dover scaricare l&#39;intero documento.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Effettuare una chiamata API personalizzata

Questa azione invia una richiesta HTTP personalizzata all’API dei servizi PDF.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Immetti un percorso relativo o un URL. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Per ogni campo che desideri aggiungere alla chiamata API, fai clic su <b>Aggiungi elemento</b> e immetti la chiave del campo e il valore facoltativo.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR per file PDF]

Questo strumento esegue il riconoscimento ottico dei caratteri (OCR) su un file e produce un PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Selezionare la lingua del documento.<p>Per le opzioni relative alla lingua, vedere <a href="#convert-document-to-pdf-file" class="MCXref xref" >Converti documento in file PDF</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR type]</td> 
   <td> 
    <ul> 
     <li> <p>Il tipo [!UICONTROL Immagine originale modificata] garantisce che il testo sia ricercabile e selezionabile, ma modifica l'immagine originale durante il processo di pulizia (ad esempio, la disegna) prima di posizionarvi sopra un livello di testo invisibile. Questo tipo rimuove gli artefatti indesiderati e può risultare in un documento più leggibile in alcuni scenari. </p> </li> 
     <li> <p>Anche il tipo [!UICONTROL Immagine originale non modificata] sovrappone un livello di testo ricercabile all'immagine originale, ma in questo caso l'immagine originale rimane invariata. Questo tipo produce la massima fedeltà all'immagine originale.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Manipolazione pagina]

Questo modulo consente di ruotare o eliminare selettivamente le pagine di un documento PDF. È possibile, ad esempio, passare dalla visualizzazione verticale alla visualizzazione orizzontale o rimuovere alcune pagine dal documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> <p>Selezionare l'azione da eseguire sul file.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Elimina]</b> </p> <p>Selezionare questa opzione per eliminare le pagine dal documento.</p><p>Per ogni intervallo di pagine che si desidera eliminare, fare clic su <strong>[!UICONTROL Add]</strong> e quindi immettere la prima e l'ultima pagina dell'intervallo di pagine. </p> <p>Nota:   
     <ul> 
      <li> <p>È possibile utilizzare numeri negativi per eseguire il conteggio dalla fine del documento. L'ultima pagina di un documento è -1, la seconda all'ultima pagina è -2 e così via.</p> </li> 
      <li> <p>Per eliminare una singola pagina, impostare lo stesso numero di pagina come inizio e fine dell'intervallo.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Ruota]</b> </p> <p>Selezionare questa opzione per ruotare le pagine, quindi immettere l'angolo, espresso in gradi in senso orario, che si desidera ruotare le pagine del documento rispetto al relativo orientamento iniziale.</p> <p>Per ruotare da verticale a orizzontale o viceversa, ruotare la pagina di 90 o 270 gradi.</p> <p>Se una pagina è capovolta, ruotarla di 180 gradi.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>Per ogni intervallo di pagine che si desidera eliminare, fare clic su <strong>[!UICONTROL Add]</strong> e quindi immettere la prima e l'ultima pagina dell'intervallo di pagine. </p> <p>Nota:   
     <ul> 
      <li> <p>È possibile utilizzare numeri negativi per eseguire il conteggio dalla fine del documento. L'ultima pagina di un documento è -1, la seconda all'ultima pagina è -2 e così via.</p> </li> 
      <li> <p>Per eliminare una singola pagina, impostare lo stesso numero di pagina come inizio e fine dell'intervallo.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record con cui si desidera lavorare il modulo durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Tag automatico di accessibilità PDF]

Questo modulo di azione crea un PDF a cui vengono assegnati tag per i casi di utilizzo di accessibilità. Viene inoltre creato un report Microsoft Excel facoltativo che elenca i problemi e suggerisce le correzioni.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni MAIUSC]</td> 
   <td> <p>Abilitare questa opzione per spostare le intestazioni sul documento.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Genera report]</td> 
   <td> <p>Abilita questa opzione per generare un rapporto che elenca i problemi di accessibilità in PDF insieme alla loro posizione e fornisce suggerimenti su come risolverli.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Proprietà file PDF]

Questo strumento estrae informazioni di base sul documento, ad esempio:

* Conteggio pagine
* Versione PDF
* Se il file è crittografato
* Se il file è linerizzato
* Se il file contiene file incorporati

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Proteggere un file PDF]

Questo strumento protegge un documento PDF con una password utente o proprietario. Inoltre, imposta restrizioni su alcune funzioni quali la stampa, la modifica e la copia nel documento di PDF. È possibile selezionare il tipo di contenuto da crittografare e l&#39;algoritmo di crittografia.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password Protection Type]</td> 
   <td> <p>Abilita questa opzione per utilizzare le password per crittografare il documento PDF di input. Se si abilita questa opzione, è necessario specificare e immettere un valore per uno o entrambi i seguenti elementi: </p> 
    <ul> 
     <li> <p>[!UICONTROL Password Utente]</p> </li> 
     <li> <p>Password proprietario  </p> </li> 
    </ul> <p>Ogni password può contenere fino a 128 caratteri.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encryption Algorithm]</td> 
   <td> <p>Selezionare l'algoritmo di crittografia. </p> 
    <ul> 
     <li> <p>[!UICONTROL Codifica AES-128]</p> <p>La password supporta solo caratteri LATIN-I. </p> </li> 
     <li> <p>[!UICONTROL Codifica AES-256]</p> <p>La password supporta il set di caratteri Unicode</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto da crittografare]</td> 
   <td> <p>Selezionare il tipo di contenuto da crittografare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Tutto il contenuto]</p> </li> 
     <li> <p>[!UICONTROL Tutti i contenuti tranne i metadati]</p> </li> 
     <li> <p>[!UICONTROL Solo dati incorporati] </p> </li> 
    </ul> <p>Selezionando "[!UICONTROL Only embedded data]" le autorizzazioni di accesso fornite diventano inefficaci.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permissions]</td> 
   <td> <p>Selezionare le autorizzazioni da includere per consentire la stampa, la modifica o la copia del contenuto.</p> <p>Le impostazioni delle autorizzazioni vengono utilizzate solo se la password del proprietario  è impostata nel campo [!UICONTROL Password Protection Type].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Rimuovere la protezione di un file PDF]

Questo strumento rimuove la protezione (protezione tramite password) da un documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>Immettere la password che attualmente protegge il file.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dividi un file PDF]

Questo modulo di azione suddivide un documento PDF in più documenti più piccoli. È possibile specificare se dividerlo per numero di file, pagine per file o intervalli di pagine.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], vedere <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split option]</td> 
   <td>Selezionare la modalità di divisione del file. 
   <ul>
   <li><p><b>Intervalli di pagine</b></p><p>Per ogni intervallo di pagine che si desidera dividere in un documento separato, fare clic su <b>Aggiungi</b> e immettere la pagina iniziale e la pagina finale.</p></li>
   <li><p><b>Conteggio pagine</b></p><p>Immettere il numero di pagine da includere nei nuovi documenti.</p></li>
   <li><p><b>Account file</b></p><p>Immettere il numero di file di dimensioni uguali in cui si desidera dividere il documento.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

