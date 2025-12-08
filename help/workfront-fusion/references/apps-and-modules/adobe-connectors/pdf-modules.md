---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '4151'
ht-degree: 100%

---

# [!DNL Adobe PDF Services]

Con Adobe Workfront Fusion [!DNL Adobe PDF Services] puoi estrarre dati da un file PDF o generarne uno nuovo dai dati che hai fornito. Inoltre puoi convertire diversi tipi di file in PDF o convertire file PDF in altri tipi di file. I servizi PDF ti consentono anche di combinare, comprimere o leggere i metadati di un file PDF e di controllare la protezione del file tramite password.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

Per informazioni sull’API utilizzata per i servizi PDF, consulta [API per generazione documenti Adobe](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Considerazioni sulla sicurezza durante l’utilizzo di [!DNL Adobe PDF Services]

[!DNL Adobe PDF Services] può leggere, convertire o modificare i tuoi file, ma né [!DNL Adobe] né Workfront Fusion archivano i tuoi file o i tuoi dati. Questo significa che:

* Mantieni il controllo dei tuoi file, inclusa la sicurezza.
* Per utilizzare i servizi PDF non è necessario disporre di un account di archiviazione o di archiviazione cloud di [!UICONTROL Adobe].

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni di questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per creare una connessione OAuth da server a server, devi aggiungere l’API Adobe PDF Services in Adobe Developer Console. Quando aggiungi l’API, seleziona l’opzione Da server a server OAuth.

Per istruzioni, consulta [Aggiungere API al progetto utilizzando le credenziali di autenticazione utente OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication) nella documentazione per gli sviluppatori di Adobe.

## Informazioni sull’API Adobe PDF Services

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

## Creare una connessione ad [!DNL Adobe PDF Services]

Per creare una connessione per i moduli [!DNL Adobe PDF Services]:

1. In qualsiasi modulo di [!DNL Adobe PDF Services], fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
          <td>
            <p>Seleziona se creare una connessione da server a server o una connessione JWT.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
          <td>
            <p>Specifica un nome per questa connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]</td>
          <td>Inserisci il tuo [!UICONTROL ID client] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
          <td>Inserisci il tuo [!UICONTROL Segreto client] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID account tecnico] (solo JWT)</td>
          <td>Inserisci il tuo [!UICONTROL ID account tecnico] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID organizzazione] (solo JWT)</td>
          <td>Inserisci il tuo [!UICONTROL ID organizzazione] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Ambinti Meta] (solo JWT)</td>
          <td>
            Inserisci gli ambiti Meta necessari per la connessione.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Chiave privata]</td>
        <td>
          <p>Se hai selezionato una connessione JWT, inserisci la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fai clic su <b>[!UICONTROL Estrai]</b>.</p>
            </li>
            <li value="2">
              <p>Seleziona il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Inserisci la password per il file.</p>
            </li>
            <li value="5">
              <p>Fai clic su <b>[!UICONTROL Salva]</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## Moduli di [!DNL Adobe PDF Services] e relativi campi

