---
title: Panoramica delle API
description: Le interfacce API (Application Programming Interface) consentono le comunicazioni tra le applicazioni e i servizi. Fusion utilizza le API per comunicare con l’applicazione a cui ti connetti. Ciascuna applicazione dispone di un’API separata.
author: Becky
feature: Workfront Fusion
source-git-commit: 74308a6a43418296b29739f03683f23357d545bc
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 87%

---

# Panoramica delle API in Fusion

<!--Add me to TOCs-->

Le interfacce API (Application Programming Interface) consentono le comunicazioni tra le applicazioni e i servizi. Fusion utilizza le API per comunicare con le applicazioni a cui ti connetti.

Le API vengono create e controllate dai proprietari dell’applicazione. Ad esempio l’API Workfront è di proprietà del team Workfront di Adobe e l’API Microsoft Graph è di proprietà di Microsoft. Il proprietario dell’API definisce le azioni disponibili tramite l’API.

>[!NOTE]
>
>Workfront Fusion dispone di una propria API che è possibile utilizzare per automatizzare le azioni in Fusion.
>Le API vengono rilasciate in modo incrementale e sono attualmente contrassegnate come sperimentali. Il team di Fusion sta sviluppando ed espandendo attivamente le API, e verranno pubblicati aggiornamenti non appena saranno disponibili nuove funzionalità.
>Per la documentazione sull&#39;API di Workfront Fusion, vedere [API di Workfront Fusion](https://developer.adobe.com/workfront-fusion-apis/).

## Considerazioni

Il fatto che le API siano definite dai rispettivi proprietari e non da Fusion implica alcune considerazioni importanti:

* **È possibile utilizzare Fusion per connettersi a qualsiasi app o servizio che dispone di un’API pubblica**, indipendentemente dal fatto che Fusion offra o meno un connettore dedicato per l’app o il servizio. Puoi utilizzare i connettori universali di Fusion per inserire queste app o servizi nei tuoi scenari.

  Per un elenco dei connettori universali, consulta [Connettori universali](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **Le modifiche apportate dal proprietario all’API di un’applicazione possono influire sulla funzionalità di Fusion.** Se le modifiche sono sufficientemente rilevanti, Fusion potrebbe dover aggiornare i moduli o i tipi di connessione, oppure, in casi estremi, potrebbe dover creare un nuovo connettore per l’applicazione.

  Per ulteriori informazioni su queste situazioni estreme, note come “breaking change”, consulta [Modifiche che introducono errori o incompatibilità](#breaking-changes) in questo articolo.


## Modifiche che introducono errori o incompatibilità

Spesso le modifiche che introducono errori o incompatibilità sono dovute a funzionalità che vengono rimosse, ad esempio se il proprietario di un’API la ritira in parte o del tutto. In questi casi, il team Fusion si impegna al massimo per riallineare rapidamente la funzionalità di Fusion alla nuova versione dell’API dell’applicazione. Di solito ciò si traduce in nuovi moduli, tipi di connessione o connettori.

Poiché i tuoi scenari di Fusion sono configurati con dati specifici, potresti doverli aggiornare.

* Se le modifiche sono correlate all’autenticazione o all’autorizzazione, potresti dover aggiornare le connessioni per l’applicazione.
* Se le modifiche sono relative a un’azione specifica (endpoint) dell’API, potresti dover aggiornare tutti i moduli correlati a tale azione a una nuova versione.
* Se l’intera versione API utilizzata da Fusion risulta obsoleta, potresti dover aggiornare tutti i moduli del connettore a una nuova versione.

In molti casi puoi eseguire l’aggiornamento alla nuova versione di un modulo senza dover riconfigurare il modulo stesso.

Per informazioni e istruzioni sull’aggiornamento di un modulo, consulta [Aggiornare un modulo a una nuova versione](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
