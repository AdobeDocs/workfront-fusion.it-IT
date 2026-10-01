---
title: Strumenti server Adobe Workfront Fusion MCP
description: Elenco di riferimento degli strumenti esposti dal server MCP di Adobe Workfront Fusion alle piattaforme AI e a Coworker.
source-git-commit: 322a34df48a5218bc045e6cac6a5a8b3837e8c2e
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 7%
---

# Strumenti server Adobe Workfront Fusion MCP


In questo articolo sono elencati gli strumenti che il server MCP di Adobe Workfront Fusion espone a un agente di IA connesso. L’agente chiama questi strumenti per tuo conto quando gli chiedi di trovare, ispezionare, creare, eseguire, aggiornare o eliminare elementi di Fusion.

Gli stessi strumenti sono disponibili in ogni superficie supportata: connessioni MCP personalizzate in Claude, ChatGPT, Copilot o il tuo agente; e Coworker, sia standalone che nella barra a destra di Fusion. Per la configurazione, vedere [Configurare il server MCP di Adobe Workfront Fusion](configure-fusion-mcp-server.md).

L’agente agisce in Fusion utilizzando il tuo Adobe ID, il tuo ruolo organizzazione Fusion e i tuoi ruoli team. Uno strumento funziona solo se disponi dell’autorizzazione corrispondente in Fusion. Adobe non è responsabile delle modifiche apportate dall’agente ai dati di Fusion.

## Azioni di lettura e scrittura

Ogni strumento è classificato come:

* **Lettura**: recupera le informazioni senza modificare nulla, ad esempio elencando scenari o ottenendo un&#39;esecuzione.
* **Scrittura**: crea, modifica, esegue o elimina dati di Fusion, ad esempio clonando uno scenario o cancellando una coda del webhook.

## Strumenti di organizzazione

L&#39;organizzazione attiva viene applicata a tutti gli altri strumenti della sessione corrente.

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elenca organizzazioni | `fusion_orgs_list` | Leggi | Elenca le organizzazioni di Fusion a cui è possibile accedere, con ID, regione (zona) ed etichetta. |
| Imposta organizzazione attiva | `fusion_orgs_set` | Session | Cambia l&#39;organizzazione attiva per la sessione corrente. Non modifica i dati di Fusion. |

## Strumenti scenario

### Scenari

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare scenari | `fusion_scenarios_list` | Leggi | Elenca gli scenari dell’organizzazione. |
| Ottieni scenario | `fusion_scenarios_get` | Leggi | Restituisce uno scenario, inclusa la sua blueprint completa. |
| Ottieni dipendenze scenario | `fusion_scenarios_getDependencies` | Leggi | Restituisce connessioni, chiavi, archivi dati, strutture di dati e webhook dei riferimenti blueprint dello scenario. |
| Trova scenari dipendenti | `fusion_scenarios_dependents` | Leggi | Trova scenari che fanno riferimento a un determinato webhook, archivio dati, struttura dati, connessione, chiave o scenario. Utile per l’analisi di impatto prima di modificare o eliminare una risorsa. |
| Convalida blueprint | `fusion_scenarios_validate_blueprint` | Leggi | Convalida strutturalmente una blueprint rispetto a un team (riferimenti ai moduli, connessioni, campi obbligatori) senza salvare nulla. |
| Crea scenario | `fusion_scenarios_create` | Scrittura | Crea uno scenario in un team da una blueprint, con nome, descrizione, cartella, pianificazione ed elaborazione sequenziale facoltativi. |
| Scenario clone | `fusion_scenarios_clone` | Scrittura | Clona uno scenario nello stesso team o in un team diverso. Quando si esegue la clonazione tra team, ogni connessione, webhook, archivio dati, struttura dati e chiave viene mappata a una risorsa target. Facoltativamente continua dall’ultimo record elaborato. |
| Aggiorna scenario | `fusion_scenarios_update` | Scrittura | Modifica il nome, la descrizione, la cartella, la pianificazione o lo stato attivo (attiva/disattiva). Può anche ripristinare uno scenario eliminato. |
| Esegui lo scenario una volta | `fusion_scenarios_execute` | Scrittura | Esegue uno scenario una volta e attende (fino a un timeout) il risultato, restituendo lo stato ed eventuali messaggi di errore. Non supportato per scenari istantanei (attivati dal webhook). |
| Elimina scenario | `fusion_scenarios_delete` | Scrittura | Elimina uno scenario. Gli scenari eliminati possono essere ripristinati con **Aggiorna scenario**. |

