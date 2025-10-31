---
content-type: reference
title: Pianificare uno scenario
description: Per impostazione predefinita, uno scenario viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza viene eseguito uno scenario attivato. È possibile pianificare l'esecuzione di scenari di fusione ogni 5 minuti.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# Pianificare uno scenario

Per impostazione predefinita, uno scenario viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza viene eseguito uno scenario attivato. È possibile pianificare l&#39;esecuzione di scenari di fusione ogni 5 minuti.

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

## Pianificare uno scenario

1. Fai clic sulla scheda **Scenario** nel pannello a sinistra.
1. Seleziona lo scenario da pianificare.
1. Nell&#39;angolo superiore destro della pagina dei dettagli Scenario, fare clic su **[!UICONTROL Opzioni]** > **[!UICONTROL Pianificazione]**

   Oppure

   Fai clic sull&#39;icona **[!UICONTROL Pianificazione]** (orologio) nel modulo di attivazione dello scenario.

1. Immettere le informazioni nei campi seguenti:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Seleziona la frequenza con cui desideri eseguire lo scenario, quindi seleziona l’intervallo.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL A intervalli regolari]</strong> </p> <p>Immetti il numero di minuti tra le esecuzioni. Il valore predefinito è 15 minuti.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Inserire la data e l'ora in cui si desidera eseguire lo scenario. Utilizza il formato <code>MM/DD/YYYY h:mm A</code>. Esempio: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Ogni giorno]</strong> </p> <p>Immettere l'ora in cui si desidera eseguire lo scenario. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Giorni della settimana]</strong> </p> <p>Giorni: selezionare i giorni della settimana in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Giorni del mese]</strong> </p> <p>Giorni: selezionare i giorni del mese in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Date specificate]</strong> </p> <p>Mesi: selezionare i mesi in cui eseguire lo scenario. Puoi selezionare uno o più mesi.</p> <p>Giorni: selezionare i giorni del mese in cui si desidera eseguire lo scenario. Puoi selezionare uno o più giorni.</p> <p>Tempo: inserire l'ora in cui si desidera eseguire lo scenario nei giorni selezionati. Utilizza il formato <code>h:mm A</code>. Esempio: <code>11:00 PM</code></p> </li> 
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
      <td role="rowheader">[!UICONTROL Fine]</td> 
      <td>Inserire la data e l'ora prima delle quali si desidera eseguire lo scenario. Utilizza il formato <code>MM/DD/YYYY h:mm A</code>. Esempio: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fare clic su **[!UICONTROL OK]** per salvare le impostazioni della pianificazione e tornare allo scenario.
