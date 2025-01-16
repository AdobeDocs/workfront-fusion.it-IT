---
title: Crittografia
description: I moduli di Adobe Workfront Fusion Encryptor consentono di crittografare qualsiasi dato di testo. Attualmente supportano la crittografia dei messaggi tramite AES256 e PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# Crittografia

I moduli [!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] ti consentono di crittografare qualsiasi dato di testo. Attualmente supportano la crittografia dei messaggi tramite AES256 e PGP ([!UICONTROL OpenPGP]).

## Requisiti di accesso

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
   <p>Requisito licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione lavoro, [!UICONTROL [!DNL Workfront Fusion] per automazione lavoro</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Crittografia e decrittografia dei messaggi tramite PGP

Durante la crittografia e la decrittografia tramite PGP, è necessario utilizzare un portachiavi e creare una chiave privata o pubblica (o entrambe).

Per ulteriori informazioni sulle chiavi pubbliche e private, vedere [Glossario di Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md). <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor] moduli e relativi campi

Durante la configurazione di [!UICONTROL Encryptor] moduli, vengono visualizzati i campi seguenti. Un titolo in grassetto in un modulo indica un campo obbligatorio.

### Crittografare un messaggio PGP

Questo modulo consente di crittografare un messaggio utilizzando chiavi pubbliche e private.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Immetti la chiave privata del mittente. Questa operazione può autenticare l’identità del mittente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Immetti la chiave pubblica del destinatario.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Immetti il messaggio da crittografare.</td>
    </tr>

### Decrittare un messaggio PGP

Questo modulo consente di decrittografare un messaggio utilizzando chiavi pubbliche e private.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Immetti la chiave privata del destinatario.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Immetti la chiave pubblica del destinatario. Questa operazione può autenticare l’identità del mittente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Mappa il messaggio da decrittografare.</td>
    </tr>
</table>
