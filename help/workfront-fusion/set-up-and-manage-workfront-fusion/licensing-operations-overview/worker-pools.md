---
title: Pool di lavoro
description: Un pool di lavoratori è una quantità di risorse di elaborazione Workfront Fusion dedicate a una o più organizzazioni specifiche. Tutte le operazioni e le elaborazioni di Fusion vengono eseguite nel contesto del pool di lavoratori assegnato a un'organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# Pool di lavoro

Un pool di lavoratori è una quantità di risorse di elaborazione Workfront Fusion dedicate a un&#39;organizzazione specifica. Tutte le operazioni e le elaborazioni di Fusion vengono eseguite nel contesto del pool di lavoratori assegnato a un&#39;organizzazione.

I pool di lavoro consentono un&#39;esecuzione più efficiente degli scenari ed eliminano le possibilità di competere con altre organizzazioni per la capacità di elaborazione Fusion.

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Panoramica del pool di lavoro

Un pool di lavoro è un modo per elaborare le esecuzioni degli scenari in parallelo. Ogni pool di lavoratori è associato a:

* Un certo numero di lavoratori.
* Una coda di esecuzione.

Quando viene eseguito uno scenario, questo passa nella coda di esecuzione del pool di lavoro. I processi di lavoro nel pool estraggono continuamente le attività dal pool di esecuzione ed elaborarle in parallelo.

Se la profondità della coda di esecuzione aumenta e tutti i processi di lavoro esistenti vengono utilizzati, Workfront Fusion ridimensiona automaticamente il pool aggiungendo altri processi di lavoro. Questa scalabilità è dinamica e guidata dagli eventi, il che significa che la capacità esatta o si contrae in base al carico in tempo reale senza l’azione dell’azienda.

Il team di Workfront Fusion monitora costantemente l&#39;utilizzo e il comportamento di scalabilità dei pool e può esaminare soglie o modelli per garantire prestazioni coerenti in base alla crescita dell&#39;utilizzo.

## Rinominare un pool di lavoro

I proprietari e gli amministratori dell&#39;organizzazione possono rinominare i pool di lavoratori assegnati alla propria organizzazione. Per impostazione predefinita, ogni pool mostra un nome generato dal sistema. È possibile assegnare a un pool un nome personalizzato, ad esempio `Marketing EU` o `High-volume integrations`, e modificarlo quando necessario.

La ridenominazione di un pool cambia solo il modo in cui viene etichettato. Gli scenari, le esecuzioni e la capacità del pool non sono interessati. Il nuovo nome viene visualizzato ovunque venga visualizzato il pool, ad esempio quando si assegnano scenari a un pool.

>[!NOTE]
>
>La scheda **[!UICONTROL Pool di lavoro]** viene visualizzata solo quando all&#39;organizzazione sono assegnati più pool di lavoro. Se la tua organizzazione dispone di un singolo pool di lavoro o utilizza il pool condiviso, la scheda non viene visualizzata.

Per rinominare un pool di lavoratori:

1. Nel menu di navigazione a sinistra, fai clic su **Panoramica organizzazione**
1. Fare clic sulla scheda **[!UICONTROL Pool di lavoro]**, nella parte superiore della pagina.

   La scheda elenca ogni pool e mostra il numero di scenari ad esso assegnati.

1. Fare clic su **[!UICONTROL Rinomina]** accanto al pool che si desidera rinominare.
1. Nel pannello visualizzato, immetti il nuovo nome.
1. Fai clic su **Salva**.
