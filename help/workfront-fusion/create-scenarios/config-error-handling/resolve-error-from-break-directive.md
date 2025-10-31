---
title: Risolvere gli errori gestiti dalla direttiva Break
description: A volte è utile rieseguire un modulo non riuscito se è possibile che il motivo dell’errore si risolva rapidamente.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Risolvere gli errori gestiti dalla direttiva Break

Quando un errore viene gestito dalla direttiva di interruzione, viene creato un record nella cartella Esecuzioni incomplete. Questo record memorizza lo stato dell’esecuzione dello scenario, insieme ai dati dei moduli precedenti. Il record fa riferimento al modulo in cui si è verificato l’errore e contiene informazioni relative ai dati ricevuti dal modulo come input. Per ogni bundle di dati che causa l’errore, viene creato un record separato.

Per ulteriori informazioni, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

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

## Risolvere gli errori derivanti dalla direttiva Break

Puoi risolvere l’errore manualmente aggiornando lo scenario (se necessario) ed eseguendolo una volta.

Puoi anche configurare lo scenario in modo da elaborare automaticamente un’esecuzione incompleta rieseguendo lo scenario. Per configurare il modulo in modo da elaborare le esecuzioni incomplete:

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera aggiungere la soluzione alternativa.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic sull&#39;icona **Controllo flusso** ![Controllo flusso](assets/flow-control-icon.png) e selezionare **Interruzione**.
1. All&#39;interno del modulo Break, abilita l&#39;opzione [!UICONTROL **Esecuzione automatica**].
1. Nel campo **Numero di tentativi**, immettere o mappare il numero massimo di tentativi che si desidera vengano ripetuti dal modulo

   Questo numero deve essere compreso tra 1 e 100.
1. Nel campo **Intervallo tra tentativi**, immettere o mappare il numero di minuti tra ogni tentativo.

Con questa opzione abilitata, quando si verifica un errore, l&#39;esecuzione incompleta viene recuperata (dopo il tempo specificato nel campo [!UICONTROL Intervallo tra tentativi]) ed eseguita con i dati di input originali. Questo verrà ripetuto fino al completamento dell’esecuzione del modulo senza errori o fino al raggiungimento del numero di tentativi specificato.

>[!NOTE]
>
>Se il tentativo iniziale di nuovo tentativo non riesce, l’intervallo tra i nuovi tentativi aumenta in modo esponenziale ogni altro tentativo.


Quando l’opzione di esecuzione Automatically complete (Completamento automatico) è abilitata, l’esecuzione dello scenario è contrassegnata come &quot;Completata&quot; perché il tentativo automatico del gestore degli errori di interruzione gestisce il problema automaticamente. In questo caso, gli utenti non ricevono un messaggio e-mail relativo all’esecuzione non riuscita.

Quando l’opzione di esecuzione Automatically complete (Completamento automatico) è disattivata, l’esecuzione viene contrassegnata come &quot;Avviso&quot;.

Esistono alcune eccezioni alle esecuzioni memorizzate in Esecuzioni incomplete e, con alcuni tipi di errore, non è possibile ritentare automaticamente l’esecuzione di uno scenario.

## Risorse

Per ulteriori informazioni, vedere [Consentire l&#39;archiviazione di esecuzioni incomplete](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) nell&#39;articolo Configurare le impostazioni dello scenario.
