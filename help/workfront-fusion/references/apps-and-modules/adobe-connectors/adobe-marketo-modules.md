---
title: Moduli Marketo
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Marketo], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2237'
ht-degree: 0%

---

# [!DNL Marketo] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Marketo] e collegarlo a più applicazioni e servizi di terze parti.

Per un video introduttivo sul connettore Marketo, vedi:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

Puoi creare una connessione al tuo account [!DNL Marketo] direttamente da qualsiasi modulo di [!DNL Marketo].

1. In qualsiasi modulo di Marketo, fai clic su **Aggiungi** accanto al campo Connessione.
1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Nome connessione]</td>
        <td>
          <p>Immettere un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Specificare se ci si connette a un account di servizio o a un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Account [!UICONTROL / ID Munchkin]</td>
        <td>
          <p>Immetti l'account [!DNL Marketo] o l'ID [!DNL Marketo] di [!UICONTROL Munchkin]. Parte univoca dell'URL di base o dell'endpoint assegnato all'account, utilizzata per accedere a [!DNL Marketo] tramite l'API REST di . Per istruzioni su come individuare questa posizione, vedere [URL di base](https://developers.marketo.com/rest-api/base-url/) nella documentazione di [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti l'ID client di Marketo. Per istruzioni su come individuare questo elemento, vedere [Authentication](https://developers.marketo.com/rest-api/authentication/) nella documentazione di [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti il segreto client Marketo. Per istruzioni su come individuarli, vedere [Authentication](https://developers.marketo.com/rest-api/authentication/) nella documentazione di [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## [!DNL Marketo] moduli e relativi campi

Quando si configurano [!DNL Marketo] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Marketo], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [[!UICONTROL Guarda gli eventi (istantanei)]](#watch-events-instant)
* [[!UICONTROL Osserva record]](#watch-records)

#### [!UICONTROL Guarda gli eventi (istantanei)]

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Immetti il webhook che desideri venga utilizzato dal modulo.</p> <p>Per ulteriori informazioni sui webhook, vedere <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Osserva record]

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Attività]</strong> </p> <p>Seleziona il tipo di attività da monitorare. </p> <p>Il modulo controlla solo le nuove attività.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Nel campo <b>Tipo evento</b>, selezionare se si desidera controllare nuovi record, record aggiornati, record nuovi e aggiornati o aggiornamenti di campi specifici. Se selezioni di controllare specifici aggiornamenti del campo, seleziona il campo che desideri che il modulo controlli.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>Nel campo <b>Tipo evento</b>, selezionare se si desidera controllare i nuovi record, i record aggiornati o sia i record nuovi che quelli aggiornati.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Aggiungi lead a un elenco]](#add-leads-to-a-list)
* [[!UICONTROL Clona un programma]](#clone-a-program)
* [[!UICONTROL Crea un record]](#create-a-record)
* [[!UICONTROL Chiamata API personalizzata]](#custom-api-call)
* [[!UICONTROL Scarica un file]](#download-a-file)
* [[!UICONTROL Leggi un record]](#read-a-record)
* [[!UICONTROL Rimuovi lead da elenco]](#remove-leads-from-a-list)
* [[!UICONTROL Pianificazione di una campagna]](#schedule-a-campaign)
* [[!UICONTROL Aggiorna un record]](#update-a-record)
* [[!UICONTROL Carica un file]](#upload-a-file)

#### [!UICONTROL Aggiungi lead a un elenco]

Questo modulo di azione aggiunge uno o più lead a un elenco, utilizzando l’ID lead. Puoi aggiungere fino a 300 lead alla volta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td>Immettere o mappare l'ID dell'elenco in cui si desidera aggiungere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID lead]</td> 
   <td> <p>Per ogni lead che si desidera aggiungere all'elenco, fare clic su <b>[!UICONTROL Add]</b>, quindi immettere o mappare l'ID del lead che si desidera aggiungere. Puoi aggiungere fino a 300 lead per il modulo da aggiungere all’elenco.</p> <p>Fare clic sull'interruttore Mappa per mappare una raccolta esistente di lead che si desidera aggiungere all'elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clona un programma]

Questo modulo di azione crea una copia di un programma utilizzando l’ID del programma esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID programma esistente]</td> 
   <td>Immetti o mappa l’ID del programma da copiare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome nuovo programma]</p> </td> 
   <td> <p>Immettere o mappare un nome per il nuovo programma</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Immettere o mappare l'ID della cartella in cui si desidera posizionare il nuovo programma.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un record]

Questo modulo azioni crea un nuovo record in [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona campi da mappare]</td> 
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
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td> <p>Se si sta creando una cartella o un programma, immettere o mappare una descrizione per il nuovo record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella padre]</td> 
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

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Marketo]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Per ogni campo che desideri aggiungere alla chiamata API, fai clic su <b>Aggiungi elemento</b> e immetti la chiave e il valore del campo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica un file]

Questo modulo di azione scarica un file utilizzando l’ID file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Inserisci o mappa l’ID del file da scaricare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge le informazioni su un record utilizzando il relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
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
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi sono disponibili in base al tipo di record  selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;ID Oggetto&gt;]</td> 
   <td>Immetti o mappa l’ID dell’oggetto di cui desideri recuperare le informazioni.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rimuovi lead da elenco]

Questo modulo di azione rimuove uno o più lead da un elenco, utilizzando l’ID lead. Puoi rimuovere fino a 300 lead alla volta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td>Immettere o mappare l'ID dell'elenco in cui si desidera rimuovere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID lead]</td> 
   <td> <p>Per ogni lead che si desidera rimuovere dall'elenco, fare clic su <b>[!UICONTROL Add item]</b>, quindi immettere o mappare l'ID del lead che si desidera rimuovere. Puoi aggiungere fino a 300 lead per il modulo da rimuovere dall’elenco. </p> <p>Fare clic sull'interruttore Mappa per mappare una raccolta esistente di lead che si desidera rimuovere dall'elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pianificazione di una campagna]

