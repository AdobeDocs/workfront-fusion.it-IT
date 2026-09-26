---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Attività sulla versione di Workfront Fusion: settimana del martedì 17 maggio 2021'
description: Questa pagina descrive tutti i miglioramenti apportati a Adobe Workfront Fusion la settimana del martedì 17 maggio 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 2ea57c69-8db7-4500-9157-e2c2d8c74938
TQID: 'https://experienceleague.adobe.com/m2429hptKDPLLMtHLk-lqJ9ofXaRo8uzmaF7iR7bflE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: d968a1bc-9a90-4926-a531-bcf272c32aad
    internal-label: Administration
subfeature_v2:
  - id: a29813d3-f0cc-4b60-9396-13b558370803
    internal-label: Product announcements
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 30%
---
# Attività sulla versione di Workfront Fusion: settimana del martedì 17 maggio 2021

Questa pagina descrive tutti i miglioramenti apportati a Adobe Workfront Fusion la settimana del martedì 17 maggio 2021.

Per un elenco di tutte le modifiche recenti, consulta [Attività sulla versione di Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Per un elenco delle correzioni di bug recenti in Workfront Fusion, consulta la pagina [Aggiornamenti di manutenzione di Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=it) e controlla la presenza di eventuali aggiornamenti etichettati Aggiornamento di manutenzione di Workfront Fusion.

## Copiare moduli in scenari Workfront Fusion

Per semplificare l’utilizzo degli scenari di Workfront Fusion, è stato possibile copiare e incollare moduli. Ora è possibile copiare un modulo o un gruppo di moduli e incollarli nello stesso scenario o in uno diverso. La copia dei moduli mantiene i valori dei campi in quel modulo.


## Selezionare più moduli in uno scenario Workfront Fusion

Ora, quando modifichi uno scenario, puoi selezionare più moduli alla volta. È quindi possibile eseguire azioni in blocco sui moduli selezionati.

* Copia
* Sposta
* Elimina

Copiando e spostando i moduli vengono mantenuti i valori dei moduli e le linee che li collegano.


## I moduli ora conservano le informazioni non salvate

Per semplificare la creazione degli scenari, abbiamo consentito ai moduli di mantenere i valori dei campi quando non sono attivi. Ora, quando si fa clic lontano da un modulo senza salvarlo e quindi si torna ad esso, i campi mostrano i valori precedentemente immessi. Quando il modulo viene chiuso, viene visualizzato un indicatore della presenza di campi non salvati.

## Il connettore Azure AD ora gestisce separatamente i record nuovi e aggiornati.

I nuovi record e gli aggiornamenti ai record esistenti vengono ora gestiti da moduli separati.

* Per verificare la presenza di nuovi record, puoi utilizzare il modulo di trigger Record di controllo. Questo modulo non controlla più i record aggiornati.
* Per ottenere record aggiornati, puoi utilizzare il nuovo modulo Delta utenti/gruppi di ricerca. Questo modulo restituisce record nuovi, aggiornati ed eliminati.
