---
title: coda di k
description: Molti servizi forniscono webhook per inviare notifiche istantanee ogni volta che si verifica una certa modifica nel servizio. I trigger istantanei, noti anche come webhook, possono utilizzare questi eventi per iniziare gli scenari. Gli eventi entrano nella coda del webhook mentre sono in attesa di elaborazione, ad esempio quando lo scenario è già in esecuzione. Puoi visualizzare la coda del webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 1c28e4007e3e9d6503618482002e506f9393ee57
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 16%
---
# Visualizzare la coda di un webhook

Molti servizi forniscono webhook per inviare notifiche istantanee ogni volta che si verifica una certa modifica nel servizio. I trigger istantanei, noti anche come webhook, possono utilizzare questi eventi per iniziare gli scenari. Gli eventi entrano nella coda del webhook mentre sono in attesa di elaborazione, ad esempio quando lo scenario è già in esecuzione. Puoi visualizzare la coda del webhook.

I dati del webhook in arrivo vengono sempre memorizzati nella coda indipendentemente da come hai impostato l’opzione Dati riservati nel pannello delle impostazioni dello scenario. Dopo che i dati vengono elaborati in uno scenario, vengono eliminati definitivamente dalla coda.

Per ulteriori informazioni, consulta [Trigger istantanei (webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Visualizzare la coda di un webhook

Tutti i messaggi provenienti dai webhook in ingresso vengono memorizzati nella coda del webhook.

Se uno scenario al momento presenta una coda, in tale scenario viene visualizzato un banner:

![Banner coda](assets/queue-banner.png)

La pagina della coda del webhook ha lo stesso layout degli elenchi **[!UICONTROL Scenari]** e **[!UICONTROL Webhook]**.

>[!NOTE]
>
>La ricerca e l’ordinamento si applicano solo agli eventi attualmente caricati nella tabella, non all’intera coda. Per includere altri eventi, carica prima gli eventi aggiuntivi.

Per visualizzare e gestire la coda di un webhook:

1. Fai clic su **[!UICONTROL Webhook]** nel menu a sinistra.
1. Individuare il webhook per il quale si desidera visualizzare la coda.
1. Individuare il numero di eventi nella colonna Coda completa.

   ![Coda webhook](assets/webhook-queue.png)

1. Fare clic sul pulsante **Operazioni** per visualizzare i dettagli sugli eventi nella coda.

   Viene visualizzata la pagina di coda del webhook. Nella pagina sono elencati gli eventi nella coda in una tabella con le colonne seguenti: **[!UICONTROL ID]**, **[!UICONTROL Creato alle]**, **[!UICONTROL Dimensione]** e **[!UICONTROL Dettagli]**.

1. (Facoltativo) Per filtrare gli eventi nella tabella, immettere il testo nel campo **[!UICONTROL Ricerca]** sopra la tabella.
1. (Facoltativo) Per ordinare gli eventi, fai clic sull&#39;intestazione della colonna **[!UICONTROL ID]**, **[!UICONTROL Creato alle]** o **[!UICONTROL Dimensione]**.
1. (Facoltativo) Per modificare il numero di eventi visualizzati in ogni pagina, selezionare un numero nell&#39;elenco a discesa **[!UICONTROL Mostra]** nella parte inferiore della pagina.
1. (Facoltativo) Per spostarsi tra le pagine degli eventi, fai clic su **[!UICONTROL Primo]**, **[!UICONTROL Precedente]**, **[!UICONTROL Successivo]** o **[!UICONTROL Ultimo]** nella parte inferiore della pagina.

   Questi pulsanti non sono disponibili quando la coda dispone di una sola pagina di eventi.

1. (Facoltativo) Per visualizzare il payload di un evento, fai clic su **[!UICONTROL Dettagli]** nella riga dell&#39;evento.

   Viene visualizzata la finestra di dialogo dei dettagli con il payload dell’evento.

1. (Facoltativo) Per eliminare gli eventi:

   1. Selezionare gli eventi che si desidera eliminare eseguendo una delle operazioni seguenti:

      * Seleziona la casella di controllo accanto a ogni evento che desideri selezionare.
      * Selezionare la casella di controllo **[!UICONTROL Seleziona tutto]** per selezionare l&#39;intera coda, non solo gli eventi attualmente caricati. È quindi possibile deselezionare la casella di controllo per tutti gli eventi che si desidera escludere dalla selezione.

   1. Nella barra nella parte inferiore della schermata, fai clic su **Elimina**.
