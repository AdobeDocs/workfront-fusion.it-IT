---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Attività sulla versione di Workfront Fusion: settimana del 7 novembre 2022'
description: Questa pagina descrive tutti i miglioramenti apportati a Adobe Workfront Fusion la settimana del martedì 7 novembre 2022.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
TQID: 'https://experienceleague.adobe.com/iigr0fKWxXA-DvvPZVjZvIQ3s-dW6XUBWgMYaxoGZRs'
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 32%
---
# Attività sulla versione di Workfront Fusion: settimana del 7 novembre 2022

**Ottimizzazione coda webhook**

La coda del webhook di Fusion è stata ottimizzata con questa versione. Il servizio che accetta i webhook è ora separato dall’accodamento e da altri processi. Questa modifica consente a Fusion di elaborare le code dei webhook a una velocità più rapida e coerente.

Durante l’implementazione di questa modifica, siamo stati in grado di comprendere meglio il tempo di elaborazione del registro previsto per gli eventi del webhook in coda. La pagina del visualizzatore del webhook di Fusion non deve essere precedente a 1 minuto.

Per visualizzare gli eventi del webhook attualmente in coda, passa a Webhook nel menu di navigazione a sinistra. Le icone del camion con un numero nel numeratore indicano gli eventi di coda per quel webhook. Fai clic sull’icona del carrello per visualizzare gli eventi in coda.


**I webhook inutilizzati verranno disattivati o eliminati**

Sono state apportate alcune modifiche al modo in cui Workfront Fusion gestisce i webhook inutilizzati. Ora, i webhook vengono disattivati automaticamente se si applica una delle seguenti condizioni:

* Il webhook non è stato connesso ad alcuno scenario per più di 5 giorni.
* Il webhook viene utilizzato solo in scenari che rimangono inattivi per più di 30 giorni.

I webhook disattivati vengono eliminati e ne viene automaticamente annullata la registrazione se non connessi ad alcun scenario e se in stato di disattivazione da oltre 30 giorni.