Quando esegui la configurazione di [!DNL PDF Services], Workfront Fusion mostra i campi elencati di seguito. Insieme a questi, potrebbero essere mostrati campi aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combina file PDF]](#combine-pdf-files)
* [[!UICONTROL Comprimi file PDF]](#compress-pdf-files)
* [[!UICONTROL Converti documento in file PDF]](#convert-document-to-pdf-file)
* [[!UICONTROL Converti HTML in file PDF]](#convert-html-to-pdf-file)
* [[!UICONTROL Converti immagine in file PDF]](#convert-image-to-pdf-file)
* [[!UICONTROL Converti PDF in documento]](#convert-pdf-to-document)
* [[!UICONTROL Converti PDF in immagine]](#convert-pdf-to-image)
* [[!UICONTROL Estrai testo/tabella]](#extract-text--table)
* [[!UICONTROL Genera documento]](#generate-document)
* [[!UICONTROL Linearizza un file PDF]](#linearize-a-pdf-file)
* [Effettua chiamata API personalizzata](#make-a-custom-api-call)
* [[!UICONTROL OCR per file PDF]](#ocr-for-pdf-file)
* [[!UICONTROL Manipolazione pagina]](#page-manipulation)
* [[!UICONTROL Tag automatico di accessibilità PDF]](#pdf-accessibility-auto-tag)
* [[!UICONTROL Proprietà file PDF]](#pdf-file-properties)
* [[!UICONTROL Proteggi file PDF]](#protect-pdf-file)
* [[!UICONTROL Rimuovi protezione di un file PDF]](#remove-protection-of-a-pdf-file)
* [Dividi un file PDF](#split-a-pdf-file)

### [!UICONTROL Combina file PDF]

Questo modulo di azione raccoglie più file PDF e li combina in un unico file PDF. Questo modulo potrebbe ad esempio combinare tutti i documenti di un progetto [!UICONTROL Workfront] in un unico PDF al termine del progetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documenti]</td> 
   <td> <p>È possibile utilizzare un modulo di aggregazione per raccogliere i documenti da combinare in un PDF oppure aggiungere i documenti manualmente. </p> <p>È consigliabile utilizzare un modulo [!UICONTROL Aggregatore array] per aggregare l’output di un modulo precedente. Utilizzando un aggregatore, non è necessario conoscere i nomi, le posizioni o i numeri dei file da combinare. L’utilizzo di un aggregatore è quindi molto più flessibile e scalabile rispetto all’immissione manuale dei documenti da combinare.</p> <p>Per utilizzare il modulo dei file [!UICONTROL Combina PDF] con un aggregatore, è necessario abilitare la mappatura nel campo [!UICONTROL Documenti]. </p> <p>In questo esempio, il modulo [!UICONTROL Leggi record correlati] identifica i documenti associati a un progetto e il modulo [!UICONTROL Scarica documenti] scarica ciascuno di essi. Tutti i PDF vengono aggregati in un array, che viene trasferito nel modulo dei file [!UICONTROL Combina PDF].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Puoi anche inserire i documenti manualmente.</p> <p>Per ciascun documento da includere nel PDF combinato:</p> 
    <ol> 
     <li value="1"> <p>Fai clic su [!UICONTROL Aggiungi documento]</p> </li> 
     <li value="2"> <p>Nel campo [!UICONTROL File di origine], seleziona il modulo che restituisce il documento che desideri includere oppure mappa il nome e i dati del file di origine. </p> </li> 
     <li value="3"> <p>(Facoltativo) Se desideri includere solo determinate pagine del file di origine, per ogni intervallo di pagine da aggiungere fai clic su <strong>[!UICONTROL Aggiungi elemento]</strong> nel campo [!UICONTROL Pagine], quindi inserisci la prima e l’ultima pagina dell’intervallo di pagine da includere e fai clic su <strong>[!UICONTROL Aggiungi]</strong>. Puoi includere più di un intervallo di pagine da un singolo documento.</p> </li> 
     <li value="4"> <p>Fai clic su <strong>[!UICONTROL Aggiungi]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Comprimi file PDF]

Questo modulo di azione acquisisce un file PDF e lo comprime. Questo può essere utile per conservare la larghezza di banda o la memoria.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Livello di compressione]</td> 
   <td>Seleziona il livello di compressione che desideri utilizzare.</td> 
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
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in uno dei seguenti formati:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lingua]</td> 
   <td> <p>Seleziona la lingua predefinita per il documento di origine. Questo consente al modulo di selezionare un font appropriato, se non è incluso nel file di origine.</p> <p>Seleziona una delle seguenti lingue:</p> 
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
     <li> <p>fi-FI: Finlandese (Finlandia)</p> </li> 
     <li> <p>fr-CA: Francese (Canada)</p> </li> 
     <li> <p>fr-FR: Francese (Francia)</p> </li> 
     <li> <p>fr-MA: Francese (Marocco)</p> </li> 
     <li> <p>hr-HR: Croato (Croazia)</p> </li> 
     <li> <p>hu-HU: Ungherese (Ungheria)</p> </li> 
     <li> <p>it-IT: Italiano (Italia)</p> </li> 
     <li> <p>ja-JP: Giapponese (Giappone)</p> </li> 
     <li> <p>kr-KR: Coreano (Corea del Sud)</p> </li> 
     <li> <p>nb-NO: Bokmål norvegese (Norvegia)</p> </li> 
     <li> <p>nl-NL: Olandese (Paesi Bassi)</p> </li> 
     <li> <p>pl-PL: Polacco (Polonia)</p> </li> 
     <li> <p>pt-BR: Portoghese (Brasile)</p> </li> 
     <li> <p>pt-PT: Portoghese (Portogallo)</p> </li> 
     <li> <p>ro-RO: Rumeno (Romania)</p> </li> 
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
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Importante: il file di origine deve essere in formato HTML o ZIP. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Se il file HTML fa riferimento a variabili di JavaScript, puoi includerle qui. </p> <p>Per ciascuna variabile, fai clic su <strong>[!UICONTROL Aggiungi elemento]</strong> e includi la chiave e il valore della variabile.</p> <p>Nota:   
     <ul> 
      <li> <p>Durante la creazione di un PDF da un file ZIP, il materiale di origine deve includere un elemento script come: <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>Durante la creazione di un PDF da un URL, il contenuto di questo oggetto JSON viene inserito nella macchina virtuale del browser prima che la pagina sia sottoposta a rendering. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Includi intestazione e piè di pagina]</td> 
   <td> <p>Abilita questa opzione per creare intestazioni e piè di pagina per il documento PDF.</p> 
    <ul> 
     <li> <p>L’intestazione include una data e il titolo del documento.</p> </li> 
     <li> <p>Il piè di pagina include il nome del file e un numero di pagina.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Larghezza pagina]</td> 
   <td>Inserisci la larghezza del foglio in pollici. Il modulo utilizza queste informazioni per formattare le pagine nel file PDF creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altezza pagina]</td> 
   <td>Inserisci l’altezza del foglio in pollici. Il modulo utilizza queste informazioni per formattare le pagine nel file PDF creato.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti immagine in file PDF]

Questo strumento converte un’immagine in un file PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e il file di immagine del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Converti PDF in documento]

Questo strumento converte un file PDF in un documento. Puoi selezionare uno dei seguenti formati per il file di output.

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
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato file di output]</td> 
   <td> <p>Seleziona il formato che desideri utilizzare come output dei file:</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lingua]</td> 
   <td> <p>Seleziona la lingua predefinita per il documento di origine. Questo consente al modulo di selezionare un font appropriato, se non è incluso nel file di origine.</p> <p>Seleziona una delle seguenti lingue:</p> 
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
     <li> <p>fi-FI: Finlandese (Finlandia)</p> </li> 
     <li> <p>fr-CA: Francese (Canada)</p> </li> 
     <li> <p>fr-FR: Francese (Francia)</p> </li> 
     <li> <p>fr-MA: Francese (Marocco)</p> </li> 
     <li> <p>hr-HR: Croato (Croazia)</p> </li> 
     <li> <p>hu-HU: Ungherese (Ungheria)</p> </li> 
     <li> <p>it-IT: Italiano (Italia)</p> </li> 
     <li> <p>ja-JP: Giapponese (Giappone)</p> </li> 
     <li> <p>kr-KR: Coreano (Corea del Sud)</p> </li> 
     <li> <p>nb-NO: Bokmål norvegese (Norvegia)</p> </li> 
     <li> <p>nl-NL: Olandese (Paesi Bassi)</p> </li> 
     <li> <p>pl-PL: Polacco (Polonia)</p> </li> 
     <li> <p>pt-BR: Portoghese (Brasile)</p> </li> 
     <li> <p>pt-PT: Portoghese (Portogallo)</p> </li> 
     <li> <p>ro-RO: Rumeno (Romania)</p> </li> 
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

Questo strumento converte un PDF in un’immagine in formato PNG o JPEG., che viene quindi generata come elenco o combinata in un file ZIP.

Se l’output è in formato ZIP, il PDF viene convertito in un’immagine per pagina e ciascuna immagine termina con il numero della pagina. I file di immagine vengono quindi combinati in un file ZIP.

Ad esempio, un file denominato “TestFile” con 8 pagine genera 8 immagini, denominate da “TestFile_1” a “TestFile_8”. L’output del modulo è un file ZIP contenente le 8 immagini.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato file di output]</td> 
   <td> <p>Seleziona il formato che desideri utilizzare come output dei file:</p> 
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

Questo modulo di azione ti consente di estrarre dati da un file PDF. Il modulo restituisce singoli elementi di testo, ad esempio un paragrafo o il testo in una singola cella di una tabella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elementi che devono essere estratti come JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Testo]</p> </li> 
     <li> <p>[!UICONTROL Tabelle]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Estrarre i rettangoli di selezione?]</td> 
   <td>Abilita questa opzione per estrarre i dati relativi al rettangolo di selezione del testo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Includere informazioni sullo stile per l’output?]</td> 
   <td>Abilita questa opzione per aggiungere informazioni sullo stile al JSON di output.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Genera documento]

Il modulo [!UICONTROL Genera documento] rappresenta un modo efficace per creare un PDF che contiene i dati selezionati. Puoi formattarlo utilizzando un modello [!DNL Microsoft Word] o fornendo dati in formato JSON.

Per ulteriori informazioni sulla funzionalità [!UICONTROL [!DNL Adobe PDF Services] Genera documento], consulta la [Panoramica sulla generazione di documenti](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) nella documentazione di [!DNL Adobe Document Services].

* [Utilizzare il modulo [!UICONTROL Genera documento] con un modello  [!DNL Microsoft Word]  ](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Utilizzare il modulo [!UICONTROL Genera documento] con JSON](#use-the-generate-document-module-with-json)

#### Utilizzare il modulo [!UICONTROL Genera documento] con un modello [!DNL Microsoft Word]


>[!NOTE]
>
>Per informazioni sui modelli di Microsoft Word, consulta [Moduli del modello Microsoft Word](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Non è necessario utilizzare i moduli del modello Microsoft Word per usare un modello di Microsoft Word con il modulo Genera documento dei servizi PDF.


Per utilizzare il modulo [!UICONTROL Genera documento] con un modello [!UICONTROL Microsoft Word], è necessario prima creare il modello. Per istruzioni, cerca “Creare un modello” nella documentazione di [!DNL Microsoft Office].

Compila i campi del modulo [!UICONTROL Genera documento] nel modo seguente:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine è il modello [!DNL Microsoft Word] utilizzato dal modulo per generare il nuovo PDF.</p> <p>È consigliabile creare un progetto in Workfront per i modelli [!DNL Microsoft Word] utilizzati in Workfront Fusion. Puoi quindi utilizzare il modulo Workfront &gt; [!UICONTROL Scarica documento] per richiamare il modello appropriato nello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato di output]</td> 
   <td> <p>Seleziona il formato per il documento generato.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dati per l’unione]</td> 
   <td> <p>Per ciascun tag valore nel modello che desideri sostituire con testo, compila il modulo seguente:</p> 
    <ul> 
     <li> <p>[!UICONTROL Chiave]</p> <p>Inserisci una chiave. Nel modello, la chiave è il testo mostrato nel tag valore. Se ad esempio desideri inserire del testo nel tag valore <code>&#123;&#123;name&#125;&#125;</code>, inserisci <code>name </code> nel campo chiave.</p> </li> 
     <li> <p>Tipo di valore</p> <p>Seleziona se i dati nel campo valore rappresentano un valore, un oggetto o un array di oggetti.</p> </li> 
     <li> <p>[!UICONTROL Valore]</p> <p>Inserisci oppure mappa il testo che desideri visualizzare nel documento generato al posto del tag valore.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Utilizzare il modulo [!UICONTROL Genera documento] con JSON

Per utilizzare il modulo [!UICONTROL Genera documento] con JSON, compila i campi nel modo seguente:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato di output]</td> 
   <td> <p>Seleziona il formato per il documento generato.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Dati per l’unione]</td> 
   <td> <p>Per utilizzare JSON in questo modulo, è necessario abilitare la mappatura su questo campo.</p> <p>Inserisci oppure mappa il JSON da cui generare il documento. </p> <p>Puoi digitare JSON direttamente in questo campo, oppure mappare l’output JSON da un modulo JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearizza un file PDF]

