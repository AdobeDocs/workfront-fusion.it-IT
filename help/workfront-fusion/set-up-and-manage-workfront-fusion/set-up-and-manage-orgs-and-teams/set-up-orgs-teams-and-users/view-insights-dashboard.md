---
title: Visualizzare la dashboard Approfondimenti per un’organizzazione
description: Gli amministratori di Fusion possono visualizzare un dashboard che mostra le metriche di esecuzione per un’organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 3%
---
# Visualizzare la dashboard Approfondimenti per un’organizzazione

Il dashboard Fusion Insights consente di vedere rapidamente quali scenari sono più in esecuzione, dove si verificano ritardi e con quale efficacia funzionano i pool di lavoro. Questo fornisce visibilità in tempo reale sui volumi di esecuzione, sulla profondità della coda, sull’utilizzo del pool e sulle prestazioni a livello di scenario.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Flusso di lavoro di Adobe Workfront Ultimate e Adobe Workfront Automazione e integrazione Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Componenti del dashboard Approfondimenti

>[!NOTE]
>
>Le metriche vengono visualizzate per pool di lavoro. Per visualizzare un pool di lavoro diverso, fare clic sul campo Pool nell&#39;angolo superiore sinistro del dashboard, quindi selezionare il pool per il quale si desidera visualizzare le metriche.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Nel dashboard Fusion Insights puoi visualizzare le metriche seguenti.

* **Registri esecuzioni non riuscite**
In questa tabella vengono elencati tutti gli scenari di errore o di avviso eseguiti nell’organizzazione, in modo da poter individuare e risolvere i problemi senza uscire dal dashboard.
* **Operazioni organizzazione**
Questo grafico consente di visualizzare il numero di operazioni utilizzate nell’organizzazione. È possibile selezionare team o scenari specifici e visualizzare le operazioni dell&#39;ultima settimana, mese o anno.
* **Scenari principali per operazioni**
Questo grafico consente di visualizzare quali scenari utilizzano il maggior numero di operazioni. Puoi selezionare team specifici o visualizzare i dati dell’ultimo giorno, settimana o mese.

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

## Visualizzare il dashboard di Fusion Insights

1. In Fusion, fai clic su **Approfondimenti** nell&#39;area di navigazione a sinistra.

   Viene visualizzata la dashboard.

1. Per visualizzare i dati relativi a un determinato point in time, posizionare il cursore del mouse su un dashboard e posizionare il cursore sul point in time desiderato.

   Su tutti i grafici viene visualizzata una linea sopra quel punto nel tempo e in ciascun grafico viene visualizzata una finestra con i dati relativi a quel momento.
1. Per visualizzare i dati di uno scenario specifico nel grafico Esecuzioni per scenario o nel grafico Durata delle esecuzioni, fare clic su una barra del colore dello scenario per il quale si desidera visualizzare i dati. Per tornare alla visualizzazione che mostra tutti gli scenari, fai di nuovo clic sul grafico.
1. Per passare a uno scenario specifico visualizzato nel grafico Esecuzioni per scenario o nel grafico Durata delle esecuzioni, fare clic con il pulsante destro del mouse su una barra del colore dello scenario e selezionare **Apri scenario nella nuova scheda**.
1. Per espandere un grafico, fare clic sull&#39;icona **Espandi** ![Espandi icona](assets/expand-icon.png) nell&#39;angolo superiore destro del grafico.
1. Per modificare l&#39;intervallo di tempo del dashboard, selezionare il campo Intervallo di tempo nell&#39;angolo superiore destro del dashboard, quindi selezionare un nuovo intervallo di tempo. L’intervallo di tempo disponibile più lungo è di 24 ore e il più breve è di 15 minuti.
1. Per aggiornare i grafici, fare clic sull&#39;icona Aggiorna nell&#39;angolo superiore destro del dashboard.
1. Per visualizzare un pool di lavoro diverso, fare clic sul campo Pool nell&#39;angolo superiore sinistro del dashboard, quindi selezionare il pool da visualizzare.

## Personalizzare la dashboard Approfondimenti

Puoi scegliere quali widget visualizzare nel dashboard Approfondimenti e in quale ordine.

### Aggiungere, rimuovere o riordinare widget

1. Nel menu di navigazione a sinistra, fai clic su **Informazioni** ![Icona Approfondimenti](assets/insights-icon.png).
1. Fai clic su **[!UICONTROL Personalizza]** nell&#39;intestazione Approfondimenti.

   Viene visualizzato un pannello laterale. Elenca ogni widget come una scheda che mostra un’anteprima, il nome del widget e una descrizione.

1. Per mostrare o nascondere un widget, fare clic sulla relativa scheda oppure fare clic sul pulsante **[!UICONTROL Aggiungi widget]** o **[!UICONTROL Rimuovi widget]** sulla scheda.

   I widget visualizzati hanno un segno di spunta.
1. Per riordinare i widget, trascina una scheda widget in una nuova posizione nel pannello.

   Un segnaposto tratteggiato e una barra a discesa indicano dove verrà posizionata la scheda.

Le scelte vengono salvate per browser. I widget aggiunti nelle versioni successive vengono visualizzati automaticamente nel pannello.

Se rimuovi tutti i widget, nella pagina viene visualizzato il messaggio &quot;Nessun widget in questa pagina&quot;.

