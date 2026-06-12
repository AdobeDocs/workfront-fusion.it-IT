---
title: Guardrail delle prestazioni di Fusion
description: Poiché l’automazione del lavoro richiede un’elaborazione rapida, Workfront Fusion è progettato per prestazioni elevate. Gli scenari con esecuzioni prolungate possono rallentare il ritmo del tuo lavoro; pertanto Workfront Fusion è stato progettato con guardrail per il mantenimento delle prestazioni che limitano il tempo di esecuzione, le dimensioni dei dati e altri parametri dello scenario. Chi progetta gli scenari in Workfront Fusion deve essere consapevole di questi guardrail e incorporarli nelle attività di progettazione.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
TQID: https://experienceleague.adobe.com/TARMza99lJaSq6kUUr3xxMf0ExtoQBNk6L-KzzEEL8U
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: c9c182d6c6acc34295970f9138067a6cb6c2ba2a
workflow-type: tm+mt
source-wordcount: 1360
ht-degree: 76%

---

# Guardrail delle prestazioni di Fusion

Poiché l’automazione del lavoro richiede un’elaborazione rapida, Workfront Fusion è progettato per prestazioni elevate. Gli scenari con esecuzioni prolungate possono rallentare il ritmo del tuo lavoro; pertanto Workfront Fusion è stato progettato con guardrail per il mantenimento delle prestazioni che limitano il tempo di esecuzione, le dimensioni dei dati e altri parametri dello scenario. Chi progetta gli scenari in Workfront Fusion deve essere consapevole di questi guardrail e incorporarli nelle attività di progettazione.

## Browser

* Workfront Fusion supporta solo browser basati su Chrome.

## Scenari

* Il timeout predefinito per l’esecuzione di uno scenario è di **40 minuti**. Quando il tempo di esecuzione raggiunge questo timeout, Workfront Fusion interrompe l’esecuzione dello scenario dopo il ciclo o l’operazione successiva, a seconda dello scenario. Di conseguenza lo scenario si interrompe poco dopo il raggiungimento del limite di 40 minuti

  La concatenazione di scenari non viene considerata per il timeout di esecuzione dello scenario. Uno scenario principale non accumula tempo durante l’attesa dell’esecuzione di uno scenario secondario.

  >[!IMPORTANT]
  >
  > Anche se il concatenamento consente ai flussi di lavoro di durare oltre 40 minuti, deve essere trattato come un segnale di rischio di progettazione, non come una soluzione alternativa supportata. Gli scenari principali che si estendono su più scenari figlio a lunga durata non hanno un limite di timeout complessivo. Se uno scenario figlio si blocca o riscontra un problema di piattaforma, l’elemento padre attende indefinitamente senza errori e senza ripristino automatico.
  >
  > Se la progettazione dello scenario richiede il concatenamento per evitare il limite di 40 minuti, controlla l’architettura prima di implementare in produzione. Consulta [Incatenare più scenari](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios) per indicazioni sulla progettazione.
* La dimensione massima della blueprint di uno scenario è di **5 MB**, ma ti consigliamo di mantenere la dimensione dello scenario al di sotto di **3 MB**.

  I moduli di app che creano o aggiornano dati con un numero elevato di campi possono determinare blueprint molto grandi.

   * Quando utilizzi l’app Workfront, accertati di selezionare solo i campi necessari per i casi d’uso relativi alla creazione o all’aggiornamento.
   * Quando lavori con altre app, utilizza moduli API personalizzati per interagire con i tipi di record con un numero elevato di campi.

* Anche se non esiste un limite per il numero di moduli in uno scenario, gli scenari con più di 150 moduli limitano le prestazioni del sistema Workfront Fusion. Per questo motivo non è consigliato creare scenari con più di 150 moduli.
* I nomi degli scenari non possono contenere più di 120 caratteri.

## Scenari concatenati

* La funzionalità di concatenamento degli scenari è disponibile in Beta e non è consigliata per i flussi di lavoro mission-critical. In quanto funzione di Beta, il comportamento può cambiare e i casi limite potrebbero non essere gestiti completamente.

  Per integrazioni stabili, puoi attivare un secondo scenario tramite webhook utilizzando un modulo di richiesta HTTP. Questo modello utilizza primitive completamente supportate e fornisce a ogni scenario un controllo di esecuzione indipendente.

  Se scegli di utilizzare scenari concatenati, controlla le linee guida di progettazione e i vincoli nell&#39;articolo [Catena più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

## Operazioni

* Il timeout predefinito per un’operazione è in genere di **40 secondi**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## File

* La capacità di elaborazione totale di Fusion per i file è di **1 GB**. Il limite si basa sul costo totale in termini di memoria. Ogni operazione contribuisce a tale costo. Se viene scaricato e quindi ricaricato un singolo file di 400 MB, il costo totale in termini di capacità di file sarà di 800 MB.
* Le organizzazioni con il piano Workfront Ultimate dispongono di una capacità di elaborazione file superiore a 1 GB. Tuttavia esistono altri fattori che influiscono sul trasferimento dei dati. Il servizio a cui si connette Fusion può limitare le dimensioni dei file, con conseguenze sui file elaborati da tale servizio. Inoltre, i file di grandi dimensioni possono influire sul tempo di esecuzione dello scenario. Fusion elaborerà i file fino al raggiungimento del limite del tempo di esecuzione di 40 minuti, dopodiché l’esecuzione verrà interrotta.
* Se un file viene scaricato utilizzando un modulo che supporta i file di grandi dimensioni e quindi trasferito a un modulo che non supporta tali file, il modulo di destinazione non elabora correttamente il file. I file di grandi dimensioni devono essere gestiti esclusivamente con moduli che supportano tali file nell’intero flusso di lavoro.
* I moduli che non supportano file di grandi dimensioni possono elaborare file con dimensioni massime di **200 MB**.

