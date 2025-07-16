---
title: Operazioni
description: Un'operazione in Adobe Workfront Fusion è un'operazione eseguita da un modulo. Ai fini del tracciamento, qualsiasi azione eseguita correttamente da un modulo è un’operazione.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: 3470f7a9658ac4e6214c27f94f5b41821f2f8665
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Operazioni

Un&#39;operazione in Adobe Workfront Fusion è un&#39;operazione eseguita da un modulo. Ai fini del tracciamento, qualsiasi azione eseguita correttamente da un modulo è un’operazione.

## Considerazioni durante il conteggio del numero di operazioni

* In generale, qualsiasi esecuzione di un’azione eseguita con successo viene considerata un’operazione.
* Il primo modulo di uno scenario viene eseguito una sola volta e viene sempre conteggiato come un’unica operazione, anche se non restituisce un bundle.
* Il numero di volte in cui gli altri moduli vengono eseguiti dipende dal numero di bundle che devono elaborare.  Un’esecuzione di un modulo per un bundle è un’unica operazione. Un’eccezione è il modulo aggregatore, conteggiato come un’unica operazione per set di bundle in fase di elaborazione.
* Le operazioni vengono conteggiate nella fase [!UICONTROL Finalizzazione] dell&#39;esecuzione di uno scenario.
* **non** sono conteggiati come operazioni:
   * Qualsiasi passaggio di filtro.
   * Qualsiasi azione che si verifichi un errore o si arresti.
   * Qualsiasi route non eseguita perché non sono state soddisfatte le regole della route, ad esempio route di fallback o disabilitate.
   * Qualsiasi azione non eseguita, perché un filtro non ha consentito il passaggio dei dati o perché lo scenario è stato interrotto a causa di un errore.

## Limiti operativi

La tua organizzazione potrebbe avere un limite mensile di operazioni. Si basa sul piano [!DNL Workfront] acquistato dalla tua organizzazione. Il piano [!UICONTROL Ultimate] [!DNL Workfront] offre operazioni illimitate.

Se la tua organizzazione dispone di un limite mensile, riceverai una notifica quando l’organizzazione si avvicina al limite. Se l&#39;organizzazione supera il limite, [!DNL Workfront] contatterà l&#39;organizzazione per assicurarsi che il piano soddisfi le tue esigenze.

Workfront Fusion invia una notifica quando l’organizzazione raggiunge le seguenti percentuali del limite mensile:

* 50%
* 75%
* 90%
* 100%

## Visualizza il numero di operazioni eseguite negli ultimi 30 giorni

È possibile visualizzare un grafico che mostra il numero di operazioni eseguite. Questi grafici sono disponibili nelle seguenti posizioni:

* **Dashboard organizzazione**: operazioni utilizzate dall&#39;intera organizzazione
* **Dashboard team**: operazioni utilizzate da scenari di proprietà di questo team
* **Pagina dettagli scenario**: operazioni utilizzate da questo scenario
