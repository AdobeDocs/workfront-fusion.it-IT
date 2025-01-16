---
title: Moduli Google Sheets
description: Per utilizzare  [!DNL Google Sheets] con [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] estensione (facoltativo, ma richiesto per i trigger istantanei).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3367'
ht-degree: 0%

---

# [!DNL Google Sheets] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Google Sheets] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla connessione dell&#39;account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere [Creare una connessione a  [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

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

Per utilizzare i moduli [!UICONTROL Google Sheets], è necessario disporre di un account [!UICONTROL Google].

## Informazioni API per i fogli di Google

Il connettore Google Sheets utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Triggers

### [!UICONTROL Watch Rows]

Recupera i valori da ogni riga appena aggiunta nel foglio di calcolo.

Il modulo recupera solo le nuove righe che non sono state compilate in precedenza. Il trigger non elaborerà una riga sovrascritta.

>[!IMPORTANT]
>
>Se il foglio di lavoro contiene una riga vuota, non verrà elaborata alcuna riga dopo la riga vuota.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo contenente il foglio che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio da controllare per una nuova riga.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table contains headers]</td> 
   <td> <p> Selezionare se il foglio di calcolo contiene la riga di intestazione.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Il modulo non recupera la riga di intestazione come dati di output. </p> <p>I nomi delle variabili nell’output vengono richiamati dalle intestazioni.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Il modulo recupera anche la prima riga della tabella</p> <p>I nomi delle variabili nell'output sono denominati A, B, C, D e così via.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers] </td> 
   <td> <p>Immettere l'intervallo della riga di intestazione. Ad esempio, <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First table row]</td> 
   <td> <p>Immettere l'intervallo della prima riga della tabella. Ad esempio, <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Value render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>I valori verranno calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"$1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>I valori verranno calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirà il numero <code>"1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>I valori non verranno calcolati. La risposta includerà le formule. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"=A1"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Date and time render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come duplicati in formato "numero seriale", come reso popolare da Lotus 1-2-3. La porzione del numero intero del valore (a sinistra del decimale) conta i giorni dal 30 dicembre 1899. La parte frazionaria (a destra del decimale) conta l’ora come frazione del giorno. Ad esempio, il 1 gennaio 1900 a mezzogiorno sarebbe 2,5, 2 perché sono 2 giorni dopo il 30 dicembre 1899, e 0,5 perché mezzogiorno è mezza giornata. Il primo febbraio 1900 alle 15:00 sarebbe il 33.625. Questo considera correttamente l'anno 1900 come non un anno bisestile.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come stringhe nel formato numero specificato (che dipende dalle impostazioni internazionali del foglio di calcolo).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di risultati con cui [!DNL Workfront Fusion] lavorerà durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Azioni

