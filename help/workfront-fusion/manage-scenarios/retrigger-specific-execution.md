---
title: Riattivare l’esecuzione di uno scenario specifico
description: Puoi riattivare l’esecuzione di uno scenario specifico per elaborare i dati utilizzando una blueprint di scenario aggiornata o per visualizzarne il flusso di dati.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 0c732add9c1ec75d7aed43bb7097bb1c95aa6408
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 18%

---

# Riattivare l’esecuzione di uno scenario specifico

Puoi riattivare l’esecuzione di uno scenario specifico per elaborare i dati utilizzando una blueprint di scenario aggiornata o per visualizzarne il flusso di dati. Quando riattivi un’esecuzione, lo scenario viene eseguito utilizzando i dati di tale esecuzione.

Ad esempio, se aggiorni uno scenario per aggiungere un’azione, ad esempio la creazione di un problema, puoi riattivare un’esecuzione che si è verificata prima dell’aggiornamento. Lo scenario aggiornato verrà eseguito utilizzando l’evento di attivazione dello scenario originale, ma includerà l’azione aggiornata. In questo esempio, lo scenario crea un problema come parte della nuova esecuzione.

Il riavvio è disponibile per gli scenari che dispongono di trigger del webhook e per gli scenari figlio.

Quando si riattiva uno scenario che utilizza un webhook, è possibile utilizzare di nuovo l’evento webhook originale, pertanto non è necessario ricreare l’evento per riattivare lo scenario.

Quando si utilizzano scenari concatenati, il riavvio può essere applicato anche a uno scenario figlio. Lo scenario figlio può essere riattivato utilizzando i dati inviati dallo scenario padre nell’esecuzione originale, senza riattivare lo scenario padre.

Per ulteriori informazioni, consulta [Trigger istantanei (webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md).

Per ulteriori informazioni sugli scenari di concatenamento, vedere [Creare concatenamenti di più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

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

## Riattivazione di un’esecuzione

È possibile riattivare l&#39;esecuzione di uno scenario dalla pagina Diagramma dello scenario, dall&#39;area Cronologia dello scenario o dalla pagina dell&#39;esecuzione dello scenario specifico.

### Attivare un’esecuzione dal diagramma di scenario

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario che ha eseguito l’esecuzione da riattivare.

   Viene visualizzato il diagramma dello scenario.
1. Individua l’esecuzione da riattivare nell’elenco Esecuzioni sul lato destro della pagina.
1. Fai clic su **Riattiva** per lo scenario.

![Riavvio dal diagramma](assets/retrigger-from-diagram.png)

### Attivare un’esecuzione dalla cronologia dello scenario

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario che ha eseguito l’esecuzione da riattivare.

   Viene visualizzato il diagramma dello scenario.

1. Fai clic sulla scheda **Cronologia** sotto il nome dello scenario.
1. Individua l’esecuzione da riattivare. Se necessario, è possibile utilizzare la ricerca full-text.
1. Fai clic su **Riattiva** per lo scenario.

![Riavvio dalla cronologia](assets/retrigger-from-history.png)

### Riattivare uno scenario dalla pagina di esecuzione dello scenario

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario che ha eseguito l’esecuzione da riattivare.

   Viene visualizzato il diagramma dello scenario.
1. Individua l’esecuzione da riattivare nell’elenco Esecuzioni sul lato destro della pagina.
1. Fai clic sull’esecuzione per aprirla.
1. Nella pagina di esecuzione, fare clic su **Trigger**.


![Riavvio dall&#39;esecuzione](assets/retrigger-from-execution.png)






