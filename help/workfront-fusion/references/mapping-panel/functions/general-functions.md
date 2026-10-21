---
title: Funzioni generali
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni generali.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: 'https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 8ea986eb6573bb49accfad312bb0796faa2642ab
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 5%
---
# Funzioni generali

## Variabili

Puoi utilizzare queste variabili generali per identificare i dettagli di un’esecuzione:

* `executionId`: ID dell&#39;esecuzione dello scenario
* `scenarioId`: ID dello scenario attualmente aperto
* `scenarioName`: nome dello scenario attualmente in esecuzione
* `scenarioUrl`: collegamento allo scenario corrente nell&#39;interfaccia utente di Fusion
* `executionUrl`: collegamento all&#39;esecuzione dello scenario corrente nell&#39;interfaccia utente di Fusion
* `scenarioApiUrl`: URL Fusion API per lo scenario corrente
* `executionApiUrl`: URL Fusion API per i dettagli dell&#39;esecuzione corrente
* `teamId`: ID del team Fusion proprietario dello scenario corrente
* `organizationId`: ID dell&#39;organizzazione Fusion associata all&#39;esecuzione corrente. Questo non è un ID organizzazione Adobe IMS.
* `triggerTimestamp`: ora in cui è stata attivata l&#39;esecuzione
* `operationsConsumed`: numero di operazioni utilizzate in quel punto dello scenario.

I nomi delle variabili fanno distinzione tra maiuscole e minuscole. Ad esempio, utilizzare `scenarioUrl`, non `scenarioURL`.

Puoi utilizzare queste variabili in campi mappati senza creare URL o ID di team e organizzazioni hardcoding. Ad esempio, puoi includere quanto segue in un campo di testo mappato in una notifica:

<pre><code>
Scenario: &#123;&#123;scenarioName&#125;&#125;
Open scenario: &#123;&#123;scenarioUrl&#125;&#125;
Open execution: &#123;&#123;executionUrl&#125;&#125;
Team: &#123;&#123;teamId&#125;&#125;
Organization: &#123;&#123;organizationId&#125;&#125;
</code></pre>

Quando utilizzi queste variabili, tieni presente quanto segue:

* I valori vengono risolti durante l’esecuzione dello scenario. Il pannello di mappatura elenca le variabili, ma non ne visualizza l’anteprima i valori.
* `scenarioUrl` e `executionUrl` si collegano allo scenario e all&#39;esecuzione nell&#39;interfaccia utente di Fusion. `scenarioApiUrl` e `executionApiUrl` sono URL endpoint API, non collegamenti a pagine Fusion.
* Le variabili URL API restituiscono solo testo. Non effettuano richieste né forniscono credenziali di autenticazione. L’autenticazione e le autorizzazioni API normali sono ancora valide.
* I collegamenti non concedono accesso aggiuntivo. Si applicano le normali autorizzazioni di Fusion.
* `executionUrl` non viene generato per le esecuzioni che non vengono salvate nella cronologia di esecuzione, ad esempio le esecuzioni sandbox o le esecuzioni con sincronizzazione cronologia disattivata. Un collegamento generato non garantisce che i dettagli di esecuzione siano disponibili al momento dell’utilizzo.
* Impossibile generare `scenarioUrl` per un modello o uno scenario non salvato.
* Se non è possibile generare un URL, la variabile non ha alcun valore.

## [!UICONTROL get (oggetto o array; percorso)]

Restituisce il percorso del valore di un oggetto o di una matrice. Per accedere agli oggetti nidificati, utilizzare la notazione del punto. Il primo elemento di un array è l&#39;indice 1.

>[!BEGINSHADEBOX]

**Esempi:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (espressione; valore1; valore2)]

Restituisce `value1` se l&#39;espressione viene valutata come true, altrimenti restituisce `value2`.

Per creare un&#39;istruzione if che restituisca un valore solo se due o più espressioni vengono valutate come true, utilizzare la parola chiave `and`.

Per combinare `if` istruzioni, utilizzare gli operatori `and` e `or`.

![e operatore](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Esempi:**

* `if( 1 = 1 ; A ; B )`

  Restituisce Un

* `if( 1 = 2 ; A ; B )`

  Restituisce B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Restituisce B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (valore1; valore2)]

