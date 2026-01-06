---
title: Moduli Jira
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano il software Jira e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: e65d868dc2165cbe800600f271f6b03d0a906cb4
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 20%

---

# Moduli Jira

>[!NOTE]
>
>Queste istruzioni si applicano alla nuova versione del connettore Jira, semplicemente etichettato Jira. Per istruzioni sui connettori legacy Jira Cloud e Jira Server, consulta [Moduli software Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Jira e collegarlo a più applicazioni e servizi di terze parti.

Il connettore Jira può essere utilizzato sia per Jira Cloud che per Jira Data Server.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

* Per utilizzare i moduli Jira è necessario disporre di un account Jira.
* Devi avere accesso a Jira Developer Console per creare un’applicazione OAuth2 in Jira.

## Collegare Jira a Workfront Fusion

La procedura per la creazione di una connessione a Jira varia a seconda che si stia creando una connessione di base o una connessione OAuth2.

* [Creare una connessione OAuth2 a Jira](#create-an-oauth2-connection-to-jira)
* [Creare una connessione di base a Jira](#create-a-basic-connection-to-jira)

### Creare una connessione OAuth2 a Jira

Per creare una connessione OAuth2 a Jira, è necessario creare un’applicazione in Jira prima di poter configurare la connessione in Fusion.

* [Creare un’applicazione OAuth2 in Jira](#create-an-oauth2-application-in-jira)
* [Configurare la connessione OAuth2 in Fusion](#configure-the-oauth2-connection-in-fusion)

#### Creare un’applicazione OAuth2 in Jira

>[!IMPORTANT]
>
>Devi avere accesso a Jira Developer Console per creare e configurare un’applicazione OAuth2 per la tua connessione Jira.

1. Vai a [Jira Developer Console](https://developer.atlassian.com/console.myapps/).
1. Nell&#39;area Le mie app, fai clic su **Crea**, quindi seleziona **Integrazione OAuth 2.0**.
1. Immetti un nome per l&#39;integrazione, accetta i termini dello sviluppatore e fai clic su **Crea**.

   L’applicazione viene creata e viene visualizzata l’area di configurazione dell’applicazione.
1. Fai clic su **Autorizzazioni** nel pannello di navigazione a sinistra.
1. Nell&#39;area Autorizzazioni, individuare la riga **Jira API**.
1. Fai clic su **Aggiungi** nella riga Jira API, quindi fai clic su **Continua** nella stessa riga.
1. Abilita i seguenti ambiti:

   * Visualizza dati problema Jira (`read:jira-work`)
   * Visualizza profili utente (`read:jira-user`)
   * Crea e gestisci i problemi (`write:jira-work`)

1. Nel menu di navigazione a sinistra, fai clic su **Autorizzazione**.
1. Fai clic su **Aggiungi** nella riga per l&#39;autorizzazione OAuth 2.0.
1. Nel campo **URL callback**, immettere uno dei seguenti URL, in base al data center di Workfront Fusion:

   | Datacenter di Fusion | URL di callback |
   |---|---|
   | STATI UNITI | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |

1. Nel menu di navigazione a sinistra, fai clic su **Impostazioni**.
1. (Facoltativo) Immetti una descrizione nel campo Descrizione e fai clic su **Salva modifiche** sotto tale campo.
1. Copiare l&#39;ID client e il segreto client dall&#39;area Impostazioni in una posizione sicura oppure lasciare aperta questa pagina durante la configurazione della connessione in Fusion.
1. Continua con [Configurare la connessione OAutt2 in Fusion](#configure-the-oauth2-connection-in-fusion)

#### Configurare la connessione OAuth2 in Fusion

1. In qualsiasi modulo Jira, fai clic su **Aggiungi** accanto al campo Connessione.
1. Configura i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Tipo di connessione</p> </td> 
      <td> <p>Selezionare <b>OAuth 2</b>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nome connessione</p> </td> 
      <td> <p>Inserisci un nome per la nuova connessione.</p> </td> 
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
      <td> <p>Immettere l'ID client dell'applicazione Jira creata in <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">Creare un'applicazione OAuth2 in Jira</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Segreto client</td> 
      <td> <p>Immettere il segreto client dell'applicazione Jira creata in <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">Creare un'applicazione OAuth2 in Jira</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Ambiti aggiuntivi</td> 
      <td>Immettere gli ambiti aggiuntivi che si desidera aggiungere alla connessione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Versione API</td> 
      <td>Seleziona la versione API Jira a cui vuoi connettere la connessione.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

### Creare una connessione di base a Jira

La creazione di una connessione di base a Jira varia a seconda che si crei una connessione a Jira Cloud o al centro dati Jira.

* [Creare una connessione di base a Jira Cloud](#create-a-basic-connection-to-jira-cloud)
* [Creare una connessione di base al centro dati Jira](#create-a-basic-connection-to-jira-data-center)

#### Creare una connessione di base a Jira Cloud

>[!IMPORTANT]
>
> Per creare una connessione di base a Jira Cloud, è necessario disporre di un token API Jira.
>Per istruzioni sull&#39;acquisizione di un token Jira API, consulta [Gestire i token API per il tuo account Atlassian](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account) nella documentazione di Atlassian.


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
      <td> <p>Inserisci un nome per la nuova connessione.</p> </td> 
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
      <td role="rowheader">E-mail</td> 
      <td>Inserisci il tuo indirizzo e-mail.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token API</td> 
      <td>Immetti il token API.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Versione API</td> 
      <td>Seleziona la versione API Jira a cui vuoi connettere la connessione.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

#### Creare una connessione di base al centro dati Jira

>[!IMPORTANT]
>
> Per creare una connessione di base al centro dati Jira, è necessario disporre di un token di accesso personale Jira (PAT).
>Per istruzioni sull&#39;acquisizione di un token di accesso personale Jira, consulta [Gestire i token API per il tuo account Atlassian](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) nella documentazione di Atlassian.
>Per considerazioni sulla creazione del PAT, vedere [Configurare il PAT](#configure-your-pat) in questo articolo.

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
      <td> <p>Inserisci un nome per la nuova connessione.</p> </td> 
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
      <td role="rowheader">PAT (token di accesso personale)</td> 
      <td>Inserisci il token di accesso personale Jira.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Versione API</td> 
      <td>Seleziona la versione API Jira a cui vuoi connettere la connessione.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

##### Configurare il PAT

Per creare una connessione di base al centro dati Jira, è necessario disporre di un token di accesso personale Jira (PAT).

Per istruzioni sull&#39;acquisizione di un token di accesso personale Jira, consulta [Gestire i token API per il tuo account Atlassian](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) nella documentazione di Atlassian.

Durante la configurazione del PAT potrebbero essere necessarie le seguenti informazioni

* URL di reindirizzamento

  | Datacenter di Fusion | Reindirizza URL |
  |---|---|
  | STATI UNITI | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

* Configurazioni file

Per utilizzare un PAT, è necessario abilitare quanto segue nei file `jira/bin/WEB-INF/classes`, nel file `jira-config.properties`:

* `jira.rest.auth.allow.basic = true`
* `jira.rest.csrf.disabled = true`

Se il file non esiste, è necessario crearlo.

## Moduli Jira e relativi campi

Quando configuri i moduli Jira, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi Jira aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTPS</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Intestazioni</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stringa query</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> in JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
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

>[!IMPORTANT]
>
>Il modulo di ricerca utilizzato dal connettore Jira legacy può causare il seguente errore:
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>Ciò è dovuto a una deprecazione da parte di Jira.
>
>Se si verifica questo errore, è possibile sostituire il modulo di ricerca del connettore Jira legacy con il modulo di ricerca del nuovo connettore. Il nuovo connettore consente di selezionare la versione API utilizzata. Assicurati di selezionare V3 durante la creazione della connessione.
>
> ![Opzione di versione API nel nuovo connettore Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>Tieni presente che:
>
>* È interessato solo il modulo di ricerca. Al momento, altri endpoint API Jira utilizzati dal connettore Fusion non sono interessati da questa rimozione.
>
>* Il rollout geografico può causare incongruenze. Atlassian sta implementando questa modifica a livello regionale, il che significa che alcune istanze di Jira Cloud potrebbero ancora supportare temporaneamente gli endpoint precedenti. Questo può causare comportamenti non coerenti tra gli ambienti.

#### Cerca record

Questo modulo di ricerca cerca i record in un oggetto in Jira che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

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
