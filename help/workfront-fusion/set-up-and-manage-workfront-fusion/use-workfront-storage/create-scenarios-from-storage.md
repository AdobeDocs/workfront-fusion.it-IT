---
title: Creare scenari dall’archiviazione
description: Storage si integra con il generatore di scenari di Fusion, in modo da poter creare scenari preconfigurati direttamente dalla pagina Storage per scaricare o caricare i file.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# Creare scenari dall’archiviazione

Per una panoramica dell&#39;archiviazione, vedere [Panoramica archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

Storage si integra con lo scenario builder di Fusion. Dalla pagina Archiviazione, gli utenti possono creare uno scenario in cui verrà scaricato il file selezionato.

## Scarica in scenario

1. In Workfront Fusion, fai clic su **Archiviazione** nell&#39;area di navigazione a sinistra.
1. Passare al repository contenente il file che si desidera scaricare in uno scenario.
1. Selezionare un file, quindi fare clic su **&quot;Scarica nello scenario&quot;** dalla barra delle azioni.

Fusion crea quindi un nuovo scenario denominato **&quot;Download di {fileName}&quot;**. Questo scenario si apre in una scheda del browser separata.

Lo scenario è preconfigurato con:

* La connessione attiva.
* L’archivio, la cartella e il file preselezionati.
* Modulo per generare un URL di download preceduto da un segno.
* Un modulo HTTP per recuperare il file da tale URL.
* Intervallo di pianificazione predefinito di 15 minuti.

## Carica file nello scenario

1. In Workfront Fusion, fai clic su **Archiviazione** nell&#39;area di navigazione a sinistra.
1. Passare al repository e alla cartella che contiene il file che si desidera scaricare in uno scenario.
1. Durante la navigazione in una cartella, fare clic sul menu a discesa **&quot;Carica file&quot;**.
1. Selezionare **&quot;Carica file nello scenario&quot;**.

Fusion crea quindi un nuovo scenario denominato **&quot;Carica in {folderName}&quot;**. Questo scenario si apre in una nuova scheda del browser. Per fornire il file da caricare, devi aggiungere dei moduli, ad esempio Workfront > Scarica modulo documento.

Lo scenario è preconfigurato con:

* La connessione attiva.
* L’archivio e la cartella preselezionati.
* Modulo per generare un URL di caricamento preceduto da un segnaposto con un nome file.
* Intervallo di pianificazione predefinito di 15 minuti.