Questo strumento linearizza un documento PDF per crearne uno ottimizzato per il web. Un documento PDF linearizzato può essere visualizzato pagina per pagina senza dover scaricare l’intero documento.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Effettua chiamata API personalizzata

Questo modulo di azione invia una richiesta HTTP personalizzata all’API PDF Services.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Inserisci un percorso relativo o un URL. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi]</td> 
   <td> <p>Per ciascun campo che desideri aggiungere alla chiamata API, fai clic su <b>Aggiungi elemento</b> e inserisci la chiave del campo e il valore facoltativo.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR per file PDF]

Questo strumento esegue il riconoscimento ottico dei caratteri (OCR) su un file e genera un PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lingua]</td> 
   <td>Seleziona la lingua di questo documento.<p>Per le opzioni relative alla lingua, consulta <a href="#convert-document-to-pdf-file" class="MCXref xref" >Convertire un documento in file PDF</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo OCR]</td> 
   <td> 
    <ul> 
     <li> <p>Il tipo [!UICONTROL Immagine originale modificata] garantisce che il testo sia ricercabile e selezionabile, ma modifica l’immagine originale durante il processo di pulizia (ad esempio la raddrizza) prima di posizionarvi sopra un livello di testo invisibile. Questo tipo rimuove gli artefatti indesiderati e può rendere un documento più leggibile in alcuni scenari. </p> </li> 
     <li> <p>Anche il tipo [!UICONTROL Immagine originale non modificata] sovrappone un livello di testo ricercabile all’immagine originale, ma in questo caso l’immagine originale rimane invariata. Questo tipo assicura la massima fedeltà all’immagine originale.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Manipolazione pagina]

