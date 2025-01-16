---
content-type: reference
title: Approvare o disapprovare i modelli
description: Questo articolo descrive come approvare o disapprovare i modelli di Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: 23e9f383b25c7b3789c413e557b94418e48a636b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%

---

# Approvare o disapprovare i modelli per la scheda Pubblico

I modelli di Adobe Workfront Fusion sono scenari predefiniti progettati per automatizzare e semplificare vari flussi di lavoro. Questi modelli possono aiutare gli utenti a configurare rapidamente integrazioni e automazioni senza dover creare nulla.

Gli amministratori possono scegliere se condividere o meno determinati modelli con l&#39;intera organizzazione nella scheda Modelli pubblici.

Gli utenti possono inviare i modelli creati per l’approvazione e condividerli nella pagina Modelli pubblici. <!--do the have to be requested or can an admin just choose to approve?-->

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] piano</td>
      <td><p>Qualsiasi</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] licenza</td>
      <td><p>Nuovo: [!UICONTROL Standard]</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td>
      <td>
        <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
        <p>Oppure</p>
        <p>Legacy: qualsiasi</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Prodotto</td>
      <td>
        <p>Nuovo:</p>
        <ul>
          <li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] Piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Il piano [!DNL Workfront Fusion] è incluso.</li>
        </ul>
        <p>Oppure</p>
        <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## Approva o disapprova [!DNL Workfront Fusion] modelli

L&#39;approvazione di un modello lo rende visibile nella scheda [!UICONTROL Public templates] e disponibile a tutti gli utenti.

Se si disapprova un modello, questo viene rimosso dalla scheda [!UICONTROL Public templates] e reso disponibile solo al team che lo ha creato.

1. Fare clic su **[!UICONTROL Administration]** nel pannello di navigazione a sinistra per aprire l&#39;area [!UICONTROL Administration].
1. Fare clic su **[!UICONTROL Templates]** nel pannello di navigazione a sinistra.
1. Per approvare un modello, fare clic su **[!UICONTROL Approve]** a destra del modello.
1. Per disapprovare un modello, fare clic su **[!UICONTROL Disapprove]** a destra del modello.

>[!NOTE]
>
>Se approvi il modello precedentemente approvato e quindi modificato, la seconda approvazione sovrascriverà il modello originale.


## Stati dei modelli

Puoi controllare lo stato nella pagina del modello sotto il nome del modello.

Sono disponibili i seguenti stati:

* **[!UICONTROL Private]**: questo modello è visibile solo per l&#39;autore del modello e il relativo team.
* **[!UICONTROL Published]**: questo modello è visibile solo per l&#39;autore del modello e il relativo team. Dopo la pubblicazione, se necessario, puoi inviare il modello per l’approvazione. È inoltre possibile copiare un collegamento condivisibile.
* **[!UICONTROL Approved]**: questo modello è visibile per tutti gli utenti di Workfront Fusion nella scheda [!UICONTROL Public templates]. È inoltre possibile copiare un collegamento condivisibile facendo clic su [!UICONTROL Options] nell&#39;angolo superiore destro dello schermo.

È inoltre possibile controllare lo stato dalla scheda [!UICONTROL Team templates]. Se un modello viene pubblicato, a destra del nome del modello è presente un&#39;icona.

* **Icona dell&#39;occhio**: il modello è pubblicato, è visibile solo per il team e non è stata inviata una richiesta di approvazione.
* **Icona segno di spunta giallo**: il modello è pubblicato, è visibile solo per il team ed è in attesa di approvazione per essere aggiunto alla scheda Modelli pubblici.
* **Icona segno di spunta verde**: il modello è disponibile nella scheda Modelli pubblici ed è visibile per qualsiasi utente di Workfront Fusion. È ancora visibile nella scheda [!UICONTROL Team templates]. L’autore del modello o il suo membro del team può comunque modificarlo.

I modelli senza icone hanno lo stato [!UICONTROL Private]. Non vengono pubblicati e sono visibili solo al team.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
