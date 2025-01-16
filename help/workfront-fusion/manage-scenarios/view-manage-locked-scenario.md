---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gestisci scenari bloccati
description: Gestisci scenari bloccati in [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Gestisci scenari bloccati

In alcuni casi, uno scenario potrebbe essere temporaneamente bloccato in [!DNL Workfront Fusion]. Gli scenari bloccati verranno sbloccati automaticamente entro 2-4 ore. Puoi sbloccare gli scenari manualmente, ma in genere non è consigliato.

Gli scenari possono essere bloccati per una serie di motivi:

* Workfront Fusion non supporta l’elaborazione parallela di scenari pianificati. Questi scenari vengono bloccati all’inizio dell’esecuzione dello scenario e sbloccati al suo completamento. Se l’esecuzione viene interrotta, lo scenario potrebbe non sbloccarsi. Ciò può verificarsi quando un utente forza manualmente lo scenario o quando si verifica un problema di sistema.

* Il team di progettazione di Workfront Fusion può bloccare uno scenario perché causa problemi di prestazioni o di altro tipo.

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


## Sblocca uno scenario bloccato

Gli scenari bloccati si sbloccheranno tra 2 e 4 ore dal momento in cui sono stati bloccati. È possibile sbloccare manualmente uno scenario prima che venga pianificato lo sblocco automatico.

>[!WARNING]
>
>Lo sblocco manuale di uno scenario può causare errori nelle esecuzioni di uno scenario. È consigliabile sbloccare manualmente gli scenari solo quando uno scenario è bloccato a causa dell’esecuzione e dell’arresto delle esecuzioni come parte della progettazione dello scenario. In altre circostanze, si consiglia di attendere che lo scenario venga sbloccato automaticamente.


Per sbloccare manualmente uno scenario bloccato:

1. Vai alla pagina dei dettagli dello scenario bloccato.
1. Fare clic su **[!UICONTROL Options]** nell&#39;angolo superiore destro dello schermo.
1. Selezionare **[!UICONTROL Unlock execution]**.
1. Fare clic su **[!UICONTROL Unlock]**.
   ![](assets/unlock-scenario.png)
