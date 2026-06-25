---
name: release-notes-formatter
description: Formatta e convalida le note sulla versione di Workfront per coerenza, struttura corretta e collegamento corretto. Da utilizzare solo per i file delle note sulla versione nelle directory delle versioni di prodotto o quando l’utente cita note sulla versione, versioni di prodotto o versioni trimestrali. Non applicare ad articoli tutorial o alla documentazione generale.
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 2%

---


# Note sulla versione Formatter

Formatta e convalida le note sulla versione di Adobe Workfront nella directory `help/quicksilver/product-announcements/product-releases/`.

## Tipi di pagina

Identifica il tipo di pagina dal percorso e dal contenuto del file:

| Tipo di pagina | Pattern file | Modello |
|-----------|-------------|----------|
| **Panoramica** | `{YY}-q{N}-release-overview.md` | Vedi .claude/commands/_release-notes-formatter-reference.md#overview-page-template |
| **Area di prodotto** | `{YY}-q{N}-{area}.md` | Vedi .claude/commands/_release-notes-formatter-reference.md#product-area-page-template |
| **Pianificazione** | `planning-release-activity-{YY}-q{N}.md` | Simile all&#39;area di prodotto |
| **Aspetto** | `look-and-feel-updates-{YY}-q{N}.md` | Vedi .claude/commands/_release-notes-formatter-reference.md#look-and-feel-page-template |

## Flusso di lavoro di formattazione

### Passaggio 1: Convalida materiale

Campi obbligatori per tutte le pagine delle note sulla versione:

```yaml
---
title: <descriptive title>
description: <matches or summarizes the title>
author: <author name>
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: <existing UUID — never generate or change>
---
```

Regole:
- `feature` deve essere esattamente `Product Announcements`
- `recommendations` deve essere esattamente `noDisplay, noCatalog`
- Non inventare mai un `exl-id`. Includere solo se ne esiste già uno
- Non aggiungere `draft: Probably` a pagine reali (solo modelli)

### Passaggio 2: Convalida struttura per tipo di pagina

#### Pagine area prodotto

1. **H1**: `{Written Quarter} {Area} enhancements`
   - Esempio: `# Second Quarter 2026 Administrator enhancements`
   - Il trimestre deve essere compilato: &quot;Primo trimestre&quot;, &quot;Secondo trimestre&quot;, &quot;Terzo trimestre&quot;, &quot;Quarto trimestre&quot;

2. **Paragrafo introduttivo**: descrive l&#39;area e i collegamenti alla panoramica
   - Deve essere collegato al file di panoramica **del trimestre corretto**
   - Bug comune: collegamento al trimestre precedente (ad esempio, `26-q1` anziché `26-q2`)

3. **H2 per funzionalità**: titolo funzionalità come intestazione
   - **Prima le nuove funzioni**: la nota sulla versione più recente deve apparire come primo H2 dopo il paragrafo dell&#39;introduzione
   - Le feature meno recenti seguono in ordine cronologico inverso

4. **Blocco callout data** dopo ogni H2:

```markdown
>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}
```

5. **Corpo**: descrizione funzione, quindi collegamento alla documentazione

#### Pagine Panoramica

1. **H1**: `{Written Quarter} release overview`

2. **Paragrafo introduttivo** con mese di rilascio pianificato

3. **`>[!IMPORTANT]`blocco** con tabella di pianificazione della versione

4. **H2`Adobe Workfront enhancements`** con elenco puntato di collegamenti di ancoraggio:

```markdown
* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
```

