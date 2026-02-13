---
title: Modulo Adobe App Builder
description: Il connettore App Builder di Adobe consente di utilizzare funzioni personalizzate negli scenari.
author: Becky
feature: Workfront Fusion
source-git-commit: 8250d4fdad8ed7ffe63cd003f6e0cb325cbbfa8d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 31%

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

## Modulo Adobe App Builder

L’unico modulo di Adobe App Builder attualmente disponibile è Esegui un’azione, che consente di utilizzare una funzione di JavaScript personalizzata configurata in precedenza.

Per istruzioni sulla configurazione di una funzione personalizzata, vedere [Mappare i dati utilizzando le funzioni personalizzate](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

### Eseguire un’azione

Questo modulo esegue una funzione personalizzata configurata in precedenza.

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


