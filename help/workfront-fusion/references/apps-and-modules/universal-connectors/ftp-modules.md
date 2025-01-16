---
title: Moduli FTP
description: I moduli FTP consentono di monitorare le modifiche apportate ai file in una cartella selezionata, caricare nuovi file nella cartella desiderata e modificare o eliminare i file esistenti già presenti in una cartella.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# Moduli FTP

I moduli FTP consentono di monitorare le modifiche apportate ai file in una cartella selezionata, caricare nuovi file nella cartella desiderata e modificare o eliminare i file esistenti già presenti in una cartella.

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

Per utilizzare [Fusion App] con [!DNL Workfront Fusion], è necessario disporre di un account FTP.

## Creare una connessione in un modulo FTP {#create-a-connection}

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection name]</td> 
   <td> <p> Immetti il nome della connessione FTP.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Host] </td> 
   <td> <p>Immetti il nome host del server FTP. E.g. <code>myftp123.server.com</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Port] </td> 
   <td> <p>Immettere il numero di porta del server FTP. E.g. <code>21</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL User name] </td> 
   <td> <p>Immetti il nome utente dell'account FTP.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Password] </td> 
   <td> <p>Immettere la password dell'account FTP.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Utilizzare una connessione protetta (TLS)</p> </td> 
   <td> <p>Selezionare se si desidera utilizzare una connessione protetta.</p> <p style="font-weight: bold;">[!UICONTROL No]</p> <p>Connessione non protetta.</p> <p style="font-weight: bold;">[!UICONTROL Explicit encryption or Implicit encryption]</p> <p>La connessione è protetta tramite SSL.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>Abilita questa opzione per verificare il certificato del server FTP. Se la verifica non riesce, la connessione non viene creata. Per superare la verifica, il certificato deve soddisfare uno dei seguenti criteri:</p> 
    <ul> 
     <li>essere firmato da un'autorità di certificazione <a href="https://en.wikipedia.org/wiki/Certificate_authority">radice</a></li> 
     <li>essere firmato da un'autorità di certificazione intermedia (vedere ad esempio <a href="https://knowledge.digicert.com/solution/SO16297.html">Funzionamento delle catene di certificati</a> per ulteriori spiegazioni). In questo caso, tutti i certificati intermedi devono essere installati sul server FTP.</li> 
     <li>essere un certificato autofirmato fornito nel campo [!UICONTROL Self-signed certificate] (vedere di seguito)</li> </ul>

Se questa opzione è disabilitata, il certificato del server FTP non viene verificato. Consigliamo vivamente di non disabilitare l’opzione in quanto rende la connessione insicura e comporta un grave rischio per la sicurezza.</td>
</tr> 
  <tr> 
   <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
   <td> <p>Fare clic sul pulsante <b>[!UICONTROL Extract]</b> per aprire la finestra di dialogo di caricamento.</p> <p>Carica il certificato per utilizzare TLS con il certificato autofirmato. [!DNL Workfront Fusion] non conserva né archivia i dati forniti, ad esempio file e password. File e password vengono utilizzati solo per estrarre il certificato.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Moduli FTP e relativi campi

* [Triggers](#triggers)
* [Azioni](#actions)

### Triggers

#### [!UICONTROL Watch files]

[!UICONTROL Watch files] è l&#39;unico modulo di attivazione per FTP. Controlla il contenuto del file della cartella selezionata. Il trigger viene eseguito quando un nuovo file viene inserito nella cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Seleziona la cartella da controllare.</p> <p><b>Nota:</b> è consentita una sola cartella per scenario. Le sottocartelle vengono ignorate.</p> <p><b>Suggerimento:</b> Per tenere traccia di più cartelle, creare uno scenario indipendente per ognuna di esse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>Impostare il numero massimo di risultati con cui [!DNL Workfront Fusion] lavorerà durante un ciclo. Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). [!DNL Workfront Fusion] non ha alcuna influenza su questo elemento. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Change permissions]](#change-permissions)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL List of files in a folder]](#list-of-files-in-a-folder)
* [[!UICONTROL Move a file or folder]](#move-a-file-or-folder)
* [[!UICONTROL Upload] un file](#upload-a-file)

#### [!UICONTROL Change permissions]

Questo modulo di azione modifica le impostazioni delle autorizzazioni di un file o di una cartella.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Change permission settings of]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">
               <p>Specificare se si desidera modificare le impostazioni di un file o di una cartella.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL File path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Immettere o mappare il percorso del file alla cartella o al file.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-MediumGray" role="rowheader">[!UICONTROL Permissions]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-MediumGray">
               <p>Imposta le autorizzazioni per il file o la cartella desiderate. Utilizzare i parametri chmod. Ad esempio: <code>777 </code> o <code>-rwxrwxrwx</code>.</p>
               <p>Le autorizzazioni devono corrispondere al pattern <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Create a folder]

Questo modulo di azione crea una nuova cartella.

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Folder path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">Immettere o mappare il percorso del file alla nuova cartella.</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL New folder name]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
               <p>Immettere o mappare un nome per la nuova cartella.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Delete a file]

Elimina un file dalla cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella FTP da cui si desidera eliminare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> Immettere il nome del file, inclusa l'estensione. Esempio: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

Questo modulo di azione elimina definitivamente la cartella specificata.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Folder]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-MediumGray">
               <p>Selezionare la cartella FTP da cui si desidera eliminare un file.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Get a file]

Recupera un file dal server FTP che può essere ulteriormente elaborato, ad esempio caricato in [!DNL Dropbox].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#creating-the-ftp-connection" class="MCXref xref">Creazione della connessione FTP</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> Immettere il percorso del file che si desidera ottenere.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List of files in a folder]

Recupera le informazioni sul file e/o sulla cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#creating-the-ftp-connection" class="MCXref xref">Creazione della connessione FTP</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Seleziona la cartella FTP in cui desideri eseguire la ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Specificare se si desidera recuperare informazioni su file, cartelle o entrambi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Immettere il termine di ricerca. Se non viene immesso alcun termine di ricerca, verranno recuperati tutti i file e le cartelle della cartella specificata.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Imposta il numero massimo di file recuperati da questo modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file or folder]

Questo modulo di azione sposta un file o una cartella in una posizione diversa.

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Old file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-MediumGray">
               <p>Immettere il percorso da cui si desidera spostare il file. Esempio: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-LightGray" style="font-weight: bold;">[!UICONTROL New file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-LightGray">
               <p>Immettere il percorso in cui spostare il file. Esempio: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Upload a file]

Carica un file sul server FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#creating-the-ftp-connection" class="MCXref xref">Creazione della connessione FTP</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella FTP in cui si desidera caricare il file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>Se questa opzione è abilitata e il file esiste già sul server FTP, il contenuto del file viene aggiunto al file esistente. Se questa opzione non è abilitata, il contenuto del file verrà sovrascritto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>Se questa opzione è abilitata e la cartella immessa nel campo Cartella non esiste sul server FTP, il modulo crea la cartella</p> </td> 
  </tr> 
 </tbody> 
</table>

## Risoluzione dei problemi {#troubleshooting}

Se riscontri problemi con l’app FTP durante la creazione della connessione o durante l’operazione di un modulo, prova a utilizzare uno dei client FTP più diffusi e prova a eseguire la stessa azione (ad esempio, crea una connessione o elenca i file in una cartella). con il client FTP. Se si verificano gli stessi problemi anche con il client FTP, il motivo potrebbe essere una configurazione errata del server FTP.
