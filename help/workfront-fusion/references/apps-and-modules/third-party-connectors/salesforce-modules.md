---
title: Moduli Salesforce
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Salesforce e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
TQID: https://experienceleague.adobe.com/P-GPOboH09jZI9dQ5wBfFNV3NNOk-lpSPs7SI4rXHE4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 3032
ht-degree: 35%

---

# Moduli [!DNL Salesforce]

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Salesforce] e collegarlo a più applicazioni e servizi di terze parti.

Per un video introduttivo sul connettore Salesforce, vedi:

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Non tutte le edizioni di [!DNL Salesforce] dispongono dell&#39;accesso API. Per informazioni dettagliate, vedere le informazioni sulle edizioni [!DNL Salesforce] con accesso API sul sito della community [!DNL Salesforce].
>* Per informazioni su errori specifici restituiti dall&#39;API [!DNL Salesforce], vedere i documenti API [!DNL Salesforce]. È inoltre possibile controllare lo stato dell&#39;API [!DNL Salesforce] per individuare eventuali interruzioni del servizio.
>

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

Per utilizzare i moduli [!DNL Salesforce], è necessario disporre di un account [!DNL Salesforce].

## Informazioni API di Salesforce

Il connettore Salesforce utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td><pre><code>&#123;&#123;connection.instanceUrl&#125;&#125;</code></pre></td>
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v62.0 </td> 
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

## Creare una connessione ad [!DNL Salesforce]

Per creare una connessione per i moduli [!DNL Salesforce]:

1. In qualsiasi modulo di [!DNL Salesforce], fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

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
        <td>Immetti l'ID client di Salesforce.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Immetti il segreto del client Salesforce. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>Abilita questa opzione se si tratta di un ambiente Sandbox.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Versione API]</td>
        <td>Immetti la versione dell’API Salesforce che desideri utilizzare. La versione predefinita è 62.0.</td>
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.


## Moduli [!DNL Salesforce] e relativi campi

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [[!UICONTROL Osserva un campo]](#watch-a-field)
* [[!UICONTROL Controlla i record]](#watch-for-records)
* [[!UICONTROL Guarda i messaggi in uscita]](#watch-outbound-messages)

#### [!UICONTROL Osserva un campo]

Questo modulo trigger avvia uno scenario quando un campo viene aggiornato in [!DNL Salesforce].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record] </td> 
   <td> <p>Selezionare il tipo di record contenente il campo che si desidera controllare nel modulo. È necessario scegliere un tipo di record con [!UICONTROL Field History] attivato nella configurazione di [!DNL Salesforce]. Per ulteriori informazioni, vedere <a href="https://help.salesforce.com/s/articleView?id=xcloud.tracking_field_history.htm&type=5">Tracciamento cronologia campi</a> nella documentazione di [!DNL Salesforce]. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campo]</td> 
   <td> <p>Selezionare i campi che si desidera che il modulo controlli per verificare le modifiche. I campi disponibili dipendono dal tipo di record selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di campi che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Controlla i record]

Questo modulo trigger esegue uno scenario quando viene creato o aggiornato un record in un oggetto. Il modulo restituisce tutti i campi standard associati al record oppure ai record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera controllare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi Record]</td> 
   <td>Selezionare i campi che si desidera controllare nel modulo. I campi disponibili dipendono dal tipo di record.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conteggio massimo dei record]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Determinare se si desidera che lo scenario controlli solo i nuovi record del tipo selezionato o i nuovi record del tipo selezionato e tutte le altre modifiche apportate ai record di tale tipo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Guarda i messaggi in uscita]

Questo modulo di attivazione esegue uno scenario quando un utente invia un messaggio. Il modulo restituisce tutti i campi standard associati al record oppure ai record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Questo modulo richiede una configurazione aggiuntiva. È necessario configurare un flusso per i messaggi in uscita.

