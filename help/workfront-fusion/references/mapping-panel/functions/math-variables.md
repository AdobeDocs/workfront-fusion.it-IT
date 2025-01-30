---
title: Variabili matematiche
description: Le seguenti variabili matematiche sono disponibili nel pannello  [!DNL Adobe Workfront Fusion mapping] .
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# Variabili matematiche

## pi greco

Rappresenta il simbolo matematico $\pi$.

## [!UICONTROL random]

Restituisce un numero a virgola mobile pseudo-casuale compreso nell&#39;intervallo [`0`,`1`] (incluso `0`, ma non `1`).

Utilizzare la formula seguente per generare un numero intero pseudo-casuale nell&#39;intervallo [`min`,`max`] (inclusi `min` e `max`):

![Casuale](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