Restituisce `value1` se questo valore non è vuoto, altrimenti restituisce `value2`.

>[!BEGINSHADEBOX]

**Esempi:**

* `ifempty(` `A` `;` `B` )

  Restituisce Un

* `ifempty(` `unknown` `;` `B` )

  Restituisce B

* `ifempty(` `""` `;` `B` )

  Restituisce B

>[!ENDSHADEBOX]

## [!UICONTROL opzione (espressione; valore1; risultato1; [valore2; risultato2; ...]; [altro])]

Valuta un valore (denominato espressione) rispetto a un elenco di valori; restituisce il risultato corrispondente al primo valore corrispondente. Per includere un valore `else`, aggiungerlo dopo l&#39;espressione o il valore finale.

>[!BEGINSHADEBOX]

**Esempi:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Restituisce 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Restituisce 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Restituisce 4

  In questa funzione, 4 è il valore da restituire se non viene applicata alcuna espressione (il valore `else`).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Omette le chiavi specificate dell&#39;oggetto e restituisce il resto.

>[!BEGINSHADEBOX]

**Esempio:**

`omit(` Utente `;` password `)`

Restituisce una raccolta delle informazioni dell&#39;utente, esclusa la password.

>[!ENDSHADEBOX]

## [!UICONTROL scegli(oggetto; chiave1; [chiave2; ...])]

Seleziona dall’oggetto solo le chiavi specificate.

>[!BEGINSHADEBOX]

**Esempio:**

`pick(` Utente `;` password `;` e-mail `)`

Restituisce una raccolta contenente solo la password e l&#39;indirizzo e-mail dell&#39;utente.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

Unisce due raccolte combinando le rispettive coppie chiave-valore. Se entrambi gli insiemi contengono la stessa chiave, il valore della seconda raccolta sovrascrive quello della prima raccolta.

### [!UICONTROL isBlank(value)]

Restituisce `true` se il valore è `null` o una stringa vuota, altrimenti restituisce `false`. A differenza di `ifEmpty`, questa funzione non considera il numero `0` o le stringhe solo spazi vuoti come vuoti.

>[!BEGINSHADEBOX]

**Esempio:**

* `isBlank("")     `

  Restituisce true
* `isBlank(null)   `

  Restituisce true
* `isBlank("Hello")`

  Restituisce false
* `isBlank(0)      `

  Restituisce false
* `isBlank(" ")    `

  Restituisce false

>[!ENDSHADEBOX]


### [!UICONTROL in(valore; valore1; valore2; ...)]

Restituisce `true` se il valore è uguale a uno dei valori specificati (uguaglianza rigorosa, nessuna coercizione del tipo).

>[!BEGINSHADEBOX]

**Esempio:**

* `in("B"; "A"; "B"; "C")`

  Restituisce true
* `in("D"; "A"; "B"; "C")`

  Restituisce false
* `in(2; 1; 2; 3)        `

  Restituisce true
* `in("2"; 1; 2; 3)      `

  Restituisce false

>[!ENDSHADEBOX]

### [!UICONTROL ifin(value; value1; value2; ...; trueExpression; falseExpression)]

Restituisce `trueExpression` se il valore corrisponde a uno qualsiasi dei valori di corrispondenza forniti, altrimenti restituisce `falseExpression`. Richiede almeno 3 argomenti (valore, un valore di corrispondenza e trueExpression + falseExpression).

>[!BEGINSHADEBOX]

**Esempio:**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  Restituisce sì
* `ifin("D"; "A"; "B"; "yes"; "no")`

  Restituisce no
* `ifin("X"; "X"; "found"; "not found")`

  Restituzioni trovate

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber; value1; value2; ...)]

Restituisce il valore nella posizione specificata dal numero di indice (basato su 1). Restituisce `null` se l&#39;indice non è compreso nei limiti o è 0.

>[!BEGINSHADEBOX]

**Esempio:**

* `case(1; "Sun"; "Mon"; "Tue")`

  Restituisce il sole
* `case(2; "Sun"; "Mon"; "Tue")`

  Restituisce il lunedì
* `case(3; "Sun"; "Mon"; "Tue")`

  Restituisce Mar
* `case(5; "a"; "b")           `

  Restituisce null

>[!NOTE]
>
>È consigliabile utilizzare questa opzione per ottenere il nome del giorno da una data:
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

