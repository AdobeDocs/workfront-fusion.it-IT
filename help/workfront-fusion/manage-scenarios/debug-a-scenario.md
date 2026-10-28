---
title: Eseguire il debug di uno scenario
description: Adobe Workfront Fusion Devtool consente di comprendere e risolvere gli scenari. Devtool aggiunge un pannello aggiuntivo a Chrome Developer Tools. Utilizzando questo pannello di debugger, puoi controllare tutte le esecuzioni manuali dello scenario, esaminare tutte le operazioni eseguite e visualizzare i dettagli di ogni chiamata API eseguita. Puoi vedere quale modulo, operazione o singola risposta ha causato l’errore e sfruttare queste informazioni per perfezionare lo scenario.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
TQID: 'https://experienceleague.adobe.com/7NXYVXxbQvgKnqvRUNV-ySBApe9kl-Kn57sSKCh4NLE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1962'
ht-degree: 5%
---
# Eseguire il debug di uno scenario

Adobe Workfront Fusion Devtool consente di comprendere e risolvere gli scenari. Utilizzando Devtool, puoi controllare tutte le esecuzioni manuali dello scenario, esaminare tutte le operazioni eseguite e visualizzare i dettagli di ogni chiamata API eseguita. Puoi vedere quale modulo, operazione o singola risposta ha causato l’errore e sfruttare queste informazioni per perfezionare lo scenario.

>[!NOTE]
>
>La registrazione nel pannello Debugger sarà limitata o non disponibile per scenari riservati, esecuzioni automatiche e operazioni di successo.

>[!NOTE]
>
>Nella nuova esperienza, diversi strumenti DevTool sono incorporati nell’editor di scenari, in modo da poterli utilizzare senza aprire DevTool:
>
>| Strumento | Dove trovarlo nella nuova esperienza |
>| ---------- | ---------- |
>| Ottenere i metadati dell’app | Fare clic con il pulsante destro del mouse su un modulo e selezionare **Metadati app**. |
>| Copia mappatura | Fare clic con il pulsante destro del mouse sul modulo di origine, selezionare **Copia mapping**, quindi incollarlo in un modulo compatibile. |
>| Copia filtro | Fare clic con il pulsante destro del mouse sul collegamento filtrato, selezionare **Copia filtro**, quindi incollarlo in un altro collegamento. |
>| Copia nome modulo | Fare clic con il pulsante destro del mouse su un modulo e selezionare **Copia nome modulo** o **Incolla nome modulo**. |
>| Scambia connessione | Apri Trova e sostituisci, quindi utilizza la scheda **Connessione**. |
>| Scambia variabile | Apri Trova e sostituisci, quindi utilizza la scheda **Variabile**. |
>| Rimappatura origine | Apri Trova e sostituisci, quindi utilizza la scheda **Source**. |
>
>Questi strumenti sono ancora disponibili nella scheda **Strumenti** di DevTool, insieme a Focus a module, Find module by mapping e Base 64. È inoltre possibile utilizzare le funzioni `base64()` e di conversione binaria nelle mappature.
>
>Puoi anche visualizzare i dettagli delle richieste e delle risposte direttamente da [Live Trail](/help/workfront-fusion/manage-scenarios/live-trail.md) e la cronologia di esecuzione nell&#39;editor di scenari. Per ulteriori informazioni su Trova e sostituisci, vedere [Trovare e sostituire variabili, origini e connessioni in uno scenario](/help/workfront-fusion/manage-scenarios/find-and-replace.md).
<!-- BECKY CHECK ME: DevTool screenshots (10/27/26) show all ten tools still on the Tools tab, so this note now says the seven built-in tools are available in both places. The release notes implied only Focus a module, Find modules by mapping, and Base 64 would remain. Confirm after release whether the other seven are removed from the DevTool, and update this note and the Tools section if so.  -->
<!-- BECKY CHECK ME: note added from the 10/23/26 release notes; the DevTool is NOT being removed. This article still needs a fuller restructure (new/classic split for the seven tools, Live Trail section or separate article). Confirm the menu labels. -->

Per un video introduttivo e una descrizione dettagliata dello strumento Fusion Devtool, vedere

* [Strumento di sviluppo Fusion](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Procedura dettagliata Devtool](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=en)

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Accedere a Devtool

Se utilizzi Fusion in Adobe Unified Shell o hai eseguito l’aggiornamento alla nuova esperienza Fusion, puoi accedere a Devtool dall’editor scenari.

### Accedere a Devtool nella nuova esperienza

1. Passare all&#39;editor scenario per lo scenario di cui si desidera eseguire il debug.

   Per individuare l&#39;editor scenario, vedere [L&#39;editor scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Fare clic sull&#39;icona a tre punti nell&#39;area Controlli, quindi selezionare **DevTool**.

