---
title: Funzioni data e ora
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni di data e ora.
author: Becky
feature: Workfront Fusion
exl-id: 92813dac-4bf0-4681-9b71-7bd2e92a89a4
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1879'
ht-degree: 1%

---

# Funzioni data e ora

## Variabili

### now

Ottiene l&#39;ora corrente in formato AAAA-MM-GG-hh:mm:ss.

### timestamp

Ottiene l&#39;ora corrente come marca temporale Unix.

## Funzioni

### [!UICONTROL addSeconds (data; numero)]

Restituisce una nuova data in seguito all’aggiunta di un determinato numero di secondi a una data. Per sottrarre i secondi, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addSeconds(2016-12-08T15:55:57.536Z;2)`

  Restituisce 2016-12-08T15:55:59.536Z

* `addSeconds(2016-12-08T15:55:57.536Z;-2)`

  Restituisce 2016-12-08T15:55:55.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMinutes (data; numero)] {#addminutes-date-number}

Restituisce una nuova data in seguito all’aggiunta di un determinato numero di minuti a una data. Per sottrarre i minuti, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addMinutes(2016-12-08T15:55:57.536Z;2)`

  Restituisce 2016-12-08T15:57:57.536Z

* `addMinutes(2016-12-08T15:55:57.536Z;-2)`

  Restituisce 2016-12-08T15:53:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addHours (date; number)] {#addhours-date-number}

Restituisce una nuova data in seguito all’aggiunta di un determinato numero di ore a una data. Per sottrarre le ore, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addHours(2016-12-08T15:55:57.536Z; 2)`

  Restituisce 2016-12-08T17:55:57.536Z

* `addHours(2016-12-08T15:55:57.536Z;-2)`

  Restituisce 2016-12-08T13:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addDays (data; numero)] {#adddays-date-number}

Restituisce una nuova data come risultato dell’aggiunta di un numero specificato di giorni a una data. Per sottrarre i giorni, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addDays(2016-12-08T15:55:57.536Z;2)`

  Restituisce 2016-12-10T15:55:57.536Z

* `addDays(2016-12-08T15:55:57.536Z;-2)`

  Restituisce 2016-12-6T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMonths (data; numero)]

