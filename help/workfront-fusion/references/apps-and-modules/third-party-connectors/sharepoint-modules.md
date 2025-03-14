---
title: Moduli SharePoint
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Microsoft SharePoint Online, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3124'
ht-degree: 0%

---

# Moduli SharePoint Online di Microsoft

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano Microsoft SharePoint Online, nonché collegarlo a più applicazioni e servizi di terze parti.

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

## Prerequisiti

Per utilizzare i moduli SharePoint Online di Microsoft, è necessario disporre di un account SharePoint Online di Microsoft.

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

## Connetti Microsoft SharePoint Online a [!DNL Workfront Fusion] {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Connetti Microsoft SharePoint Online a  [!DNL Workfront Fusion]  tramite un account  [!DNL Microsoft] ](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Connetti Microsoft SharePoint Online a  [!DNL Workfront Fusion]  utilizzando le impostazioni avanzate](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)

### Connetti Microsoft SharePoint Online a [!DNL Workfront Fusion] utilizzando un account [!DNL Microsoft]

È possibile utilizzare l&#39;account [!DNL Microsoft] per creare una connessione a Microsoft SharePoint Online. Per istruzioni sulla connessione dell&#39;account [!DNL Sharepoint] a [!DNL Workfront Fusion], vedere [Creare una connessione a  [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Connetti Microsoft SharePoint Online a [!DNL Workfront Fusion] utilizzando le impostazioni avanzate

Per connettere Microsoft SharePoint Online a [!DNL Workfront Fusion] senza un account [!DNL Microsoft], è necessario un ID client, un segreto client e un ID tenant.

1. Fai clic su **[!UICONTROL Aggiungi]** nella parte superiore della casella **Microsoft SharePoint Online** per aprire la casella **[!UICONTROL Crea connessione]**.

1. (Facoltativo) Modificare il nome predefinito della connessione ****.
1. Fare clic su **[!UICONTROL Mostra impostazioni avanzate]**.
1. Immetti **[!UICONTROL ID client]** e **[!UICONTROL Segreto client]** di Microsoft SharePoint Online.

1. Fai clic su **[!UICONTROL Continua]**.
1. Nella finestra di accesso visualizzata, inserisci le credenziali per accedere all’app, se non lo hai già fatto.
1. (Condizionale) Se viene visualizzato un pulsante **[!UICONTROL Consenti]**, fare clic sul pulsante per connettere l&#39;app a [!DNL Workfront Fusion].

## Moduli SharePoint Online di Microsoft e relativi campi

