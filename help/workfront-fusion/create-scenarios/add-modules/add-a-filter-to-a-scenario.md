---
title: Aggiungere un filtro a uno scenario
description: In alcuni scenari, devi lavorare solo con bundle che soddisfano criteri specifici. I filtri ti consentono di selezionare tali bundle.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: bec838423e13c3efe4f3d002f824c203cad6ecf8
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 19%

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

Puoi copiare un filtro esistente e incollarlo altrove nello scenario.

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un filtro.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic con il pulsante destro del mouse sui punti di connessione tra i moduli in cui si trova il filtro.
1. Seleziona **Copia filtro**.
1. Fai clic con il pulsante destro del mouse sui punti di connessione tra i moduli in cui desideri incollare il filtro.
1. Seleziona **Incolla filtro
1. (Facoltativo) Per modificare il filtro, fare clic sull&#39;icona o sull&#39;etichetta del filtro e immettere i valori come descritto in [Aggiungere un filtro tra due moduli](#add-a-filter-between-two-modules) in questo articolo.




<!--

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.

-->
