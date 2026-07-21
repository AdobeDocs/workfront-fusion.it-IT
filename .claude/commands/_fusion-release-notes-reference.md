---
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# Esempi di riferimento delle note sulla versione di Fusion

Esempi funzionanti per l&#39;abilità `fusion-release-notes`, in base alle pagine recenti effettive in
`help/workfront-fusion/fusion-product-releases/fusion-releases-2026/`.

&#x200B;---

## Esempio 1: settimana multifunzionale diretta

Basato su `fusion-2026-6-22.md`.

```markdown
---
title: Workfront Fusion release activity Week of June 22, 2026
description: Workfront Fusion release activity Week of June 22, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of June 22, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of June 22, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/it/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Create custom JavaScript packages to use in scenarios

To provide better flexibility and control of your scenarios, we've added the ability to create a custom JavaScript packages that you can then use in scenarios. You can create custom packages in the Packages area of Fusion. You then add functions or variables from these packages to your scenarios in the form of an Adobe App Builder module.

Packages include functions, along with any variables or dependencies the functions rely on. You can also test functions in your package before using them in your scenarios

Because custom packages work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

For more information on using custom functions in Fusion, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

## View changes between scenario versions

To make it easier to understand changes between scenario versions, we've added the ability to view and compare those changes. Now you can bring up a window that displays specific changes between two selected versions of the same scenario.

For more information, see [View and manage scenario versions](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).
```

&#x200B;---

## Esempio 2: settimana con un callout obbligatorio/obsoleto

Basato su `fusion-2026-3-9.md`.

```markdown
---
title: Workfront Fusion release activity Week of March 9, 2026
description: Workfront Fusion release activity Week of March 9, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of March 9, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of March 9, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/it/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Log in to Fusion through Adobe IMS

>[!IMPORTANT]
>
>**Action Required: Migrate to IMS Login for Adobe Workfront Fusion by April 15.**
>
>To ensure that you will be able to log in after April 15, your Fusion administrator must migrate you to Adobe IMS. Please contact your Fusion administrator to be migrated.

As part of our ongoing security enhancements, Adobe is deprecating the legacy username and password login method for Adobe Workfront Fusion. Effective **April 15**, the legacy login flow **will no longer be supported**.

Going forward, access to Adobe Workfront Fusion will require authentication through the Adobe Identity Management System (IMS) login flow.

For instructions on provisioning access through the Adobe Admin Console, see [Add users to Adobe Workfront Fusion through the Adobe Admin Console](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-fusion-users-admin-console.md).

If you have questions or need assistance with the migration process, please contact your Adobe representative.

## New route labels

To make it easier to identify routes, we've added labels. Now, routes are labeled in the order they execute. Fallback and error handling routes are also labeled. Route labels also display any filters used for that route.

For more information on routes, see [Add a Router module and configure routes](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).
```

&#x200B;---

## Schema di aggiornamento della pagina Panoramica (`fusion-release-activity.md`)

Aggiunta della settimana del 20 luglio 2026 a una sezione del mese di luglio 2026 esistente:

```markdown
## Fusion releases in 2026

### July 2026

* [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
* [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
```

A partire dal nuovo anno del brand (solo ad esempio, eseguire questa operazione quando viene pubblicata la prima versione di {YYYY+1}):

```markdown
## Fusion releases in 2027

### January 2027

* [Workfront Fusion release activity: Week of January 4, 2027](/help/workfront-fusion/fusion-product-releases/fusion-releases-2027/fusion-2027-1-4.md)

## Fusion releases in 2026

+++ **Click to open**

### December 2026
...
+++
```

&#x200B;---

## Schema di aggiornamento TOC.md

Aggiunta della settimana del 20 luglio 2026 come voce più recente:

```markdown
* Fusion release activity {#fusion-release-activity}
    * [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)
    * Fusion releases - 2026 {#fusion-releases-2026}
        * [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
        * [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
        ...
```

&#x200B;---

## Incongruenze note nelle pagine esistenti (solo come riferimento, non copiarle in nuove pagine)

1. **Intestazione anno non posizionata correttamente in TOC.md**. Le voci di gennaio-febbraio 2026 si trovano attualmente sotto l&#39;intestazione `Fusion releases - 2025` invece di `Fusion releases - 2026`. Si tratta di un bug preesistente, non della struttura prevista.
2. **Virgola mancante prima dell&#39;anno** — per pagine come `fusion-2026-7-13.md`, nel titolo/descrizione/H1 viene utilizzato &quot;13 luglio 2026&quot; invece di &quot;13 luglio 2026&quot;. Includi sempre la virgola nelle nuove pagine.
3. **`hidefromtoc`rispetto a `exl-id`/`TQID`** — le pagine fino a `fusion-2026-4-27.md` hanno un `exl-id` (e a volte `TQID`); le pagine da `fusion-2026-5-4.md` in poi usano invece `hidefromtoc: true`. Le nuove pagine devono seguire il pattern più recente (`hidefromtoc: true`, no `exl-id`/`TQID`) poiché tali identificatori vengono assegnati successivamente dalla pipeline di pubblicazione.
4. Prefisso **`{hide-from-toc}`in TOC.md**: utilizzato per de-enfatizzare le voci precedenti nella navigazione sottoposta a rendering una volta scadute le visualizzazioni recenti. Non aggiungerlo a una voce nuova.