Quando si configurano i moduli di Microsoft SharePoint Online, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati campi SharePoint Online aggiuntivi di Microsoft, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Elemento unità](#drive-item)
* [Elemento](#item)
* [Elenco](#list)
* [Pagina (Beta)](#page-beta)
* [Sito](#site)
* [Altro](#other)

### Elemento unità

* [Creare un file](#create-a-file)
* [Creare una cartella](#create-a-folder)
* [Ottieni un file](#get-a-file)
* [Osserva elementi cartella](#watch-folder-items)

#### Creare un file

Questo modulo restituisce le modifiche apportate in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID di sito, unità e cartella]</td> 
   <td> <p>Seleziona la modalità di identificazione della posizione della cartella in cui desideri recuperare le modifiche.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID unità]</strong> e <strong>[!UICONTROL ID cartella]</strong> del percorso in cui si desidera creare il file.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Selezionare il percorso in cui si desidera creare il file. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p>
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
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID di sito, unità e cartella]</td> 
   <td> <p>Seleziona la modalità di identificazione della posizione della cartella da creare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID unità]</strong> e <strong>[!UICONTROL ID cartella]</strong> del percorso in cui si desidera creare la cartella.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Seleziona il percorso in cui desideri creare la cartella. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome cartella]</td> 
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
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID di sito, unità e cartella]</td> 
   <td> <p>Selezionare la modalità di identificazione della posizione del file che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID elenco]</strong> e <strong>[!UICONTROL ID file]</strong> per il file da recuperare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Selezionare il percorso del file. </p> </li> 
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
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID di sito, unità e cartella]</td> 
   <td> <p>Selezionare la modalità di identificazione della posizione del file che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immetti o mappa l'ID <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> e <strong>[!UICONTROL folder ID]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Seleziona il percorso della cartella da controllare. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere il numero massimo di elementi che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione dello scenario.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Elemento

* [[!UICONTROL Copia un elemento]](#copy-an-item)
* [[!UICONTROL Crea un elemento]](#create-an-item)
* [[!UICONTROL Eliminare un elemento]](#delete-an-item)
* [[!UICONTROL Ottieni un elemento]](#get-an-item)
* [[!UICONTROL Elementi elenco]](#list-items)
* [[!UICONTROL Sposta elemento]](#move-an-item)
* [[!UICONTROL Aggiorna un elemento]](#update-an-item)
* [[!UICONTROL Oggetti osservati] (pianificato)](#watch-items-scheduled)


#### [!UICONTROL Copia un elemento]

Questo modulo di azione copia un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Immetti ID sito, unità e cartella</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'unità che contiene l'elemento da copiare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID unità]</strong> e <strong>[!UICONTROL ID elemento]</strong> dell'elemento da copiare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Nel campo Tipo elemento selezionare se si sta spostando un campo o una cartella.  Selezionare il sito contenente l'elemento che si desidera copiare, quindi selezionare l'elenco, quindi selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID destinazione]</td> 
   <td> Immettere o mappare l'ID della cartella in cui si desidera copiare l'elemento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nuovo nome]</td> 
   <td>Immettere o mappare un nome per la nuova copia dell'elemento. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un elemento]

Questo modulo di azione crea un nuovo elemento in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Crea un elemento]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e il percorso in cui si desidera creare un elemento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong> e <strong>[!UICONTROL ID elenco]</strong> nel punto in cui si desidera creare l'elemento.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elenco in cui si desidera creare un elemento, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Per ogni campo che si desidera impostare per il nuovo elemento, fare clic su <b>Aggiungi elemento</b> e immettere la chiave del campo (che identifica il campo) e il valore che si desidera assegnare al nuovo elemento per il campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un elemento]

Questo modulo di azione elimina un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aggiorna un elemento]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera eliminare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID elenco]</strong> e <strong>[!UICONTROL ID elemento]</strong> dell'elemento che si desidera eliminare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera eliminare, quindi selezionare l'elenco e l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un elemento]

Questo modulo di azione restituisce i dati di un elemento specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ottiene un elemento]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID elenco]</strong> e <strong>[!UICONTROL ID elemento]</strong> dell'elemento per cui si desidera restituire i dati.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elenco dal quale si desidera recuperare un elemento, quindi selezionare l'elenco e selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elementi elenco]

Questo modulo di azione recupera un elenco di tutti gli elementi in un elenco specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL voci di elenco]</td> 
   <td> <p>Selezionare la modalità di identificazione dell'elenco da cui si desidera recuperare gli elementi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong> e <strong>[!UICONTROL ID elenco]</strong> per l'elenco per il quale si desidera elencare gli elementi.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elenco da cui si desidera recuperare gli elementi, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elementi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Sposta un elemento]

Questo modulo di azione copia un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Immetti ID sito, unità e cartella</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera spostare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID elenco]</strong> e <strong>[!UICONTROL ID elemento]</strong> per l'elemento che si desidera spostare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Nel campo Tipo elemento selezionare se si sta spostando un campo o una cartella. Selezionare il sito contenente l'elemento che si desidera copiare, quindi selezionare l'elenco, quindi selezionare l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID destinazione]</td> 
   <td> Immettere o mappare l'ID della cartella in cui si desidera spostare l'elemento. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nuovo nome]</td> 
   <td>Immettere o mappare un nome per l'elemento spostato. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un elemento]

Questo modulo di azione aggiorna un elemento esistente in un elenco SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aggiorna un elemento]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco contenente l'elemento che si desidera aggiornare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare <strong>[!UICONTROL ID sito]</strong>, <strong>[!UICONTROL ID elenco]</strong> e <strong>[!UICONTROL ID elemento]</strong> dell'elemento da aggiornare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera aggiornare, quindi selezionare l'elenco e l'elemento. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Per ogni campo che si desidera aggiornare per il nuovo elemento, fare clic su <b>Aggiungi elemento</b> e immettere la chiave del campo (che identifica il campo) e il nuovo valore che si desidera assegnare all'elemento per il campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Oggetti osservati] (pianificato)

Questo modulo di attivazione avvia uno scenario quando un elemento viene creato o modificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elenchi di controllo]</td> 
   <td>Seleziona se desideri controllare gli elenchi in base all’ora di creazione (nuovi elementi) o di modifica (elementi aggiornati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID sito ed elenco]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che si desidera controllare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID sito <strong>[!UICONTROL]</strong> e l'ID elenco <strong>[!UICONTROL]</strong> che si desidera controllare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Seleziona il sito da monitorare, quindi fai clic sull’elenco. Questi menu a discesa recuperano solo i siti seguiti.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elementi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Elenco

