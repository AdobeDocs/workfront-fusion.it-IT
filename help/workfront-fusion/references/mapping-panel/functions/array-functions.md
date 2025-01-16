---
title: Funzioni array
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni di array.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Funzioni array

## [!UICONTROL join (array; separator)]

Concatena tutti gli elementi di un array in una stringa utilizzando il separatore specificato tra ogni elemento.

## [!UICONTROL length (array)]

Restituisce il numero di elementi in una matrice.

## [!UICONTROL keys (object)]

Restituisce una matrice delle proprietà di un determinato oggetto o matrice.

## [!UICONTROL slice (array; start; [end])]

Restituisce una nuova matrice contenente solo gli elementi selezionati.

## [!UICONTROL merge (array1; array2; ...)]

Unisce uno o più array in un unico array.

## [!UICONTROL contains (array; value)]

Verifica se un array contiene il valore.

## [!UICONTROL remove (array; value1; value2; ...)]

Rimuove i valori specificati nei parametri di un array. Questa funzione è efficace solo su array primitivi di testo o numeri.

## [!UICONTROL add (array; value1; value2; ...)]

Aggiunge i valori specificati nei parametri a un array e restituisce tale array.

## [!UICONTROL map (complex array; key;[key for filtering];[possible values for filtering])]

Restituisce una matrice primitiva contenente i valori di una matrice complessa. Questa funzione consente di filtrare i valori. Utilizza nomi di variabili non elaborati per le chiavi.

>[!BEGINSHADEBOX]

**Esempi:**

* `map(Emails[];email)`

  Restituisce un array primitivo con le e-mail

* `map(Emails[];email;label;work;home)`

  Restituisce un array primitivo con e-mail aventi un’etichetta uguale a lavoro o casa

>[!ENDSHADEBOX]

Per ulteriori informazioni, vedere [Mappare un array o un elemento di array](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).

## mischiare

## [!UICONTROL sort (array; [order]; [key])]

Ordina i valori di un array. I valori validi del parametro `order` sono:

* `asc`

  (impostazione predefinita) - Ordine crescente: 1, 2, 3, ... per il tipo Numero. A, B, C, a, b, c, ... per il tipo Testo

* `desc`

  ordine decrescente: ..., 3, 2, 1 per il tipo Numero. ..., c, b, a, C, B, A per il tipo Testo.

* `asc ci`

  ordine crescente senza distinzione tra maiuscole e minuscole: A, a, B, b, C, c, ... per il tipo Testo.

* `desc ci`

  ordine decrescente senza distinzione tra maiuscole e minuscole: ..., C, c, B, b, A, a per il tipo Testo.

Utilizzare il parametro `key` per accedere alle proprietà di oggetti complessi.

Utilizza nomi di variabili non elaborati per le chiavi.

Per accedere alle proprietà nidificate, utilizza la notazione del punto.

Il primo elemento di un array è l&#39;indice 1.

>[!BEGINSHADEBOX]

**Esempi:**

* `sort(Contacts[];name)`

  Ordina un array di contatti in base alla proprietà &quot;name&quot; in ordine crescente predefinito

* `sort(Contacts[];desc;name)`

  Ordina un array di contatti in base alla proprietà &quot;name&quot; in ordine decrescente

* `sort(Contacts[];asc ci;name)`

  Ordina un array di contatti in base alla proprietà &quot;name&quot;, in ordine crescente senza distinzione tra maiuscole e minuscole

* `sort(Emails[];sender.name)`

  Ordina un array di e-mail in base alla proprietà &quot;sender.name&quot;

>[!ENDSHADEBOX]

## [!UICONTROL reverse (array)]

Il primo elemento dell’array diventa l’ultimo elemento, il secondo diventa il successivo-ultimo e così via.

## [!UICONTROL flatten (array)]

Crea un nuovo array con tutti gli elementi sub-array concatenati in esso, in modo ricorsivo, fino alla profondità specificata.

## [!UICONTROL distinct (array; [key])]

Rimuove i duplicati all&#39;interno di un array. Utilizzare l&#39;argomento &quot;[!UICONTROL key]&quot; per accedere alle proprietà di oggetti complessi. Per accedere alle proprietà nidificate, utilizza la notazione del punto. Il primo elemento di un array è l&#39;indice 1.

>[!BEGINSHADEBOX]

**Esempio:** `distinct(Contacts[];name)`

Rimuove i duplicati in un array di contatti confrontando la proprietà &quot;name&quot;

>[!ENDSHADEBOX]

## toCollection

## toArray

Questa funzione converte una raccolta in un array di coppie chiave-valore.

>[!BEGINSHADEBOX]

**Esempi:**

Data la raccolta

`{ key1: "value1", key2: "value2:}`

La funzione

`toArray({ key1: "value1", key2: "value2:})`

Restituisce la matrice di coppie chiave-valore

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

Restituisce la differenza tra due array.

Immettere uno dei seguenti valori per il parametro `mode`.

* `classic`: restituisce un nuovo array che contiene tutti gli elementi di `array1` che non esistono in `array2`.

* `symmetric`: restituisce una matrice di elementi non comuni a entrambe le matrici.

  In altre parole, la funzione restituisce un array che contiene tutti gli elementi di `array1` che non esistono in `array2` e tutti gli elementi di `array2` che non esistono in `array1`.

>[!BEGINSHADEBOX]

**Esempi:**

Considerati i seguenti array:

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  Restituisce `[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  Restituisce `[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  Restituisce `[1,2,6,7]`

>[!ENDSHADEBOX]

## deDuplica

## Parole chiave

## emptyarray
