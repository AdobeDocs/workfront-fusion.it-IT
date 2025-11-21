---
title: Moduli Slack
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Slack e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
source-git-commit: 0dbe23c5eb7a0d890b7b543f2f310b163baa3793
workflow-type: tm+mt
source-wordcount: '4580'
ht-degree: 8%

---

# [!DNL Slack] moduli

>[!IMPORTANT]
>
>Questo articolo descrive i moduli disponibili nel nuovo connettore Slack, rilasciato il 17 novembre 2025.
>
>Per informazioni sul connettore Slack legacy, consulta [[!DNL Slack] moduli (legacy)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md).

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Slack] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze di Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza di Workfront Fusion</p>
   <p>Basata sul connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
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

* Per utilizzare i moduli [!DNL Slack], è necessario disporre di un account [!DNL Slack].
* Se stai creando connessioni OAuth@, devi aggiungere i seguenti URL al inserisco nell&#39;elenco Consentiti di della tua organizzazione:
   * token bot: `https://oauth.app.workfrontfusion.com/oauth/cb/slack3`
   * token utente:` https://oauth.app.workfrontfusion.com/oauth/cb/slack2`

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

## Moduli [!DNL Slack] e relativi campi

Quando configuri [!DNL Slack] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Slack], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione mappatura](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messaggi](#messages)
* [File](#files)
* [Canali](#channels)
* [Reazioni](#reactions)
* [Stelle](#stars)
* [Elementi salvati](#saved-items)
* [Pin](#pins)
* [Utenti](#users)
* [Promemoria](#reminders)
* [Eventi](#events)
* [Profilo](#profile)
* [Altro](#other)

### Messaggi

+++ **[!UICONTROL Crea un messaggio]**

Questo modulo di azione crea un nuovo messaggio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Testo]</p> </td> 
   <td> <p>Inserisci il contenuto del testo del messaggio che desideri creare.</p> <p>Nota: per informazioni dettagliate sulla formattazione del testo, vedere <a href="https://api.slack.com/reference/surfaces/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocks]</td> 
   <td>I blocchi sono componenti riutilizzabili che puoi utilizzare per personalizzare e organizzare i messaggi. Per ulteriori informazioni sui blocchi, vedere <a href="https://api.slack.com/block-kit">Block Kit</a> nella documentazione di [!DNL Slack].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread message ID (timestamp)]</td> 
   <td>Se il nuovo messaggio è una risposta, immettere il timestamp del messaggio a cui si desidera rispondere. Non inserire il timestamp di un messaggio che è già una risposta.</td> 
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
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elimina messaggio]**

Questo modulo di azione elimina un messaggio specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID canale.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio (timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da eliminare.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo Guarda canale privato.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni un messaggio canale privato]**

Questo modulo di azione recupera i dettagli di un messaggio da un canale selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel]</p> </td> 
   <td> <p>Seleziona il canale che contiene il messaggio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Timestamp)]</p> </td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio di cui desideri recuperare le informazioni.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni un messaggio del canale pubblico]**

Questo modulo di azione restituisce un messaggio con un determinato ID da un canale pubblico specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Seleziona il canale che contiene il messaggio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio di cui desideri recuperare le informazioni.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca risposte]**

Questo modulo di azione recupera un thread di messaggi inviati a una conversazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale contenente il messaggio per il quale desideri recuperare le risposte, quindi seleziona il canale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio padre (timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio per il quale desideri recuperare le risposte.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di risposte che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cerca messaggio]**

Questo modulo di ricerca restituisce messaggi che corrispondono a una query di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Immettere la query in base alla quale si desidera eseguire la ricerca. </p> <p>Per informazioni sulla creazione di formule dal pannello di mappatura, vedere <a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">Mappare gli elementi utilizzando le funzioni in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per] </td> 
   <td> <p>Seleziona se desideri ordinare i messaggi restituiti in base al punteggio o alla marca temporale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Seleziona se desideri ordinare i messaggi in ordine crescente o decrescente.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aggiorna un messaggio]**

Questo modulo di azione ti consente di modificare un messaggio esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserisci un nome o un ID canale]</p> </td> 
   <td> <p>Scegli come desideri selezionare il messaggio che desideri.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID o nome canale]</strong>, immetti o mappa l'ID canale o del canale che contiene il messaggio, quindi immetti il timestamp <strong>[!UICONTROL (ID messaggio)]</strong> del messaggio. .</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona il tipo di canale, quindi il canale, infine il messaggio.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Testo]</p> </td> 
   <td> <p>Inserisci il nuovo contenuto testuale del messaggio da aggiornare.</p> <p>Per ulteriori informazioni, vedere <a href="https://api.slack.com/docs/formatting">Formattazione del testo per le superfici dell'app</a> nella documentazione di [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocks]</td> 
   <td>I blocchi sono componenti riutilizzabili che puoi utilizzare per personalizzare e organizzare i messaggi. Per ulteriori informazioni sui blocchi, vedere <a href="https://api.slack.com/block-kit">Block Kit</a> nella documentazione di [!DNL Slack].</td> 
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

+++

+++ **[!UICONTROL Messaggi Diretti Attenti]**

Questo modulo di attivazione avvia lo scenario quando un nuovo messaggio viene aggiunto a un messaggio diretto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona la conversazione per messaggi diretti che desideri controllare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immetti il numero massimo di messaggi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Messaggi Diretti Multiparty]**