* [[!UICONTROL Crea un elenco]](#create-a-list)
* [[!UICONTROL Ottieni un elenco]](#get-a-list)
* [[!UICONTROL Elenchi]](#list-lists)
* [[!UICONTROL Elenchi di controllo]](#watch-lists)

#### [!UICONTROL Crea un elenco]

Questo modulo di azione crea un nuovo elenco in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti un ID sito]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito in cui si desidera creare un elenco.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID sito <strong>[!UICONTROL]</strong> in cui si desidera creare un elenco.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito in cui si desidera creare un elenco. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome visualizzato]</td> 
   <td>Immettere o mappare un nome per il nuovo elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td>Immettere o mappare una descrizione per il nuovo elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aggiungi colonne]</td> 
   <td>Per ogni colonna che si desidera impostare per il nuovo elenco, fare clic su <b>Aggiungi elemento </b>, immettere un <strong>[!UICONTROL Name]</strong> per il campo e selezionare il <strong>[!UICONTROL Type]</strong> del valore che si desidera assegnare alla nuova colonna.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un elenco]

Questo modulo di azione restituisce i dati di un elenco specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ottiene un elenco]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'elenco che contiene l'elemento che si desidera ottenere.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'<strong>[!UICONTROL ID sito]</strong> e l'<strong>ID elenco</strong> che si desidera restituire.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elenco che si desidera recuperare, quindi selezionare l'elenco. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenchi]

Questo modulo di azione recupera un elenco di tutti gli elementi in un sito specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elenchi]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito da cui si desidera recuperare gli elenchi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID sito <strong>[!UICONTROL]</strong> contenente gli elenchi che si desidera restituire.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente gli elenchi che si desidera recuperare. Il menu a discesa recupera solo i siti che segui.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di elenchi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenchi di controllo]

Questo modulo di attivazione avvia uno scenario quando viene creato o modificato un elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elenchi di controllo]</td> 
   <td>Seleziona se desideri controllare gli elenchi in base all’ora di creazione (nuovi elementi) o di modifica (elementi aggiornati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID sito]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito da controllare per gli elenchi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immetti o mappa l'ID sito <strong>[!UICONTROL]</strong> in cui desideri guardare gli elenchi.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco che segui]</strong> </p> <p>Seleziona il sito da monitorare. L’elenco a discesa recupera solo il sito che segui.</p> </li> 
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

#### [!UICONTROL Ottieni una pagina]

Questo modulo di azione restituisce i dati di una pagina specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ottieni pagina]</td> 
   <td> <p>Seleziona la modalità di identificazione della pagina da recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immetti o mappa l'ID sito <strong>[!UICONTROL]</strong>e l'ID pagina <strong>[!UICONTROL]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona il sito contenente la pagina da recuperare, quindi fai clic sulla pagina.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Sito

* [[!UICONTROL Ottieni sito]](#get-a-site)
* [[!UICONTROL Cerca siti]](#search-sites)

#### [!UICONTROL Ottieni sito]

Questo modulo di azione restituisce i dati di un sito specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ottieni sito]</td> 
   <td> <p>Seleziona la modalità di identificazione della pagina da recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID sito <strong>[!UICONTROL]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona il sito da recuperare.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca siti]

Questo modulo di azione cerca i siti in base a un parametro specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Parola chiave [!UICONTROL del nome visualizzato]</td> 
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
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immetti ID di sito, unità e cartella]</td> 
   <td> <p>Selezionare la modalità di identificazione del sito e dell'unità che contiene l'elemento che si desidera aggiornare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID sito <strong>[!UICONTROL]</strong>, <strong>[!UICONTROL ID unità]</strong> e <strong>[!UICONTROL ID cartella]</strong> nei campi visualizzati.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare il sito contenente l'elemento che si desidera aggiornare, quindi selezionare l'unità e la cartella. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Il token identifica da quale punto il modulo deve iniziare a recuperare le modifiche.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft SharePoint Online a [!DNL Workfront Fusion], vedere <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connettere Microsoft SharePoint Online a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
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
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona un webhook esistente oppure fai clic su Aggiungi e immetti la connessione per crearne uno nuovo.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