Restituisce una nuova data in seguito all’aggiunta di un numero specificato di mesi a una data. Per sottrarre i mesi, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addMonths(2016-08-08T15:55:57.536Z;2)`

  Restituisce 2016-10-08T15:55:57.536Z

* `addMonths(2016-08-08T15:55:57.536Z;-2)`

  Restituisce 2016-06-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addYears (data; numero)]

Restituisce una nuova data risultante dall&#39;aggiunta di un numero specificato di anni a una data. Per sottrarre gli anni, immettere un numero negativo.

>[!BEGINSHADEBOX]

**Esempi:**

* `addYears(2016-08-08T15:55:57.536Z;2)`

  Restituisce 2018-08-08T15:55:57.536Z

* `addYears(2016-12-08T15:55:57.536Z; -2)`

  Restituisce 2014-08-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL setSecond (date; number)]

Questa funzione restituisce una nuova data con i secondi specificati nei parametri.

Specificare un numero compreso tra 0 e 59. Se il numero non rientra nell’intervallo, la funzione restituisce un secondo dal minuto precedente (per un numero negativo) o dal minuto successivo (per un numero positivo).

Se devi specificare un numero non compreso nell&#39;intervallo, ti consigliamo di utilizzare [!UICONTROL  addSeconds], come descritto in precedenza nella sezione [addSeconds (date; number)](#addseconds-date-number).

>[!BEGINSHADEBOX]

**Esempi:**

* `setSecond(2015-10-07T11:36:39.138Z;10)`

  Restituisce 2015-10-07T11:36:10.138Z

* `setSecond(2015-10-07T11:36:39.138Z; 61)`

  Restituisce 2015-10-07T11:37:01.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMinute (data; numero)]

Questa funzione restituisce una nuova data con i minuti specificati nei parametri.

Specificare un numero compreso tra 0 e 59. Se il numero non rientra nell’intervallo, la funzione restituisce un minuto dall’ora precedente (per un numero negativo) o dall’ora successiva (per un numero positivo).

Se è necessario specificare un numero non compreso nell&#39;intervallo, è consigliabile utilizzare addMinutes, come descritto in precedenza in [addMinutes (date; number)](#addminutes-date-number).

>[!BEGINSHADEBOX]

**Esempi:**

* `setMinute(2015-10-07T11:36:39.138Z;10)`

  Restituisce 2015-10-07T11:10:39.138Z

* `setMinute(2015-10-07T11:36:39.138Z;61)`

  Restituisce 2015-10-07T12:01:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setHour (data; numero)]

Questa funzione restituisce una nuova data con l’ora specificata nei parametri.

Specificare un numero compreso tra 0 e 23. Se il numero non rientra in questo intervallo, la funzione restituisce un’ora dal giorno precedente (per un numero negativo) o dal giorno successivo (per un numero positivo).

Se è necessario specificare un numero non compreso nell&#39;intervallo, è consigliabile utilizzare addHours, come descritto in precedenza in [addHours (date; number)](#addhours-date-number).

>[!BEGINSHADEBOX]

**Esempi:**

* `setHour(2015-08-07T11:36:39.138Z;6)`

  Restituisce 2015-08-07T06:36:39.138Z

* `setHour(2015-08-07T11:36:39.138;-6)`

  Restituisce 2015-08-06T18:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDay (data; numero/nome del giorno in inglese)]

Questa funzione restituisce una nuova data con il giorno specificato nei parametri.

È possibile utilizzare questa funzione per impostare il giorno della settimana, con domenica 1 e sabato 7. Se specifichi un numero compreso tra 1 e 7, la data risultante rientra nella settimana corrente (da domenica a sabato). Se il numero non è compreso nell&#39;intervallo, la funzione restituisce un giorno della settimana precedente (per un numero negativo) o della settimana successiva (per un numero positivo).

Se è necessario specificare un numero non compreso nell&#39;intervallo, è consigliabile utilizzare addDays, come descritto in precedenza in [addDays (date; number)](#adddays-date-number).

>[!BEGINSHADEBOX]

**Esempi:**

* `setDay(2018-06-27T11:36:39.138Z;Monday)`

  Restituisce 2018-06-25T11:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;1)`

  Restituisce 2018-06-24T11:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;7)`

  Restituisce 2018-06-30T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDate (date; number)]

Questa funzione restituisce una nuova data con il giorno del mese specificato nei parametri.

Specifica un numero compreso tra 1 e 31. Se il numero non rientra in questo intervallo, la funzione restituisce un giorno del mese precedente (per un numero negativo) o del mese successivo (per un numero positivo).

>[!BEGINSHADEBOX]

**Esempi:**

* `setDate(2015-08-07T11:36:39.138Z;5)`

  Restituisce 2015-08-05T11:36:39.138Z

* `setDate(2015-08-07T11:36:39.138Z;32)`

  Restituisce 2015-09-01T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMonth (data; numero/nome del mese in inglese)]

Questa funzione restituisce una nuova data con il mese specificato nei parametri.

Specifica un numero compreso tra 1 e 12. Se il numero non rientra in questo intervallo, la funzione restituisce il mese dell’anno precedente (per un numero negativo) o dell’anno successivo (per un numero positivo).

>[!BEGINSHADEBOX]

**Esempi:**

* `setMonth(2015-08-07T11:36:39.138Z;5)`

  Restituisce 2015-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;17)`

  Restituisce 2016-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;january)`

  Restituisce 2015-01-07T12:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setYear (data; numero)]

Restituisce una nuova data con l’anno specificato nei parametri.

>[!BEGINSHADEBOX]

**Esempio:**

* `setYear(2015-08-07T11:36:39.138Z;2017)`

  Restituisce 2017-08-07T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL formatDate (date; format; [timezone])]

Utilizzare questa funzione quando si dispone di un valore Data, ad esempio `12-10-2021 20:30`, che si desidera formattare come valore Testo, ad esempio `Dec 10, 2021 8:30 PM`.

Questo è utile, ad esempio, quando devi modificare il formato della data di un’app o di un servizio web con quello di un’app o di un servizio web connesso nello stesso scenario.

Per ulteriori informazioni, vedere Date and Text nell&#39;articolo [Tipi di dati elemento](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parametri

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parametro</th> 
   <th>Tipo di dati previsto* </th> 
   <th>Funzionamento</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL date] </td> 
   <td>Data </td> 
   <td> <p>Converte un valore Date in un valore Text. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>Testo </td> 
   <td> <p>Consente di specificare un formato utilizzando i token di formattazione per data e ora. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Token per la formattazione della data e dell'ora</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>Testo </td> 
   <td> <p>(Facoltativo) Consente di specificare il fuso orario utilizzato per la conversione. </p> <p>Per l'elenco dei fusi orari riconosciuti, vedere la colonna "Nome database TZ" in Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">Elenco dei fusi orari del database tz</a>. Solo i valori elencati in questa colonna vengono riconosciuti dalla funzione come fuso orario valido. Qualsiasi altro valore viene ignorato e viene utilizzato il fuso orario Scenarios specificato nel profilo. </p> <p>Se si omette questo parametro, viene applicato il fuso orario Scenarios specificato nelle impostazioni del profilo. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Se viene fornito un tipo diverso, viene applicata la coercizione del tipo. Per ulteriori informazioni, vedere [Tipo di coercizione](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Valore e tipo restituiti

La funzione `formatDate` restituisce una rappresentazione testuale del valore Data specificato in base al formato e al fuso orario specificati. Il tipo di dati è Testo.

>[!BEGINSHADEBOX]

**Esempi:** In questi esempi, il fuso orario Scenario e Web sono entrambi impostati su `Europe/Prague`.

![Esempio di funzione data e ora](assets/date&time-functions-examples-350x61.png)

* `formatDate(1. Date created;MM/DD/YYYY)`

  Restituisce 10/01/2018

* `formatDate(1. Date created; YYYY-MM-DD hh:mm A)`

  Restituisce 2018-10-01 09:32 AM

* `formatDate(1. Date created;DD.MM.YYYY HH:mm;UTC)`

  Restituisce 01.10.2018 07:32

* `formatDate(now;DD.MM.YYYY HH:mm)`

  Restituisce 19.03.2019 15:30

>[!ENDSHADEBOX]

### [!UICONTROL parseDate (testo; formato; [fuso orario])]

Utilizzare questa funzione quando si dispone di un valore Text che rappresenta una data (ad esempio `12-10-2019 20:30` o `Aug 18, 2019 10:00 AM`) e si desidera convertirlo (analizzarlo) in un valore Date (una rappresentazione leggibile da un computer binario). Per ulteriori informazioni, vedere Date and Text nell&#39;articolo [Tipi di dati elemento](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

#### Parametri

La seconda colonna indica il tipo previsto. Se viene fornito un tipo diverso, viene applicata la coercizione del tipo. Per ulteriori informazioni, vedere [Tipo di coercizione](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Parametro</th> 
   <th>Tipo di dati previsto* </th> 
   <th>Funzionamento</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL text] </td> 
   <td>Testo </td> 
   <td> <p>Converte un valore Date in un valore Text. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>Testo </td> 
   <td> <p>Consente di specificare un formato utilizzando i token di formattazione per data e ora. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">Token per la formattazione della data e dell'ora</a>.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>Testo </td> 
   <td> <p>(Facoltativo) Consente di specificare il fuso orario utilizzato per la conversione. </p> <p>Per l'elenco dei fusi orari riconosciuti, vedere la colonna "Nome database TZ" in Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">Elenco dei fusi orari del database tz</a>. Solo i valori elencati in questa colonna vengono riconosciuti dalla funzione come fuso orario valido. Qualsiasi altro valore viene ignorato e viene utilizzato il fuso orario Scenarios specificato nel profilo. </p> <p>Se si omette questo parametro, viene applicato il fuso orario Scenarios specificato nelle impostazioni del profilo.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

Se viene fornito un tipo diverso, viene applicata la coercizione del tipo. Per ulteriori informazioni, vedere [Tipo di coercizione](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

#### Valore e tipo restituiti

Questa funzione converte una stringa di testo in una data, in base al formato e al fuso orario specificati. Il tipo di dati del valore è Data.

>[!BEGINSHADEBOX]

**Esempi:** Negli esempi seguenti, il valore di Data restituito è espresso in base allo standard ISO 8601, ma il tipo di dati del risultato è Date.

* `parseDate(2016-12-28;YYYY-MM-DD)`

  Restituisce 2016-12-28T00:00:00.000Z

* `parseDate(2016-12-28 16:03;YYYY-MM-DD HH:mm)`

  Restituisce 2016-12-28T16:03:00.000Z

* `parseDate(2016-12-28 04:03 pm; YYYY-MM-DD hh:mm a)`

  Restituisce 2016-12-28T16:03:06.000Z

* `parseDate(1482940986;X)`

  Restituisce 2016-12-28T16:03:06.000Z

>[!ENDSHADEBOX]

### [!UICONTROL dataDifferenza (Data1; Data2; Unità)]

Restituisce un numero che rappresenta la differenza tra le due date, espresso nell&#39;unità specificata.

Data2 viene sottratto da Data1.

Utilizzare uno dei valori di tempo seguenti per il parametro `unit`:

* millisecondi
* secondi
* minuti
* ore
* giorni
* settimane
* mesi

Se non viene specificata alcuna unità, la funzione restituisce la differenza in millisecondi.

>[!BEGINSHADEBOX]

**Esempi:**

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z)`

  Restituisce `600,000`

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;hours)`

  Restituisce `4`

* `dateDifference2021-06-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;months)`

  Restituisce `1`

>[!ENDSHADEBOX]

### Altri esempi

#### Come calcolare l’n-esimo giorno della settimana nel mese

Questa sezione è stata adattata per Workfront Fusion dalla pagina Web [!DNL Exceljet] che spiega come ottenere l&#39;ennesimo giorno della settimana in un mese.

Per calcolare una data corrispondente all&#39;ennesimo giorno della settimana del mese, ad esempio primo martedì, terzo venerdì e così via, è possibile utilizzare la formula seguente:

![Calcola nono giorno](assets/date&time-functions-calc-nth-day-350x31.png)

```
{{addDays(setDate(1.date; 1); 1.n * 7 - formatDate(addDays(setDate(1.date; 1); "-" + 1.dow); "E"))}}
```

La formula contiene i seguenti elementi:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>1.n</code> </td> 
   <td> <p> Giorno n:</p> 
    <ul> 
     <li><code>1</code> per il 1° martedì</li> 
     <li><code>2</code> per il 2° martedì</li> 
     <li><code>3</code> per il 3° martedì e così via</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>2.dow</code> </td> 
   <td> <p> giorno della settimana:</p> 
    <ul> 
     <li><code>1</code> per lunedì</li> 
     <li><code>2</code> per martedì</li> 
     <li><code>3</code> per mercoledì</li> 
     <li><code>4</code> per giovedì</li> 
     <li><code>5</code> per venerdì</li> 
     <li><code>6</code> per sabato</li> 
     <li><code>7</code> per domenica</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>1.date</code> </td> 
   <td> <p> La data determina il mese. Per calcolare l'n-esimo giorno della settimana nel mese corrente, utilizzare la variabile <code>now</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

Se si desidera calcolare solo un caso specifico, ad esempio ogni due mercoledì, è possibile sostituire gli elementi `1.n` e `2.dow` nella formula con i numeri corrispondenti. Per il secondo mercoledì del mese corrente, vengono utilizzati i seguenti valori:

* `1.n` = `2`
* `1.dow` = `3`
* `1.date` = `now`

![Valore variabile del nono giorno](assets/nth-day-variable-value-350x33.png)

#### Spiegazione:

* `setDate(now;1)` restituisce il primo del mese corrente
* `formatDate(....;E)` restituisce il giorno della settimana (1, 2, ... 6)

### Come calcolare i giorni tra le date

Una possibilità consiste nell’utilizzare la seguente espressione:

![Calcola giorni tra date](assets/calculate-days-between-dates-350x68.png)

```
{{round((2.value - 1.value) / 1000 / 60 / 60 / 24)}}
```

>[!NOTE]
>
>* I valori di `D1` e `D2` sono valori di tipo Data. Se si tratta di valori di tipo String (ad esempio, 20.10.2018), utilizzare la funzione `parseDate()` per convertirli in valori di tipo Date.
>
>* La funzione `round()` viene utilizzata per i casi in cui una delle date rientra nel periodo di tempo di risparmio dell&#39;ora legale e l&#39;altra no. In questi casi, la differenza di ore è di un’ora in meno o più. È possibile dividerlo per 24 per un risultato non intero. Perdi un&#39;ora di luce. L&#39;arrotondamento la appiattisce in modo da non avere una percentuale

#### Come calcolare l’ultimo giorno/millisecondo del mese

Quando si specifica un intervallo di date, ad esempio in un modulo di ricerca, se l’intervallo si estende sull’intero mese precedente come intervallo chiuso (l’intervallo che include entrambi i punti limite), è necessario calcolare l’ultimo giorno del mese.

2019-09-01 ≤ D ≤ 2019-09-30

La formula seguente mostra un modo per calcolare l’ultimo giorno del mese precedente:

![Ultimo giorno del mese precedente](assets/last-day-prev-month.png)

```
{{addDays(setDate(now; 1); -1)}}
```

In alcuni casi, è necessario calcolare non solo l’ultimo giorno del mese, ma letteralmente il suo ultimo millisecondo:

2019-09-01T00:00:00.000Z ≤ D ≤ 2019-09-30T23:59:59.999Z

Questa formula mostra un modo per calcolare l’ultimo millisecondo del mese precedente:

![Ultimo millisecondo del mese precedente](assets/last-millisecond-prev-month-350x45.png)

```
{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD"; "UTC") - 1; "x")}}
```

Se è necessario che il risultato utilizzi l’impostazione del fuso orario, ometti l’argomento UTC:

![Ometti UTC](assets/omit-utc-argument-350x45.png)

`{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD") - 1; "x")}}`

Tuttavia, è preferibile utilizzare l’intervallo semi-aperto (l’intervallo che esclude uno dei suoi punti limite), specificando il primo giorno del mese successivo e sostituendo l’operatore &quot;minore o uguale a&quot; con &quot;minore di&quot; come segue:

`2019-09-01 ≤ D < 2019-10-01`

`2019-09-01T00:00:00.000Z ≤ D < 2019-10-01T00:00:00.000Z`
