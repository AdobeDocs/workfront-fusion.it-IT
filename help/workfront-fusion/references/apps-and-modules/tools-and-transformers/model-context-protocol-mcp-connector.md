---
title: Moduli MCP (Model Context Protocol)
description: Il modulo MCP (Model Context Protocol) consente di elaborare un prompt utente utilizzando MCP.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 97abe6bf0ff7b10a139268f02f8a1a24f3e31b47
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 18%

---

# Modulo agente MCP

<!--SET UP REDIRECTS-->

Model Context Protocol (MCP) è un modo per collegare in modo sicuro i modelli di linguaggio AI con altre applicazioni. Puoi configurare i server MCP, che consentono al modello di intelligenza artificiale di accedere all’applicazione. È quindi possibile inviare un messaggio di richiesta al modello di IA, che può restituire informazioni dall&#39;applicazione.

Ad esempio, puoi configurare un server MCP per collegare un modello di IA con Gmail. Quando invii il messaggio &quot;Dammi le mie ultime 5 e-mail da Gmail&quot;, l’utente può accedere a Gmail e restituire le e-mail.

Il modulo MCP (Model Context Protocol) consente di elaborare un prompt utente utilizzando un modello del linguaggio e server MCP.

Per ulteriori informazioni su MCP in scenari Fusion, consulta [Aggiungere un prompt di IA allo scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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

* Devi aver configurato tutti i server MCP a cui intendi connetterti.
* È necessario disporre di una chiave LLM per il modello di lingua di grandi dimensioni selezionato.

## Modulo Model Context Protocol e relativi campi

### Prompt utente processo

Questo modulo di azione elabora un prompt utilizzando il modello di linguaggio e i server MCP specificati.

>[!NOTE]
>
>Questo modulo deve restituire un oggetto. Non restituisce output come stringhe o numeri.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Chiave LLM</td> 
   <td> Selezionare una chiave LLM esistente o crearne una nuova facendo clic su <b>Aggiungi</b> e immettendo le seguenti informazioni: 
     <ul>
       <li><b>Nome chiave</b>: immettere un nome per la nuova chiave.</li>
       <li><b>LLM</b>: selezionare il modello di lingua di grandi dimensioni a cui è associata la chiave.</li>
       <li><b>Chiave</b>: immetti o mappa la chiave API per il modello selezionato.</li>
       <li><b>Modello</b>: selezionare il modello LLM utilizzato dalla chiave.</li>
       <li><b>Numero massimo di token</b>: immettere o mappare il numero massimo di token che il modulo LLM può generare nella risposta.<p>Un token equivale in genere a quattro caratteri, o 0,75 di una parola in inglese. "Hello world" equivale a due token e "Authentication" equivale a uno o due token.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Server MCP</td> 
   <td> <p>Per ogni server MCP a cui si desidera connettersi, fare clic su <b>Aggiungi</b> e immettere le informazioni seguenti: </p> 
     <ul>
       <li><b>Connessione</b>: selezionare la connessione che verrà utilizzata da Fusion per connettersi al server MCP.</li>
       <li><b>Host server MCP</b>: immettere l'URL del server MCP.</li>
       <li><b>Nome server MCP</b>: immettere o associare un nome per questo server MCP.</li>
       <li><b>Intestazioni</b>: aggiungi eventuali intestazioni applicabili.</li>
       <li><b>Tipo di server MCP</b>: selezionare il tipo di server.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Immetti il prompt </td> 
   <td> <p>Immettere o mappare il prompt da elaborare.</p> </td> 
  </tr> 
 </tbody> 
</table>


