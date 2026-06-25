---
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---
# Modelli di riferimento per le note sulla versione

Modelli dettagliati per ogni tipo di pagina per le note sulla versione. Si basano sui modelli in
`help/quicksilver/product-announcements/product-releases/release-note-templates/` e
la formattazione effettiva utilizzata nelle ultime versioni trimestrali.

&#x200B;---

## Modello per pagina area di prodotto

```markdown
---
title: {Written Quarter} {Year} {Area} enhancements
description: {Written Quarter} {Year} {Area} enhancements
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} {Area} enhancements

This page describes {Area} enhancements made with the {Written Quarter} {Year} release to the Preview environment. These enhancements will be made available in the Production environment as noted.

For a list of all changes available at this point in the {Written Quarter} {Year} release cycle, see [{Written Quarter} {Year} release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title Here

>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}

Feature description paragraph.

For more information, see [Help article title](/help/quicksilver/path/to/article.md).
```

### Regole per le pagine dell&#39;area prodotto

- Utilizza markdown (non HTML) per il contenuto del corpo
- A ogni funzione viene assegnata un&#39;intestazione H2
- Il callout `>[!NOTE]` deve essere preceduto da una riga vuota
- Il formato `>[!NOTE]` è esattamente:

  ```
  >[!NOTE]
  >
  >Preview: {date}
  >Production fast release: {date}
  >Production for everyone: {date}
  ```

- Se una funzione è stata temporaneamente rimossa, aggiungi una riga dopo la data:

  ```
  >
  >This feature has been temporarily removed from the Production environment on {date}.
  ```

- I collegamenti della Guida utilizzano percorsi assoluti a partire da `/help/quicksilver/`

&#x200B;---

## Modello per pagina panoramica

```markdown
---
title: {Written Quarter} {Year} release overview
description: This page provides information about functionality that is included in the {Written Quarter} {Year} release. These enhancements are planned to become available in the Production environment throughout the quarter.
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} release overview

This page provides information about functionality that is included in the {Written Quarter} {Year} release scheduled for {Release Month} {Year}.

The enhancements on this page are available in the Preview environment. This page will be updated with additional enhancements as the {Written Quarter} {Year} release nears its planned Production release.

>[!IMPORTANT]
>
>
>Monthly and quarterly releases are planned to be available on the Thursday of the second full week of the month, unless otherwise specified.
>
>|Monthly release|Quarterly release|
>|----|----|
>|<ul><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li></ul>|<ul><li>{VV}.{M} ({Month Day, Year})</li></ul>|
>
>Note that for the final release of each quarter ({VV}.{M} this quarter), users on the fast release schedule will receive the release one day early ({Month Day, Year}).
>
>For more information on the fast release process, see [Enable or disable the fast release process](/help/quicksilver/administration-and-setup/set-up-workfront/configure-system-defaults/enable-fast-release-process.md).

## Adobe Workfront enhancements

* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
* [Project enhancements](#project-enhancements)
* [Reporting enhancements](#reporting-enhancements)
* [Requesting enhancements](#requesting-enhancements)
* [Other enhancements](#other-enhancements)
```

### Tabella delle funzioni di panoramica

Ogni sezione dell’area di prodotto H3 contiene una tabella HTML. Utilizza questa struttura esatta:

```html
### {Area} enhancements

<table>
            <col style="width: 50%;" />
            <col style="width: 25%;" />
            <tbody>
              <tr>
        <td><strong>Feature</strong>
        </td>
        <td><strong>Preview</strong></td>
        <td><strong>Fast release</strong></td>
        <td><strong>Quarterly</strong></td>
        </tr>
    <tr>
        <td>
            <a href="/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-{area}.md" class="MCXref xref" xrefformat="{para}">Feature Title</a><p>Short description of the feature.</p>
        </td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
    </tr>
            </tbody>
        </table>
```

#### Regole di tabella

