---
title: Visualizzare e gestire i ruoli del team
description: Ogni team dispone di una scheda Ruoli in cui è possibile visualizzare i ruoli del team, creare ruoli personalizzati, scegliere le autorizzazioni incluse in ogni ruolo e aggiornare o eliminare i ruoli.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 10%
---
# Visualizzare e gestire i ruoli del team

Puoi visualizzare i ruoli disponibili in un team, creare ruoli personalizzati e scegliere quali autorizzazioni includere in ogni ruolo. Puoi anche aggiornare ed eliminare i ruoli.

I ruoli personalizzati offrono i seguenti vantaggi:

* Ogni membro del team ha solo l’accesso necessario al proprio lavoro, riducendo il rischio di modifiche accidentali a scenari critici.
* I ruoli personalizzati possono corrispondere meglio al funzionamento dell’organizzazione, anziché adattare i team ai ruoli predefiniti.
* Puoi gestire autonomamente l’accesso senza contattare il supporto tecnico.

Per una panoramica delle organizzazioni, dei team e dei ruoli di team predefiniti, vedere [Panoramica dell&#39;organizzazione e del team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md). Per le autorizzazioni incluse nei ruoli predefiniti, vedere [Ruoli organizzazione e team](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td> 
     <p>È necessario disporre dell'autorizzazione <b>[!UICONTROL Gestisci membri]</b> nel team. Nei ruoli predefiniti, questa autorizzazione è inclusa nei ruoli Amministratore team e Proprietario organizzazione.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Chi può gestire i ruoli del team

Chiunque disponga dell&#39;autorizzazione **[!UICONTROL Gestione membri]** in un team può creare, aggiornare, eliminare e assegnare gli utenti ai ruoli del team.

* I proprietari dell’organizzazione possono creare e gestire ruoli in tutti i team.
* Gli amministratori dell&#39;organizzazione possono gestire i ruoli solo nei team di cui sono membri e in cui dispongono dell&#39;autorizzazione **[!UICONTROL Gestisci membri]**.
* Gli amministratori del team possono gestire i ruoli nei propri team.

## Creare o modificare un ruolo

1. In Fusion, nel menu di navigazione a sinistra, fai clic su **Panoramica team**.
1. (Condizionale) Se non ti trovi nella pagina del team per il quale desideri visualizzare i ruoli, fai clic sul menu a discesa **Team** nella parte superiore della pagina e seleziona il team corretto.
1. Apri la scheda **[!UICONTROL Ruoli]**.

   Nella scheda sono elencati i ruoli disponibili nel team, inclusi quelli predefiniti. Per ogni ruolo, l’elenco mostra il nome del ruolo e un riepilogo delle relative autorizzazioni, ad esempio &quot;Nessuna autorizzazione&quot;, &quot;Membro&quot; o &quot;Personalizzato · 19 autorizzazioni&quot;.

1. Per creare un ruolo, fare clic su **[!UICONTROL Crea ruolo]**.

   Oppure

   Per modificare un ruolo, fare clic su **[!UICONTROL Modifica]** nella riga del ruolo che si desidera modificare.

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. Immettere un nome per il ruolo nel campo **[!UICONTROL Nome ruolo]**.
1. Nel menu a discesa **[!UICONTROL Modello ruolo]**, seleziona il modello da cui vuoi iniziare.

   Il modello imposta le autorizzazioni iniziali per il ruolo. Il modello predefinito è **[!UICONTROL Visualizzatore]**.

1. Nell&#39;area **[!UICONTROL Autorizzazioni con ambito]**, selezionare le autorizzazioni che si desidera includere nel ruolo.

   Le autorizzazioni sono raggruppate per area, ad esempio **[!UICONTROL Automazioni]**, **[!UICONTROL Connessioni]** e **[!UICONTROL Team]**. Per ogni area, potete effettuare una delle seguenti operazioni:

   * Per impostare contemporaneamente tutte le autorizzazioni in un&#39;area, fare clic su **[!UICONTROL Nessun accesso]**, **[!UICONTROL Visualizza solo]** o **[!UICONTROL Accesso completo]** accanto al nome dell&#39;area.
   * Per scegliere autorizzazioni specifiche, seleziona o deseleziona la casella di controllo di ciascuna autorizzazione.

   Per un elenco delle autorizzazioni, vedere [Autorizzazioni che è possibile includere in un ruolo](#permissions-that-you-can-include-in-a-role) in questo articolo.

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. Fai clic su **[!UICONTROL Salva]**. Per chiudere la pagina senza salvare, fare clic su **[!UICONTROL Annulla]**.
1. (Facoltativo) Per eliminare un ruolo, fare clic su **[!UICONTROL Elimina]** nella riga del ruolo nella scheda **[!UICONTROL Ruoli]**.

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

Un ruolo creato è disponibile nel team. Puoi assegnarlo ai membri del team.

### Autorizzazioni che è possibile includere in un ruolo

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>Area</th>
   <th>Autorizzazioni</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automations]</td>
   <td>Visualizza elenco, Visualizza dettagli, Visualizza cronologia esecuzioni, Gestisci notifiche, Reimposta statistiche, Esegui una volta, Modifica pianificazione, Attiva, Disattiva, Crea, Modifica, Pubblica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL esecuzioni incomplete]</td>
   <td>Visualizza, Gestisci</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhook]</td>
   <td>Visualizza, Visualizza coda, Crea, Modifica, Gestisci coda, Modifica priorità, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Connessioni]</td>
   <td>Visualizza, Crea, Modifica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Keys]</td>
   <td>Visualizza, Crea, Modifica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Data Store]</td>
   <td>Visualizza elenco, Sfoglia record, Crea, Modifica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Strutture dati]</td>
   <td>Visualizza, Crea, Modifica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Modelli]</td>
   <td>Visualizza elenco, Visualizza dettagli, Crea, Modifica, Elimina</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Team]</td>
   <td>Visualizzare il team, modificare le impostazioni del team, gestire i membri, eliminare il team</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## Clona i ruoli in un altro team

