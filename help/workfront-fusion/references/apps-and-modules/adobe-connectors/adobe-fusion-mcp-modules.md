---
title: Moduli MCP di Adobe Fusion
description: Con il modulo MCP di Adobe Fusion, puoi inviare un messaggio in inglese semplice al server MCP di Adobe Fusion e consentire a un modello di intelligenza artificiale di eseguire la richiesta.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 14%
---
# Moduli MCP di Adobe Fusion

Il connettore MCP di Adobe Fusion invia un messaggio in inglese semplice al server MCP (Adobe Fusion Model Context Protocol). Un modello di intelligenza artificiale interpreta la richiesta e chiama gli strumenti Fusion necessari per completarla.

Il connettore funziona solo con il server Adobe Fusion MCP in hosting. Non è possibile puntarlo a un altro server MCP.

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Collegare Adobe Fusion MCP a Workfront Fusion

Puoi creare una connessione direttamente dall’interno del modulo Adobe Fusion MCP.

1. Nel modulo MCP di Adobe Fusion, fai clic su **[!UICONTROL Aggiungi]** accanto al campo **Connessione**.
1. Compila i seguenti campi:

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
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

Viene visualizzata la pagina di accesso di Adobe. Accedi con il tuo account Adobe e approva l&#39;accesso. Viene eseguito il reindirizzamento a Workfront Fusion e la nuova connessione è disponibile nel modulo.

## Modulo MCP di Adobe Fusion e relativi campi

### Elabora un prompt utente

Questo modulo di azione invia un messaggio in inglese semplice al server Adobe Fusion MCP. Un modello di IA interpreta il prompt, chiama gli strumenti di Fusion necessari per completarlo e restituisce il risultato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Chiave LLM <i>(Facoltativa, avanzata)</i></td> 
   <td> <p>Per impostazione predefinita, questo modulo elabora la richiesta utilizzando Adobe Managed AI e non è necessario selezionare una chiave.</p> <p>Per utilizzare un provider di IA personale, selezionare una chiave LLM esistente o crearne una nuova facendo clic su <b>Aggiungi</b> e immettendo le seguenti informazioni:</p>
     <ul>
       <li><b>Nome chiave</b>: immettere un nome per la nuova chiave.</li>
       <li><b>LLM</b>: selezionare il modello di lingua di grandi dimensioni a cui è associata la chiave. I provider supportati sono OpenAI, Anthropic e Amazon Bedrock.</li>
       <li><b>Chiave</b>: immetti o mappa la chiave API per il provider selezionato.</li>
       <li><b>Modello</b>: selezionare il modello LLM utilizzato dalla chiave.</li>
       <li><b>Altri campi</b>: immettere i valori per tutti gli altri campi richiesti da LLM.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Adobe Fusion MCP a Workfront Fusion, vedere <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Connettere Adobe Fusion MCP a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Strumenti di sola lettura <i>(facoltativo)</i></td> 
   <td> <p>Seleziona strumenti di sola lettura specifici per limitare l’intelligenza artificiale. Se non è selezionato nessuno, sono consentiti tutti gli strumenti di sola lettura di questa categoria.</p> </td> 
  </tr> 
  <tr> 
   <td>Strumenti di scrittura/eliminazione <i>(facoltativo)</i></td> 
   <td> <p>Seleziona strumenti di scrittura o eliminazione specifici per limitare l’intelligenza artificiale. Se non è selezionato nessuno, sono consentiti tutti gli strumenti di scrittura ed eliminazione di questa categoria.</p> <p>Per garantire che uno scenario incustodito non intraprenda mai un'azione distruttiva, si consiglia di lasciare questo campo impostato su una selezione deliberatamente vuota, anziché lasciarlo senza restrizioni.</p> </td> 
  </tr> 
  <tr> 
   <td>Immetti il prompt</td> 
   <td> <p>Immetti o mappa l’istruzione, in inglese semplice, che desideri che l’intelligenza artificiale esegua.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Limita gli strumenti che l’intelligenza artificiale può chiamare

È possibile limitare quali strumenti Fusion possono essere chiamati dall’IA selezionando gli strumenti nei campi Strumenti di sola lettura e Strumenti di scrittura/eliminazione.

* Se lasci vuoto un campo, l’intelligenza artificiale può chiamare ogni strumento di quella categoria.
* Se lasciate entrambi i campi vuoti, l’intelligenza artificiale può chiamare ogni strumento sul server Fusion MCP.

Per evitare che uno scenario automatico esegua un&#39;azione di scrittura o eliminazione, selezionare solo gli strumenti che si desidera consentire nel campo Strumenti di sola lettura e selezionare almeno uno strumento nel campo Strumenti di scrittura/eliminazione che si ha familiarità con la chiamata AI.

I nomi degli strumenti negli elenchi provengono dal server Fusion MCP.

#### Elaborazione della richiesta da parte del modulo

* Il modulo non ha un turno successivo. Se il prompt non è chiaro, l’IA fa un presupposto ragionevole e lo afferma nella risposta anziché porti una domanda.
* L’intelligenza artificiale verifica le informazioni che possono cambiare utilizzando gli strumenti.
* L’intelligenza artificiale non esegue alcuna azione di scrittura o eliminazione oltre a quelle richieste dal prompt.
* Il modulo richiede una connessione valida. Non funziona senza.

#### Output

Il modulo restituisce le seguenti informazioni, che puoi mappare nei moduli successivi nello scenario:

* **Risposta**: la risposta finale dell&#39;IA, sotto forma di testo.
* **Audit Trail**: record della sessione, inclusi gli strumenti denominati, i relativi argomenti e risultati e gli intervalli.
* **Riepilogo**: totali per la sessione, compreso il numero di chiamate dello strumento riuscite e lo stato finale.
