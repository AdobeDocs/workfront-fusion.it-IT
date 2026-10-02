---
title: Modulo MCP Adobe Marketo Engage
description: Il modulo MCP di Adobe Marketo Engage consente di inviare un prompt in linguaggio naturale al server MCP (Model Context Protocol) di Adobe Marketo Engage.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 9%
---
# Modulo MCP Adobe Marketo Engage

Il modulo MCP di Adobe Marketo Engage ti consente di inviare un prompt in linguaggio naturale al server MCP (Model Context Protocol) di Adobe Marketo Engage, utilizzando un modello di intelligenza artificiale per interpretare la richiesta e chiamare gli strumenti di Marketo per soddisfarla. A differenza di un connettore Marketo tradizionale in cui ogni modulo esegue un’azione fissa, ad esempio &quot;Crea un lead&quot;, questo connettore ha un singolo modulo che accetta un’istruzione aperta in inglese semplice e consente all’intelligenza artificiale di decidere quali operazioni Marketo sono necessarie per soddisfarla.

Questo connettore è specifico per il server MCP di Marketo Engage

Per connettersi a MCP per altre applicazioni, consulta [Aggiungere un prompt di IA al tuo scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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

* È necessario disporre di un account Adobe Marketo Engage e di un&#39;istanza Marketo valida.

## Collegare Adobe Marketo Engage MCP a Workfront Fusion {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

Puoi creare una connessione all’istanza di Marketo direttamente dall’interno del modulo MCP di Adobe Marketo Engage.

1. Nel modulo MCP di Adobe Marketo Engage, fai clic su **Aggiungi** accanto al campo **Connessione**.
1. Compila i seguenti campi:

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Inserisci un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>
          <p>Specifica se ti connetti a un account di servizio o a un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>
          <p>Immetti l’ID client per il servizio API REST di Marketo, come creato in Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>
          <p>Immetti il segreto client per il servizio API REST di Marketo, come creato in Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Immetti l’ID Munchkin dell’istanza Marketo (ad esempio, `123-ABC-456`). L'ID Munchkin viene visualizzato in Marketo in <b>Amministratore → Munchkin</b>.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Fai clic su **Continua** per creare la connessione e tornare al modulo.

>[!IMPORTANT]
>
> * Invece di riutilizzare un account amministratore, utilizza un utente Marketo dedicato e solo API con il ruolo e le autorizzazioni minimi necessari per lo scenario.
> * La creazione della connessione non convalida le credenziali. Fusion li salva senza una chiamata di prova, quindi la connessione può apparire creata correttamente anche se un valore è errato o digitato in modo errato. Se una credenziale non è corretta, l’errore viene in genere visualizzato in un secondo momento quando il modulo tenta di raggiungere per la prima volta Marketo o quando gli elenchi degli strumenti non vengono caricati.

## Modulo: &quot;Elabora un prompt utente&quot;

Questo è l’unico modulo fornito dal connettore. Uno scenario lo utilizza fornendo:

1. **Connessione**: la connessione Marketo creata in precedenza.
2. **Immettere il prompt**, ovvero l&#39;istruzione, in inglese semplice (ad esempio, &quot;trova ogni lead aggiunto all&#39;elenco dei webinar di primavera nell&#39;ultima settimana e indica quali non hanno impostato il nome della società&quot;).
3. **Strumenti** (facoltativo) - descritto di seguito. Questi campi vengono visualizzati solo dopo aver selezionato una connessione.
4. **Chiave LLM** (facoltativa, avanzata) - descritta di seguito.

Restituisce la risposta finale dell’intelligenza artificiale come testo, più una traccia di audit completa di ciò che è accaduto durante la produzione della risposta.

## Modulo MCP Adobe Marketo Engage e relativi campi

### Elabora un prompt utente

Questo modulo di azione invia un’istruzione in inglese semplice al server MCP di Adobe Marketo Engage e restituisce la risposta dell’intelligenza artificiale.

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
   <td><p>Per istruzioni sulla connessione dell'account Marketo a Workfront Fusion, vedere <a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">Connettere Adobe Marketo Engage MCP a Workfront Fusion</a> in questo articolo.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Prompt utente</td>
   <td><p>Immetti o mappa l’istruzione, in inglese semplice, che desideri che l’intelligenza artificiale esegua.</p><p>Esempio: <i>Trova tutti i lead aggiunti all'elenco dei webinar di primavera negli ultimi 7 giorni e riepiloga i settori più comuni.</i></p></td>
  </tr>
 </tbody>
</table>

### Uscita modulo

L’output è un singolo bundle contenente quanto segue:

* Risposta: la risposta finale dell’intelligenza artificiale, sotto forma di testo. Puoi mappare questi dati nei moduli successivi.
* Audit Trail: record dettagliato dell’esecuzione, tra cui un ID sessione, il prompt originale, gli orari di inizio e fine, la durata totale, lo stato complessivo, la risposta finale e un elenco di chiamate allo strumento. Ogni voce di chiamata dello strumento registra l&#39;esecuzione dello strumento Marketo, i relativi argomenti, l&#39;output, l&#39;ora e la durata di inizio e fine, se l&#39;esecuzione è avvenuta e l&#39;ordine nella sequenza.
* Riepilogo: la stessa esecuzione è ridotta in numero: chiamate utensile totali, chiamate riuscite, chiamate non riuscite, tempo di elaborazione e stato.

### Modelli IA

Per impostazione predefinita, il modulo utilizza automaticamente il servizio di intelligenza artificiale gestita di Adobe, senza chiave o credenziali da immettere.

È invece possibile selezionare una chiave LLM specifica da utilizzare OpenAI, Anthropic Claude o Amazon Bedrock, se l’organizzazione dispone di un account con uno di questi.

### Scelta delle azioni di Marketo che l’IA può eseguire

Dopo aver selezionato una connessione, il modulo chiede al server Marketo MCP quali strumenti offre e li presenta come elenchi a selezione multipla, ognuno dei quali mostra il numero di strumenti contenuti:

* Strumenti di sola lettura: azioni che cercano solo un elemento e non modificano mai nulla, ad esempio la ricerca di un lead, l’elenco dei membri della campagna o la lettura dei dettagli di un programma.
* Strumenti di scrittura/eliminazione: azioni che modificano elementi, ad esempio la creazione o l’aggiornamento di un lead, l’aggiunta di un utente a un elenco, l’attivazione di una campagna o l’approvazione o l’invio di un messaggio e-mail.
* Altri strumenti: un terzo elenco che viene visualizzato solo se il server Marketo offre strumenti non etichettati come di sola lettura o meno. Questi vengono mostrati separatamente piuttosto che essere considerati sicuri o non sicuri. Se il server etichetta tutto, l&#39;elenco non viene visualizzato.

Se non è selezionato alcun strumento, l’intelligenza artificiale può utilizzarli tutti. È possibile limitare un elenco ad azioni specifiche. Ad esempio, se selezioni solo 2 azioni di &quot;scrittura&quot; specifiche lasciando solo &quot;sola lettura&quot;, l’intelligenza artificiale può cercare liberamente tutto ciò di cui ha bisogno, ma può apportare solo questi 2 tipi specifici di modifiche. Se si lascia vuoto un elenco, tutte le azioni della categoria sono consentite. Per limitare l’intelligenza artificiale è necessario scegliere attivamente quali azioni specifiche consentire in tale categoria. In questo modo puoi assicurarti che l’intelligenza artificiale non intraprenda un’azione distruttiva inaspettata contro i dati di marketing in tempo reale, pur consentendo alla libreria di raccogliere liberamente le informazioni.

Poiché gli elenchi vengono letti in tempo reale dal server Marketo, gli strumenti mostrati possono cambiare man mano che Adobe aggiorna tale server.

### Nessuna cronologia di conversazione persistente

Ogni esecuzione di questo modulo è una singola esecuzione autonoma. L’intelligenza artificiale non può porre una domanda di follow-up e attendere una risposta. Deve invece esprimere il suo giudizio e fornire una risposta completa e definitiva in un solo passaggio. Se una richiesta è ambigua, l’IA effettuerà un presupposto ragionevole, lo dichiarerà come parte della sua risposta e procederà. Non si fermerà e chiederà all&#39;utente di chiarire, perché non c&#39;è modo per esso di ricevere una risposta all&#39;interno di una singola esecuzione.

L’intelligenza artificiale è anche istruita a verificare i fatti con una chiamata allo strumento anziché basarsi sulla memoria, perché i dati di Marketo potrebbero essere cambiati rispetto all’esecuzione precedente.

L’IA esegue un’azione di scrittura, aggiornamento o eliminazione solo quando il prompt ne richiede effettivamente una. Non eseguirà un’azione non richiesta, incluse l’attivazione o la disattivazione di campagne, la creazione o l’eliminazione di lead ed elenchi e l’approvazione o l’invio di e-mail, anche nella stessa esecuzione in cui esegue un’altra operazione richiesta dall’utente.

Poiché ogni esecuzione è indipendente, l’intelligenza artificiale non dispone di memoria di un’esecuzione precedente. Uno scenario che richieda un’esperienza a più turni simile a una chat deve fornire esplicitamente tale cronologia come parte del nuovo prompt, ad esempio memorizzando la domanda e la risposta precedenti nel Data Store di Fusion, o passata tra i moduli, e includendola come testo all’inizio del nuovo prompt, seguito dalla nuova domanda. Non esiste alcuna sessione o ID di conversazione che ricordi automaticamente le esecuzioni precedenti.

## Esempi di prompt

È possibile utilizzare prompt quali:

* *Elenca i lead che hanno aderito al programma &#39;Lancio prodotto Q3&#39; negli ultimi 7 giorni e riepiloga i settori di appartenenza.*
* *Verifica se la campagna avanzata &quot;Serie di benvenuto&quot; è attualmente attiva e indica quante persone vi partecipano.*
* *Trovare il modulo utilizzato nella pagina dei prezzi e indicare i campi contrassegnati come obbligatori.*
* *Aggiungere il lead con l&#39;e-mail `jane@example.com` all&#39;elenco statico &#39;Clienti VIP&#39;.*
* *Riepiloga le prestazioni di ogni e-mail nel programma &#39;Newsletter di primavera&#39;.*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/mcp-server

  -->
