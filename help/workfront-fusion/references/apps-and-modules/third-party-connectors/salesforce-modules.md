---
title: Moduli Salesforce
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Salesforce e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---

# [!DNL Salesforce] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Salesforce] e collegarlo a più applicazioni e servizi di terze parti.

Per un video introduttivo sul connettore Salesforce, vedi:

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Non tutte le edizioni di [!DNL Salesforce] dispongono dell&#39;accesso API. Per informazioni dettagliate, vedere le informazioni sulle edizioni [!DNL Salesforce] con accesso API sul sito della community [!DNL Salesforce].
>* Per informazioni su errori specifici restituiti dall&#39;API [!DNL Salesforce], vedere i documenti API [!DNL Salesforce]. È inoltre possibile controllare lo stato dell&#39;API [!DNL Salesforce] per individuare eventuali interruzioni del servizio.
>

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare i moduli [!DNL Salesforce], è necessario disporre di un account [!DNL Salesforce].

## Informazioni API di Salesforce

Il connettore Salesforce utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v46.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## Informazioni sulla ricerca di [!DNL Salesforce] oggetti

Durante la ricerca di oggetti, è possibile immettere singole parole di ricerca o creare una query più complessa utilizzando caratteri jolly e operatori:

* Utilizza il carattere jolly asterisco (\*) in sostituzione di zero o più caratteri. Ad esempio, la ricerca di Ca\* trova gli elementi che iniziano con Ca
* Utilizza un carattere jolly con punto interrogativo (?) come sostituto di un singolo carattere. Ad esempio, la ricerca di Jo?n consente di trovare elementi con il termine John o Joan ma non Jon
* Utilizza l’operatore tra virgolette (&quot;&quot;) per trovare una corrispondenza esatta della frase. Ad esempio: &quot;Riunione del lunedì&quot;

Per ulteriori informazioni sulle possibilità di ricerca, vedere la documentazione per gli sviluppatori [!DNL Salesforce] su SOQL e SOSL.

## [!DNL Salesforce] moduli e relativi campi

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Triggers

* [[!UICONTROL Watch for Records]](#watch-for-records)
* [[!UICONTROL Watch Outbound Messages]](#watch-outbound-messages)
* [[!UICONTROL Watch a field]](#watch-a-field)

#### [!UICONTROL Watch for Records]

Questo modulo trigger esegue uno scenario quando viene creato o aggiornato un record in un oggetto. Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera controllare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Fields]</td> 
   <td>Selezionare i campi che si desidera controllare nel modulo. I campi disponibili dipendono dal tipo di record.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Determinare se si desidera che lo scenario controlli solo i nuovi record del tipo selezionato o i nuovi record del tipo selezionato e tutte le altre modifiche apportate ai record di tale tipo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Outbound Messages]

Questo modulo di attivazione esegue uno scenario quando un utente invia un messaggio. Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Questo modulo richiede una configurazione aggiuntiva:

1. Passare alla pagina di installazione di [!DNL Salesforce].

   Per accedere alla pagina di configurazione, individuare e fare clic sul pulsante con etichetta &quot;[!UICONTROL Setup]&quot; nell&#39;angolo superiore destro dell&#39;account [!DNL Salesforce]. Dalla pagina di installazione di [!DNL Salesforce], individuare la barra &quot;[!UICONTROL Quick Find / Search]&quot; sul lato sinistro. Cerca &quot;[!UICONTROL Workflow Rules]&quot;.

1. Fare clic su **[!UICONTROL Workflow Rules]**.
1. Nella pagina [!UICONTROL Workflow Rules] visualizzata, fare clic su **[!UICONTROL New Rule]** e selezionare il tipo di oggetto a cui applicare la regola (ad esempio &quot;[!UICONTROL Opportunity]&quot; se si monitorano gli aggiornamenti ai record Opportunità).
1. Fare clic su **[!UICONTROL Next]**.
1. Impostare un nome di regola, criteri di valutazione e criteri di regola, quindi fare clic su **[!UICONTROL Save]** e **[!UICONTROL Next]**.

1. Fare clic su **[!UICONTROL Done]**.
1. Dalla regola del flusso di lavoro appena creata, fare clic su **[!UICONTROL Edit]**.
1. Dall&#39;elenco a discesa **[!UICONTROL Add Workflow Action]**, selezionare **[!UICONTROL New Outbound Message]**.

1. Specificare nome, descrizione, URL endpoint e campi da includere nel nuovo messaggio in uscita, quindi fare clic su **[!UICONTROL Save]**.

   Il campo **[!UICONTROL Endpoint URL]** contiene l&#39;URL specificato per [!DNL Salesforce] [!UICONTROL Outbound Message] in [!DNL Workfront Fusion].

1. Configurare uno scenario che inizia con l&#39;evento [!UICONTROL Outbound Message].

1. Fai clic sull&#39;icona **&lt;/>** in basso a destra e copia l&#39;URL specificato.
1. Torna alla pagina **[!UICONTROL Workflow Rules]**, individua la regola appena creata, quindi fai clic su **[!UICONTROL Activate]**.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook che desideri utilizzare per guardare i messaggi in uscita. Per aggiungere un webhook, fare clic su <strong>[!UICONTROL Add]</strong> e immettere il nome e la connessione del webhook.</p> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera che il modulo controlli per i messaggi in uscita.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fields]</td> 
   <td> <p>Seleziona i campi che desideri che il modulo controlli per i messaggi in uscita. I campi disponibili dipendono dal tipo di record.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### *[!UICONTROL Watch a field]*

