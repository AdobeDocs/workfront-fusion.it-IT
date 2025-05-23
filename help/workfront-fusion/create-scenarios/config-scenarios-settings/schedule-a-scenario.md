---
content-type: reference
title: Pianificare uno scenario
description: Per impostazione predefinita, uno scenario viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza viene eseguito uno scenario attivato. È possibile pianificare l'esecuzione di scenari di fusione ogni 5 minuti.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Pianificare uno scenario

Per impostazione predefinita, uno scenario viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza viene eseguito uno scenario attivato. È possibile pianificare l&#39;esecuzione di scenari di fusione ogni 5 minuti.

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
   <p>Nuovo:</p> <ul><li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] Piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Il piano [!DNL Workfront Fusion] è incluso.</li></ul>
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

## Pianificare uno scenario

1. Fai clic sulla scheda **Scenario** nel pannello a sinistra.
1. Seleziona lo scenario da pianificare.
1. Nell&#39;angolo superiore destro della pagina dei dettagli Scenario, fare clic su **[!UICONTROL Options]** > **[!UICONTROL Scheduling]**

   Oppure

   Fare clic sull&#39;icona **[!UICONTROL Scheduling]** (orologio) nel modulo di attivazione dello scenario.

1. Immettere le informazioni nei campi seguenti:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Seleziona la frequenza con cui desideri eseguire lo scenario, quindi seleziona l’intervallo.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Immetti il numero di minuti tra le esecuzioni. Il valore predefinito è 15 minuti.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Inserire la data e l'ora in cui si desidera eseguire lo scenario. Utilizza il formato <code>MM/DD/YYYY h:mm A</code>. Esempio: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Immettere l'ora in cui si desidera eseguire lo scenario. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Giorni: selezionare i giorni della settimana in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Giorni: selezionare i giorni del mese in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Mesi: selezionare i mesi in cui eseguire lo scenario. Puoi selezionare uno o più mesi.</p> <p>Giorni: selezionare i giorni del mese in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
       </ul> <p>Nota: affinché uno scenario venga eseguito in tale data, è necessario che esista una data. Ad esempio, uno scenario pianificato solo per il 31 del mese non verrà eseguito in febbraio, aprile, giugno, settembre o novembre, perché tali mesi non hanno un giorno 31.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>Puoi definire intervalli di tempo specifici durante i quali deve essere eseguito lo scenario. È possibile specificare intervalli di tempo, giorni feriali o mesi. Per ogni intervallo, fare clic su <strong>[!UICONTROL Add]</strong> e compilare i campi come descritto nel campo [!UICONTROL Run scenario].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Immettere la data e l'ora dopo la quale si desidera eseguire lo scenario. Utilizza il formato <code>MM/DD/YYYY h:mm A</code>. Esempio: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Inserire la data e l'ora prima delle quali si desidera eseguire lo scenario. Utilizza il formato <code>MM/DD/YYYY h:mm A</code>. Esempio: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fare clic su **[!UICONTROL OK]** per salvare le impostazioni di pianificazione e tornare allo scenario.
