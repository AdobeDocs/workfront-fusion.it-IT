---
content-type: reference
title: 'Set up and managing organizations and teams: article index'
description: This section contains articles related to setting up and managing organizations and teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 21%

---

# Delete users through the [!DNL Adobe Admin Console]

You can remove a user from Adobe Workfront Fusion only, leaving access to any other [!DNL Adobe] product profiles, or you can remove the user from the [!DNL Adobe Admin Console] entirely.

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
     <p>You must be an Adobe Admin Console administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Remove a user from Adobe Workfront Fusion only

You can remove a user from Workfront Fusion while leaving their other Adobe product permissions intact.

For instructions, see &quot;Remove users and user groups from a product&quot; in the article [Manage products on Admin Console](https://helpx.adobe.com/it/enterprise/using/manage-products.html).

## Deactivate a user in all products in the [!DNL Adobe Admin Console]

To delete a user, you must deactivate the user through the [!DNL Adobe Admin Console].

A user is deactivated from the [!DNL Adobe Admin Console] when one of the following applies:

* The user is moved out from a product or product profile, and are not assigned to any other product or product profile.
* The user is removed from a group that is linked to a product profile, and is not included in any other group linked to a product profile.
* The user is removed from a product profile and is not assigned to another product profile.
* The user is deleted or deactivated in the organization that includes Workfront Fusion.

  For instructions, see the section &quot;Remove users&quot; in [Manage users individually](https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html).

In Workfront Fusion, the deactivation affects the user in one of the following ways:

* If the user is in only one organization, the user is deactivated.
* If the user is in more than one organization, the user is removed from the organization that the user was modified in on the [!DNL Adobe Admin Console].

### Considerations when deleting a user in Workfront Fusion

Consider the following when deleting a user.

* When a user is deleted, the user&#39;s connections, keys, and webhooks are removed.
* Any scenarios belonging to the user are transferred to the organization Owner. The connections in these scenarios must be updated, because the connections belonging to the user are no longer valid.
* If the deleted user owns any applications or public templates, the applications or public templates are transferred to the organization Owner. If there is not an organization Owner, the applications or public templates are transferred to another user.
