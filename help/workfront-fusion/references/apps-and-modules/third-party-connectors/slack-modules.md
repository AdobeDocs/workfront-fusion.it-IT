---
title: Moduli Slack
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Slack e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2037'
ht-degree: 0%

---

# [!DNL Slack] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Slack] e collegarlo a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL Slack], è necessario disporre di un account [!DNL Slack].

## Informazioni API di Slack

Il connettore Slack utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>{{ifempty(parameters.domain, 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] moduli e relativi campi

Quando si configurano [!DNL Slack] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Slack], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messaggi](#messages)
* [Conversazioni](#channels)
* [Altro](#other)

### Messaggi

* [Creare un messaggio](#create-a-message)
* [Eliminare un messaggio](#delete-a-message)
* [Ottieni un messaggio canale privato](#get-a-private-channel-message)
* [Ottieni un messaggio di canale pubblico](#get-a-public-channel-message)
* [Aggiornare un messaggio](#update-a-message)
* [Guarda i messaggi del canale privato](#watch-private-channel-messages)
* [Guarda i messaggi del canale pubblico](#watch-public-channel-messages)

### [!UICONTROL Crea un messaggio]

Questo modulo di azione crea un nuovo messaggio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserisci un nome o un ID canale]</p> </td> 
   <td> <p>Scegli come selezionare il canale in cui desideri creare un messaggio.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID o nome canale]</strong>, immetti o mappa l'ID o il nome del canale in cui desideri inserire il messaggio.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona il tipo di canale, quindi seleziona il canale.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Inserisci il contenuto del testo del messaggio che desideri creare.</p> <p>Nota: per informazioni dettagliate sulla formattazione del testo, vedere <a href="https://api.slack.com/reference/surfaces/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL come utente]</td> 
   <td>Abilita questa opzione per pubblicare il messaggio come utente proprietario delle credenziali utilizzate dalla connessione per questo modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread message ID (timestamp)]</td> 
   <td>Se il nuovo messaggio è una risposta, immettere il timestamp del messaggio a cui si desidera rispondere. Non inserire l'indicatore orario di un messaggio che è già una risposta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Risposta trasmessa]</td> 
   <td> <p>Selezionare <strong>[!UICONTROL Sì]</strong> se si applicano entrambe le condizioni seguenti:</p> 
    <ul> 
     <li> <p>Il nuovo messaggio è una risposta a un altro messaggio</p> </li> 
     <li> <p>Desideri che il nuovo messaggio sia visibile a tutti gli utenti del canale</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Allegati]</td> 
   <td>Per ogni elemento che si desidera allegare al messaggio, fare clic su <b>Aggiungi elemento</b> e inserire i dettagli dell'elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon emoji]</td> 
   <td>Immettere o mappare l'emoji da utilizzare come icona per il messaggio nel formato <code>:icon-name:</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon URL]</td> 
   <td>Inserisci o mappa l’URL dell’immagine da utilizzare come icona per questo messaggio. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nomi collegamenti]</p> </td> 
   <td> <p>Abilitare questa opzione per consentire ai nomi e ai canali di utilizzare il formato <code>@username</code> o <code>#channel</code>. </p> <p>Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Analizza testo messaggio]</p> </td> 
   <td> <p>Abilita questa opzione per consentire l’analisi automatica. </p> <p>Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> <p>Nota: se nel messaggio originale sono state utilizzate opzioni [!UICONTROL Link names] o [!UICONTROL Parse message text], è necessario specificarle durante l'esecuzione del modulo [!UICONTROL Update a Message].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usa markdown]</p> </td> 
   <td> <p>Abilita questa opzione per consentire a [!DNL Slack] di utilizzare markdown nel testo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sblocca principalmente il contenuto basato su testo]</p> </td> 
   <td> <p>Abilita questa opzione per consentire la disattivazione di contenuti principalmente basati su testo. </p> <p>Per ulteriori informazioni sull'esecuzione dell'aggiornamento in [!DNL Slack], vedere <a href="https://api.slack.com/reference/messaging/link-unfurling">Scaricamento dei collegamenti nei messaggi</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Svuota contenuto multimediale]</p> </td> 
   <td> <p>Abilita questa opzione per consentire l’espansione del contenuto multimediale. </p> <p>Per ulteriori informazioni sull'esecuzione dell'aggiornamento in [!DNL Slack], vedere <a href="https://api.slack.com/reference/messaging/link-unfurling">Scaricamento dei collegamenti nei messaggi</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome utente]</td> 
   <td>Specifica il nome utente utilizzato per pubblicare il messaggio. Se non viene specificato alcun nome utente, viene utilizzato il nome "Bot".</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Elimina messaggio]

Questo modulo di azione elimina un messaggio specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID canale.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Immetti o mappa l’indicatore orario del messaggio da eliminare.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo Guarda messaggi canale privati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL come utente]</td> 
   <td> <p> Abilita questa opzione per eliminare il messaggio come utente con le credenziali utilizzate nella connessione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un messaggio canale privato]

