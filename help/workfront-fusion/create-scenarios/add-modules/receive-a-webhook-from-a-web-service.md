---
title: Configurare un webhook per un servizio Web senza connettore
description: Se un servizio web non dispone al momento di un connettore dedicato in Workfront Fusion, ma supporta l’invio di webhook, puoi aggiungere il servizio a uno scenario utilizzando il modulo Webhook personalizzato come attivatore immediato.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Configurare un webhook per un servizio Web senza connettore

Se un servizio web non dispone al momento di un connettore dedicato in Workfront Fusion, ma supporta l’invio di webhook, puoi aggiungere il servizio a uno scenario utilizzando il modulo Webhook personalizzato come attivatore immediato. Questo processo è denominato ricezione di un webhook e richiede una configurazione sul lato dell&#39;applicazione a cui ci si connette.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Selezionare o Prime Workfront Plan: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Ultimate Workfront: Workfront Fusion è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Ricevi un webhook

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un webhook.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Aggiungi il modulo **Webhook > Webhook personalizzato** per iniziare lo scenario.
1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Immetti un **nome webhook** nella casella visualizzata
1. Configurare il webhook (facoltativo).

   Per istruzioni, consulta [Webhook](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Fai clic su **Salva**.

1. Fai clic su **Copia indirizzo negli Appunti**, quindi fai clic su **OK**.

1. Accedi al servizio web ed effettua le seguenti operazioni:

   1. Nell’area Impostazioni del servizio web, crea un webhook.

      Le istruzioni specifiche dipendono dall’applicazione. È consigliabile cercare &quot;Crea un webhook&quot; nella documentazione dell’applicazione.
   1. Incolla l&#39;indirizzo copiato negli Appunti al passaggio 3.
   1. Seleziona l’evento che attiverà il webhook.

1. Esegui lo scenario.

   Quando si verificano l’evento o gli eventi, viene attivato il modulo del webhook personalizzato e viene eseguito lo scenario.