Questo modulo di attivazione avvia lo scenario quando un nuovo messaggio viene aggiunto a un canale di messaggi diretti multiparte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona la conversazione per messaggi diretti che desideri controllare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immetti il numero massimo di messaggi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Guarda i messaggi del canale privato]**

Questo modulo di attivazione avvia lo scenario quando un nuovo messaggio viene aggiunto a un canale privato (gruppo).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona il canale privato da guardare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immetti il numero massimo di messaggi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Guardare I Messaggi Del Canale Pubblico]**

Questo modulo di attivazione avvia lo scenario quando viene aggiunto un nuovo messaggio a un canale pubblico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Seleziona il canale pubblico da guardare per i nuovi messaggi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immetti il numero massimo di messaggi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### File

+++ **[!UICONTROL Elimina un file]**

Questo modulo di azione restituisce l’eliminazione del file specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> <p>Immetti o mappa l’ID del file da eliminare. </p> <p>Nota: l'ID file può essere recuperato utilizzando un altro modulo, ad esempio il modulo [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni un file]**

Questo modulo di azione restituisce i dettagli del file specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> <p>Immetti o mappa l’ID del file da recuperare. </p> <p>Nota: l'ID file può essere recuperato utilizzando un altro modulo, ad esempio il modulo [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL File di elenco]**

Questo modulo di azione restituisce un elenco di file in base al filtro specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selezionare il tipo o i tipi di file che si desidera recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di canale]</p> </td> 
   <td> <p>Seleziona il tipo di canale che rappresenta il canale da cui desideri elencare i file, quindi seleziona il canale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Creato da]</td> 
   <td> <p>Selezionare un utente per restituire solo i file creati dall'utente specificato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data da]</td> 
   <td>Immettere la prima data da cui si desidera restituire i file. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date to]</td> 
   <td>Immettere l'ultima data da cui si desidera restituire i file. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Carica un file]**

Questo modulo di azione crea o carica un file in [!DNL Slack]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Canali]</td> 
   <td> <p>Per ogni canale in cui si desidera caricare il file, fare clic su <b>[!UICONTROL Add item]</b>, quindi selezionare il tipo di canale e il canale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Inserisci un titolo per il file da caricare</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread ID (timestamp)]</td> 
   <td> <p>Se stai caricando il file come risposta, immetti o mappi la marca temporale del messaggio a cui desideri rispondere.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Commento iniziale]</td> 
   <td> <p>Inserisci o mappa il testo del messaggio che introduce il file.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL File di controllo]**

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un nuovo file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Seleziona il tipo di file che desideri che il modulo guardi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td> <p>Seleziona il tipo di canale da guardare per i file, quindi seleziona il canale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Creato da]</td> 
   <td> <p>Selezionare un utente per restituire solo i file creati dall'utente specificato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Canali

+++ **[!UICONTROL Archivia un canale]**

Questo modulo di azione archivia un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale che desideri archiviare.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea un canale]**

Questo modulo di azione crea un nuovo canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome]</p> </td> 
   <td> <p>Inserisci o mappa un nome per il nuovo canale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL È privato]</td> 
   <td>Abilita questa opzione per impostare il nuovo canale come privato.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni un canale]**

Questo modulo di azione restituisce informazioni su un canale dell’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale di cui desideri recuperare le informazioni.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Partecipa a un canale]**

Questo modulo di azione unisce l’utente a un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale a cui desideri partecipare.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Lascia un canale]**

Questo modulo di azione rimuove l’utente da un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale che desideri lasciare.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca canali]**

Questo modulo di ricerca restituisce un elenco di tutti i canali di un’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
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
   <td> <p>Imposta il numero massimo di canali che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca membri nel canale]**

