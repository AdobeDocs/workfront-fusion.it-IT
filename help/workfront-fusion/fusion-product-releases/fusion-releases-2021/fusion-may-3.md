---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Attività sulla versione di Workfront Fusion: settimana del 3 maggio 2021'
description: Questa pagina descrive tutti i miglioramenti apportati a Adobe Workfront Fusion la settimana del martedì 3 maggio 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
TQID: 'https://experienceleague.adobe.com/GZ5W-9Q1Y9M-cCVN1CupZVs8GuQPy4Dusifz-5sxJm8'
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 35%
---
# Attività sulla versione di Workfront Fusion: settimana del 3 maggio 2021

Questa pagina descrive tutti i miglioramenti apportati a Adobe Workfront Fusion la settimana del martedì 3 maggio 2021.

Per un elenco di tutte le modifiche recenti, consulta [Attività sulla versione di Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Per un elenco delle correzioni di bug recenti in Workfront Fusion, consulta la pagina [Aggiornamenti di manutenzione di Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=it) e controlla la presenza di eventuali aggiornamenti etichettati Aggiornamento di manutenzione di Workfront Fusion.

## Il connettore Salesforce ora può effettuare ricerche utilizzando SOQL

Il modulo Salesforce > Cerca record ora dispone dell’opzione per eseguire ricerche utilizzando SOQL (Salesforce Object Query Language). È inoltre possibile eseguire ricerche utilizzando le opzioni disponibili in precedenza (SOSL e ricerche semplici).

## Il nuovo tipo di connessione nel connettore Azure DevOps richiede meno ambiti

Per migliorare la sicurezza, è stato aggiunto un nuovo tipo di connettore al connettore Workfront Fusion Azure DevOps. Ora, quando crei una connessione in un modulo DevOps di Azure, puoi scegliere tra due tipi di connessione:

* DevOps di Azure

  Questo nuovo tipo di connessione limita gli ambiti a quelli specificamente necessari per Workfront Fusion.

* Azure DevOps (Richiedi tutti gli ambiti)

  Si tratta del tipo di connessione legacy, che richiede tutti gli ambiti disponibili in una connessione ad Azure DevOps.

È consigliabile utilizzare il tipo di connessione DevOps di Azure in tutti i nuovi scenari che utilizzano Azure DevOps. È inoltre consigliabile modificare i moduli DevOps di Azure negli scenari esistenti in modo da utilizzare il nuovo tipo di connessione. Il tipo di connessione legacy Azure DevOps (Richiedi tutti gli ambiti) diventerà obsoleto nel prossimo futuro.
