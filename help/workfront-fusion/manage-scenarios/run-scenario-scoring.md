---
title: Eseguire l’esperto di punteggio scenario
description: L’esperto di valutazione degli scenari può aiutarti a garantire che lo scenario sia configurato nel modo che segue le best practice. Controlla lo scenario e fornisce consigli per la sua struttura e organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 1ac1c4358901ef81bb7375c24fcdf1a44119af13
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 1%

---

# Eseguire l’esperto di punteggio scenario

>[!IMPORTANT]
>
>L&#39;esperto punteggio scenario è stato temporaneamente disabilitato.

L’esperto di valutazione degli scenari può aiutarti a garantire che lo scenario sia configurato nel modo che segue le best practice. Controlla lo scenario e fornisce consigli per la sua struttura e organizzazione.

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

## Eseguire l’esperto di punteggio scenario

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
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

  Per istruzioni, vedere [Filtri sottoscrizioni eventi nel modulo  [!DNL Workfront] > [!UICONTROL Watch Events]](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
