---
title: Panoramica sulle organizzazioni e sui team di Fusion
description: Le funzioni Organizzazione e Team di Adobe Workfront Fusion consentono alle aziende di controllare l'accesso a scenari e altre funzioni all'interno di Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 44e6de2a-b2d3-410d-abc3-10facd258495
source-git-commit: 4cd97fe2924150b9e7be140a25215f135b2788da
workflow-type: tm+mt
source-wordcount: '549'
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

* Situazioni che potrebbero verificarsi con
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