Questo modulo consente di ruotare o eliminare selettivamente le pagine di un documento PDF. Puoi, ad esempio, passare dalla visualizzazione verticale alla visualizzazione orizzontale o rimuovere alcune pagine dal documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azione]</td> 
   <td> <p>Seleziona l’azione che desideri eseguire sul file.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Elimina]</b> </p> <p>Seleziona questa opzione per eliminare le pagine dal documento.</p><p>Per ogni intervallo di pagine che desideri eliminare, fai clic su <strong>[!UICONTROL Aggiungi]</strong>, quindi inserisci la prima e l’ultima pagina dell’intervallo di pagine. </p> <p>Nota:   
     <ul> 
      <li> <p>Puoi utilizzare numeri negativi per effettuare il conteggio a partire dalla fine del documento. L’ultima pagina di un documento è -1, la penultima è -2 e così via.</p> </li> 
      <li> <p>Per eliminare una singola pagina, imposta lo stesso numero di pagina come inizio e fine dell’intervallo.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Ruota]</b> </p> <p>Seleziona questa opzione per ruotare le pagine, quindi inserisci il valore dell’angolo desiderato, espresso in gradi, per ruotare le pagine del documento rispetto al relativo orientamento iniziale.</p> <p>Per ruotare da verticale a orizzontale o viceversa, ruota la pagina di 90 o 270 gradi.</p> <p>Se una pagina è capovolta, ruotala di 180 gradi.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pagine]</td> 
   <td> <p>Per ciascun intervallo di pagine che desideri eliminare, fai clic su <strong>[!UICONTROL Aggiungi]</strong>, quindi inserisci la prima e l’ultima pagina dell’intervallo di pagine. </p> <p>Nota:   
     <ul> 
      <li> <p>Puoi utilizzare numeri negativi per effettuare il conteggio a partire dalla fine del documento. L’ultima pagina di un documento è -1, la penultima è -2 e così via.</p> </li> 
      <li> <p>Per eliminare una singola pagina, imposta lo stesso numero di pagina come inizio e fine dell’intervallo.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che deve utilizzare il modulo durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Tag automatico di accessibilità PDF]

