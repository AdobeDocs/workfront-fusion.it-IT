---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Attività di rilascio di Workfront Fusion: settimana del 16 novembre 2020'
description: Questa pagina descrive tutti i miglioramenti apportati ad Adobe Workfront Fusion la settimana del 16 novembre 2020.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 69e4a458-fd32-4dcd-be43-19a9467cf678
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Attività di rilascio di Workfront Fusion: settimana del 16 novembre 2020

Questa pagina descrive tutti i miglioramenti apportati ad Adobe Workfront Fusion la settimana del 16 novembre 2020.

Per un elenco di tutte le modifiche recenti, vedere [Attività di Adobe Workfront Fusion release](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Per un elenco delle correzioni di bug recenti in Workfront Fusion, vedere la pagina [Aggiornamenti di manutenzione di Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=it) e verificare la presenza di eventuali aggiornamenti etichettati Aggiornamento di manutenzione di Workfront Fusion.

## Aggiornamenti al connettore Jira Cloud

Per espandere le modalità di utilizzo del connettore Jira Cloud, sono stati aggiunti tre nuovi moduli:

* Aggiungi problema a sprint
* Elenca record
* Cerca record

Sono stati inoltre aggiornati i moduli esistenti per supportare il tipo di oggetto &quot;Sprint&quot;. In precedenza, era possibile accedere all’oggetto &quot;Sprint&quot; solo tramite il modulo Chiamata API personalizzata.

## L’ID di esecuzione è ora disponibile per la mappatura negli scenari

L’ID di esecuzione di uno scenario è ora disponibile nel pannello di mappatura. Questo ID rappresenta un’esecuzione specifica dello scenario e può essere utilizzato come metadati. Ad esempio, l’ID di esecuzione può essere salvato con un record creato da Fusion, in modo da poter determinare in seguito quale esecuzione di Fusion ha creato il record. Puoi trovare l’ID esecuzione nel pannello di mappatura in Funzioni generali.

## Scelte rapide da tastiera per gli scenari Workfront Fusion 2.0

Per semplificare la creazione dello scenario, sono state aggiunte alcune scelte rapide da tastiera:

* Ctrl/Comando+Maiusc+Invio: esegui uno scenario una volta
* Ctrl/Comando + Maiusc + S: salvare uno scenario

## Aggiornamenti al connettore Office 365 Excel

Per espandere le modalità di utilizzo del connettore Office 365 Excel, sono stati aggiunti alcuni nuovi moduli. Ora è possibile:

* Attivare un modulo da modifiche a cartelle di lavoro
* Cercare o scaricare cartelle di lavoro
* Elencare fogli di lavoro, righe del foglio di lavoro, tabelle o righe di tabella
* Aggiornare una riga di tabella o di foglio di lavoro
* Eliminare una riga di tabella o di foglio di lavoro
* Recuperare i metadati per una tabella
* Effettuare una chiamata API personalizzata

I moduli precedentemente disponibili sono ancora presenti nell’app.


## Utilizzare OAuth 2.0 nelle connessioni dell&#39;app Workfront

Il connettore Workfront è stato aggiornato per utilizzare OAuth 2.0. Grazie a questo aggiornamento, è più semplice apportare modifiche alle connessioni alle app Workfront. Ad esempio, se qualcosa sulla connessione cambia (come una password), non è più necessario aggiornare ogni singola connessione negli scenari. Inoltre, OAuth2 offre altri vantaggi come una maggiore sicurezza e la possibilità di utilizzare il Single Sign-On (SSO).

Le connessioni esistenti al momento non richiedono alcuna modifica. Tuttavia, puoi autorizzare nuovamente le connessioni esistenti se desideri sfruttare i vantaggi di OAuth 2.0.
