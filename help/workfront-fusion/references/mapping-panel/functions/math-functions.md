---
title: Funzioni matematica
description: Nel pannello di mappatura di Adobe Workfront Fusion sono disponibili le seguenti funzioni matematiche.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Funzioni matematica

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Restituisce il valore medio dei valori numerici in una matrice specifica o il valore medio dei valori numerici immessi singolarmente.

## [!UICONTROL ceil (number)]

Restituisce il numero intero più piccolo maggiore o uguale a un numero specificato.

>[!BEGINSHADEBOX]

**Esempi:**

* `ceil(` `1.2` `)`

  Restituisce 2

* `ceil(` `4` `)`

  Restituisce 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

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

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Restituisce il numero più grande in una matrice specificata o il numero più grande tra i numeri immessi singolarmente.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

Restituisce il numero più piccolo di una matrice specificata o il numero più piccolo tra i numeri immessi singolarmente.

## [!UICONTROL round (number)]

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

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Restituisce la somma dei valori in una matrice specificata o la somma dei numeri immessi singolarmente.

## [!UICONTROL parseNumber (number; decimal separator)]

Analizza una stringa con un numero e restituisce il numero. Ad esempio, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Restituisce un numero nel formato richiesto. Per impostazione predefinita, il punto decimale è una virgola (,) e il separatore delle migliaia è un punto (.).

>[!BEGINSHADEBOX]

**Esempio:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Restituisce 123.456.789.000

>[!ENDSHADEBOX]
