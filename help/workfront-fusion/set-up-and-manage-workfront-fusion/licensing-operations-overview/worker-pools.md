---
title: Pool di lavoro
description: Un pool di lavoratori è una quantità di risorse di elaborazione Workfront Fusion dedicate a una o più organizzazioni specifiche. Tutte le operazioni e le elaborazioni di Fusion vengono eseguite nel contesto del pool di lavoratori assegnato a un'organizzazione.
author: Becky
feature: Workfront Fusion
source-git-commit: bb94083eb9f58dc3ae9f94a59288da43317b567b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Pool di lavoro

Un pool di lavoratori è una quantità di risorse di elaborazione Workfront Fusion dedicate a un&#39;organizzazione specifica. Tutte le operazioni e le elaborazioni di Fusion vengono eseguite nel contesto del pool di lavoratori assegnato a un&#39;organizzazione.

I pool di lavoro consentono un&#39;esecuzione più efficiente degli scenari ed eliminano le possibilità di competere con altre organizzazioni per la capacità di elaborazione Fusion.

## Panoramica del pool di lavoro

Un pool di lavoro è un modo per elaborare le esecuzioni degli scenari in parallelo. Ogni pool di lavoratori è associato a:

* Un certo numero di lavoratori.
* Una coda di esecuzione.

Quando viene eseguito uno scenario, questo passa nella coda di esecuzione del pool di lavoro. I processi di lavoro nel pool estraggono continuamente le attività dal pool di esecuzione ed elaborarle in parallelo.

Se la profondità della coda di esecuzione aumenta e tutti i processi di lavoro esistenti vengono utilizzati, Workfront Fusion ridimensiona automaticamente il pool aggiungendo altri processi di lavoro. Questa scalabilità è dinamica e guidata dagli eventi, il che significa che la capacità esatta o si contrae in base al carico in tempo reale senza l’azione dell’azienda.

Il team di Workfront Fusion monitora costantemente l&#39;utilizzo e il comportamento di scalabilità dei pool e può esaminare soglie o modelli per garantire prestazioni coerenti in base alla crescita dell&#39;utilizzo.