## Aggiorna la dashboard Approfondimenti

Per ricaricare i dati di ogni widget, fai clic su **[!UICONTROL Aggiorna]** accanto a **[!UICONTROL Personalizza]**.

* Ogni widget mantiene i propri filtri.
* Il pulsante **[!UICONTROL Aggiorna]** mostra uno stato in sospeso fino al completamento del caricamento di tutti i widget.
* I grafici mantengono il grafico precedente sotto un’estensione di caricamento, mentre il registro esecuzioni riduce la tabella sotto un’estensione durante il ricaricamento dei dati.
* Se un aggiornamento non riesce, i widget conservano gli ultimi dati validi.

## Presentazione di Insights

La prima volta che apri la dashboard Approfondimenti, una finestra di dialogo di benvenuto ti consente di avviare una presentazione o di saltarla.

La presentazione evidenzia ogni widget, nell&#39;ordine salvato, nonché il pulsante e il pannello **[!UICONTROL Personalizza]**, il pulsante **[!UICONTROL Aggiorna]** e il pulsante **[!UICONTROL Riproduci presentazione]** nella barra del titolo.

Per riavviare la presentazione in qualsiasi momento, fare clic sull&#39;icona delle informazioni sulla presentazione ![icona informazioni](assets/insights-tour-information.png) nella barra del titolo.

La presentazione non inizia quando apri la dashboard Approfondimenti da un collegamento in uno scenario. Per ulteriori informazioni, vedere [Aprire la dashboard Approfondimenti da uno scenario](#open-the-insights-dashboard-from-a-scenario) in questo articolo.

## Cerca scenari e team per ID

Nei widget **[!UICONTROL Operazioni organizzazione]** e **[!UICONTROL Scenari principali per operazioni]**, i campi **[!UICONTROL Scenario]** e **[!UICONTROL Team]** corrispondono per ID e nome. Ogni opzione mostra il proprio ID sotto il nome, ad esempio &quot;ID 123&quot;.

* Gli elenchi caricano i primi 500 scenari e i primi 200 team. Se si immette un ID non presente nell&#39;elenco caricato, Fusion lo cerca automaticamente dopo un breve ritardo.
* Se si cancella uno scenario, viene cancellato anche il team che è stato compilato automaticamente per quello scenario.

>[!NOTE]
>
>Il filtro dello scenario nel registro esecuzioni non corrisponde per l’ID.

## Apri la dashboard Approfondimenti da uno scenario

Puoi aprire il dashboard Approfondimenti con il widget **[!UICONTROL Operazioni organizzazione]** filtrato per uno scenario e un team specifici.

Per passare alla pagina Approfondimenti da uno scenario:

1. Apri la pagina dei dettagli dello scenario:

   1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic su uno scenario su cui desideri visualizzare i dettagli.

      Oppure

      Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.
      1. Fai clic sulla scheda **Rapporti** nella parte superiore della pagina.

* Il widget **[!UICONTROL Operazioni organizzazione]** viene aperto filtrato in base allo scenario e al team e la pagina scorre fino al widget.
* Se hai rimosso il widget dalla pagina, viene invece visualizzato un avviso con un pulsante **[!UICONTROL Aggiungi widget]**.

## Usa modalità scura

La dashboard di Insights e i relativi widget seguono automaticamente l’impostazione della modalità scura. Quando modifichi l’impostazione, la pagina si aggiorna immediatamente, senza ricaricare, e mantiene lo stato corrente. La modalità Light (Luce) non viene modificata.

## Accesso widget prestazioni

Il widget **[!UICONTROL Prestazioni]** viene visualizzato solo agli utenti che dispongono di una delle seguenti autorizzazioni:

* Modifica organizzazione nell’organizzazione attiva
* Vista organizzazione nella pagina di amministrazione

Il widget è nascosto dalla pagina e dal pannello **[!UICONTROL Personalizza]** per altri utenti. Se un utente ottiene l’accesso in un secondo momento, il widget torna nella posizione in cui è stato salvato. L’apertura diretta dell’URL di Insights non ignora questo controllo.

## Filtrare e valutare le esecuzioni nel registro di esecuzione

Utilizza il registro di esecuzione per trovare le esecuzioni degli scenari che hanno avuto esito negativo o hanno restituito un avviso nell’organizzazione e riattivare tutti gli scenari che sono stati disattivati automaticamente dopo errori ripetuti.

1. Nel registro di esecuzione, filtrare le esecuzioni in base a una delle seguenti opzioni:

   * [!UICONTROL Team]
   * [!UICONTROL Scenario]
   * [!UICONTROL Esegui tipo]
   * [!UICONTROL Intervallo date]
   * [!UICONTROL Stato disattivazione]
   * [!UICONTROL Messaggio di errore]

   Per la maggior parte dei filtri, puoi scegliere di far corrispondere solo i valori selezionati o tutto tranne loro.

1. Fai clic su un’esecuzione per visualizzare ulteriori dettagli sul relativo errore.
1. Per riattivare uno o più scenari disattivati automaticamente dopo errori ripetuti, selezionare le esecuzioni, quindi fare clic su **Attiva**.

   >[!NOTE]
   >
   >Prima di riattivare uno scenario, indaga la causa degli errori, ad esempio credenziali scadute o un problema del connettore, in modo che lo scenario non si riproduca immediatamente.