Questo modulo di azione pianifica una campagna esistente per una determinata data.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID campagna]</td> 
   <td>Immetti o mappa l’ID della campagna da pianificare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Pianifica per data]</p> </td> 
   <td>Seleziona la data in cui desideri eseguire la campagna. Se questo campo viene lasciato vuoto, la campagna viene eseguita cinque minuti dopo l’inizio dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un record esistente utilizzando il relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
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
   <td role="rowheader">[!UICONTROL Seleziona campi da mappare]</td> 
   <td>Se si sta aggiornando una società o un lead, selezionare i campi per i quali si desidera aggiornare i valori, quindi immettere i valori per questi campi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Se si sta aggiornando un programma, immettere o mappare un nuovo nome per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td> <p>Se si sta aggiornando un programma, immettere o mappare una nuova descrizione del programma.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Inizio]</td> 
   <td>Se si sta aggiornando un programma, immettere o mappare una nuova data di inizio per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
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

#### [!UICONTROL Carica un file]

Questo modulo azioni carica un nuovo file in [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Immettere o mappare l'ID della cartella in cui si desidera posizionare il nuovo file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td>Inserisci una descrizione del file caricato.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL Elenca record]](#list-records)
* [[!UICONTROL Cerca record]](#update-a-record)

#### [!UICONTROL Elenca record]

Questo modulo di azione recupera tutti i record di un tipo specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da elencare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Leggi tutte le campagne]</p> </li> 
     <li> <p>[!UICONTROL - Leggi tutti i programmi]</p> </li> 
     <li> <p>[!UICONTROL - Leggi tutti i lead] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Se si è scelto di recuperare i lead, selezionare se si desidera recuperare i lead da un elenco o da un programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni da includere nel bundle di output per questo modulo. I campi sono disponibili in base al tipo di record  selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca record]

Questo modulo di ricerca recupera un elenco di record che corrispondono a criteri di ricerca specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Marketo] a Workfront Fusion, vedere <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record che si desidera cercare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campagne]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programmi]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Selezionare il campo in base al quale si desidera eseguire la ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valore/Valori]</td> 
   <td>Immettere il valore del campo che si desidera cercare. Se il campo consente di cercare più valori, per ogni valore che si desidera cercare fare clic su <b>[!UICONTROL Aggiungi elemento]</b> e immettere il valore.</td> 
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