* [[!UICONTROL Add a Row]](#add-a-row)
* [[!UICONTROL Update a Row]](#update-a-row)
* [[!UICONTROL Clear a Row]](#clear-a-row)
* [[!UICONTROL Delete a Row]](#delete-a-row)
* [[!UICONTROL Get a Cell]](#get-a-cell)
* [[!UICONTROL Update a Cell]](#update-a-cell)
* [[!UICONTROL Clear a Cell]](#clear-a-cell)
* [[!UICONTROL Add a Sheet]](#add-a-sheet)
* [[!UICONTROL Create a Spreadsheet]](#create-a-spreadsheet)
* [[!UICONTROL Delete a Sheet]](#delete-a-sheet)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

### [!UICONTROL Add a Row]

Questo modulo aggiunge una riga a un foglio.

Quando configuri [!DNL Google Sheets] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Sheets], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Specificare se si desidera selezionare il foglio di calcolo e il foglio manualmente o mediante mapping.</p> <p>Nota: la mappatura manuale è utile, ad esempio, quando si crea un nuovo foglio di calcolo in uno scenario [!DNL Workfront Fusion] e si desidera aggiungere dati nel nuovo foglio di calcolo direttamente nello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio a cui si desidera aggiungere una riga.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Range]</td> 
   <td>Selezionare l'intervallo di colonne che si desidera utilizzare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selezionare se il foglio di calcolo contiene la riga di intestazione.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Il modulo non recupera la riga di intestazione come dati di output. </p> <p>I nomi delle variabili nell’output vengono richiamati dalle intestazioni.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Il modulo recupera anche la prima riga della tabella</p> <p>I nomi delle variabili nell'output sono denominati A, B, C, D e così via.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Immetti o mappa le celle desiderate della riga da aggiungere.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>I valori vengono analizzati come se l’utente li avesse digitati nell’interfaccia utente. I numeri rimangono numeri, ma le stringhe possono essere convertite in numeri, date o altri formati seguendo le stesse regole applicate quando si immette testo in una cella tramite l'interfaccia utente [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> I valori immessi dall’utente non vengono analizzati e vengono memorizzati così come sono. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert data option]</td> 
   <td> <p>Specifica come vengono modificati i dati esistenti quando vengono immessi nuovi dati. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>Le righe vengono inserite per i nuovi dati.</p> </li> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>I nuovi dati sovrascrivono quelli esistenti nelle aree in cui vengono scritti. L'aggiunta di dati alla fine del foglio consente di inserire nuove righe o colonne in modo da poter scrivere i dati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Row]

Questo modulo consente di modificare il contenuto della cella in una riga selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Specificare se si desidera selezionare il foglio di calcolo e il foglio manualmente o mediante mapping.</p> <p>Nota: la mappatura manuale è utile, ad esempio, quando si crea un nuovo foglio di calcolo nello scenario [!UICONTROL Workfront Fusion] e si desidera aggiungere dati al nuovo foglio di calcolo direttamente nello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio in cui si desidera aggiornare una riga.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p> Immettere il numero della riga da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selezionare se il foglio di calcolo contiene la riga di intestazione.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>Il modulo non recupera la riga di intestazione come dati di output. </p> <p>I nomi delle variabili nell’output vengono richiamati dalle intestazioni.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>Il modulo recupera anche la prima riga della tabella</p> <p>I nomi delle variabili nell'output sono denominati A, B, C, D e così via.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Immettere o mappare i valori alle celle desiderate della riga che si desidera modificare (aggiornare).</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>I valori vengono analizzati come se l’utente li avesse digitati nell’interfaccia utente. I numeri rimangono numeri, ma le stringhe possono essere convertite in numeri, date o altri formati seguendo le stesse regole applicate quando si immette testo in una cella tramite l'interfaccia utente [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> I valori immessi dall’utente non vengono analizzati e vengono memorizzati così come sono. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Row]

Elimina i valori da una riga specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google] contenente il foglio da cui si desidera cancellare una riga.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p> Selezionare il foglio da cui si desidera cancellare i dati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p>Immettere il numero della riga da cui si desidera cancellare i dati. Ad esempio, <code> 23</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Row]

Elimina una riga specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo di Google contenente il foglio da cui si desidera eliminare una riga.</p> </td> 
  </tr> 
  <tr> 
   <td>Foglio </td> 
   <td> <p>Selezionare il foglio da cui si desidera eliminare una riga.</p> </td> 
  </tr> 
  <tr> 
   <td>Numero riga</td> 
   <td> <p>Immettere il numero della riga che si desidera eliminare. Esempio: <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a Cell]

Recupera un valore da una cella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio contenente la cella da cui si desidera recuperare i dati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Immettere l'ID della cella da cui si desidera recuperare i dati. Esempio: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>I valori verranno calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"$1.23"</code>.</p> <p style="font-weight: bold;">[!DNL Unformatted value]</p> <p>I valori verranno calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirà il numero <code>"1.23"</code>.</p> <p style="font-weight: bold;">[!DNL Formula]</p> <p>I valori non verranno calcolati. La risposta includerà le formule. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"=A1"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!DNL Serial number]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come duplicati in formato "numero seriale", come reso popolare da Lotus 1-2-3. La porzione del numero intero del valore (a sinistra del decimale) conta i giorni dal 30 dicembre 1899. La parte frazionaria (a destra del decimale) conta l’ora come frazione del giorno. Ad esempio, il 1 gennaio 1900 a mezzogiorno sarebbe 2,5, 2 perché sono 2 giorni dopo il 30 dicembre 1899, e 0,5 perché mezzogiorno è mezza giornata. Il primo febbraio 1900 alle 15:00 sarebbe il 33.625. Questo considera correttamente l'anno 1900 come non un anno bisestile.</p> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come stringhe nel formato numero specificato (che dipende dalle impostazioni internazionali del foglio di calcolo).</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Cell]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Immettere l'ID della cella da aggiornare. Esempio: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td> <p>Immettere il nuovo valore per la cella.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>I valori vengono analizzati come se l’utente li avesse digitati nell’interfaccia utente. I numeri rimangono numeri, ma le stringhe possono essere convertite in numeri, date o altri formati seguendo le stesse regole applicate quando si immette testo in una cella tramite l'interfaccia utente [!DNL Google Sheets].</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> I valori immessi dall’utente non vengono analizzati e vengono memorizzati così come sono. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Cell]

Elimina un valore da una cella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo di Google contenente il foglio da cui si desidera cancellare una cella.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio da cui si desidera cancellare una cella.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Immettere l'ID della cella che si desidera cancellare. Esempio: <code>A5</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Add a Sheet]

Crea un nuovo foglio in un foglio di calcolo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo Google in cui si desidera aggiungere un foglio.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Properties]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Title]</p> <p>Immettere il nome del nuovo foglio.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Index]</p> <p>Immettere la posizione del foglio. Il valore di default è 0 (posiziona il foglio al primo posto)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a Spreadsheet]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>Immettere il nome di un nuovo foglio di calcolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Locale]</td> 
   <td> <p>Immettere le impostazioni locali del foglio di calcolo in uno dei seguenti formati:</p> 
    <ul> 
     <li>un codice lingua ISO 639-1 come <code>en</code></li> 
     <li>un codice del linguaggio ISO 639-2 come <code>haw</code>, se non esiste alcun codice 639-1</li> 
     <li>una combinazione del codice della lingua ISO e del codice del paese, come <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recalculation interval]</td> 
   <td> <p>Quantità di tempo di attesa prima del ricalcolo delle funzioni volatili:</p> <p style="font-weight: bold;">[!UICONTROL On change]</p> <p>Le funzioni volatili vengono aggiornate a ogni modifica.</p> <p style="font-weight: bold;">[!UICONTROL On change and every minute]</p> <p>Le funzioni volatili vengono aggiornate a ogni cambiamento e ogni minuto.</p> <p style="font-weight: bold;">[!UICONTROL On change and hourly]</p> <p>Le funzioni volatili vengono aggiornate a ogni modifica e ogni ora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Time zone]</td> 
   <td> <p> Seleziona il fuso orario del foglio di calcolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Number format]</td> 
   <td> <p>Selezionare il formato predefinito di tutte le celle del foglio di calcolo.</p> <p><strong>[!UICONTROL Text]</strong>: formattazione del testo. Esempio: <code>1000. 12</code></p> <p><strong>[!UICONTROL Number]</strong>: formattazione dei numeri. Esempio: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: formattazione percentuale. Esempio: <code>10. 12%</code></p> <p><strong>[!UICONTROL Currency]</strong>: formattazione della valuta. Esempio: <code>$1,000.12</code></p> <p><strong>[!UICONTROL Date]</strong>: formattazione della data. Esempio: <code>9/26/2008</code></p> <p><strong>[!UICONTROL Time]</strong>: formattazione del tempo. Esempio: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL Date time]</strong>: formattazione di data e ora. Esempio: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>Formattazione scientifica dei numeri. Esempio: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheets] </td> 
   <td> <p>Fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere un foglio al foglio di calcolo. Per ogni foglio, immettere o mappare un titolo per il foglio e l'indice del foglio. Un indice pari a 0 rappresenta il primo foglio.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Sheet]