Questo modulo di ricerca restituisce un elenco di utenti nel canale selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Selezionare il tipo di canale contenente i membri che si desidera elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private Channel]</td> 
   <td>Seleziona il canale di cui desideri elencare i membri.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di membri che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Imposta lo scopo di un canale]**

Questo modulo di azione cambia lo scopo di un canale

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Selezionare il tipo di canale per il quale si desidera cambiare lo scopo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / User / [!UICONTROL Multiple IM Channel]</td> 
   <td>Selezionare il canale o l'utente per il quale si desidera modificare lo scopo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scopo]</td> 
   <td>Inserisci o mappa il nuovo scopo del canale. Questo campo non supporta la formattazione o i collegamenti.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Imposta l&#39;argomento di un canale]**

Questo modulo di azione modifica l’argomento di un canale

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Selezionare il tipo di canale per il quale si desidera modificare l'argomento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>Selezionare il canale o l'utente per il quale si desidera modificare l'argomento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Argomento]</td> 
   <td>Inserisci o mappa il nuovo argomento del canale. Questo campo non supporta la formattazione o i collegamenti.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Annulla archiviazione di un canale]**

Questo modulo di azione annulla l’archiviazione di un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID canale]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del canale di cui vuoi annullare l’archiviazione.</p> <p>Nota: è possibile recuperare l'ID canale utilizzando il modulo [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Reazioni

+++ **[!UICONTROL Aggiungi una reazione]**

Questo modulo di azione aggiunge una reazione a un elemento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale a cui desideri aggiungere una reazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>Seleziona il canale o l’utente a cui desideri aggiungere una reazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio (timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio a cui desideri aggiungere una reazione.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reaction (emoji) name]</td> 
   <td>Inserisci o mappa il nome dell’emoji che desideri utilizzare per una reazione. Esempio: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca reazioni]**

Questo modulo di azione restituisce le reazioni effettuate da un utente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Utente]</p> </td> 
   <td> <p>Seleziona l’utente che ha effettuato le reazioni da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immetti o mappa il numero massimo di reazioni che il modulo deve restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rimuovi una reazione]**

Questo modulo di azione rimuove una reazione da un elemento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Selezionare il tipo di canale da cui si desidera rimuovere una reazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>Selezionare il canale o l'utente da cui si desidera rimuovere una reazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da cui desideri rimuovere una reazione.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reaction (emoji) name]</td> 
   <td>Inserisci o mappa il nome dell’emoji che desideri rimuovere dal messaggio. Esempio: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Stelle

+++ **[!UICONTROL Aggiungi una stella]**

Questo modulo di azione fa di un canale un canale con protagonista.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale a cui desideri aggiungere una stella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>Seleziona il canale o l’utente a cui desideri aggiungere una stella.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rimuovi una stella]**

Questo modulo rimuove la stella da un canale stellato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale a cui desideri aggiungere una stella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>Seleziona il canale o l’utente a cui desideri aggiungere una stella.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Elementi salvati

+++ **[!UICONTROL Rimuovi elemento salvato]**

Questo modulo rimuove un elemento dagli elementi salvati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da rimuovere dagli elementi salvati.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> <p>Immettere o mappare il file da rimuovere dagli elementi salvati.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Salva un elemento]**

Questo modulo di azione aggiunge un elemento agli elementi salvati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Timestamp)]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da salvare.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> <p>Immetti o mappa il file da salvare.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Pin

+++ **[!UICONTROL Fissa un elemento]**

Questo modulo di azione invia un elemento a un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale a cui vuoi fissare un elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM Channel] / [!UICONTROL User]</td> 
   <td>Selezionare il canale o l'utente a cui si desidera fissare un elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da fissare.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Sblocca un elemento]**

Questo modulo di azione elimina un elemento da un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale da cui vuoi sbloccare un elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM Channel] / [!UICONTROL User]</td> 
   <td>Selezionare il canale o l'utente da cui si desidera rimuovere un elemento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Immetti o mappa la marca temporale del messaggio da sbloccare.</p> <p>Nota: la marca temporale può essere recuperata utilizzando un altro modulo, ad esempio il modulo [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Utenti

+++ **[!UICONTROL Ottieni un utente]**

Questo modulo di azione recupera i dettagli su un membro di un’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID utente]</p> </td> 
   <td> <p>Inserisci o mappa l’ID utente dell’utente per il quale desideri recuperare i dettagli.</p> <p>Nota: l'ID utente può essere recuperato utilizzando un altro modulo, ad esempio il modulo [!DNL List Users].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Invita utenti]**