Questo modulo trigger avvia uno scenario quando un campo viene aggiornato in [!DNL Salesforce].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selezionare il tipo di record contenente il campo che si desidera controllare nel modulo. Scegliere un tipo di record con [!UICONTROL Field History] attivato nella configurazione di [!DNL Salesforce]. Per ulteriori informazioni, vedere <a href="https://help.salesforce.com/articleView?id=tracking_field_history.htm&amp;type=5">Tracciamento cronologia campi</a> nella documentazione di [!DNL Salesforce]. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td> <p>Selezionare i campi che si desidera che il modulo controlli per verificare le modifiche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di campi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Upload Attachment/Document]](#upload-attachmentdocument)
* [[!UICONTROL Download Attachment/Document]](#download-attachmentdocument)

#### [!UICONTROL Create a Record]

Questo modulo di azione crea un nuovo record in un oggetto.

Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo. Questo riduce il numero di campi da scorrere durante la configurazione del modulo.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera venga creato dal modulo. I campi diventano disponibili in base al tipo di record selezionato nel campo [!UICONTROL Record Type]. Questi campi sono basati sull'API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selezionare i campi che si desidera configurare nel modulo durante la creazione del nuovo record. I campi obbligatori si trovano all’inizio dell’elenco. </p> <p>I campi selezionati vengono aperti sotto questo campo. È ora possibile immettere valori in questi campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

Questo modulo di azione legge i dati da un singolo oggetto in [!DNL Salesforce].

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Record Type]</td>
    <td>Selezionare il tipo di record [!DNL Salesforce] che si desidera impostare come [action] per il modulo.read.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Record Fields]</td>
    <td>Seleziona i campi che desideri che il modulo legga. Selezionare almeno un campo.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera venga letto dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

Questo modulo di azione elimina un record esistente in un oggetto.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] da eliminare dal modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera eliminare dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Salesforce]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Salesforce].

Il modulo restituisce quanto segue:

* **[!UICONTROL Status Code]** (numero): indica l&#39;esito positivo o negativo della richiesta HTTP. Si tratta di codici standard che puoi cercare su Internet.
* **[!UICONTROL Headers]** (oggetto): contesto più dettagliato per il codice di risposta/stato che non è correlato al corpo di output. Non tutte le intestazioni visualizzate in un’intestazione di risposta sono intestazioni di risposta, quindi alcune potrebbero non essere utili.

  Le intestazioni di risposta dipendono dalla richiesta HTTP scelta durante la configurazione del modulo.

