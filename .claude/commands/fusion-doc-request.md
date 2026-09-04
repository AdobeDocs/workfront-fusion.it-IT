---
name: fusion-doc-request
description: Gestire una richiesta di documentazione di Fusion dal modello Slack
source-git-commit: 6726c582294758de0bbab19d6014ad80bb66e553
workflow-type: tm+mt
source-wordcount: '1120'
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

&#x200B;* **Titolo funzionalità**
&#x200B;* **Descrizione**
&#x200B;* **Punti da aggiungere alla documentazione** *(talvolta presenti - sezioni/dettagli specifici richiesti dal richiedente; trattarli come obbligatori, non facoltativi, se forniti)*
&#x200B;* **Data di rilascio prevista**
&#x200B;* **Annuncio necessario** *(Sì/No - solo informativo; vedere la nota precedente. Non intervenire su questo campo.)*

Se la richiesta è collegata a una pagina wiki di Confluence con le specifiche complete, recuperarla (`get_wiki_content`) prima di scrivere la documentazione. Non fare affidamento solo sul riepilogo di Slack per i dettagli tecnici (nomi di campo esatti, passaggi, etichette dell’interfaccia utente) - richiamare quelli dalla specifica wiki quando ne viene collegata una.

Se invece la richiesta è collegata a un’origine secondaria non di Confluence (ad esempio un post della community Experience League, un articolo di supporto, un riepilogo generato da AI) anziché a una specifica autorevole, puoi utilizzarla per compilare i dettagli tecnici mancanti nel testo di Slack, ma trattarla come un elemento di affidabilità inferiore rispetto alla richiesta Slack stessa. Se è in conflitto o si aggiunge al testo di Slack (un nome diverso per lo stesso pulsante/campo, un dettaglio non menzionato in Slack), non sceglierne immediatamente uno; scrivi il documento utilizzando il testo della richiesta Slack come origine principale e contrassegna la discrepanza in linea con un commento di HTML (ad esempio `<!-- BECKY CHECK ME: Slack calls this "Activate," but the linked community post calls it "Reactivate" - confirm against the live UI. -->`) in base alle indicazioni del passaggio 2.

## Passaggio 2: aggiornare la documentazione

Trova gli articoli esistenti rilevanti in questo archivio (grep per i nomi dei moduli, le etichette dell’interfaccia utente o i nomi delle impostazioni correlati, non indovinare il file). Aggiornali per riflettere la modifica, seguendo la struttura esistente dell’articolo, il livello di intestazione e lo stile della casa.

&#x200B;* Non inventare dettagli tecnici (nomi di campo esatti, ambiti di autorizzazione, passaggi di configurazione) che non sono presenti nella richiesta Slack o nelle specifiche wiki collegate. Se qualcosa non è confermato, contrassegnalo in linea come commento HTML (ad esempio `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) invece di indovinare - mai come callout visibile. Non deve essere riprodotto sulla pagina pubblicata.
&#x200B;* Se questo richiede un file di articolo nuovo di zecca (non solo una modifica a uno esistente), segui le convenzioni di posizione di questo repository: nessun `exl-id`/`TQID` creato in frontmatter, e converti il file in CRLF/no-BOM dopo averlo creato (lo strumento `Write` predefinito è LF).
&#x200B;* Inserire una nuova pagina nel &quot;sommario&quot; significa ENTRAMBE queste, non una sola: una pagina può essere collegata da un sottoindice pur rimanendo invisibile ai lettori:
  - Il file di navigazione principale per l&#39;area di prodotto (ad esempio `help/workfront-fusion/TOC.md`): è questo che determina la struttura di navigazione pubblicata.
  - Qualsiasi sottoindice/pagina di destinazione nel contenuto che collega anche articoli di questo tipo (ad esempio `apps-and-modules-toc.md` per una nuova pagina di moduli connettore).
    Seleziona esplicitamente e conferma che la nuova voce si trovi nello stesso elenco, allo stesso livello di nidificazione, in quanto gli articoli di pari livello più vicini in ciascun file - non presumere di aggiungerla a una copre l’altra.

## Passaggio 3: creare l&#39;attività Workfront

Progetto: **Attività di documentazione del prodotto - per problemi di sviluppo che richiedono la messaggistica**. Risolvi il suo ID con `insights_find_id_by_name` (entità `project`) invece di codificarlo, nel caso in cui dovesse cambiare. Vedi Valori noti di seguito per l&#39;ultimo ID risolto.

Campi attività:

| Campo | Valore |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | dalla ricerca del progetto precedente |
| `parentID` | l&#39;ID dell&#39;attività padre (`parentID`, un campo di sistema - nessun prefisso `DE:`). Vedere i valori noti di seguito. In questo modo la nuova attività diventa una sottoattività e non un&#39;attività di livello superiore nel progetto. |
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

&#x200B;* Quali file di documenti hai modificato e cosa hai aggiunto.
&#x200B;* Il nome dell’attività e l’URL.
&#x200B;* I valori esatti dei campi impostati, inclusi i campi della data di anteprima.
&#x200B;* Tutto ciò per cui non eri completamente sicuro: ad esempio, Slack non era raggiungibile e lavoravi solo con testo incollato, l&#39;articolo del documento di destinazione era ambiguo, o un dettaglio tecnico non era nel materiale sorgente e veniva segnalato invece di essere indovinato.

## Valori noti (da esecuzioni precedenti)

Conferma che questi siano ancora risolti, anziché presupporre che siano permanenti:

&#x200B;* Il progetto &quot;Attività di documentazione del prodotto - per problemi di sviluppo che richiedono la messaggistica&quot; è mappato sull&#39;ID `5e69583f00236b9f767c3e3944100ee4`
&#x200B;* L&#39;attività padre &quot;Becky - Tasks from Fusion-Documentation channel&quot; è mappata sull&#39;ID `6a9b065100003a7554832780c2015e93` (nello stesso progetto) - resolve con `insights_find_id_by_name` (entità `task`) anziché mediante codifica fissa, nel caso in cui cambi mai
&#x200B;* Il modulo personalizzato per la documentazione del prodotto (`categoryID`) è `5d7275b9000514604bd969d418725843`
&#x200B;* Campi personalizzati utilizzati: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
