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
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# Aggiungere utenti ad Adobe Workfront Fusion tramite Adobe Admin Console

È possibile aggiungere un utente a [!DNL Adobe Admin Console] e assegnarlo a [!DNL Adobe Workfront Fusion] oppure assegnare un utente esistente in [!DNL Adobe Admin Console] a [!DNL Workfront Fusion].

Per un video che descrive [!DNL Workfront Fusion] in [!DNL Adobe Admin Console], incluso come aggiungere utenti, vedi [[!DNL Fusion] su Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td> 
   <td> <p>[!UICONTROL Pro] o superiore</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] diritti di amministratore</td> 
   <td>Devi essere un [!UICONTROL Product Configuration Administrator] di [!DNL Adobe] prodotti per la tua organizzazione.</td> 
  </tr>
  </tbody> 
</table>

&#42;Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore [!DNL Workfront].

&#42;&#42;Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza</td> 
   <td> <p>Nuovo: [!UICONTROL Standard]</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] piano: [!DNL Workfront Fusion] incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per la tua organizzazione.</p>
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Prerequisiti

Prima di utilizzare [!DNL Admin Console] per [!DNL Workfront], è necessario ricevere un&#39;e-mail di invito alla console.

1. Se sei alle prime armi con [!DNL Adobe] e hai ricevuto un&#39;e-mail che ti informa che ora disponi dei diritti di amministrazione per gestire software e servizi [!DNL Adobe] per la tua organizzazione, fai clic sul pulsante nell&#39;e-mail per creare un account [!DNL Adobe] e aprire [!DNL Admin Console].

   Oppure

   Se hai già un account Adobe, passa alla [[!DNL Adobe Admin Console] pagina](https://adminconsole.adobe.com).


## Aggiungi un nuovo utente a [!DNL Adobe Admin Console] e [!DNL Workfront Fusion]

1. Dalla [[!DNL Adobe Admin Console] pagina](https://adminconsole.adobe.com/), seleziona la scheda **[!UICONTROL Products]** nella barra di navigazione superiore, quindi fai clic sul riquadro del prodotto **[!DNL Workfront Fusion]**.

   ![Fusione in Admin Console](assets/fusion-product-admin-console.png)

1. Nell’elenco visualizzato, seleziona l’organizzazione in cui desideri aggiungere un utente.

   ![Istanza Fusion in Admin Console](assets/fusion-instances-admin-console.png)

1. Nell&#39;elenco visualizzato, con la scheda **[!UICONTROL Product Profiles]** selezionata, fare clic sul nome del collegamento [!DNL Workfront Fusion] [!UICONTROL Product Profile].

   >[!IMPORTANT]
   >
   > Non apportare modifiche a [!UICONTROL Product Profile].

1. Con la scheda **[!UICONTROL Users]** selezionata sopra l&#39;elenco, fare clic su **[!UICONTROL Add User]**.

1. Nella casella **[!UICONTROL Add users to this product profile]** immettere l&#39;indirizzo di posta elettronica o il nome di un utente che si desidera aggiungere, quindi selezionare l&#39;utente nell&#39;elenco visualizzato.

1. Fare clic su **[!UICONTROL Save]**.

   L&#39;utente è stato creato in [!DNL Workfront Fusion].

1. (Facoltativo) Continua con [Modifica il livello di accesso di un utente in [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion)

## Modificare il livello di accesso di un utente in Workfront Fusion

* [Cambia il ruolo di un utente in Amministratore](#change-a-users-role-to-admin)
* [Modificare il ruolo di un utente in Membro, Contabile o Sviluppatore app](#change-a-users-role-to-member-accountant-or-app-developer)

### Cambia il ruolo di un utente in Amministratore

L&#39;assegnazione di un ruolo di amministratore a un utente deve essere eseguita in [!DNL Adobe Admin Console].

1. Nella pagina [!DNL Workfront Fusion] [!UICONTROL Product Profile] in cui è stato aggiunto l&#39;utente, selezionare la scheda **[!UICONTROL Admins]**.

1. Fare clic su **[!UICONTROL Add Admin]**.

1. Nella casella **[!UICONTROL Add product profile administrators]** immettere l&#39;indirizzo di posta elettronica o il nome dell&#39;utente che si desidera diventare amministratore, quindi selezionare l&#39;utente nell&#39;elenco visualizzato.

1. Fare clic su **[!UICONTROL Save]**.

   L&#39;utente è ora un amministratore in [!DNL Workfront Fusion].

### Modificare il ruolo di un utente in Membro, Contabile o Sviluppatore app

I ruoli Membro, Contabile e Sviluppatore app vengono gestiti all’interno di Workfront Fusion.

Per istruzioni, vedere [Visualizzare o modificare i ruoli utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Assegna un utente esistente in [!DNL Adobe Admin Console] a [!DNL Workfront Fusion]

È possibile aggiungere un utente esistente a un team in Fusion. Questa operazione viene gestita all&#39;interno di Fusion.

Per istruzioni, vedere [Aggiungere un utente a un team](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
