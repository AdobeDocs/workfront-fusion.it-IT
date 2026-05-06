---
title: Funzioni matematiche
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni matematiche.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 6%

---

# Funzioni matematiche

## [!UICONTROL media ([matrice di valori]) media(valore1; [valore2], ...)]

Restituisce il valore medio dei valori numerici in una matrice specifica o il valore medio dei valori numerici immessi singolarmente.

## [!UICONTROL ceil (numero)]

Restituisce il numero intero più piccolo maggiore o uguale a un numero specificato.

>[!BEGINSHADEBOX]

**Esempi:**

* `ceil(` `1.2` `)`

  Restituisce 2

* `ceil(` `4` `)`

  Restituisce 4

>[!ENDSHADEBOX]

## [!UICONTROL piano (numero)]

Restituisce il numero intero più grande minore o uguale a un numero specificato.

>[!BEGINSHADEBOX]

**Esempi:**

* `floor(` `1.2` `)`

  Restituisce 1

* `floor(` `1.9` `)`

  Restituisce 1

* `floor(` `4` `)`

  Restituisce 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([matrice di valori]), max(valore1;valore2; ...)]

Restituisce il numero più grande in una matrice specificata o il numero più grande tra i numeri immessi singolarmente.

## [!UICONTROL min ([matrice di valori]), min(valore1; valore2; ...)]

Restituisce il numero più piccolo di una matrice specificata o il numero più piccolo tra i numeri immessi singolarmente.

## [!UICONTROL round (numero)]

Arrotonda un valore numerico al numero intero più vicino.

>[!BEGINSHADEBOX]

**Esempi:**

* `round(` `1.2` `)`

  Restituisce 1

* `round(` `1.5` `)`

  Restituisce 2

* `round(` `1.7` `)`

  Restituisce 2

* `round(` `2` `)`

  Restituisce 2

>[!ENDSHADEBOX]

## [!UICONTROL somma ([matrice di valori]), somma(valore1; valore2; ...)]

Restituisce la somma dei valori in una matrice specificata o la somma dei numeri immessi singolarmente.

## [!UICONTROL parseNumber (numero; separatore decimale)]

Analizza una stringa con un numero e restituisce il numero. Ad esempio, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (numero; separatore decimale; [separatore decimale]; [migliaiaSeparatore])]

Restituisce un numero nel formato richiesto. Per impostazione predefinita, il punto decimale è una virgola (,) e il separatore delle migliaia è un punto (.).

>[!BEGINSHADEBOX]

**Esempio:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Restituisce 123.456.789.000

>[!ENDSHADEBOX]

### [!UICONTROL abs(number)]

[!BADGE Nuovo!]{type=Informative}

Restituisce il valore assoluto di un numero.

>[!BEGINSHADEBOX]

**Esempio:**

* `abs(-3.14)`

  Restituisce 3,14
* `abs(3.14)`

  Restituisce 3,14


### [!UICONTROL div(number1; number2; ...)]

[!BADGE Nuovo!]{type=Informative}

Divide tutti i numeri nell&#39;ordine specificato.

>[!BEGINSHADEBOX]

**Esempio:**

* `div(10; 2)`

  Restituisce 5
* `div(100; 5; 4)`

  Restituisce 5


### [!UICONTROL ln(number)]

[!BADGE Nuovo!]{type=Informative}

Restituisce il logaritmo naturale del numero.


>[!BEGINSHADEBOX]

**Esempio:**

* `ln(1)`

  Restituisce 0
* `ln(2.718281828)`

  Restituisce 1


### [!UICONTROL log(number1; number2)]

[!BADGE Nuovo!]{type=Informative}

Restituisce il logaritmo di `number2` alla base `number1`.

>[!BEGINSHADEBOX]

**Esempio:**

* `log(10; 100)`

  Restituisce 2
* `log(2; 8)`

  Restituisce 3


### [!UICONTROL numero(stringa)]

[!BADGE Nuovo!]{type=Informative}

Converte una stringa in un numero.

>[!BEGINSHADEBOX]

**Esempio:**

* `number("3.14")`

  Restituisce 3,14
* `number("42")`

  Restituisce 42


### [!UICONTROL potenza(numero; potenza)]

[!BADGE Nuovo!]{type=Informative}

Restituisce un numero elevato alla potenza specificata.

>[!BEGINSHADEBOX]

**Esempio:**

* `power(2; 3)`

  Restituisce 8
* `power(4; 0.5)`

  Restituisce 2


### [!UICONTROL prod(number1; number2; ...)]

[!BADGE Nuovo!]{type=Informative}

Moltiplica tutti i numeri forniti insieme.

>[!BEGINSHADEBOX]

**Esempio:**

* `prod(2; 3; 4)`

  Restituisce 24
* `prod(5; 5)`

  Restituisce 25


### [!UICONTROL sortAscNum(number1; number2; ...)]

[!BADGE Nuovo!]{type=Informative}

Restituisce i numeri forniti ordinati in ordine crescente.

>[!BEGINSHADEBOX]

**Esempio:**

* `sortAscNum(3; 1; 2)`

  Restituisce \[1, 2, 3]
* `sortAscNum(5; 3; 4)`

  Restituisce \[3, 4, 5]


### [!UICONTROL sortDescNum(number1; number2; ...)]

[!BADGE Nuovo!]{type=Informative}

Restituisce i numeri forniti ordinati in ordine decrescente.

>[!BEGINSHADEBOX]

**Esempio:**

* `sortDescNum(3; 1; 2)`

  Restituisce \[3, 2, 1]
* `sortDescNum(5; 3; 4)`

  Restituisce \[5, 4, 3]


### [!UICONTROL sqrt(number)]

[!BADGE Nuovo!]{type=Informative}

Restituisce la radice quadrata di un numero.

>[!BEGINSHADEBOX]

**Esempio:**

* `sqrt(9)`

  Restituisce 3
* `sqrt(4)`

  Restituisce 2


### [!UICONTROL sub(number1; number2; ...)]

[!BADGE Nuovo!]{type=Informative}

Sottrae tutti i numeri nell&#39;ordine specificato.

>[!BEGINSHADEBOX]

**Esempio:**

* `sub(10; 3; 2)`

  Restituisce 5
* `sub(20; 5)`

  Restituisce 15
