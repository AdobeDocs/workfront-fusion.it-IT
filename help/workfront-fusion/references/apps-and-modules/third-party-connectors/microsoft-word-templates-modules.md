---
title: Moduli modello di Microsoft Word
description: In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano modelli di Microsoft Word e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: a5ba5634-226b-4886-a4f1-3a14948c1605
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 0%

---

# [!DNL Microsoft Word Template] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft Word Templates] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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
  </tr> <!--
   <tr> 
    <td role="rowheader">Access level configurations*</td> 
    <td> 
      <p>You must be a Workfront Fusion administrator for your organization.</p>
     --> <!--
      <p>You must be a Workfront Fusion administrator for your team.</p>
     --> </td> 
   </tr>
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare [!DNL Miscrosoft Word Templates] con [!DNL Adobe Workfront Fusion], è necessario disporre di un account [!DNL Office 365]. Puoi crearne uno in `www.office.com`.



## Connessione del servizio [!DNL Office] a [!DNL Workfront Fusion]

Per istruzioni sulla connessione dell&#39;account [!DNL Office] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## Utilizzo di [!DNL Microsoft Word Templates] moduli

È possibile utilizzare un modulo [!DNL Microsoft Word Template] per unire dati provenienti da più servizi Web in un documento [!DNL Microsoft Word].

È possibile, ad esempio, utilizzare questo modello [!DNL Microsoft Word]:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-before-filled-350x62.png)

Per creare questo documento:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-exampled-filled-350x85.png)

## Informazioni sui tag dei valori

Un modello [!DNL Microsoft Word] è un normale documento [!DNL Microsoft Word] (file .docx) con tag speciali nel testo che determinano dove e come unire o compilare i dati. Esistono tre tipi di tag:

* [Tag valore semplice](#simple-value-tag)
* [Tag condizione](#condition-tag)
* [Tag loop](#loop-tag)

### Tag valore semplice {#simple-value-tag}

Un tag di valore semplice viene semplicemente sostituito con un valore corrispondente. Il nome del tag corrisponde al valore del campo [!UICONTROL Key], che viene inserito all&#39;interno di parentesi graffe doppie, ad esempio `{{name}}`.

**Esempio:** Per creare un documento con la dicitura &quot;Ciao, Petr!&quot;, puoi utilizzare un modulo [!DNL Microsoft Word Template] per creare il seguente modello:

```
> Hi {{name}}!
```

A questo scopo, imposta il modulo come segue:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-simple-value-350x286.png)

### Tag condizione {#condition-tag}

È possibile utilizzare un tag condizione per racchiudere il testo di cui eseguire il rendering solo quando vengono soddisfatte determinate condizioni. Per racchiudere il testo, posizionalo tra i tag della condizione di apertura e chiusura, ad esempio &quot;hasPhone&quot; se la condizione è se i dati includono o meno un numero di telefono. Il nome di un tag di apertura è preceduto da un hash sign #, il nome di un tag di chiusura è preceduto da una barra /, come mostrato nell&#39;esempio seguente.

**Esempio:** Per produrre un documento che includa il numero di telefono di un cliente se i dati di input includono un numero di telefono, ma nessun indirizzo e-mail, è possibile utilizzare un modulo [!DNL Microsoft Word Template] e creare il seguente modello:

```
> {{#hasPhone}}Phone: {{phone}} {{/hasPhone}}
> {{#hasEmail}}Email: {{email}} {{/hasEmail}}
```

A questo scopo, imposta il modulo come segue:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-conditional-350x501.png)

Nel documento, il numero di telefono apparirà come segue:

```
> Phone: 4445551234
```

### Tag loop {#loop-tag}

Per ripetere una sezione di testo, è possibile utilizzare un tag loop, noto anche come tag di sezione. Racchiudi il testo posizionandolo tra i tag loop di apertura e chiusura. Il nome di un tag di apertura è preceduto da un hash sign #; il nome di un tag di chiusura è preceduto da una barra /.

* [Esegui ciclo con Compila un modulo documento](#loop-tag-with-fill-out-a-document-module)
  <!-- [Loop tag with Fill a document with a batch of data module](#loop-tag-with-fill-a-document-with-a-batch-of-data-module)-->

#### Collega tag con Compila un modulo documento {#loop-tag-with-fill-out-a-document-module}

**Esempio:** Per produrre un documento che elenca il nome e il numero di telefono di ciascun contatto in un elenco clienti, è possibile utilizzare un modulo [!DNL Microsoft Word Template] e creare il seguente modello:

```
> {{#contact}}
>     {{name}}, {{phone}}
> {{/contact}}
```

A questo scopo, imposta il modulo come segue:


![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-fill-out-a-document-350x732.png)

Il modulo crea il seguente documento:

```
> Jan Toman, 4445551234
> Eduard Salo, 4445552345
```

<!--

#### Loop tag with Fill a document with a batch of data module {#loop-tag-with-fill-a-document-with-a-batch-of-data-module}

**Example:** You can export Google contacts into a table that you create using loop tags.

The first module loads the template. The next module retrieves all contacts from the group you specify in [!DNL Google Contacts]. The aggregator module aggregates all values retrieved from Google Contacts and merges them into the template. And the last module saves the filled template to the desired location.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-scenario-350x124.png)

You could use this scenario with the following template:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-template-350x26.png)

To do this, you would set up the module as follows:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-module-setup-350x323.png)

