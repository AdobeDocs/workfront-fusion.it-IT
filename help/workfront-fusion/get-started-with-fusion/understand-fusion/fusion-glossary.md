---
title: Glossario di Adobe Workfront Fusion
description: Il glossario seguente illustra alcuni termini comuni di Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7f098ec2-8594-4e5d-9ce7-d1738a05f9a6
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# Glossario di Adobe Workfront Fusion

Il glossario seguente illustra alcuni termini comuni di Adobe Workfront Fusion.


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Azione</p> </td> 
   <td>Modulo che consente di eseguire un’azione, ad esempio leggere o scrivere dati da o in un’app o un servizio selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Aggregator</p> </td> 
   <td> <p>Tipo di modulo che unisce più bundle (più raccolte di dati) in un singolo bundle. </p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">Modulo aggregatore</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>Le interfacce API (Application Programming Interface) consentono alle applicazioni e ai servizi di comunicare tra loro. Fusion utilizza le API per comunicare con l’applicazione a cui ti stai connettendo. Ogni applicazione ha un’API separata. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chiave API</td> 
   <td>Codice univoco che identifica l'utente, lo sviluppatore o il programma che chiama l'API di un software, utilizzato per l'autenticazione. Poiché i moduli Fusion funzionano tramite la connessione delle API, a volte sono necessarie le chiavi API. Le chiavi API sono distribuite dall’app che le richiede. Ad esempio, se hai bisogno di una chiave API per collegare Fusion ad Adobe Lightroom, puoi richiederla tramite il tuo account Adobe Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">App o servizio</td> 
   <td> <p>Applicazione software. Fusion è in grado di connettersi alla maggior parte delle applicazioni, anche se non dispone di un connettore dedicato per tale applicazione.</p> <p>Un’app può anche essere una funzione speciale che manipola i dati, ad esempio un iteratore o un aggregatore. </p> <p>Un servizio è un’origine di dati che può includere un’API web, una pagina web, diversi tipi di server (FTP, SMTP, IMAP) e così via. </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Bundle</p> </td> 
   <td> <p>Un bundle è un’unità di base di dati restituita o ricevuta dai moduli. Ad esempio, un modulo di ricerca che restituisce tre record genera tre bundle di dati, uno per ogni record. Un bundle è costituito da elementi.</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>Connessione</p> </td> 
   <td> <p>Una connessione rappresenta un insieme di credenziali per la connessione a un determinato servizio. Puoi configurare le connessioni all’interno di qualsiasi modulo e quindi utilizzare tale connessione in qualsiasi altro modulo. Ogni modulo deve avere una connessione selezionata, in modo che Fusion possa utilizzare tali credenziali per accedere alle informazioni richieste dal modulo. </p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md" class="MCXref xref">Panoramica della connessione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connettore</td> 
   <td>Un connettore è il set di moduli per una determinata applicazione. Workfront Fusion offre connettori per molte applicazioni di lavoro comuni, come Workfront, Salesforce e Jira.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ciclo</p> </td> 
   <td> <p>Un ciclo è costituito da due fasi dell'esecuzione dello scenario: operazione e commit. Lo scenario può essere costituito da uno o più cicli. Per informazioni più dettagliate, vedere <a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">Esecuzione dello scenario, cicli e fasi</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Archivio dati</p> </td> 
   <td> <p>Un archivio dati memorizza i dati provenienti da scenari o consente di trasferire i dati tra singoli scenari o esecuzioni di scenari. </p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/map-data/data-stores.md" class="MCXref xref">Archivi dati</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Filtro</p> </td> 
   <td> <p> Un filtro può essere applicato tra due moduli e consente di lavorare solo con bundle che soddisfano determinati criteri. È possibile applicare diversi filtri. </p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md" class="MCXref xref">Aggiungere un filtro a uno scenario</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>Nome utilizzato per identificare in modo univoco un bundle. Un ID viene in genere utilizzato per distinguere un bundle da aggiornare o eliminare da un determinato servizio. Gli ID possono essere mappati dall’output di un modulo precedente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Voci</p> </td> 
   <td> <p>Parte di un bundle. I bundle possono essere costituiti da più elementi. Esistono diversi tipi di elementi: testo, numero, booleano (sì/no), data, ora, buffer (dati binari), raccolte, menu di selezione, array e convalida.</p><p> Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipi di dati elemento</a>.</p> </td> 
  </tr>
  <tr> 
   <td role="rowheader"> <p>Iteratore</p> </td> 
   <td> <p>Tipo di modulo che consente di prendere un bundle di dati (una raccolta di dati) e dividerlo in bundle separati. Questi bundle possono quindi essere elaborati singolarmente dai moduli successivi. </p><p>Per ulteriori informazioni, vedere il modulo <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Modulo</p> </td> 
   <td> <p>Un singolo passaggio all’interno di uno scenario che esegue una funzione, ad esempio la creazione di un record, nell’app o nel servizio associato.</p> <p>Ogni app o servizio dispone di vari moduli che definiscono il modo in cui risponde a una richiesta.</p>  <p> <img src="assets/module.png"> </p> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Panoramica del modulo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Operazione</p> </td> 
   <td> <p>Un’attività eseguita da un modulo, ad esempio il recupero di un record o il caricamento di un file.</p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md" class="MCXref xref">Operazioni</a>.</p>
  </tr> 
  <tr> 
   <td role="rowheader">Chiavi pubbliche/private</td> 
   <td>Le chiavi pubbliche e private vengono utilizzate per crittografare e decrittografare i dati. La chiave pubblica può essere distribuita e chiunque disponga della chiave pubblica può crittografare i dati, ma solo la chiave privata può decrittografarli. Analogamente, un utente con una chiave privata può crittografare i dati che chiunque abbia la chiave pubblica può decrittografare. La crittografia della chiave privata garantisce che i dati provengano dal proprietario della chiave privata e funge da convalida dell'origine dei dati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Router</p> </td> 
   <td>Un router consente di duplicare i dati o aggiungere nuove route a uno scenario, in modo da instradare nuovamente i dati e gestire separatamente diversi gruppi di dati.</p><p> Per ulteriori informazioni, vedere il modulo <a href="/help/workfront-fusion/create-scenarios/add-modules/router-module.md" class="MCXref xref">[!UICONTROL Router]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Scenario</p> </td> 
   <td> <p>Una serie di passaggi automatizzati creati dall’utente, ciascuno rappresentato ed eseguito da un modulo. Lo scopo di uno scenario è quello di spostare e manipolare i dati.</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <p> Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md" class="MCXref xref">Panoramica dello scenario</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Segmento scenario</p> </td> 
   <td> <p> Un segmento di scenario è una sezione di uno scenario costituita da una serie di moduli che si connettono tutti alla stessa applicazione. I segmenti di scenario spesso rappresentano un breve flusso di lavoro nell’applicazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Trigger</p> </td> 
   <td> <p>Un trigger è un tipo di modulo che controlla i dati nuovi e aggiornati e avvia lo scenario quando si applicano determinate condizioni configurate nel modulo. Gli attivatori possono essere configurati per avviare uno scenario secondo una pianificazione (polling) o ogni volta che si verificano modifiche ai dati (trigger istantaneo o webhook).</p> <p>Per ulteriori informazioni, vedi <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Triggers</a> nell'articolo Panoramica del modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>Tipo speciale di trigger che consente di eseguire uno scenario immediatamente dopo la disponibilità di un nuovo bundle. </p><p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Trigger istantanei (webhook)</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
