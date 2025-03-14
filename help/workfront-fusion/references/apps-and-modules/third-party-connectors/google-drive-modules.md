---
title: Moduli unità Google
description: I  [!DNL Adobe Workfront Fusion Google Drive] moduli ti consentono di monitorare, cercare, creare, aggiornare, eliminare e gestire i tuoi file, cartelle o unità condivise nel tuo [!DNL Google Drive].
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Google Drive] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL Google Drive] consentono di monitorare, cercare, creare, aggiornare, eliminare e gestire i file, la cartella o le unità condivise in [!DNL Google Drive].

In uno scenario [!DNL Adobe Workfront Fusion], è possibile collegare l&#39;account [!DNL Google Drive] a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Informazioni sull&#39;API di Google Drive

Il connettore Google Drive utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## Connessione di [!DNL Google Drive] a [!DNL Workfront Fusion]

Se utilizzi l&#39;utente [!DNL @gmail.com] o [!DNL @googlemail.com], devi creare un client OAuth in [!DNL Google Cloud Platform] per ottenere il tuo [!UICONTROL ID client] e [!UICONTROL Segreto client].

Per istruzioni dettagliate su come creare il client OAuth (e ottenere [!UICONTROL ID client] e [!UICONTROL Segreto client]), vedi [Connetti [!DNL Adobe Workfront Fusion] a [!DNL Google Services] utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Per istruzioni sulla connessione dell&#39;account [!DNL Google Drive] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive] moduli e relativi campi

Quando configuri [!DNL Google Drive] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Drive], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Trigger](#triggers)
* [Azioni](#actions)

### Trigger

* [[!UICONTROL Controlla tutti i file]](#watch-all-files)
* [[!UICONTROL Osserva i commenti]](#watch-comments)
* [[!UICONTROL Controlla i file nella cartella]](#watch-files-in-folder)
* [[!UICONTROL Guarda i file condivisi]](#watch-shared-files)

#### [!UICONTROL Controlla tutti i file]

Questo modulo trigger avvia uno scenario quando un file in [!DNL Google Drive] viene aggiunto o modificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quali file guardare]</td> 
   <td> <p>Selezionare il tipo di file che si desidera visualizzare.</p> 
    <ul> 
     <li>[!UICONTROL Tutto]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converti [!DNL Google Documents] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Spreadsheets] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Slides] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Drawings] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Drawings].</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Selezionare se si desidera visualizzare i nuovi file e tutte le modifiche o solo i nuovi file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di file scaricati]</td> 
   <td>Impostare il numero massimo di risultati che [!DNL Workfront Fusion] scaricherà durante un ciclo (il numero di ripetizioni per esecuzione dello scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Osserva commenti]

Questo modulo di attivazione avvia uno scenario quando un commento viene aggiunto o modificato sul file selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File]</td> 
   <td>Selezionare il file da controllare per i commenti.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Seleziona se desideri controllare tutte le modifiche o solo i nuovi commenti</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di commenti restituiti]</td> 
   <td>Impostare il numero massimo di commenti che [!DNL Workfront Fusion] restituirà durante un ciclo (il numero di ripetizioni per esecuzione dello scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Controlla i file nella cartella]

Questo modulo di attivazione avvia uno scenario quando un file viene aggiunto o modificato nella cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Seleziona la cartella da controllare]</td>
    <td >Selezionare nell'unità la cartella in cui si desidera visualizzare i file.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Quali file guardare]</td>
   <td> <p>Selezionare il tipo di file che si desidera visualizzare.</p> 
    <ul> 
     <li>[!UICONTROL Tutto]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converti [!DNL Google Documents] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Spreadsheets] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Slides] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Drawings] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Drawings].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>Selezionare se si desidera visualizzare i nuovi file e tutte le modifiche o solo i nuovi file.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Numero massimo di file scaricati]</td>
    <td>Impostare il numero massimo di risultati che [!DNL Workfront Fusion] scaricherà durante un ciclo (il numero di ripetizioni per esecuzione dello scenario).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Guarda i file condivisi]

