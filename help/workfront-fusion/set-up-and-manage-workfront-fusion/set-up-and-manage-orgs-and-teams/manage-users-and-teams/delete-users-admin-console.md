---
content-type: reference
title: 'Configurazione e gestione di organizzazioni e team: indice degli articoli'
description: Questa sezione contiene articoli relativi alla configurazione e alla gestione di organizzazioni e team in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Elimina utenti tramite [!DNL Adobe Admin Console]

È possibile rimuovere un utente solo da Adobe Workfront Fusion, lasciando l&#39;accesso a qualsiasi altro profilo di prodotto [!DNL Adobe], oppure è possibile rimuovere completamente l&#39;utente da [!DNL Adobe Admin Console].

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
     <p>Devi essere un amministratore di Adobe Admin Console per la tua organizzazione.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Rimuovere un utente solo da Adobe Workfront Fusion

È possibile rimuovere un utente da Workfront Fusion lasciando intatte le altre autorizzazioni di prodotto di Adobe.

Per istruzioni, vedere &quot;Rimuovere utenti e gruppi di utenti da un prodotto&quot; nell&#39;articolo [Gestire prodotti in Admin Console](https://helpx.adobe.com/it/enterprise/using/manage-products.html).

## Disattivare un utente in tutti i prodotti in [!DNL Adobe Admin Console]

Per eliminare un utente, è necessario disattivarlo tramite [!DNL Adobe Admin Console].

Un utente viene disattivato da [!DNL Adobe Admin Console] quando si verifica una delle condizioni seguenti:

* L’utente viene spostato da un prodotto o profilo di prodotto e non viene assegnato ad alcun altro prodotto o profilo di prodotto.
* L’utente viene rimosso da un gruppo collegato a un profilo di prodotto e non viene incluso in alcun altro gruppo collegato a un profilo di prodotto.
* L’utente viene rimosso da un profilo di prodotto e non viene assegnato a un altro profilo di prodotto.
* L’utente viene eliminato o disattivato nell’organizzazione che include Workfront Fusion.

  Per istruzioni, vedere la sezione &quot;Rimuovere utenti&quot; in [Gestire gli utenti singolarmente](https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html).

In Workfront Fusion, la disattivazione influisce sull’utente in uno dei seguenti modi:

* Se l’utente fa parte di una sola organizzazione, viene disattivato.
* Se l&#39;utente fa parte di più organizzazioni, viene rimosso da quella in cui è stato modificato l&#39;utente in [!DNL Adobe Admin Console].
* Quando elimini un utente, considera quanto segue.

### Considerazioni durante l’eliminazione di un utente in Workfront Fusion

Quando elimini un utente, considera quanto segue.

* Quando un utente viene eliminato, le connessioni, le chiavi e i webhook dell’utente vengono rimossi.
* Eventuali scenari appartenenti all’utente vengono trasferiti al proprietario dell’organizzazione. Le connessioni in questi scenari devono essere aggiornate, perché le connessioni appartenenti all’utente non sono più valide.
* Se l’utente eliminato è proprietario di applicazioni o modelli pubblici, le applicazioni o i modelli pubblici vengono trasferiti al proprietario dell’organizzazione. Se non è presente un proprietario dell’organizzazione, le applicazioni o i modelli pubblici vengono trasferiti a un altro utente.