Oppure:

1. Passare all&#39;editor scenario per lo scenario di cui si desidera eseguire il debug.
1. Fai clic con il pulsante destro del mouse in un’area vuota della pagina (non in un modulo).
1. Selezionare **Apri Devtool**.

DevTool si apre in un pannello sotto l’area di lavoro.

<!-- BECKY CHECK ME: new-experience access steps from your 10/27/26 notes (three-dot menu in Controls, or right-click). Confirm the menu label ('DevTool') and the 'panel below the canvas' description, and add a screenshot. I assumed the Helper tools icon steps below apply to the classic experience only; confirm. -->

### Accedere a Devtool nell’esperienza classica

1. Fai clic sull&#39;icona **Helper tools** ![Helper tools](assets/debugger-icon.png) nella parte inferiore dello schermo.

Oppure:

1. Passare all&#39;editor scenario per lo scenario di cui si desidera eseguire il debug.

   Per individuare l&#39;editor scenario, vedere [L&#39;editor scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Fai clic con il pulsante destro del mouse in un’area vuota della pagina (non in un modulo).
1. Selezionare **Apri Devtool**.

## Utilizzare Workfront Fusion Devtool

Workfront Fusion Devtool è suddiviso in 3 sezioni principali, più un collegamento di aiuto. Puoi trovarli nel pannello a sinistra della finestra di Devtool.

