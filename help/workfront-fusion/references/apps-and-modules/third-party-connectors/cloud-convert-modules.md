---
title: Moduli CloudConvert
description: Moduli CloudConvert
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2498'
ht-degree: 0%

---

# [!DNL CloudConvert] moduli

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano CloudConvert e collegarlo a più applicazioni e servizi di terze parti. I moduli [!DNL CloudConvert] ti consentono di monitorare e gestire processi, attività e importare ed esportare file nel tuo account [!DNL CloudConvert].

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

## Informazioni API di CloudConvert

Il connettore CloudConvert utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.cloudconvert.com/v2/</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.14.22</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL CloudConvert] a [!DNL Workfront Fusion] {#connect-cloudconvert-to-workfront-fusion}

Per connettere l&#39;account [!DNL CloudConvert] a [!DNL Workfront Fusion], è necessario ottenere la chiave API dall&#39;account [!DNL CloudConvert].

1. Accedi al tuo account [!DNL CloudConvert] e apri [!UICONTROL Dashboard].
1. Apri la sezione **[!UICONTROL Authorization]>[!UICONTROL API Keys]**.
1. Fare clic su **[!UICONTROL Create New API key]**.
1. Immettere il nome per la chiave API, abilitare gli ambiti che si desidera utilizzare, quindi fare clic su **[!UICONTROL Create]**.
1. Copia il token fornito e archivialo in un luogo sicuro.
1. In [!DNL Workfront Fusion], iniziare a creare uno scenario e aprire la finestra di dialogo **[!UICONTROL Create a connection]** del modulo [!DNL CloudConvert].

   Per istruzioni, vedere [Creare uno scenario in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

1. Immettere il token salvato nel passaggio 5, quindi fare clic su **[!UICONTROL Continue]** per stabilire la connessione.

## [!DNL CloudConvert] moduli e relativi campi {#cloudconvert-modules-and-their-fields}

Quando configuri [!DNL CloudConvert] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL CloudConvert], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Attività comuni](#common-tasks)
* [Processi](#jobs)
* [Attività](#tasks)
* [Altro](#other)

### Attività comuni

* [Acquisire un sito Web](#capture-a-website)
* [[!UICONTROL Convert a file]](#convert-a-file)
* [Crea un archivio](#create-an-archive)
* [Unisci file](#merge-files)
* [Ottimizzare un file](#optimize-a-file)

#### [!UICONTROL Capture a Website]

Questo modulo di azione acquisisce un sito web specifico e lo salva in formato PDF, JPG o PNG.

Puoi specificare l’URL del sito web e altre informazioni, ad esempio dove desideri che vengano memorizzate.

Il modulo restituisce l’ID del file e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immetti l’URL del sito web che desideri acquisire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Seleziona se desideri salvare il sito web acquisito in formato PNG, JPG-PDF o. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td>Immettere un nome di file (con estensione) per il file di output di destinazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>(Facoltativo) Definisci le intestazioni delle richieste. </p> <p>Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Specifica le opzioni di conversione e specifiche per il motore. Per visualizzare le opzioni disponibili, vedere la documentazione dell'API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]</a> per <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Abilita questa opzione se desideri includere anche i dati dei file nell’output del modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert a file]

Converte un file nel formato di output selezionato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input file]</td> 
   <td>Selezionare se si desidera caricare un file utilizzando [!DNL Workfront Fusion] o specificare l'URL da cui verrà caricato il file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a File from URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Immettere l'URL del file che si desidera convertire.</p> </li> 
     <li> <p><strong>[!UICONTROL Headers]</strong></p> <p>Definire le intestazioni di richiesta (facoltativo). Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>Specificare se si desidera specificare il formato di input del file da convertire. Se non viene specificata, come formato di input viene utilizzata l'estensione del file di input.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>Selezionare il formato corrente del file.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td>Selezionare il formato di file di destinazione in cui si desidera convertire il file.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL File Name]</td> 
   <td>Scegliete un nome file (estensione inclusa) per il file di output di destinazione.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>Specifica le opzioni di conversione e specifiche per il motore. Per visualizzare le opzioni disponibili, vedere la documentazione dell'API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]</a> per <code>input_format</code> e <code>output_format</code>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>Abilita questa opzione se desideri includere anche i dati dei file nell’output del modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Archive]

Consente di aggiungere uno o più file all&#39;archivio ZIP, RAR, 7Z, TAR, TAR.GZ o TAR.BZ2.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Specificare i file da aggiungere all'archivio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Immettere l'URL del file che si desidera archiviare.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definire le intestazioni di richiesta (facoltativo). Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selezionare il formato di destinazione del file archiviato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Immettere il nome del file di output di destinazione, inclusa l'estensione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Specifica le opzioni di conversione e specifiche per il motore. Per visualizzare le opzioni disponibili, vedere la documentazione dell'API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]</a> per <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Abilita questa opzione se desideri includere anche i dati dei file nell’output del modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Merge Files]

Unisce almeno due file in un unico PDF. Se i file di input non sono PDF, vengono automaticamente convertiti in PDF.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>Specificare i file da unire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>Immettere l'URL del file che si desidera archiviare.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>Definire le intestazioni di richiesta (facoltativo). Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> Selezionare il formato di destinazione del file unito.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> Immettere il nome del file di output di destinazione, inclusa l'estensione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>Specifica le opzioni di conversione e specifiche per il motore. Per visualizzare le opzioni disponibili, vedere la documentazione dell'API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]</a> per <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>Abilita questa opzione se desideri includere anche i dati dei file nell’output del modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Optimize a File]

Questo modulo di azione ottimizza e comprime un file in formato PDF, PNG o JPG.

È possibile specificare il file e i parametri per l&#39;ottimizzazione e la memorizzazione.

Il modulo restituisce l’ID del file e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input File]</td> 
   <td>Seleziona se desideri caricare un file utilizzando Workfront Fusion o fornisci l’URL da cui verrà caricato il file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Upload a File]</p> </td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a file from URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: immetti l’URL del file da convertire.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (facoltativo) definisci le intestazioni della richiesta. Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimization for] </td> 
   <td> <p>Seleziona il profilo di ottimizzazione per esigenze di destinazione specifiche.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: ottimizzazione per il web (impostazione predefinita)</p> 
      <ul> 
       <li>Rimuovere i dati ridondanti e non necessari per il Web</li> 
       <li>Downsampling, clip e compressione intelligente delle immagini</li> 
       <li>Unisci e crea sottoinsiemi di font</li> 
       <li>Converti colori in RGB</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Print]</strong>: ottimizzazione per la stampa</p> 
      <ul> 
       <li> <p>Rimuovere i dati ridondanti e non necessari per la stampa</p> </li> 
       <li> <p>Downsampling, clip e compressione intelligente delle immagini</p> </li> 
       <li> <p>Unisci e crea sottoinsiemi di font</p> </li> 
       <li> <p>Converti colori in CMYK</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Archive]</strong>: ottimizzazione a scopo di archiviazione</p> 
      <ul> 
       <li> <p>Eliminazione dei dati ridondanti e non necessari per l'archiviazione</p> </li> 
       <li> <p>Compressione intelligente delle immagini</p> </li> 
       <li> <p>Unisci e crea sottoinsiemi di font</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Scanned images]</strong>: ottimizzazione per le immagini digitalizzate</p> 
      <ul> 
       <li> <p>Profilo ottimizzato per PDF costituiti principalmente da immagini raster</p> </li> 
       <li> <p>Comprimi le immagini senza ridurre significativamente la qualità visiva</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximal size reduction]</strong>: ottimizzazione per la massima riduzione delle dimensioni</p> 
      <ul> 
       <li> <p>Utilizzare la compressione massima possibile</p> </li> 
       <li> <p>Potrebbe ridurre la qualità visiva</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input format] </td> 
   <td>Selezionare il formato del file di input che si desidera ottimizzare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p>Immettere un nome di file (con estensione) per il file di output di destinazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options]</td> 
   <td> <p>Specifica le opzioni di conversione e specifiche per il motore. Per visualizzare le opzioni disponibili, vedere la documentazione dell'API <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert]</a> per <code>input_format</code> e <code>output_format</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file]</td> 
   <td> <p>Abilita questa opzione se desideri includere anche i dati dei file nell’output del modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Lavori

