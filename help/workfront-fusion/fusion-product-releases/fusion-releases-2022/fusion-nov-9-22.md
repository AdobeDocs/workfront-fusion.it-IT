---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Attività di rilascio di Workfront Fusion: settimana del 7 novembre 2022'
description: Questa pagina descrive tutti i miglioramenti apportati ad Adobe Workfront Fusion la settimana del 7 novembre 2022.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Attività di rilascio di Workfront Fusion: settimana del 7 novembre 2022

**Ottimizzazione coda webhook**

La coda del webhook di Fusion è stata ottimizzata con questa versione. Il servizio che accetta i webhook è ora separato dall’accodamento e da altri processi. Questa modifica consente a Fusion di elaborare le code dei webhook a una velocità più rapida e coerente.

Durante l’implementazione di questa modifica, siamo stati in grado di comprendere meglio il tempo di elaborazione del registro previsto per gli eventi del webhook in coda. La pagina del visualizzatore del webhook di Fusion non deve essere precedente a 1 minuto.

Per visualizzare gli eventi del webhook attualmente in coda, passa a Webhook nel menu di navigazione a sinistra. Le icone del camion con un numero nel numeratore indicano gli eventi di coda per quel webhook. Fai clic sull’icona del carrello per visualizzare gli eventi in coda.


**I webhook inutilizzati verranno disattivati o eliminati**

Sono state apportate alcune modifiche al modo in cui Workfront Fusion gestisce i webhook inutilizzati. Ora, i webhook vengono disattivati automaticamente se si applica una delle seguenti condizioni:

* Il webhook non è stato connesso ad alcuno scenario per più di 5 giorni.
* Il webhook viene utilizzato solo in scenari inattivi, che sono stati inattivi per più di 30 giorni.

I webhook disattivati vengono eliminati e annullati automaticamente se non sono connessi ad alcun scenario e se sono in stato disattivato da oltre 30 giorni.
