---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere utenti ad Adobe Workfront Fusion tramite Adobe Admin Console
description: È possibile aggiungere un utente a Adobe Admin Console e assegnarlo ad Adobe Workfront Fusion oppure assegnare un utente esistente in Adobe Admin Console a Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# Aggiungere utenti ad Adobe Workfront Fusion tramite Adobe Admin Console

È possibile aggiungere un utente a [!DNL Adobe Admin Console] e assegnarlo ad Adobe Workfront Fusion oppure assegnare un utente esistente in [!DNL Adobe Admin Console] a Workfront Fusion.

Per un video che descrive Workfront Fusion in [!DNL Adobe Admin Console] e spiega come aggiungere utenti, vedi [[!DNL Fusion] su Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
  </tr>
   <tr> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td>Devi essere amministratore della configurazione del prodotto dei prodotti Adobe per la tua organizzazione.</td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Prerequisiti

Prima di utilizzare [!DNL Admin Console] per Workfront, è necessario ricevere un&#39;e-mail di invito alla console.

1. Se sei alle prime armi con [!DNL Adobe] e hai ricevuto un&#39;e-mail che ti informa che ora disponi dei diritti di amministrazione per gestire software e servizi [!DNL Adobe] per la tua organizzazione, fai clic sul pulsante nell&#39;e-mail per creare un account [!DNL Adobe] e aprire [!DNL Admin Console].

   Oppure

   Se disponi già di un account Adobe, passa alla [[!DNL Adobe Admin Console] pagina](https://adminconsole.adobe.com).


## Aggiungere un nuovo utente a [!DNL Adobe Admin Console] e Workfront Fusion

1. Dalla [[!DNL Adobe Admin Console] pagina](https://adminconsole.adobe.com/), seleziona la scheda **[!UICONTROL Prodotti]** nella barra di navigazione superiore, quindi fai clic sul riquadro del prodotto **Workfront Fusion**.

   ![Fusione in Admin Console](assets/fusion-product-admin-console.png)

1. Nell’elenco visualizzato, seleziona l’organizzazione in cui desideri aggiungere un utente.

   ![Istanza Fusion in Admin Console](assets/fusion-instances-admin-console.png)

1. Nell&#39;elenco visualizzato, con la scheda **[!UICONTROL Profili di prodotto]** selezionata, fare clic sul collegamento [!UICONTROL Profilo di prodotto] di Workfront Fusion.

   >[!IMPORTANT]
   >
   > Non apportare modifiche al [!UICONTROL profilo di prodotto] stesso.

1. Con la scheda **[!UICONTROL Utenti]** selezionata sopra l&#39;elenco, fare clic su **[!UICONTROL Aggiungi utente]**.

1. Nella casella **[!UICONTROL Aggiungi utenti a questo profilo di prodotto]**, immetti l&#39;indirizzo e-mail o il nome di un utente che desideri aggiungere, quindi seleziona l&#39;utente nell&#39;elenco visualizzato.

1. Fai clic su **[!UICONTROL Salva]**.

   L&#39;utente viene creato in Workfront Fusion.

1. (Facoltativo) Continua con [Modifica il livello di accesso di un utente in Workfront Fusion](#change-a-users-access-level-in-workfront-fusion)

## Modificare il livello di accesso di un utente in Workfront Fusion

* [Cambia il ruolo di un utente in Amministratore](#change-a-users-role-to-admin)
* [Modificare il ruolo di un utente in Membro, Contabile o Sviluppatore app](#change-a-users-role-to-member-accountant-or-app-developer)

### Cambia il ruolo di un utente in Amministratore

L&#39;assegnazione di un ruolo di amministratore a un utente deve essere eseguita in [!DNL Adobe Admin Console].

1. Nella pagina del [!UICONTROL profilo di prodotto] di Workfront Fusion in cui hai aggiunto l&#39;utente, seleziona la scheda **[!UICONTROL Amministratori]**.

1. Fai clic su **[!UICONTROL Aggiungi amministratore]**.

1. Nella casella **[!UICONTROL Aggiungi amministratori del profilo di prodotto]**, inserisci l&#39;indirizzo e-mail o il nome dell&#39;utente che desideri diventare amministratore, quindi seleziona l&#39;utente nell&#39;elenco visualizzato.

1. Fai clic su **[!UICONTROL Salva]**.

   L&#39;utente è ora amministratore in Workfront Fusion.

### Modificare il ruolo di un utente in Membro, Contabile o Sviluppatore app

I ruoli Membro, Contabile e Sviluppatore app vengono gestiti all’interno di Workfront Fusion.

Per istruzioni, vedere [Visualizzare o modificare i ruoli utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Assegnare un utente esistente in [!DNL Adobe Admin Console] a Workfront Fusion

È possibile aggiungere un utente esistente a un team in Fusion. Questa operazione viene gestita all&#39;interno di Fusion.

Per istruzioni, vedere [Aggiungere un utente a un team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
