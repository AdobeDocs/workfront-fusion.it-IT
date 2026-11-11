---
title: Panoramica sulle organizzazioni e sui team di Fusion
description: Le funzioni Organizzazione e Team di Adobe Workfront Fusion consentono alle aziende di controllare l'accesso a scenari e altre funzioni all'interno di Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 44e6de2a-b2d3-410d-abc3-10facd258495
TQID: 'https://experienceleague.adobe.com/rWg9TitUlX092UIFTY1LUZsR7UlmWwE5dItl6wnlBMA'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: f9cdbcf936fc6b022f6513f47b9b377424731419
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%
---
# Panoramica sulle organizzazioni e sui team di Adobe Workfront Fusion

Le funzioni Organizzazione e Team di Adobe Workfront Fusion consentono alle aziende di controllare l&#39;accesso a scenari e altre funzioni all&#39;interno di Fusion.

Un’organizzazione è l’entità più grande in Adobe Workfront Fusion. Ad esempio, l’organizzazione Fusion potrebbe rappresentare l’account Fusion per l’intera azienda.

I team sono gruppi più piccoli all’interno dell’organizzazione e condividono risorse Fusion come scenari, connessioni e modelli.

Per istruzioni sulla creazione di un team, vedere [Creare un team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/create-a-team.md).

## Organizzazioni

Gli utenti di Workfront Fusion appartengono a un’organizzazione.

Gli utenti devono essere aggiunti a un’organizzazione prima di essere aggiunti a un team.

### Risorse dell’organizzazione

Le risorse seguenti interessano l&#39;intera organizzazione di Fusion e sono pertanto di proprietà e gestite a livello di organizzazione:

* **Pool di lavoro:**: un pool di lavoro è una quantità di risorse di elaborazione di Workfront Fusion dedicate a un&#39;organizzazione specifica.

  Per ulteriori informazioni, vedere [Pool di lavoro](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/worker-pools.md).

