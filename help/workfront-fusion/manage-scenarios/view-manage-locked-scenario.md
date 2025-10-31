---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gestisci scenari bloccati
description: Gestire gli scenari bloccati in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Gestisci scenari bloccati

In alcuni casi, uno scenario potrebbe essere temporaneamente bloccato in Workfront Fusion. Gli scenari bloccati verranno sbloccati automaticamente entro 2-4 ore. Puoi sbloccare gli scenari manualmente, ma in genere non è consigliato.

Gli scenari possono essere bloccati per una serie di motivi:

* Workfront Fusion non supporta l’elaborazione parallela di scenari pianificati. Questi scenari vengono bloccati all’inizio dell’esecuzione dello scenario e sbloccati al suo completamento. Se l’esecuzione viene interrotta, lo scenario potrebbe non sbloccarsi. Ciò può verificarsi quando un utente forza manualmente lo scenario o quando si verifica un problema di sistema.

* Il team di progettazione di Workfront Fusion può bloccare uno scenario perché causa problemi di prestazioni o di altro tipo.

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

## Sblocca uno scenario bloccato

Gli scenari bloccati si sbloccheranno tra 2 e 4 ore dal momento in cui sono stati bloccati. È possibile sbloccare manualmente uno scenario prima che venga pianificato lo sblocco automatico.

>[!WARNING]
>
>Lo sblocco manuale di uno scenario può causare errori nelle esecuzioni di uno scenario. È consigliabile sbloccare manualmente gli scenari solo quando uno scenario è bloccato a causa dell’esecuzione e dell’arresto delle esecuzioni come parte della progettazione dello scenario. In altre circostanze, si consiglia di attendere che lo scenario venga sbloccato automaticamente.


Per sbloccare manualmente uno scenario bloccato:

1. Vai alla pagina dei dettagli dello scenario bloccato.
1. Fai clic su **[!UICONTROL Opzioni]** nell&#39;angolo superiore destro dello schermo.
1. Selezionare **[!UICONTROL Sblocca esecuzione]**.
1. Fai clic su **[!UICONTROL Sblocca]**.
   ![Sblocca scenario](assets/unlock-scenario.png)