* Per istruzioni sui flussi in Salesforce, vedi [Automatizzare le attività con flussi](https://help.salesforce.com/s/articleView?id=platform.flow.htm) nella documentazione di Salesforce.
* Per informazioni sulla configurazione di un messaggio in uscita in Salesforce, vedi [Inviare un messaggio in uscita dal flusso attivato dal record](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_outbound_message.htm) nella documentazione di Salesforce

<!--

1. Go to the [!DNL Salesforce] setup page.

   To access the setup page, locate and click the button labeled "[!UICONTROL Setup]" in the upper-right hand corner of the [!DNL Salesforce] account. From the [!DNL Salesforce] setup page, locate the "[!UICONTROL Quick Find / Search]" bar on the left hand side. Search for "[!UICONTROL Workflow Rules]." 

1. Click **[!UICONTROL Workflow Rules]**. 
1. On the the [!UICONTROL Workflow Rules] page that appears, click **[!UICONTROL New Rule]** and select the object type the rule will apply to (such as "[!UICONTROL Opportunity]" if you are monitoring updates to Opportunity records).
1. Click **[!UICONTROL Next]**.
1. Set a rule name, evaluation criteria, and rule criteria, then click **[!UICONTROL Save]** and **[!UICONTROL Next]**.

1. Click **[!UICONTROL Done]**.
1. From the newly created Workflow rule, click **[!UICONTROL Edit]**..
1. From the **[!UICONTROL Add Workflow Action]** drop-down list, select **[!UICONTROL New Outbound Message]**.

1. Specify name, description, Endpoint URL, and fields you want to include in the new outbound message, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Endpoint URL]** field contains the URL provided on the [!DNL Salesforce] [!UICONTROL Outbound Message] in Workfront Fusion.

1. Configure a scenario beginning with the [!UICONTROL Outbound Message] event. 

1. Click the **</>** icon in the bottom right and copy the provided URL.
1. Return to the **[!UICONTROL Workflow Rules]** page, locate the newly created rule, then click **[!UICONTROL Activate]**.

