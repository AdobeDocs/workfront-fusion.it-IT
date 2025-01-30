---
title: Moduli JSON
description: L’app JSON per Adobe Workfront Fusion fornisce moduli per elaborare i dati in formato JSON, in modo che Adobe Workfront Fusion possa lavorare ulteriormente con il contenuto dei dati o creare nuovi contenuti JSON.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 0%

---

# [!UICONTROL JSON] moduli

L&#39;app [!DNL Adobe Workfront Fusion] [!UICONTROL JSON] fornisce moduli per elaborare i dati in formato JSON in modo che [!DNL Adobe Workfront Fusion] possa lavorare ulteriormente con il contenuto dei dati o creare nuovo contenuto JSON.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Considerazioni durante l’analisi del codice JSON

* [Struttura dati](#data-structure)
* [Confronto tra raccolta e array](#collection-vs-array)

### Struttura dei dati

La struttura dati descrive come sono organizzati i dati JSON e consente la mappatura di singoli elementi JSON ad altri moduli nello scenario. Se non fornisci la struttura dati, puoi eseguire manualmente il modulo e [!DNL Workfront Fusion] creerà la struttura dal JSON fornito:

1. Aggiungi il modulo [!UICONTROL Parse JSON] a uno scenario.
1. Nel campo **[!UICONTROL JSON String]**, immetti il JSON da cui desideri creare una struttura di dati.
1. Non connettere altri moduli al modulo [!UICONTROL Parse JSON]. Poiché [!DNL Workfront Fusion] non conosce ancora la struttura dei dati JSON, non è ancora possibile mappare i dati dal modulo [!UICONTROL Parse JSON] ad altri moduli nello scenario.
1. Esegui manualmente lo scenario. Questo consente al modulo [!UICONTROL Parse JSON] di identificare la struttura JSON dal JSON fornito.
1. È ora possibile collegare i seguenti moduli. Gli elementi del modulo JSON di analisi sono ora disponibili per la mappatura.

Per ulteriori informazioni, vedere [Strutture dati in [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Confronto tra raccolta e array

Se il campo stringa JSON contiene una raccolta `{ ... }`, l&#39;output è un singolo bundle contenente gli elementi della raccolta.

>[!BEGINSHADEBOX]

**Esempio:**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![Raccolta JSON](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

Se il campo stringa JSON contiene un array `[ ... ]`, l&#39;output è una serie di bundle. ogni bundle contiene un elemento dell’array.

>[!BEGINSHADEBOX]

**Esempio:**

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![Array JSON](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## [!UICONTROL JSON] moduli e relativi campi

Quando configuri [!DNL JSON] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi JSON aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Converti JSON in XML](#convert-json-to-xml)
* [Analizza JSON](#parse-json)
* [Crea JSON](#create-json)
* [Trasforma JSON](#transform-json)

### Aggregatori

#### [!UICONTROL Aggregate to JSON]

Questo modulo aggregatore aggrega l’output di un modulo precedente in JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module] </td> 
   <td> <p>Seleziona il modulo che restituisce i dati da aggregare in JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Seleziona la struttura dati da utilizzare per creare JSON. La struttura dati determina quali altri campi sono disponibili in questo modulo. Per ulteriori informazioni, vedere <a href="#data-structure" class="MCXref xref">Struttura dati</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indentation]</td> 
   <td> <p> Seleziona se desideri applicare un rientro al JSON utilizzando schede, due spazi o quattro spazi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td>Definire un'espressione in base alla quale raggruppare l'output aggregato. Questa espressione può contenere uno o più elementi mappati. I dati aggregati vengono quindi separati in gruppi utilizzando il valore di questa espressione. Ogni gruppo produce come bundle separato con una chiave (l’espressione valutata) e un valore (il testo aggregato). Puoi utilizzare la chiave come filtro nei moduli successivi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Abilita questa opzione per interrompere lo scenario quando non ci sono risultati.</td> 
  </tr> 
 </tbody> 
</table>

### Trasformatori

* [Converti JSON in XML](#convert-json-to-xml)
* [Crea JSON](#create-json)
* [Analizza JSON](#parse-json)
* [Trasforma JSON](#transform-json)

#### [!UICONTROL Convert JSON to XML]

Questo modulo di azione converte una stringa JSON in XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Immetti o mappa il JSON da convertire in XML.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create JSON]

Questo modulo di azione crea JSON da una struttura di dati.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Struttura dei dati</td> 
   <td> <p>Seleziona la struttura dati da utilizzare per creare JSON. Per ulteriori informazioni, vedere <a href="#data-structure" class="MCXref xref">Struttura dati</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rientro</td> 
   <td> <p>Seleziona il rientro da utilizzare per questo JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Parse JSON]

Questo modulo di azione analizza una stringa JSON in una struttura di dati, consentendo di accedere ai dati all’interno della stringa JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Seleziona la struttura dati da utilizzare per creare JSON. Per ulteriori informazioni, vedere <a href="#data-structure" class="MCXref xref">Struttura dati</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Immetti o mappa il JSON da analizzare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Transform JSON]

Questo modulo di azione trasforma un oggetto in una stringa json.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Rientro</td> 
   <td> <p>Seleziona il rientro da utilizzare per questo JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object]</td> 
   <td> <p>Inserisci o mappa l’oggetto da trasformare in JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Trasformazione dei record di dati in JSON

>[!BEGINSHADEBOX]

**Esempio:** Nell&#39;esempio seguente viene illustrato come trasformare i record di dati da [!DNL Google Sheets] in formato JSON:

1. Inserisci il modulo [!DNL Google Sheets] > [!UICONTROL Select rows] nello scenario per recuperare i dati. Configurare il modulo per recuperare le righe dal foglio di calcolo [!DNL Google]. Impostare il valore&#x200B;**[!UICONTROL Maximum number of returned rows]** su un numero piccolo, ma maggiore di uno a scopo di test (ad esempio, tre). Eseguire il modulo [!DNL Google Sheets] facendo clic con il pulsante destro del mouse su di esso e scegliendo &quot;**[!UICONTROL Run this module only]**&quot;. Verifica l’output del modulo.

1. Connetti il modulo [!UICONTROL Array Aggregator] dopo il modulo [!DNL Google Sheets]. Nella configurazione del modulo, scegliere il modulo [!DNL Google Sheets] nel campo **[!UICONTROL Source node]**. Lascia gli altri campi così come sono per il momento.

1. Connetti il modulo [!UICONTROL JSON] > [!UICONTROL Create JSON] dopo il modulo [!UICONTROL Array Aggregator]. La configurazione del modulo richiede una struttura dati che descriva il formato JSON. Fare clic su **[!UICONTROL Add]** per aprire la configurazione della struttura dati. Il modo più semplice per creare questa struttura dati è generarla automaticamente da un campione JSON. Fai clic su **[!UICONTROL Generator]** e incolla l&#39;esempio JSON nel campo **[!UICONTROL Sample data]**:

   **Esempio:**

   ```
   {
   "books": [
   {
   "id": "ID",
   "title": "Title",
   "author": "Author"
   }
   ]
   }
   ```

1. Fare clic su **[!UICONTROL Save]**. Il campo [!UICONTROL Specification] nella struttura dati ora contiene la struttura generata.
1. Modificare il nome della struttura dati in un nome più specifico e fare clic su **[!UICONTROL Save]**. Un campo corrispondente all’attributo dell’array principale viene visualizzato come campo mappabile nella configurazione del modulo JSON.

1. Fare clic sul pulsante **[!UICONTROL Map]** accanto al campo e mappare l&#39;elemento `Array[]` dell&#39;output dell&#39;aggregatore di array su di esso.

1. Fare clic su **[!UICONTROL OK]** per chiudere la configurazione del modulo [!UICONTROL JSON].

1. Aprire la configurazione del modulo [!UICONTROL Array Aggregator]. Modificare **[!UICONTROL Target structure]** da [!UICONTROL Custom] nel campo del modulo [!UICONTROL JSON] corrispondente all&#39;attributo di matrice radice. Mappare gli elementi dal modulo [!DNL Google Sheets] ai campi appropriati.

1. Fare clic su **[!UICONTROL OK]** per chiudere la configurazione del modulo [!UICONTROL Array Aggregator].

1. Esegui lo scenario.

   Il modulo [!UICONTROL JSON] restituisce il formato JSON corretto.

1. Aprire la configurazione del modulo [!DNL Google Sheets] e aumentare il numero di [!UICONTROL Maximum number of returned rows] affinché sia maggiore del numero di righe nel foglio di calcolo per elaborare tutti i dati.

>[!ENDSHADEBOX]

## Risoluzione dei problemi

### Impossibile mappare i dati dal modulo [!UICONTROL Parse JSON]

Verificare che il contenuto JSON sia mappato correttamente nel modulo [!UICONTROL Parse JSON] e che la struttura dati sia definita correttamente. Per ulteriori informazioni, vedere [Trasformazione dei record di dati in JSON](#transforming-data-records-to-json) in questo articolo.

### Il modulo genera un errore quando si utilizzano istruzioni condizionali in JSON

Quando si utilizzano istruzioni condizionali come `if` nel JSON, inserire le virgolette al di fuori dell&#39;istruzione condizionale.

>[!BEGINSHADEBOX]

**Esempio:**

![Virgolette in JSON](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
