---
title: Inizializza archiviazione
description: Quando un utente passa a Archiviazione per la prima volta, viene visualizzata una schermata di inizializzazione che crea una connessione protetta a Archiviazione Adobe per conto del team.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# Inizializzazione dell&#39;archiviazione in Workfront Fusion

Per poter visualizzare archivi, cartelle e file nell’archiviazione cloud Adobe, è necessario inizializzare l’area di archiviazione Fusion.

Per una panoramica dell&#39;archiviazione, vedere [Panoramica archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

## Inizializza archiviazione

1. In Workfront Fusion, fai clic su **Archiviazione** nell&#39;area di navigazione a sinistra.
1. Fare clic su **Inizializza archiviazione**.

Fusion crea automaticamente una connessione protetta allo storage Adobe per conto del team.

Una volta stabilita la connessione, Fusion carica gli archivi di archiviazione del team.

## Risoluzione dei problemi di inizializzazione

| Messaggio | Motivo | Operazioni che l&#39;utente deve eseguire |
| -------- | -------- | ------------------------ |
| **Accesso limitato** | L’organizzazione non è integrata in Adobe IMS. | Contatta l’amministratore dell’organizzazione per completare l’onboarding IMS. |
| **Organizzazione non corrispondente** | L’utente accede a un’organizzazione Adobe diversa da quella selezionata in Fusion. | Esci, quindi accedi di nuovo con l’organizzazione Adobe IMS corretta. |
| **Accesso negato** | L’account dell’utente non dispone delle autorizzazioni necessarie oppure Adobe Storage non è disponibile per l’organizzazione. | Verifica le autorizzazioni dell’account con l’amministratore dell’organizzazione. Dopo la risoluzione, fare clic su **Riprova**. |
| **Impossibile trovare archiviazione** | La connessione è stata stabilita, ma non è stato trovato alcun archivio. | Verifica che sia stato eseguito il provisioning dello storage Adobe per l’organizzazione. Dopo la verifica, fare clic su **Carica archiviazione** per riprovare. |
