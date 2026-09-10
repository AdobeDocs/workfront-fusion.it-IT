---
title: Moduli MCP di Adobe Experience Manager
description: Con il modulo MCP di Adobe Experience Manager, puoi inviare un messaggio in inglese semplice al server MCP di Adobe Experience Manager e consentire a un modello AI di eseguire la richiesta.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 4c23409465b4be9fd10ff6938a750bc662ba2fe4
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 11%

---

# Moduli MCP di Adobe Experience Manager

Il connettore MCP di Adobe Experience Manager è un&#39;integrazione Fusion dedicata per il server MCP (Model Context Protocol) di Adobe Experience Manager. A differenza di un connettore tipico, in cui ogni modulo esegue un’azione fissa, questo connettore ha un singolo modulo che accetta un’istruzione aperta in inglese semplice e consente a un modello di intelligenza artificiale di decidere quali operazioni Adobe Experience Manager sono necessarie per eseguirlo, in aree come siti, risorse digitali, frammenti di contenuto, cartelle, archivio dei contenuti e IA per l’analisi dei contenuti.

Questo connettore è dedicato al server MCP di Adobe Experience Manager. Non supporta altri server MCP non correlati. Per un connettore che può invece puntare a qualsiasi server MCP, utilizza il connettore dell’agente MCP.

Per informazioni sul connettore dell&#39;agente MCP, vedere [Modulo dell&#39;agente MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).

>[!NOTE]
>
>Le risposte di questo modulo sono generate dall’intelligenza artificiale e possono occasionalmente essere imperfette, anche con ogni protezione disponibile. Questo modulo è appropriato per l’automazione, in cui un utente non esamina ogni esecuzione in tempo reale, ma non è una garanzia del comportamento deterministico che si otterrebbe da un modulo Adobe Experience Manager tradizionale.

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
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: disponibile per le organizzazioni con licenze basate su operazioni</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

* Per utilizzare questo modulo è necessario disporre di un account Adobe Experience Manager.

## Collegare Adobe Experience Manager MCP a Workfront Fusion {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

Il connettore MCP di Adobe Experience Manager utilizza OAuth per connettersi a Adobe Experience Manager. Non sono presenti campi di connessione da compilare manualmente, ad esempio un nome utente, una password o una chiave API.

Per creare una connessione:

1. Nel modulo MCP di Adobe Experience Manager, fai clic su **[!UICONTROL Aggiungi]** accanto al campo Connessione.
1. Seleziona se ti connetti a un ambiente di produzione o non di produzione.
1. Seleziona se ti stai connettendo a un account Servizio o a un account Personale
1. Fai clic su **Continue** (Continua).

   Viene visualizzata la pagina di accesso di Adobe.
1. Nella pagina di accesso di Adobe, accedi e approva l’accesso.

Viene eseguito il reindirizzamento a Workfront Fusion e la nuova connessione è disponibile nel modulo.

## Modulo MCP Adobe Experience Manager e relativi campi

Attualmente, il connettore MCP di Adobe Experience Manager contiene un solo modulo.

### Elabora un prompt utente

Questo modulo di azione invia un’istruzione in inglese semplice al server MCP di Adobe Experience Manager e restituisce la risposta dell’intelligenza artificiale.

Ogni esecuzione di questo modulo è una singola esecuzione autonoma, simile all’invio di un’e-mail anziché di una conversazione in tempo reale. L’intelligenza artificiale non può porre una domanda di follow-up e attendere la tua risposta. Invece, fa il suo miglior giudizio e restituisce una risposta completa. Se il prompt è ambiguo, l’intelligenza artificiale indica qualsiasi presupposto che ha fatto come parte della sua risposta, anziché fermarsi per chiederti di chiarire.

>[!IMPORTANT]
>
>Questo modulo esegue un’azione di scrittura o eliminazione solo quando il prompt ne richiede effettivamente una. Non richiede alcuna azione aggiuntiva che non hai richiesto, nemmeno nella stessa corsa in cui esegue qualcos&#39;altro che hai richiesto.

Poiché ogni esecuzione è indipendente, il modulo non dispone di memoria delle esecuzioni precedenti. Per creare un’esperienza a più turni e conversazionale su più esecuzioni, archivia la domanda e la risposta precedenti. A tale scopo, è possibile utilizzare un archivio dati e quindi includere la cronologia come testo all&#39;inizio del prompt successivo, seguito dalla nuova domanda.

Per informazioni sugli archivi dati, vedere [Archivio dati](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md).

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">Chiave LLM <i>(Facoltativa, avanzata)</i></td>
   <td><p>Per impostazione predefinita, questo modulo elabora la richiesta utilizzando il servizio AI di Adobe e non è necessario selezionare una chiave.</p><p>Per utilizzare un provider di IA personale, selezionare una chiave LLM esistente o crearne una nuova facendo clic su <b>Aggiungi</b> e immettendo le seguenti informazioni:</p>
    <ul>
     <li><b>Nome chiave</b>: immettere un nome per la nuova chiave.</li>
     <li><b>LLM</b>: selezionare il modello di lingua di grandi dimensioni a cui è associata la chiave. I fornitori supportati sono OpenAI, Anthropic Claude e Amazon Bedrock.</li>
     <li><b>Chiave</b>: immetti o mappa la chiave API per il provider selezionato.</li>
     <li><b>Modello</b>: selezionare il modello LLM utilizzato dalla chiave.</li>
     <li><b>Altri campi</b>: immettere i valori per tutti gli altri campi richiesti da LLM.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">Connessione</td>
   <td><p>Per istruzioni sulla connessione dell'account Adobe Experience Manager a Workfront Fusion, vedere <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager MCP a Workfront Fusion</a> in questo articolo.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Prompt utente</td>
   <td><p>Immetti o mappa l’istruzione, in inglese semplice, che desideri che l’intelligenza artificiale esegua.</p><p>Esempio: <i>Trova tutte le risorse nella cartella di marketing che non sono state aggiornate in 90 giorni.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">Strumenti di sola lettura <i>(facoltativo)</i></td>
   <td><p>Limita le azioni di sola lettura di Adobe Experience Manager che l’IA può chiamare: azioni che cercano solo elementi, come la ricerca di una risorsa o la lettura del contenuto di una pagina, e non cambiano mai nulla.</p><p>Se si lascia vuoto questo campo, sono consentite tutte le azioni di sola lettura.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Strumenti di scrittura/eliminazione <i>(facoltativo)</i></td>
   <td><p>Limita le azioni di scrittura o eliminazione di Adobe Experience Manager che l’IA può chiamare, azioni che modificano qualcosa, ad esempio l’aggiornamento di una pagina, la pubblicazione di contenuto o l’eliminazione di una risorsa.</p><p>Se lasci vuoto questo campo, sono consentite tutte le azioni di scrittura ed eliminazione. Per garantire che uno scenario incustodito non intraprenda mai un'azione distruttiva, si consiglia di lasciare questo campo impostato su una selezione deliberatamente vuota, anziché lasciarlo senza restrizioni.</p></td>
  </tr>
 </tbody>
</table>

Il modulo restituisce la risposta finale dell’intelligenza artificiale, come testo, insieme a una registrazione di ciò che è accaduto durante la produzione della risposta, inclusi gli strumenti chiamati, se ogni chiamata è riuscita e quanto tempo è stato necessario per l’elaborazione.
