---
title: coda di k
description: Molti servizi forniscono webhook per inviare notifiche istantanee ogni volta che si verifica una certa modifica nel servizio. I trigger istantanei, noti anche come webhook, possono utilizzare questi eventi per iniziare gli scenari. Gli eventi entrano nella coda del webhook mentre sono in attesa di elaborazione, ad esempio quando lo scenario è già in esecuzione. Puoi visualizzare la coda del webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---

# Visualizzare la coda di un webhook

Molti servizi forniscono webhook per inviare notifiche istantanee ogni volta che si verifica una certa modifica nel servizio. I trigger istantanei, noti anche come webhook, possono utilizzare questi eventi per iniziare gli scenari. Gli eventi entrano nella coda del webhook mentre sono in attesa di elaborazione, ad esempio quando lo scenario è già in esecuzione. Puoi visualizzare la coda del webhook.

I dati del webhook in arrivo vengono sempre memorizzati nella coda indipendentemente da come hai impostato l’opzione Dati riservati nel pannello delle impostazioni dello scenario. Dopo che i dati vengono elaborati in uno scenario, vengono eliminati definitivamente dalla coda.

Per ulteriori informazioni sui webhook, vedere [Trigger istantanei (webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visualizzare la coda di un webhook

Tutti i messaggi provenienti dai webhook in ingresso vengono memorizzati nella coda del webhook.

Se uno scenario al momento presenta una coda, in tale scenario viene visualizzato un banner:

![Banner coda](assets/queue-banner.png)

Per visualizzare la coda di un webhook:

1. Fare clic su **[!UICONTROL Webhooks]** nel menu a sinistra.
1. Individuare il webhook per il quale si desidera visualizzare la coda.
1. Individua il numero di eventi nel pulsante Eventi ricevuti.

   ![Coda webhook](assets/webhook-queue.png)

1. Fai clic sul pulsante per visualizzare i dettagli sugli eventi in coda.
