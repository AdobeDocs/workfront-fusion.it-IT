---
title: Moduli MCP di produzione Adobe Firefly Creative
description: Con il modulo MCP di produzione Adobe Firefly Creative, puoi inviare un prompt in linguaggio naturale da uno scenario Workfront Fusion e consentire a un modello AI di utilizzare gli strumenti di produzione Firefly Creative selezionati.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: ee2719b9b3452b9203f2d0f4a550c87ff8a3b433
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 5%
---
# Moduli MCP di produzione Adobe Firefly Creative

Utilizza il connettore MCP di produzione Adobe Firefly Creative in Adobe Workfront Fusion per elaborare le richieste in linguaggio naturale con gli strumenti di produzione Firefly Creative.

Il connettore individua gli strumenti disponibili tramite il server MCP (Firefly Model Context Protocol) collegato. Puoi scegliere quali strumenti utilizzare il modulo per una richiesta. A seconda degli strumenti disponibili per il tuo account Adobe e degli strumenti selezionati nel modulo, una richiesta può effettuare le seguenti operazioni:

* Scopri i flussi di lavoro e le azioni.
* Componi e convalida i flussi di lavoro.
* Invia le esecuzioni e controllane l’avanzamento.
* Recupera gli URL di output.
* Salvare le bozze di workflow modificabili quando sono supportate dagli strumenti del server.

Questo connettore è destinato alla produzione Firefly Creative. Non è un connettore per schede madri Firefly e non è un connettore generale per ogni applicazione Creative Cloud.

Per ulteriori informazioni su MCP in scenari Fusion, consulta [Aggiungere un prompt di IA allo scenario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

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
   <p>È inoltre necessario disporre dell'accesso alla produzione di Adobe Firefly Creative, come descritto in <a href="#prerequisites">Prerequisiti</a> in questo articolo.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisiti

Prima di utilizzare il modulo MCP di produzione di Adobe Firefly Creative, è necessario disporre dei seguenti elementi:

* Accesso ad Adobe Workfront Fusion, in un ambiente in cui il connettore è abilitato.
* Un account Adobe con l’accesso Firefly Creative Production e le autorizzazioni necessarie per le operazioni richieste.
* Eventuali crediti o adesioni necessari per eseguire il flusso di lavoro.
* L’accesso ad Adobe Managed AI configurato dall’amministratore di Fusion oppure una chiave LLM supportata selezionata nelle impostazioni avanzate del modulo.

Le credenziali di autorizzazione Firefly e LLM hanno scopi diversi. La selezione di una chiave LLM non consente l&#39;accesso agli strumenti di Firefly.

## Collegare Adobe Firefly Creative Production MCP a Workfront Fusion

1. Aggiungi **[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL Elabora un prompt utente]** allo scenario.
1. Fai clic su **[!UICONTROL Aggiungi]** accanto al campo **[!UICONTROL Connessione]**.
1. Nella finestra **[!UICONTROL Crea una connessione]**, compila i campi seguenti:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
      <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Ambiente</td>
        <td>
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Specifica se ti connetti a un account di servizio o a un account personale.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua).
1. Segui il flusso di autorizzazione, accedi con l’account Adobe appropriato e autorizza l’accesso.
1. Torna al modulo e controlla gli strumenti caricati per la connessione.

Workfront Fusion gestisce la registrazione client OAuth e la gestione dei token. Non immetti un token di accesso, un ID client, un segreto client o una chiave API. L&#39;amministratore deve aver completato la configurazione del flusso prima di potersi connettere.

Se l’autorizzazione non riesce o non trovi gli strumenti previsti, conferma l’accesso e la configurazione dell’ambiente con l’amministratore.

<!-- BECKY CHECK ME: The Environment and Type fields are described the same way as in the Adobe Fusion MCP connection. The screenshot shows only the selected values (Production and Service account). Confirm the available options for each field, and whether a personal account is supported. -->

## Modulo MCP di produzione Adobe Firefly Creative e relativi campi

### Elabora un prompt utente