Questo modulo di azione crea un PDF a cui vengono assegnati tag per i casi d’uso relativi all’accessibilità. Crea inoltre un rapporto Microsoft Excel facoltativo che elenca i problemi e suggerisce le correzioni.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sposta intestazioni]</td> 
   <td> <p>Abilita questa opzione per spostare le intestazioni sul documento.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Genera rapporto]</td> 
   <td> <p>Abilita questa opzione per generare un rapporto che elenca i problemi di accessibilità dei PDF insieme alla rispettiva posizione e fornisce suggerimenti su come risolverli.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Proprietà file PDF]

Questo strumento estrae informazioni di base sul documento, ad esempio:

* Numero pagine
* Versione PDF
* Se il file è crittografato
* Se il file è linearizzato
* Se il file contiene file incorporati

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Proteggi un file PDF]

Questo strumento protegge un documento PDF con una password utente o proprietario. Inoltre, imposta restrizioni su alcune funzioni quali la stampa, la modifica e la copia nel documento di PDF. Puoi selezionare il tipo di contenuto da crittografare e l’algoritmo di crittografia.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di protezione tramite password]</td> 
   <td> <p>Abilita questa opzione per utilizzare le password per crittografare il documento PDF di input. Se abiliti questa opzione, è necessario specificare e inserire un valore per uno o entrambi i seguenti elementi: </p> 
    <ul> 
     <li> <p>[!UICONTROL Password utente]</p> </li> 
     <li> <p>[!UICONTROL Password proprietario] </p> </li> 
    </ul> <p>Ciascuna password può contenere fino a 128 caratteri.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algoritmo di crittografia]</td> 
   <td> <p>Seleziona l’algoritmo di crittografia. </p> 
    <ul> 
     <li> <p>[!UICONTROL Crittografia AES-128]</p> <p>La password supporta solo caratteri LATIN-I. </p> </li> 
     <li> <p>[!UICONTROL Crittografia AES-256]</p> <p>La password supporta il set di caratteri Unicode.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto da crittografare]</td> 
   <td> <p>Seleziona il tipo di contenuto da crittografare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Tutto il contenuto]</p> </li> 
     <li> <p>[!UICONTROL Tutto il contenuto esclusi i metadati]</p> </li> 
     <li> <p>[!UICONTROL Solo dati incorporati] </p> </li> 
    </ul> <p>Selezionando “[!UICONTROL Solo dati incorporati]” le autorizzazioni di accesso fornite diventano inefficaci.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Autorizzazioni]</td> 
   <td> <p>Seleziona le autorizzazioni che desideri includere per consentire la stampa, la modifica o la copia del contenuto.</p> <p>Le impostazioni delle autorizzazioni vengono utilizzate solo se la [!UICONTROL Password del proprietario] è impostata nel campo [!UICONTROL Tipo di protezione tramite password].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Rimuovi protezione di un file PDF]

Questo strumento rimuove la protezione (protezione tramite password) da un documento PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>Inserisci la password che attualmente protegge il file.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Dividi un file PDF]

Questo modulo di azione divide un documento PDF in documenti più piccoli. Puoi specificare se dividerlo per numero di file, pagine per file o intervalli di pagine.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la connessione da utilizzare per questo modulo.</p> Per istruzioni sulla creazione di una connessione a [!DNL Adobe PDF Services], consulta <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Creare una connessione a [!DNL Adobe PDF Services]</a> in questo articolo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> <p>Il file di origine deve essere in formato PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opzione dividi]</td> 
   <td>Seleziona in che modo desideri dividere il file. 
   <ul>
   <li><p><b>Intervalli di pagine</b></p><p>Per ciascun intervallo di pagine che desideri dividere in un documento separato, fai clic su <b>Aggiungi</b> e inserisci la pagina di inizio e la pagina di fine.</p></li>
   <li><p><b>Numero pagine</b></p><p>Inserisci il numero di pagine che desideri includere nei nuovi documenti.</p></li>
   <li><p><b>Numero file</b></p><p>Inserisci il numero di file di dimensioni uniformi in cui desideri dividere il documento.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

