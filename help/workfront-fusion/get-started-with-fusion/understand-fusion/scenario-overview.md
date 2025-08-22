---
title: Panoramica dello scenario
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: de81ad4c-27e5-4b6c-acf0-f01a8c85922e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Panoramica dello scenario

Il ruolo di Adobe Workfront Fusion è quello di automatizzare i processi in modo che gli utenti non debbano dedicare più tempo alle attività di routine. Funziona tramite il collegamento di azioni all’interno e tra app e servizi per creare uno scenario che trasferisce e trasforma automaticamente i dati. Lo scenario in cui si creano controlli i dati in un’app o in un servizio ed elabora tali dati in modo da fornire il risultato desiderato.

Uno scenario è costituito da una serie di moduli che indicano come i dati devono essere trasformati all’interno di un’app o trasferiti tra app e servizi web.

## Panoramica degli elementi dello scenario

Uno scenario è costituito da elementi diversi. Comprendere la terminologia di tali elementi semplifica l’utilizzo della documentazione.

* [Scenario](#scenario)
* [Trigger](#trigger)
* [Modulo](#module)
* [Percorso](#route)
* [Segmento scenario](#scenario-segment)
* [Connettore ](#connector)

### Scenario

Uno **scenario** è una serie di passaggi automatizzati creati dall&#39;utente per spostare e manipolare i dati. Il termine &quot;scenario&quot; si riferisce all&#39;intero gruppo di fasi collegate.

![Scenario](assets/entire-scenario-scenario.png)

### Trigger

Uno scenario inizia con un **trigger**. Il trigger controlla i dati nuovi e aggiornati e avvia lo scenario quando si applicano determinate condizioni configurate nel modulo. Gli attivatori possono essere configurati per avviare uno scenario secondo una pianificazione (polling) o ogni volta che si verificano modifiche ai dati (istantanei).

![Attivatore](assets/scenario-trigger.png)

### Modulo

Il trigger è seguito da **moduli**. Un modulo rappresenta un singolo passaggio in uno scenario che esegue un’azione specifica. I moduli sono configurati e concatenati tra loro per creare scenari.

![Modulo](assets/scenario-module.png)

### Percorso

Uno scenario può essere diviso in **route**. Una route è una sezione dello scenario che può essere o meno utilizzata per un determinato bundle di dati. Le route vengono configurate utilizzando un modulo router e filtri.

![Route](assets/scenario-route.png)

### Segmento scenario

Un segmento di scenario è una sezione di uno scenario costituita da una serie di moduli contigui che si connettono tutti alla stessa applicazione. I segmenti di scenario spesso rappresentano un breve flusso di lavoro nell’applicazione.

![Segmento scenario](assets/scenario-segment.png)

### Connettore 

Un connettore è il set di moduli per una determinata applicazione. Workfront Fusion offre connettori per molte applicazioni di lavoro comuni, come Workfront, Salesforce e Jira, nonché connettori generici che possono essere utilizzati per qualsiasi servizio web.

![Connettori](assets/scenario-connectors.png)

## Esempi

Espandi le sezioni seguenti per visualizzare scenari di esempio e le relative spiegazioni.

+++**Automazione dei processi in Adobe Workfront**

Workfront Fusion consente di automatizzare flussi di lavoro semplici o complessi all’interno di Workfront, risparmiando tempo e garantendo un’esecuzione coerente del processo.

In questo esempio, lo scenario si attiva quando un campo specificato cambia in un’attività o in un problema in Workfront. Quando viene attivato, lo scenario ottiene informazioni nel progetto correlato e crea un aggiornamento personalizzato per una persona assegnata a un ruolo specifico nel progetto.

![Esempio di modello](assets/fusion-template-example.png)

+++

+++**Connessione di Workfront a un&#39;altra app o servizio Web**

>[!NOTE]
>
>Se la tua organizzazione utilizza il modello di licenza legacy, per connettersi ad altre applicazioni è necessario disporre di una licenza Workfront Fusion for Work Automation and Integration.

Workfront Fusion è in grado di connettersi ad altre applicazioni e servizi Web. È possibile accedere, importare, manipolare o esportare dati da altre applicazioni, integrandoli con Workfront o tra loro.

Molte applicazioni dispongono di connettori Workfront Fusion dedicati. Se non è disponibile un connettore dedicato per l&#39;applicazione a cui si desidera accedere, è possibile utilizzare i moduli HTTP o SOAP di Workfront Fusion per connettersi all&#39;applicazione tramite la relativa API.

In questo esempio, lo scenario viene attivato quando un utente viene aggiunto a un foglio di calcolo [!DNL Excel]. Lo scenario controlla se l’utente si trova in Workfront. In caso contrario, l’utente verrà creato in Workfront e il relativo ID utente Workfront verrà nuovamente aggiunto al foglio di calcolo.

![Esempio di integrazione](assets/fusion-integration-example.png)

Per un elenco dei connettori dedicati, vedere [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).


>[!IMPORTANT]
>
>Adobe Workfront Fusion è in grado di connettersi a quasi tutti i servizi web. Se l’app con cui desideri lavorare non dispone di un connettore Workfront Fusion dedicato, puoi utilizzare connettori universali per connettersi all’app o al servizio.
>
>Per un elenco dei connettori universali, vedere [Connettori universali](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

+++

## Riferimenti

* Per un glossario dei termini utilizzati in Workfront Fusion, vedere [Glossario di Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).
* Per iniziare a creare uno scenario di esercitazione, vedere [Creare uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).
* Per informazioni sulla creazione e la gestione degli scenari, consulta gli articoli elencati in:
   * [Creare scenari](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)
   * [Gestisci scenari](/help/workfront-fusion/manage-scenarios/manage-scenarios-toc.md)
