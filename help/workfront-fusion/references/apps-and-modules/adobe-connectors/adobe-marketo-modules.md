---
title: Moduli Marketo
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Marketo], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '2237'
ht-degree: 100%

---

# Moduli [!DNL Marketo]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Marketo], nonché collegarli a più applicazioni e servizi di terze parti.

Per un video introduttivo sul connettore Marketo, consulta:

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Marketo], è necessario disporre di un account [!DNL Marketo].

## Informazioni sull’API di Marketo

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

## Connettere [!DNL Marketo] a Workfront Fusion {#connect-marketo-to-workfront-fusion}

Puoi creare una connessione al tuo account [!DNL Marketo] direttamente da qualsiasi modulo di [!DNL Marketo].

1. In qualsiasi modulo di Marketo, fai clic su **Aggiungi** accanto al campo Connessione.
1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Inserisci un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>
          <p>Specifica se ti connetti a un account di servizio o a un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / ID Munchkin]</td>
        <td>
          <p>Inserisci l’account [!DNL Marketo] o l’ID [!DNL Marketo] di [!UICONTROL Munchkin]. Questa è la parte univoca dell’URL di base o dell’endpoint assegnato all’account, utilizzata per accedere a [!DNL Marketo] tramite l’API [!UICONTROL REST]. Per istruzioni su come individuare questa posizione, consulta [URL di base](https://developers.marketo.com/rest-api/base-url/) nella documentazione di [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Inserisci il tuo ID client Marketo. Per istruzioni su come individuarlo consulta [Autenticazione](https://developers.marketo.com/rest-api/authentication/) nella documentazione di [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il Segreto client Marketo. Per istruzioni su come individuarli, consulta [Autenticazione](https://developers.marketo.com/rest-api/authentication/) nella documentazione di [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## Moduli di [!DNL Marketo] e relativi campi

Durante la configurazione di moduli di [!DNL Marketo], in Workfront Fusion vengono mostrati i campi elencati di seguito. Insieme a questi, potrebbero essere mostrati ulteriori campi di [!DNL Marketo], a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [[!UICONTROL Controlla eventi (istantanei)]](#watch-events-instant)
* [[!UICONTROL Controlla record]](#watch-records)

#### [!UICONTROL Controlla eventi (istantanei)]

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Inserisci il webhook che il modulo deve utilizzare.</p> <p>Per ulteriori informazioni sui webhook, consulta <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di ambiente da creare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Attività]</strong> </p> <p>Seleziona il tipo di attività che desideri controllare. </p> <p>Il modulo controlla solo le attività nuove.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Nel campo <b>Tipo di evento</b>, seleziona se desideri controllare nuovi record, record aggiornati, record nuovi e aggiornati o aggiornamenti di campi specifici. Se selezioni di controllare aggiornamenti specifici del campo, seleziona il campo che il modulo deve controllare.</p> </li> 
     <li> <p><strong>[!UICONTROL Programma]</strong> </p> <p>Nel campo <b>Tipo di evento</b>, seleziona se desideri controllare i nuovi record, i record aggiornati o sia i record nuovi che quelli aggiornati.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi che desideri includere nel bundle di output di questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
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
* [[!UICONTROL Rimuovi lead da un elenco]](#remove-leads-from-a-list)
* [[!UICONTROL Pianifica una campagna]](#schedule-a-campaign)
* [[!UICONTROL Aggiorna un record]](#update-a-record)
* [[!UICONTROL Carica un file]](#upload-a-file)

#### [!UICONTROL Aggiungi lead a un elenco]

Questo modulo di azione aggiunge uno o più lead a un elenco utilizzando l’ID lead. Puoi aggiungere fino a 300 lead alla volta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td>Inserisci oppure mappa l’ID dell’elenco al quale desideri aggiungere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID lead]</td> 
   <td> <p>Per ciascun lead che desideri aggiungere all’elenco, fai clic su <b>[!UICONTROL Aggiungi]</b>, quindi inserisci oppure mappa l’ID del lead che desideri aggiungere. Puoi aggiungere fino a 300 lead per il modulo da aggiungere all’elenco.</p> <p>Fai clic sul pulsante di attivazione/disattivazione Mappa per mappare una raccolta di lead esistente che desideri aggiungere all’elenco.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID programma esistente]</td> 
   <td>Inserisci oppure mappa l’ID del programma che desideri copiare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome nuovo programma]</p> </td> 
   <td> <p>Inserisci oppure mappa un nome per il nuovo programma</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Inserisci oppure mappa l’ID della cartella in cui desideri posizionare il nuovo programma.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un record]

Questo modulo di azione crea un nuovo record in [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di ambiente da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Azienda]</p> </li> 
     <li> <p>[!UICONTROL Cartella]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Programma]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona i campi da mappare]</td> 
   <td>Se stai creando un’azienda o un lead, seleziona i campi per i quali impostare i valori al momento della creazione del nuovo record, quindi inserisci i valori per questi campi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di programma]</td> 
   <td>Se stai creando un programma, seleziona il tipo di programma che desideri creare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canale del programma] </td> 
   <td>Se stai creando un programma, seleziona il canale in cui desideri creare il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartella] / [!UICONTROL Nome programma]</td> 
   <td>Se stai creando una cartella o un programma, inserisci oppure mappa un nome per il nuovo record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td> <p>Se stai creando una cartella o un programma, inserisci oppure mappa una descrizione per il nuovo record.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Cartella principale]</td> 
   <td>Se stai creando una cartella o un programma, inserisci oppure mappa l’ID della cartella principale in cui desideri creare il nuovo record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costi]</td> 
   <td>Se stai creando un programma, aggiungi gli eventuali costi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag]</td> 
   <td>Se stai creando un programma, aggiungi eventuali tag.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Marketo]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci un percorso relativo a <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi]</td> 
   <td> <p>Per ogni campo che desideri aggiungere alla chiamata API, fai clic su <b>Aggiungi elemento</b> e inserisci la chiave e il valore del campo.</td> 
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
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Inserisci oppure mappa l’ID del file che desideri scaricare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge le informazioni su un record utilizzando l’ID corrispondente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di ambiente da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campagna]</p> </li> 
     <li> <p>[!UICONTROL Azienda]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Elenco]</p> </li> 
     <li> <p>[!UICONTROL Programma]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo. I campi sono disponibili in base al [!UICONTROL Tipo di record] che hai selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID &lt;Object&gt;]</td> 
   <td>Inserisci oppure mappa l’ID dell’oggetto per il quale desideri recuperare le informazioni.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rimuovi lead da un elenco]

