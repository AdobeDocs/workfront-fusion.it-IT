---
title: Modulo Adobe App Builder
description: Il connettore App Builder di Adobe consente di utilizzare funzioni personalizzate negli scenari.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 042f32f35e630ec76a7356fa750f5238f74a6f25
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 23%

---

# Modulo Adobe App Builder

È possibile creare funzioni personalizzate nell&#39;area Funzioni di Fusion. Puoi quindi aggiungere queste funzioni agli scenari sotto forma di un modulo App Builder di Adobe.

Poiché le funzioni personalizzate funzionano tramite Adobe App Builder, la tua organizzazione deve disporre di una licenza Adobe App Builder per utilizzarle.

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
   <p><ul><li>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li><li>Per utilizzare le funzioni personalizzate è necessario disporre di una licenza Adobe App Builder.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Moduli di Adobe App Builder

<!--

### Run a custom code block

This module allows you to run a code block. You configure the code block when you set up the module, and it is run when the module runs during a scenario execution.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Enter the block of code that you want the module to run.<p>To format the code for easier reading, click the <b>Format code</b> icon.</td> 
  </tr> 
   </tbody> 
</table>

-->

### Eseguire una funzione personalizzata dal pacchetto

Questo modulo esegue una funzione da un pacchetto.

<!--For information on packages, see []().-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Selezionare il pacchetto che include la funzione da eseguire nello scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Selezionare la funzione da eseguire nello scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Usa variabile da pacchetto

Questo modulo porta nello scenario una variabile configurata in un pacchetto.

<!--For information on packages, see []().-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Seleziona il pacchetto che include la variabile da inserire nello scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Seleziona la variabile da inserire nello scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Eseguire una funzione personalizzata o un blocco di codice

Questo modulo consente di utilizzare una funzione JavaScript personalizzata precedentemente configurata e memorizzata nell’area Funzioni.

Per istruzioni sulla configurazione di una funzione personalizzata, vedere [Mappare i dati utilizzando le funzioni personalizzate](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azione]</td> 
   <td>Selezionare la funzione personalizzata che si desidera eseguire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parameters] </td> 
   <td>Immettere i valori per i parametri della funzione. I parametri disponibili si basano sui parametri configurati al momento della creazione della funzione.<p>Se un parametro ha un valore predefinito, non lo visualizzerai nel campo, ma puoi sovrascriverlo immettendo o mappando un valore nel campo.</p></td> 
  </tr> 
   </tbody> 
</table>
