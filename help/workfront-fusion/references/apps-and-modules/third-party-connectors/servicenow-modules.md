---
title: Moduli ServiceNow
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL ServiceNow], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 3e39d284014c76a1cc300a075e61c25964c49995
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 43%

---

# Moduli [!DNL ServiceNow]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL ServiceNow], nonché collegarli a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL ServiceNow], è necessario disporre di un account [!DNL ServiceNow].

## Informazioni API ServiceNow

Il connettore ServiceNow utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td><pre><code>https://&#123;&#123;connection.instance&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL ServiceNow] a Workfront Fusion

Per creare una connessione per i moduli [!DNL ServiceNow]:

1. Fare clic su **[!UICONTROL Aggiungi]** accanto alla casella [!UICONTROL Connessione] quando si inizia la configurazione del primo modulo [!DNL ServiceNow].
1. Immetti il codice seguente:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name] (Nome della connessione)</p> </td> 
      <td>Immettere un nome per la nuova connessione [!DNL ServiceNow].</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Ambiente]</p> </td> 
      <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Specifica se ti connetti a un account di servizio o a un account personale. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>Immetti il nome utente [!DNL ServiceNow].</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>Immettere la password ServiceNow.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>Immettere l'indirizzo dell'account [!DNL ServiceNow] senza <code>https://</code> (in genere <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **Continua** per salvare la connessione e tornare al modulo.

   <!--Markdown placeholder-->

## Moduli [!UICONTROL ServiceNow] e relativi campi

Quando configuri i moduli [!DNL ServiceNow], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL ServiceNow], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se si seleziona un record personalizzato in un campo &quot;[!UICONTROL Tipo di record]&quot;, il caricamento dei campi personalizzati potrebbe richiedere del tempo.
>
>* Se non sono presenti record personalizzati, il menu a discesa del campo &quot;Tipo di record&quot; sarà vuoto.

### Trigger

#### [!UICONTROL Controlla record]

Questo modulo di attivazione attiva uno scenario quando viene creato o aggiornato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di tabella]</td> 
   <td>Seleziona se la tabella da guardare è una tabella personalizzata o standard.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selezionare il tipo di valori che si desidera visualizzare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi che si desidera vengano generati dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Specificare se si desidera controllare i nuovi record o i record aggiornati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Crea un record]](#create-a-record)
* [[!UICONTROL Chiamata API personalizzata]](#custom-api-call)
* [[!UICONTROL Disattiva un utente]](#deactivate-a-user)
* [[!UICONTROL Eliminare un record]](#delete-a-record)
* [[!UICONTROL Scarica un allegato]](#download-an-attachment)
* [[!UICONTROL Leggi un record]](#read-a-record)
* [[!UICONTROL Carica un allegato]](#upload-an-attachment)
* [[!UICONTROL Aggiorna un record]](#update-a-record)

#### [!UICONTROL Crea un record]

Questo modulo azioni crea un nuovo record [!DNL ServiceNow].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di tabella]</td> 
   <td>Specificare se si desidera creare un record in una tabella personalizzata o standard.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record [!DNL ServiceNow] che si desidera venga creato dal modulo. È quindi possibile compilare i campi disponibili per questo tipo di record.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL ServiceNow]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL ServiceNow].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL relativo]</td> 
   <td> Inserisci un percorso relativo a <code>https://&ltinstance_url&gt/api/</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Disattiva un utente]

Questo modulo di azione disattiva un utente in [!DNL ServiceNow] utilizzando l&#39;ID di sistema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> Immettere o mappare l'ID [!DNL ServiceNow] univoco dell'utente che si desidera disattivare nel modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un record]

Questo modulo di azione elimina un incidente o un utente.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Specificare se si desidera eliminare un incidente o un utente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID sistema]</td> 
   <td>Immettere o mappare l'ID [!DNL ServiceNow] univoco del record che si desidera eliminare dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica un allegato]

Questo modulo di azione scarica un allegato in un record [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> Immettere o mappare l'ID [!DNL ServiceNow] univoco dell'allegato che si desidera scaricare dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge un record [!DNL ServiceNow] utilizzando l&#39;ID di sistema.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Immettere o mappare l'ID [!DNL ServiceNow] univoco del record che si desidera venga letto dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di tabella]</td> 
   <td>Specificare se il record da leggere si trova in una tabella personalizzata o in una tabella standard.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record [!DNL ServiceNow] che si desidera venga letto dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selezionare il tipo di valori che si desidera visualizzare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi che si desidera vengano generati dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un record]

Questo modulo azioni crea un nuovo record [!DNL ServiceNow].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>Immettere o mappare l'ID [!DNL ServiceNow] univoco del record che si desidera aggiornare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di tabella]</td> 
   <td>Specificare se il record da aggiornare si trova in una tabella personalizzata o in una tabella standard.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record [!DNL ServiceNow] da aggiornare nel modulo. È quindi possibile compilare i campi disponibili per questo tipo di record.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un allegato]

Questo modulo di azione carica un allegato in un record [!DNL ServiceNow].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome tabella]</td> 
   <td>Immettere o mappare il nome della tabella in cui si desidera caricare l'allegato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID sistema]</td> 
   <td>Immettere o mappare l'ID [!DNL ServiceNow] univoco dell'elemento in cui si desidera caricare l'allegato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Cerca record]

Questo modulo cerca i record utilizzando i criteri selezionati.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account ServiceNow a Workfront Fusion, vedere <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">Connettere [!DNL ServiceNow] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di tabella]</td> 
   <td>Seleziona se la tabella da cercare è una tabella personalizzata o standard.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record che si desidera cercare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Set di risultati]</td> 
   <td>Specificare se si desidera che il modulo restituisca tutti i record che corrispondono ai criteri oppure solo il primo record corrispondente. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conteggio massimo dei record]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di ricerca [!UICONTROL]</td> 
   <td> <p>Seleziona il tipo di ricerca da eseguire nel modulo</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query avanzata]</strong> </p> 
      <ul> 
       <li> <p>Query di ricerca [!UICONTROL]</p> <p>Immettere la query di ricerca personalizzata. Per informazioni su [!DNL ServiceNow] query di ricerca personalizzate, consulta la <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">documentazione sulle query ServiceNow</a>.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Semplice]</strong> </p> 
      <ul> 
       <li> <p>Criteri di ricerca di [!UICONTROL]</p> <p>Immettere i criteri in base ai quali si desidera eseguire la ricerca nel modulo. </li> 
       <li> <p>[!UICONTROL Ordina per]</p> <p>Indica per quale campo desideri che il modulo ordini i risultati e se devono essere ordinati in ordine crescente o decrescente.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>Selezionare il tipo di valori che si desidera visualizzare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi che si desidera vengano generati dal modulo.</td> 
  </tr> 
 </tbody> 
</table>