Questo modulo di azione rimuove uno o più lead da un elenco, utilizzando l’ID lead. Puoi rimuovere fino a 300 lead alla volta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td>Inserisci oppure mappa l’ID dell’elenco dal quale desideri rimuovere i lead.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID lead]</td> 
   <td> <p>Per ciascun lead che desideri rimuovere dall’elenco, fai clic su <b>[!UICONTROL Aggiungi elemento]</b>, quindi inserisci oppure mappa l’ID del lead da rimuovere. Puoi aggiungere fino a 300 lead per modulo da rimuovere dall’elenco. </p> <p>Fai clic sul pulsante di attivazione/disattivazione Mappa per mappare una raccolta di lead esistente che desideri rimuovere dall’elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Pianifica una campagna]

Questo modulo di azione pianifica una campagna esistente per una data specifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID campagna]</td> 
   <td>Inserisci oppure mappa l’ID della campagna da pianificare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Pianifica per data]</p> </td> 
   <td>Seleziona la data in cui desideri che venga eseguita la campagna. Se questo campo rimane vuoto, la campagna viene eseguita cinque minuti dopo l’inizio dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un record esistente utilizzando l’ID del record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di ambiente da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Azienda]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Programma]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azienda]/[!UICONTROL Lead]/[!UICONTROL ID programma]</td> 
   <td>Inserisci oppure mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona i campi da mappare]</td> 
   <td>Se stai aggiornando un’azienda o un lead, seleziona i campi dei quali desideri aggiornare i valori, quindi inserisci i valori per tali campi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome programma]</td> 
   <td>Se stai aggiornando un programma, inserisci oppure mappa un nuovo nome per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td> <p>Se stai aggiornando un programma, inserisci oppure mappa una nuova descrizione per il programma.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di inizio]</td> 
   <td>Se stai aggiornando un programma, inserisci oppure mappa una nuova data di inizio per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
   <td>Se stai aggiornando un programma, inserisci oppure mappa una nuova data di fine per il programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costi]</td> 
   <td>Se stai aggiornando un programma, aggiungi gli eventuali costi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag]</td> 
   <td>Se stai aggiornando un programma, aggiungi gli eventuali tag.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un file]

Questo modulo di azione carica un nuovo file in [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Inserisci oppure mappa l’ID della cartella in cui desideri posizionare il nuovo file.</td> 
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
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record che desideri creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Leggi tutte le campagne]</p> </li> 
     <li> <p>[!UICONTROL - Leggi tutti i programmi]</p> </li> 
     <li> <p>[!UICONTROL - Leggi tutti i lead] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campo]</td> 
   <td>Se hai scelto di recuperare i lead, seleziona se recuperarli da un elenco oppure da un programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo. I campi sono disponibili in base al [!UICONTROL Tipo di record] che hai selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca record]

Questo modulo di ricerca recupera un elenco di record corrispondenti ai criteri di ricerca specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Marketo] a Workfront Fusion, consulta <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Marketo] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record che desideri cercare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campagne]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Programmi]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Campo]</p> </td> 
   <td> <p>Seleziona il campo in base al quale desideri eseguire la ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valore/Valori]</td> 
   <td>Inserisci il valore del campo che desideri cercare. Se il campo consente di cercare più valori, per ciascun valore che desideri cercare fai clic su <b>[!UICONTROL Aggiungi elemento]</b> e inserisci il valore.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>