Elimina un foglio specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio che si desidera eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Make an API Call]

Questo modulo di azione ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [Fusion App] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Immettere un percorso relativo a <code>https://sheets.googleapis.com/v4/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:   <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ricerche

* [[!UICONTROL Search Rows]](#search-rows)
* [[!UICONTROL Search Rows (Advanced)]](#search-rows-advanced)
* [[!UICONTROL Get Range Values]](#get-range-values)
* [[!UICONTROL List Sheets]](#list-sheets)

### [!UICONTROL Search Rows]

Cerca le righe utilizzando le opzioni di filtro.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [Fusion App] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Seleziona il foglio in cui desideri cercare le righe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selezionare se il foglio di calcolo contiene la riga di intestazione. Se è selezionata l'opzione [!UICONTROL Yes], il modulo non recupera la riga di intestazione in quanto i dati di output e i nomi delle variabili nell'output vengono quindi chiamati dalle intestazioni. Se è selezionata l'opzione [!UICONTROL No], il modulo recupera anche la prima riga della tabella e i nomi delle variabili nell'output vengono quindi chiamati solo A, B, C, D e così via.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column range]</td> 
   <td>Seleziona l’intervallo di colonne su cui lavorare. Esempio: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter]</td> 
   <td> <p>Impostare il filtro per la riga in base alla quale eseguire la ricerca.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort order]</td> 
   <td>Seleziona se desideri ordinare in modo crescente o decrescente.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td>Scegliere la colonna in base alla quale si desidera eseguire l'ordinamento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>I valori verranno calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"$1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>I valori verranno calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirà il numero <code>"1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>I valori non verranno calcolati. La risposta includerà le formule. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"=A1"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come duplicati in formato "numero seriale", come reso popolare da Lotus 1-2-3. La porzione del numero intero del valore (a sinistra del decimale) conta i giorni dal 30 dicembre 1899. La parte frazionaria (a destra del decimale) conta l’ora come frazione del giorno. Ad esempio, il 1 gennaio 1900 a mezzogiorno sarebbe 2,5, 2 perché sono 2 giorni dopo il 30 dicembre 1899, e 0,5 perché mezzogiorno è mezza giornata. Il primo febbraio 1900 alle 15:00 sarebbe il 33.625. Questo considera correttamente l'anno 1900 come non un anno bisestile.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come stringhe nel formato numero specificato (che dipende dalle impostazioni internazionali del foglio di calcolo).</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned rows]</td> 
   <td>Impostare il numero massimo di righe che [!DNL Workfront Fusion] restituirà durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Rows (Advanced)]

