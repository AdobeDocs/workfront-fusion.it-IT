---
title: Utilizza Live Trail per rivedere l’esecuzione di uno scenario
description: Live Trail mostra uno scenario eseguito nel modo in cui si verifica, combinando le richieste del modulo ed eseguendo l’attività in un elenco. Puoi aprire i dettagli della richiesta e della risposta per qualsiasi operazione.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# Utilizza Live Trail per rivedere l’esecuzione di uno scenario

Live Trail mostra uno scenario eseguito mentre si verifica. Combina le richieste dei moduli e l’attività di esecuzione in un elenco cronologico, in modo da poter seguire un’esecuzione nell’editor di scenari e vedere cosa è andato storto senza uscire dall’area di lavoro.

>[!NOTE]
>
>Questa funzionalità è disponibile solo nella nuova esperienza dell’editor di scenari. Per ulteriori informazioni, consulta [Esperienze nuove e classiche](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) nell&#39;articolo Editor scenari.

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

## Apri Live Trail

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario da rivedere.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Avviare un&#39;esecuzione dello scenario, ad esempio facendo clic su **Esegui una volta**.



Live Trail si apre nel pannello sul lato destro dell’area di lavoro. Se chiudi il pannello durante un’esecuzione, una piccola scheda a destra dello schermo ti consente di aprirlo nuovamente senza perdere gli eventi acquisiti.

## Rivedi gli eventi in Live Trail

Live Trail elenca le richieste del modulo ed esegue l’attività nell’ordine in cui si verificano. Puoi eseguire le seguenti operazioni:

* Cerca nell&#39;elenco.
* Filtra l’elenco per stato.
* Segui l’evento più recente mentre l’esecuzione continua.
* Cancella la traccia corrente.

## Visualizza dettagli di richieste e risposte

1. In Live Trail, fai clic sulla richiesta per la quale desideri visualizzare i dettagli.

   Il modulo che ha effettuato la richiesta viene mostrato nell’area di lavoro e i dettagli della richiesta e della risposta vengono aperti nel pannello.

1. Rivedi i dettagli. La visualizzazione dei dettagli include:

   * Navigazione tra le operazioni del modulo
   * Intestazioni e corpo della richiesta
   * Intestazioni e corpo della risposta

1. (Facoltativo) Copiare i dettagli per utilizzarli altrove facendo clic su **Copia raw** o **Copia cURL**:

   * Copia un rapporto non elaborato della richiesta e della risposta.
   * Copia un comando cURL per la richiesta.

1. Per tornare all’elenco, fai clic sulla freccia indietro in alto a sinistra nel pannello.

## Assicurati che i dettagli della richiesta e della risposta siano disponibili

I dettagli di richieste e risposte non vengono conservati per ogni esecuzione pianificata o attivata, perché richiedono molto spazio di archiviazione.

* Esegui una volta conserva sempre i dettagli delle richieste e delle risposte.
* Per le esecuzioni regolari di uno scenario, attiva i registri di debug temporanei nelle impostazioni dello scenario prima delle esecuzioni che desideri verificare. Per ulteriori informazioni, vedere [Log di debug temporanei](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) nell&#39;articolo Configurare le impostazioni dello scenario.

Se apri un’esecuzione dalla cronologia di esecuzione e il pannello di richiesta e risposta non contiene dati, il pannello indirizza all’impostazione dei registri di debug temporanei.
