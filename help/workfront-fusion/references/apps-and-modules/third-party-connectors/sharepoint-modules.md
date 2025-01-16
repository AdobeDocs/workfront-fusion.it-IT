---
title: Moduli SharePoint
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano SharePoint e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---

# [!DNL SharePoint] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL SharePoint] e collegarlo a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL SharePoint], è necessario disporre di un account [!DNL SharePoint].

## Informazioni API di SharePoint

Il connettore SharePoint utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL SharePoint] a [!DNL Workfront Fusion] {#connect-sharepoint-to-workfront-fusion}

* [Connetti [!DNL SharePoint] a [!DNL Workfront Fusion] tramite un account [!DNL Microsoft] ](#connect-sharepoint-to-workfront-fusion-using-a-microsoft-account)
* [Connetti [!DNL SharePoint] a [!DNL Workfront Fusion] tramite impostazioni avanzate](#connect-sharepoint-to-workfront-fusion-using-advanced-settings)

### Connetti [!DNL SharePoint] a [!DNL Workfront Fusion] utilizzando un account [!DNL Microsoft]

Puoi usare il tuo account [!DNL Microsoft] per creare una connessione a [!DNL SharePoint]. Per istruzioni sulla connessione dell&#39;account [!DNL Sharepoint] a [!DNL Workfront Fusion], vedere [Creare una connessione a  [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Connetti [!DNL SharePoint] a [!DNL Workfront Fusion] utilizzando le impostazioni avanzate

Per connettere [!DNL SharePoint] a [!DNL Workfront Fusion] senza un account [!DNL Microsoft], è necessario un ID client, un segreto client e un ID tenant.

1. Fare clic su **[!UICONTROL Add]** nella parte superiore della casella **[!DNL SharePoint]** per aprire la casella **[!UICONTROL Create a connection]**.

1. (Facoltativo) Modificare il valore predefinito **[!UICONTROL Connection name]**.
1. Fare clic su **[!UICONTROL Show advanced settings]**.
1. Immettere [!DNL SharePoint] **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

1. Fare clic su **[!UICONTROL Continue]**.
1. Nella finestra di accesso visualizzata, inserisci le credenziali per accedere all’app, se non lo hai già fatto.
1. (Condizionale) Se viene visualizzato un pulsante **[!UICONTROL Allow]**, fare clic sul pulsante per connettere l&#39;app a [!DNL Workfront Fusion].

## [!DNL SharePoint] moduli e relativi campi

Quando configuri [!DNL SharePoint] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL SharePoint], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Elemento unità](#drive-item)
* [Voce](#item)
* [Elenco](#list)
* [Pagina (Beta)](#page-beta)
* [Sito](#site)
* [Altro](#other)

### Elemento unità

* [Creare un file](#create-a-file)
* [Creare una cartella](#create-a-folder)
* [Ottieni un file](#get-a-file)
* [Osserva elementi cartella](#watch-folder-items)

#### Ottieni modifiche

Questo modulo restituisce le modifiche apportate in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Seleziona la modalità di identificazione della posizione della cartella in cui desideri recuperare le modifiche.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Folder ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Seleziona il percorso in cui desideri recuperare le modifiche. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> </td> 
  </tr>  </tbody> 
</table>

#### Creare una cartella

Questo modulo di azione crea una nuova cartella in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Seleziona la modalità di identificazione della posizione della cartella da creare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Folder ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Seleziona il percorso in cui desideri creare la cartella. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>Immettere o mappare un nome per la nuova cartella.</td> 
  </tr>
  </tbody> 
</table>

#### Ottieni un file

Questo modulo di azione recupera il file SharePoint specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selezionare la modalità di identificazione della posizione del file che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL File ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selezionare il percorso del file. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Osserva elementi cartella

Questo modulo di attivazione avvia uno scenario quando un elemento viene aggiornato in una cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selezionare la modalità di identificazione della posizione del file che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL folder ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Seleziona il percorso della cartella da controllare. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere il numero massimo di elementi che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione dello scenario.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Voce

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move Item]](#move-an-item)
* [[!UICONTROL Update an item]](#update-an-item)
* [[!UICONTROL Watch Items] (pianificato)](#watch-items-scheduled)


#### [!UICONTROL Copy Item]

Questo modulo di azione copia un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Immetti ID sito, unità e cartella</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco contenente l'elemento che si desidera copiare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Item ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Nel campo Tipo elemento selezionare se si sta spostando un campo o una cartella.  Selezionare il sito contenente l'elemento che si desidera copiare, quindi selezionare l'elenco, quindi selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Immettere o mappare l'ID della cartella in cui si desidera copiare l'elemento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Immettere o mappare un nome per la nuova copia dell'elemento. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an item]

Questo modulo di azione crea un nuovo elemento in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco in cui si desidera creare un elemento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> e <strong>[!UICONTROL List ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elenco in cui si desidera creare un elemento, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Per ogni campo che si desidera impostare per il nuovo elemento, immettere la chiave del campo (identifica il campo) e il valore che si desidera assegnare al nuovo elemento per tale campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

Questo modulo di azione elimina un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera eliminare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Item ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera eliminare, quindi selezionare l'elenco e l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

Questo modulo di azione restituisce i dati di un elemento specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Item ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elenco dal quale si desidera recuperare un elemento, quindi selezionare l'elenco e selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Items]

Questo modulo di azione recupera un elenco di tutti gli elementi in un elenco specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Selezionare la modalità di identificazione dell'elenco da cui si desidera recuperare gli elementi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> e <strong>[!UICONTROL List ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elenco da cui si desidera recuperare gli elementi, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elementi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

Questo modulo di azione copia un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Immetti ID sito, unità e cartella</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera spostare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Item ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Nel campo Tipo elemento selezionare se si sta spostando un campo o una cartella. Selezionare il sito contenente l'elemento che si desidera copiare, quindi selezionare l'elenco, quindi selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Immettere o mappare l'ID della cartella in cui si desidera spostare l'elemento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Immettere o mappare un nome per l'elemento spostato. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an item]

Questo modulo di azione aggiorna un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco contenente l'elemento che si desidera aggiornare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL Item ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera aggiornare, quindi selezionare l'elenco e l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Per ogni campo che si desidera aggiornare per il nuovo elemento, immettere la chiave del campo (identifica il campo) e il nuovo valore che si desidera assegnare all'elemento per tale campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] (pianificato)

Questo modulo di attivazione avvia uno scenario quando un elemento viene creato o modificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Seleziona se desideri controllare gli elenchi in base all’ora di creazione (nuovi elementi) o di modifica (elementi aggiornati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che si desidera controllare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> e <strong>[!UICONTROL List ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Seleziona il sito da monitorare, quindi fai clic sull’elenco. Questi menu a discesa recuperano solo i siti seguiti.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elementi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Elenco

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

Questo modulo di azione crea un nuovo elenco in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco in cui si desidera creare un elenco.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> nel punto in cui si desidera creare un elenco.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito in cui si desidera creare un elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>Immettere o mappare un nome per il nuovo elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione per il nuovo elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>Per ogni colonna che si desidera impostare per il nuovo elenco, immettere <strong>[!UICONTROL Name]</strong> per il campo e selezionare <strong>[!UICONTROL Type]</strong> di valore da assegnare alla nuova colonna.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

Questo modulo di azione restituisce i dati di un elenco specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> e <strong>ID elenco</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elenco che si desidera recuperare, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

Questo modulo di azione recupera un elenco di tutti gli elementi in un elenco specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito da cui si desidera recuperare gli elenchi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente gli elenchi che si desidera recuperare. Il menu a discesa recupera solo i siti che segui.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elenchi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

Questo modulo di attivazione avvia uno scenario quando viene creato o modificato un elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Seleziona se desideri controllare gli elenchi in base all’ora di creazione (nuovi elementi) o di modifica (elementi aggiornati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che si desidera controllare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> dove si trova l'elenco che si desidera controllare.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Seleziona il sito da monitorare. L’elenco a discesa recupera solo il sito che segui.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elenchi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pagina (Beta)

>[!NOTE]
>
>Le API nella versione `beta` in [!DNL Microsoft Graph] sono soggette a modifiche. L’utilizzo di queste API nelle applicazioni di produzione non è supportato.

#### [!UICONTROL Get a Page]

Questo modulo di azione restituisce i dati di una pagina specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Seleziona la modalità di identificazione della pagina da recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong> e <strong>[!UICONTROL Page ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Seleziona il sito contenente la pagina da recuperare, quindi fai clic sulla pagina.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Sito

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

Questo modulo di azione restituisce i dati di un sito specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Seleziona la modalità di identificazione della pagina da recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Seleziona il sito da recuperare.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

Questo modulo di azione cerca i siti in base a un parametro specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>Immettere o mappare il termine di ricerca che si desidera cercare nei siti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di siti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [Ottieni modifiche](#get-changes)
* [Effettuare una chiamata API](#make-an-api-call)
* [Guarda gli eventi](#watch-events)

#### Ottieni modifiche

Questo modulo recupera le aggiunte, gli aggiornamenti e le eliminazioni effettuati nella cartella SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco contenente l'elemento che si desidera aggiornare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> e <strong>[!UICONTROL Folder ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera aggiornare, quindi selezionare l'unità e la cartella. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Il token identifica da quale punto il modulo deve iniziare a recuperare le modifiche.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL SharePoint] a [!DNL Workfront Fusion], vedere <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL SharePoint] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Seleziona il tipo di dati da inviare nella chiamata API.</td> 
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

#### Guarda gli eventi

Questo modulo di attivazione immediata avvia uno scenario quando un elemento viene aggiunto, aggiornato o eliminato in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL SharePoint] account to [!DNL Workfront Fusion], see <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect [!DNL SharePoint] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona un webhook esistente oppure fai clic su Aggiungi per crearne uno nuovo.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
