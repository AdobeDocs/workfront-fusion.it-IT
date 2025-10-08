---
title: Panoramica API
description: Le interfacce API (Application Programming Interface) consentono alle applicazioni e ai servizi di comunicare tra loro. Fusion utilizza le API per comunicare con l’applicazione a cui ti stai connettendo. Ogni applicazione ha un’API separata.
author: Becky
feature: Workfront Fusion
source-git-commit: b30aac8040cc0b6bcad92914b1c0997a8ddebdd5
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Panoramica delle API in Fusion

<!--Add me to TOCs-->

Le interfacce API (Application Programming Interface) consentono alle applicazioni e ai servizi di comunicare tra loro. Fusion utilizza le API per comunicare con le applicazioni a cui ti stai connettendo.

Le API vengono create e controllate dai proprietari dell’applicazione. Ad esempio, l’API di Workfront è di proprietà del team Workfront di Adobe e l’API di Microsoft Graph è di proprietà di Microsoft. Il proprietario dell’API definisce le azioni disponibili tramite l’API.

## Considerazioni

Il fatto che le API siano definite dai rispettivi proprietari e non da Fusion porta ad alcune considerazioni importanti:

* **È possibile utilizzare Fusion per connettersi a qualsiasi app o servizio che dispone di un&#39;API pubblica**, indipendentemente dal fatto che Fusion offra o meno un connettore dedicato all&#39;app o al servizio. Puoi utilizzare i connettori universali di Fusion per inserire queste app o servizi negli scenari.

  Per un elenco dei connettori universali, vedere [Connettori universali](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **Le modifiche apportate dal proprietario all&#39;API di un&#39;applicazione possono influire sulla funzionalità di Fusion.** Se le modifiche sono sufficientemente severe, Fusion potrebbe dover aggiornare i moduli o i tipi di connessione oppure, in casi estremi, potrebbe creare un nuovo connettore per l&#39;applicazione.

  Per ulteriori informazioni su queste situazioni estreme, note come &quot;modifiche che causano interruzioni&quot;, vedere [Modifiche che causano interruzioni](#breaking-changes) in questo articolo.


## Interruzione delle modifiche

Una causa comune per l’interruzione delle modifiche è la rimozione definitiva, quando il proprietario di un’API rimuove una parte o la totalità di un’API dalla disponibilità. In questo caso, il team Fusion si impegna al massimo per riallineare rapidamente la funzionalità Fusion alla nuova versione dell’API dell’applicazione. Questo di solito assume la forma di nuovi moduli, tipi di connessione o connettori.

Poiché gli scenari di Fusion sono configurati con dati specifici, potrebbe essere necessario aggiornare gli scenari.

* Se le modifiche sono correlate all&#39;autenticazione o all&#39;autorizzazione, potrebbe essere necessario aggiornare le connessioni per tale applicazione.
* Se le modifiche erano relative a un’azione specifica (endpoint) nell’API, potrebbe essere necessario aggiornare tutti i moduli relativi a tale azione a una nuova versione del modulo.
* Se l’intera versione API utilizzata da Fusion è obsoleta, potrebbe essere necessario aggiornare tutti i moduli del connettore a una nuova versione.

In molti casi, è possibile eseguire l&#39;aggiornamento alla nuova versione di un modulo senza dover riconfigurare tale modulo.

Per informazioni e istruzioni sull&#39;aggiornamento di un modulo, vedere [Aggiornare un modulo a una nuova versione](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
