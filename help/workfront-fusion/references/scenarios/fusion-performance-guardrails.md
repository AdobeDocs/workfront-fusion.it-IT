---
title: Guardrail delle prestazioni di fusione
description: L'automazione del lavoro richiede un'elaborazione rapida, quindi  [!DNL Adobe Workfront Fusion]  è progettato per prestazioni elevate. Poiché gli scenari con tempi di esecuzione lunghi possono rallentare il ritmo del tuo lavoro, abbiamo progettato [!DNL Workfront Fusion] con guardrail per il mantenimento delle prestazioni che limitano il tempo di esecuzione, la dimensione dei dati e altri parametri dello scenario. [!DNL Workfront Fusion] i designer devono essere a conoscenza di questi guardrail e incorporarli nelle loro procedure di progettazione.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: f2ddf62d660c4709f1e7e59c4302cde5b062725f
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 0%

---

# Guardrail delle prestazioni di fusione

L&#39;automazione del lavoro richiede una rapida elaborazione, quindi [!DNL Adobe Workfront Fusion] è progettato per prestazioni elevate. Poiché gli scenari con tempi di esecuzione lunghi possono rallentare il ritmo del tuo lavoro, abbiamo progettato [!DNL Workfront Fusion] con guardrail per il mantenimento delle prestazioni che limitano il tempo di esecuzione, la dimensione dei dati e altri parametri dello scenario. I designer di [!DNL Workfront Fusion] devono essere a conoscenza di questi guardrail e incorporarli nelle loro procedure di progettazione.

## Browser

* Workfront Fusion supporta solo browser basati su Chrome.

## Scenari

* Il timeout predefinito per l&#39;esecuzione dello scenario è **40 minuti**. Quando l&#39;esecuzione raggiunge questo timeout, [!DNL Workfront Fusion] interrompe l&#39;esecuzione dello scenario dopo il ciclo o l&#39;operazione successiva, a seconda dello scenario. Questo costringe lo scenario a interrompersi poco dopo il raggiungimento del limite di 40 minuti

  Gli scenari di concatenamento non vengono considerati per il timeout di esecuzione dello scenario. Uno scenario padre non accumula tempo durante l’attesa dell’esecuzione di uno scenario figlio.
* La dimensione massima di una blueprint dello scenario è **5 MB**, ma è consigliabile mantenere la dimensione dello scenario sotto **3 MB**.

  I moduli di app che creano o aggiornano dati con un numero elevato di campi possono causare blueprint molto grandi.

   * Quando utilizzi l&#39;app [!DNL Workfront], assicurati di selezionare solo i campi necessari per i casi d&#39;uso relativi alla creazione o all&#39;aggiornamento.
   * Quando utilizzi altre app, utilizza moduli API personalizzati per interagire con qualsiasi tipo di record con un numero elevato di campi.

* Anche se non esiste un limite per il numero di moduli in uno scenario, gli scenari con più di 150 moduli influiscono negativamente sulle prestazioni del sistema [!DNL Workfront Fusion]. Per questo motivo, si sconsiglia di creare scenari con oltre 150 moduli.

## Operazioni

* Il timeout predefinito dell&#39;operazione è in genere di **40 secondi**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## File

* La capacità di elaborazione totale di Fusion per i file è **1 GB**. Il limite si basa sul costo totale della memoria. Ogni operazione contribuisce a tale costo. Se viene scaricato e caricato un singolo file di 400 MB, il costo totale per la capacità del file sarebbe di 800 MB.
* Le organizzazioni che aderiscono al piano Workfront Ultimate hanno accesso a una maggiore capacità di elaborazione dei file superiore a 1 GB. La piattaforma Fusion può supportare singoli file fino a 15 GB per una singola azione (ad esempio, caricamento di file), ma ci sono altri fattori che influiscono sul trasferimento dei dati. Il limite di dimensione file per una singola azione dipende dal servizio web a cui Fusion si connette. Il trasferimento di dati è l’elaborazione totale per una singola esecuzione. Ciò significa che più azioni in una singola esecuzione contribuiscono al trasferimento totale dei dati. Fusion elaborerà i file fino al raggiungimento del limite di esecuzione di 40 minuti.