* [Flusso live](#live-stream)
* [Debugger scenario](#scenario-debugger)
* [Strumenti](#tools)
* **Guida di DevTool**: fare clic sull&#39;icona del punto interrogativo per aprire l&#39;articolo relativo a DevTool.

<!-- BECKY CHECK ME: the DevTool left panel now has a fourth item, 'DevTool help' (question mark icon), per your 10/27/26 screenshots. Confirm the label, that it opens this article or another one, and whether to apply this to the classic experience too. Retake the left-panel screenshot. -->

### Live Stream

Live Stream mostra cosa accade in background quando fai clic su Esegui una volta nello scenario.

<!-- BECKY CHECK ME: HOLD: in the new experience, Live Stream shows a 'no events available' message even while a scenario is running, which may be a bug. No updates have been made to this section. Re-test after release before changing anything here. If it is intended behavior, this section may need to point to Live Trail instead. -->

1. Fai clic sull&#39;icona **[!UICONTROL Live Stream]** ![Live Stream icon](assets/live-stream-icon.png) per aprire la sezione Live Stream.
1. Effettua una delle seguenti operazioni:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Azione</th> 
      <th>Istruzioni</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">Visualizza informazioni richiesta</td> 
      <td> <p>Puoi visualizzare le seguenti informazioni per ogni modulo nello scenario</p> 
       <ul> 
        <li> <p>Intestazioni di richiesta (URL dell’endpoint API, metodo http, ora e data in cui è stata chiamata la richiesta, intestazioni di richiesta e stringa di query)</p> </li> 
        <li> <p>Corpo della richiesta</p> </li> 
        <li> <p>Intestazioni di risposta</p> </li> 
        <li> <p>Corpo risposta</p> </li> 
       </ul> <p>Per visualizzare queste informazioni, fate clic sulla scheda appropriata nel pannello destro di Workfront Fusion Devtool.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Cerca eventi per contenuto</p> </td> 
      <td> <p>Immettere il termine di ricerca nel campo di ricerca nel pannello sinistro di Workfront Fusion Devtool per visualizzare solo le richieste che contengono il termine di ricerca.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Cancella elenco di richieste </p> </td> 
      <td> <p>Fai clic sull’icona cestino nell’angolo in alto a destra del pannello di sinistra di Devtool per cancellare l’elenco delle richieste registrate da Workfront Fusion Devtool. </p> </td> 
     </tr> 
     <!--
     <tr>
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>
     -->
     <tr> 
      <td role="rowheader"> <p>Recuperare la richiesta nel formato Raw JSON o in cURL</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>JSON non elaborato</strong> </p> <p>Fare clic su <strong>[!UICONTROL Copy RAW]</strong> nell'angolo superiore destro del riquadro di destra di Devtool.</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>Fare clic su <strong>[!UICONTROL Copy cURL]</strong> nell'angolo superiore destro del riquadro di destra di Devtool.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Scenario Debugger

>[!NOTE]
>
>Per passare rapidamente al debugger da uno scenario che ha generato un errore, è possibile fare clic su **Ottieni dettagli** nel messaggio di errore nell&#39;output del modulo.
>
>![Ottieni dettagli nell&#39;output del modulo](assets/go-to-debugger.png)

Scenario Debugger è utile per scenari più complessi. Visualizza la cronologia dello scenario eseguito e consente di cercare i moduli in base al nome o all’ID.

1. Fai clic sull&#39;icona **[!UICONTROL Scenario Debugger]** ![icona Debugger](assets/scenario-debugger-icon.png) per aprire Scenario Debugger.

   Scenario Debugger elenca i moduli dello scenario. Ogni modulo mostra il proprio nome, l’app e l’azione, e un badge numerato con l’ID del modulo.

1. (Facoltativo) Immetti il termine di ricerca (nome o ID modulo) nel campo **Moduli di ricerca per nome o ID**.
1. Fai clic sul nome del modulo.

   I cicli dell’esecuzione più recente del modulo sono elencati accanto all’elenco dei moduli. Se il modulo non contiene dati di esecuzione, Scenario Debugger visualizza **Nessun risultato trovato**.

1. Espandere un ciclo, quindi fare clic su un&#39;operazione.

   Ogni operazione indica se è stata eseguita correttamente e il tempo impiegato, ad esempio **Operazione 1** con una durata di 0 ms.

1. Rivedi i dettagli della richiesta. Utilizza le schede per visualizzare:

   * **Intestazioni richiesta**: l&#39;URL dell&#39;endpoint API, il metodo HTTP, quando è stata chiamata la richiesta e le intestazioni della richiesta.
   * **Corpo richiesta**
   * **Intestazioni risposta**
   * **Corpo risposta**

1. (Facoltativo) Per copiare la richiesta, fai clic su **Copia RAW** o **Copia cURL**.

<!-- BECKY CHECK ME: Scenario Debugger steps expanded from your 10/27/26 new-experience DevTool screenshots. Confirm: (1) the 'Search modules by Name or ID' label; (2) that the module list sub-labels, badge (module ID), cycle/operation layout, and 'No Result found' state are described correctly; (3) the tab names, since Response Body was partly hidden behind the Copy buttons in the screenshot; (4) whether Copy RAW and Copy cURL copy the request only or the request and response; (5) whether the classic experience's Scenario Debugger looks the same, or this needs a new/classic split. The screenshot also shows a collapsed 'Live trail' tab with an event count on the right edge of the editor; see the Live Trail article. Retake the Scenario Debugger screenshots. -->

### Strumenti

Workfront Fusion Devtool offre strumenti che semplificano la configurazione dello scenario.

1. Fai clic sull&#39;icona **[!UICONTROL Strumenti]** ![Strumenti console](assets/console-tools-icon.png) per aprire gli Strumenti.
1. (Facoltativo) Per trovare uno strumento, immetterne il nome nel campo **Ricerca per nome**.
1. Selezionare lo strumento che si desidera utilizzare
1. Configura i campi come descritto di seguito.
1. Fare clic su **[!UICONTROL Esegui]**.

Fino a quando non selezionate uno strumento, il lato destro del pannello richiede di selezionarne uno. Un collegamento nella parte inferiore della scheda Strumenti consente di accedere all&#39;articolo relativo a DevTool.

<!-- BECKY CHECK ME: added from your 10/27/26 screenshots: the 'Search tool by name' field, the select-a-tool prompt, and the link to the DevTool article. Confirm the field label and link destination; retake the Tools screenshot. -->

Strumenti e relativi campi:

* [Attiva modulo](#focus-a-module)
* [Trova moduli per mappatura](#find-modules-by-mapping)
* [Ottieni metadati app](#get-app-metadata)
* [Copia mapping](#copy-mapping)
* [Copia Filtro](#copy-filter)
* [Copia nome modulo](#copy-module-name)
* [Scambia connessione](#swap-connection)
* [Scambia variabile](#swap-variable)
* [Base 64](#base-64)
* [Nuova mappatura di Source](#remap-source)

#### [!UICONTROL Attiva modulo]

Apre le impostazioni del modulo specificato in base all&#39;ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Module ID]</td>
        <td>Immetti l’ID del modulo per aprirne le impostazioni.</td>
    </tr>
</table>

#### [!UICONTROL Trova moduli per mappatura]

Consente di cercare i valori dei moduli per un termine specificato. L’output contiene ID di moduli che contengono il termine cercato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Parola chiave </td> 
   <td> <p> Immettere il termine che si desidera cercare. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Usa solo valori]</p> </td> 
   <td> <p>Abilita questa opzione per eseguire ricerche solo nei valori dei campi modulo.</p> <p>Disattiva questa opzione per eseguire ricerche anche nei nomi dei campi modulo.</p> <p>La ricerca viene eseguita tramite i parametri name ed label.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni metadati app]

Recupera i metadati dell’app in base al nome o all’ID del modulo dell’app. Questa funzione è utile, ad esempio, quando devi conoscere la versione dell’app utilizzata nel tuo scenario.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Modulo Source]</td>
        <td>Seleziona il modulo per il quale desideri recuperare i metadati.</td>
    </tr>
</table>

#### [!UICONTROL Copia mapping]

Copia i valori dal modulo di origine al modulo di destinazione.

>[!CAUTION]
>
>Assicurati di impostare i moduli di origine e di destinazione corretti. Se selezioni un tipo diverso di modulo, i valori nel modulo di destinazione verranno eliminati.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo Source]</td> 
   <td> <p> Seleziona il modulo o immetti l’ID del modulo da cui desideri copiare i valori dei campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Modulo Di Destinazione]</p> </td> 
   <td> <p>Seleziona il modulo o immetti l’ID del modulo in cui desideri inserire i valori del modulo sorgente.</p> <p>Importante: i valori nel modulo di destinazione verranno sovrascritti.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copia Filtro]

Copia le impostazioni del filtro dal modulo di origine al modulo di destinazione.

>[!NOTE]
>
>L&#39;azione di copia viene eseguita sul filtro posizionato sul lato sinistro del modulo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo Source]</td> 
   <td> <p> Seleziona il modulo o immetti l’ID del modulo da cui desideri copiare i valori del filtro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Modulo Di Destinazione]</p> </td> 
   <td> <p>Seleziona il modulo o immetti l’ID del modulo in cui desideri inserire i valori del filtro dal modulo sorgente.</p> <p>Importante: i valori nel modulo di destinazione verranno sovrascritti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Mantieni route di fallback]</p> </td> 
   <td> <p>Il filtro di origine viene impostato come route di fallback. Abilita questa opzione per impostare anche il filtro di destinazione impostato come route di fallback.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copia nome modulo]

Copia negli Appunti il nome del modulo selezionato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo] </td> 
   <td> <p>Seleziona il modulo di cui desideri copiare il nome.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scambia connessione]

Duplica una connessione dal modulo di origine a ogni modulo nello scenario della stessa app.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Modulo Source]</td>
        <td>Seleziona il modulo o immetti l’ID del modulo da cui desideri duplicare la connessione.</td>
    </tr>
</table>

#### [!UICONTROL Scambia variabile]

Cerca le variabili specificate nello scenario e le sostituisce con una nuova variabile.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variabile da trovare]</td> 
   <td> <p> Individua la pillola di variabili che desideri sostituire dal modulo di variabili nello scenario e copiala in questo campo ([!UICONTROL Variabile da trovare]). Nel campo, viene visualizzato con parentesi graffe doppie. Esempio: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sostituisci Con]</p> </td> 
   <td> <p>Individua la pillola di variabili con cui desideri sostituire la variabile dal modulo delle variabili nello scenario e copiala in questo campo ([!UICONTROL Variabile da trovare]). Nel campo, viene visualizzato con parentesi graffe doppie. Esempio: <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Modulo]</p> </td> 
   <td> <p>Seleziona il modulo delle variabili in cui desideri sostituire la variabile. Se non è selezionato alcun modulo, la variabile verrà sostituita nell’intero scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Consente di codificare i dati immessi in Base64 o di decodificare Base64. Alcune richieste sono codificate in Base64. Questo strumento può essere utile quando desideri cercare dati particolari nella richiesta codificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Specificare se si desidera codificare i dati dal campo [!UICONTROL Raw Data] in Base64 o decodificare Base64 in Dati non elaborati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Dati Non Elaborati]</p> </td> 
   <td> <p> Immettere i dati che si desidera codificare in Base64 o Base64 se si desidera decodificare in dati non elaborati, a seconda dell'opzione selezionata nel campo Operazione  precedente.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Nuova mappatura di Source]

Consente di cambiare l&#39;origine di mappatura da un modulo all&#39;altro.

È innanzitutto necessario aggiungere il modulo che si desidera utilizzare come modulo di origine al ciclo di lavorazione nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo Source] </td> 
   <td> <p> Seleziona il modulo da sostituire come origine di mappatura per altri moduli nello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Modulo Di Destinazione]</p> </td> 
   <td> <p>Selezionare il modulo da utilizzare come nuova origine di mappatura.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Modulo [!UICONTROL da modificare]</p> </td> 
   <td> <p>Selezionare il modulo per il quale si desidera modificare il mapping se non si desidera modificare il mapping nell'intero scenario. </p> </td> 
  </tr> 
 </tbody> 
</table>
