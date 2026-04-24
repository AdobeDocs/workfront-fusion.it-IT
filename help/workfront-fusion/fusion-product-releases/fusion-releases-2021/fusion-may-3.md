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
source-git-commit: 80f2d078cd624424f23bd007e852f49643fec7f3
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 29%

---

# Attività di rilascio di Workfront Fusion: settimana del 3 maggio 2021

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