* [[!UICONTROL Create a Job (advanced)]](#create-a-job-advanced)
* [[!UICONTROL New Job Event]](#new-job-event)
* [[!UICONTROL List Jobs]](#list-jobs)
* [[!UICONTROL Get a Job]](#get-a-job)
* [[!UICONTROL Delete a Job]](#delete-a-job)

#### [!UICONTROL Create a Job (advanced)]

Questo modulo crea un processo. Un processo può essere costituito da una o più attività identificate nel campo [!UICONTROL Name] e collegate tra loro mediante il campo [!UICONTROL Input].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Files]</td> 
   <td> <p>Selezionare se si desidera caricare un file utilizzando [!DNL Workfront Fusion] o fornire l'URL da cui verrà caricato il file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a File from URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: immetti l’URL del file da elaborare.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (facoltativo) definisci le intestazioni della richiesta. Ciò è utile, ad esempio, quando l’URL specificato richiede l’autorizzazione.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tasks]</p> </td> 
   <td> <p>Aggiungi le attività che verranno eseguite all’interno del processo.</p> <p>Le descrizioni dei campi relativi alle operazioni sono disponibili nella sezione corrispondente.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Convert a file]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capture a Websit]e</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Optimize a File]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Create an Archive]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Merge Files]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Execute a Command]</strong> </p> <p>Per ulteriori informazioni sull'esecuzione di un comando, vedere la documentazione API <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert]</a>.</p> </li> 
     <li> <p><strong>[!UICONTROL Export a File to Temporary URL]</strong> </p> <p> Specifica il nome dell’attività e il nome dell’attività di input (ad esempio, Conversione).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>Immetti un tag. I tag sono stringhe arbitrarie per identificare il processo. Non hanno alcun effetto e possono essere utilizzati per associare il processo a un ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Job]

