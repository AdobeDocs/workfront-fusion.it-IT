---
title: Aggiungi un prompt di IA al tuo scenario
description: Puoi includere un prompt di IA nello scenario che si connette al tuo
author: Becky
feature: Workfront Fusion
source-git-commit: 09e8ca28c12990a699816671d07f85288d973bc7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Aggiungi un prompt di IA allo scenario

È possibile includere un prompt di IA nello scenario utilizzando il protocollo MCP (Model Context Protocol) combinato con i modelli di linguaggio di grandi dimensioni (LLM, Large Language Model). Configurandoli nel modulo dell’agente MCP, puoi usare l’intelligenza artificiale per impostare flussi di lavoro efficienti, sicuri e flessibili.

>[!NOTE]
>
>Questa funzionalità è distinta dalla possibilità di aggiungere moduli a uno scenario utilizzando l’intelligenza artificiale.
>
>Per informazioni sull&#39;aggiunta di moduli con IA, vedere [Generare un segmento di scenario utilizzando IA](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md).

## Panoramica di Model Context Protocol

Model Context Protocol (MCP) è un modo per collegare in modo sicuro i modelli di linguaggio AI con altre applicazioni. Puoi configurare i server MCP, che consentono al modello di intelligenza artificiale di accedere all’applicazione. È quindi possibile inviare un messaggio di richiesta al modello di IA, che può restituire informazioni dall&#39;applicazione.

Ad esempio, puoi configurare un server MCP per collegare un modello di IA con Gmail. Quando invii il prompt &quot;Dammi le mie ultime 5 e-mail da Gmail&quot; al modello in lingua di grandi dimensioni, il prompt viene analizzato e inviato al server MPC di Gmail, che può quindi accedere a Gmail e restituire le e-mail.

Il modulo dell’agente MCP ti consente di elaborare un prompt utente utilizzando un modello di linguaggio e server MCP.

## Vantaggi dell&#39;utilizzo di MCP negli scenari Fusion

L’utilizzo di MCP negli scenari offre i seguenti vantaggi:

* L’utilizzo di MCP nello scenario riduce la necessità di riflettere in tutte le situazioni e sulle possibili varianti di un’azione. Utilizzando un prompt, elimina la necessità di utilizzare dati regex o di analisi per tenere conto di queste varianti.
* Potete fornire contesto al prompt utilizzando gli elementi mappati dai moduli precedenti o altre funzioni nel pannello di mappatura.
* L’utilizzo di un prompt può essere più efficiente e flessibile rispetto alla creazione di uno scenario con moduli specifici, perché può utilizzare il ragionamento al prompt e selezionare la migliore linea di azione dal contesto disponibile.
* Poiché si configurano i server MCP a cui il modulo può connettersi, è possibile controllare la protezione del server e assicurarsi che sia adatta alle esigenze della propria organizzazione.

>[!NOTE]
>
>La funzionalità disponibile dipende dagli strumenti disponibili nel server MCP e non è controllata da Fusion.

## Aggiungi un prompt di IA allo scenario

Puoi aggiungere un prompt di IA allo scenario utilizzando il modulo dell’agente MCP.

Per istruzioni, vedere [Modulo agente MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).
