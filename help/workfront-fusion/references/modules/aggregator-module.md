---
title: Modulo Aggregator
description: Un modulo aggregatore è un tipo di modulo progettato per unire diversi bundle di dati in un singolo bundle.
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---

# Modulo [!UICONTROL Aggregator]

Un modulo aggregatore è un modulo che unisce diversi bundle di dati in un singolo bundle.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza</td> 
   <td> Nuovo: Standard<p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licenza</td> 
   <td>
   <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] piano: [!DNL Workfront Fusion] incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>


Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle licenze di Adobe Workfront Fusion, vedi [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Panoramica del modulo [!UICONTROL Aggregator]

Quando viene eseguito un modulo [!UICONTROL Aggregator], vengono eseguite le seguenti operazioni:

* Accumula tutti i bundle dal funzionamento di un singolo modulo di origine.
* Restituisce un singolo bundle con un array contenente un elemento per bundle accumulato. Il contenuto degli elementi dell&#39;array dipende dal modulo [!UICONTROL Aggregator] e dalla relativa configurazione.

Nell&#39;immagine seguente viene illustrata una configurazione tipica del modulo [!UICONTROL Aggregator]:

![Aggregatore array](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source Module]</p> </td> 
   <td> <p>Il modulo da cui inizia l’aggregazione del bundle. Il modulo sorgente è in genere un iteratore o un modulo di ricerca che produce una serie di bundle.</p><p>Quando si imposta il modulo di origine dell'aggregatore (e si chiude la relativa configurazione), il percorso tra il modulo di origine e il modulo dell'aggregatore viene racchiuso in un'area grigia, in modo da visualizzare chiaramente l'inizio e la fine dell'aggregazione. 
   </p> <p>Per ulteriori informazioni sugli iteratori, vedere il modulo <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator]</a>.</p> 
   <p>Per ulteriori informazioni sui moduli di ricerca, vedere <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">Moduli di ricerca</a> nella panoramica del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Target structure type]</p><p>(Applicabile solo per il modulo [!UICONTROL Array aggregator]).</p> </td> 
   <td> <p> Struttura di destinazione in cui vengono aggregati i dati. L'opzione predefinita, [!UICONTROL Custom], consente di scegliere gli elementi da aggregare nel <code>Array </code> elemento del bundle di output di [!UICONTROL Array aggregator]:</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>Dopo aver connesso altri moduli dopo il modulo [!UICONTROL Array aggregator] e aver ripristinato la configurazione del modulo aggregatore, il menu a discesa del tipo di struttura [!UICONTROL Target] contiene tutti i moduli seguenti e i relativi campi che sono di tipo "Array of Collections". <p>In questo esempio, il campo [!UICONTROL Attachments] del modulo [!DNL Slack] &gt;[!UICONTROL Create a Message] viene visualizzato nel campo Aggregatore array &gt; Tipo di struttura di destinazione. </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregated fields]</td> 
   <td>I campi che si desidera includere nell'output del modulo aggregatore.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>Utilizzando il campo Raggruppa per è possibile definire un'espressione contenente uno o più elementi mappati. I dati aggregati verranno quindi separati in Gruppi dal valore dell’espressione. Ogni gruppo produce come bundle separato, contenente una Chiave e un array di dati. Raggruppando i risultati, puoi utilizzare la Chiave come filtro nei moduli successivi.</p>
   <p>Ogni bundle contiene due elementi:</p> 
    <ul> 
     <li><code>Key</code>: valore in base al quale si esegue il raggruppamento.</li> 
     <li><code>Array</code>: i dati aggregati dai bundle per i quali la formula ha restituito il valore <code>Key</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>Interrompi elaborazione dopo un'aggregazione vuota</p> </td> 
   <td> <p>Per impostazione predefinita, il modulo [!UICONTROL Aggregator] restituisce il risultato dell'aggregazione anche quando nessun bundle ha raggiunto il modulo [!UICONTROL Aggregator] (ad esempio, perché sono stati tutti filtrati dal percorso che include l'aggregatore). Se l'opzione [!UICONTROL Stop processing after an empty aggregation] è abilitata, il modulo [!UICONTROL Aggregator] non produce alcun bundle di output quando non sono presenti bundle di input. Al contrario, il flusso si interrompe.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>I bundle generati dai moduli tra il modulo di origine e il modulo [!UICONTROL Aggregator] non vengono generati dal modulo [!UICONTROL Aggregator]. Questi bundle non sono accessibili dai moduli nel flusso dopo [!UICONTROL Aggregator]. Se sono necessari dati da un bundle generato da un modulo tra il modulo di origine e il modulo [!UICONTROL Aggregator], assicurarsi di includere l&#39;elemento specificato nella configurazione del modulo [!UICONTROL Aggregator] (ad esempio nel campo [!UICONTROL Aggregated fields] nella configurazione del modulo [!UICONTROL Array aggregator]).


## Scenario di esempio del funzionamento degli aggregatori

Questo scenario di esempio mostra come comprimere tutti gli allegati e-mail e caricare il file ZIP in [!DNL Dropbox].

![Dropbox archivio esempio](assets/dropbox-archive.png)

Lo scenario seguente mostra come:

* Il primo modulo controlla una cassetta postale per le e-mail in arrivo. Il trigger [!UICONTROL Email] >[!UICONTROL Watch emails] restituisce un bundle con l&#39;elemento `Attachments[]`, che è un array contenente tutti gli allegati dell&#39;e-mail.

* Il secondo modello esegue l&#39;iterazione degli allegati dell&#39;e-mail: l&#39;iteratore [!UICONTROL Email] >[!UICONTROL Iterate attachments] prende gli elementi dell&#39;array `Attachments[]` uno alla volta e li invia ulteriormente come bundle separati.

* Il terzo modulo è l&#39;aggregatore. Aggrega i bundle generati dal modulo [!UICONTROL Email] >[!UICONTROL Iterate attachments]. [!UICONTROL Archive] >[!UICONTROL Create an archive aggregator] accumula tutti i bundle che riceve e restituisce un singolo bundle contenente il file ZIP.

* L&#39;ultimo modulo carica il file ZIP risultante in [!DNL Dropbox].  [!DNL Dropbox] > [!UICONTROL Upload a file] ottiene il file ZIP dal modulo [!UICONTROL Archive] > [!UICONTROL Create an archive] e lo carica in [!DNL Dropbox].



Di seguito è riportato un esempio di configurazione dell&#39;aggregatore [!UICONTROL Archive] > [!UICONTROL Create an archive]:

![Crea un archivio](assets/archive-create-an-archive.png)