Restituisce risultati che corrispondono ai criteri specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo di Google contenente il foglio che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio contenente le righe da cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Utilizza [!DNL Google Charts Query Language]. Esempio: <code>select * where B = "John"</code></p> <p>Per ulteriori informazioni su [!DNL Google Charts Query Language], vedere <a href="https://developers.google.com/chart/interactive/docs/querylanguage">Riferimento linguaggio query</a> nella documentazione di [!DNL Google].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get Range Values]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selezionare il foglio da cui si desidera ottenere il contenuto dell'intervallo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Range] </td> 
   <td> <p>Immettere l'intervallo che si desidera ottenere. Esempio: <code>A1:D25</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p>Selezionare questa casella se il foglio contiene una riga di intestazione</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row with headers]</td> 
   <td>Immetti l’intervallo delle intestazioni della tabella. Esempio <code>A1:F1</code>. Se si lascia vuoto il campo, [!DNL Workfront Fusion] supporrà che l'intestazione si trovi nella prima riga dell'intervallo specificato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>I valori verranno calcolati e formattati nella risposta in base alla formattazione della cella. La formattazione si basa sulle impostazioni locali del foglio di calcolo, non sulle impostazioni locali dell'utente richiedente. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"$1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>I valori verranno calcolati, ma non formattati nella risposta. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirà il numero <code>"1.23"</code>.</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>I valori non verranno calcolati. La risposta includerà le formule. Ad esempio, se <code>A1</code> è <code>1.23</code> e <code>A2</code> è <code>=A1</code> e formattato come valuta, <code>A2</code> restituirebbe <code>"=A1"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come duplicati in formato "numero seriale", come reso popolare da Lotus 1-2-3. La porzione del numero intero del valore (a sinistra del decimale) conta i giorni dal 30 dicembre 1899. La parte frazionaria (a destra del decimale) conta l’ora come frazione del giorno. Ad esempio, il 1 gennaio 1900 a mezzogiorno sarebbe 2,5, 2 perché sono 2 giorni dopo il 30 dicembre 1899, e 0,5 perché mezzogiorno è mezza giornata. Il primo febbraio 1900 alle 15:00 sarebbe il 33.625. Questo considera correttamente l'anno 1900 come non un anno bisestile.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Indica che i campi di data, ora, dataora e durata devono essere generati come stringhe nel formato numero specificato (che dipende dalle impostazioni internazionali del foglio di calcolo).</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL List Sheets]

