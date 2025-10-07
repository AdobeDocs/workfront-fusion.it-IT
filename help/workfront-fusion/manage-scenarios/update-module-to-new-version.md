---
title: Aggiornare un modulo a una nuova versione
description: Poiché le applicazioni a cui Workfront Fusion si connette possono aggiornare o rilasciare una nuova versione, è talvolta necessario che Fusion rilasci moduli aggiornati per tali applicazioni.
author: Becky
feature: Workfront Fusion
exl-id: b7f07fa5-9d81-48b3-b0ce-7a18b3b44508
source-git-commit: d0d9d7cdad993ecceaa0abf0ac69e9a9abd78b69
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%

---

# Aggiornare un modulo a una nuova versione

Poiché le applicazioni a cui Workfront Fusion si connette possono aggiornare o rilasciare una nuova versione, è talvolta necessario che Fusion rilasci moduli aggiornati per tali applicazioni.

Se in uno scenario viene visualizzata l&#39;icona verde del modulo Aggiornamento, Workfront Fusion ha rilasciato una nuova versione di tale modulo.

![Icona aggiornamento](assets/update-indicator-workfront.png)

Puoi aggiornare il modulo senza creare un nuovo scenario.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Aggiornare un modulo Workfront a una nuova versione

1. Fai clic sull&#39;icona **Aggiorna modulo** ![Icona Aggiorna](assets/upgrade-icon.png) nel modulo che desideri aggiornare a una nuova versione.
   ![Icona aggiornamento](assets/update-indicator-workfront.png)
1. Scegliere una delle opzioni seguenti:

   * Per selezionare un nuovo modulo da sostituire (anziché aggiornare il modulo), fare clic su **Scegli nuovo**, quindi procedere come descritto in [Aggiornare un modulo non Workfront a una nuova versione](#upgrade-a-non-workfront-module-to-a-new-version).
   * Per aggiornare solo questo modulo, mantenendo la configurazione del modulo, fai clic su **Aggiorna**.
   * Per aggiornare tutti i moduli Workfront nello scenario, fare clic su **Aggiorna tutti**.

1. Salva lo scenario.

>[!NOTE]
>
>Se hai aggiornato i moduli Workfront, ti consigliamo di aprirli e di controllare la configurazione del modulo.

## Aggiornare un modulo non Workfront a una nuova versione

1. Fai clic sull&#39;icona **Aggiorna modulo** ![Icona Aggiorna](assets/upgrade-icon.png) nel modulo che desideri aggiornare a una nuova versione.
   ![Icona aggiornamento](assets/update-indicator.png)
1. Fare clic su **Scegli nuovo**.
1. Selezionare il modulo che si desidera sostituire al modulo precedente.
1. Configura il modulo con le stesse impostazioni del modulo esistente.
1. Connetti il nuovo modulo allo scenario nello stesso punto del modulo esistente.
1. Elimina il modulo precedente.
1. Salva lo scenario.
