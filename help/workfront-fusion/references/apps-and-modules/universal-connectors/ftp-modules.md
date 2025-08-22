---
title: Moduli FTP
description: I moduli FTP consentono di monitorare le modifiche apportate ai file in una cartella selezionata, caricare nuovi file nella cartella desiderata e modificare o eliminare i file esistenti già presenti in una cartella.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 1%

---

# Moduli FTP

I moduli FTP consentono di monitorare le modifiche apportate ai file in una cartella selezionata, caricare nuovi file nella cartella desiderata e modificare o eliminare i file esistenti già presenti in una cartella.

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
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli FTP, è necessario disporre di un account con un servizio FTP.

## Creare una connessione in un modulo FTP {#create-a-connection}

1. In qualsiasi modulo FTP, fai clic su **Aggiungi** accanto alla casella di connessione.
1. Compila i campi seguenti.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome connessione]</td> 
      <td> <p> Immetti il nome della connessione FTP.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Seleziona se utilizzi un ambiente di produzione o non di produzione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Seleziona se utilizzi un account di servizio o un account personale.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Immetti il nome host del server FTP. Esempio: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>Porta [!UICONTROL] </td> 
      <td> <p>Immettere il numero di porta del server FTP. Esempio: <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Nome utente] </td> 
      <td> <p>Immetti il nome utente dell'account FTP.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Password] </td> 
      <td> <p>Immettere la password dell'account FTP.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Utilizzare una connessione protetta (TLS)</p> </td> 
      <td> <p>Selezionare se si desidera utilizzare una connessione protetta.</p> <ul><li><p><b>[!UICONTROL No]</b></p> <p>Connessione non protetta.</p></li><li> <p><b>Crittografia esplicita</b> o <b>Crittografia implicita</b></p> <p>La connessione è protetta tramite SSL.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Rifiuta certificati non autorizzati]</p> </td> 
   <td> <p>Abilita questa opzione per verificare il certificato del server FTP. Se la verifica non riesce, la connessione non viene creata. Per superare la verifica, il certificato deve soddisfare uno dei seguenti criteri:</p> 
    <ul> 
     <li>essere firmato da un’autorità di certificazione radice</a></li> 
     <li>essere firmata da un’autorità di certificazione intermedia. In questo caso, tutti i certificati intermedi devono essere installati sul server FTP.</li> 
     <li>essere un certificato autofirmato fornito nel campo [!UICONTROL Self-signed certificate] (vedi di seguito)</li> </ul>
     <p>Se questa opzione è disabilitata, il certificato del server FTP non viene verificato. Consigliamo vivamente di non disabilitare l’opzione in quanto rende la connessione insicura e comporta un grave rischio per la sicurezza.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
     <td> <p>Fai clic sul pulsante <b>[!UICONTROL Extract]</b> per aprire la finestra di dialogo di caricamento.</p> <p>Carica il certificato per utilizzare TLS con il certificato autofirmato. In Workfront Fusion non vengono conservati né memorizzati i dati forniti, ad esempio file e password. File e password vengono utilizzati solo per estrarre il certificato.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## Moduli FTP e relativi campi

