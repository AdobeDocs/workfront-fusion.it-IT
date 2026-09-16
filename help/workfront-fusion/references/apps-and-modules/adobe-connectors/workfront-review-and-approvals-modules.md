---
title: Moduli Contenuto e approvazioni di Adobe Workfront
description: Con i moduli Contenuto e approvazioni di Adobe Workfront puoi ottenere i dettagli di approvazione, prendere una decisione su una risorsa, aggiungere o eliminare partecipanti all’approvazione, aggiungere o aggiornare fasi di approvazione, bloccare o sbloccare e effettuare chiamate API personalizzate.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4f637dcb9d7865f73b41faa5b0acf397944bb559
workflow-type: tm+mt
source-wordcount: '5202'
ht-degree: 11%
---
# Moduli di revisione e approvazione unificate di Adobe Workfront

Con i moduli Revisione e approvazioni unificate di Adobe Workfront, puoi ottenere i dettagli di approvazione, prendere una decisione su una risorsa, aggiungere o eliminare partecipanti all’approvazione, aggiungere o aggiornare fasi di approvazione, bloccare o sbloccare e effettuare chiamate API personalizzate.

Per informazioni sulla revisione e le approvazioni unificate di Workfront, vedere [Panoramica sulla revisione e l&#39;approvazione unificate](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview) nella documentazione di Workfront.

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

Per accedere al contenuto e alle approvazioni di Workfront è necessario disporre dei seguenti elementi:

* È necessaria una versione di Workfront che supporti l’archiviazione cloud di Adobe. Se la tua organizzazione non utilizza già una versione supportata, contatta il rappresentante del tuo account Adobe.

## Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront


1. In qualsiasi modulo Adobe Workfront Unified Review and Approvals, fai clic su **Aggiungi** accanto al campo Connessione.
1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
        <td>
          <p>Seleziona <b>Connessione da server a server Adobe Workfront</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Inserisci un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Nome istanza]</td>
        <td>
          <p>Inserisci i il nome dell’istanza, noto anche come dominio.</p><p>Esempio: se l’URL è <code>https://example.my.workfront.com</code>, inserisci <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Percorso dell’istanza]</td>
        <td>
          <p>Inserisci il tipo di ambiente della connessione.</p><p>Esempio: se l’URL è <code>https://example.my.workfront.com</code>, inserisci <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Inserisci il tuo ID client. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Apri l’applicazione specifica a cui ti stai connettendo per visualizzare l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il Segreto client di Workfront. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Se non disponi di un Segreto client per l’applicazione OAuth2 in Workfront, puoi generarne un altro. Per istruzioni, consulta la documentazione di Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiti]</td>
        <td>Inserisci gli ambiti applicabili per questa connessione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Prefisso host]</td>
        <td>Nella maggior parte dei casi, questo valore deve essere <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

   Se non hai effettuato l’accesso a Revisione e approvazioni unificate di Workfront, vieni indirizzato a una schermata di accesso. Dopo aver effettuato l’accesso, puoi autorizzare la connessione.

## Moduli di revisione e approvazione unificate di Adobe Workfront

