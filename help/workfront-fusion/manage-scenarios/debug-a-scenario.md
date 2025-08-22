---
title: Debug di uno scenario
description: Adobe Workfront Fusion Devtool consente di comprendere e risolvere gli scenari. Devtool aggiunge un pannello aggiuntivo a Chrome Developer Tools. Utilizzando questo pannello di debugger, puoi controllare tutte le esecuzioni manuali dello scenario, esaminare tutte le operazioni eseguite e visualizzare i dettagli di ogni chiamata API eseguita. Puoi vedere quale modulo, operazione o singola risposta ha causato l’errore e sfruttare queste informazioni per perfezionare lo scenario.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Debug di uno scenario

Adobe Workfront Fusion Devtool consente di comprendere e risolvere gli scenari. Utilizzando Devtool, puoi controllare tutte le esecuzioni manuali dello scenario, esaminare tutte le operazioni eseguite e visualizzare i dettagli di ogni chiamata API eseguita. Puoi vedere quale modulo, operazione o singola risposta ha causato l’errore e sfruttare queste informazioni per perfezionare lo scenario.

>[!NOTE]
>
>La registrazione nel pannello Debugger sarà limitata o non disponibile per scenari riservati, esecuzioni automatiche e operazioni di successo.

Per un video introduttivo e una descrizione dettagliata dello strumento Fusion Devtool, vedere

* [Strumento di sviluppo Fusion](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Procedura dettagliata per Devtool](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=en)

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
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Accedere a Devtool

Se utilizzi Fusion in Adobe Unified Shell o hai eseguito l’aggiornamento alla nuova esperienza Fusion, puoi accedere a Devtool dall’editor scenari.

1. Fai clic sull&#39;icona **Helper tools** ![Helper tools](assets/debugger-icon.png) nella parte inferiore dello schermo.

Oppure:

1. Passare all&#39;editor scenario per lo scenario di cui si desidera eseguire il debug.

   Per individuare l&#39;editor scenario, vedere [L&#39;editor scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Fai clic con il pulsante destro del mouse in un’area vuota della pagina (non in un modulo).
1. Selezionare **Apri Devtool**.

## Utilizzare Workfront Fusion Devtool

Workfront Fusion Devtool è suddiviso in 3 sezioni principali. Puoi trovarli nel pannello a sinistra della finestra di Devtool.

* [Flusso live](#live-stream)
* [Debugger scenario](#scenario-debugger)
* [Strumenti](#tools)

### Live Stream

Live Stream mostra cosa accade in background quando fai clic su Esegui una volta nello scenario.

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
     <!--<tr> 
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>-->
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

Scenario Debugger è utile per scenari più complessi. Visualizza la cronologia dello scenario eseguito e consente di cercare i moduli in base al nome o all’ID.

1. Fai clic sull&#39;icona **[!UICONTROL Scenario Debugger]** ![icona Debugger](assets/scenario-debugger-icon.png) per aprire Scenario Debugger.
1. (Facoltativo) Immetti il termine di ricerca (nome o ID modulo) nel campo di ricerca.
1. Fai clic sul nome del modulo.
1. Fare clic sull&#39;operazione per visualizzare i dettagli della richiesta.

### Strumenti

Workfront Fusion Devtool offre strumenti che semplificano la configurazione dello scenario.

1. Fai clic sull&#39;icona **[!UICONTROL Strumenti]** ![Strumenti console](assets/console-tools-icon.png) per aprire gli Strumenti.
1. Selezionare lo strumento che si desidera utilizzare
1. Configura i campi come descritto di seguito.
1. Fare clic su **[!UICONTROL Esegui]**.

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
   <td role="rowheader">Parola chiave [!UICONTROL]</td> 
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
   <td role="rowheader">[!UICONTROL Module] </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
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
   <td> <p> Immettere i dati che si desidera codificare in Base64 o Base64 se si desidera decodificare in dati non elaborati, a seconda dell'opzione selezionata nel campo Operazione [!UICONTROL] precedente.</p> </td> 
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