Questo modulo invita 1-30 utenti a un canale pubblico o privato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Seleziona il tipo di canale a cui desideri invitare gli utenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>Seleziona il canale a cui desideri invitare gli utenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Utenti]</td> 
   <td> <p>Seleziona gli utenti che desideri aggiungere al canale.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Scegli un utente]**

Questo modulo di azione rimuove un utente da un canale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di canale]</td> 
   <td>Selezionare il tipo di canale da cui si desidera rimuovere un utente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>Selezionare il canale da cui si desidera rimuovere un utente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Utenti]</td> 
   <td> <p>Seleziona l’utente da rimuovere dal canale.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca utenti]**

Questo modulo di azione restituisce un elenco di tutti gli utenti in un’area di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Immettere o mappare il numero massimo di utenti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cerca utente]**

Questo modulo di azione recupera i dettagli relativi a un singolo utente utilizzando il relativo indirizzo e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL E-Mail] </p> </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail dell’utente di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Osserva utenti]**

Questo modulo di attivazione avvia lo scenario quando un nuovo utente viene aggiunto all&#39;area di lavoro [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Imposta il numero massimo di utenti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Promemoria

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Crea un promemoria]**

Questo modulo crea un promemoria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo]</td> 
   <td>Inserisci o mappa il contenuto del promemoria</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time]</td> 
   <td> <p>Immetti o mappa la data e l’ora in cui questo promemoria dovrebbe verificarsi. Immettere una delle seguenti opzioni: </p> 
    <ul> 
     <li> <p>La marca temporale Unix (fino a cinque anni da ora)</p> </li> 
     <li> <p>Il numero di secondi trascorsi fino al promemoria (se entro 24 ore) </p> </li> 
     <li> <p>Una descrizione in lingua naturale (ad esempio: "in 15 minuti" o "ogni giovedì")</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Utente] </p> </td> 
   <td> <p>Selezionare l'utente che riceve il promemoria.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### Eventi

+++ **[!UICONTROL Nuovo evento]**

Questo trigger immediato avvia uno scenario quando viene creato un nuovo messaggio o un altro evento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Selezionare il webhook che si desidera utilizzare.</p> <p>Oppure</p> <p>Crea un nuovo webhook.</p> 
    <ol> 
     <li value="1"> <p>Fare clic su <b>[!UICONTROL Add]</b>.</p> </li> 
     <li value="2"> <p>Seleziona il tipo di evento.</p> </li> 
     <li value="3"> <p>Seleziona o aggiungi una connessione. Per istruzioni sulla connessione dell'account [!DNL Slack] a [!UICONTROL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base</a></p> </li> 
     <li value="4"> <p>Se richiesto, selezionare il canale che si desidera guardare.</p> </li> 
     <li value="5"> <p>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Profilo

+++ **[!UICONTROL Imposta uno stato]**

Questo modulo aggiorna lo stato corrente di un utente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Testo di stato]</p> </td> 
   <td> <p>Immettere o mappare il testo dello stato. Considera quanto segue:</p> 
    <ul> 
     <li> <p>È possibile immettere un massimo di 100 caratteri.</p> </li> 
     <li> <p>È possibile utilizzare il markup o altra formattazione, ad esempio le menzioni utente.</p> </li> 
     <li> <p>È possibile includere emoji nel testo dello stato utilizzando il formato <code>:emojiname:</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status emoji]</td> 
   <td> <p>Inserisci o mappa le emoji che desideri utilizzare per rappresentare il tuo stato. Utilizza il formato <code>:emojiname:</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Scadenza stato </td> 
   <td>Immettere o mappare la data e l'ora di scadenza dello stato. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione</a>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Altro

+++ **[!UICONTROL Effettuare una chiamata API]**

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Slack]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Slack] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci un percorso relativo a <code>https://slack.com/api/</code>. Esempio: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> in JSON, inserisci le virgolette al di fuori dell’istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL di base]</td> 
   <td>Seleziona l’URL di base da utilizzare per la chiamata API.</td> 
  </tr> 
 </tbody> 
</table>

+++

## Terminologia

La seguente terminologia può essere utile durante la configurazione di [!DNL Slack] moduli:

* **DM**: [!UICONTROL Messaggio diretto]
* **IM**: [!UICONTROL Messaggio immediato]
* **Canale privato**: in precedenza [!UICONTROL Gruppo]
* **Messaggio diretto**: in precedenza [!UICONTROL IM]
* **Canale**: [!UICONTROL Conversazione] nella documentazione API, [!UICONTROL canale] nell&#39;app [!DNL Slack].