Esempio di prompt:

* _Quali scenari attivi nel team Marketing non sono stati modificati in 6 mesi?_
* _Quali connessioni utilizza lo scenario &quot;Salesforce → Workfront sync&quot;?_
* _Clona &quot;Assunzione lead&quot; nel team vendite e sostituisci nella connessione Salesforce vendite._
* _Convalida questo blueprint prima di importarlo._
* _Esegui il report notturno e indica se ha esito positivo._

### Versioni scenario

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elenca versioni scenario | `fusion_scenario_versions_list` | Leggi | Elenca le versioni salvate di uno scenario. Filtra per `version`, `createdAt`, `comment`. |
| Ottieni versione scenario | `fusion_scenario_versions_get` | Leggi | Restituisce il blueprint e i metadati per una versione specifica. |

Esempio di prompt:

* _Che cosa è cambiato tra la versione 12 e la versione 14 di questo scenario?_

### Cartelle

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare le cartelle | `fusion_folders_list` | Leggi | Elenca le cartelle di scenario, con i conteggi degli scenari. |
| Crea cartella | `fusion_folders_create` | Scrittura | Crea una cartella in un team. |
| Rinomina cartella | `fusion_folders_update` | Scrittura | Rinomina una cartella. |
| Elimina cartella | `fusion_folders_delete` | Scrittura | Elimina una cartella. |

## Strumenti di esecuzione

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare esecuzioni | `fusion_executions_list` | Leggi | Elenca le esecuzioni per uno scenario o per un’esecuzione incompleta. Filtra per `status` (ad esempio `status==3` per gli errori, `status==2` per gli avvisi), `timestamp`, `duration`, `bundles`, `operations`, `transfer`. Facoltativamente include esecuzioni di controllo. |
| Ottieni esecuzione | `fusion_executions_get` | Leggi | Restituisce una singola esecuzione e metadati relativi allo scenario o all’esecuzione incompleta. |

Esempio di prompt:

* _Mostra esecuzioni non riuscite di &quot;Sincronizzazione fatture&quot; da ieri e riepiloga gli errori._
* _Quale esecuzione di questo scenario ha utilizzato il maggior numero di operazioni questa settimana?_

## Strumenti per operazioni (utilizzo)

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Ottieni operazioni | `fusion_operations_get` | Leggi | Restituisce una serie temporale di operazioni (per giorno o mese) per un intervallo di date fino a 1 anno. Filtra per team, scenario o pacchetto; raggruppa per modulo, pacchetto, scenario o team. |
| Ottieni riepilogo operazioni | `fusion_operations_summary_by_org` | Leggi | Restituisce il totale delle operazioni per scenario e team per un intervallo di date, più il totale complessivo. |

Esempio di prompt:

* _Primi 10 scenari per operazioni del mese scorso._
* _Quante operazioni ha utilizzato l&#39;app Salesforce nel terzo trimestre?_

## Strumenti di connessione e chiave

Questi strumenti restituiscono solo i metadati. Non restituiscono credenziali, token o valori segreti.

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Cerca connessioni | `fusion_connections_search` | Leggi | Elenca le connessioni. Filtra per `name`, `accountName`, `accountType`, `expire`, `teamId`, `scopesCount`, `editable`, `environmentType`, `authenticationType`. |
| Ottieni connessione | `fusion_connections_get` | Leggi | Restituisce i dettagli di una singola connessione. |
| Cerca chiavi | `fusion_keys_search` | Leggi | Elenca le chiavi. Filtra per `name`, `typeName`, `teamId`. |
| Ottieni chiave | `fusion_keys_get` | Leggi | Restituisce i dettagli di una singola chiave. |

Esempio di prompt:

* _Quali connessioni scadono nei prossimi 30 giorni e quali scenari le utilizzano?_