Per ulteriori informazioni, consulta [Utilizzare file di grandi dimensioni](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Utilizzo della memoria del server

* L’utilizzo della memoria del server per una singola esecuzione è limitato a **1 GB**.

  Molti fattori, ad esempio file di grandi dimensioni o moduli complessi, possono influire sull’utilizzo della memoria del server in modi difficili da prevedere o controllare. Per questo motivo, l’esecuzione del tuo scenario può superare il limite di memoria di 1 GB anche se lo scenario è conforme a tutti gli altri guardrail sulle prestazioni. Se il limite di memoria viene superato, l’esecuzione non riesce.

## Webhook

* La dimensione massima predefinita di un payload è di **5 MB**.
* I webhook sono limitati a **100 richieste al secondo**. Al raggiungimento di questo limite, Workfront Fusion restituisce uno stato 429 ([!UICONTROL Troppe richieste]).
* Workfront Fusion archivia i payload dei webhook per 30 giorni. L’accesso a un payload del webhook dopo più di 30 giorni dalla ricezione genera un errore di tipo “[!UICONTROL Impossibile leggere il file dall’archivio.]”
* I webhook vengono disattivati automaticamente se è una delle seguenti condizioni è vera:

   * Il webhook non è stato collegato a nessuno scenario da più di 5 giorni
   * Il webhook viene utilizzato solo in scenari che rimangono inattivi per più di 30 giorni.

* I webhook disattivati vengono eliminati e ne viene automaticamente annullata la registrazione se non connessi ad alcun scenario e se in stato di disattivazione da oltre 30 giorni.
* Il timeout per una risposta del webhook è di 5 minuti.

## Cronologia di esecuzione

* I registri della cronologia di esecuzione sono limitati a **100 MB**. Se la cronologia di esecuzione supera queste dimensioni, verranno visualizzati solo i primi 100 MB.
* Se l&#39;input o l&#39;output di una singola operazione supera i 15 MB, non viene visualizzato nella cronologia di esecuzione.
* Se uno scenario presenta più esecuzioni simultanee, nell’area Esecuzioni della pagina dei dettagli dello scenario vengono visualizzate solo 5 esecuzioni. Questo vale anche quando sono in esecuzione più di 5 esecuzioni.
* Se uno scenario fa parte di una rete concatenata, la cronologia di esecuzione viene mantenuta separatamente per ogni scenario della catena. Non esiste una visualizzazione di traccia unificata tra scenari padre e figlio. Per analizzare un’esecuzione a catena, apri singolarmente la cronologia di esecuzione di ogni scenario.
* Se l&#39;input o l&#39;output di una singola operazione supera i 15 MB, non viene visualizzato nella cronologia di esecuzione. Questo limite si applica ai dati trasmessi tra scenari padre e figlio tramite moduli a catena.

## Esecuzioni incomplete

* Le esecuzioni incomplete sono limitate a una dimensione totale di **1 GB** o **100 esecuzioni incomplete** per scenario, a seconda del limite raggiunto per primo. Se viene raggiunto un limite, per tale scenario non verranno memorizzate altre esecuzioni incomplete.

## Nuovi tentativi

* Quando viene utilizzato il modulo Break specificando la direttiva Retry, se uno scenario non riesce consecutivamente 10 volte in un arco temporale di 2 minuti, viene disattivato automaticamente.

## Ricorsione

La ricorsione si verifica quando uno scenario attiva una nuova esecuzione di se stesso, attivando una nuova esecuzione e così via in un ciclo infinito.

Ad esempio, uno scenario viene attivato quando viene creata un’attività e tale scenario crea due attività. Le attività appena create attivano nuovamente lo scenario, creando quattro nuove attività. Ogni volta che viene creata un’attività, lo scenario viene attivato e ogni volta che lo scenario viene eseguito, il numero di attività raddoppia. Il numero di attività aumenta in modo esponenziale.

La ricorsione può causare problemi di prestazioni sia per l’organizzazione proprietaria dello scenario ricorsivo che per altre organizzazioni.

Per quanto riguarda la ricorsione, prendi in considerazione quanto segue:

* **Quando uno scenario sta causando la ricorsione, viene disattivato dal team di progettazione di Fusion per evitare ulteriori problemi di prestazioni.**
* Poiché la ricorsione è il risultato della progettazione dello scenario, è necessario progettare gli scenari in modo tale che lo scenario non includa azioni che lo attivino.

## TLS

* Per impostazione predefinita, Fusion supporta attualmente la versione 1.2 di TLS.
* Fusion può utilizzare TLS 1.3 per le richieste HTTPS in uscita se TLS 1.3 è abilitato per il servizio di destinazione.
* Fusion supporta sia TLS 1.2 che TLS 1.3 per le richieste HTTPS in entrata ai webhook.
* Le organizzazioni possono richiedere che TLS versione 1.3 sia abilitato per la propria istanza di Fusion.

>[!NOTE]
>
> Se ti connetti a Workfront, tieni presente che questa funzionalità TLS è abilitata in Workfront per le chiamate a domini che hanno il formato `https://<domain>.my.workfront.com`.
