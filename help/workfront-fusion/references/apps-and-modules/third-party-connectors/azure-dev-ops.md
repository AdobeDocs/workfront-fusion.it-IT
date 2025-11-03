---
title: Moduli DevOps di Azure
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Azure DevOps], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 0%

---

# [!DNL Azure DevOps] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Azure DevOps] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Azure DevOps], è necessario disporre di un account DevOps [!DNL Azure].

## Informazioni API di [!DNL Azure DevOps]

Il connettore DevOps di Azure utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Connetti [!DNL Azure DevOps] a Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

1. Aggiungi un modulo [!DNL Azure DevOps] allo scenario.
1. Fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Nel campo [!UICONTROL Tipo di connessione], selezionare il tipo di connessione che si desidera utilizzare.

   >[!NOTE]
   >
   >[!UICONTROL [!DNL Azure DevOps] (EntraApp)] consente di richiedere tutti gli ambiti per la connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Nome connessione]</td>
            <td>Immettere un nome per la connessione che si sta creando.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organizzazione]</td>
            <td>Immettere il nome dell'organizzazione con cui è stata creata l'applicazione [!DNL Azure DevOps].</td>
      </tr>
      <tr>
            <td>[!UICONTROL ID app]</td>
            <td>Immettere l'ID dell'applicazione DevOps a cui ci si connette.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Segreto client]</td>
            <td>Immettere il segreto client per le applicazioni DevOps a cui ci si connette.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Richiedi tutti gli ambiti]</td>
            <td>Se si utilizza il tipo di connessione [!DNL Azure DevOps] (EntraApp), abilitare questa opzione per richiedere tutti gli ambiti per la connessione.</td>
      </tr>
   </table>

1. Per immettere un ID app o un segreto client di Azure DevOps, fare clic su <b>Mostra impostazioni avanzate</b> e immetterle nei campi aperti.
1. Fai clic su **[!UICONTROL Continua]** per completare la configurazione della connessione e continuare a creare lo scenario.

## [!UICONTROL Moduli DevOps di Azure] e relativi campi

Quando si configurano [!DNL Azure DevOps] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Azure DevOps], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### [!UICONTROL Controlla elementi di lavoro]

