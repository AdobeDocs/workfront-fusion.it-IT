---
title: Eseguire l’esperto di punteggio scenario
description: L’esperto di valutazione degli scenari può aiutarti a garantire che lo scenario sia configurato nel modo che segue le best practice. Controlla lo scenario e fornisce consigli per la sua struttura e organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Eseguire l’esperto di punteggio scenario

>[!IMPORTANT]
>
>L&#39;esperto punteggio scenario è stato temporaneamente disabilitato.

L’esperto di valutazione degli scenari può aiutarti a garantire che lo scenario sia configurato nel modo che segue le best practice. Controlla lo scenario e fornisce consigli per la sua struttura e organizzazione.

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Eseguire l’esperto di punteggio scenario

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera eseguire l&#39;esperto punteggio scenario.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic sull&#39;icona Esperto punteggio scenario ![Esperto punteggio scenario](assets/scoring-expert-icon.png) nella parte inferiore dello schermo.

   Viene visualizzato il pannello Esperto punteggio scenario.
1. Fare clic su **Valuta**.

L’esperto di punteggio dello scenario restituisce un punteggio su 10 e mostra quali controlli sono stati superati o non riusciti. Se un controllo non è riuscito, l’esperto di valutazione dello scenario fornisce consigli su come garantire che lo scenario soddisfi questi controlli.

![Punteggio scenario](assets/scenario-score.png)

## Controlli punteggio scenario

L’esperto di valutazione degli scenari utilizza i seguenti controlli:

* Lo scenario deve essere denominato.
* Tutti i moduli devono essere etichettati.
* Lo scenario deve essere eseguito in base a una pianificazione impostata.

  Per istruzioni, consulta [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* La dimensione del blueprint dello scenario deve essere inferiore a 5 MB.

  Per ulteriori informazioni, vedere [Guardrail delle prestazioni di Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* Se viene utilizzato un modulo di attivazione immediata di Workfront, deve essere filtrato.

  Per istruzioni, consulta [Filtri abbonamento eventi nel modulo Workfront > [!UICONTROL Osserva eventi]](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
