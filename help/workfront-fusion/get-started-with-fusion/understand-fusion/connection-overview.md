---
title: Panoramica della connessione
description: Per la maggior parte delle app, è necessario creare una connessione tramite la quale Adobe Workfront Fusion possa comunicare con il servizio di terze parti in base alle impostazioni dello scenario specifico.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Panoramica della connessione

Workfront Fusion richiede una connessione per la maggior parte delle applicazioni.  Utilizza questa connessione per comunicare con il servizio di terze parti specificato.

Ad esempio, se desideri creare uno scenario che recuperi informazioni da Workfront, devi concedere a Workfront Fusion l’autorizzazione per accedere al tuo account Workfront.

Una connessione rappresenta l&#39;autorizzazione e le autorizzazioni utilizzate da Fusion per accedere all&#39;applicazione. È possibile creare una o più connessioni per ogni applicazione utilizzata negli scenari e utilizzare la stessa connessione in più moduli o scenari.

La maggior parte delle connessioni viene utilizzata solo per una singola applicazione. Ad esempio, non è possibile utilizzare una connessione Workfront in un modulo [!UICONTROL Salesforce]. Alcune applicazioni di [!DNL Adobe] possono condividere le connessioni. Per informazioni dettagliate, vedere gli articoli relativi alle applicazioni elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Le connessioni sono di proprietà dei team. Tutti i membri di un team hanno accesso alle connessioni del team e gli utenti all&#39;esterno di un team non hanno accesso alle connessioni del team.

## Diritti di accesso

Per ogni connessione, Workfront Fusion richiede solo i diritti di accesso necessari per completare correttamente un determinato scenario. Se ad esempio si crea uno scenario per scaricare un documento da Workfront, Workfront Fusion non richiede l&#39;autorizzazione per la creazione di un nuovo progetto. In seguito, se scopri che è necessario creare un progetto, puoi aggiornare la connessione o crearne una nuova in grado di creare progetti.

Non tutti i servizi consentono di limitare l’accesso ad attività specifiche. In questi casi, Workfront Fusion deve richiedere diritti di accesso completi. Per ulteriori informazioni su come limitare l&#39;accesso a Workfront Fusion all&#39;account registrato per tali servizi, vedere la documentazione specifica dell&#39;applicazione elencata in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