Questo modulo elimina un processo, inclusi tutti i task e i dati.

>[!NOTE]
>
>I processi vengono eliminati automaticamente 24 ore dopo la loro fine.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Immetti o mappa l’ID del processo da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Job]

Questo modulo recupera i dettagli del processo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>Immetti o mappa l’ID del processo su cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Jobs]

Questo modulo recupera tutti i processi eseguiti nel tuo account.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selezionare lo stato del processo in base al quale filtrare i processi restituiti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero di processi restituiti da Workfront Fusion 2.0 durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL New Job Event]

Si attiva quando un processo nell’account o nell’attività viene creato, terminato o ha esito negativo.

>[!NOTE]
>
>* Il processo creato dal modulo [!UICONTROL Create a Job (advanced)] è costituito da *diverse* attività.
>* Il trigger [!UICONTROL New Job Event] viene attivato anche quando viene creata, terminata o non riuscita un&#39;attività *individuale*.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhhook name]</td> 
   <td>Immetti il nome del webhook. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>Seleziona se desideri salvare il sito web acquisito in formato PNG, JPG-PDF o. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event]</td> 
   <td>Seleziona se attivare il modulo quando il processo o l'attività viene creata, terminata o non riesce.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Se si utilizza l&#39;aggregatore di matrici (ad esempio, sono presenti molti file in formati diversi da convertire), utilizzare l&#39;opzione **[!UICONTROL I don't know the input format]** nella finestra di dialogo [!UICONTROL Add a task]. In caso contrario, viene restituito l’errore.