Questo modulo di attivazione immediata esegue uno scenario quando un record viene aggiunto, aggiornato o eliminato in [!UICONTROL Azure DevOps].

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona o aggiungi un webhook per il modulo.</p> <p>Per ulteriori informazioni sui webhook nei moduli trigger, vedere <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Trigger istantanei (webhook)</a>.</p> <p>Per informazioni su come creare un webhook, vedere <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [Creare un record](#create-a-record)
* [Chiamata API personalizzata](#custom-api-call)
* [Scaricare un allegato](#download-an-attachment)
* [Collega elementi di lavoro](#link-work-items)
* [Leggi record](#read-record)
* [Aggiornare un elemento di lavoro](#update-a-work-item)
* [[!UICONTROL Carica un allegato]](#upload-an-attachment)

#### [!UICONTROL Crea un record]

Questo modulo di azione crea un nuovo progetto o elemento di lavoro.

Il modulo restituisce l’ID oggetto per il nuovo elemento di lavoro creato oppure l’URL e il codice di stato di un progetto appena creato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Specificare se si desidera creare un elemento di lavoro o un progetto.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Progetto]</strong> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: immettere o mappare un nome per il nuovo progetto.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: immettere o mappare una descrizione per il nuovo progetto. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: specificare se il progetto deve essere pubblico o privato. Per interagire con un progetto privato, gli utenti devono aver effettuato l’accesso alla tua organizzazione e disporre dell’accesso al progetto. I progetti pubblici sono visibili agli utenti che non hanno effettuato l'accesso all'organizzazione.</p> </li> 
       <li> <p><strong>[!UICONTROL Controllo della versione]</strong>: specificare se si desidera che il progetto utilizzi [!DNL Git] o [!UICONTROL Controllo della versione di Team Foundation (TFCV)] per il controllo della versione.</p> </li> 
       <li> <p><strong>[!UICONTROL Processo elemento di lavoro]</strong>: selezionare il processo di lavoro da utilizzare per il progetto. Le opzioni sono [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] e [!UICONTROL Agile].</p> <p>Per ulteriori informazioni sui processi [!DNL Azure DevOps], vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=basic-process">Processi predefiniti e modelli di processo</a> nella documentazione di [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Elemento di lavoro]</strong> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: selezionare il progetto in cui si desidera creare l'elemento di lavoro.</p> </li> 
       <li> <p><strong>[!UICONTROL Tipo di elemento di lavoro]</strong>: selezionare il tipo di elemento di lavoro da creare.</p> </li> 
       <li> <p><strong>[!UICONTROL Altri campi]</strong>: in questi campi immettere il valore desiderato per l'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Azure DevOps]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Azure DevOps].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL di base]</td> 
   <td> <p>Selezionare o mappare l'URL di base utilizzato per connettersi all'account [!DNL Azure DevOps]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL relativo]</td> 
   <td> <p>Immetti l’URL relativo a cui desideri connetterti per questa chiamata API.</p> <p><b>Esempio: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL versione API]</td> 
   <td>Selezionare o mappare la versione dell'API [!DNL Azure DevOps] a cui connettersi per questa chiamata API. Se non è selezionata alcuna versione, Workfront Fusion si connette alla versione 5.1 dell'API [!DNL Azure DevOps].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
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

#### [!UICONTROL Scarica un allegato]

Questo modulo di azione scarica un allegato.

Il modulo restituisce il contenuto del file dell’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL allegato]</td> 
   <td> <p>Inserisci o mappa l’URL dell’allegato da scaricare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Collega elementi di lavoro]

Questo modulo di azione collega due elementi di lavoro e definisce la relazione tra di essi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro principale a cui si desidera collegare un altro elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked Work Item ID]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera collegare all'elemento di lavoro principale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di collegamento]</td> 
   <td> <p>Definire la relazione tra gli elementi di lavoro da collegare.</p> <p>Per ulteriori informazioni, vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Guida di riferimento per i tipi di collegamento</a> nella documentazione di [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Immettere o mappare il testo di un commento. Ciò è utile per spiegare il ragionamento o l’intenzione del collegamento.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi record]

Questo modulo di azione legge i dati da un singolo record in [!DNL Azure DevOps].

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri leggere un progetto o un elemento di lavoro</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: selezionare il progetto che si desidera leggere.</p> </li> 
     <li> <p><strong>[!UICONTROL Elemento di lavoro]</strong>: selezionare il progetto che contiene l'elemento di lavoro che si desidera leggere, quindi selezionare il tipo di elemento di lavoro.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID del record da leggere.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un elemento di lavoro]

Questo modulo di azione aggiorna un elemento di lavoro esistente utilizzando il relativo ID.

Il modulo restituisce l’ID dell’elemento di lavoro aggiornato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Progetto </td> 
   <td>Selezionare il progetto contenente l'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di elemento di lavoro </td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altri Campi]</td> 
   <td>In ciascuno di questi campi immettere il valore che si desidera assegnare all'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un allegato]

Questo modulo di azione carica un file e lo allega a un elemento di lavoro.

Il modulo restituisce l’ID dell’allegato e un URL di download per l’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Progetto  </td> 
   <td> <p>Seleziona il progetto in cui desideri caricare un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td> <p>Inserisci o mappa l’ID dell’elemento di lavoro in cui desideri caricare un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Immettere il testo di un commento da aggiungere all'allegato caricato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td> 
   <td>Selezionare un file di origine da un modulo precedente oppure immettere o mappare il nome e il contenuto del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Elencare elementi di lavoro]

Questo modulo di azione recupera tutti gli elementi di lavoro di un tipo specifico in un progetto [!DNL Azure DevOps].

Il modulo restituisce l’ID dell’elemento di lavoro principale e di tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Progetto </td> 
   <td>Selezionare il progetto dal quale si desidera recuperare gli elementi di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di elemento di lavoro]</td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. I campi disponibili dipendono dal tipo di elemento di lavoro che si desidera recuperare. Selezionare almeno una proprietà.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi di lavoro restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>
