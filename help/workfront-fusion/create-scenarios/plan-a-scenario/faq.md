---
title: Domande frequenti sulla pianificazione dello scenario
description: Le informazioni contenute in questo articolo possono essere utili quando si inizia a creare scenari in Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---

# Domande frequenti sulla pianificazione dello scenario

Le informazioni contenute in questo articolo possono essere utili quando si inizia a creare scenari in Workfront Fusion.

## Che cos&#39;è uno scenario?

### Risposta

Uno scenario definisce una sequenza di passaggi che devono essere eseguiti da Adobe Workfront Fusion. Per ogni scenario, specificare l&#39;origine dati, i dati da utilizzare e la modalità di elaborazione dei dati. Fusion consente di creare scenari semplici o complessi, in grado di soddisfare i casi d’uso per la tua organizzazione.

Per ulteriori informazioni sugli scenari, vedere [Panoramica dello scenario](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## Quanti moduli posso utilizzare in uno scenario?

### Risposta

Puoi utilizzare tutti i moduli che desideri in uno scenario. È possibile separare i moduli in cicli di lavorazione e specificare i dati che devono scorrere in ogni ciclo di lavorazione. È inoltre possibile utilizzare l&#39;output di un modulo come input per un altro modulo.

Anche se non esiste un limite al numero di moduli in uno scenario, più di 150 moduli possono influire sulle prestazioni dello scenario.

Per ulteriori informazioni sui moduli, vedere [Panoramica modulo](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## Workfront Fusion può funzionare con i file?

### Risposta

Sì. Workfront Fusion può ricevere, salvare, trasformare, convertire e crittografare i file. Fusion offre inoltre un&#39;ampia gamma di funzioni integrate progettate per consentire agli utenti di lavorare in modo efficace e creativo con i dati contenuti nei file.

Per ulteriori informazioni sull&#39;utilizzo dei file in Fusion, vedere [Mappare un file tra moduli](/help/workfront-fusion/create-scenarios/map-data/map-files.md).

## Alcuni trigger consentono l’esecuzione immediata degli scenari. Cosa significa &quot;istantaneamente&quot;?

### Risposta

Gli scenari possono essere eseguiti a intervalli in base alla pianificazione specificata, ad esempio ogni ora o ogni 5 minuti. Esistono trigger speciali, denominati trigger istantanei (webhook), che possono avviare lo scenario immediatamente dopo aver ricevuto i dati da un determinato servizio. Fusion elabora i dati ricevuti immediatamente, senza attendere la successiva esecuzione pianificata.

Per ulteriori informazioni sulla differenza tra i trigger di polling e i trigger istantanei, vedere [Moduli trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) nell&#39;articolo Panoramica dei moduli.

## Che cos&#39;è un&#39;operazione?

### Risposta

Per operazione si intende qualsiasi operazione eseguita da un modulo. Un&#39;operazione si verifica, ad esempio, ogni volta che viene eseguito un trigger e ogni volta che un&#39;azione esegue un&#39;attività.

Alcuni piani Fusion si basano sul numero di operazioni utilizzate dall&#39;organizzazione.

Per ulteriori informazioni sulle operazioni, vedere [Operazioni](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Che cos’è il trasferimento di dati?

### Risposta

Il trasferimento di dati si riferisce alla quantità di dati trasferiti attraverso lo scenario. Ad esempio, uno scenario che recupera un’immagine da 100 KB da Workfront, quindi carica l’immagine in un provider di archiviazione documenti. La quantità di dati utilizzata in questo scenario è di 200 KB.

## Che cos&#39;è una connessione?

### Risposta

Una connessione è il collegamento tra l’account Workfront Fusion e il servizio di terze parti che desideri utilizzare. La connessione può essere creata durante la modifica di uno scenario.

Per ulteriori informazioni, vedere [Panoramica della connessione](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## Cosa sono gli aggregatori?

### Risposta

Un [!UICONTROL Aggregator] unisce i dati in un&#39;unica raccolta. Un esempio è dato dai file compressi in un archivio zip e inviati come allegato e-mail.

Per ulteriori informazioni, vedere il modulo [[!UICONTROL Aggregator]](/help/workfront-fusion/references/modules/aggregator-module.md).

## Cosa succede se consento a Workfront Fusion di elaborare un’e-mail contenente più di un allegato?

### Risposta

Se utilizzi il modulo [!UICONTROL E-mail] [!UICONTROL Recupera allegati], ogni allegato viene inviato singolarmente tramite gli altri moduli dello scenario. Moduli simili sono disponibili anche in altre app che ricevono più file contemporaneamente.