>* Collegamento di task all&#39;interno del job (nome > input, nome > input,...):
>
>  ![Collegamento del nome tra processi](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### Attività

* [[!UICONTROL Get a Task]](#get-a-task)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL List Tasks]](#list-tasks)
* [[!UICONTROL Retry a Task]](#retry-a-task)
* [[!UICONTROL Cancel a Task]](#cancel-a-task)
* [[!UICONTROL Delete a Task]](#delete-a-task)

#### [!UICONTROL Cancel a Task]

Questo modulo annulla un&#39;operazione con stato In attesa o in elaborazione.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Immettere o mappare l'ID dell'attività che si desidera annullare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Task]

Elimina un&#39;attività, inclusi tutti i dati.

>[!NOTE]
>
>Le attività vengono eliminate automaticamente 24 ore dopo la loro fine.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Immetti (mappa) l’ID dell’attività da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Questo modulo recupera il nome e i dati del file dall&#39;operazione specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Immetti o mappa l’ID dell’attività da cui desideri scaricare il file.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Task]

Questo modulo recupera i dettagli dell’attività.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Immetti o mappa l’ID dell’attività di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Tasks]

Questo modulo recupera tutte le attività nell’account in base alle impostazioni del filtro.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>Selezionare lo stato dell'attività in base al quale filtrare le attività restituite.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID] </td> 
   <td> <p>Immettere o mappare l'ID processo in modo da restituire solo le attività all'interno del processo specificato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Immettere il tipo di operazione per restituire solo i task con l'operazione specificata. </p> <p>Nota: utilizzare il modulo [!UICONTROL List Possible Operations] per recuperare le operazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Retry a Task]

Questo modulo crea una nuova attività, basata sulle impostazioni (payload) di un’altra attività.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> Immettere o mappare l'ID dell'attività da cui si desidera creare una nuova attività.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Get My Info]](#get-my-info)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Get My Info]

Recupera i dettagli dell&#39;account autenticato dell&#39;utente corrente.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL CloudConvert] a [!DNL Workfront Fusion], vedere <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL CloudConvert] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [Fusion App] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Immettere un percorso relativo a <code>https://api.cloudconvert.com/</code>. Ad esempio: <code>/v2/tasks</code></p> <p>Per un elenco degli endpoint disponibili, vedere la documentazione dell'API v2 <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 2.0 aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard. Quando utilizzi istruzioni condizionali come <code>if</code> nel JSON, inserisci le virgolette al di fuori dell'istruzione condizionale.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio:** attività elenco

La seguente chiamata API restituisce tutte le attività dal tuo account CloudFront:

URL: `/v2/tasks`

Metodo: `GET`

![Esempio di input API](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

Le corrispondenze della ricerca si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data].

Nel nostro esempio, sono state restituite 6 attività:

![Output di esempio API](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

## Risoluzione dei problemi {#troubleshooting}

Per informazioni sui possibili errori e sulle relative soluzioni, vedere la tabella seguente:

<table style="table-layout:auto">
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>Errore</p> </th> 
   <th>Passaggi successivi</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL The output file size exceeds the limit allowed for your scenario.]</span> </p> </td> 
   <td> <p>Consulta i limiti di dimensione del file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL You have exceeded the maximum conversion time.]</span> </p> </td> 
   <td> <p>Il piano gratuito [!DNL CloudConvert] offre 25 minuti di conversione al giorno. Se l’utilizzo supera il limite del piano gratuito, puoi passare a un pacchetto (prepagato) o a un abbonamento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Failed to read frame size: Could not seek to 1508. �/output/JLIADSA00137P0.mp3: Invalid argument.]</span> </p> </td> 
   <td> <p>Questo errore viene generato, ad esempio, durante la conversione di file da MP3 a WAV. Accertatevi di aver selezionato l'area corretta poiché troverà riferimenti ai file ma non solo il file corretto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximum number of repeats exceeded.]</span> </p> </td> 
   <td> <p>Individua il processo [!DNL CloudConvert] corrispondente nell'elenco dei processi del dashboard [!DNL CloudConvert] e controlla la durata del processo:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>Il timeout del modulo [!DNL CloudConvert] &gt; [!UICONTROL Convert a File] è impostato su 3 minuti. Se la durata del processo supera i 3 minuti (probabilmente a causa di un sovraccarico temporaneo del servizio [!DNL CloudConvert]), il modulo restituisce l'errore sopra indicato.</p> <p>In questo caso, considera una delle seguenti opzioni:</p> 
    <ul> 
     <li>Abilitare l'opzione <strong>[!UICONTROL Allow storing of Incomplete Executions]</strong> nelle impostazioni dello scenario per memorizzare le esecuzioni incomplete per una successiva risoluzione manuale. Facoltativamente, è possibile allegare un percorso di gestione degli errori al modulo [!DNL CloudConvert] con la direttiva [!UICONTROL Break] per risolvere automaticamente le esecuzioni incomplete.</li> 
     <li>Disattivare l'opzione <strong>[!UICONTROL Download a file]</strong> nel modulo [!DNL CloudConvert] &gt; [!UICONTROL Convert a file]. In questo caso, il modulo non attende il risultato della conversione. Per ottenere il risultato della conversione, creare un nuovo scenario e utilizzare il trigger [!DNL CloudConvert] &gt; [!UICONTROL New Job Event].</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio di flusso di lavoro per il connettore [!DNL CloudConvert]

>[!INFO]
>
>**Esempio:** conversione di un video dal formato MOV al formato MP4
>
>1. Visita [https://cloudconvert.com/video-converter](https://>cloudconvert.com/video-converter)
>1. Fare clic su **[!UICONTROL Select File]** e scegliere il file MOV di esempio.
>1. Fare clic sul menu a discesa accanto a **[!UICONTROL Convert to]** e scegliere **[!UICONTROL MP4]**.
>
>1. Fare clic sull&#39;icona **[!UICONTROL wrench]**.
>1. Configura le impostazioni di compressione MP4 come lo ritieni opportuno.
>1. Fare clic su **[!UICONTROL Convert]**.
>1. Una volta completata la conversione, fare clic su **[!UICONTROL Download]**.
>1. Rivedi il video convertito.
>1. Ripetere i passaggi da 1 a 8 fino a trovare le impostazioni di conversione ottimali per il passaggio 5.
>1. Visita [https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks)
>1. Scegliere **[!UICONTROL mov]** per il campo **[!UICONTROL input_format]**.
>
>1. Scegliere **[!UICONTROL mp4]** per il campo **[!UICONTROL output_format]**.
>
>1. Un elenco di tutti i parametri possibili come video_codec, crf, ecc. verrà visualizzato.
>1. In Workfront Fusion 2.0, inserisci il modulo **[!UICONTROL CloudConvert]** > **[!UICONTROL Convert a File]** nello scenario.
>
>1. Apri le impostazioni del modulo.
>1. Configura il modulo come mostrato di seguito:
>
>   ![Esempio CloudConvert](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. Assicurati di includere tutte le impostazioni nel campo Conversione e opzioni specifiche del motore: per ogni impostazione dal punto 5, individua il parametro corrispondente dal punto 13 e il relativo valore corrispondente.
