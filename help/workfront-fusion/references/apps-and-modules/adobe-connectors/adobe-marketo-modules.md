---
title: Moduli Marketo
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Marketo], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1740'
ht-degree: 0%

---

# [!DNL Marketo] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Marketo] e collegarlo a più applicazioni e servizi di terze parti.

Per un video introduttivo sul connettore Marketo, vedi:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

Per utilizzare i moduli [!DNL Marketo], è necessario disporre di un account [!DNL Marketo].

## Informazioni API di Marketo

Il connettore Marketo utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Marketo] a Workfront Fusion {#connect-marketo-to-workfront-fusion}

Puoi creare una connessione al tuo account [!DNL Marketo] direttamente dal modulo [!DNL Marketo].

1. In qualsiasi modulo [!DNL Marketo], fare clic su **[!UICONTROL Add]** accanto al campo [!UICONTROL Connection].
1. Immetti l&#39;account [!DNL Marketo] o l&#39;ID [!DNL Marketo] [!UICONTROL Munchkin]. Parte univoca dell&#39;URL di base o dell&#39;endpoint assegnato all&#39;account, utilizzata per accedere a [!DNL Marketo] tramite l&#39;API [!UICONTROL REST]. Per istruzioni su come individuare questo elemento, vedere [URL di base](https://developers.marketo.com/rest-api/base-url/) nella documentazione di [!DNL Marketo].
1. Immettere [!UICONTROL Client ID] e [!UICONTROL Client secret]. Per istruzioni su come individuarli, vedere [Autenticazione](https://developers.marketo.com/rest-api/authentication/) nella documentazione di [!DNL Marketo].
1. Fare clic su **[!UICONTROL Continue]** per creare la connessione e tornare al modulo.

## [!DNL Marketo] moduli e relativi campi

Quando configuri [!DNL Marketo] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Marketo], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Triggers

* [[!UICONTROL Watch events (Instant)]](#watch-events-instant)
* [[!UICONTROL Watch records]](#watch-records)

#### [!UICONTROL Watch events (Instant)]

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Immetti il webhook che desideri venga utilizzato dal modulo.</p> <p>Per ulteriori informazioni sui webhook, vedere <!--<a href="For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->" class="MCXref xref"&gt;Trigger istantanei (webhook) in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch records]

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Seleziona il tipo di attività da monitorare. </p> <p>Il modulo controlla solo le nuove attività.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Specificare se si desidera controllare i nuovi record, i record aggiornati, i record nuovi e aggiornati o gli aggiornamenti specifici dei campi. Se selezioni di controllare specifici aggiornamenti del campo, seleziona il campo che desideri che il modulo controlli.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>Specificare se si desidera controllare i nuovi record, i record aggiornati o i record nuovi e aggiornati.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Add Leads to a List]](#add-leads-to-a-list)
* [[!UICONTROL Clone a Program]](#clone-a-program)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API call]](#custom-api-call)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Remove Leads from a List]](#remove-leads-from-a-list)
* [[!UICONTROL Schedule a Campaign]](#schedule-a-campaign)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Add Leads to a List]

Questo modulo di azione aggiunge uno o più lead a un elenco, utilizzando l’ID lead.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Immettere o mappare l'ID dell'elenco in cui si desidera aggiungere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Per ogni lead che si desidera aggiungere all'elenco, fare clic su <b>[!UICONTROL Add]</b>, quindi immettere o mappare l'ID del lead che si desidera aggiungere. Puoi aggiungere fino a 300 lead per il modulo da aggiungere all’elenco.</p> <p>Fare clic sull'interruttore Mappa per mappare una raccolta esistente di lead che si desidera aggiungere all'elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clone a Program]

Questo modulo di azione crea una copia di un programma utilizzando l’ID del programma esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>Immetti o mappa l’ID del programma da copiare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>Immettere o mappare un nome per il nuovo programma</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Immettere o mappare l'ID della cartella in cui si desidera posizionare il nuovo programma.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

Questo modulo azioni crea un nuovo record in [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se si sta creando una società o un lead, selezionare i campi per i quali si desidera impostare i valori al momento della creazione del nuovo record, quindi immettere i valori per questi campi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>Se si sta creando un programma, selezionare il tipo di programma da creare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>Se si sta creando un programma, selezionare il canale in cui si desidera creare il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>Se si sta creando una cartella o un programma, immettere o associare un nome per il nuovo record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se si sta creando una cartella o un programma, immettere o mappare una descrizione per il nuovo record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>Se si sta creando una cartella o un programma, immettere o mappare l'ID della cartella principale in cui si desidera creare il nuovo record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se stai creando un programma, aggiungi eventuali costi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se stai creando un programma, aggiungi eventuali tag</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API call]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Marketo]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record con cui si desidera lavorare il modulo durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Questo modulo di azione scarica un file utilizzando l’ID file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Mappa l’ID del file da scaricare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Questo modulo di azione legge le informazioni su un record utilizzando il relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi sono disponibili in base a [!UICONTROL Record Type] selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Object> ID]</td> 
   <td>Immetti o mappa l’ID dell’oggetto di cui desideri recuperare le informazioni.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

Questo modulo di azione rimuove uno o più lead da un elenco, utilizzando l’ID lead.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Immettere o mappare l'ID dell'elenco in cui si desidera rimuovere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Per ogni lead che si desidera rimuovere dall'elenco, fare clic su <b>[!UICONTROL Add]</b>, quindi immettere o mappare l'ID del lead che si desidera rimuovere. Puoi aggiungere fino a 300 lead per il modulo da rimuovere dall’elenco. </p> <p>Fare clic sull'interruttore Mappa per mappare una raccolta esistente di lead che si desidera rimuovere dall'elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schedule a Campaign]

Questo modulo di azione pianifica una campagna esistente per una determinata data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Immetti o mappa l’ID della campagna da pianificare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Seleziona la data in cui desideri eseguire la campagna. Se questo campo viene lasciato vuoto, la campagna viene eseguita cinque minuti dopo l’inizio dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Questo modulo di azione aggiorna un record esistente utilizzando il relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>Immetti o mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Se si sta aggiornando una società o un lead, selezionare i campi per i quali si desidera aggiornare i valori, quindi immettere i valori per questi campi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Se si sta aggiornando un programma, immettere o mappare un nuovo nome per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Se si sta aggiornando un programma, immettere o mappare una nuova descrizione del programma.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Se si sta aggiornando un programma, immettere o mappare una nuova data di inizio per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Se si sta aggiornando un programma, immettere o mappare una nuova data di fine per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Se stai aggiornando un programma, aggiungi eventuali costi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Se stai aggiornando un programma, aggiungi eventuali tag</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Questo modulo azioni carica un nuovo file in [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Immettere o mappare l'ID della cartella in cui si desidera posizionare il nuovo file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Inserisci una descrizione del file caricato.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search Records]](#update-a-record)

#### [!UICONTROL List records]

Questo modulo di azione recupera tutti i record di un tipo specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da elencare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Se si è scelto di recuperare i lead, selezionare se si desidera recuperare i lead da un elenco o da un programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi sono disponibili in base a [!UICONTROL Record Type] selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Records]

Questo modulo di ricerca recupera un elenco di record che corrispondono a criteri di ricerca specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a [!DNL Workfront Fusion], vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Marketo] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selezionare il tipo di record che si desidera cercare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Specificare se si desidera eseguire la ricerca per nome, nome del programma o nome dell'area di lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td>Per ogni valore che si desidera cercare, fare clic su <b>[!UICONTROL Add item]</b> e immettere il valore.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>
