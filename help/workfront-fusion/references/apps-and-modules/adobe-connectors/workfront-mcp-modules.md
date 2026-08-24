---
title: Moduli MCP di Adobe Workfront
description: Con il modulo MCP di Adobe Workfront, puoi inviare un messaggio in inglese semplice al server MCP di Adobe Workfront e consentire a un modello AI di eseguire la richiesta.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 88515edc81bafe2d1a81df627fd51dd4ed674c02
workflow-type: tm+mt
source-wordcount: 884
ht-degree: 16%

---

# Moduli MCP di Adobe Workfront

Il connettore MCP di Adobe Workfront è un’integrazione dedicata di Fusion per il server MCP (Model Context Protocol) di Adobe Workfront. A differenza di un connettore tipico, in cui ogni modulo esegue un’azione fissa, questo connettore ha un singolo modulo che accetta un’istruzione aperta in inglese semplice e consente a un modello di intelligenza artificiale di decidere quali operazioni Workfront sono necessarie per soddisfarla.

Ad esempio, puoi immettere il prompt &quot;Trova tutti i miei progetti attivi che sono in ritardo sulla programmazione e riepiloga il loro stato&quot; e il modulo restituisce una risposta sintetizzata, invece di dover concatenare diversi moduli Get e Filter.

Puoi limitare quali azioni di Workfront l’IA può eseguire, in modo che anche uno scenario incustodito possa garantire che non venga eseguita alcuna azione distruttiva inaspettata.

Per impostazione predefinita, questo modulo utilizza Adobe Managed AI, che utilizza il modello `claude-sonnet-5`. È possibile configurare il modulo in modo che utilizzi un LLM diverso, utilizzando una chiave e altre credenziali fornite.

>[!NOTE]
>
>L’utilizzo di Adobe Managed AI è limitato a 25 $ per organizzazione al mese.

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

## Collegare Adobe Workfront MCP a Workfront Fusion

Il connettore MCP di Adobe Workfront utilizza OAuth 2.0 per connettersi a Workfront. A differenza di altri connettori Workfront, non vi sono campi di connessione manuali da compilare, come un host, un ID client o un segreto client.

Per creare una connessione:

1. Nel modulo MCP di Adobe Workfront, fai clic su **[!UICONTROL Aggiungi]** accanto al campo Connessione.
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
          <p>Specifica un nome per questa connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

   Se non hai effettuato l’accesso a Workfront, verrà aperta una schermata di accesso. Accedi e approva l’accesso.

Viene eseguito il reindirizzamento a Workfront Fusion e la nuova connessione è disponibile nel modulo.

>[!NOTE]
>
>Al primo utilizzo, la connessione si registra automaticamente con il server MCP di Workfront e riutilizza tale registrazione per ogni connessione successiva creata.

## Modulo MCP Adobe Workfront e relativi campi

### Elabora un prompt utente

Questo modulo di azione elabora un prompt in inglese semplice contro il server MCP di Workfront, utilizzando il modello di lingua specificato, e restituisce la risposta dell’intelligenza artificiale.

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
  </tr>   <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Connettere Adobe Workfront MCP a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Strumenti di sola lettura <i>(facoltativo)</i></td> 
   <td> <p>Limita le azioni di Workfront di sola lettura che l’IA può chiamare. Se non è selezionato alcun strumento, sono consentiti tutti gli strumenti di sola lettura.</p> </td> 
  </tr> 
  <tr> 
   <td>Strumenti di scrittura/eliminazione <i>(facoltativo)</i></td> 
   <td> <p>Inserisci le azioni Workfront di scrittura o eliminazione che l’IA può chiamare. Se si lascia vuoto, tutti gli strumenti di scrittura ed eliminazione sono consentiti.</p> <p>Per garantire che uno scenario incustodito non intraprenda mai un'azione distruttiva, si consiglia di lasciare questo campo impostato su una selezione deliberatamente vuota, anziché lasciarlo senza restrizioni.</p> </td> 
  </tr> 
  <tr> 
   <td>Immetti il prompt</td> 
   <td> <p>Immetti o mappa l’istruzione, in inglese semplice, che desideri che l’intelligenza artificiale esegua.</p> <p>Esempio: <i>Trova tutti i progetti assegnati all'utente che sono in ritardo.</i></p> </td> 
  </tr>  </tbody> 
</table>

Per un elenco degli strumenti che è possibile selezionare per i campi Strumenti di sola lettura e Strumenti di scrittura/eliminazione, vedere [Strumenti server Adobe Workfront MCP](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools) nella documentazione di Workfront.

Il modulo restituisce le seguenti informazioni, che puoi mappare nei moduli successivi nello scenario:

* **Risposta**: la risposta finale dell&#39;IA, sotto forma di testo.
* **Audit Trail**: un record della sessione, inclusi il prompt originale, l&#39;ora di inizio e di fine e i dettagli di ogni chiamata all&#39;intelligenza artificiale effettuata dallo strumento, ad esempio il nome dello strumento, gli argomenti, l&#39;esito positivo, la durata e l&#39;output.
* **Riepilogo**: totali per la sessione, compreso il numero di chiamate allo strumento tentate, il numero di operazioni riuscite o non riuscite, il tempo totale di elaborazione e lo stato complessivo.
