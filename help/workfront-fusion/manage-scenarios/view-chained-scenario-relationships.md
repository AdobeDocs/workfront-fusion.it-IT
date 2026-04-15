---
title: Visualizzare le relazioni tra scenari concatenati
description: È possibile creare una mappa delle relazioni tra gli scenari padre e figlio.
author: Becky
feature: Workfront Fusion
source-git-commit: e7b12ec51474440990cc28996bc70fd97688b082
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 20%

---

# Visualizzare e gestire le relazioni tra scenari concatenati

È possibile creare una mappa delle relazioni tra gli scenari padre e figlio. Puoi anche utilizzare la mappa per passare a diversi scenari della catena.

Per ulteriori informazioni sugli scenari concatenati, vedere [Incatenare più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Per informazioni sulla configurazione di scenari concatenati, vedere [Moduli concatenati](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)

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

## Visualizzare una mappa delle relazioni concatenate

È possibile visualizzare una mappa dello scenario corrente e dei relativi scenari padre o figlio. La mappa mostra un diagramma del flusso di dati in tutti gli scenari concatenati.

![Relazioni tra scenari concatenati](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

Per visualizzare la mappa delle relazioni per uno scenario concatenato:

1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic sulla scheda **Relazioni**.

   ![Scheda Relazioni](assets/relations-tab.png)

1. Per informazioni generali su ogni scenario concatenato, controlla i tag.

   Ogni scenario ha uno o più dei seguenti tag:

   * Radice: lo scenario è l&#39;inizio della catena e non ha uno scenario padre.
   * Elemento padre: lo scenario è di tipo padre.
   * Figlio: lo scenario è figlio. Uno scenario può essere sia padre che figlio.
   * Corrente: questo è lo scenario attualmente visualizzato dall’utente. In altre parole, questo è lo scenario da cui l’utente ha aperto la mappa delle relazioni.

   ![Tag scenario nella mappa relazioni](assets/chained-scenario-maps-tag.png)
1. (Facoltativo) Per visualizzare un piccolo diagramma di uno scenario, passa il cursore del mouse sullo scenario.
1. (Facoltativo) per passare direttamente a un altro scenario dalla mappa, fai clic sullo scenario.

   Lo scenario su cui è stato fatto clic si apre in un’altra finestra.
1. (Facoltativo) Per passare dalla visualizzazione orizzontale a quella verticale della mappa, fare clic su **Orizzontale** o **Verticale** nella parte superiore destra della pagina Dettagli scenario.
1. (Facoltativo) Per visualizzare una visualizzazione semplificata della mappa, controlla l&#39;angolo inferiore destro della pagina.

   Questo può essere utile se la mappa della catena è grande o complessa.

   * Se visualizzi solo una parte della mappa, questa è più scura sulla mappa semplificata.
   * Lo scenario corrente è contrassegnato in blu sulla mappa semplificata.


