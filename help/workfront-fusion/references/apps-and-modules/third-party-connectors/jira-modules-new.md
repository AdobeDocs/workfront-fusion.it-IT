---
title: Moduli Jira
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano il software Jira e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
source-git-commit: d16c1d9f257d44b72cfb93caa2a814fd62b0b733
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 5%

---

# Moduli Jira

>[!NOTE]
>
>Queste istruzioni si applicano alla nuova versione del connettore Jira, semplicemente etichettato Jira. Per istruzioni sui connettori legacy Jira Cloud e Jira Server, consulta [Moduli software Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Jira e collegarlo a più applicazioni e servizi di terze parti.

Il connettore Jira può essere utilizzato sia per Jira Cloud che per Jira Data Server.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli Jira è necessario disporre di un account Jira.

## Collegare Jira a Workfront Fusion

Puoi creare una connessione al tuo account Jira direttamente dall’interno di un modulo Jira.

>[!IMPORTANT]
>
>* Per creare una connessione di base al centro dati Jira, è necessario un token di accesso personale Jira.
>* Per creare una connessione di base a Jira Cloud, è necessario un token API Jira
>* Per creare una connessione OAuth 2 a Jira Cloud o Jira Data Center, è necessario disporre di un ID client e di un segreto client Jira.
>
>Per istruzioni sulla creazione di uno di questi, consulta la documentazione di Jira.

1. In qualsiasi modulo Jira, fai clic su **Aggiungi** accanto al campo Connessione.
1. Configura i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Tipo di connessione</p> </td> 
      <td> <p>Seleziona se stai creando una connessione di base o una connessione OAuth 2.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nome connessione</p> </td> 
      <td> <p>Immettere un nome per la nuova connessione.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">URL servizio</td>
      <td>Immetti l’URL dell’istanza Jira. Questo è l’URL che utilizzi per accedere a Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Tipo di account Jira</td>
       <td>Seleziona se ti stai connettendo a Jira Cloud o Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">ID client</td> 
      <td> <p>Se stai creando una connessione OAuth 2, immetti l’ID client Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Segreto client</td> 
      <td> <p>Se stai creando una connessione OAuth 2, inserisci il segreto client Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mail</td> 
      <td>Se stai creando una connessione di base a Jira Cloud, inserisci il tuo indirizzo e-mail.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token API</td> 
      <td>Se stai creando una connessione di base a Jira Cloud, immetti il token API.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token di accesso personale</td> 
      <td>Se stai creando una connessione di base al centro dati Jira, immetti il token di accesso personale.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Versione API</td> 
      <td>Seleziona la versione API Jira a cui vuoi connettere la connessione.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.


## Moduli Jira e relativi campi

Quando configuri i moduli Jira, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi Jira aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### Controlla i record

Questo modulo di attivazione avvia uno scenario quando viene aggiunto, aggiornato o eliminato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>Selezionare il webhook che si desidera utilizzare per controllare i record o crearne uno nuovo. </p> <p>Per creare un nuovo webhook:</p> 
    <ol> 
     <li>Fai clic su <strong>Aggiungi</strong></li> 
     <li>Immettere un nome per il webhook.</li> 
     <li> Seleziona la connessione da utilizzare per il webhook. <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </li> 
     <li> <p>Selezionare il tipo di record che si desidera che venga controllato dal software:</p> 
      <ul> 
       <li>Problema</li> 
       <li>Commento </li> 
       <li>Registro di lavoro </li> 
       <li>Progetto </li> 
       <li>Sprint</li> 
       <li>Allegato </li> 
      </ul> </li> 
     <li>Seleziona uno o più tipi di evento che attiveranno questo scenario.</li> 
     <li>Immetti un filtro Jira Query Language per questo modulo.<p>Per ulteriori informazioni su JQL, vedere <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> nella Guida di Atlassian. </p></li>
     <li>Fai clic su <b>Salva</b> per salvare il webhook. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [Aggiungi problema a sprint](#add-issue-to-sprint)
* [Crea un record](#create-a-record)
* [Chiamata API personalizzata](#custom-api-call)
* [Eliminare un record](#delete-a-record)
* [Scaricare un allegato](#download-an-attachment)
* [Leggi un record](#read-a-record)
* [Aggiornare un record](#update-a-record)

#### Aggiungi problema a sprint

Questo modulo di azione aggiunge uno o più problemi a uno sprint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID Sprint</td> 
   <td>Immetti o mappa l’ID Sprint dello sprint a cui desideri aggiungere un problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID problema o chiavi</td> 
   <td>Per ogni problema o chiave che si desidera aggiungere allo sprint, fare clic su <b>Aggiungi elemento</b> e immettere l'ID o la chiave del problema. In un modulo è possibile immettere fino a 50 caratteri.</td> 
  </tr> 
 </tbody> 
</table>

#### Crea un record

Questo modulo di azione crea un nuovo record in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Selezionare il tipo di record che si desidera venga creato dal modulo.</p> 
    <ul> 
     <li>Allegato</li> 
     <li>Commento</li> 
     <li>Problema</li> 
     <li>Progetto</li> 
     <li>Sprint </li> 
     <li>Registro di lavoro</li> 
     <li>Utente</li> 
     <li>Bacheca</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td> Compila gli altri campi. I campi sono disponibili a seconda del tipo di record selezionato. </td> 
  </tr> 
 </tbody> 
</table>

#### Chiamata API personalizzata

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Inserisci un percorso relativo a<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metodo</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Intestazioni</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stringa di query</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un record

Questo modulo di azione elimina il record specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Selezionare il tipo di record da eliminare dal modulo. </p> 
    <ul> 
     <li>Commento</li> 
     <li>Problema</li> 
     <li>Progetto</li> 
     <li>Sprint </li> 
     <li>Registro di lavoro</li> 
     <li>Allegato</li> 
     <li>Bacheca</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Tipo di record)ID</td> 
   <td>Immetti o mappa l’ID o la chiave del record da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Scaricare un allegato

Questo modulo di azione scarica l’allegato specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Immetti o mappa l’ID dell’allegato da scaricare.</td> 
  </tr> 
 </tbody> 
</table>

#### Leggi un record

Questo modulo di azione legge i dati dal record specificato in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Seleziona il tipo di record Jira che desideri che il modulo legga.</p> 
    <ul> 
     <li>Allegato</li> 
     <li>Commento</li> 
     <li>Problema</li> 
     <li>Progetto</li> 
     <li>Sprint </li> 
     <li>Registro di lavoro</li> 
     <li>Utente</li> 
     <li>Bacheca</li> 
     <li>Categoria</li> 
     <li>Filtro</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uscite</td> 
   <td>Selezionare gli output che si desidera ricevere. Le opzioni di output sono disponibili in base al tipo di record selezionato nel campo "Tipo di record".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Tipo di record) ID</td> 
   <td> <p>Immetti o mappa l’ID Jira univoco del record che desideri che il modulo legga.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un record

Questo modulo aggiorna un record esistente, ad esempio un problema o un progetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Selezionare il tipo di record da aggiornare nel modulo. Quando si seleziona un tipo di record, nel modulo vengono visualizzati altri campi specifici per tale tipo di record.</p> 
    <ul> 
     <li>Commento</li> 
     <li>Problema</li> 
     <li>Progetto</li> 
     <li>Sprint </li> 
     <li>Problema di transizione</li> 
     <li>Categoria </li> 
     <li>Filtro </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID o chiave</td> 
   <td>Immetti o mappa l’ID o la chiave del record da aggiornare.</td> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td> Compila gli altri campi. I campi sono disponibili a seconda del tipo di record selezionato. </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### Cerca record

Questo modulo di ricerca cerca i record in un oggetto in Jira che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Jira a Workfront Fusion, vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di Jira a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Selezionare il tipo di record da cercare nel modulo. Quando si seleziona un tipo di record, nel modulo vengono visualizzati altri campi specifici per tale tipo di record.</p> 
    <ul> 
     <li>Problema</li> 
     <li>Progetto</li> 
     <li>Utente</li> 
     <li>Sprint</li> 
     <li>Bacheca</li> 
     <li>Registro di lavoro</li> 
     <li>Commento</li> 
     <li>Problema di transizione</li> 
     <li>Categoria</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Risultati Max</p> </td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Immetti o mappa l’ID del primo elemento per il quale desideri recuperare i dettagli. Questo è un modo per impaginare i record. Se si immette l'elemento 5000 come offset, il modulo restituirà gli elementi 5000-9999.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td> Compila gli altri campi. I campi sono disponibili a seconda del tipo di record selezionato. </td> 
  </tr> 
 </tbody> 
</table>
