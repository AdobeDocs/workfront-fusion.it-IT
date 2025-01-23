---
title: Moduli aerodinamici
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 2%

---

# Moduli aerodinamici


Con il connettore [!DNL Airtable] per [!DNL Adobe Workfront Fusion], puoi avviare uno scenario basato sugli eventi nel tuo account [!DNL Airtable], creare, caricare e aggiornare record, cercare record ed effettuare chiamate API personalizzate all&#39;API Airtable.

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] per l'automazione e l'integrazione del lavoro] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>La tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare le funzionalità di questo articolo è necessario disporre di un account Airtable.

<!--
<p>For more information, see the tutorial .</p>
-->

## Informazioni API Airtable

Il connettore Airtable utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## Collegamento di Airtable a Workfront Fusion {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. Aprire Workfront Fusion e la finestra di dialogo **Crea una connessione** del modulo desiderato.
1. Immettere un nome per la connessione.
1. (Facoltativo) Fai clic su Mostra impostazioni avanzate e immetti l&#39;ID cliente Airtable e il segreto cliente.
1. Fai clic sul pulsante **Continua** per creare la connessione e tornare al modulo.

## Moduli aerodinamici e relativi campi

### Record

* [Crea un record](#create-a-record)
* [Eliminare un record](#delete-a-record)
* [Ottieni un record](#get-a-record)
* [Cerca record](#search-records)
* [Aggiorna un record](#update-a-record)
* [Eseguire l&#39;upsert di un record](#upsert-a-record)
* [Osserva i record](#watch-records)
* [Osservare le risposte](#watch-responses)
* [Effettuare una chiamata API](#make-an-api-call)

#### Crea un record {#create-a-record}

Questo modulo di azione crea un nuovo record.

È possibile specificare i dati desiderati nel record e la posizione in cui archiviarli.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base di appartenenza del nuovo record.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella a cui apparterrà il nuovo record.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Inserimento</p> </td> 
   <td> <p>Immettere i valori per il nuovo record. I campi disponibili dipendono dalla tabella selezionata.</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Collegamenti avanzati</td> 
   <td> <p>Abilitare questa opzione per immettere nomi anziché ID record nei campi collegati a un'altra tabella. Se non viene trovata alcuna corrispondenza, il record viene creato automaticamente nella tabella collegata.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un record {#delete-a-record}

Questo modulo di azione elimina un record specifico.

Specificare l&#39;ID e le posizioni del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base contenente il record che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella contenente il record che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>ID record</td> 
   <td> <p>Immettere o mappare l'ID univoco della tabella di volo del record che si desidera eliminare dal modulo. Puoi recuperare l’ID, ad esempio, utilizzando il modulo Record di ricerca.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni un record {#get-a-record}

Questo modulo di azione recupera i dettagli del record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base che contiene la tabella con il record che si desidera recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella</td> 
   <td> <p> Selezionare la tabella contenente il record per cui si desidera recuperare i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td>ID record</td> 
   <td> <p> Immetti o mappa l’ID del record per il quale desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Cerca record {#search-records}

Questo modulo di ricerca cerca i record in un oggetto in Airtable che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base da cercare nei record.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella in cui si desidera cercare i record.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formula</p> </td> 
   <td> <p>Formula utilizzata per filtrare i record. La formula viene valutata per ogni record e se il risultato non è <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> o <code>#Error!</code> il record viene incluso nella risposta.</p> <p>Se combinati con <code>view</code>, verranno restituiti solo i record della visualizzazione che soddisfano la formula.</p> <p>Ad esempio, per includere solo i record in cui Nome non è vuoto, passare:<code> NOT({Name} = '')</code></p> <p>Per ulteriori informazioni, consulta la documentazione di supporto di Airtable per informazioni sui riferimenti ai campi della formula.</p> </td> 
  </tr> 
  <tr> 
   <td>Ordina </td> 
   <td> <p>Selezionare la direzione di ordinamento e il campo in base al quale si desidera ordinare i risultati.</p> </td> 
  </tr> 
  <tr> 
   <td>Visualizza </td> 
   <td> <p>Selezionare la visualizzazione in cui si desidera cercare i record.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un record {#update-a-record}

Questo modulo di azione aggiorna un record specifico.

È possibile specificare l&#39;ID del record e i nuovi dati che si desidera che contenga.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base contenente il record che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella contenente il record che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>ID record </td> 
   <td> <p>Immettere o mappare l'ID univoco della tabella di volo del record che si desidera aggiornare nel modulo. Puoi recuperare l’ID, ad esempio, utilizzando il modulo Record di ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Inserimento</p> </td> 
   <td> <p>Immettere i valori per il nuovo record. I campi disponibili dipendono dalla tabella selezionata.</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Collegamenti avanzati</td> 
   <td> <p>Immettere i nomi anziché gli ID record per i campi collegati a un'altra tabella. Se non viene trovata alcuna corrispondenza, il record viene creato automaticamente nella tabella collegata.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Eseguire l&#39;upsert di un record

Questo modulo di azione aggiorna o inserisce un record specifico.

È possibile specificare l&#39;ID del record e i nuovi dati che si desidera che contenga.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base contenente il record che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella contenente il record che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>ID record </td> 
   <td> <p>Se si sta aggiornando un record, immettere o mappare l'ID univoco della tabella di volo del record che si desidera aggiornare nel modulo. Puoi recuperare l’ID, ad esempio, utilizzando il modulo Record di ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Inserimento</p> </td> 
   <td> <p>Immettere i valori per il nuovo record. I campi disponibili dipendono dalla tabella selezionata.</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Collegamenti avanzati</td> 
   <td> <p>Immettere i nomi anziché gli ID record per i campi collegati a un'altra tabella. Se non viene trovata alcuna corrispondenza, il record viene creato automaticamente nella tabella collegata.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva i record {#watch-records}

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un record nella tabella specificata.

>[!NOTE]
>
>Per utilizzare questo modulo, è necessario creare nella tabella il campo Ora di creazione o Ultima modifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Selezionare la base da controllare per i nuovi record.</p> </td> 
  </tr> 
  <tr> 
   <td>Tabella </td> 
   <td> <p>Selezionare la tabella da controllare per i nuovi record.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Configurazione dell'attivatore</p> </td> 
   <td> <p>Campo trigger</p> <p>Campo <code>Created Time</code> o <code>Last Modified Time</code> utilizzato per ordinare i record. Se nello schema non è presente un campo <code>Created Time</code> o <code>Last Modified Time</code>, è necessario crearne uno. </p> <p>Campo etichetta</p> <p>Campo utilizzato come etichetta per un record, ad esempio nella finestra di dialogo Scegli da dove iniziare.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve controllare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>Visualizza</td> 
   <td> <p>Selezionare la visualizzazione che si desidera utilizzare.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formula</p> </td> 
   <td> <p>Formula utilizzata per filtrare i record. La formula viene valutata per ogni record e se il risultato non è <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> o <code>#Error!</code> il record viene incluso nella risposta.</p> <p>Se combinati con <code>view</code>, verranno restituiti solo i record della visualizzazione che soddisfano la formula.</p> <p>Ad esempio, per includere solo i record in cui Nome non è vuoto, passare:<code> NOT({Name} = '')</code></p> <p>Per ulteriori informazioni, consulta le informazioni sui riferimenti ai campi della formula nella documentazione di supporto di Airtable.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osservare le risposte

Questo modulo di attivazione avvia uno scenario quando viene inviato un modulo.

>[!NOTE]
>
>Questa funzionalità è disponibile solo per il piano Airtable Pro a pagamento.

L’URL del webhook deve essere generato in Workfront Fusion e quindi aggiunto alla configurazione del modulo in Airtable.

1. Aggiungi il modulo Guarda nuove risposte allo scenario Workfront Fusion.
1. Genera e copia l’URL del webhook.

   <!--For instructions, see [ (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. Accedi al tuo account Airtable.
1. Aprire la base e la tabella che si desidera utilizzare per la maschera e creare una visualizzazione Maschera.
1. Imposta il modulo in base alle esigenze, scorri il modulo verso il basso e abilita l’opzione Reindirizza all’URL dopo l’invio del modulo.
1. Immetti l&#39;URL del webhook generato al passaggio 2 nella finestra di dialogo visualizzata e aggiungi l&#39;?record_id={record_id} subito dopo l&#39;URL del webhook per includere l&#39;ID record nell&#39;output del modulo, quindi fai clic su Salva. L’URL risultante sarà, ad esempio, simile al seguente:
1. Torna allo scenario Workfront Fusion ed esegui il modulo Risposte di controllo solo per caricare i campi da Airtable e per essere in grado di mappare tali campi negli altri moduli.
1. Invia il modulo in Airtable se è abilitata l’opzione Reindirizza all’URL dopo l’invio del modulo e viene aggiunto l’URL del webhook (passaggio 6 di cui sopra).

   Viene attivato il modulo Osserva risposte e vengono caricati i dati desiderati.

1. Aggiungi Airtable > Get a Record module subito dopo il modulo Airtable > Watch Responses (Osserva risposte) e mappa record_id nel campo Record ID (ID record).

Ora, ogni volta che il modulo viene inviato, viene attivato il modulo Osserva risposte nello scenario di Workfront Fusion e il modulo Ottieni un record restituisce i dettagli del modulo inviato.

#### Effettuare una chiamata API

#### Chiamata API personalizzata

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Airtable]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Airtable].

L’azione si basa sul tipo di entità (tipo di oggetto Allocadia) specificato.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Connessione</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Airtable a Workfront Fusion, vedere <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connessione Airtable a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Immettere un percorso relativo a <code>https://api.airtable.com/</code>. Esempio: <code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metodo</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Intestazioni</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stringa di query</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di chiave e valore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