Quando configuri i moduli di Workfront, Workfront Fusion mostra i campi elencati di seguito. Oltre a questi campi potrebbero essere mostrati campi di Workfront aggiuntivi, in base a fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Ricerche](#searches)
* [Altro](#other)

### Azioni

* [Aggiungi o aggiorna partecipanti](#add-or-update-participants)
* [Modelli di eliminazione in blocco](#bulk-delete-templates)
* [Creare un modello](#create-a-template)
* [Crea approvazione raggruppata](#create-grouped-approval)
* [Creare le fasi](#create-stages)
* [Bloccare una fase](#lock-a-stage)
* [Prendi una decisione](#make-a-decision)
* [Prendere una decisione su una fase](#make-a-decision-on-a-stage)
* [Gestire le risorse con un’approvazione raggruppata](#manage-assets-on-a-grouped-approval)
* [Gestire i partecipanti alla fase](#manage-stage-participants)
* [Gestire le fasi di un’approvazione raggruppata](#manage-stages-on-a-grouped-approval)
* [Ricordare a un partecipante su un palco](#remind-a-participant-on-a-stage)
* [Ricorda partecipante](#remind-participant)
* [Promemoria ai partecipanti indecisi](#remind-undecided-participants)
* [Ricordare i partecipanti indecisi su un palco](#remind-undecided-participants-on-a-stage)
* [Sblocca una fase](#unlock-a-stage)
* [Aggiornare una fase](#update-a-stage)
* [Aggiornare un modello](#update-a-template)
* [Aggiorna tutte le fasi](#update-all-stages)
* [Aggiorna approvazione raggruppata (stato completo)](#update-grouped-approval-full-state)


#### Aggiungi o aggiorna partecipanti

Questo modulo di azione aggiunge o aggiorna i partecipanti nella fase predefinita di un’approvazione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>ID Documento</p>
      </td>
      <td>Inserisci o mappa l’ID della risorsa per la quale desideri aggiungere o aggiornare un partecipante.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Aggiungere partecipanti alle fasi</p>
      </td>
      <td>Per ogni fase a cui si desidera aggiungere partecipanti, fare clic su <b>Aggiungi elemento</b> e immettere la fase.<p> Quindi, per ogni partecipante che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del partecipante.</p>
      <ul>
      <li><b>ID partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Tipo di partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Ruolo partecipante</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### Modelli di eliminazione in blocco

Questo modulo elimina i modelli di approvazione specificati.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID modello</p></td>
      <td>Per ogni modello da eliminare, fare clic su <b>Aggiungi elemento</b> e immettere l'ID del modello.</td> 
      </tr>
  </tbody>
</table>

#### Creare un modello

Questo modulo crea un modello di approvazione

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Immettere o mappare un nome per il modello.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID azienda</p></td>
      <td>Se si desidera aggiungere un ambito società al modello, immettere o mappare l'ID società.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Fasi</p>
      </td>
      <td>Per ogni fase che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dati dell'area di visualizzazione.<p>Per informazioni specifiche, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Condiviso con</p></td>
      <td>Per ogni utente con cui vuoi condividere il modello, fai clic su <b>Aggiungi elemento</b> e ID utente, quindi fai clic sul livello di accesso desiderato.</td> 
      </tr>
  </tbody>
</table>

#### Crea approvazione raggruppata

Questo modulo di azione crea un’approvazione raggruppata: un insieme di versioni di documenti che si spostano insieme attraverso uno o più percorsi di approvazione, ognuno dei quali è una sequenza ordinata di fasi con i propri partecipanti.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Inserisci o mappa un nome visualizzato per l’approvazione raggruppata. Il nome deve contenere tra 1 e 255 caratteri.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Risorse</p></td>
      <td>Per ogni versione del documento che si desidera includere nel gruppo, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della versione del documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Percorsi</p></td>
      <td>Per ogni percorso di approvazione che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere l'ID percorso, il nome e le fasi. Ogni percorso contiene una sequenza ordinata di stadi. Per ogni fase, nel campo Stadi, fare clic su <b>Aggiungi elemento</b> e immettere i dati seguenti:
      <ul>
      <li><b>ID fase</b><p>Inserisci un identificatore assegnato dal client per la fase, univoco per tutti i percorsi. Deve essere alfanumerico, con sottolineature o trattini consentiti e non più di 64 caratteri.</p></li>
      <li><b>Nome fase</b><p>Immettere o mappare un nome per l'area di visualizzazione.</p></li>
      <li><b>ID fase padre</b><p>Per ogni fase padre che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere l'ID padre.</p></li>
      <li><b>Partecipanti</b><p>Per ogni partecipante che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del partecipante.
      <ul>
      <li><b>ID partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Tipo di partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Ruolo partecipante</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul>
      </p></li>
      <li><b>Data di scadenza</b><p>Se la scadenza è una data specifica, inserirla o eseguirne il mapping.</p></li>
      <li><b>Giorni Lavorativi Fino Alla Scadenza</b><p>Se la scadenza è successiva a un numero specifico di giorni lavorativi, immettere o mappare il numero di giorni.</p></li>
      <li><b>Scadenza: ore</b><p>Immetti o mappa l’ora del giorno per la scadenza (0-23). Coppia con data di scadenza: minuti.</p></li>
      <li><b>Scadenza: minuti</b><p>Immetti o mappa il minuto dell’ora per la scadenza (0-59). Coppia con data di scadenza: ore.</p></li>
      <li><b>Messaggio personalizzato</b><p>Inserisci o mappa un messaggio personalizzato per l’area di visualizzazione.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID oggetto principale</p></td>
      <td>Immettere o mappare l'ID dell'oggetto padre di Workfront, ad esempio un progetto o un task, che si desidera associare all'approvazione raggruppata. Se si utilizza questo campo, è necessario immettere anche il codice oggetto.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Codice oggetto</p></td>
      <td>Immettere o mappare il codice del tipo di oggetto Workfront per l'oggetto padre, ad esempio <code>PROJ</code> o <code>TASK</code>. Obbligatorio se si immette un ID oggetto padre.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID modello</p></td>
      <td>(Facoltativo) Inserisci o mappa un ID modello da registrare sull’approvazione raggruppata per la tracciabilità.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Creare le fasi

Questo modulo di azione crea un’approvazione con i dati della fase specificati.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri creare o aggiornare una fase.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Fasi</p>
      </td>
      <td>Per ogni fase che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dati dell'area di visualizzazione.<p>Per informazioni specifiche, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID modello</p></td>
      <td>Inserisci o mappa l’ID del cespite per il quale desideri creare delle fasi.</td> 
      </tr>
  </tbody>
</table>

<!--
BECKY CHECK ME: The following block of Delete-prefixed Actions modules (Delete a decision on a stage, Delete a stage, Delete a template, Delete an approval, Delete decisions, Delete grouped approval, Delete participants) is not confirmed to be current in the live connector as of this update - status uncertain. Commented out for now; restore (and remove this comment) once confirmed, or delete for good if confirmed removed.

#### Delete a decision on a stage

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
   </tbody>
</table>


#### Delete a stage

This action module deletes the specified stage from the approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a stage from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete a template

This module deletes the specified approval template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete an approval

This action module deletes the approval for the given document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete an approval from.</td> 
      </tr>
  </tbody>
</table>

#### Delete decisions

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
  </tbody>
</table>

#### Delete grouped approval

This action module deletes a grouped approval, cascading to its child asset approvals and paths.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Group GUID</p></td>
      <td>Enter or map the GUID of the grouped approval that you want to delete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limit</p></td>
      <td>Enter or map the maximum number of results you want the module to work with during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>
-->

#### Bloccare una fase

Questo modulo di azione blocca la fase di approvazione specificata e imposta la fase su inattiva.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa da bloccare.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID fase</p>
      </td>
      <td>Inserisci o mappa l’ID della fase che desideri bloccare.</td> 
      </tr>
  </tbody>
</table>

#### Prendi una decisione

Questo modulo di azione applica una decisione a una fase di approvazione o approvazione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa da bloccare.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Decisione</p></td>
      <td>Seleziona la decisione da applicare all’approvazione o alla fase.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID fase</p>
      </td>
      <td>Per ogni fase a cui si desidera applicare la decisione, fare clic su <b>Aggiungi elemento</b> e immettere l'ID fase.</td> 
      </tr>
  </tbody>
</table>

#### Prendere una decisione su una fase

Questo modulo applica una decisione alla fase specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID del documento su cui desideri prendere una decisione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Inserisci o mappa l’ID della fase su cui desideri prendere una decisione.</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Decisione</p></td>
      <td>Seleziona la decisione da applicare a questa fase.</td> 
      </tr>
  </tbody>
</table>

#### Gestire le risorse con un’approvazione raggruppata

Questo modulo di azione aggiunge e/o rimuove versioni di documenti in un’approvazione raggruppata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID approvazione raggruppata</p></td>
      <td>Immetti o mappa il GUID dell’approvazione raggruppata su cui desideri gestire le risorse.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Aggiungi Assets</p></td>
      <td>Per ogni versione del documento che si desidera aggiungere al gruppo, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della versione del documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Rimuovi Assets</p></td>
      <td>Per ogni versione del documento che si desidera rimuovere dal gruppo, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della versione del documento (DOCV).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Gestire i partecipanti alla fase

Questo modulo di azione aggiunge, aggiorna e/o rimuove partecipanti in una fase specifica di un’approvazione raggruppata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID approvazione raggruppata</p></td>
      <td>Immetti o mappa il GUID dell’approvazione raggruppata.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Immettere o mappare l'ID della fase su cui si desidera gestire i partecipanti.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Aggiungi partecipanti</p></td>
      <td>Per ogni partecipante che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli seguenti:
      <ul>
      <li><b>Tipo partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Ruolo</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Aggiorna partecipanti</p></td>
      <td>Per ogni partecipante che si desidera aggiornare nell'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli seguenti:
      <ul>
      <li><b>Tipo partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Ruolo</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Rimuovi partecipanti</p></td>
      <td>Per ogni partecipante che si desidera rimuovere dall'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli seguenti:
      <ul>
      <li><b>Tipo partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Gestire le fasi di un’approvazione raggruppata

Questo modulo di azione aggiunge, aggiorna e/o rimuove fasi in un’approvazione raggruppata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID approvazione raggruppata</p></td>
      <td>Immetti o mappa il GUID dell’approvazione raggruppata.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Aggiungi fasi</p></td>
      <td>Per ogni fase che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli seguenti:
      <ul>
      <li><b>ID fase</b><p>Immettere o mappare un identificatore per la fase.</p></li>
      <li><b>Nome fase</b><p>Immettere o mappare un nome per l'area di visualizzazione.</p></li>
      <li><b>Data di scadenza</b><p>Se la scadenza è una data specifica, inserirla o eseguirne il mapping.</p></li>
      <li><b>Giorni Lavorativi Fino Alla Scadenza</b><p>Se la scadenza è successiva a un numero specifico di giorni lavorativi, immettere o mappare il numero di giorni.</p></li>
      <li><b>Messaggio personalizzato</b><p>Inserisci o mappa un messaggio personalizzato per l’area di visualizzazione.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Aggiorna fasi</p></td>
      <td>Per ogni fase che si desidera aggiornare, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli seguenti:
      <ul>
      <li><b>ID fase</b><p>Inserisci o mappa l’ID della fase da aggiornare.</p></li>
      <li><b>Nome fase</b><p>Immettere o mappare un nome per l'area di visualizzazione.</p></li>
      <li><b>Data di scadenza</b><p>Se la scadenza è una data specifica, inserirla o eseguirne il mapping.</p></li>
      <li><b>Giorni Lavorativi Fino Alla Scadenza</b><p>Se la scadenza è successiva a un numero specifico di giorni lavorativi, immettere o mappare il numero di giorni.</p></li>
      <li><b>Messaggio personalizzato</b><p>Inserisci o mappa un messaggio personalizzato per l’area di visualizzazione.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Rimuovi fasi</p></td>
      <td>Per ogni fase che si desidera rimuovere, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della fase.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Ricordare a un partecipante su un palco

Questo modulo invia un promemoria a un partecipante specifico in una fase specifica.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri inviare un promemoria.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID fase</p>
      </td>
      <td>Inserisci o mappa l’ID della fase a cui desideri inviare un promemoria.</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID partecipante</p></td>
      <td>Inserisci o mappa l’ID del partecipante a cui vuoi inviare un promemoria.</td> 
      </tr>
  </tbody>
</table>

#### Ricorda partecipante

Questo modulo invia una notifica di promemoria al partecipante specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri inviare un promemoria.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID partecipante</p>
      </td>
      <td>Inserisci o mappa l’ID del partecipante a cui vuoi inviare il promemoria.</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>Tipo di partecipante</p>
      </td>
      <td>Immettere o mappare il tipo di partecipante a cui si desidera inviare il promemoria.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Ruolo partecipante</p>
      </td>
      <td>Immetti o mappa il ruolo del partecipante a cui desideri inviare il promemoria.</td> 
      </tr>
  </tbody>
</table>

#### Promemoria ai partecipanti indecisi

Questo modulo invia notifiche di promemoria a tutti i partecipanti indecisi per l’approvazione specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri inviare un promemoria.</td> 
      </tr>
  </tbody>
</table>

#### Ricordare i partecipanti indecisi su un palco

Questo modulo invia notifiche di promemoria a tutti i partecipanti indecisi su una fase.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri inviare un promemoria.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID fase</p>
      </td>
      <td>Inserisci o mappa l’ID della fase a cui desideri inviare un promemoria.</td> 
      </tr>
  </tbody>
</table>

#### Sblocca una fase

Questo modulo consente di sbloccare la fase di approvazione specificata e di impostarla su attiva.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID della risorsa da sbloccare.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID fase</p>
      </td>
      <td>Inserisci o mappa l’ID della fase che desideri bloccare.</td> 
      </tr>
  </tbody>
</table>


#### Aggiornare una fase

Questo modulo di azione aggiorna i campi nella fase specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID del documento su cui desideri prendere una decisione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Inserisci o mappa l’ID della fase su cui desideri prendere una decisione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nome fase</p></td>
      <td>Immettere o mappare un nome per il modello.</td> 
      </tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Immettere i dati nei campi dell'area di visualizzazione.<p>Per ulteriori informazioni, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Condiviso con</p></td>
      <td>Per ogni utente con cui vuoi condividere il modello, fai clic su <b>Aggiungi elemento</b> e ID utente, quindi fai clic sul livello di accesso desiderato.</td> 
      </tr>
  </tbody>
</table>

#### Aggiornare un modello

Questo modulo aggiorna i campi del modello di approvazione specificato.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID modello</p></td>
      <td>Immettere o mappare un nome per il modello.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Inserisci o mappa l’ID del modello da aggiornare.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID azienda</p></td>
      <td>Se si desidera aggiungere un ambito società al modello, immettere o mappare l'ID società.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Fasi</p>
      </td>
      <td>Per ogni fase che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dati dell'area di visualizzazione.<p>Per informazioni specifiche, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Condiviso con</p></td>
      <td>Per ogni utente con cui vuoi condividere il modello, fai clic su <b>Aggiungi elemento</b> e ID utente, quindi fai clic sul livello di accesso desiderato.</td> 
      </tr>
  </tbody>
</table>

#### Aggiorna tutte le fasi

Questo modulo sostituisce tutte le fasi di un’approvazione esistente con i dati della fase specificata. Il documento deve essere in uno stato modificabile.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Inserisci o mappa l’ID del cespite per il quale desideri aggiornare le fasi.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Fasi</p>
      </td>
      <td>Per ogni fase da aggiornare, fare clic su <b>Aggiungi elemento</b> e immettere i dati dell'area di visualizzazione.<p>Per informazioni specifiche, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
  </tbody>
</table>

#### Aggiorna approvazione raggruppata (stato completo)

Questo modulo di azione applica un aggiornamento completo a un’approvazione raggruppata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID approvazione raggruppata</p></td>
      <td>Immetti o mappa il GUID dell’approvazione raggruppata che desideri aggiornare. Ad esempio, <code>9f8b60820000462ecf66c409d1248fa9</code>.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Percorsi</p></td>
      <td>Per ogni percorso di approvazione che si desidera assegnare all'approvazione raggruppata, fare clic su <b>Aggiungi elemento</b> e immettere l'ID percorso, il nome e le fasi. Fusion esegue la riconciliazione dello stato corrente, aggiungendo, aggiornando e rimuovendo i percorsi in modo che corrispondano a quelli inviati. Ogni percorso contiene una sequenza ordinata di stadi. Per ogni fase, nel campo Stadi, fare clic su <b>Aggiungi elemento</b> e immettere i dati seguenti:
      <ul>
      <li><b>ID fase</b><p>Inserisci un identificatore assegnato dal client per la fase, univoco per tutti i percorsi. Deve essere alfanumerico, con sottolineature o trattini consentiti e non più di 64 caratteri.</p></li>
      <li><b>Nome fase</b><p>Immettere o mappare un nome per l'area di visualizzazione.</p></li>
      <li><b>ID fase padre</b><p>Per ogni fase padre che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere l'ID padre.</p></li>
      <li><b>Partecipanti</b><p>Per ogni partecipante che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del partecipante.
      <ul>
      <li><b>ID partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Tipo di partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Ruolo partecipante</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul>
      </p></li>
      <li><b>Data di scadenza</b><p>Se la scadenza è una data specifica, inserirla o eseguirne il mapping.</p></li>
      <li><b>Giorni Lavorativi Fino Alla Scadenza</b><p>Se la scadenza è successiva a un numero specifico di giorni lavorativi, immettere o mappare il numero di giorni.</p></li>
      <li><b>Scadenza: ore</b><p>Immetti o mappa l’ora del giorno per la scadenza (0-23). Coppia con data di scadenza: minuti.</p></li>
      <li><b>Scadenza: minuti</b><p>Immetti o mappa il minuto dell’ora per la scadenza (0-59). Coppia con data di scadenza: ore.</p></li>
      <li><b>Messaggio personalizzato</b><p>Inserisci o mappa un messaggio personalizzato per l’area di visualizzazione.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Risorse</p></td>
      <td>(Facoltativo) Per ogni versione del documento che si desidera includere nel gruppo, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della versione del documento (DOCV). Se ometti questo campo, le risorse correnti vengono lasciate invariate.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Chiave Idempotenza</p></td>
      <td>(Facoltativo) Inserisci o mappa una chiave fornita dal client (massimo 128 caratteri) che rende sicura una richiesta ritentata. Se invii nuovamente la stessa chiave, il modulo non applica l’aggiornamento una seconda volta.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

### Ricerche

* [Ottieni un modello](#get-a-template)
* [Ottieni dettagli approvazione](#get-approval-details)
* [Ottenere approvazioni in un’approvazione raggruppata](#get-approvals-in-a-grouped-approval)
* [Ottieni dettagli approvazione raggruppati](#get-grouped-approval-details)
* [Ottenere più approvazioni](#get-multiple-approvals)
* [Ottieni approvazioni suggerite](#get-suggested-approvals)
* [Ottieni partecipanti suggeriti](#get-suggested-participants)
* [Elenca bot](#list-bots)
* [Elenca approvazioni raggruppate per elemento padre](#list-grouped-approvals-by-parent)
* [Modelli di elenco](#list-templates)
* [Ricerca in base alle recensioni del brand AI](#search-ai-brand-reviews)
* [Cerca approvazioni raggruppate](#search-grouped-approvals)


#### Ottieni un modello

Questo modulo restituisce il modello di approvazione specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID modello</p></td>
      <td>Immetti o mappa l’ID del documento per il quale desideri ottenere i partecipanti di approvazione suggeriti.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di modelli restituiti
         </td>
         <td>
              Immettere o mappare il numero massimo di modelli che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Ottieni dettagli approvazione

Questo modulo di ricerca recupera i dettagli di approvazione di una risorsa.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Documento</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri recuperare i dettagli di approvazione.</td> 
      </tr>
  </tbody>
</table>

#### Ottenere approvazioni in un’approvazione raggruppata

Questo modulo di ricerca restituisce le singole approvazioni di risorse che compongono un’approvazione raggruppata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>GUID gruppo</p></td>
      <td>Immetti o mappa il GUID dell'approvazione raggruppata per la quale desideri ottenere le approvazioni.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Dati versione documento</p></td>
      <td>Selezionare se allegare il record documentVersion Redrock all'approvazione di ogni versione del documento (DOCV). </td>
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Ottieni dettagli approvazione raggruppati

Questo modulo di ricerca restituisce un’approvazione raggruppata in base al relativo GUID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>GUID gruppo</p></td>
      <td>Immetti o mappa il GUID dell’approvazione raggruppata per la quale desideri ottenere i dettagli.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Ottenere più approvazioni

Questo modulo recupera i dettagli delle approvazioni per un elenco di documenti di un tipo specifico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID documento</p></td>
      <td>Per ogni documento per cui si desidera recuperare i dettagli di approvazione, fare clic su <b>Aggiungi elemento</b> e immettere l'ID del documento.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di risultati restituiti
         </td>
         <td>
              Immettere o mappare il numero massimo di risultati che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Ottieni approvazioni suggerite

Questo modulo restituisce i payload di approvazione consigliati da versioni di documenti precedenti.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID del documento per il quale desideri ricevere le approvazioni suggerite.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di approvazioni restituite
         </td>
         <td>
              Immettere o mappare il numero massimo di approvazioni che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Ottieni partecipanti suggeriti

Questo modulo restituisce i suggerimenti dei partecipanti dall&#39;approvazione per l&#39;approvazione del documento precedente.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Documento</p></td>
      <td>Immetti o mappa l’ID del documento per il quale desideri ottenere i partecipanti di approvazione suggeriti.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di partecipanti restituiti
         </td>
         <td>
              Immettere o mappare il numero massimo di partecipanti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Elenca bot

Questo modulo restituisce un elenco impaginato di account bot.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Pagina</p></td>
      <td>Immettere o mappare la pagina dei risultati che si desidera restituire.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di risultati restituiti
         </td>
         <td>
              Immettere o mappare il numero massimo di risultati che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Elenca approvazioni raggruppate per elemento padre

Questo modulo di ricerca restituisce le approvazioni raggruppate associate a un oggetto padre di Workfront.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Genitore</p></td>
      <td>Immetti o mappa l’ID dell’oggetto principale di Workfront (ad esempio, un progetto o un’attività) per il quale desideri ottenere approvazioni raggruppate.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Codice oggetto</p></td>
      <td>(Facoltativo) Immettere o mappare il codice del tipo di oggetto Workfront per l'oggetto padre, ad esempio <code>PROJ</code> o <code>TASK</code>.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

#### Modelli di elenco

Questo modulo restituisce un elenco di tutti i modelli di approvazione disponibili per l’utente corrente. L&#39;utente corrente è l&#39;utente le cui credenziali vengono utilizzate nella connessione utilizzata in questo modulo.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
   </tbody>
</table>

#### Ricerca in base alle recensioni del brand AI

Questo modulo restituisce i risultati della revisione del marchio AI prodotti per una versione del documento come parte di un’approvazione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID utente bot</p></td>
      <td>Immetti o mappa l’ID utente del bot per il quale desideri cercare le recensioni.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID documento principale</p></td>
      <td>Immettere o mappare l'ID del documento principale per il quale si desidera eseguire la ricerca delle revisioni.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID versione documento</p></td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri inviare un promemoria.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Immetti o mappa un ID fase per limitare i risultati a una fase specifica dell'approvazione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Pagina</p></td>
      <td>Immetti o mappa un numero di pagina per limitare i risultati a tale pagina.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Numero massimo di recensioni restituite
         </td>
         <td>
              Immettere o mappare il numero massimo di revisioni che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
  </tbody>
</table>

#### Cerca approvazioni raggruppate

Questo modulo di ricerca cerca le approvazioni raggruppate utilizzando una vista denominata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Visualizzazione</p></td>
      <td>(Facoltativo) Seleziona o mappa la vista denominata che determina la forma della risposta. Attualmente, sono supportate solo le approvazioni in attesa di approvazione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>(Facoltativo) Immetti o mappa le dimensioni della pagina per la prima pagina dei risultati. Il valore massimo è 100 e quello predefinito è 20.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Cursore</p></td>
      <td>(Facoltativo) Inserisci o mappa il cursore opaco da una risposta precedente, per recuperare la pagina successiva dei risultati. Se si fornisce un cursore, il modulo ignora il campo Limite.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID team</p></td>
      <td>(Facoltativo) Per ogni team a cui si desidera associare anche le approvazioni raggruppate (di cui il team è un partecipante), fare clic su <b>Aggiungi elemento</b> e immettere l'ID team.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limite</p></td>
      <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: the screenshot shows two separate fields both labeled "Limit" - an optional pagination page-size field (max 100, default 20, ignored if Cursor is set) and a required general execution-cycle limit, matching the Limit field used in every other module in this article. Confirm this isn't a UI labeling issue before publishing, and that both rows are needed/correctly distinguished. -->

### Altro

* [Effettua chiamata API personalizzata](#make-a-custom-api-call)
* [Campi delle fasi](#stages-fields)


#### Effettua chiamata API personalizzata

Questo modulo effettua una chiamata API personalizzata all’API Adobe Workfront Unified Review and Approvals.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Percorso relativo</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://workfront.adobe.io</code>. Ad esempio: <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Metodo</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Intestazioni</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stringa di query]  </td>
      <td>
        <p>Per ogni coppia chiave/valore che si desidera aggiungere alla stringa di query, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



#### Campi delle fasi

I campi seguenti sono disponibili durante la configurazione delle fasi. È possibile che non tutti i campi siano disponibili per tutti i moduli.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Nome fase</td>
      <td>Immettere o mappare un nome per l'area di visualizzazione.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Data di scadenza</p></td>
      <td>Se la scadenza è una data specifica, inserirla o eseguirne il mapping.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>Giorni lavorativi di scadenza</p></td>
      <td>Se la scadenza è successiva a un numero specifico di giorni lavorativi, immettere o mappare il numero di giorni.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Scadenza</p></td>
      <td>Se la scadenza è un’ora specifica, inserisci o mappa l’ora.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Partecipanti</p></td>
      <td>Per ogni partecipante che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del partecipante.      
      <ul>
      <li><b>ID partecipante</b><p>Inserisci o mappa l’ID del partecipante.</p></li>
      <li><b>Tipo di partecipante</b><p>Seleziona se il partecipante è un utente o un team.</p></li>
      <li><b>Ruolo partecipante</b><p>Specificare se il partecipante è un approvatore o un revisore.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Blocco automatico abilitato</p></td>
      <td>Specificare se si desidera bloccare automaticamente l'area di visualizzazione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Regole di decisione</p></td>
      <td>Seleziona se desideri richiedere una sola decisione per la fase.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID padre/ID fase padre</p></td>
      <td>Per ogni fase padre che si desidera aggiungere all'area di visualizzazione, fare clic su <b>Aggiungi elemento</b> e immettere l'ID padre.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Trigger</p></td>
      <td>Per configurare un trigger per questa fase di approvazione, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del trigger.      <ul>
      <li><b>Tipo</b><p>Seleziona <b>Attivazione</b></p></li>
      <li><b>Quando</b><p>Seleziona se attivare la fase al momento della creazione dell’approvazione o al completamento di un’altra fase.</p></li>
      <li><b>Fasi</b><p>Per ogni fase che si desidera aggiungere al trigger, fare clic su <b>Aggiungi elemento</b> e immettere o mappare l'ID fase.</p></li>
      <li><b>Decisioni</b><p>Per ogni decisione che desideri aggiungere al trigger, fai clic su <b>Aggiungi elemento</b> e immetti o mappa la decisione.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Messaggio personalizzato</p></td>
      <td>Inserisci o mappa un messaggio personalizzato per l’area di visualizzazione.</td> 
      </tr>
</table>
