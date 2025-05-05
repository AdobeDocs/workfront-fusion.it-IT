---
title: Moduli Box
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Box e collegarlo a più applicazioni e servizi di terze parti. controlla una cartella specificata per verificare la presenza di modifiche ai file, modificare ed eliminare file esistenti o caricare nuovi file in una cartella.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 0ed33cbed2b8ed4ab2c89c86b7e8f37b2683ec75
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 1%

---

# Moduli Box

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Box] e collegarlo a più applicazioni e servizi di terze parti. controlla una cartella specificata per verificare la presenza di modifiche ai file, modificare ed eliminare file esistenti o caricare nuovi file in una cartella.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Per utilizzare i moduli [!DNL Box], è necessario disporre di un account [!DNL Box].

## Casella informazioni API

Il connettore Box utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] moduli e relativi campi

Quando configuri [!DNL Box] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Box], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [[!UICONTROL Evento nuovo file]](#new-file-event)
* [Evento nuova cartella](#new-folder-event)
* [[!UICONTROL File di controllo]](#watch-files)

#### [!UICONTROL Evento nuovo file]

Questo modulo di attivazione immediata avvia uno scenario in cui l’azione selezionata si verifica su un file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook da utilizzare per guardare i messaggi in uscita o aggiungi un webhook. </p><p>Per aggiungere un webhook, fare clic su <strong>[!UICONTROL Add]</strong> e immettere il nome e la connessione del webhook, il file che si desidera controllare e i trigger che si desidera controllare.</p> <p> Per istruzioni sulla connessione dell'account [!UICONTROL Box] a [!UICONTROL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connessione a un servizio - Istruzioni di base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Evento nuova cartella

Questo modulo di attivazione immediata avvia uno scenario quando l’azione di selezione si verifica nella cartella.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook da utilizzare per guardare i messaggi in uscita o aggiungi un webhook. </p><p>Per aggiungere un webhook, fare clic su <strong>[!UICONTROL Add]</strong> e immettere il nome e la connessione del webhook, la cartella che si desidera controllare e i trigger che si desidera controllare.</p> <p> Per istruzioni sulla connessione dell'account [!UICONTROL Box] a [!UICONTROL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connessione a un servizio - Istruzioni di base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL File di controllo]

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un nuovo file o un file esistente viene aggiornato in una cartella controllata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Osserva nella cartella</td> 
   <td> <p>Seleziona la cartella da controllare. Uno scenario può guardare una singola cartella.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Osserva</td> 
   <td> <p>Selezionare il tipo di file che si desidera controllare.</p> 
    <ul> 
     <li> <p><strong>Solo i nuovi file</strong> </p> <p>Lo scenario inizierà quando viene aggiunto un nuovo file.</p> </li> 
     <li> <p><strong>Nuovi file e tutte le modifiche</strong> </p> <p>Lo scenario inizia quando viene aggiunto un file o quando viene modificato il contenuto del file o un attributo del file (come il nome).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Numero massimo di file scaricati</p> </td> 
   <td> <p>Immettere il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Creare una cartella](#create-a-folder)
* [Ottieni una cartella](#get-a-folder)
* [Ottieni metadati cartella](#get-folder-metadata)
* [Effettuare una chiamata API](#make-an-api-call)
* [Aggiorna metadati cartella](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Creare una cartella

Questo modulo di azione crea una nuova cartella vuota all’interno della cartella principale specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Immettere o mappare un nome per la nuova cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cartella padre </td> 
   <td> <p>Selezionare la cartella in cui si desidera creare la nuova cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Upload Email Access]</td> 
   <td> <p>Una volta impostato questo parametro, gli utenti possono inviare i file tramite e-mail all'indirizzo e-mail creato automaticamente per la cartella. Le opzioni collaboratori consentono solo le e-mail registrate per i collaboratori.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stato sincronizzazione]</td> 
   <td> <p>Specifica se una cartella deve essere sincronizzata con il dispositivo di un utente. Viene utilizzato da Box Sync (discontinuo) e non da Box Drive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni una cartella

Questo modulo di azione recupera i dettagli di una cartella, incluse le prime 100 voci della cartella.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selezionare la cartella per la quale si desidera recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni metadati cartella

Questo modulo di azione recupera i metadati della cartella per ID cartella.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ambito]</td> 
   <td> <p>Selezionare l'ambito da utilizzare per il recupero dei metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Seleziona la cartella per la quale desideri recuperare i metadati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Effettuare una chiamata API

Questo modulo di azione effettua una chiamata personalizzata all’API Box.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Bynder] a [!DNL Workfront Fusion], vedere <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Bynder] a [!DNL Workfront Fusion] </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Immettere un percorso relativo a <code>https://api.box.com</code>. <p>Esempio: <code>/2.0/users/me</code></p></td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiorna metadati cartella

Questo modulo crea o aggiorna i metadati di una cartella.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ambito]</td> 
   <td> <p>Selezionare l'ambito da utilizzare per l'aggiornamento dei metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Seleziona la cartella per la quale desideri aggiornare i metadati.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Ricerche

#### Cerca contenuto

Questo modulo di ricerca cerca gli elementi disponibili per l’utente o per l’azienda.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Immettere o mappare la stringa da cercare. Questa query viene confrontata con i nomi degli elementi, le descrizioni, il contenuto di testo dei file e vari altri campi dei diversi tipi di elementi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ambito]</td> 
   <td> <p>Specificare se si desidera cercare contenuto associato all'utente le cui credenziali vengono utilizzate per la connessione utilizzata in questo modulo o contenuto associato all'intera organizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Seleziona se stai cercando file, cartelle o collegamenti web.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Specificare se si desidera ordinare in base alla rilevanza o alla data di modifica.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Contenuto cestino]</td> 
   <td> <p>Seleziona se desideri cercare contenuto eliminato o contenuto che non è stato eliminato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella padre]</td> 
   <td> <p>Per eseguire la ricerca in una cartella specifica, per ogni cartella in cui si desidera eseguire la ricerca, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della cartella. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Creato Da]</td> 
   <td> <p>Per cercare le risorse create in un determinato intervallo di date, immettere la data meno recente nell'intervallo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL creato in]</td> 
   <td> <p>Per cercare le risorse create in un determinato intervallo di date, inserisci la data più recente nell’intervallo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aggiornato Da]</td> 
   <td> <p>Per cercare le risorse aggiornate in un determinato intervallo di date, immettere la data meno recente nell'intervallo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL aggiornato a]</td> 
   <td> <p>Per cercare le risorse aggiornate in un determinato intervallo di date, inserisci la data più recente nell’intervallo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Per ogni attributo che si desidera restituire nella risposta del modulo, fare clic su <b>Aggiungi elemento</b> e immettere il campo.</p><p>Può essere utilizzato per richiedere campi che normalmente non vengono restituiti in una risposta standard. Tieni presente che la specifica di questo parametro avrà l’effetto che nessuno dei campi standard viene restituito nella risposta, a meno che non sia specificato esplicitamente. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Estensioni file di </td> 
   <td> <p>Per limitare la ricerca a estensioni di file specifiche, immettere un elenco di estensioni di file separate da virgole.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size From]</td> 
   <td> <p>Per cercare le risorse in un intervallo di dimensioni specifico, inserisci il limite inferiore dell’intervallo, in byte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size To]</td> 
   <td> <p>Per cercare le risorse in un intervallo di dimensioni specifico, inserisci l’estremità più grande dell’intervallo, in byte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID utente proprietario di </td> 
   <td> <p>Per cercare le risorse di proprietà di utenti specifici, inserisci un elenco separato da virgole di ID proprietari.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di risultati che il modulo deve restituire in ogni ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>