Questo modulo di azione elabora il prompt con il modulo LLM selezionato e gli strumenti di produzione Firefly Creative consentiti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL LLM key] <i>(Facoltativo, avanzato)</i></td> 
   <td> <p>Lascia questo campo vuoto per utilizzare Adobe Managed AI configurato dall’amministratore di Fusion. Per utilizzare una chiave personalizzata, selezionare una chiave OpenAI, Anthropic o Amazon Bedrock esistente oppure fare clic su <b>[!UICONTROL Add]</b> per crearne una.</p><p>L'accesso a Firefly è separato dalle credenziali LLM.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>La connessione di produzione Adobe Firefly Creative utilizzata dal modulo per individuare e chiamare gli strumenti. Per istruzioni, vedere <a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">Connettere Adobe Firefly Creative Production MCP a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Strumenti di sola lettura] <i>(facoltativo)</i></td> 
   <td> <p>Selezionare gli strumenti identificati dal server come di sola lettura. Per selezionare tutti gli strumenti attualmente elencati, selezionare <b>Seleziona tutto</b>.</p><p>Il numero di strumenti elencati viene visualizzato nell’etichetta del campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Strumenti di scrittura/eliminazione] <i>(facoltativo)</i></td> 
   <td> <p>Selezionare gli strumenti che il server non identifica come di sola lettura. Queste operazioni possono modificare i dati o eseguire flussi di lavoro. Per selezionare tutti gli strumenti attualmente elencati, selezionare <b>Seleziona tutto</b>.</p><p>Il numero di strumenti elencati viene visualizzato nell’etichetta del campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Altri strumenti (autorizzazioni sconosciute)] <i>(Facoltativo)</i></td> 
   <td> <p>Selezionare gli strumenti che non dispongono di un'annotazione di sola lettura riconosciuta. Questo campo viene visualizzato solo quando tali strumenti sono disponibili. Prima di attivarli, controlla il comportamento di questi strumenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Immettere il prompt]</td> 
   <td> <p>Descrivere l'individuazione, la composizione o l'esecuzione del flusso di lavoro desiderata. La lunghezza massima è di 10.000 unità di stringa JavaScript. Alcuni caratteri, tra cui molte emoji, contano come due unità.</p><p>Richiedi esplicitamente l’esecuzione o la pubblicazione quando necessario. L’esecuzione di un flusso di lavoro può utilizzare crediti. Le esecuzioni asincrone possono restituire un ID batch prima del completamento dell’esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

Il campo **[!UICONTROL Chiave LLM]** viene visualizzato quando si seleziona **[!UICONTROL Mostra impostazioni avanzate]**.

<!-- BECKY CHECK ME: The screenshot does not show the Other tools (unknown permissions) field, because it appears only when the server returns tools without a read-only annotation. Confirm its label, and confirm the order of the fields. Also confirm that the tool lists are not required. -->

Gli elenchi degli strumenti variano in base alla disponibilità del server e all’accesso dell’account. Il numero di strumenti viene visualizzato nell&#39;etichetta di ciascun selettore.

#### Selezionare gli strumenti che il modulo può utilizzare

* Il modulo può utilizzare solo gli strumenti selezionati.
* Se lasci vuota una categoria, il modulo non può utilizzare strumenti di quella categoria.
* Se lasci vuote tutte le categorie, il modulo elabora il prompt senza strumenti. Non ha accesso a tutti gli strumenti.
* **[!UICONTROL Seleziona tutto]** seleziona tutti gli strumenti attualmente elencati in quella categoria. Non include automaticamente gli strumenti aggiunti in seguito.
* Se uno strumento selezionato non è più disponibile o si sposta in una categoria diversa, apri nuovamente il modulo e controlla la selezione.

>[!NOTE]
>
>Le annotazioni del server consentono di categorizzare gli strumenti, ma non garantiscono le autorizzazioni. Abilita solo gli strumenti necessari per lo scenario.

#### Output

