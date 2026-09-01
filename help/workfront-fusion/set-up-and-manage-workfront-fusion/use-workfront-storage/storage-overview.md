---
title: Panoramica sull’archiviazione
description: Storage è una pagina di Workfront Fusion che offre ai team l'accesso diretto ai repository di Adobe Enterprise Storage Management (ESM), consentendo agli utenti di sfogliare le cartelle, caricare e scaricare file, visualizzare la cronologia delle versioni e creare scenari di automazione.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# Panoramica sull’archiviazione

<!--Add to navigation articles once this goes to production-->

L&#39;area di storage in Workfront Fusion consente ai team di accedere direttamente agli archivi Adobe Enterprise Storage Management (ESM). Gli utenti possono sfogliare le cartelle, caricare e scaricare file, visualizzare la cronologia delle versioni e creare scenari di automazione, il tutto senza uscire da Fusion.

Lo storage è di proprietà dei team e richiede l’onboarding dell’organizzazione in Adobe Identity Management System (IMS) con accesso allo storage Adobe.

I file in Fusion Storage vengono rispecchiati in Adobe Files (adobe.com/files), pertanto tutti i file a cui è possibile accedere in Adobe Files sono accessibili in Fusion Storage.

Per istruzioni sull&#39;uso di Storage, vedere:

* [Inizializza archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [Visualizzazione e gestione dello storage in Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [Carica file nell&#39;archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [Scaricare i file dall&#39;archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [Elimina file dall&#39;archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [Visualizzare la cronologia delle versioni dei file in Archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [Creare scenari dall’archiviazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## Prerequisiti per l’archiviazione

Per utilizzare l&#39;area di archiviazione di Workfront Fusion, è necessario che siano soddisfatte le seguenti condizioni:

* L&#39;organizzazione è stata integrata in **Adobe Identity Management System (IMS)**
* L&#39;organizzazione dispone di **archiviazione Adobe**
* L&#39;utente è connesso all&#39;**organizzazione Adobe IMS corretta** (quella corrispondente all&#39;organizzazione Fusion selezionata)
* L&#39;account dell&#39;utente dispone dell&#39;accesso **ad Adobe Storage**

## Glossario

Quando si utilizza

| Termine | Definizione |
| ------ | ----------- |
| **Archivio** | Contenitore di storage di livello superiore in Adobe ESM, in genere mappato a un progetto o a un’area di lavoro |
| **Connessione** | Un collegamento sicuro tra Fusion e Adobe Storage, creato automaticamente durante l’inizializzazione. Utilizza l’autenticazione Adobe IMS con l’aggiornamento automatico del token |
| **ESM** | Enterprise Storage Management, il servizio di archiviazione dei file cloud di Adobe |
| **IMS** | Adobe Identity Management System, la piattaforma di autenticazione e identità di Adobe |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
