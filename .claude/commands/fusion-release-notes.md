---
name: fusion-release-notes
description: Crea una nuova pagina delle note sulla versione settimanale di Workfront Fusion e collegala alla pagina di panoramica delle attività di rilascio e al sommario. Da utilizzare quando l’utente desidera scrivere, aggiungere o creare una nuova nota sulla versione di Fusion o una nuova pagina sulla versione settimanale, oppure quando richiede di documentare le nuove funzioni di Fusion per una versione. Non utilizzare per le note sulla versione di Workfront (Quicksilver) in annunci di prodotti/versioni di prodotti; utilizza le note sulla versione-formattatore per tali note.
source-git-commit: 94492dbd382eee2f4e66e53d53a441ca82492bfb
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---


# Note sulla versione di Fusion

Crea una nuova pagina delle note sulla versione settimanale di Adobe Workfront **Fusion** in `help/workfront-fusion/fusion-product-releases/` e la collega dalle due posizioni che ne rendono individuabile la presenza: la pagina di panoramica dell&#39;attività sulla versione e `help/workfront-fusion/TOC.md`.

Si tratta di un sistema diverso dalle note sulla versione di Quicksilver (core Workfront) gestite dall&#39;abilità `release-notes-formatter`:

| | Note sulla versione di Fusion (questa abilità) | Note sulla versione di Quicksilver (`release-notes-formatter`) |
|---|---|---|
| Cadenza | Settimanale | Trimestrale |
| Directory | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| Callout data per funzione | No - il titolo della pagina riporta la settimana | Sì — `>[!NOTE]` blocco per funzione |
| Pagina indice | `fusion-release-activity.md` (per anno/mese) | `{YY}-q{N}-release-overview.md` (per trimestre) |

## Passaggio 1: raccogliere le funzionalità

Chiedi all’utente (se non già fornito) l’elenco delle funzioni/modifiche al documento per la settimana e per ciascuna:

- Titolo breve della funzione
- Una semplice descrizione di ciò che è cambiato e del perché è importante
- Gli articoli della guida a cui è collegato (verifica che il percorso esista — non indovinare)
- Se richiede un&#39;azione utente/amministratore o è una dichiarazione di obsolescenza (richiede un callout `>[!IMPORTANT]`)
- **Se si tratta di un nuovo avvio del connettore** (un nuovo connettore/app che diventa disponibile, non solo nuovi moduli aggiunti a un connettore esistente). In caso affermativo, questo attiva **Passaggio 7** — non saltare le richieste di reindirizzamento solo perché è stata completata la nota sulla versione.

## Passaggio 2: determinare il nome e la data del file

- Trova il lunedì (o data di rilascio) per la settimana da documentare e confermalo con l’utente se ambiguo.
- Percorso file: `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` e `{D}` non hanno **zeri iniziali**: `fusion-2026-7-20.md`, non `fusion-2026-07-20.md`.
  - Se la cartella dell&#39;anno non esiste ancora, creala.
- Controlla se esiste già una pagina per quella settimana prima di crearne una nuova.

## Passaggio 3: scrivere la pagina

### Frontmatter

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

Regole:
- `title` e `description` sono identici.
- Includi sempre la virgola nella data (`July 20, 2026`), anche se alcune pagine meno recenti la omettono, non copiare tale incoerenza.
- **Utilizza `hidefromtoc: true` per ogni nuova pagina. Non aggiungere `exl-id` o `TQID`.** Questi vengono assegnati in un secondo momento, dopo la pubblicazione della pagina; inventarne uno è sbagliato. (Le pagine a partire dalla metà del 2026 seguono tutte questo pattern. Se devi controllare un esempio, consulta `_fusion-release-notes-reference.md`).

### Corpo

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

Note:
- Una H2 per funzione, nell’ordine assegnato dall’utente (nessun nuovo ordine forzato all’interno della pagina — è una sola settimana).
- Nessun callout di data `>[!NOTE]` per funzione: il titolo della pagina contiene già la data.
- Se una funzionalità richiede un&#39;azione o rappresenta una modifica o un&#39;esclusione, aggiungere un callout `>[!IMPORTANT]` direttamente sotto H2, prima della descrizione:

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```

- Ogni funzionalità deve terminare con un &quot;Per ulteriori informazioni, vedere [...]&quot; collegamento all’articolo della guida pertinente. Verifica che la destinazione del collegamento esista nell’archivio.

## Passaggio 4: aggiungere la pagina all’indice della panoramica

Modifica `help/workfront-fusion/fusion-product-releases/fusion-release-activity.md`:

- Trovare la sezione `## Fusion releases in {current year}` (è **not** racchiusa in un blocco comprimibile `+++`, solo gli anni passati sono compressi).
- Trova o crea l&#39;intestazione `### {Month} {Year}` per il mese della versione, direttamente sotto l&#39;intestazione dell&#39;anno.
  - Se l&#39;intestazione del mese non esiste ancora, aggiungerla **al di sopra** del mese precedente (prima il mese più recente).
