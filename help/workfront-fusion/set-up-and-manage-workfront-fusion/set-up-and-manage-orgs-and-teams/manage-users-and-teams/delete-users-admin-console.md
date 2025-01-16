---
content-type: reference
title: 'Configurazione e gestione di organizzazioni e team: indice degli articoli'
description: Questa sezione contiene articoli relativi alla configurazione e alla gestione di organizzazioni e team in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Elimina utenti tramite [!DNL Adobe Admin Console]

È possibile rimuovere un utente solo da [!DNL Adobe Workfront Fusion], lasciando l&#39;accesso a qualsiasi altro profilo di prodotto [!DNL Adobe], oppure è possibile rimuovere completamente l&#39;utente da [!DNL Adobe Admin Console].

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
     <p>Devi essere un amministratore [!DNL Adobe Admin Console] per la tua organizzazione.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Rimuovi un utente solo da [!DNL Adobe Workfront Fusion]

È possibile rimuovere un utente da Workfront Fusion lasciando intatte le altre autorizzazioni di prodotto di Adobe.

Per istruzioni, vedere &quot;Rimuovere utenti e gruppi di utenti da un prodotto&quot; nell&#39;articolo [Gestire i prodotti nell&#39;Admin Console](https://helpx.adobe.com/enterprise/using/manage-products.html).

## Disattivare un utente in tutti i prodotti in [!DNL Adobe Admin Console]

Per eliminare un utente, è necessario disattivarlo tramite [!DNL Adobe Admin Console].

Un utente viene disattivato da [!DNL Adobe Admin Console] quando si verifica una delle condizioni seguenti:

* L’utente viene spostato da un prodotto o profilo di prodotto e non viene assegnato ad alcun altro prodotto o profilo di prodotto.
* L’utente viene rimosso da un gruppo collegato a un profilo di prodotto e non viene incluso in alcun altro gruppo collegato a un profilo di prodotto.
* L’utente viene rimosso da un profilo di prodotto e non viene assegnato a un altro profilo di prodotto.
* L’utente viene eliminato o disattivato nell’organizzazione che include Workfront Fusion.

  Per istruzioni, vedere la sezione &quot;Rimuovere utenti&quot; in [Gestire gli utenti singolarmente](https://helpx.adobe.com/enterprise/using/manage-users-individually.html).

In [!DNL Workfront Fusion], la disattivazione interessa l&#39;utente in uno dei seguenti modi:

* Se l’utente fa parte di una sola organizzazione, viene disattivato.
* Se l&#39;utente fa parte di più organizzazioni, viene rimosso da quella in cui è stato modificato l&#39;utente in [!DNL Adobe Admin Console].
* Quando elimini un utente, considera quanto segue.

### Considerazioni durante l’eliminazione di un utente in Workfront Fusion

Quando elimini un utente, considera quanto segue.

* Quando un utente viene eliminato, le connessioni, le chiavi e i webhook dell’utente vengono rimossi.
* Eventuali scenari appartenenti all’utente vengono trasferiti al proprietario dell’organizzazione. Le connessioni in questi scenari devono essere aggiornate, perché le connessioni appartenenti all’utente non sono più valide.
* Se l’utente eliminato è proprietario di applicazioni o modelli pubblici, le applicazioni o i modelli pubblici vengono trasferiti al proprietario dell’organizzazione. Se non è presente un proprietario dell’organizzazione, le applicazioni o i modelli pubblici vengono trasferiti a un altro utente.
