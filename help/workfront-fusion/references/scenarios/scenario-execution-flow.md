---
content-type: overview
title: Flusso di esecuzione dello scenario
description: Questo articolo spiega come viene eseguito uno scenario e come i dati scorrono attraverso di esso. Vengono inoltre illustrate le aree in cui è possibile trovare informazioni sui dati elaborati e su come leggerle.
author: Becky
feature: Workfront Fusion
exl-id: bd4f05e2-df3c-4848-9a70-3df18ca4461b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Flusso di esecuzione dello scenario

Questo articolo spiega come viene eseguito uno scenario, come scorrono i dati al suo interno e come visualizzare i dati elaborati da ciascun modulo.

Per visualizzare il modo in cui i dati scorrono attraverso uno scenario attivo, vedere [Visualizzare il flusso di dati in uno scenario in esecuzione](/help/workfront-fusion/manage-scenarios/view-scenario-data-flow.md).

## Flusso di esecuzione dello scenario

Dopo aver configurato correttamente e attivato uno scenario, questo viene eseguito in base alla pianificazione definita.

All’inizio dello scenario, il primo modulo risponde a un evento che è stato impostato per osservare. Quando restituisce i dati, questi vengono inseriti in bundle. Lo scenario restituisce un bundle per ogni evento. Ad esempio, se un modulo è impostato per la ricerca di problemi, restituirà un bundle di dati per ogni problema rilevato.

Se il modulo trigger restituisce eventuali bundle di dati, tali bundle passano al modulo successivo e lo scenario continua, passando i bundle attraverso ciascun modulo successivo, uno alla volta.

Se i bundle vengono elaborati correttamente in tutti i moduli, lo scenario viene contrassegnato come riuscito nella pagina dei dettagli dello scenario.

### Esempio: [!UICONTROL Workfront Fusion per l&#39;automazione del lavoro]

>[!BEGINSHADEBOX]

**Esempio:** In questo scenario che controlla le richieste in arrivo in Workfront e le converte in progetti Workfront, i dati scorrono come segue:

Il primo passaggio dello scenario, eseguito dal primo modulo, consiste nel controllare le richieste. Ogni richiesta trovata viene considerata un bundle. Se il modulo viene eseguito senza trovare bundle, lo scenario termina dopo il primo modulo.

Se il primo modulo restituisce un bundle, il bundle passa attraverso il resto dello scenario. In questo esempio, il bundle passerebbe al secondo modulo, che converte la richiesta in un progetto.

![Flusso di esecuzione dello scenario Workfront](assets/example-execution-flow-wf-only.png)

>[!ENDSHADEBOX]

### Esempio: [!UICONTROL Workfront Fusion per l&#39;automazione e l&#39;integrazione del lavoro]

>[!BEGINSHADEBOX]

**Esempio:** In questo scenario che scarica documenti da Adobe Workfront e li invia a una cartella in [!DNL Dropbox], i dati scorrono come segue:

Il primo passaggio dello scenario, eseguito dal primo modulo, consiste nel controllare i documenti in Workfront. Ogni documento trovato viene considerato un unico bundle. Se il modulo viene eseguito senza trovare bundle, lo scenario termina dopo il primo modulo.

Se viene restituito un bundle, questo passa attraverso il resto dello scenario. In questo esempio, il resto dello scenario è costituito dal modulo secondario, che carica il bundle nella cartella [!DNL Dropbox].

![Flusso di esecuzione dello scenario di integrazione](assets/example-execution-flow-wf-dropbox.png)

Se il primo modulo restituisce più bundle, il primo viene caricato in [!DNL Dropbox] prima del secondo. Poi viene caricato il secondo bundle, poi il terzo e così via.

>[!ENDSHADEBOX]

## Informazioni sui bundle elaborati

Per ogni modulo, il bundle passa attraverso un processo in 4 fasi prima di passare al modulo successivo o di raggiungere la sua destinazione finale.

* Inizializzazione
* Operazione
* Commit/Rollback
* Finalizzazione

>[!NOTE]
>
>Anche lo scenario più ampio è sottoposto a questo processo. Per informazioni sul processo a livello di scenario, vedere [Esecuzione, cicli e fasi dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Al termine dell’esecuzione di uno scenario, ogni modulo visualizza un’icona che mostra il numero di operazioni eseguite. Puoi fare clic su questa icona per visualizzare informazioni dettagliate sui bundle elaborati per ogni passaggio del processo. Puoi vedere quali impostazioni del modulo sono state utilizzate e quali bundle sono stati restituiti da ciascun modulo.

![Bundle elaborati](assets/Info-processed-bundles.png)

In questo esempio, il modulo ha ricevuto informazioni di input quali:

* ID del problema rilevato
* Oggetto in cui verrà convertito il problema (Progetto)
* ID del modello che verrà utilizzato per creare il progetto
* Tipo di record dell&#39;oggetto trovato (OPTASK, che è un problema)

Dopo l’elaborazione, il modulo ha restituito le seguenti informazioni di output:

* ID del progetto appena creato.

Se il modulo ha rilevato più di un problema, le informazioni vengono acquisite separatamente per ciascun bundle. Ci sarebbe un&#39;area Operazione 2 con sezioni di input e output che descrivono il secondo bundle, e così via.

## Errori durante l’esecuzione di uno scenario

Durante l’esecuzione dello scenario potrebbe verificarsi un errore. Ad esempio, se hai eliminato il modello che verrà utilizzato dal modulo per creare il nuovo progetto, lo scenario termina con un messaggio di errore. Per ulteriori informazioni sulla gestione degli errori, vedere [Tipi di errore](/help/workfront-fusion/references/errors/error-processing.md).

## Risorse

* Per ulteriori informazioni sulla configurazione di uno scenario, vedere [Editor scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).
* Per ulteriori informazioni sulla pagina dei dettagli dello scenario, vedere [Dettagli dello scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md).
* Per ulteriori informazioni sull&#39;attivazione di uno scenario, vedere [Attivare o disattivare uno scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).
* Per ulteriori informazioni sulla pianificazione di uno scenario, vedere [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* Per ulteriori informazioni sui moduli, vedere [Panoramica del modulo](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).