* **Operazioni**: un&#39;operazione in Adobe Workfront Fusion è un&#39;attività eseguita da un modulo.

  Per ulteriori informazioni, consulta [Operazioni](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

### Ruoli organizzazione

Un utente ha uno dei seguenti ruoli in un’organizzazione:

* **[!UICONTROL Proprietario]**: il proprietario dispone di tutte le autorizzazioni disponibili nell&#39;organizzazione.
* **[!UICONTROL Amministratore]**: gli amministratori possono gestire gli utenti su Adobe Admin Console se l&#39;organizzazione è abilitata per Adobe Identity Management System (IMS) o possono invitare nuovi utenti per organizzazioni non su IMS. Possono anche approvare i modelli.
* **[!UICONTROL Membro]**: i membri possono utilizzare Workfront Fusion, ma non possono apportare modifiche organizzative.
* **[!UICONTROL Contabile]**: gli account possono visualizzare le informazioni sulla licenza nel dashboard dell&#39;organizzazione, ma non possono eseguire alcuna azione.
* **[!UICONTROL Sviluppatore app]**: la funzionalità per questo ruolo non è attualmente disponibile e lo sarà prossimamente. Non è consigliabile assegnare gli utenti a questo ruolo in questo momento.

Per informazioni sulle azioni specifiche disponibili per gli utenti in ogni ruolo dell&#39;organizzazione, vedere [Ruoli dell&#39;organizzazione e del team](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

## Team

I team sono gruppi di utenti che condividono l’accesso a risorse specifiche. Tali risorse possono includere:

* Scenari
* Connessioni
* Webhook
* Chiavi
* Archivi di dati
* Strutture di dati
* Impostazioni delle notifiche e-mail

>[!NOTE]
>
>Poiché i team condividono le risorse, a volte è utile che un team abbia un solo membro. Ad esempio, gli utenti in formazione possono creare connessioni ai propri account Workfront individuali. Tutti i membri del gruppo possono connettersi al singolo account Workfront. In questo caso, consigliamo che l’utente sia l’unico membro di un team di formazione.

Le organizzazioni possono disporre di tutti i team necessari e gli utenti possono appartenere a uno o più team.

Gli utenti possono selezionare il proprio team dall’elenco a discesa nel pannello di navigazione a sinistra. Gli utenti visualizzano solo i team di cui sono membri. La selezione di un team consente a un utente di accedere alle risorse del team.

### Ruoli di team

Un utente ha uno dei seguenti ruoli in ciascuno dei propri team:

* **[!UICONTROL Amministratore team]**: gli amministratori possono aggiungere, rimuovere o modificare il ruolo di un membro del team. Possono inoltre eseguire qualsiasi azione disponibile per gli altri ruoli del team.
* **[!UICONTROL Membro team]**: il ruolo del membro del team consente agli utenti di creare ed eseguire scenari.
* **[!UICONTROL Monitoraggio team]**: il ruolo [!UICONTROL monitoraggio] consente agli utenti di accedere alle informazioni sull&#39;esecuzione per gli scenari, ma non è possibile progettare scenari o modificare lo stato &quot;Attivo&quot;.
* **[!UICONTROL Operatore team]**: il ruolo [!UICONTROL operatore] consente agli utenti di visualizzare i dati di esecuzione e di modificare lo stato &quot;Attivo&quot; degli scenari.
* **[!UICONTROL Membro con restrizioni team]**: la funzionalità per questo ruolo non è attualmente disponibile e sarà disponibile prossimamente. Non è consigliabile assegnare gli utenti a questo ruolo in questo momento.

Per informazioni sulle azioni specifiche disponibili per gli utenti in ogni ruolo del team, vedere [Ruoli organizzazione e team](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

### Ruoli di team personalizzati

<!-- BECKY CHECK ME: The source material (the Slack announcement) says flexible permissions are live in QA and for internal customers, with a limited pilot with paid customers next, then general availability. Confirm availability at the 2026-11-12 release before publishing, and whether this section should say that the feature is available only to some organizations. -->

Oltre ai ruoli di team predefiniti, ogni team dispone di una scheda **[!UICONTROL Ruoli]** in cui è possibile creare ruoli personalizzati. È possibile creare, aggiornare ed eliminare ruoli e scegliere esattamente quali autorizzazioni includere in ogni ruolo. Non sei più limitato a un set fisso di ruoli.

Per istruzioni, vedere [Visualizzare e gestire i ruoli del team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-and-manage-team-roles.md).

Con i ruoli personalizzati, puoi:

* Offri a ogni persona solo l’accesso di cui ha bisogno per il lavoro, riducendo il rischio di modifiche accidentali a scenari critici.
* Imposta l’accesso in base al funzionamento dell’organizzazione, anziché adattare i team ai ruoli predefiniti.
* Gestisci autonomamente l’accesso, senza contattare il supporto tecnico.

Chiunque disponga dell&#39;autorizzazione **[!UICONTROL Gestione membri]** in un team può creare, aggiornare, eliminare e assegnare gli utenti ai ruoli del team. Nei ruoli predefiniti, questa autorizzazione è inclusa nei ruoli Amministratore team e Proprietario organizzazione.

* I proprietari dell’organizzazione possono creare e gestire ruoli in tutti i team.
* Gli amministratori dell&#39;organizzazione possono gestire i ruoli solo nei team di cui sono membri e in cui dispongono dell&#39;autorizzazione **[!UICONTROL Gestisci membri]**.
* Gli amministratori del team possono gestire i ruoli nei propri team.

<!-- BECKY CHECK ME: The source does not describe the steps in the Roles tab, the list of permissions that you can choose from, or whether you can edit or delete the predefined roles. Add the steps and permissions list once confirmed. Also confirm that Team Admins can manage roles (the source says the Manage members permission was previously given to Team Admin and Org Owner roles, and that team and org admins can create roles only in the teams where they are admins). -->