* [Trigger](#triggers)
* [Azioni](#actions)

### Trigger

#### [!UICONTROL File di controllo]

[!UICONTROL File di controllo] è l&#39;unico modulo di attivazione per FTP. Controlla il contenuto del file della cartella selezionata. Il trigger viene eseguito quando viene aggiunto un nuovo file nella cartella specificata.

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
   <td> <p>Seleziona la cartella da controllare.</p> <p><b>Nota:</b> è consentita una sola cartella per scenario. Le sottocartelle vengono ignorate.</p> <p><b>Suggerimento:</b> Per controllare più cartelle, crea uno scenario separato per ciascuna di esse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di file restituiti] </td> 
   <td> <p>Impostare il numero massimo di risultati con cui si desidera che il modulo funzioni durante un ciclo. Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del server FTP. Workfront Fusion non ha alcuna influenza su questo aspetto. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Modifica autorizzazioni]](#change-permissions)
* [[!UICONTROL Crea una cartella]](#create-a-folder)
* [[!UICONTROL Eliminare un file]](#delete-a-file)
* [[!UICONTROL Eliminare una cartella]](#delete-a-folder)
* [[!UICONTROL Ottieni un file]](#get-a-file)
* [[!UICONTROL Elenco di file in una cartella]](#list-of-files-in-a-folder)
* [[!UICONTROL Spostare un file o una cartella]](#move-a-file-or-folder)
* [[!UICONTROL Carica] un file](#upload-a-file)

#### [!UICONTROL Modifica autorizzazioni]

Questo modulo di azione modifica le impostazioni delle autorizzazioni di un file o di una cartella.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Modifica le impostazioni delle autorizzazioni di]</td>
            <td>
               <p>Specificare se si desidera modificare le impostazioni di un file o di una cartella.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Percorso file]</td>
            <td>Immettere o mappare il percorso del file alla cartella o al file.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Permissions]</td>
            <td>
               <p>Imposta le autorizzazioni per il file o la cartella desiderate. Utilizzare i parametri chmod. Ad esempio: <code>777 </code> o <code>-rwxrwxrwx</code>.</p>
               <p>Le autorizzazioni devono corrispondere al pattern <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Crea una cartella]

Questo modulo di azione crea una nuova cartella.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Percorso cartella]</td>
            <td>Immettere o mappare il percorso del file alla nuova cartella.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Nome nuova cartella]</td>
            <td>
               <p>Immettere o mappare un nome per la nuova cartella.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Eliminare un file]

Questo modulo di azione elimina un file dalla cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella FTP da cui si desidera eliminare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome file]</td> 
   <td> <p> Immettere il nome del file, inclusa l'estensione. Esempio: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare una cartella]

Questo modulo di azione elimina definitivamente la cartella specificata.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder]</td>
            <td>
               <p>Selezionare la cartella FTP da cui si desidera eliminare un file.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Ottieni un file]

Questo modulo di azione recupera un file dal server FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#creating-the-ftp-connection" class="MCXref xref">Creazione della connessione FTP</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Percorso file]</td> 
   <td> <p> Immettere il percorso del file che si desidera ottenere.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenco di file in una cartella]

Questo modulo di azione recupera le informazioni sul file e/o sulla cartella.

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
   <td>[!UICONTROL - Ricerca] </td> 
   <td> <p>Immettere il termine di ricerca. Se non viene immesso alcun termine di ricerca, verranno recuperati tutti i file o le cartelle della cartella specificata.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di file restituiti]</td> 
   <td> <p>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Spostare un file o una cartella]

Questo modulo di azione sposta un file o una cartella in una posizione diversa.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Per istruzioni su come stabilire una connessione all'account FTP, vedere <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] in un modulo FTP</a> in questo articolo.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Percorso file precedente]</td>
            <td>
               <p>Immettere il percorso da cui si desidera spostare il file. Esempio: <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL Percorso nuovo file]</td>
            <td>
               <p>Immettere il percorso in cui spostare il file. Esempio: <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Carica un file]

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
   <td>[!UICONTROL Aggiungi a un file già esistente]</td> 
   <td> <p>Se questa opzione è abilitata e il file esiste già sul server FTP, il contenuto del file viene aggiunto al file esistente. Se questa opzione non è abilitata, il contenuto del file verrà sovrascritto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Crea cartelle se non esiste] </td> 
   <td> <p>Se questa opzione è abilitata e la cartella immessa nel campo Cartella non esiste sul server FTP, il modulo crea la cartella</p> </td> 
  </tr> 
 </tbody> 
</table>

## Risoluzione dei problemi {#troubleshooting}

Se riscontri problemi con l’app FTP durante la creazione della connessione o durante l’operazione di un modulo, prova a utilizzare uno dei client FTP più diffusi e prova a eseguire la stessa azione (ad esempio, crea una connessione o elenca i file in una cartella). con il client FTP. Se si verificano gli stessi problemi anche con il client FTP, il motivo potrebbe essere una configurazione errata del server FTP.
