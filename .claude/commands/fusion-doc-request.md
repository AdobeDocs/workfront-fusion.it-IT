---
name: fusion-doc-request
description: Gestire una richiesta di documentazione di Fusion dal modello Slack
source-git-commit: e354c51f13bd4f15172de068cac9720bd097eb8d
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# Richiesta documentazione Fusion

Gestisce il modello ricorrente &quot;Nuova richiesta documentazione da {person}&quot; pubblicato nel canale Slack `#fusion-documentation`: leggi la richiesta, aggiorna i documenti, quindi crea un&#39;attività di tracciamento sullo stesso modulo personalizzato Workfront utilizzato per ogni richiesta precedente di questo tipo.

Flusso di lavoro diverso dall&#39;abilità `fusion-release-notes`. Questa abilità aggiorna un articolo di riferimento e crea un’attività Workfront; non crea o aggiorna una pagina di note sulla versione di Fusion settimanale in questo archivio, anche se la richiesta dice &quot;Annuncio necessario: sì&quot;. Utilizzare `fusion-release-notes` solo se l&#39;utente richiede separatamente una nota di rilascio settimanale.

## Passaggio 1: ottenere i dettagli della richiesta

Se viene fornito un collegamento Slack, analizzare `channel_id` e `message_ts` dall&#39;URL e recuperare il thread (`slack_get_thread_replies` o `slack_read_thread`, a seconda dello strumento Slack MCP connesso. In caso di errore, provare entrambi). Mantieni il collegamento/URL permanente del thread, necessario nel passaggio 3.

Le connessioni Slack in questo ambiente sono incomplete (token scaduti, disconnette una sessione intermedia). Se un recupero non riesce:
- Riprova una volta.
- Se il recupero non riesce, informa chiaramente l’utente che non è riuscito e chiedi di incollare direttamente il contenuto della richiesta. Non indovinare il contenuto, e non arrenderti silenziosamente senza dirlo.

Il modello di richiesta include i campi seguenti: estrarre ciascuno:

* **Titolo funzionalità**
* **Descrizione**
* **Punti da aggiungere alla documentazione** *(talvolta presenti - sezioni/dettagli specifici richiesti dal richiedente; trattarli come obbligatori, non facoltativi, se forniti)*
* **Data di rilascio prevista**
* **Annuncio necessario** *(Sì/No - solo informativo; vedere la nota precedente. Non intervenire su questo campo.)*

Se la richiesta è collegata a una pagina wiki di Confluence con le specifiche complete, recuperarla (`get_wiki_content`) prima di scrivere la documentazione. Non fare affidamento solo sul riepilogo di Slack per i dettagli tecnici (nomi di campo esatti, passaggi, etichette dell’interfaccia utente) - richiamare quelli dalla specifica wiki quando ne viene collegata una.

## Passaggio 2: aggiornare la documentazione

Trova gli articoli esistenti rilevanti in questo archivio (grep per i nomi dei moduli, le etichette dell’interfaccia utente o i nomi delle impostazioni correlati, non indovinare il file). Aggiornali per riflettere la modifica, seguendo la struttura esistente dell’articolo, il livello di intestazione e lo stile della casa.

* Non inventare dettagli tecnici (nomi di campo esatti, ambiti di autorizzazione, passaggi di configurazione) che non sono presenti nella richiesta Slack o nelle specifiche wiki collegate. Se qualcosa non è confermato, contrassegnalo in linea come commento HTML (ad esempio `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) invece di indovinare - mai come callout visibile. Non deve essere riprodotto sulla pagina pubblicata.
* Se questo richiede un file di articolo nuovo di zecca (non solo una modifica a uno esistente), segui le convenzioni di posizione di questo repository: nessun `exl-id`/`TQID` creato in frontmatter, collegare la nuova pagina nel TOC rilevante e convertire il file in CRLF/no-BOM dopo averlo creato (lo strumento `Write` predefinito è LF).

## Passaggio 3: creare l&#39;attività Workfront

Progetto: **Attività di documentazione del prodotto - per problemi di sviluppo che richiedono la messaggistica**. Risolvi il suo ID con `insights_find_id_by_name` (entità `project`) invece di codificarlo, nel caso in cui dovesse cambiare. Vedi Valori noti di seguito per l&#39;ultimo ID risolto.

Campi attività:

| Campo | Valore |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | dalla ricerca del progetto precedente |
| `assignedToID` | utente corrente, da `insights_get_current_user` |
| `categoryID` | ID del modulo personalizzato della documentazione del prodotto: consulta Valori noti di seguito. Se non è chiaro, eseguire una query `task.task_categoryID` su qualsiasi attività di pari livello recente in questo progetto per confermare. |
| `description` | il **testo completo del messaggio di Slack** (tutti i campi del modello di richiesta, non una parafrasi), seguito da un collegamento alla conversazione Slack |
| `DE:Release notes` | una nota sulla versione formattata, consulta la sezione seguente formato |
| `DE:Preview Date Known` | `Yes`, per impostazione predefinita |
| `DE:Preview Date` | **Data di rilascio prevista** della richiesta, per impostazione predefinita |
| Prodotto/Area | selezionare `Fusion` (un campo enum nel modulo Documentazione prodotto; confermare il nome esatto del campo con `insights_search_fields` se non è mai chiaro) |

Imposta i campi della data di anteprima come parte della stessa chiamata di creazione: non lasciarli per dopo né attendere di essere richiesti. Se l’utente assegna una data diversa in un secondo momento o dice che la data non è ancora nota, effettua l’aggiornamento di conseguenza, ma per impostazione predefinita questa viene compilata ogni volta.

Formato nota sulla versione per il campo `DE:Release notes`. Inizia sempre con `***FUSION***` sulla propria riga, poi una riga vuota, quindi il titolo. In questo modo la nota viene contrassegnata come appartenente a Fusion (anziché al core Workfront) a colpo d&#39;occhio:

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Prima della chiamata di creazione, chiama `read_workflow_docs` con `workfront://tools/create-any-object`. Questa chiamata imposta campi personalizzati e un valore enum (`DE:Preview Date Known`) che lo richiede in base alle regole del server MCP.

## Passaggio 4: conferma all’utente

Report semplice:

* Quali file di documenti hai modificato e cosa hai aggiunto.
* Il nome dell’attività e l’URL.
* I valori esatti dei campi impostati, inclusi i campi della data di anteprima.
* Tutto ciò per cui non eri completamente sicuro: ad esempio, Slack non era raggiungibile e lavoravi solo con testo incollato, l&#39;articolo del documento di destinazione era ambiguo, o un dettaglio tecnico non era nel materiale sorgente e veniva segnalato invece di essere indovinato.

## Valori noti (da esecuzioni precedenti)

Conferma che questi siano ancora risolti, anziché presupporre che siano permanenti:

* Il progetto &quot;Attività di documentazione del prodotto - per problemi di sviluppo che richiedono la messaggistica&quot; è mappato sull&#39;ID `5e69583f00236b9f767c3e3944100ee4`
* Il modulo personalizzato per la documentazione del prodotto (`categoryID`) è `5d7275b9000514604bd969d418725843`
* Campi personalizzati utilizzati: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