Questo modulo di azione recupera i dettagli di un messaggio da un canale selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Immetti (mappa) l’ID canale.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Timestamp)]</p> </td> 
   <td> <p> Immettere o mappare il timestamp del messaggio di cui si desidera recuperare le informazioni.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel Messages].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un messaggio del canale pubblico]**

Questo modulo di azione restituisce un messaggio con un determinato ID da un canale pubblico specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID canale.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Timestamp)]</td> 
   <td> <p> Immettere o mappare il timestamp del messaggio di cui si desidera recuperare le informazioni.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un messaggio]

Questo modulo di azione ti consente di modificare un messaggio esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale che contiene il messaggio da aggiornare.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Timestamp)]</p> </td> 
   <td> <p> Immettere o mappare il timestamp del messaggio di cui si desidera recuperare le informazioni.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Inserisci il nuovo contenuto testuale del messaggio da aggiornare.</p> <p>Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL come utente]</td> 
   <td>Abilita questa opzione per aggiornare il messaggio come utente proprietario delle credenziali utilizzate dalla connessione per questo modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Allegati]</td> 
   <td>Per ogni elemento che si desidera allegare al messaggio, fare clic su <b>Aggiungi elemento</b> e inserire i dettagli dell'elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nomi collegamenti]</p> </td> 
   <td> <p>Abilitare questa opzione per consentire ai nomi e ai canali di utilizzare il formato <code>@username</code> o <code>#channel</code>. </p> <p>Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Analizza testo messaggio]</p> </td> 
   <td> <p>Abilita questa opzione per consentire l’analisi automatica. </p> <p> Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> <p>Nota: se nel messaggio originale sono state utilizzate opzioni [!UICONTROL Link names] o [!UICONTROL Parse message text], è necessario specificarle anche durante l'esecuzione del modulo Aggiorna messaggio.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Guarda i messaggi del canale privato]

Questo modulo di attivazione avvia lo scenario quando un nuovo messaggio viene aggiunto a un canale privato (gruppo).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona il canale privato da guardare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di messaggi restituiti da Workfront Fusion durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Guardare I Messaggi Del Canale Pubblico]

Questo modulo di attivazione avvia lo scenario quando viene aggiunto un nuovo messaggio a un canale pubblico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona il canale pubblico da guardare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di messaggi restituiti da Workfront Fusion durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Conversazioni

* [Ottieni un canale](#get-a-channel)
* [Elenca canali](#list-channels)
* [Elencare i membri nel canale](#list-members-in-channel)

#### [!UICONTROL Ottieni un canale]

Questo modulo di azione restituisce informazioni su un canale dell’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale di cui desideri recuperare le informazioni.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL Elenca canali]

Questo modulo di ricerca restituisce un elenco di tutti i canali di un’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Exclude archiviato]</p> </td> 
   <td> <p>Selezionare [!UICONTROL Sì] per escludere i canali archiviati nei risultati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selezionare il tipo o i tipi di canali da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Imposta il numero massimo di canali restituiti da Workfront Fusion durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Elenca membri nel canale]

Questo modulo di ricerca restituisce un elenco di utenti nel canale selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserisci un nome o un ID canale]</p> </td> 
   <td> <p>Scegli come desideri selezionare il messaggio che desideri.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID o nome canale]</strong>, immetti o mappa l'ID canale o del canale da cui elencare gli utenti.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona il tipo di canale, quindi seleziona il canale.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di membri restituiti da Workfront Fusion durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Altro

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Slack]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://slack.com/api/</code>. Esempio: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL di base]</td> 
   <td>Seleziona l’URL di base da utilizzare per la chiamata API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invia token di accesso]</td> 
   <td>Seleziona se desideri inviare il token di accesso come intestazione o come parametro di query.</td> 
  </tr> 
 </tbody> 
</table>

## Terminologia

La seguente terminologia può essere utile durante la configurazione di [!DNL Slack] moduli:

* **DM**: [!UICONTROL Messaggio diretto]
* **IM**: [!UICONTROL Messaggio immediato]
* **Canale privato**: in precedenza [!UICONTROL Gruppo]
* **Messaggio diretto**: in precedenza [!UICONTROL IM]
* **Canale**: [!UICONTROL Conversazione] nella documentazione API, [!UICONTROL canale] nell&#39;app [!DNL Slack].
