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
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 2%

---

# Aggiungere utenti ad Adobe Workfront Fusion tramite Adobe Admin Console

È possibile aggiungere un utente a [!DNL Adobe Admin Console] e assegnarlo ad Adobe Workfront Fusion oppure assegnare un utente esistente in [!DNL Adobe Admin Console] a Workfront Fusion.

Per un video che descrive Workfront Fusion in [!DNL Adobe Admin Console] e spiega come aggiungere utenti, vedi [[!DNL Fusion] su Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Piano Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Pro] o versione successiva</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito di licenza corrente: nessun requisito di licenza per Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno corrente del prodotto: se disponi del piano Adobe Workfront [!UICONTROL Select] o [!UICONTROL Prime], per utilizzare le funzionalità descritte in questo articolo la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront. Workfront Fusion è incluso nel piano Workfront di [!UICONTROL Ultimate].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: per utilizzare le funzionalità descritte in questo articolo, la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] diritti di amministratore</td> 
   <td>Devi essere un [!UICONTROL Product Configuration Administrator] di [!DNL Adobe] prodotti per la tua organizzazione.</td> 
  </tr>
  </tbody> 
</table>

&#42;Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore di Workfront.

&#42;&#42;Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