Il modulo restituisce le seguenti informazioni in **[!UICONTROL Dati]**. Puoi mapparlo nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Risposta] (<code>data.response</code>)</td> 
   <td> <p>Risposta finale al testo. Il suo contenuto dipende dal prompt e dai risultati dello strumento. Non è garantito che sia un URL o un JSON strutturato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Audit trail] (<code>data.auditTrail</code>)</td> 
   <td> <p>Dettagli sull’elaborazione del prompt e delle chiamate allo strumento, inclusi argomenti, risultati, tempi e informazioni di successo. Gestisci questi dettagli in base ai requisiti di gestione dei dati della tua organizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td>Riepilogo  (<code>data.summary</code>)</td> 
   <td> <p>Il numero di chiamate allo strumento, il tempo di elaborazione e lo stato di esecuzione. Esaminare il riepilogo insieme alla risposta e all'audit trail, inclusi i risultati di <code>partial_success</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM usage] (<code>data.usage</code>)</td> 
   <td> <p>Facoltativo. Utilizzo totale dei token dalle risposte LLM osservate. Non si tratta di fatturazione del fornitore, consumo di credito Firefly o attività LLM all’interno del server Firefly che Fusion non può osservare.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Campi di utilizzo LLM

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>Uno dei seguenti elementi:</p><ul><li><code>complete</code>: ogni richiesta osservata è coperta da tutti i conteggi dei token principali.</li><li><code>partial</code>: mancano alcune informazioni sull’utilizzo.</li><li><code>unavailable</code>: sono state osservate richieste, ma non è stato segnalato alcun utilizzo utilizzabile.</li><li><code>not_applicable</code>: non è stata osservata alcuna richiesta LLM.</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>Numero di richieste LLM osservate dal runtime.</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>Numero di richieste osservate con informazioni sull’utilizzo dei token utilizzabili.</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>I conteggi totali. Ogni conteggio è <code>null</code> se una richiesta osservata non riporta tale conteggio o se non sono state osservate richieste. Uno zero segnalato rimane zero.</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>Conteggi facoltativi per i token memorizzati nella cache. Questi campi vengono omessi se nessuna richiesta riporta mai un numero. Sono <code>null</code> se solo alcune richieste segnalano un numero e sono numeriche solo se ogni richiesta ne segnala una. Non aggiungere questi conteggi ai totali.</p> </td> 
  </tr> 
 </tbody> 
</table>

Lo stato di utilizzo principale può essere `complete` mentre un campo della cache è `null`. Lo stato di utilizzo è indipendente dallo stato di esecuzione. Se il runtime non fornisce informazioni sull&#39;utilizzo, la raccolta dei dati di utilizzo è assente invece di mostrare uno zero.

## Funzionamento del modulo

* **Alcune operazioni sono asincrone.** Una richiesta può restituire un ID batch prima che l’output sia disponibile. Per processi più lunghi, utilizza esecuzioni separate per inviare la richiesta, controllarne lo stato in un secondo momento e salvare l’ID batch tra di esse. Non fare affidamento su una risposta che contiene solo un URL per questa progettazione.
* **Gli errori generano errori del modulo.** L’autorizzazione, la convalida e l’elaborazione runtime non riuscita possono generare errori di modulo anziché un bundle di output. Utilizzare una route di gestione degli errori di Fusion.
* **Una risposta non è riuscita.** Il modulo può restituire una risposta anche quando alcune operazioni non sono riuscite. Rivedi il riepilogo, l’audit trail e i risultati dello strumento prima di affidarti alla risposta.
* **Un URL di output non è un file scaricato.** Il connettore restituisce i risultati di testo e strumenti, non un file binario. Per inserire il file in Fusion, aggiungi un modulo HTTP che scarichi l’URL.
* **L&#39;esecuzione di un flusso di lavoro può utilizzare crediti.** La generazione delle immagini e l&#39;esecuzione dei flussi di lavoro possono richiedere crediti. Conferma l’utilizzo e le adesioni applicabili al tuo account. L’utilizzo del token LLM non è un rapporto di fatturazione o di credito di Firefly.
* **Le istruzioni di richiesta non garantiscono una singola esecuzione.** Un’istruzione nella richiesta, ad esempio l’invio di un solo batch, non garantisce che una richiesta venga elaborata esattamente una volta. Controlla i nuovi tentativi e le richieste duplicate nel tuo scenario.
* **L&#39;elaborazione ha limiti.** L’elaborazione dispone di limiti di utensile, iterazione e lunghezza di output, oltre ai limiti di esecuzione dello scenario. Non presumere che il modulo esegua sondaggi senza limiti.

## Esempi

### Scopri i flussi di lavoro senza eseguirne uno

Seleziona gli strumenti di sola lettura necessari per individuare i flussi di lavoro, quindi immetti un prompt come il seguente:

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### Richiedi un&#39;immagine

