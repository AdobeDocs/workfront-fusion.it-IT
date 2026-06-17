---
title: Moduli Contenuto e approvazioni di Adobe Workfront
description: Con i moduli Contenuto e approvazioni di Adobe Workfront puoi ottenere i dettagli di approvazione, prendere una decisione su una risorsa, aggiungere o eliminare partecipanti all’approvazione, aggiungere o aggiornare fasi di approvazione, bloccare o sbloccare e effettuare chiamate API personalizzate.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: e9ea91840c9be594e98b97202cb46dfa009349a9
workflow-type: tm+mt
source-wordcount: 3743
ht-degree: 15%

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

1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.

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
* [Creare un’approvazione](#create-an-approval)
* [Creare le fasi](#create-stages)
* [Eliminare una decisione in una fase](#delete-a-decision-on-a-stage)
* [Eliminare una fase](#delete-a-stage)
* [Eliminare un modello](#delete-a-template)
* [Eliminare un’approvazione](#delete-an-approval)
* [Elimina decisioni](#delete-decisions)
* [Elimina partecipanti](#delete-participants)
* [Bloccare una fase](#lock-a-stage)
* [Prendi una decisione](#make-a-decision)
* [Prendere una decisione su una fase](#make-a-decision-on-a-stage)
* [Ricordare a un partecipante su un palco](#remind-a-participant-on-a-stage)
* [Ricorda partecipante](#remind-participant)
* [Promemoria ai partecipanti indecisi](#remind-undecided-participants)
* [Ricordare i partecipanti indecisi su un palco](#remind-undecided-participants-on-a-stage)
* [Sblocca una fase](#unlock-a-stage)
* [Aggiornare una fase](#update-a-stage)
* [Aggiornare un modello](#update-a-template)
* [Aggiorna tutte le fasi](#update-all-stages)


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
      <td role="rowheader"><p>ID Azienda</p></td>
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

#### Creare un’approvazione

Questo modulo di azione crea un’approvazione per un documento sull’archiviazione cloud Adobe, inclusi i dati di staging o un modello.

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
      <td>Immetti o mappa l’ID della risorsa per la quale desideri creare un’approvazione.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Fasi</p>
      </td>
      <td>Per ogni fase che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dati dell'area di visualizzazione.<p>Per informazioni specifiche, vedere <a href="#stages-fields" class="MCXref xref" >Campi Stadi</a> in questo articolo. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>ID Modello</p></td>
      <td>Immetti o mappa l’ID del modello da utilizzare per questa approvazione.</td> 
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
      <td role="rowheader"><p>ID Modello</p></td>
      <td>Inserisci o mappa l’ID del cespite per il quale desideri creare delle fasi.</td> 
      </tr>
  </tbody>
</table>

#### Eliminare una decisione in una fase

Questo modulo rimuove la decisione dell’utente corrente dalla fase specificata. L&#39;utente corrente è l&#39;utente le cui credenziali vengono utilizzate nella connessione utilizzata in questo modulo.

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
      <td>Inserisci o mappa l’ID del documento da cui desideri eliminare una decisione.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Immetti o mappa l’ID della fase da eliminare.</td> 
      </tr>
   </tbody>
</table>


#### Eliminare una fase

Questo modulo di azione elimina la fase specificata dall’approvazione.

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
      <td>Immettere o mappare l'ID del documento da cui si desidera eliminare una fase.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID fase</p></td>
      <td>Immetti o mappa l’ID della fase da eliminare.</td> 
      </tr>
  </tbody>
</table>

#### Eliminare un modello

Questo modulo elimina il modello di approvazione specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione alle approvazioni e alle revisioni unificate di Adobe Workfront, vedere <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connessione alle approvazioni e alle revisioni unificate di Adobe Workfront</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID Modello</p></td>
      <td>Inserisci o mappa l’ID del modello da eliminare.</td> 
      </tr>
  </tbody>
</table>

#### Eliminare un’approvazione

Questo modulo di azione elimina l’approvazione per il documento specificato.

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
      <td>Immetti o mappa l’ID del documento da cui desideri eliminare un’approvazione.</td> 
      </tr>
  </tbody>
</table>

#### Elimina decisioni

Questo modulo rimuove la decisione dell’utente corrente dalla fase specificata. L&#39;utente corrente è l&#39;utente le cui credenziali vengono utilizzate nella connessione utilizzata in questo modulo.

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
      <td>Inserisci o mappa l’ID del documento da cui desideri eliminare una decisione.</td> 
      </tr>
  </tbody>
</table>

#### Elimina partecipanti

Questo modulo di azione elimina i partecipanti da un’approvazione.

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
      <td>Inserisci o mappa l’ID della risorsa da cui desideri eliminare i partecipanti.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Tipo di partecipante</p>
      </td>
      <td>Seleziona se i partecipanti sono un utente o un team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID partecipante</p>
      </td>
      <td>Inserisci o mappa l’ID del partecipante.</td> 
      </tr>
  </tbody>
</table>

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
      <td role="rowheader"><p>ID Modello</p></td>
      <td>Immettere o mappare un nome per il modello.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nome</p></td>
      <td>Inserisci o mappa l’ID del modello da aggiornare.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID Azienda</p></td>
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

### Ricerche

* [Ottieni un modello](#get-a-template)
* [Ottieni dettagli approvazione](#get-approval-details)
* [Ottenere più approvazioni](#get-multiple-approvals)
* [Ottieni approvazioni suggerite](#get-suggested-approvals)
* [Ottieni partecipanti suggeriti](#get-suggested-participants)
* [Elenca bot](#list-bots)
* [Modelli di elenco](#list-templates)
* [Cerca revisori del brand AI](#search-ai-brand-reviews)


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
      <td role="rowheader"><p>ID Modello</p></td>
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

