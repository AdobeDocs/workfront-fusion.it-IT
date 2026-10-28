---
title: Trovare e sostituire variabili, origini e connessioni in uno scenario
description: Utilizza Trova e sostituisci per sostituire una variabile mappata, rimappare i riferimenti da un modulo di origine a un altro o copiare una connessione ad altri moduli nello scenario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# Trovare e sostituire variabili, origini e connessioni in uno scenario

>[!NOTE]
>
>Questa funzionalità è disponibile solo nella nuova esperienza dell’editor di scenari. Per ulteriori informazioni, consulta [Esperienze nuove e classiche](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) nell&#39;articolo Editor scenari.

Trova e sostituisci consente di apportare la stessa modifica in più moduli contemporaneamente. Puoi eseguire le seguenti operazioni:

* Sostituisci una variabile mappata in tutto lo scenario o in un modulo.
* Rimappatura dei riferimenti da un modulo di origine a un altro.
* Copia una connessione a uno o a tutti i moduli compatibili dalla stessa app.

Prima di apportare una modifica, Trova e sostituisci mostra un’anteprima dei moduli che saranno interessati.

Nell&#39;esperienza classica, è possibile utilizzare gli strumenti di connessione Scambia variabile, Ripeti origine e Scambia in DevTool per eseguire queste operazioni. Per ulteriori informazioni, vedere [Eseguire il debug di uno scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

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

## Apri Trova e sostituisci

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri apportare modifiche.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic sull&#39;icona **Trova e sostituisci** ![Trova e sostituisci](assets/find-replace-icon.png) nell&#39;area Controlli.

   Per visualizzare l&#39;icona Trova e sostituisci, potrebbe essere necessario fare clic sull&#39;icona a tre punti nell&#39;area Controlli.

Trova e sostituisci si apre nel pannello sul lato destro dell’area di lavoro.

## Sostituire una variabile

Utilizzare la scheda **Variabile** per sostituire una variabile mappata.

1. Apri Trova e sostituisci, quindi fai clic sulla scheda **Variabile**.
1. Nel campo Variabile da trovare, incolla la variabile da sostituire.
1. Nel campo Sostituisci con, incolla la variabile che sostituirà la variabile precedente.
1. Nel campo Modulo scegliere il modulo a cui applicare la modifica oppure selezionare **Intero scenario** per applicare la modifica a tutti i moduli interessati nello scenario.
1. Fai clic su **Sostituisci**
1. Rivedi l’anteprima dei moduli che saranno interessati. Per passare a un modulo nell’area di lavoro, selezionane la riga nell’anteprima.
1. Fai clic su **Applica**.

## Rimappare un&#39;origine

Utilizza la scheda **Source** per modificare il modulo a cui fanno riferimento le mappature in altri moduli.

1. Apri Trova e sostituisci, quindi fai clic sulla scheda **Source**.
1. Nel campo Modulo Source, seleziona il modulo di origine a cui si riferiscono attualmente le mappature.
1. Nei campi del modulo Target, seleziona il modulo a cui devono fare riferimento.
1. Nel campo Modulo scegliere il modulo a cui applicare la modifica oppure selezionare **Intero scenario** per applicare la modifica a tutti i moduli interessati nello scenario.
1. Fai clic su **Sostituisci**
1. Rivedi l’anteprima dei moduli che saranno interessati. Per passare a un modulo nell’area di lavoro, selezionane la riga nell’anteprima.
1. Fai clic su **Applica**.

## Copiare una connessione in altri moduli

Utilizza la scheda **Connessione** per utilizzare la stessa connessione in più moduli della stessa app.

1. Apri Trova e sostituisci, quindi fai clic sulla scheda **Connessione**.
1. Nel campo Connessione da selezionare un modulo che dispone della connessione che si desidera utilizzare per altri moduli.
1. Nel campo Applica a scegliere il modulo a cui applicare la modifica o se applicarla a tutti i moduli compatibili dello scenario.
1. Fai clic su **Applica**.