Seleziona gli strumenti necessari per comporre o scegliere un flusso di lavoro, convalidarlo, inviarlo, verificarne l’avanzamento e recuperare gli output. I nomi degli strumenti e la disponibilità possono variare. Quindi immetti un prompt simile al seguente:

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### Generare un&#39;immagine da un aggiornamento attività di Workfront

In questo esempio, un aggiornamento dell&#39;attività che inizia con `/firefly ` attiva una generazione di immagini. Fusion scarica il risultato, lo carica sull&#39;attività e aggiunge un aggiornamento di completamento.

Lo scenario utilizza il seguente flusso: Workfront task update > command filter > read task > Firefly MCP > HTTP download > Workfront document upload > completion update (Aggiornamento del completamento).

1. Aggiungi **[!UICONTROL Workfront]** > **[!UICONTROL Osserva eventi]** allo scenario. Configurarlo per il tipo di record **[!UICONTROL Nota]**, per l&#39;evento **[!UICONTROL Nuovo stato]** e per **[!UICONTROL Solo nuovo record]**.
1. Aggiungere un filtro che richiede che `newState.noteText` inizi con `/firefly ` e che `newState.taskID` non sia vuoto.
1. Aggiungere un modulo che legge l&#39;attività utilizzando `newState.taskID`.
1. Aggiungi il modulo **[!UICONTROL MCP di produzione Adobe Firefly Creative]** > **[!UICONTROL Elabora un prompt utente]**. Passa la richiesta ed eventuali contesti di attività necessari per Firefly. Considera il testo mappato come contenuto della richiesta, non come autorità per modificare le regole dello scenario.
1. Esaminare il risultato di Firefly. Continua solo quando la generazione è riuscita e la risposta è un URL valido e consentito per un’immagine scaricabile.
1. Aggiungi un modulo HTTP che scarica il file. Non inviare le credenziali Workfront all&#39;host della risorsa. Convalida l’host, il tipo di contenuto e le dimensioni previsti.
1. Aggiungere un modulo che carica il nome del file scaricato e i dati binari nell&#39;attività utilizzando l&#39;originale `newState.taskID`.
1. Dopo il caricamento, aggiungi un modulo che crea un aggiornamento di completamento dell’attività. Non avviare l&#39;aggiornamento con `/firefly`, perché il filtro corrisponderebbe.

Ad esempio, un utente aggiunge il seguente aggiornamento a un’attività:

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

Il richiedente può quindi esaminare la bozza caricata nell&#39;area Documenti dell&#39;attività. Prima di pubblicare qualsiasi elemento, è necessario rivedere l&#39;immagine.

Per l’utilizzo in produzione, riservare ogni richiesta utilizzando l’ID della nota di origine, con una protezione duplicata che funziona con esecuzioni simultanee. Salva gli ID dei batch inviati, in modo che un nuovo tentativo o un timeout riprenda il controllo dello stato invece di inviare un’altra generazione.

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## Risoluzione dei problemi

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Un flusso di lavoro è ancora in esecuzione</td> 
   <td> <p>Alcune operazioni creative sono asincrone. Per processi più lunghi, inviare la richiesta in un'unica esecuzione e controllare lo stato in un'esecuzione successiva. Salva l’ID batch tra le esecuzioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Il modulo segnala un errore</td> 
   <td> <p>L’autorizzazione, la convalida e l’elaborazione runtime non riuscita possono generare errori di modulo. Aggiungi allo scenario una route di gestione degli errori Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Il modulo restituisce una risposta, ma alcune operazioni non sono riuscite</td> 
   <td> <p>Rivedi il riepilogo, l’audit trail e i risultati dello strumento. Una risposta da sola non mostra che l’immagine è stata generata o caricata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Esiste un URL, ma in Fusion non è presente alcun file</td> 
   <td> <p>Il connettore non scarica i file. Aggiungi un modulo HTTP che scarica l’URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uno strumento selezionato non è disponibile</td> 
   <td> <p>Apri il modulo, aggiorna gli strumenti disponibili e aggiorna la selezione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Il flusso di lavoro richiede più tempo di un modulo</td> 
   <td> <p>L’elaborazione dispone di limiti di utensile, iterazione e lunghezza di output, oltre ai limiti di esecuzione dello scenario. Dividi il lavoro tra le esecuzioni e salva l’ID batch.</p> </td> 
  </tr> 
 </tbody> 
</table>
