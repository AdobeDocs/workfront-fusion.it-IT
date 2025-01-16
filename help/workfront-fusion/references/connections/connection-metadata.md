---
title: Metadati di connessione
description: Fusion utilizza i metadati per identificare gli attributi importanti di una connessione.
author: Becky
feature: Workfront Fusion
exl-id: b41fbe8c-30fa-49d0-8a24-3535642b97ae
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# Metadati di connessione

Fusion utilizza i metadati per identificare gli attributi importanti di una connessione.

È possibile impostare i metadati della connessione durante la creazione di una nuova connessione. Questi attributi si trovano nella stessa finestra di dialogo utilizzata per impostare una connessione:

![Metadati di connessione](assets/connection-metadata-setup.png)

Gli utenti di Fusion possono visualizzare e modificare le connessioni dall&#39;area Connessioni.

![Metadati di connessione nell&#39;area Connessioni](assets/connections-area-metadata.png)

## Tipo di ambiente

Le connessioni di fusione possono essere utilizzate sia da sistemi di produzione che da sistemi non di produzione. Puoi contrassegnare il tipo di ambiente a cui si connette una connessione, per proteggere gli ambienti di produzione.

Il tipo di ambiente, come altri metadati di connessione, viene utilizzato solo a scopo informativo. Gli utenti sono responsabili dell’impostazione accurata di questo attributo e dell’utilizzo di una connessione con l’ambiente corretto in uno scenario.

## Tipo di autenticazione

Le connessioni Fusion possono essere utilizzate sia per gli account di servizio che per gli account personali. Gli account di servizio vengono utilizzati per l’autenticazione quando uno scenario si automatizza come Fusion. Gli account personali sono autenticazioni basate su una persona specifica. Il tipo di autenticazione utilizzato dipende dai requisiti dello scenario. Gli account personali devono essere utilizzati per azioni utente automatizzate. Ad esempio, se uno scenario Fusion automatizza l’approvazione da parte di una persona specifica, il tipo di autenticazione deve essere per tale persona. In caso contrario, Fusion agisce come Fusion e il tipo deve essere Account di servizio.

Il tipo di autenticazione, come altri metadati di connessione, viene utilizzato solo a scopo informativo. Gli utenti sono responsabili dell’impostazione accurata di questo attributo e dell’utilizzo del tipo di connessione corretto in uno scenario.

Per ulteriori informazioni sui tipi di autenticazione, vedere [Autenticazione](https://developer.adobe.com/developer-console/docs/guides/authentication/) nella Guida all&#39;autenticazione di Adobe.

## Risorse

* Per istruzioni sulla gestione dei metadati della connessione, vedere [Gestire le connessioni](/help/workfront-fusion/create-scenarios/connect-to-apps/manage-connections.md).