Si attiva quando viene condiviso un nuovo file o viene aggiornato un file condiviso esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Seleziona la cartella da controllare]</td> 
   <td>Seleziona la cartella condivisa in cui desideri guardare i file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Quali file guardare]</td> 
   <td> <p>Selezionare il tipo di file che si desidera visualizzare.</p> 
    <ul> 
     <li>[!UICONTROL Tutto]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Converti [!DNL Google Documents] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Spreadsheets] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Slides] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Converti [!DNL Google Drawings] file in formato]</td>
    <td>Selezionare il formato di file in cui convertire [!DNL Google Drawings].</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Selezionare se si desidera visualizzare i nuovi file e tutte le modifiche o solo i nuovi file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di file scaricati]</td> 
   <td>Impostare il numero massimo di risultati che [!DNL Workfront Fusion] scaricherà durante un ciclo (il numero di ripetizioni per esecuzione dello scenario).</td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Copia un file]](#copy-a-file)
* [[!UICONTROL Creare una fFolder]](#create-a-folder)
* [[!UICONTROL Eliminare un file]](#delete-a-file)
* [[!UICONTROL Ottieni un file]](#get-a-file)
* [[!UICONTROL Ottieni un collegamento di condivisione]](#get-a-share-link)
* [[!UICONTROL Spostare un file nel cestino]](#move-a-filefolder-to-trash)
* [[!UICONTROL Cerca file/cartelle]](#search-for-filesfolders)
* [[!UICONTROL Aggiorna un file]](#update-a-file)
* [[!UICONTROL Carica un file]](#upload-a-file)

#### [!UICONTROL Copia un file]

Questo modulo di azione copia un file nella nuova posizione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selezionare la destinazione in cui si desidera copiare un file.</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella di destinazione]</td> 
   <td>Selezionare la cartella contenente il file da copiare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file da copiare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Il nome della copia]</td> 
   <td>Immettere un titolo per il nuovo file. Lasciare vuoto questo campo se non si desidera modificare il nome del file originale.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea una cartella]

Questo modulo di azione crea una cartella nel percorso specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Seleziona la destinazione in cui desideri creare una cartella.</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nuovo percorso cartella]</td> 
   <td>Passa alla posizione in cui desideri creare una nuova cartella.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome della nuova cartella]</td> 
   <td>Immettere un nome per la cartella che si sta creando.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Condividi cartella]</td> 
   <td>Selezionare questa opzione se si desidera condividere la cartella con altri utenti tramite il collegamento [!UICONTROL Share]. In caso contrario, il collegamento di condivisione è solo per il proprietario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un file]

Questo modulo di azione elimina definitivamente un file o una cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un file]

Questo modulo di azione recupera il file con l’ID specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converti [!DNL Google Documents] file in formato]</td> 
   <td>Selezionare il formato di file in cui convertire [!DNL Google Documents].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converti [!DNL Google Spreadsheets] file in formato]</td> 
   <td>Selezionare il formato di file in cui convertire [!DNL Google Spreadsheets].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converti [!DNL Google Slides] file in formato]</td> 
   <td>Selezionare il formato di file in cui convertire [!DNL Google Slides].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converti [!DNL Google Drawings] file in formato]</td> 
   <td>Selezionare il formato di file in cui convertire [!DNL Google Drawings].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file da recuperare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un collegamento di condivisione]

Questo modulo di azione recupera il collegamento di condivisione per un file in Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file per il quale desideri ottenere il collegamento di condivisione.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Spostare un file nel cestino]

Questo modulo di azione sposta un file o una cartella nel cestino.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file da spostare nel cestino.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca file/cartelle]

Questo modulo di ricerca cerca file o cartelle in base ai criteri di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selezionare l'unità di destinazione in cui si desidera eseguire la ricerca.</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Elenca una cartella]</td> 
   <td>Passare alla cartella in cui si desidera cercare i file o le cartelle.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td> <p> Seleziona se desideri cercare file, cartelle o entrambi.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL - Ricerca]</p> </td> 
   <td> <p>Selezionare il tipo di ricerca che si desidera eseguire.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Cerca nei nomi di file/cartelle]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Immettere una parte del nome o del nome completo del file (compreso il suffisso) che si desidera cercare.</p> </li> 
       <li> <p><strong>[!UICONTROL Opzioni di ricerca]</strong> </p> <p>Selezionare se si desidera cercare il termine esatto o se si desidera cercare nomi contenenti il termine di ricerca.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext] ricerca</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Immettere un termine di ricerca da cercare in [!DNL Google Drive].</p> </li> 
      </ul> </li> 
     <li> <p><strong>Immettere una query di ricerca personalizzata</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Immettere la query di ricerca personalizzata. Per ulteriori informazioni, consulta la sezione [!UICONTROL Search for Files] di questo articolo.</p> </li> 
       <li> <p><strong>Aggiungi la cartella selezionata in precedenza alla query</strong> </p> <p>Cerca la cartella nell'insieme parent. In questo modo vengono trovati tutti i file e le cartelle che si trovano direttamente nella cartella selezionata in precedenza.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di risultati restituiti]</td> 
   <td>Impostare il numero massimo di file o cartelle [!DNL Workfront Fusion] restituiti durante un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continua l'esecuzione della route anche se il modulo non restituisce alcun risultato]</td> 
   <td>Abilita questa opzione per garantire che lo scenario non venga interrotto se il modulo non restituisce alcun risultato.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un file]

Questo modulo di azione aggiorna i metadati o il contenuto di un file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selezionare la destinazione contenente il file che si desidera aggiornare.</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sposta in una cartella]</td> 
   <td>Per spostare il file in una cartella specifica, selezionare la cartella in cui si desidera spostare il file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td>Mappa l’ID del file da aggiornare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Immetti un titolo per il file aggiornato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Modificare il contenuto di un file]</td> 
   <td>Seleziona se desideri sostituire il contenuto del file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Se stai sostituendo il contenuto, seleziona un file di origine da un modulo precedente o mappane il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conversione di un file]</td> 
   <td>Abilita questa opzione per convertire il file nel formato di file Google corrispondente.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un file]

Carica un file in [!DNL Google Drive].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Drive] a [!DNL Workfront Fusion], vedere <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Google Drive] a [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>Seleziona la destinazione in cui desideri caricare un file.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella di destinazione]</td> 
   <td>Selezionare la cartella in cui si desidera caricare un file. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Immettere un titolo per il nuovo file.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Converti un file]</td> 
   <td>L'attivazione di questa opzione consente al modulo di convertire i file nel formato [!DNL Google] corrispondente.</td> 
  </tr> 
 </tbody> 
</table>

## Risoluzione dei problemi

### Impossibile caricare o aggiornare un file

Esistono diversi motivi per cui il caricamento o l’aggiornamento di un file non riesce:

* Il file caricato è troppo grande e supera la dimensione massima consentita per il piano [!DNL Google Drive] oppure hai superato il limite di archiviazione di [!DNL Google Drive]. È possibile aggiornare il piano di archiviazione o eliminare i file esistenti dal servizio [!DNL Google Drive].
* La cartella selezionata in cui doveva essere caricato il file non esiste più. In questo caso, lo scenario si interrompe e devi selezionare una cartella di destinazione diversa nel modulo.

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
