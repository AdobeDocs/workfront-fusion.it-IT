---
title: Visualizzare e risolvere le esecuzioni incomplete
description: Nella cartella [!UICONTROL Incomplete executions] sono archiviate esecuzioni dello scenario che non sono state completate correttamente a causa di un errore. Ogni esecuzione incompleta archiviata può essere risolta manualmente o automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---

# Visualizzare la cronologia di esecuzione di uno scenario

È possibile visualizzare informazioni sugli eventi o sulle esecuzioni di uno scenario oppure cercare dati specifici in tutte le esecuzioni dello scenario.

L’esecuzione di uno scenario rappresenta una singola esecuzione dello scenario.

Un evento scenario è una modifica allo scenario, ad esempio la modifica, l’attivazione o la disattivazione.

>[!NOTE]
>
>La cronologia di uno scenario visualizza tutti gli eventi e le esecuzioni dello scenario per gli ultimi 30 giorni.

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
   <td> <p>Nuovo: [!UICONTROL Standard]</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per la tua organizzazione.</p>
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visualizzare la cronologia dello scenario


### Visualizzare la cronologia degli scenari nella scheda Cronologia

La scheda [!UICONTROL History] mostra più dettagli di quelli disponibili nella pagina [!UICONTROL Scenario detail]. È inoltre possibile filtrare e ordinare le esecuzioni nella scheda [!UICONTROL History].

1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenari, fare clic sulla freccia sinistra ![](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic su **Cronologia** accanto al nome dello scenario.
   ![scheda cronologia](assets/history-tab.png)

   Per ogni esecuzione dello scenario sono elencati i seguenti dettagli:

   * Data di esecuzione: **[!UICONTROL Started]**
   * ID esecuzione
   * **[!UICONTROL Status]** (operazione riuscita o non riuscita)
   * Esegui **[!UICONTROL Duration]**
   * Numero di **[!UICONTROL Operations]**
   * Dimensione di **[!UICONTROL Data Transfer]**

   >[!NOTE]
   >
   >Nella cronologia degli scenari viene visualizzato un contrassegno **Elaborazione** accanto agli scenari eseguiti di recente, mentre i dettagli di esecuzione vengono scritti nell&#39;archivio. L’elaborazione si verifica immediatamente dopo l’esecuzione dello scenario. e non dovrebbe durare più di qualche minuto. I dettagli dell’esecuzione dello scenario potrebbero non essere visibili durante l’elaborazione dell’esecuzione.

1. Per visualizzare i dettagli di un&#39;esecuzione di uno scenario specifico, fare clic su **Dettagli** all&#39;estrema destra. Il collegamento [!UICONTROL details] è visibile solo se sono disponibili dettagli sull&#39;esecuzione.
1. Per visualizzare gli eventi, attiva **Mostra eventi**.


### Visualizzare la cronologia dello scenario nella pagina Dettagli scenario


1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenari, fare clic sulla freccia sinistra ![](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic sulla scheda **[!UICONTROL History]** nel pannello di destra.
1. (Facoltativo) Per informazioni dettagliate sull’esecuzione di uno scenario selezionato, fai clic sull’esecuzione nel pannello a destra.

   Per ulteriori informazioni sull&#39;elaborazione dei bundle, vedi [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* La cronologia degli scenari visualizza un contrassegno **Cronologia elaborazione** accanto agli scenari eseguiti di recente, mentre i dettagli di esecuzione vengono scritti nell&#39;archivio. L’elaborazione si verifica immediatamente dopo l’esecuzione dello scenario. e non dovrebbe durare più di qualche minuto. I dettagli dell’esecuzione dello scenario potrebbero non essere visibili durante l’elaborazione dell’esecuzione.

1. Per visualizzare gli eventi, fare clic sulla scheda **Eventi**.

## Filtrare la cronologia di esecuzione dello scenario

Puoi filtrare la cronologia di esecuzione per visualizzare solo le esecuzioni con i valori specificati.

1. Aprire la cronologia a pagina intera per uno scenario come descritto in [Visualizzare la cronologia di esecuzione dello scenario nella scheda [!UICONTROL History]](#view-scenario-history-on-the-history-tab) in questo articolo.
1. Fare clic sull&#39;icona [!UICONTROL filter] ![](assets/fusion-scenario-filter-icon.png) nell&#39;intestazione della colonna in base alla quale si desidera filtrare.
1. Nella finestra di dialogo [!UICONTROL filter], immettere i valori in base ai quali si desidera filtrare.
1. Fare clic su **[!UICONTROL Save]**.

L’icona del filtro è arancione nelle colonne con un filtro attivo.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Cercare tutte le esecuzioni di uno scenario

1. Aprire la cronologia a pagina intera per uno scenario come descritto in [Visualizzare la cronologia di esecuzione dello scenario nella scheda [!UICONTROL History]](#view-scenario-history-on-the-history-tab) in questo articolo.
1. Fai clic su **[!UICONTROL Fulltext search]** in alto nell&#39;elenco delle esecuzioni.

   Oppure

   Digitare **Ctrl+Maiusc+F** (Windows) o **Cmd+Maiusc+F** (Mac)
Viene visualizzata la finestra [!UICONTROL Search in history].

1. (Facoltativo) Per cercare esecuzioni contenenti testo specifico, immettere il testo nella barra di ricerca della finestra **[!UICONTROL Search in history]**.

   Per cercare il testo esatto, racchiuderlo tra virgolette doppie (&quot;esempio&quot;).

   >[!INFO]
   >
   >**Esempio:** Se desideri trovare l&#39;esecuzione che ha creato un progetto specifico, immetti l&#39;ID del progetto nella barra [!UICONTROL Fulltext search].
   >
   >&quot;625ef2ef0006036bd1794b6e52d737c5&quot;

1. (Facoltativo) Per limitare la ricerca in base all&#39;intervallo di date, selezionare le date di inizio e fine della ricerca desiderata nell&#39;area [!UICONTROL By date range].

   >[!NOTE]
   >
   >* Le esecuzioni sono disponibili solo per i 30 giorni precedenti.
   >
   >* [!DNL Workfront Fusion] memorizza i payload del webhook per 30 giorni. L&#39;accesso a un payload del webhook oltre 30 giorni dopo la sua creazione causa l&#39;errore &quot;[!UICONTROL Failed to read file from storage.]&quot;


1. (Facoltativo) Per limitare la ricerca in base allo stato, selezionare lo stato desiderato nel menu a discesa **[!UICONTROL By status]**.


   Gli stati disponibili sono:

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Facoltativo) Modificare l&#39;ordine di visualizzazione dei risultati nel menu a discesa **[!UICONTROL Sort by dates]**.

1. (Facoltativo) Per copiare un ID di esecuzione di uno scenario, fai clic sull&#39;icona **[!UICONTROL Copy execution ID]** <img src="assets/copy-fusion-execution-id-icon.png"> nella riga dell&#39;esecuzione desiderata.

1. (Facoltativo) Fare clic su un risultato di [!UICONTROL Fulltext search] per esaminare il bundle di output del modulo scenario contenente le informazioni.