* **[!UICONTROL Body]** (oggetto): a seconda della richiesta HTTP scelta durante la configurazione del modulo, alcuni dati potrebbero essere restituiti. Tali dati, ad esempio i dati di una richiesta [!UICONTROL GET], sono contenuti in questo oggetto.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code> &lt;Instance URL&gt;/services/data/v46.0/</code>.</p> <p>Per l'elenco degli endpoint disponibili, fare riferimento alla <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Guida per gli sviluppatori di API REST di Salesforce</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard. Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** La seguente chiamata API restituisce l&#39;elenco di tutti gli utenti nel tuo account [!DNL Salesforce]:
>
>* **URL**: `query`
>
>* **Metodo**: [!UICONTROL GET]
>
>* **Stringa di query**:
>
>* **Chiave**: `q`
>
>* **Valore**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`
>
>Le corrispondenze della ricerca si trovano nell&#39;output del modulo in **[!UICONTROL Bundle]> [!UICONTROL Body] >[!UICONTROL records]**.
>
>Nel nostro esempio, sono stati restituiti 6 utenti:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)


#### [!UICONTROL Upload Attachment/Document]

Questo modulo di azione carica un file e lo allega a un record specificato oppure carica un documento.

Il modulo restituisce l’ID dell’allegato o del documento e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type of Upload]</td> 
   <td>Seleziona se vuoi che il modulo carichi un allegato o un documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera caricare un allegato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td>Seleziona la cartella contenente il file da caricare nel modulo. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download Attachment/Document]

Questo modulo di azione scarica un documento o un allegato da un record.

Specificare l&#39;ID del record e il tipo di download desiderato.

Il modulo restituisce l’ID dell’allegato o del documento e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Type of Download]</td>
    <td> <p>Specifica il tipo di file da scaricare da Salesforce.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Document]</li> 
      <li>[!UICONTROL ContentDocument] Questo documento è stato caricato in una raccolta in [!DNL Saleforce CRM Content] o [!DNL Salesforce Files].</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL Attachment ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera scaricare dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Update a Record]

Questo modulo di azione modifica un record in un oggetto.

Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo. Questo riduce il numero di campi da scorrere durante la configurazione del modulo.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] da aggiornare nel modulo. I campi diventano disponibili in base al tipo di record selezionato nel campo Tipo di record. Questi campi sono basati sull'API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Selezionare i campi che si desidera configurare nel modulo durante la creazione del nuovo record. I campi obbligatori si trovano all’inizio dell’elenco. </p> <p>I campi selezionati vengono aperti sotto questo campo. È ora possibile immettere valori in questi campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Search with Query]

Questo modulo di ricerca cerca i record in un oggetto in [!DNL Salesforce] che corrispondono alla query di ricerca specificata. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search Type]</td> 
   <td> <p>Selezionare il tipo di ricerca che si desidera venga eseguita dal modulo:</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Se è stato selezionato il tipo di ricerca Semplice, scegliere il tipo di record [!DNL Salesforce] che si desidera cercare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>Immettere la query in base alla quale si desidera eseguire la ricerca.</p> <p>Per ulteriori informazioni su SOSL, vedere <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce Object Search Language (SOSL)</a> nella documentazione di [!DNL Salesforce].</p> <p>Per ulteriori informazioni su SOQL, vedere <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce Object Query Language (SOQL)</a> nella documentazione di [!DNL Salesforce].</p> <p>Nota: il valore del parametro <code>RETURNING </code> influenza l'output del modulo. Se si utilizza <code>LIMIT</code>, [!DNL Fusion] ignorerà le impostazioni nel campo [!UICONTROL Maximal count of records]. Se non si imposta alcun limite, verrà inserito il valore [!UICONTROL LIMIT = Maximal count of records].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

Questo modulo di azione recupera tutti i record che soddisfano un determinato criterio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL  Adobe Workfront Fusion] - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selezionare il tipo di oggetto che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Selezionare il campo in base al quale si desidera eseguire la ricerca, l'operatore che si desidera utilizzare nella query e il valore ricercato nel campo. È possibile connettere le query utilizzando AND o OR.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selezionare i campi da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Selezionare se si desidera che il modulo restituisca tutti i record corrispondenti o solo il primo record corrispondente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>