Questo modulo restituisce un elenco di tutti i fogli di un foglio di calcolo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Sheets] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selezionare il foglio di calcolo [!DNL Google] contenente i fogli che si desidera elencare.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Limiti di utilizzo

Se si verifica l&#39;errore `429: RESOURCE_EXHAUSTED`, è stato superato il limite di velocità API.

L&#39;API [!DNL Google Sheets] ha un limite di 500 richieste per 100 secondi per progetto e di 100 richieste per 100 secondi per utente. I limiti per le letture e le scritture vengono tracciati separatamente. Non esiste alcun limite di utilizzo giornaliero.

Ulteriori dettagli sono disponibili all&#39;indirizzo [developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits).

## Suggerimenti

* [Come ottenere celle vuote da un  [!DNL Google]  foglio](#how-to-get-empty-cells-from-a-google-sheet)
* [Aggiungere un pulsante in un foglio per eseguire uno scenario](#add-a-button-in-a-sheet-to-run-a-scenario)

### Come ottenere celle vuote da un [!DNL Google Sheet]

Utilizza il modulo [!UICONTROL Search Rows (Advanced)] e utilizza questa formula per ottenere le colonne vuote.
<pre>seleziona * dove E è nullo</pre>Qui "E" è la colonna e "è nullo" è la condizione. Puoi creare una query più avanzata utilizzando [Google Query Lang](https://developers.google.com/chart/interactive/docs/querylanguage).

### Aggiungere un pulsante in un foglio per eseguire uno scenario

1. In [!DNL Workfront Fusion], inserisci il modulo/trigger **[!UICONTROL Webhook]** > **[!UICONTROL Custom webhooks]** nello scenario e configuralo (vedi [Webhook](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)).

1. Copia l’URL del webhook.
1. Esegui lo scenario.
1. In Google Sheets, scegliere **[!UICONTROL Insert]** > **[!UICONTROL Drawing]**... dalla barra del menu principale.

1. Nella finestra [!UICONTROL Drawing], fare clic sull&#39;icona ![](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png) di **[!UICONTROL Text box]** nella parte superiore della finestra.
1. Progetta un pulsante e fai clic sul pulsante **[!UICONTROL Save and Close]** nell&#39;angolo in alto a destra:
1. Il pulsante verrà inserito nel foglio di lavoro. Fai clic sui tre punti verticali nell’angolo in alto a destra del pulsante:
1. Scegli **[!UICONTROL Assign script..].** dal menu.
1. Immettere il nome dello script (funzione), ad esempio `runScenario` e fare clic su **[!UICONTROL OK]**:
1. Scegliere **[!UICONTROL Tools]** > **[!UICONTROL Script editor]** dalla barra del menu principale.

1. Inserire il codice seguente:

   * Il nome della funzione deve corrispondere al nome specificato nel passaggio 9.
   * Sostituisci l’URL con l’URL del webhook copiato nel passaggio 2.

     <pre>function runScenario() {</pre><pre>UrlFetchApp.fetch("&lt;webhook copiato&gt;");</pre><pre>}</pre>

1. Premere **[!UICONTROL Ctrl+S]** per salvare il file script, immettere il nome di un progetto e fare clic su **[!UICONTROL OK]**.

1. Torna a [!DNL Google Sheets] e fai clic sul nuovo pulsante.
1. Concedi l&#39;autorizzazione richiesta allo script:
1. In [!DNL Workfront Fusion] verificare che lo scenario sia stato eseguito correttamente.

## Memorizzazione delle date in un foglio di calcolo

Se memorizzi un valore Data in un foglio di calcolo senza formattazione, questo verrà visualizzato nel foglio di calcolo come testo in formato ISO 8601. Tuttavia, [!DNL Google Sheets] formule o funzioni che funzionano con date che non comprendono questo testo (esempio: formula `=A1+10`) visualizzeranno il seguente errore:

![](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

Per consentire a [!DNL Google Sheets] di comprendere la data, formattarla con la funzione [[!UICONTROL formatDate] (data; formato; [fuso orario])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatda). Il formato corretto passato alla funzione come secondo argomento dipende dalle impostazioni internazionali del foglio di calcolo.

Per determinare il formato corretto:

1. Scegliere le impostazioni **[!UICONTROL File]** > **[!UICONTROL Spreadsheet]** dal menu principale per verificare/impostare le impostazioni locali.

1. Dopo aver verificato/impostato le impostazioni locali appropriate, determinare il formato di data e ora corrispondente scegliendo **[!UICONTROL Format]** > **[!UICONTROL Number]** dal menu principale. Il formato viene visualizzato accanto alla voce di menu Data e ora:

1. Per comporre il formato corretto da passare alla funzione [!UICONTROL formatDate()], fare riferimento all&#39;elenco di [token per la formattazione della data e dell&#39;ora](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md).

**Esempio:** L&#39;utilizzo del formato `MM/DD/YYYY HH:mm:ss` per le impostazioni locali degli Stati Uniti:

![](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

## Sfruttamento di [!DNL Google Sheets] funzioni

Se si dimentica una funzione incorporata, ma è presente in [!DNL Google Sheets], è possibile sfruttarla. Per ulteriori informazioni, vedere [Utilizzare [!DNL Google Sheets] funzioni](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#exploiti) in [Mappare gli elementi utilizzando le funzioni in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Impedisci a [!DNL Google Sheets] di modificare i numeri in date

È possibile che una stringa di numeri utilizzata come testo venga interpretata come una data in un foglio di lavoro [!DNL Google]. Ad esempio, si digita 1-2019 con l&#39;intento di impostarlo come testo, ma Google lo interpreta come una data. È possibile preformattare il numero come testo normale per impedirlo.

1. In [!DNL Google Sheets], evidenziare la colonna o la cella contenente il numero o i numeri.
1. Fare clic su **[!UICONTROL Format]** > **[!UICONTROL Number]** > **[!UICONTROL Plain text]**.

Un&#39;altra soluzione alternativa in [!DNL Workfront Fusion] consiste nel digitare un apostrofo (&#39;) prima di un numero, ad esempio &#39;1-2019 o &#39;1/47. L&#39;apostrofo non viene visualizzato nella cella dopo l&#39;invio dei dati da [!DNL Workfront Fusion].
