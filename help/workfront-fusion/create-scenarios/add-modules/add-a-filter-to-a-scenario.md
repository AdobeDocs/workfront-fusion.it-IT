---
title: Aggiungere un filtro a uno scenario
description: In alcuni scenari, devi lavorare solo con bundle che soddisfano criteri specifici. I filtri ti consentono di selezionare tali bundle.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 17%

---

# Aggiungere un filtro a uno scenario

In alcuni scenari, devi lavorare solo con bundle che soddisfano criteri specifici. I filtri ti consentono di selezionare tali bundle.

Ad esempio, puoi creare uno scenario con il trigger [!UICONTROL Record di controllo] affinché Workfront acquisisca solo le attività assegnate a un utente specifico.

Puoi aggiungere un filtro tra due moduli e verificare se i bundle ricevuti dai moduli precedenti soddisfano specifiche condizioni del filtro:

* In caso affermativo, i bundle passano al modulo successivo nello scenario.
* In caso contrario, l’elaborazione dei bundle termina.

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

## Prerequisiti

È necessario aggiungere entrambi i moduli a uno scenario prima di poter aggiungere un filtro tra di essi.

## Aggiungi un filtro tra due moduli:

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un filtro.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic sull&#39;icona chiave inglese ![icona chiave inglese](assets/wrench-icon.png) tra i moduli in cui desideri aggiungere un filtro e seleziona **Configura filtro**.
1. Nella casella visualizzata, immettere un **[!UICONTROL Etichetta]** per il filtro.
1. Definisci il filtro **[!UICONTROL Condizione]**.

   Immettere il campo in base al quale si desidera filtrare nel primo campo, l&#39;operatore e, se necessario, il valore con cui si desidera confrontare il campo.

   >[!TIP]
   >
   >Puoi immettere valori nei campi filtro dal pannello di mappatura
   >Per ulteriori informazioni sulla mappatura, vedere [Mappare le informazioni da un modulo all&#39;altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Se ad esempio si desidera che il filtro passi i file in Adobe Workfront che terminano con XML, immettere **[!UICONTROL Nome file]** nella prima casella e .**[!UICONTROL xml]** nella seconda casella. Nel menu a discesa tra di essi, selezionare **[!UICONTROL Termina con (senza distinzione maiuscole/minuscole)]**. Questo filtro si applica ai bundle in arrivo dal primo modulo (Workfront). Solo i bundle contenenti file XML vengono trasferiti al modulo successivo.

   ![Configura un filtro](assets/set-up-filter-box.png)

1. Fai clic su **[!DNL OK]**.

## Copiare un filtro

Attualmente, l’editor dello scenario include una funzione per copiare un filtro.

>[!NOTE]
>
>Se copi i moduli su entrambi i lati del filtro, viene copiato anche il filtro.
>
>Per ulteriori informazioni sulla copia dei moduli, vedere [Copiare moduli o scenari in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Per copiare un filtro senza copiare i moduli, potete utilizzare Fusion DevTool

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un filtro.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Aprire Fusion DevTool facendo clic sull&#39;icona DevTool ![icona DevTool](assets/debugger-icon.png) nella parte inferiore dello schermo.

   Se l&#39;icona DevTool non è visibile, vedere [Eseguire il debug di uno scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) per istruzioni sull&#39;apertura di DevTool.

1. Fai clic sull&#39;icona **[!UICONTROL Strumenti]** ![Strumenti di sviluppo](assets/devtools-tools-icon.png) nella barra laterale sinistra.

1. Fai clic su **[!UICONTROL Copia filtro]**, quindi configura lo strumento **[!UICONTROL Copia filtro]** nel pannello a destra:

   1. Imposta il **[!UICONTROL modulo Source]** come modulo direttamente dopo il filtro che desideri copiare.
   1. Imposta il **[!UICONTROL modulo di destinazione]** come modulo dopo il quale vuoi inserire il filtro.

1. Fare clic su **[!UICONTROL Esegui]**.
