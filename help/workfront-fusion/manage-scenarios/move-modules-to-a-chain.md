---
title: Spostare i moduli in una catena
description: È possibile selezionare un gruppo di moduli in uno scenario e spostarli in un nuovo scenario concatenato, senza ricreare manualmente mappature o strutture di dati.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# Spostare i moduli in una catena

>[!IMPORTANT]
>
>Questa funzione è disponibile in Beta e non è consigliata per flussi di lavoro di produzione mission-critical. In quanto funzione di Beta, il comportamento può cambiare e i casi limite potrebbero non essere gestiti completamente.

È possibile selezionare un gruppo di moduli in uno scenario e spostarli in un nuovo scenario concatenato, senza ricreare manualmente mappature o strutture di dati. Questo consente di modulare facilmente scenari di grandi dimensioni.

Quando si sposta un gruppo di moduli in una catena, Workfront Fusion:

* Sposta i moduli selezionati in uno scenario appena creato.
* Apre il nuovo scenario in una finestra del browser separata.
* Sostituisce i moduli selezionati nello scenario originale con un modulo Catena > Chiama uno scenario figlio.
* Crea automaticamente le strutture di dati di input e output necessarie per il nuovo scenario figlio.
* Mantiene il comportamento dello scenario esistente, pertanto lo scenario continua a essere eseguito come prima dello spostamento dei moduli.
* Aggiorna automaticamente le mappature:
  * I moduli spostati nello scenario figlio ricevono i dati tramite Catena > Ricevi dati dagli input del modulo padre.
  * Gli output dello scenario figlio vengono automaticamente esposti allo scenario padre.
  * Le mappature esistenti nella blueprint vengono regolate in modo da corrispondere alla nuova struttura.

Per informazioni sulla pianificazione di scenari concatenati, vedere [Creare concatenamenti di più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Per istruzioni sulla configurazione dei moduli Chain, vedere [Moduli Chain](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

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

I moduli che desideri spostare in una catena devono già esistere in uno scenario ed è necessario selezionare più di un modulo.

## Limitazioni

Non è possibile spostare una selezione di moduli in una catena nelle situazioni seguenti:

* I moduli selezionati non fanno parte di un singolo flusso ininterrotto. Ad esempio, non è possibile selezionare moduli da due route diverse e non collegate contemporaneamente.
* La selezione include un modulo webhook.
* La selezione include un altro modulo Catena.
* La selezione include un modulo Router e non sono state selezionate tutte le route del router.
* Un modulo selezionato presenta una route del gestore degli errori e non è stata selezionata tale route.

## Spostare i moduli in una catena

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario contenente i moduli che si desidera spostare.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Selezionare i moduli da spostare in una catena tenendo premuto [!UICONTROL Maiusc] e facendo clic sui moduli che si desidera spostare.
1. Fare clic con il pulsante destro del mouse su uno dei moduli selezionati.
1. Selezionare **[!UICONTROL Sposta nella catena]**.