5. **H3 per area di prodotto** con tabella delle funzionalità di HTML (vedere .claude/commands/_release-notes-formatter-reference.md#overview-feature-table)
   - All&#39;interno di ogni tabella, **prima le funzionalità più recenti**. La riga più recente viene visualizzata nella parte superiore della tabella (dopo la riga di intestazione)

6. **Sezioni finali** (H2): note sulla versione per altre aree, aggiornamenti del visualizzatore per la verifica del desktop, annunci, versione API, aggiornamenti di manutenzione, aggiornamenti di formazione

### Passaggio 3: Convalidare i collegamenti

- **Collegamento alla panoramica nelle pagine dell&#39;area di prodotto**: deve puntare allo stesso trimestre
   - Corretto: `26-q2-release-activity/26-q2-release-overview.md`
   - Sbagliato: `26-q1-release-activity/26-q1-release-overview.md`
- **Collegamenti di ancoraggio nella panoramica**: devono corrispondere agli ID H3 (lettere minuscole, trattini)
- **Collegamenti alle funzionalità nelle tabelle di panoramica**: deve utilizzare `class="MCXref xref" xrefformat="{para}"`
- **Collegamenti alla documentazione della Guida**: deve iniziare con `/help/quicksilver/`

### Passaggio 4: Convalidare le date

- Formato: `{Month} {Day}, {Year}` (esempio: &quot;12 marzo 2026&quot;)
- Usa `TBD` per date sconosciute
- Le date nel blocco della pagina dell&#39;area di prodotto `>[!NOTE]` devono corrispondere alla riga della tabella di panoramica corrispondente
- Le date di anteprima devono precedere le date di produzione

### Passaggio 5: Correzioni comuni

Applica queste correzioni durante la formattazione:

| Problema | Correggi |
|-------|-----|
| Trimestre collegamento panoramica errato | Aggiorna per corrispondere al trimestre del file |
| Blocco date `>[!NOTE]` mancante | Aggiungi blocco dopo l&#39;intestazione della funzionalità H2 |
| Formato data non coerente | Standardizza su `Month Day, Year` |
| Riga vuota mancante prima di `>[!NOTE]` | Aggiungi riga vuota |
| Spazi aggiuntivi nelle linee del callout | Ritaglia spazio vuoto finale |
| HTML nelle pagine dell’area prodotti | Mantieni come markdown (HTML è solo per tabelle di panoramica) |
| Manca `exl-id` | Escludilo — non generarne uno |

### Passaggio 6: aggiornare il sommario

Ogni volta che crei una pagina delle note sulla versione di **new** (panoramica o area prodotti), aggiungila a `help/quicksilver/TOC.md` con la stessa modifica. Una pagina non inclusa nel sommario non verrà visualizzata nella navigazione pubblicata, anche se i collegamenti presenti nella tabella panoramica vi fanno riferimento.

Dove aggiungerlo:

- Il sommario include una sezione al trimestre sotto un&#39;intestazione come `* 2026 Q3 Release {#release-26-q3}`. Se il titolo del trimestre non esiste ancora (prima pagina di un nuovo trimestre), aggiungilo sopra il trimestre precedente in modo che sia in alto il trimestre più recente.
- Sotto l’intestazione del trimestre, elenca le pagine nell’ordine seguente:
   1. **Panoramica** (`Third Quarter 2026 release overview`).
   2. **Pagine dell&#39;area di prodotto** in ordine alfabetico per nome area (amministratore, documenti, operazioni dell&#39;organizzazione, progetti, reporting, richiesta).
   3. **Altri miglioramenti** sono stati apportati per ultimi (sempre dopo le aree alfabetiche dei prodotti).

Ogni voce del sommario è un collegamento di markdown che utilizza il titolo della pagina e il percorso assoluto dell’archivio:

```markdown
      * [Third Quarter 2026 Documents enhancements](/help/quicksilver/product-announcements/product-releases/26-q3-release-activity/26-q3-documents.md)
```

Abbina il rientro (sei spazi) alle voci circostanti. Utilizzare la pagina H1 come testo di collegamento, ad esempio `Documents enhancements`, `Requesting enhancements` (non `Requests`), in modo che le etichette del sommario corrispondano ai trimestri precedenti.

Errori comuni da evitare:

- Creazione di una pagina dell&#39;area di prodotto senza aggiungerla al sommario.
- Collegamento alla panoramica di un trimestre diverso dalla nuova pagina dell’area di prodotto (passaggio 3).
- Inserire le pagine di un nuovo trimestre sotto l&#39;intestazione del trimestre precedente.

## Convenzioni di denominazione dei file

| Tipo | Pattern | Esempio |
|------|---------|---------|
| Panoramica | `{YY}-q{N}-release-overview.md` | `26-q2-release-overview.md` |
| Area di prodotto | `{YY}-q{N}-{area-slug}.md` | `26-q2-admin-and-setup.md` |
| Directory | `{YY}-q{N}-release-activity/` | `26-q2-release-activity/` |

Campioni area standard: `admin-and-setup`, `documents`, `projects`, `reports`, `requests`, `other`

## Mappatura trimestre

| Trimestre | Modulo scritto | Months |
|---------|-------------|--------|
| Q1 | Primo Trimestre | Gen-Mar |
| Q2 | Secondo trimestre | Apr-Giu |
| Q3 | Terzo trimestre | lug-set |
| Q4 | Quarto trimestre | Ott-Dic |

Il rilascio della produzione trimestrale solitamente arriva il giovedì della seconda settimana completa dell’ultimo mese del trimestre.

## Elenco di controllo convalida

Durante la revisione di un file delle note sulla versione, verificare:

- [ ] Frontmatter ha tutti i campi obbligatori con valori corretti
- [ ] H1 corrisponde al formato del tipo di pagina
- [ Il collegamento Panoramica di ] punta al trimestre corretto
- [ ] Ogni funzione ha un blocco di data `>[!NOTE]` (pagine dell&#39;area prodotti)
- [ ] Formato data coerente (`Month Day, Year`)
- [ ] righe della tabella delle funzionalità nella panoramica corrispondono al contenuto della pagina dell&#39;area di prodotto
- [ ] Nessun collegamento interno interrotto
- [ ] I collegamenti di ancoraggio nella panoramica corrispondono agli ID sezione H3
- [ Le funzionalità di ] sono ordinate in ordine di novità (sia nelle pagine dell&#39;area di prodotto che nelle tabelle di panoramica)
- [ ] Le nuove pagine delle note sulla versione sono elencate in `help/quicksilver/TOC.md` nel trimestre corretto, con la prima panoramica e le aree di prodotto in ordine alfabetico (Altre ultime)

## Risorse aggiuntive

- Per esempi e modelli completi di HTML, consultate .claude/commands/_release-notes-formatter-reference.md
