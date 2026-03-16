---
title: Gestire gli utenti di Adobe Workfront Fusion all’interno dell’organizzazione
description: Gestire gli utenti di Adobe Workfront Fusion all’interno dell’organizzazione
author: Becky
feature: Workfront Fusion
exl-id: 32c221fa-856b-4921-9fa6-5e60f2aa08cd
source-git-commit: 3f9390d8947ef2666336c1a4cc6eab8d174849d5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 18%

---

# Visualizzare o modificare i ruoli degli utenti

Gli amministratori di Adobe Workfront Fusion possono gestire i ruoli utente all’interno di Workfront Fusion.


>[!NOTE]
>
>Se la tua organizzazione è attualmente in fase di trasferimento al Adobe Admin Console, non puoi gestire gli utenti in Workfront (aggiunta o eliminazione di utenti). Puoi eseguire queste azioni in Adobe Admin Console al termine della migrazione.

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Visualizzare o modificare i ruoli utente di un&#39;organizzazione

Gli amministratori di Adobe Workfront Fusion possono visualizzare e aggiornare i ruoli utente di un’organizzazione.

1. Dopo aver effettuato l&#39;accesso come amministratore di Workfront Fusion, selezionare **[!UICONTROL Tutti gli utenti]** nell&#39;area di navigazione a sinistra.
1. Fare clic su **[!UICONTROL Dettagli]** nella riga dell&#39;utente che si desidera visualizzare.
1. (Facoltativo) Per aggiornare il ruolo dell&#39;utente in un&#39;organizzazione, fare clic sul menu a discesa nella colonna **[!DNL Role]** nella riga dell&#39;organizzazione in cui si desidera modificare il ruolo dell&#39;utente, quindi selezionare il nuovo ruolo.

### Considerazioni durante l’aggiunta o la modifica dei proprietari dell’organizzazione

La tua organizzazione può avere più di un proprietario.

Quando si assegna un utente a o da un ruolo Proprietario, tenere presente quanto segue.

* Solo un proprietario può assegnare il ruolo Proprietario o assegnare un altro ruolo a un proprietario corrente.
* Solo gli amministratori possono essere aggiornati a Proprietario.
* Se esiste un solo proprietario, il ruolo di proprietario non può essere modificato o rimosso.
* Se esiste un solo proprietario, non è possibile eliminarlo se nell’organizzazione sono presenti altri utenti.
* Quando a un amministratore viene assegnato il ruolo di Proprietario, diventa automaticamente Amministratore in tutti i team all’interno dell’organizzazione.
* Quando un proprietario viene assegnato a un altro ruolo, tale utente diventa automaticamente un membro del team in tutti i team.
* Quando viene creato un nuovo team, tutti i proprietari vengono automaticamente assegnati come amministratori del team.

## Visualizzare o modificare i ruoli utente per un team

Gli amministratori di Adobe Workfront Fusion e gli amministratori del team possono visualizzare e aggiornare i ruoli utente.

1. Dopo aver effettuato l&#39;accesso come amministratore di Workfront Fusion, selezionare **[!UICONTROL Tutti gli utenti]** nell&#39;area di navigazione a sinistra.
1. Fare clic su **[!UICONTROL Dettagli]** nella riga dell&#39;utente che si desidera visualizzare.
1. Fare clic sull&#39;icona Team nella colonna **[!DNL Role]** nella riga dell&#39;organizzazione che contiene il team in cui si desidera visualizzare o modificare il ruolo dell&#39;utente.
1. (Facoltativo) Per aggiornare il ruolo dell&#39;utente in un team, fare clic sul menu a discesa nella colonna **[!DNL Role]** nella riga del team in cui si desidera modificare il ruolo dell&#39;utente, quindi selezionare il nuovo ruolo.
