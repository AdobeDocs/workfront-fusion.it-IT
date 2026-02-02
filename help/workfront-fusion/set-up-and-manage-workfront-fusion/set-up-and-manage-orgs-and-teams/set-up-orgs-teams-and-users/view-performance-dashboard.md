---
title: Visualizzare la dashboard delle prestazioni per un’organizzazione
description: Gli amministratori di Fusion possono visualizzare un dashboard che mostra le metriche di esecuzione per un’organizzazione.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: b4c9cd075cc2bb7aa3d5c568bb91fb8ce5c6f31e
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 7%

---

# Visualizzare la dashboard delle prestazioni per un’organizzazione

Il dashboard delle prestazioni di Fusion consente di vedere rapidamente quali scenari sono più in esecuzione, dove si verificano ritardi e con quale efficacia funzionano i pool di lavoro. Questo fornisce visibilità in tempo reale sui volumi di esecuzione, sulla profondità della coda, sull’utilizzo del pool e sulle prestazioni a livello di scenario.

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

## Componenti del dashboard prestazioni

>[!NOTE]
>
>Le metriche vengono visualizzate per pool di lavoro. Per visualizzare un pool di lavoro diverso, fare clic sul campo Pool nell&#39;angolo superiore sinistro del dashboard, quindi selezionare il pool per il quale si desidera visualizzare le metriche.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Nel dashboard delle prestazioni di Fusion sono disponibili le metriche seguenti.

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

## Visualizzare il dashboard delle prestazioni di Fusion

1. In Fusion, fai clic su Prestazioni nel menu di navigazione a sinistra.

   Viene visualizzata la dashboard.

1. Per visualizzare i dati relativi a un determinato point in time, posizionare il cursore del mouse su un dashboard e posizionare il cursore sul point in time desiderato.

   Su tutti i grafici viene visualizzata una linea sopra quel punto nel tempo e in ciascun grafico viene visualizzata una finestra con i dati relativi a quel momento.
1. Per visualizzare i dati di uno scenario specifico nel grafico Esecuzioni per scenario o nel grafico Durata delle esecuzioni, fare clic su una barra del colore dello scenario per il quale si desidera visualizzare i dati. Per tornare alla visualizzazione che mostra tutti gli scenari, fai di nuovo clic sul grafico.
1. Per passare a uno scenario specifico visualizzato nel grafico Esecuzioni per scenario o nel grafico Durata delle esecuzioni, fare clic con il pulsante destro del mouse su una barra del colore dello scenario e selezionare **Apri scenario nella nuova scheda**.
1. Per espandere un grafico, fare clic sull&#39;icona **Espandi** ![Espandi icona](assets/expand-icon.png) nell&#39;angolo superiore destro del grafico.
1. Per modificare l&#39;intervallo di tempo del dashboard, selezionare il campo Intervallo di tempo nell&#39;angolo superiore destro del dashboard, quindi selezionare un nuovo intervallo di tempo. L’intervallo di tempo disponibile più lungo è di 24 ore e il più breve è di 15 minuti.
1. Per aggiornare i grafici, fare clic sull&#39;icona Aggiorna nell&#39;angolo superiore destro del dashboard.
1. Per visualizzare un pool di lavoro diverso, fare clic sul campo Pool nell&#39;angolo superiore sinistro del dashboard, quindi selezionare il pool da visualizzare.



