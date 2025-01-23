---
title: Moduli DevOps di Azure
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Azure DevOps], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 0%

---

# [!DNL Azure DevOps] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Azure DevOps] e collegarlo a più applicazioni e servizi di terze parti.

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

## Connetti [!DNL Azure DevOps] a [!DNL Workfront Fusion] {#connect-azure-devops-to-workfront-fusion}

1. Aggiungi un modulo [!DNL Azure DevOps] allo scenario.
1. Fare clic su **[!UICONTROL Add]** accanto al campo [!UICONTROL Connection].
1. Nel campo [!UICONTROL Connection Type], selezionare **[!DNL Azure DevOps]**.

   >[!IMPORTANT]
   >
   >Il tipo di connessione [!UICONTROL [!DNL Azure DevOps] (Request All Scopes)] diventerà obsoleto nel prossimo futuro. Pertanto, si sconsiglia di utilizzarlo.

1. Compila i campi seguenti:

   <table style="table-layout:auto">
        <tr>
            <td>[!UICONTROL Connection name]</td>
            <td>Immettere un nome per la connessione che si sta creando.</td>
        </tr>
      <tr>
            <td>[!UICONTROL Organization]</td>
            <td>Immettere il nome dell'organizzazione con cui è stata creata l'applicazione [!DNL Azure DevOps].</td>
        </tr>
    </table>

1. Fai clic su **[!UICONTROL Continue]** per completare la configurazione della connessione e continuare a creare lo scenario.

## [!UICONTROL Azure DevOps] moduli e relativi campi

Quando configuri [!DNL Azure DevOps] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Azure DevOps], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### [!UICONTROL Watch for work items]

Questo modulo di attivazione immediata esegue uno scenario quando un record viene aggiunto, aggiornato o eliminato in [!UICONTROL Azure DevOps].

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona o aggiungi un webhook per il modulo.</p> <!--<p>For more information on webhooks in trigger modules, see <a href="For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/)." class="MCXref xref">Instant triggers (webhooks) in [!DNL Adobe Workfront Fusion]</a>.</p> <p>For information on how to create a webhook, see <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.--></p> </td> 
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
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)

#### [!UICONTROL Custom API Call]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Azure DevOps]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Azure DevOps].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td> <p>Selezionare o mappare l'URL di base utilizzato per connettersi all'account [!DNL Azure DevOps]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>Immetti l’URL relativo a cui desideri connetterti per questa chiamata API.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selezionare o mappare la versione dell'API [!DNL Azure DevOps] a cui connettersi per questa chiamata API. Se non è selezionata alcuna versione, [!DNL Workfront Fusion] si connette alla versione 5.1 dell'API [!DNL Azure DevOps].</td> 
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
   <td role="rowheader">[!UICONTROL Query String]</td> 
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

#### [!UICONTROL Create a record]

Questo modulo di azione crea un nuovo progetto o elemento di lavoro.

Il modulo restituisce l’ID oggetto per il nuovo elemento di lavoro creato oppure l’URL e il codice di stato di un progetto appena creato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Specificare se si desidera creare un elemento di lavoro o un progetto.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: immetti o mappa un nome per il nuovo progetto.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: immetti o mappa una descrizione per il nuovo progetto. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: seleziona se desideri che il progetto sia pubblico o privato. Per interagire con un progetto privato, gli utenti devono aver effettuato l’accesso alla tua organizzazione e disporre dell’accesso al progetto. I progetti pubblici sono visibili agli utenti che non hanno effettuato l'accesso all'organizzazione.</p> </li> 
       <li> <p><strong>[!UICONTROL Version control]</strong>: seleziona se desideri che il progetto utilizzi [!DNL Git] o [!UICONTROL Team Foundation Version Control (TFCV)] per il controllo della versione.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item process]</strong>: seleziona il processo di lavoro da utilizzare per il progetto. Le opzioni sono [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] e [!UICONTROL Agile].</p> <p>Per ulteriori informazioni sui processi [!DNL Azure DevOps], vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">Scegliere un processo</a> nella documentazione di [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: selezionare il progetto in cui si desidera creare l'elemento di lavoro.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item type]</strong>: seleziona il tipo di elemento di lavoro da creare.</p> </li> 
       <li> <p><strong>[!UICONTROL Other fields]</strong>:In questi campi immettere il valore che si desidera assegnare all'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Questo modulo di azione scarica un allegato.

Il modulo restituisce il contenuto del file dell’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment URL]</td> 
   <td> <p>Inserisci o mappa l’URL dell’allegato da scaricare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Link work items]

Questo modulo di azione collega due elementi di lavoro e definisce la relazione tra di essi.

Il modulo restituisce l’ID dell’elemento di lavoro principale e di tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro principale a cui si desidera collegare un altro elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked work item ID]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera collegare all'elemento di lavoro principale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link Type]</td> 
   <td> <p>Definire la relazione tra gli elementi di lavoro da collegare.</p> <p>Per ulteriori informazioni, vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Riferimento tipo collegamento</a> nella documentazione di [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Immettere o mappare il testo di un commento. Ciò è utile per spiegare il ragionamento o l’intenzione del collegamento.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read record]

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Seleziona se desideri leggere un progetto o un elemento di lavoro</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: seleziona il progetto da leggere.</p> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong>: selezionare il progetto che contiene l'elemento di lavoro che si desidera leggere, quindi selezionare il tipo di elemento di lavoro.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID del record da leggere.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a work item]

Questo modulo di azione aggiorna un elemento di lavoro esistente utilizzando il relativo ID.

Il modulo restituisce l’ID dell’elemento di lavoro aggiornato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selezionare il progetto contenente l'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work Item Type]</td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other Fields]</td> 
   <td>In ciascuno di questi campi immettere il valore che si desidera assegnare all'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

Questo modulo di azione carica un file e lo allega a un elemento di lavoro.

Il modulo restituisce l’ID dell’allegato e un URL di download per l’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project] </td> 
   <td> <p>Seleziona il progetto in cui desideri caricare un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
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

#### [!UICONTROL List work items]

Questo modulo di azione recupera tutti gli elementi di lavoro di un tipo specifico in un progetto [!DNL Azure DevOps].

Il modulo restituisce l’ID dell’elemento di lavoro principale e di tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a [!DNL Workfront Fusion], vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selezionare il progetto dal quale si desidera recuperare gli elementi di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item type]</td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. I campi disponibili dipendono dal tipo di elemento di lavoro che si desidera recuperare. Selezionare almeno una proprietà.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi di lavoro restituiti da [!DNL Workfront Fusion] durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>
