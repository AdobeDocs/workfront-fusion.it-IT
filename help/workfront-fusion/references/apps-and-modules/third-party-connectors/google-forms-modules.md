---
title: Moduli Forms di Google
description: I  [!DNL Adobe Workfront Fusion Google Forms] moduli ti consentono di monitorare, selezionare, aggiungere, aggiornare o eliminare le risposte sul tuo Google Forms.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# [!DNL Google Forms] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL Google Forms] ti consentono di monitorare, selezionare, aggiungere, aggiornare o eliminare le risposte sul tuo [!DNL Google Forms].

Per utilizzare [!DNL Google Docs] con [!DNL Adobe Workfront Fusion], è necessario disporre di un account [!DNL Google]. Se non si dispone ancora di un account [!DNL Google], è possibile crearne uno nella pagina della guida dell&#39;account [!DNL Google].

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

Per utilizzare i moduli [!DNL Google Forms], è necessario disporre di un account [!DNL Google].

## Informazioni API di Google Forms

Il connettore Google Forms utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Creazione di un foglio di calcolo dal modulo

Per utilizzare le risposte del modulo, è necessario creare il foglio di calcolo delle risposte.

1. Aprire il modulo.
1. Passa alla scheda **[!UICONTROL Responses]**.
1. Fare clic sull&#39;icona **[!UICONTROL Create Spreadsheet]** ![](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Seleziona se desideri creare un nuovo foglio di calcolo o un foglio di calcolo esistente
1. Fare clic su **[!UICONTROL Create]**.

## [!DNL Google Forms] moduli e relativi campi

Quando configuri [!DNL Google Forms] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Forms], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Triggers

#### [!UICONTROL Watch Responses]

Controlla il modulo per individuare nuove risposte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selezionare il foglio di calcolo contenente le risposte del modulo che si desidera controllare per individuare le nuove risposte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>Specifica la riga di intestazione della tabella. La riga predefinita è <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Specifica come eseguire il rendering dei valori nell’output.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>I valori vengono calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>I valori vengono calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce il numero <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>I valori non vengono calcolati. La risposta include le formule. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>Seleziona la modalità di rappresentazione di date, ore e durata nell’output. Questo campo viene ignorato se [!UICONTROL Value Render Option] è impostato su [!UICONTROL Formatted Value].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Impostare il numero massimo di risposte con cui [!DNL Workfront Fusion] funziona durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)

#### [!UICONTROL Add a Response]

Questo modulo aggiunge una nuova risposta alla parte inferiore del foglio di calcolo del modulo.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selezionare il foglio di calcolo contenente il foglio in cui si desidera aggiungere una risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Immetti i valori desiderati nelle colonne del foglio.</p> <p>Per la colonna [!UICONTROL Timestamp] nel formato corretto, utilizzare il valore seguente:</p><pre>formatDate(now;GG/MM/AAAA HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> I valori immessi dall’utente non vengono analizzati e vengono memorizzati così come sono. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>I valori vengono analizzati come se l’utente li avesse digitati nell’interfaccia utente. I numeri rimangono numeri, ma le stringhe possono essere convertite in numeri, date o altri formati seguendo le stesse regole applicate quando si immette testo in una cella tramite l'interfaccia utente [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>Specifica come vengono modificati i dati esistenti quando vengono immessi nuovi dati. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>I nuovi dati sovrascrivono quelli esistenti nelle aree in cui vengono scritti. L'aggiunta di dati alla fine del foglio consente di inserire nuove righe o colonne in modo da poter scrivere i dati.</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>Le righe vengono inserite per i nuovi dati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

Questo modulo aggiorna la risposta selezionata.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selezionare il foglio di calcolo contenente il foglio in cui si desidera aggiornare una risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Immettere o mappare il numero della riga da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Immettere i nuovi valori nelle colonne desiderate.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> I valori immessi dall’utente non vengono analizzati e vengono memorizzati così come sono. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>I valori vengono analizzati come se l’utente li avesse digitati nell’interfaccia utente. I numeri rimangono numeri, ma le stringhe possono essere convertite in numeri, date o altri formati seguendo le stesse regole applicate quando si immette testo in una cella tramite l'interfaccia utente [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

Questo modulo elimina una risposta selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selezionare il foglio di calcolo contenente il foglio in cui si desidera eliminare una risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Immettere o mappare il numero della riga da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses]

Questo modulo restituisce le risposte che corrispondono ai criteri specificati.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Connessione</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selezionare il modulo in cui eseguire la ricerca.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> Selezionare l'intervallo di colonne che si desidera cercare.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Definisci il filtro in base al quale desideri cercare le risposte.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>Seleziona se ordinare le risposte restituite in ordine crescente o decrescente.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> Selezionare la colonna in base alla quale ordinare le risposte restituite.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Specifica come eseguire il rendering dei valori nell’output.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>I valori vengono calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>I valori vengono calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce il numero <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>I valori non vengono calcolati. La risposta include le formule. Ad esempio, se <code>A1</code> è <code>1. 23</code> e <code>A2 </code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituisce <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>Seleziona la modalità di rappresentazione di date, ore e durata nell’output. Questo campo viene ignorato se l'opzione [!UICONTROL Value Render] è impostata su Valore formattato. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> Impostare il numero massimo di risposte restituite da [!DNL Workfront Fusion] durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)]

Questo modulo esegue una ricerca utilizzando [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage). Questo modulo non restituisce un numero di riga.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selezionare il foglio di calcolo contenente il foglio che si desidera cercare.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Selezionare il foglio contenente le risposte del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Definire la query di ricerca utilizzando <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>.</p> <p>Esempio: <code>select * where C = "John"</code> recupera tutti i valori per la riga in cui la colonna C è "John".</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> Impostare il numero massimo di risposte restituite da [!DNL Workfront Fusion] durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>
