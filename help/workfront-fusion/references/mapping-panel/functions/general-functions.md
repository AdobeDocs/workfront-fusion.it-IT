---
title: Funzioni generali
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni generali.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 7%

---

# Funzioni generali

## Variabili

Puoi utilizzare queste variabili generali per identificare i dettagli di un’esecuzione:

* `executionID`: ID dell&#39;esecuzione dello scenario
* `triggerTimestamp`: ora in cui è stata attivata l&#39;esecuzione
* `scenarioID`: ID dello scenario attualmente aperto
* `operationsConsumed`: numero di operazioni utilizzate in quel punto dello scenario.

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

