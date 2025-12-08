---
title: Panoramica delle connessioni
description: Per la maggior parte delle app, è necessario creare una connessione tramite la quale Adobe Workfront Fusion può comunicare con il servizio di terze parti specificato in base alle impostazioni dello scenario specifico.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---

# Panoramica delle connessioni

Workfront Fusion richiede una connessione per la maggior parte delle applicazioni.  Utilizza questa connessione per comunicare con il servizio di terze parti specificato.

Ad esempio, se desideri creare uno scenario che recuperi informazioni da Workfront, dovrai concedere a Workfront Fusion l’autorizzazione per accedere al tuo account Workfront.

Una connessione rappresenta l’autorizzazione e le autorizzazioni utilizzate da Fusion per accedere all’applicazione. È possibile creare una o più connessioni per ciascuna applicazione utilizzata negli scenari e utilizzare la stessa connessione in più moduli o scenari.

La maggior parte delle connessioni viene utilizzata solo per una singola applicazione. Ad esempio, non è possibile utilizzare una connessione Workfront in un modulo [!UICONTROL Salesforce]. Alcune applicazioni di [!DNL Adobe] possono condividere le connessioni. Per informazioni dettagliate, consulta gli articoli relativi alle applicazioni elencate in [Documentazione di riferimento per applicazioni e moduli in Fusion: indice degli articoli](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Le connessioni sono di proprietà dei team. Tutti i membri di un team dispongono del relativo accesso alle connessioni, mentre gli utenti al di fuori del team non ne dispongono.

## Diritti di accesso

Per ciascuna connessione, Workfront Fusion richiede solo i diritti di accesso necessari per completare correttamente un determinato scenario. Ad esempio, se crei uno scenario per scaricare un documento da Workfront, Workfront Fusion non richiederà l’autorizzazione per la creazione di un nuovo progetto. In seguito, se riterrai necessario creare un progetto, potrai aggiornare la connessione o crearne una nuova in grado di creare progetti.

Non tutti i servizi consentono di limitare l’accesso ad attività specifiche. In questi casi, Workfront Fusion deve richiedere diritti di accesso completi. Per ulteriori informazioni su come limitare l’accesso di Workfront Fusion all’account registrato per tali servizi, consulta la documentazione specifica dell’applicazione elencata in [Documentazione di riferimento per applicazioni e moduli in Fusion: indice degli articoli](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