- Cella funzione: `<a>` tag con `class="MCXref xref" xrefformat="{para}"` seguito da `<p>` descrizione
- I collegamenti `href` alla pagina dell&#39;area di prodotto (non un ancoraggio specifico)
- Celle data: racchiuse in `<p>` tag
- Per gli elementi fuori pianificazione, aggiungi `<p>[!BADGE Off schedule]{type=Neutral}</p>` dopo il collegamento
- Svuota `<p></p>` dopo che il collegamento è accettabile quando non è necessario un badge
- Mantieni il rientro di HTML coerente con i file esistenti

### Sezioni finali della panoramica

Dopo tutte le tabelle dell&#39;area di prodotto:

```markdown
## Release notes for other areas

### Workfront Fusion enhancements

New features in Workfront Fusion are available in Production at a cadence outside of the standard release schedule. For more information about the latest features, see [Adobe Workfront Fusion release activity](https://experienceleague.adobe.com/it/docs/workfront-fusion/using/fusion-release-activity/fusion-release-activity).

### Workfront Planning enhancements

New features in Workfront Planning are available in Production. For more information about the latest features, see [{Written Quarter} {Year} release activity for Adobe Workfront Planning](/help/quicksilver/product-announcements/product-releases/planning-release-activity/planning-release-activity-{YY}-q{N}.md).

There are no updates for the following at this point in the release:

* Scenario Planner
* Proof
* Goals

## Desktop proofing viewer updates

{Version info if available, otherwise omit section}

## Announcements

{Announcement content}

### API version {NN}

{API version info}

### Workfront Maintenance Updates

For information about the maintenance updates made during the {Written Quarter} {Year} release, see [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=it).

### Training updates

Explore the latest updates made to learning programs, learning paths, videos, and guides for each Adobe Workfront product release. For more information, see the "What's New" section of the [Workfront Tutorials page](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/home.html?lang=it).
```

&#x200B;---

## Modello per pagina look and feel

```markdown
---
title: Look-and-feel updates during the {Written Quarter} {Year} release time frame
description: Look-and-feel updates during the {Written Quarter} {Year} release time frame
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---

# Look-and-feel updates during the {Written Quarter} {Year} release time frame

This page describes minor updates to the look and feel of various areas of the Adobe Workfront application that were made within the {Written Quarter} {Year} release timeframe. These enhancements will be made available in the Production environment a minimum of 2 weeks after releasing to Preview.

For a list of all changes available with the {Written Quarter} {Year} release, see [{Written Quarter} {Year} Release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title

>[!NOTE]
>
>Preview release: {Month Day, Year}; Planned Production release: {Month Day, Year}

Description of the look-and-feel change.
```

&#x200B;---

## Formati di callout data

### Pagine dell&#39;area di prodotto (su più righe)

```markdown
>[!NOTE]
>
>Preview: March 5, 2026
>Production fast release: April 15, 2026
>Production for everyone: April 16, 2026
```

### Pagine look-and-feel (riga singola)

```markdown
>[!NOTE]
>
>Preview release: March 5, 2026; Planned Production release: March 19, 2026
```

### Pagine settimanali (riga singola)

```markdown
>[!NOTE]
>
>Preview release: February 9, 2023; Planned Production release: February 23, 2023
```

&#x200B;---

## Incongruenze note da rilevare

1. **Collegamento errato**: le pagine dell&#39;area di prodotto a volte si collegano alla panoramica del trimestre precedente (ad esempio, `26-q1` invece di `26-q2`)
2. **Anteprima date che mostrano l&#39;anno errato** — Le tabelle di panoramica a volte mostrano l&#39;anno precedente nella colonna Anteprima (ad esempio, &quot;2025&quot; invece di &quot;2026&quot;)
3. **Tag di chiusura mancanti `</tr>`** — Alcune righe della tabella HTML non dispongono di tag di chiusura corretti
4. **`content-type: release-notes`** - Presente in file meno recenti, omesso nelle pagine più recenti dell&#39;area prodotti 26-q2. Seguire lo schema del trimestre corrente.
5. **Errore nel modello**. Il modello look-and-feel contiene `relesae` invece di `release`. Usare sempre l&#39;ortografia corretta
6. **Manca `<p></p>` dopo il collegamento alle funzionalità** — Alcune righe della tabella di panoramica omettono il tag `<p>` vuoto dopo il tag `<a>`
