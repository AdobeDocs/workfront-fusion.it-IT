---
title: Chain Multiple Scenarios Together
description: You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 12%

---

# Concatenare più scenari insieme

>[!NOTE]
>
>This feature is currently in Beta.

You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first. This allows more modular scenario creation, where you do not have to duplicate scenario sections in multiple scenarios.

È possibile chiamare più scenari figlio da uno scenario padre e uno scenario figlio da più scenari padre. Puoi anche nidificare scenari secondari, effettuando una chiamata da un altro.

When a parent scenario is waiting for a child scenario to return data, that time does not count against the parent scenario&#39;s timeout. For example, a parent scenario calls 5 child scenarios, each of which takes 10 minutes to run, for a total of 50 minutes. The modules in the parent scenario itself take 15 minutes to run. The parent scenario does not time out, even though a total of 65 minutes has passed, which is over the timeout limit of 40 minutes.

For more information on Fusion&#39;s performance guardrails, including timeouts, see [Fusion performance guardrails](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

Per istruzioni sulla configurazione dei moduli Chain, vedere [Moduli Chain](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Parent and child scenarios

* The **parent** scenario calls another scenario, using the **Chain** > **Call a child scenario** module. It receives the output of the child scenario, which it can process in later scenario modules.
* The **child** scenario is called by the parent scenario. Its trigger module receives data from the parent scenario, and returns output to the parent scenario.

The parent scenario requires a response from the child scenario. Child scenarios that do not return data are currently not supported.

## Data structures in chained scenarios

Workfront Fusion uses data structures to transfer information from the parent scenario to the child scenario. The data structure is configured in the child scenario. When the child scenario is selected from the parent scenario, the fields for the data structure used as the child scenario&#39;s input appear in the parent scenario. You can map values to these fields, which are passed to the child scenario when it is triggered.

For information on the modules to configure in the parent and child scenarios, see [Chain modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

For information on data structures, see [Data structures](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Data flow

1. Data flows through the parent scenario.
1. Data reaches the Call a child scenario module. Data is mapped to the fields in the Call a child scenario module, which match the fields in the data structure used in the child scenario&#39;s trigger module.
1. Data from the Call a child scenario is passed to the child scenario.
1. The child scenario processes data and performs actions.
1. The child scenario ends with the Return response to parent module.
1. The output of the Return response to parent module is passed to the parent scenario.
1. The output of the Call a child scenario is the output of the child scenario. This output can be processed later in the parent scenario.

## Casi d’uso

Consider the following example use cases for chaining scenarios:

* **Reusable logic**:  You can chain scenario for repeated actions used across multiple scenarios. For example, if you have multiple scenarios that archive content, you can create a single child scenario called &quot;Archive content&quot; that you can then use as a child scenario for any workflows that archive content.

* **Error handling**: It&#39;s common for organizations to have the same error handling actions across multiple scenarios, such as an error handling route that sends an error log to a data store and creates a slack notification. You can create a child scenario with these actions and chain that scenario in error handling routes in multiple scenarios.

* **Extending time**: You can use chaining for large batch operations with long running actions, such as when you export and import files. This operation takes some time if there are many files. Because child scenarios do not count against the parent scenario&#39;s timeout, you can exceed execution time by using multiple child scenarios to export or import the files.

* **Replacing iterators** Replacing iterators with child scenarios can reduce memory usage, such as in complex operations in an iteration that cause Out of Memory error. You can create a separate scenario for the complex operation and replace the iterator with Call a child scenario module

* **Search for and create a record**:  For example, you could create a scenario that searches for a user. If they exist, the scehario adds them as approver with access they need to review and approve. If they don&#39;t exist, the scenario creates a request for the admin to onboard a new user.

## Visualizzazione della cronologia di esecuzione per gli scenari concatenati

È possibile visualizzare la cronologia di esecuzione per gli scenari concatenati visualizzando la cronologia di ogni scenario incluso nella catena. Ad esempio, la cronologia di esecuzione dello scenario principale includerebbe informazioni sui moduli e sui dati elaborati direttamente nello scenario principale. Per visualizzare la cronologia di esecuzione per i moduli e i dati elaborati in uno scenario figlio, aprire lo scenario figlio e visualizzare la cronologia di esecuzione.

È consigliabile utilizzare il pulsante **Vai allo scenario figlio** nel modulo Chiama uno scenario figlio per passare rapidamente allo scenario figlio, in cui è possibile visualizzarne la cronologia di esecuzione. Lo scenario figlio si apre in un&#39;altra finestra del browser, consentendo di visualizzare contemporaneamente gli scenari padre e figlio.

![Pulsante Vai allo scenario figlio](assets/go-to-the-child-button.png)

## Errori ed esecuzioni incomplete

### Gestione degli errori

Se si verifica un errore nello scenario figlio, ciò potrebbe influire sul recupero dei dati dal genitore.

È consigliabile configurare la gestione degli errori nello scenario figlio in modo che, in caso di errori nello scenario figlio, lo scenario padre non rimanga bloccato in attesa della risposta dallo scenario figlio.

## Best Practice

Quando concili uno scenario, considera le seguenti best practice.

### Evitare la ricorsione durante il concatenamento degli scenari

La ricorsione si verifica quando uno scenario attiva una nuova esecuzione di se stesso, attivando una nuova esecuzione e così via in un ciclo infinito.

La ricorsione può causare problemi di prestazioni sia per l’organizzazione proprietaria dello scenario ricorsivo che per altre organizzazioni.

Quando si concatenano scenari, seguire queste procedure per evitare ricorsioni:

* Assicurati che **scenari figlio non possano attivare lo scenario padre**. Ad esempio, se uno scenario principale viene attivato al momento della creazione di una richiesta, assicurati che gli scenari secondari non creino richieste.
* Assicurati che **scenari secondari non si chiamino tra loro**. Ad esempio, se lo scenario figlio A chiama lo scenario figlio B, assicurati che lo scenario figlio B non chiami lo scenario figlio A.
* Assicurati che **uno scenario non possa chiamare se stesso**. Ad esempio, uno scenario viene attivato quando viene creata un’attività e tale scenario crea due attività. Le attività appena create attivano nuovamente lo scenario, creando quattro nuove attività. Ogni volta che viene creata un’attività, lo scenario viene attivato e ogni volta che lo scenario viene eseguito, il numero di attività raddoppia. Il numero di attività aumenta in modo esponenziale.

>[!IMPORTANT]
>
>* **Quando uno scenario sta causando la ricorsione, viene disattivato dal team di progettazione di Fusion per evitare ulteriori problemi di prestazioni.**
>* Poiché la ricorsione è il risultato della progettazione dello scenario, è necessario progettare gli scenari in modo tale che lo scenario non includa azioni che lo attivino.
>* È possibile visualizzare un diagramma delle relazioni tra gli scenari padre e figlio.
>   Per istruzioni, vedere [Visualizzare le relazioni tra scenari concatenati](/help/workfront-fusion/manage-scenarios/view-chained-scenario-relationships.md).

### Utilizza la gestione degli errori per garantire una risposta

Poiché lo scenario padre è in attesa di una risposta dallo scenario figlio prima di continuare, è necessario assicurarsi che lo scenario figlio sia generato in modo che fornisca una risposta anche se viene rilevato un errore.
