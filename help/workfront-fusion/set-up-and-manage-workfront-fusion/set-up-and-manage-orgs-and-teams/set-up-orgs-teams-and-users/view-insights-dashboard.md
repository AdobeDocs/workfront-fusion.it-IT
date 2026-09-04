---
title: Visualizzare la dashboard Approfondimenti per un’organizzazione
description: Gli amministratori di Fusion possono visualizzare un dashboard che mostra le metriche di esecuzione per un’organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 557ec6de4ccf0753005fed3e4772d2eb9317537d
workflow-type: tm+mt
source-wordcount: 848
ht-degree: 4%

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

* **Esecuzioni in attesa di elaborazione**
Questo grafico mostra il numero di esecuzioni in attesa di elaborazione (note anche come backlog di esecuzione) in un determinato momento.

  Un numero elevato di esecuzioni in attesa di elaborazione può influire sulle prestazioni dell’istanza di Fusion. Riceverai una notifica se il backlog di esecuzione raggiunge le 5000 esecuzioni. È consigliabile identificare gli scenari responsabili e modificarli o disattivarli. Se il backlog di esecuzione elevato persiste, il team Fusion proteggerà le prestazioni dell’istanza Fusion disabilitando gli scenari responsabili.
* **Utilizzo pool**
Questo grafico mostra l&#39;utilizzo del pool di lavoratori nel tempo. Se in questo grafico viene visualizzato di routine l&#39;utilizzo del pool di lavoratori, è possibile assegnare alcuni scenari a un altro pool.

  Se un pool si avvicina al 100% dell&#39;utilizzo, altre risorse che utilizzano lo stesso pool potrebbero subire ritardi o interruzioni. In questo caso, è consigliabile riassegnare uno scenario di utilizzo elevato a un altro pool di lavoro o modificare gli scenari esistenti in modo che richiedano meno risorse.
* **Esecuzioni per scenario**
Questo grafico mostra le esecuzioni per scenario. Colori diversi rappresentano scenari diversi. Quando passi il cursore del mouse sul grafico, viene visualizzata una finestra che mostra quale colore rappresenta lo scenario.

  È possibile utilizzare questo grafico per identificare gli scenari che potrebbero causare un backlog di esecuzione o un utilizzo elevato del pool di lavoro.
* **Durata delle esecuzioni**
Questo grafico mostra le esecuzioni per scenario. Colori diversi rappresentano scenari diversi. Quando passi il cursore del mouse sul grafico, viene visualizzata una finestra che mostra quale colore rappresenta lo scenario.

  Puoi utilizzare questo grafico per identificare scenari che richiedono più tempo del solito, inclusi quelli interessati da problemi con un’app o un servizio connesso.
* **Registro di esecuzione**
In questa tabella vengono elencati tutti gli scenari di errore o di avviso eseguiti nell’organizzazione, in modo da poter individuare e risolvere i problemi senza uscire dal dashboard.

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

   <!-- BECKY CHECK ME: confirm this button's exact label against the live UI. The Slack feature request calls it "Activate," but a related community post describes the same action as "Reactivate." -->

   Prima di riattivare uno scenario, indaga la causa degli errori, ad esempio credenziali scadute o un problema del connettore, in modo che lo scenario non si riproduca immediatamente.