- Aggiungi la nuova pagina come punto elenco **primo** sotto l&#39;intestazione del mese (prima la settimana più recente):

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- Se si tratta della prima versione di un nuovo anno, aggiungi una nuova intestazione `## Fusion releases in {YYYY}` sopra l&#39;intestazione dell&#39;anno precedente e racchiudi la sezione dell&#39;*anno precedente* in un blocco comprimibile `+++ **Click to open**` / `+++`, se non lo è già (solo l&#39;anno corrente rimane espanso).

## Passaggio 5: aggiungi la pagina al sommario

Modifica `help/workfront-fusion/TOC.md`:

- Trova `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` per l&#39;anno corrente, nidificato in `* Fusion release activity {#fusion-release-activity}`.
- Aggiungi la nuova pagina come **prima** voce sotto tale intestazione (prima più recente), corrispondente al rientro esistente (8 spazi):

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- Se l&#39;intestazione dell&#39;anno corrente non esiste ancora, aggiungere `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` sopra l&#39;intestazione dell&#39;anno precedente.
- **Non** aggiungere il prefisso `{hide-from-toc}` alle nuove voci, che viene utilizzato solo per le voci meno recenti una volta superata la navigazione visibile (vedi Incoerenze note di seguito).

### Incongruenze note da rilevare (non replicare)

- Diverse voci del sommario relative all’inizio del 2026 sono nidificate sotto l’intestazione `Fusion releases - 2025` per errore, anche se le pagine stesse sono versioni del 2026. Quando aggiungi una nuova voce, controlla sempre che arrivi sotto l&#39;intestazione corrispondente al **suo anno**, non dove si trova la voce precedente.
- Alcuni titoli di pagina/H1 meno recenti omettono la virgola prima dell&#39;anno (`July 13 2026` invece di `July 13, 2026`). Usa sempre la virgola nelle nuove pagine.

## Passaggio 7: nuovi avvii dei connettori — domande su un reindirizzamento (non saltare)

**Questo passaggio si applica ogni volta che il passaggio 1 ha identificato l&#39;avvio di un nuovo connettore.** È facile considerare la nota sulla versione &quot;completata&quot; dopo il passaggio 5 e dimenticare questo — trattare una nuova funzione del connettore come incompleta fino a quando questo passaggio non è stato affrontato in un modo o nell&#39;altro.

Chiedere all&#39;utente: *&quot;Impostare un reindirizzamento per il nuovo articolo del connettore?&quot;*

- Se **no**, tieni presente che e continua — nient&#39;altro da fare.
- Se **sì**, raccogliere:
  - Il percorso di origine **&#x200B;**&#x200B;(deve iniziare con `/en`, senza spazi)
  - La **destinazione** — un percorso relativo che inizia con `/en` o un URL `https` completo (senza spazi)
- Aggiungere la riga all&#39;archivio `Adobe-Enterprise-Docs/redirects` di pari livello in `redirects/` un file per ambiente (`redirects-dev.csv`, `redirects-stage.csv`, `redirects-prod.csv`).
- Regole di riga (dal file README dell’archivio):
  - Nessuna coppia duplicata `source` e nessuna coppia duplicata `source`/`destination`.
  - Il reindirizzamento non deve causare un loop di reindirizzamento.
- **Questa abilità aggiunge la riga CSV solo dopo la conferma dell&#39;utente.** L&#39;aumento del PR nell&#39;archivio `redirects` è un passaggio separato che questa abilità non fa: indica all&#39;utente che un PR deve ancora essere aperto e unito lì prima che il reindirizzamento venga attivato (~5 minuti dopo l&#39;unione per reindirizzamenti 1:1).

## Passaggio 8: elenco di controllo finale

- [ ] File creato nel percorso corretto senza zeri iniziali nella data
- [ ] Il materiale frontale utilizza `hidefromtoc: true`, nessun oggetto inventato `exl-id`/`TQID`
- [ ] Corrispondenza titolo/descrizione, la data include la virgola
- [ ] Per ogni funzionalità sono disponibili una descrizione e un collegamento &quot;Per ulteriori informazioni&quot; verificato
- [ ] Le funzionalità Action-required/Deprecation hanno un callout `>[!IMPORTANT]`
- [ ] Nuova pagina aggiunta come voce più recente in `fusion-release-activity.md`, nell&#39;anno/mese corretto
- [ ] Nuova pagina aggiunta come voce più recente in `TOC.md`, sotto l&#39;intestazione dell&#39;anno corretto
- [ ] intestazioni anno/mese nuove create se necessario, con l&#39;anno precedente compresso in `fusion-release-activity.md`
- [ ] **Se una funzione era un nuovo avvio del connettore: richiesta di informazioni su un reindirizzamento (passaggio 7), impostarne uno o rifiutarlo esplicitamente**

## Risorse aggiuntive

Per esempi completi di lavoro (una settimana semplice con più funzionalità e una con un callout di azione `>[!IMPORTANT]`), vedere `.claude/commands/_fusion-release-notes-reference.md`.