È possibile copiare i ruoli di un team in un altro team, in modo da non dover ricreare gli stessi ruoli in ogni team.

1. Apri la scheda **[!UICONTROL Ruoli]** del team, come descritto in [Crea o modifica un ruolo](#create-or-edit-a-role) in questo articolo.
1. Fai clic su **[!UICONTROL Clona nel team]**.

   Viene visualizzata la pagina **[!UICONTROL Clona ruoli in un altro team]**.

1. Nel menu a discesa **[!UICONTROL Team di destinazione]**, seleziona il team a cui desideri clonare i ruoli.

   Viene visualizzata una tabella in cui sono elencati i ruoli del team corrente.

1. Per ogni ruolo nella tabella, esaminare e impostare quanto segue:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Ruolo Source]</td> 
      <td> <p>Il ruolo nel team corrente, con un riepilogo delle relative autorizzazioni.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Azione]</td> 
      <td> <p>Cosa fare con il ruolo. Ad esempio, <b>[!UICONTROL Copia nel ruolo esistente]</b> copia le autorizzazioni del ruolo di origine in un ruolo già esistente nel team di destinazione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Target]</td> 
      <td> <p>Ruolo nel team di destinazione in cui viene copiato il ruolo di origine.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Changes]</td> 
      <td> <p>Se il ruolo di destinazione è diverso dal ruolo di origine. Ad esempio, <b>[!UICONTROL già sincronizzato]</b> significa che il ruolo di destinazione dispone già delle stesse autorizzazioni del ruolo di origine.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Utenti]</td> 
      <td> <p>Informazioni sugli utenti che hanno il ruolo. Ad esempio, <b>[!UICONTROL Nessun utente corrispondente]</b> significa che non sono presenti utenti da includere.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Stato]</td> 
      <td> <p>Risultato del ruolo dopo la clonazione.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fare clic su **[!UICONTROL Clona]**. Per chiudere la pagina senza clonazione, fare clic su **[!UICONTROL Annulla]**.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## Assegnare un ruolo a un utente

È possibile assegnare un ruolo personalizzato nello stesso modo in cui si assegna un ruolo predefinito. Per istruzioni, vedere [Aggiungere un utente a un team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) e [Visualizzare o modificare i ruoli utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team).

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## Considerazioni

* Autorizzazioni di organizzazione a catena. Per consentire a un utente di eseguire un&#39;azione in tutti i team, assegnare un ruolo dell&#39;organizzazione anziché creare un ruolo del team. Per ulteriori informazioni, vedere [Ruoli organizzazione e team](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).
* I ruoli creati appartengono a un unico team.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
