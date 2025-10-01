---
title: Visualizzare la cronologia di esecuzione di uno scenario
description: È possibile visualizzare informazioni sugli eventi o sulle esecuzioni di uno scenario oppure cercare dati specifici in tutte le esecuzioni dello scenario.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: c0a4e563657871f856b7d449432d563c6caa27a1
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 1%

---

# Visualizzare la cronologia di esecuzione di uno scenario

È possibile visualizzare informazioni sugli eventi o sulle esecuzioni di uno scenario oppure cercare dati specifici in tutte le esecuzioni dello scenario.

L’esecuzione di uno scenario rappresenta una singola esecuzione dello scenario.

Un evento scenario è una modifica allo scenario, ad esempio la modifica, l’attivazione o la disattivazione.

>[!NOTE]
>
>La cronologia di uno scenario visualizza tutte le esecuzioni dello scenario negli ultimi 30 giorni.

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

## Visualizzare la cronologia dello scenario


### Visualizzare la cronologia degli scenari nella scheda Cronologia

La scheda [!UICONTROL Cronologia] mostra più dettagli di quelli disponibili nella pagina [!UICONTROL Dettagli scenario]. Puoi anche filtrare e ordinare le esecuzioni nella scheda [!UICONTROL Cronologia].

1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic su **Cronologia** accanto al nome dello scenario.
   ![scheda cronologia](assets/history-tab.png)

   Per ogni esecuzione dello scenario sono elencati i seguenti dettagli:

   * Data in cui è stata **[!UICONTROL avviata]**
   * ID esecuzione
   * **[!UICONTROL Stato]** (operazione riuscita o non riuscita)
   * Esegui **[!UICONTROL Durata]**
   * Numero di **[!UICONTROL operazioni]**
   * Dimensione di **[!UICONTROL Trasferimento dati]**

   >[!NOTE]
   >
   >Nella cronologia degli scenari viene visualizzato un contrassegno **Elaborazione** accanto agli scenari eseguiti di recente, mentre i dettagli di esecuzione vengono scritti nell&#39;archivio. L’elaborazione si verifica immediatamente dopo l’esecuzione dello scenario. e non dovrebbe durare più di qualche minuto. I dettagli dell’esecuzione dello scenario potrebbero non essere visibili durante l’elaborazione dell’esecuzione.

1. Per visualizzare i dettagli di un&#39;esecuzione di uno scenario specifico, fare clic su **Dettagli** all&#39;estrema destra. Il collegamento [!UICONTROL details] è visibile solo se sono disponibili dettagli sull&#39;esecuzione.

   Per ulteriori informazioni sulla visualizzazione dei dettagli di esecuzione dello scenario, vedere [Visualizzare un&#39;esecuzione dello scenario specifica](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).
1. Per visualizzare gli eventi, attiva **Mostra eventi**.


### Visualizzare la cronologia dello scenario nella pagina Dettagli scenario


1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fai clic sulla scheda **[!UICONTROL Cronologia]** nel pannello di destra.
1. (Facoltativo) Per informazioni dettagliate sull’esecuzione di uno scenario selezionato, fai clic sull’esecuzione nel pannello a destra.

   Per ulteriori informazioni sull&#39;elaborazione dei bundle, vedi [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* La cronologia degli scenari visualizza un contrassegno **Cronologia elaborazione** accanto agli scenari eseguiti di recente, mentre i dettagli di esecuzione vengono scritti nell&#39;archivio. L’elaborazione si verifica immediatamente dopo l’esecuzione dello scenario. e non dovrebbe durare più di qualche minuto. I dettagli dell’esecuzione dello scenario potrebbero non essere visibili durante l’elaborazione dell’esecuzione.

1. Per visualizzare gli eventi, fare clic sulla scheda **Eventi**.

## Filtrare la cronologia di esecuzione dello scenario

Puoi filtrare la cronologia di esecuzione per visualizzare solo le esecuzioni con i valori specificati.

1. Aprire la cronologia a pagina intera per uno scenario come descritto in [Visualizzare la cronologia di esecuzione dello scenario nella scheda [!UICONTROL Cronologia]](#view-scenario-history-on-the-history-tab) in questo articolo.
1. Fai clic sull&#39;icona [!UICONTROL filter] ![Icona filtro scenario](assets/fusion-scenario-filter-icon.png) nell&#39;intestazione della colonna in base alla quale desideri filtrare.
1. Nella finestra di dialogo [!UICONTROL filter], immetti i valori in base ai quali desideri filtrare.
1. Fai clic su **[!UICONTROL Salva]**.

L’icona del filtro è arancione nelle colonne con un filtro attivo.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Cercare tutte le esecuzioni di uno scenario

1. Aprire la cronologia a pagina intera per uno scenario come descritto in [Visualizzare la cronologia di esecuzione dello scenario nella scheda [!UICONTROL Cronologia]](#view-scenario-history-on-the-history-tab) in questo articolo.
1. Fai clic su **[!UICONTROL Ricerca full-text]** in alto nell&#39;elenco delle esecuzioni.

   Oppure

   Digitare **Ctrl+Maiusc+F** (Windows) o **Cmd+Maiusc+F** (Mac)
Viene visualizzata la finestra [!UICONTROL Cerca nella cronologia].

1. (Facoltativo) Per cercare esecuzioni contenenti testo specifico, immettere il testo nella barra di ricerca della finestra **[!UICONTROL Cerca nella cronologia]**.

   Per cercare il testo esatto, racchiuderlo tra virgolette doppie (&quot;esempio&quot;).

   >[!INFO]
   >
   >**Esempio:** Se desideri trovare l&#39;esecuzione che ha creato un progetto specifico, immetti l&#39;ID del progetto nella barra di [!UICONTROL Ricerca full-text].
   >
   >&quot;625ef2ef0006036bd1794b6e52d737c5&quot;

1. (Facoltativo) Per limitare la ricerca in base all&#39;intervallo di date, selezionare le date di inizio e fine della ricerca desiderata nell&#39;area [!UICONTROL Per intervallo di date].

   >[!NOTE]
   >
   >* Le esecuzioni sono disponibili solo per i 30 giorni precedenti.
   >
   >* Workfront Fusion memorizza i payload del webhook per 30 giorni. L&#39;accesso a un payload del webhook dopo più di 30 giorni dalla creazione genera l&#39;errore &quot;[!UICONTROL Impossibile leggere il file dall&#39;archivio.]&quot;


1. (Facoltativo) Per limitare la ricerca in base allo stato, seleziona lo stato desiderato nel menu a discesa **[!UICONTROL Per stato]**.


   Gli stati disponibili sono:

   * [!UICONTROL Tutti]

   * [!UICONTROL Errore]

   * [!UICONTROL Avvertenza]

   * [!UICONTROL Operazione riuscita]

1. (Facoltativo) Modifica l&#39;ordine di visualizzazione dei risultati nel menu a discesa **[!UICONTROL Ordina per date]**.

1. (Facoltativo) Per copiare un ID di esecuzione dello scenario, fai clic sull&#39;icona **[!UICONTROL Copia ID esecuzione]** <img src="assets/copy-fusion-execution-id-icon.png"> nella riga dell&#39;esecuzione desiderata.

1. (Facoltativo) Fai clic su un risultato della [!UICONTROL ricerca full-text] per esaminare il bundle di output del modulo scenario contenente le informazioni.