The module would create the following document:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-document-350x46.png)
-->

## [!DNL Microsoft Word Template] moduli

Questi moduli non richiedono una connessione.

* [Compila un documento](#fill-out-a-document)
* [Riempire un documento con un batch di dati](#fill-a-document-with-a-batch-of-data)

### [!UICONTROL Fill out a document] {#fill-out-a-document}

Questo modulo di trasformazione consente di riempire un documento con i dati specificati. Può essere utilizzato con tag di valori semplici, tag condizionali o tag di loop.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Immettere il carattere o i caratteri che si desidera contrassegnare come inizio del testo da sostituire. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>Immettere <code>&#91;&#91;</code> se si desidera sostituire un testo simile al seguente: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Immettere il carattere o i caratteri che si desidera contrassegnare come fine del testo da sostituire. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>Immettere <code>&#93;&#93;</code> se si desidera sostituire un testo simile al seguente: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Mappa il file che desideri caricare dal modulo precedente (ad esempio, HTTP &gt; Ottieni un file o un Dropbox &gt; Ottieni un modulo file). In alternativa, immettere manualmente il file di dati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Immettere un nome di file (con estensione) per il file di output di destinazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>Selezionare un'opzione per indicare se i dati utilizzati provengono da un modulo o da una raccolta di dati non elaborati (dati non elaborati del computer).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Deve essere un array di raccolte, in cui:</p> 
    <ul> 
     <li>Ogni raccolta corrisponde a una voce di dati e contiene un elemento <code>entry</code></li> 
     <li>L'elemento <code>entry </code> contiene una raccolta di <code>key </code> e <code>value</code></li> 
     <li>L'elemento <code>key </code> contiene il nome del tag</li> 
     <li>l'elemento <code>value </code> contiene il valore del tag</li> 
    </ul> 
    <p>Per aggiungere una voce:</p>
    <ol> 
     <li> Fare clic su <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Selezionare il tipo di valore della voce.</li> 
     <li>Aggiungi nome e valore. Per ulteriori informazioni, consulta l’esempio per il tipo di valore scelto in questo articolo. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Tag valore semplice</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Tag condizione</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Tag loop</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Fill a document with a batch of data] {#fill-a-document-with-a-batch-of-data}

Questo modulo di aggregazione è utile se i dati inseriti vengono forniti come bundle separati. Con questo modulo, puoi facilmente impostare la struttura richiesta per il campo Valore e mappare gli elementi a ciascun elemento di valore. A differenza del modulo Compila un documento, il campo Valori del modulo Compila un documento con un batch di dati consente una sola voce contenente variabili.

Puoi utilizzare questo modulo anche se le voci di dati vengono fornite come array, utilizzando il modulo *Iterator* per trasformare il contenuto dell&#39;array in una serie di bundle.

I valori effettivi vengono creati e compilati per ogni bundle in ingresso. Il modello viene prodotto dopo l’elaborazione di tutti i bundle di input.

Questo modulo di aggregazione è particolarmente utile per la creazione di elenchi o rapporti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Selezionare il modulo che costituisce l'origine del testo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Immettere il carattere o i caratteri che si desidera contrassegnare come inizio del testo da sostituire. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>Immettere <code>&#91;&#91;</code> se si desidera sostituire un testo simile al seguente: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Immettere il carattere o i caratteri che si desidera contrassegnare come fine del testo da sostituire. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>Immettere <code>&#93;&#93;</code> se si desidera sostituire un testo simile al seguente: <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td> Definisci un’espressione contenente uno o più elementi mappati. I dati aggregati vengono separati in Gruppi con il valore della stessa espressione. Ogni gruppo restituisce come bundle separato contenente una Chiave con l’espressione valutata e il testo aggregato. In questo modo, puoi utilizzare la Chiave come filtro nei moduli successivi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Abilita questa opzione per interrompere l’elaborazione quando un’aggregazione non contiene bundle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Mappa il file che desideri caricare dal modulo precedente (ad esempio, HTTP &gt; Ottieni un file o un Dropbox &gt; Ottieni un modulo file). In alternativa, immettere manualmente il file di dati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Immettere un nome di file (con estensione) per il file di output di destinazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>Selezionare un'opzione per indicare se i dati utilizzati provengono da un modulo o da una raccolta di dati non elaborati (dati non elaborati del computer).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Deve essere un array di raccolte, in cui:</p> 
    <ul> 
     <li>Ogni raccolta corrisponde a una voce di dati e contiene un elemento <code>entry</code></li> 
     <li>L'elemento <code>entry </code> contiene una raccolta di <code>key </code> e <code>value</code></li> 
     <li>L'elemento <code>key </code> contiene il nome del tag</li> 
     <li>l'elemento <code>value </code> contiene il valore del tag</li> 
    </ul> 
    <p>Per aggiungere una voce:</p>
    <ol> 
     <li> Fare clic su <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Selezionare il tipo di valore della voce.</li> 
     <li>Aggiungi nome e valore. Per ulteriori informazioni, consulta l’esempio per il tipo di valore scelto in questo articolo. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Tag valore semplice</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Tag condizione</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Tag loop</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