## Strumenti webhook

### Webhook

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare webhook | `fusion_hooks_list` | Leggi | Elenca i webhook. Filtra per `name`, `teamId`, `type`, `enabled`, `gone`, `typeName`, `scenarioId`, `priority`, `detached` e altri. |
| Ottieni webhook | `fusion_hooks_get` | Leggi | Restituisce la configurazione di un webhook, l&#39;associazione del proprietario e i riferimenti esterni. |
| Trova webhook dipendenti | `fusion_hooks_dependents` | Leggi | Trova i webhook che fanno riferimento a una determinata connessione. |

### Coda webhook

| Strumento | Nome | Azione | Descrizione |
| --- | --- | -------- | --- |
| Ottieni statistiche coda | `fusion_queue_stats` | Leggi | Restituisce il numero di eventi in coda, il limite di coda e se il webhook è abilitato. |
| Coda elenco | `fusion_queue_list` | Leggi | Elenchi di eventi webhook ricevuti in attesa di elaborazione. |
| Ottieni elemento coda | `fusion_queue_get` | Leggi | Restituisce un singolo evento in coda, incluso il relativo payload decodificato. |
| Elimina elementi coda | `fusion_queue_delete` | Scrittura | Elimina eventi specifici in coda (fino a 50) o cancella la coda, escludendo facoltativamente alcuni eventi. Impossibile eliminare gli eventi in corso di elaborazione. |

Esempio di prompt:

* _È in corso il backup del webhook &quot;Invii modulo&quot;?_
* _Visualizza il payload dell&#39;evento in coda meno recente._

## Strumenti per l’archiviazione e la struttura dei dati

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare archivi dati | `fusion_datastores_list` | Leggi | Elenca gli archivi dati con numero di record, dimensioni e dimensioni massime. |
| Ottieni archivio dati | `fusion_datastores_get` | Leggi | Restituisce i metadati e l’utilizzo di un archivio dati, la struttura dei dati collegati e l’impostazione di convalida rigorosa. |
| Elenca i record dell’archivio dati | `fusion_data_list` | Leggi | Legge i record (chiave + dati JSON) da un archivio dati, con paging offset. |
| Trova archivi dati dipendenti | `fusion_datastores_dependents` | Leggi | Trova archivi di dati che utilizzano una determinata struttura di dati. |
| Cercare strutture di dati | `fusion_data_structures_search` | Leggi | Elenca le strutture di dati. Filtra per `name`, `strict`, `teamId`. |
| Ottieni struttura dati | `fusion_data_structures_get` | Leggi | Restituisce una struttura di dati, inclusa la specifica completa del campo. |

Esempio di prompt:

* _Quali archivi dati sono pieni per oltre l&#39;80%?_
* _Visualizza i primi 20 record nell&#39;archivio dati &quot;Mappa cliente&quot;._

## Strumenti di registro attività

| Strumento | Nome | Azione | Descrizione |
| --- | --- | --- | --- |
| Elencare i registri attività | `fusion_activity_logs_list` | Leggi | Elenca gli eventi di audit per l’organizzazione (chi ha fatto cosa, a quale entità, quando). Filtra per `entity` (ad esempio `scenario`, `connection`, `webhook`, `data store`, `user`), `action` (ad esempio `created`, `deleted`, `updated`, `transferred ownership`), utente, team e timestamp. |
| Esporta registri attività | `fusion_activity_logs_export` | Leggi | Esporta i registri attività come CSV o XLSX, utilizzando gli stessi filtri. |

Esempio di prompt:

* _Chi ha eliminato gli scenari negli ultimi 7 giorni?_
* _Esporta tutte le modifiche di connessione di questo trimestre in Excel._

## Collaboratore

Tutti gli strumenti in questo articolo sono disponibili in Collaboratore, sia singolarmente che nella barra a destra di Fusion, in base alle stesse impostazioni di lettura/scrittura e alle autorizzazioni dell’utente.

## Come vengono aggiornati gli strumenti

Quando Adobe rilascia una nuova versione del server Fusion MCP, gli agenti collegati raccolgono automaticamente il set di strumenti aggiornato. Non è necessario riconnettersi.