-->

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook che desideri utilizzare per guardare i messaggi in uscita. Per aggiungere un webhook, fare clic su <strong>[!UICONTROL Add]</strong> e immettere il nome e la connessione del webhook.</p> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera che il modulo controlli per i messaggi in uscita.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi]</td> 
   <td> <p>Seleziona i campi che desideri che il modulo controlli per i messaggi in uscita. I campi disponibili dipendono dal tipo di record.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Crea un record]](#create-a-record)
* [[!UICONTROL Chiamata API personalizzata]](#custom-api-call)
* [[!UICONTROL Eliminare un record]](#delete-a-record)
* [[!UICONTROL Scarica Allegato/Documento]](#download-attachmentdocument)
* [[!UICONTROL Leggi un record]](#read-a-record)
* [[!UICONTROL Carica allegato/documento]](#upload-attachmentdocument)
* [Carica file](#upload-file)

#### [!UICONTROL Crea un record]

Questo modulo di azione crea un nuovo record in un oggetto.

Il modulo ti consente di selezionare i campi dell’oggetto disponibili nel modulo. Questo riduce il numero di campi da scorrere durante la configurazione del modulo.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo di record] </p> </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] che si desidera venga creato dal modulo. I campi diventano disponibili in base al tipo di record selezionato nel campo [!UICONTROL Tipo di record]. Questi campi sono basati sull'API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Seleziona i campi da mappare]</td> 
   <td> <p>Selezionare i campi che si desidera configurare nel modulo durante la creazione del nuovo record. I campi obbligatori si trovano all’inizio dell’elenco. </p> <p>I campi selezionati vengono aperti sotto questo campo. È ora possibile immettere valori in questi campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Salesforce]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Salesforce].

Il modulo restituisce quanto segue:

* **[!UICONTROL Codice di stato]** (numero): indica il completamento o il mancato completamento della richiesta HTTP. I valori restituiti sono codici standard che puoi cercare su Internet.
* **[!UICONTROL Intestazioni]** (oggetto): un contesto più dettagliato per il codice di risposta/stato non correlato al corpo dell’output. Non tutte le intestazioni visualizzate in una risposta sono intestazioni di risposta, pertanto alcune potrebbero non risultarti utili.

  Le intestazioni di risposta dipendono dalla richiesta HTTP che hai scelto durante la configurazione del modulo.

* **[!UICONTROL Corpo]** (oggetto): a seconda della richiesta HTTP che hai scelto al momento della configurazione del modulo, potresti ricevere alcuni dati. Tali dati, ad esempio i dati di una richiesta [!UICONTROL GET], sono contenuti in questo oggetto.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Inserisci un percorso relativo a <code> &lt;Instance URL&gt;/services/data/v62.0/</code>.</p> <p>Per l'elenco degli endpoint disponibili, fare riferimento alla <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Guida per gli sviluppatori di API REST di Salesforce</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metodo]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard. Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!BEGINSHADEBOX]

**Esempio:** La seguente chiamata API restituisce l&#39;elenco di tutti gli utenti nel tuo account [!DNL Salesforce]:

* **URL**: `query`

* **Metodo**: [!UICONTROL GET]

* **Stringa di query**:

* **Chiave**: `q`

* **Valore**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`

Le corrispondenze della ricerca si trovano nell&#39;output del modulo in **[!UICONTROL Bundle] > [!UICONTROL Corpo] > [!UICONTROL record]**.

Nel nostro esempio, sono stati restituiti 6 utenti:

![Corrisponde alla ricerca](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Eliminare un record]

Questo modulo di azione elimina un record esistente in un oggetto.

Specifica l’ID del record.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record] </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] da eliminare dal modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera eliminare dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica Allegato/Documento]

Questo modulo di azione scarica un documento o un allegato da un record.

Specificare l&#39;ID del record e il tipo di download desiderato.

Il modulo restituisce l’ID dell’allegato o del documento e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connessione]</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Tipo di download]</td>
    <td> <p>Specifica il tipo di file da scaricare da Salesforce.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Documento]</li> 
      <li>[!UICONTROL ContentDocument] (documento caricato in una raccolta in [!DNL Saleforce CRM Content] o [!DNL Salesforce Files].)</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL ID allegato] / </p> <p>[!UICONTROL ID ContentDocument]</p> </td>
    <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera scaricare dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge i dati da un singolo oggetto in [!DNL Salesforce].

Specifica l’ID del record.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connessione]</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Tipo di record]</td>
    <td>Selezionare il tipo di record [!DNL Salesforce] che si desidera venga letto dal modulo.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Campi Record]</td>
    <td>Seleziona i campi che desideri che il modulo legga. Selezionare almeno un campo. I campi disponibili dipendono dal tipo di record.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Immettere o mappare l'ID [!DNL Salesforce] univoco del record che si desidera venga letto dal modulo.</p> <p>Per ottenere l'ID, aprire l'oggetto [!DNL Salesforce] nel browser e copiare il testo alla fine dell'URL dopo l'ultima barra (/). Ad esempio: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Aggiorna un record]

Questo modulo di azione modifica un record in un oggetto.

Il modulo ti consente di selezionare i campi dell’oggetto disponibili nel modulo. Questo riduce il numero di campi da scorrere durante la configurazione del modulo.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo di record] </p> </td> 
   <td> <p>Selezionare il tipo di record [!DNL Salesforce] da aggiornare nel modulo. I campi diventano disponibili in base al tipo di record selezionato nel campo Tipo di record. Questi campi sono basati sull'API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Seleziona i campi da mappare]</td> 
   <td> <p>Selezionare i campi che si desidera configurare nel modulo durante la creazione del nuovo record. I campi obbligatori si trovano all’inizio dell’elenco. </p> <p>I campi selezionati vengono aperti sotto questo campo. È ora possibile immettere valori in questi campi.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Carica allegato/documento]

Questo modulo di azione carica un file e lo allega a un record specificato oppure carica un documento.

Il modulo restituisce l’ID dell’allegato o del documento e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di caricamento]</td> 
   <td>Seleziona se vuoi che il modulo carichi un allegato o un documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera caricare un allegato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella]</td> 
   <td>Selezionare la cartella in cui si desidera caricare un documento. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File di origine]</td> 
   <td>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

#### Carica file

Questo modulo di azione carica un singolo file in Salesforce.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a[!DNL &#x200B; Adobe Workfront Fusion] - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collegamento documento]</td> 
   <td>Seleziona se applicare un collegamento al documento di contenuto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>Se si utilizza il collegamento di documenti, immettere o mappare l'ID dell'oggetto collegato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>Se si utilizza il collegamento di documenti, selezionare le autorizzazioni per il file.<ul><li><b>Autorizzazione visualizzatore</b><p>L’utente può visualizzare il file.</p></li><li><b>Autorizzazione collaboratore</b><p>L’utente può visualizzare e modificare il file.</p></li><li><b>Autorizzazioni dedotte</b><p>Le autorizzazioni si basano sulle autorizzazioni dell'utente per il record correlato, ad esempio una libreria.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Se si utilizza il collegamento del documento, immettere o mappare la visibilità del documento.<ul><li><b>AllUsers</b><p>Disponibile per tutti gli utenti con autorizzazioni</p></li><li><b>InternalUsers</b><p>Disponibile per gli utenti interni con autorizzazioni.</p></li><li><b>SharedUsers</b><p>Disponibile per gli utenti che possono visualizzare il feed in cui è pubblicato il file.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [Ricerca](#search)
* [Cerca con query](#search-with-query)

#### [!UICONTROL Ricerca]

Questo modulo di azione recupera tutti i record che soddisfano un determinato criterio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a[!DNL &#x200B; Adobe Workfront Fusion] - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> <p>Selezionare il tipo di oggetto che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criteri di ricerca]</td> 
   <td>Selezionare il campo in base al quale si desidera eseguire la ricerca, l'operatore che si desidera utilizzare nella query e il valore ricercato nel campo. È possibile connettere le query utilizzando AND o OR.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi da includere nell'output del modulo. I campi sono disponibili in base al tipo di record</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Set di risultati]</td> 
   <td>Selezionare se si desidera che il modulo restituisca tutti i record corrispondenti o solo il primo record corrispondente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Massimo]</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca con query]

Questo modulo di ricerca cerca i record in un oggetto in [!DNL Salesforce] che corrispondono alla query di ricerca specificata. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Salesforce] a Workfront Fusion, vedere <a href="#create-a-connection-to-salesforce">Creare una connessione a Salesforce</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Tipo di ricerca </td> 
   <td> <p>Selezionare il tipo di ricerca che si desidera venga eseguita dal modulo:</p> 
    <ul> 
     <li> <p>[!UICONTROL Semplice]</p> </li> 
     <li> <p>[!UICONTROL Tramite SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Tramite SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo] </p> </td> 
   <td> <p>Se è stato selezionato il tipo di ricerca Semplice, scegliere il tipo di record [!DNL Salesforce] che si desidera cercare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>Immettere la query in base alla quale si desidera eseguire la ricerca.</p> <p>Per ulteriori informazioni su SOSL, vedere <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce Object Search Language (SOSL)</a> nella documentazione di [!DNL Salesforce].</p> <p>Per ulteriori informazioni su SOQL, vedere <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce Object Query Language (SOQL)</a> nella documentazione di [!DNL Salesforce].</p> <p>Nota: il valore del parametro <code>RETURNING </code> influenza l'output del modulo. Se si utilizza <code>LIMIT</code>, [!DNL Fusion] ignorerà le impostazioni nel campo [!UICONTROL Conteggio massimo dei record]. Se non si imposta alcun limite, verrà inserito il valore [!UICONTROL LIMIT = Maximal count of records].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conteggio massimo dei record]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>