Per ulteriori informazioni, vedere [Utilizzo di file di grandi dimensioni](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Utilizzo memoria server

* L&#39;utilizzo della memoria del server per una singola esecuzione è limitato a **1 GB**.

  Molti fattori, ad esempio file di grandi dimensioni o moduli complessi, possono influire sull&#39;utilizzo della memoria del server in modi difficili da prevedere o controllare. Per questo motivo, l’esecuzione dello scenario potrebbe superare il limite di 1 GB di memoria, anche se lo scenario segue tutti gli altri guardrail delle prestazioni. Se si supera il limite di memoria, l’esecuzione non riesce.

## Webhook

* La dimensione massima predefinita di un payload è **5 MB**.
* I webhook sono limitati a **100 richieste al secondo**. Al raggiungimento di questo limite, Workfront Fusion invia uno stato 429 ([!UICONTROL Troppe richieste]).
* [!DNL Workfront Fusion] memorizza i payload del webhook per 30 giorni. L&#39;accesso a un payload del webhook dopo più di 30 giorni dalla ricezione genera l&#39;errore &quot;[!UICONTROL Impossibile leggere il file dall&#39;archivio.]&quot;
* I webhook vengono disattivati automaticamente se si applica una delle seguenti condizioni:

   * Il webhook non è stato connesso ad alcuno scenario per più di 5 giorni
   * Il webhook viene utilizzato solo in scenari inattivi, che sono stati inattivi per più di 30 giorni.

* I webhook disattivati vengono eliminati e annullati automaticamente se non sono connessi ad alcun scenario e se sono in stato disattivato da oltre 30 giorni.

## Cronologia di esecuzione

* I registri della cronologia di esecuzione sono limitati a **100 MB**. Se la cronologia di esecuzione supera queste dimensioni, verranno visualizzati solo i primi 100 MB.
* Se uno scenario ha più esecuzioni simultanee. nell’area Esecuzioni della pagina dei dettagli dello scenario vengono visualizzate solo 5 esecuzioni. Questo vale anche quando sono in esecuzione più di 5 esecuzioni.

## Esecuzioni incomplete

* Le esecuzioni incomplete sono limitate a una dimensione totale di *10 MB** per scenario. Se viene raggiunto il limite di 10 MB, per tale scenario non verranno memorizzate altre esecuzioni incomplete.
* Le esecuzioni incomplete sono limitate a un totale di **500 MB** per team. Se viene raggiunto il limite di 500 MB, non verranno memorizzate altre esecuzioni incomplete per tale team.

## Nuovi tentativi

* Quando si utilizza il modulo Interrompi e si specifica la direttiva Riprova, se uno scenario si interrompe consecutivamente 10 volte in un arco temporale di 2 minuti, viene disattivato automaticamente.

## Ricorsione

La ricorsione si verifica quando uno scenario attiva una nuova esecuzione di se stesso, che attiva una nuova esecuzione e così via in un ciclo infinito.

Ad esempio, uno scenario viene attivato quando viene creata un&#39;attività e tale scenario crea due attività. Le nuove attività create attivano entrambe di nuovo lo scenario, che crea quattro nuove attività. Ogni volta che viene creata un&#39;attività, lo scenario viene attivato e ogni volta che lo scenario viene eseguito, il numero di attività raddoppia. Il numero di attività aumenta in modo esponenziale.

La ricorsione può causare problemi di prestazioni sia per l’organizzazione proprietaria dello scenario ricorsivo che per altre organizzazioni.

Per quanto riguarda la ricorsione, considera quanto segue:

* **Quando uno scenario provoca la ricorsione, viene disattivato dal team di progettazione di Fusion per evitare ulteriori problemi di prestazioni.**
* Poiché la ricorsione è il risultato della progettazione dello scenario, è necessario progettare gli scenari in modo tale che lo scenario non includa azioni che attivino lo scenario.

## TLS

* Per impostazione predefinita, Fusion supporta attualmente la versione 1.2 di TLS.
* Fusion può utilizzare TLS 1.3 per le richieste HTTPS in uscita se TLS 1.3 è abilitato per il servizio di destinazione.
* Fusion supporta sia TLS 1.2 che TLS 1.3 per le richieste HTTPS in ingresso ai webhook.
* Le organizzazioni possono richiedere che TLS versione 1.3 sia abilitato per la propria istanza di Fusion.

>[!NOTE]
>
> Se ti connetti a Workfront, tieni presente che questa funzionalità TLS è abilitata in Workfront per le chiamate a domini con formato `https://<domain>.my.workfront.com`.
