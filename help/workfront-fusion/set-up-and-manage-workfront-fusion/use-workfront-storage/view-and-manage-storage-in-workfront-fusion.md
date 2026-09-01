---
title: Visualizzazione e gestione dello storage in Workfront Fusion
description: L'area di archiviazione elenca i repository disponibili e consente di esplorare cartelle e file.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 1%

---

# Visualizzazione e gestione dello storage in Workfront Fusion

L’area di archiviazione in Workfront Fusion consente di visualizzare e interagire con gli archivi nell’archiviazione cloud Adobe.

Per una panoramica dell&#39;archiviazione, vedere [Panoramica archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

>[!TIP]
>
>Per poter visualizzare gli archivi, è necessario inizializzare l&#39;archiviazione. Per istruzioni, vedere [Inizializzare l&#39;archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## Visualizzare archivi, cartelle e file

1. In Workfront Fusion, fai clic su **Archiviazione** nell&#39;area di navigazione a sinistra.
Viene visualizzato un elenco di archivi.

   Se è disponibile un solo archivio, questo si apre direttamente.

1. Fai clic su **Apri** in qualsiasi repository per visualizzarne il contenuto.

   L&#39;apertura di un repository mostra le cartelle all&#39;interno del repository.
1. Fare clic su una cartella per aprirla e visualizzarne i file.
1. Per spostarti nuovamente verso l’alto nella struttura delle cartelle, fai clic sulle breadcrumb.


>[!NOTE]
>
>Una cartella vuota visualizza il messaggio: *&quot;Questa cartella è vuota&quot;*

## Gestione di più connessioni di storage

Un team può disporre di più connessioni di archiviazione Adobe.

1. In Workfront Fusion, fai clic su **Archiviazione** nell&#39;area di navigazione a sinistra.
Quando sono presenti più connessioni, nella parte superiore della pagina Archiviazione vengono visualizzate delle schede con l&#39;etichetta del nome di ciascuna connessione.
1. Per passare agli archivi di una connessione diversa, fare clic sulla scheda della connessione.

Se una connessione non è più valida, ad esempio se il relativo token è scaduto e non può essere aggiornato, viene automaticamente filtrata e non viene visualizzata come scheda. L&#39;aggiornamento del token pianificato di Fusion mantiene le connessioni valide automaticamente.

## Informazioni file

Ogni file della tabella mostra:

| Colonna | Descrizione |
| -------- | ------------- |
| **Nome** | Nome del file con l&#39;icona del documento. |
| **Tipo** | Badge dell’estensione file, ad esempio PNG, PDF o JPG. |
| **Dimensione** | Dimensione file. Mostra *&quot;Elaborazione in corso...&quot;* se il file è stato caricato di recente e il backend lo sta ancora elaborando. |
| **Creato** | Data di creazione. |

Nei file viene inoltre visualizzato un **badge versione** (ad esempio `v2`, `v3`) quando esistono più versioni.

## Controlli tabella

* **Ricerca/filtro**: filtra i file per nome utilizzando la barra di ricerca globale.
* **Ordinamento**: fare clic sulle intestazioni di colonna per ordinare.
* **Paginazione**: scegliere 10, 25, 50 o 100 elementi per pagina. Il valore predefinito è 25.
