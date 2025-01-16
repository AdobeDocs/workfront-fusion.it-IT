---
title: Moduli CRM HubSpot
description: I moduli di gestione delle relazioni con i clienti HubSpot  [!DNL Adobe Workfront Fusion]  consentono di monitorare eventi, record, contatti, accordi, invii di file e moduli oppure di creare, recuperare, aggiornare ed eliminare record, contatti, accordi, eventi o file nel tuo account  [!DNL HubSpot CRM] .
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '5655'
ht-degree: 0%

---

# [!DNL HubSpot CRM] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM] consentono di monitorare eventi, record, contatti, accordi, invii di file e moduli oppure di creare, recuperare, aggiornare ed eliminare record, contatti, accordi, eventi o file nell&#39;account [!DNL HubSpot CRM].

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
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
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

## Prerequisiti

Per utilizzare i moduli [!DNL HubSpot CRM], è necessario disporre di un account [!DNL HubSpot CRM].

## Informazioni API CRM HubSpot

Il connettore CRM HubSpot utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Adobe Workfront Fusion] a [!DNL HubSpot CRM]

Per istruzioni sulla connessione dell&#39;account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere [Creare una connessione a  [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Durante la configurazione di una connessione, selezionare il tipo di connessione **CRM HubSpot**. Il tipo di CRM HubSpot (obsoleto) supporta le connessioni esistenti, ma si sconsiglia di utilizzarlo per creare nuove connessioni.

## [!DNL HubSpot CRM] moduli e relativi campi

Quando configuri [!DNL Hubspot CRM] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Hubspot CRM], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Oggetti CRM](#crm-objects)
* [Record (offerte, contatti e società)](#records-deals-contacts-and-companies)
* [Conttati](#contacts)
* [Offerte](#deals)
* [Aziende](#companies)
* [Coinvolgimenti](#engagements)
* [Eventi e notifiche](#events-and-notifications)
* [File](#files)
* [Attività](#tasks)
* [Utenti](#users)
* [Biglietti](#tickets)
* [Moduli](#forms)
* [Social media (broadcast)](#social-media-broadcast)
* [Post di blog](#blog-posts)
  <!--* [Workflows]-->
* [Iscrizioni](#subscriptions)
  <!--* [Associations](#associations)-->
* [Altro](#other)

+++**oggetti CRM**

### Oggetti CRM

* [Cerca oggetti CRM](#search-for-crm-objects)
* [Osserva oggetti CRM](#watch-crm-objects)

#### [!UICONTROL Search for CRM Objects]

Questo modulo di ricerca cerca oggetti CRM per proprietà personalizzate o per query. Per cercare prodotti o elementi riga, utilizza una connessione speciale con un ambito personalizzato richiesto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>Selezionare il tipo di oggetto CRM Hubspot che si desidera cercare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. I campi disponibili dipendono dall’oggetto selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>Seleziona la modalità di filtro della ricerca</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Immettere o mappare la query</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Immetti i gruppi o i filtri per la ricerca.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Fai clic su per ordinare i risultati. Se si sceglie di ordinare i risultati, vengono visualizzati i campi riportati di seguito. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>Selezionare la proprietà in base alla quale si desidera ordinare i risultati</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Scegliere se si desidera ordinare i risultati in senso crescente o decrescente.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset iniziale</td> 
    <td>Immetti o mappa l’ID del primo elemento per il quale desideri recuperare i dettagli. Questo modulo restituisce solo fino a 5000 risultati alla volta. Impostate un offset iniziale per recuperare elementi diversi dai primi 5000. Se l'offset iniziale è 5000, il modulo restituirà gli elementi da 5000 a 9999.</td> 
   </tr>
 </tbody> 
</table>

#### Osserva oggetti CRM

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un oggetto CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>Selezionare il tipo di oggetto che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selezionare le proprietà che si desidera includere nell'output per questo modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>Seleziona se desideri guardare gli oggetti creati (nuovi) o aggiornati (modificati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>Puoi aggiungere un filtro per garantire che lo scenario inizi solo quando vengono soddisfatte determinate condizioni.<ul><li><b>Query</b><p>Immettere la query in base alla quale si desidera filtrare.</li><li><b>Proprietà</b><p>Per ogni proprietà che si desidera utilizzare per filtrare i risultati, fare clic su <b>Aggiungi elemento</b> e immettere il nome, l'operatore e il valore della proprietà.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Record (offerte, contatti e società)**

### Record (offerte, contatti e società)

* [Crea un record](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [Elenca record](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)

#### Creare un record

Questo modulo di azione crea un contatto, una società o un&#39;offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Per ogni proprietà che si desidera aggiungere durante la creazione del record, selezionare il gruppo in cui si trova la proprietà. Il gruppo di proprietà si aprirà e potrai quindi inserire il valore delle proprietà. I gruppi di proprietà e le proprietà disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record (Legacy)]

Questo modulo di azione crea un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Immettere le proprietà che si desidera impostare per il record. I campi disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

Questo modulo di azione elimina un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selezionare il tipo di record che si desidera eliminare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'offerta che si desidera eliminare. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record]

Questo modulo di azione ottiene i dettagli di un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selezionare il tipo di record.</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>Se stai ricevendo un contatto, seleziona se desideri identificarlo per ID o per indirizzo e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'operazione che si desidera recuperare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Immetti l’indirizzo e-mail del contatto di cui desideri recuperare i dettagli. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record Property]

Questo modulo di azione ottiene i metadati per una proprietà record specifica in base al nome (interno).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selezionare il tipo di record con la proprietà per cui si desidera recuperare i metadati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>Seleziona la proprietà per la quale desideri recuperare i metadati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> Alcune proprietà dispongono di un set di opzioni disponibili che un utente può selezionare come valore della proprietà. Immetti l’ID dell’opzione che rappresenta il valore della proprietà da recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elenca record

Questo modulo di ricerca restituisce un elenco di contatti, aziende o offerte. La produzione è limitata a 5000 contatti, 12.500 aziende o 12.500 offerte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selezionare il tipo di record che si desidera restituire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selezionare le proprietà che si desidera includere nell'output per questo modulo.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr>

</tbody> 
</table>

#### [!UICONTROL Update a Record]

Questo modulo di azione aggiorna un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selezionare il tipo di record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>Se si sta ottenendo un contatto, selezionare la modalità di identificazione del record:</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'offerta che si desidera aggiornare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Immettere l'indirizzo di posta elettronica del contatto di cui si desidera aggiornare i dettagli. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Immettere le proprietà che si desidera impostare per il record. I campi disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Records]

Questo modulo di attivazione avvia uno scenario in cui un contatto, una società o un&#39;offerta è stata modificata o creata negli ultimi 30 giorni. L&#39;output è limitato a 10.000 record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Selezionare il tipo di record con la proprietà che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Specificare se si desidera controllare i record modificati di recente o creati di recente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selezionare le proprietà da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Contatti**

### Conttati

* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [Creare/aggiornare un contatto](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [Osservare i contatti aggiunti a un elenco](#watch-contacts-added-to-a-list)

#### [!UICONTROL Add Contacts to a List]

Questo modulo aggiunge a un elenco contatti i record contatto già creati nel sistema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selezionare l'ID dell'elenco a cui si desidera aggiungere il contatto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>Selezionare la modalità di identificazione dei contatti che si desidera aggiungere all'elenco:</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Aggiungere gli ID dei contatti che si desidera aggiungere all'elenco.</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>Aggiungere gli indirizzi di posta elettronica dei contatti che si desidera aggiungere all'elenco.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Crea/aggiorna un contatto

Questo modulo di azione crea un contatto se non esiste in un portale. Se il contatto esiste nel portale, questo modulo lo aggiorna con i valori forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Per ogni proprietà che si desidera aggiungere durante la creazione del contatto, selezionare il gruppo in cui si trova la proprietà. Il gruppo di proprietà si aprirà e sarà quindi possibile inserire i valori delle proprietà.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Contact (Legacy)]

Crea un contatto se non esiste già in un portale, oppure lo aggiorna con i valori delle proprietà più recenti se esiste già in un portale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Specificare le proprietà che si desidera impostare o aggiornare per il contatto. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Group of Contacts]

Crea un gruppo di contatti o li aggiorna se esistono già. Le prestazioni sono migliori quando la dimensione del batch è limitata a un massimo di 100 contatti. Le modifiche apportate tramite questo endpoint vengono elaborate in modo asincrono, pertanto l&#39;applicazione delle modifiche ai record dei contatti potrebbe richiedere alcuni minuti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>Aggiungi il batch di contatti.</p> <p>Fare clic su <strong>[!UICONTROL Add item]</strong> per aggiungere un nuovo contatto. Nella finestra visualizzata, inserire o mappare le seguenti informazioni:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>Selezionare la modalità di identificazione del contatto:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Immettere l'ID del contatto che si desidera creare o aggiornare. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Immetti l’indirizzo e-mail del contatto da creare o aggiornare. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Specificare le proprietà che si desidera impostare o aggiornare per il contatto.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Contacts]

Restituisce tutti i contatti creati nel portale. L&#39;output è limitato a 5000 contatti. Per elencare i contatti precedenti o successivi, è possibile utilizzare il parametro [!UICONTROL advanced] per eseguire l&#39;offset dell&#39;elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di contatti [!DNL Workfront Fusion] deve essere restituito durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID contatto [offset inizio] </td> 
    <td>Immetti o mappa l’ID dell’utente che desideri avviare l’elenco. Ad esempio, se si imposta l'ID contatto come ID del 101° contatto, il modulo potrà elencare i contatti 101-5100 anziché 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL List Contacts of a Company]

Recupera un elenco di contatti della società. L&#39;output è limitato a 5000 contatti. Per elencare i contatti precedenti o successivi, è possibile utilizzare il parametro [!UICONTROL advanced] per eseguire l&#39;offset dell&#39;elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID della società di cui si desidera elencare i contatti. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di contatti [!DNL Workfront Fusion] deve essere restituito durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID contatto [offset inizio] </td> 
    <td>Immetti o mappa l’ID dell’utente che desideri avviare l’elenco. Ad esempio, se si imposta l'ID contatto come ID del 101° contatto, il modulo potrà elencare i contatti 101-5100 anziché 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL Merge contacts]

Questo modulo di azione unisce i contatti

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>Immettere l'ID di uno dei contatti da unire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>Immettere l'ID dell'altro contatto che si desidera unire.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a Contact from a List]

Rimuove un contatto da un elenco contatti.

>[!NOTE]
>
>Non è possibile rimuovere manualmente i contatti da un elenco dinamico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Selezionare l'ID dell'elenco da cui si desidera rimuovere il contatto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>Immettere l'ID del contatto da rimuovere dall'elenco. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Contacts]

Recupera un elenco di contatti utilizzando la query di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Immettere la query di ricerca.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Immettere o mappare il numero massimo di contatti che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch contacts added to a list]

Questo modulo di attivazione avvia uno scenario quando un nuovo contatto viene aggiunto a un elenco. È disponibile solo per gli utenti con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Immettere o mappare l'ID dell'elenco contenente i contatti che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Selezionare le proprietà da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Offerte**

### Offerte

* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)

#### [!UICONTROL Get a Deal's CRM Pipeline]

Restituisce una pipeline di offerta specifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>Immetti o mappa l’ID della pipeline per la quale desideri recuperare i dettagli. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>Immetti o mappa l’ID della fase per cui desideri recuperare i dettagli. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Deal/Ticket Pipelines]

Restituisce tutte le pipeline di offerte e biglietti per un determinato portale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>Seleziona se desideri elencare offerte o biglietti.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Aziende**

### Aziende

#### [!UICONTROL Search for Companies by domain]

Recupera un elenco di aziende in base a una corrispondenza esatta con la proprietà del dominio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Immettere il dominio delle società da cercare, ad esempio <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di società [!DNL Workfront Fusion] deve essere restituito durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Coinvolgimenti**

### Coinvolgimenti

* [Associare un accordo a un oggetto CRM](#associate-an-engagement-with-a-crm-object)
* [Creare un coinvolgimento](#create-an-engagement)
* [Eliminare un coinvolgimento](#delete-an-engagement)
* [Guarda le interazioni](#watch-engagements)

#### Associare un accordo a un oggetto CRM

Questo modulo di azione associa un coinvolgimento a un contatto, a una società o a un affare.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selezionare il tipo di record di gestione delle relazioni con i clienti a cui si desidera associare un accordo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>Immettere o mappare l'ID del progetto che si desidera associare all'oggetto.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>Immettere o mappare l'ID del record a cui si desidera associare il coinvolgimento.</td> 
   </tr> 
 </tbody> 
</table>

#### Creare un coinvolgimento

Questo modulo di azione crea un coinvolgimento (ad esempio una nota, un’attività o un’attività) con un oggetto di gestione delle relazioni con i clienti in HubSpot. Gli engagement sono qualsiasi interazione con un contatto che deve essere registrato nel CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>Abilita questa opzione se il nuovo accordo sarà attivo al momento della creazione. Un impegno deve essere attivo per essere visualizzato nella timeline.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>Seleziona il tipo di coinvolgimento da creare.
  <ul>
  <li><b>E-mail</b><p></p>Passa a <a href="#email-metadata" class="MCXref xref" >Metadati e-mail</a>.</p></li>
  <li><b>Chiamata</b><p>Continua con <a href="#call-metadata" class="MCXref xref" >Chiamata metadati</a>.</p></li>
  <li><b>Riunione</b><p>Passa a <a href="#meeting-fields" class="MCXref xref" >Campi riunione</a>.</p></li>
  <li><b>Attività</b><p>Passa a <a href="#task-fields" class="MCXref xref" >Campi attività</a>.</p></li>
  <li><b>Nota</b><p>Nel campo Corpo immettere il testo della nota.</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Data/ora</td> 
   <td>Immetti o mappa un timestamp per il coinvolgimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID proprietario</td> 
   <td>Immettere o mappare l'ID proprietario della persona a cui verrà assegnato il progetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>Immetti o mappa un ID per il progetto, che può essere utilizzato tra tipi di oggetto diversi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID portale</td> 
   <td>Inserisci o mappa l’ID del portale. Questa funzione è utile se l’organizzazione dispone di più portali.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Contatti associati</td> 
   <td>Per ogni contatto a cui si desidera associare il progetto, fare clic su <b>Aggiungi elemento</b> e immettere l'ID contatto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Società associate</td> 
   <td>Per ogni società a cui si desidera associare il progetto, fare clic su <b>Aggiungi elemento</b> e immettere l'ID società.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Offerte associate</td> 
   <td>Per ogni offerta a cui si desidera associare questo accordo, fare clic su <b>Aggiungi elemento</b> e immettere l'ID offerta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ticket associati</td> 
   <td>Per ogni ticket a cui si desidera associare il progetto, fare clic su <b>Aggiungi elemento</b> e immettere l'ID ticket.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Allegati</td> 
   <td>Per ogni allegato a cui si desidera associare il progetto, fare clic su <b>Aggiungi elemento</b> e immettere l'ID file del file che si desidera allegare.</td> 
  </tr> 
 </tbody> 
</table>

##### Metadati e-mail

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail da cui verrà inviata l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Inserisci o mappa il nome della persona da cui verrà inviata l’e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>Inserisci o mappa il cognome della persona da cui verrà inviata l’e-mail.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">A</td> 
   <td>Per ogni indirizzo e-mail a cui desideri inviare l'e-mail, fai clic su <b>Aggiungi elemento</b> e immetti o mappa l'indirizzo e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cc</td> 
   <td>Per ogni indirizzo e-mail a cui desideri inviare il messaggio, fai clic su <b>Aggiungi elemento</b> e immetti o mappa l'indirizzo e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ccn</td> 
   <td>Per ogni indirizzo e-mail a cui desideri inviare il messaggio, fai clic su <b>Aggiungi elemento</b> e immetti o mappa l'indirizzo e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Oggetto</td> 
   <td>Inserisci o mappa il testo dell’oggetto e-mail</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>Per inviare un messaggio e-mail in formato HTML, immetti o mappa il corpo del messaggio, inclusi i HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Testo</td> 
   <td>Per inviare un messaggio e-mail di solo testo, immetti o mappa il testo del corpo del messaggio.</td> 
  </tr> 
 </tbody> 
</table>

##### Metadati della chiamata

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>Immettere o mappare il numero di telefono a cui verrà effettuata la chiamata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>Immettere o mappare il numero di telefono da cui verrà effettuata la chiamata.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>Seleziona lo stato della chiamata.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td>Immetti o mappa i dettagli o le note per la chiamata.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID esterno</td> 
   <td>Questo campo rappresenta l’ID interno di una chiamata effettuata in HubSpot. Non richiede alcuna azione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Durata</td> 
   <td>Immetti o mappa la lunghezza della chiamata in millisecondi</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID account esterno</td> 
   <td>Questo campo rappresenta l’ID account interno di una chiamata effettuata in HubSpot. Non richiede alcuna azione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL di registrazione</td> 
   <td>Immettere o mappare l'URL del file di registrazione.</td> 
  </tr> 
 </tbody> 
</table>

##### Campi riunione

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>Immettere o mappare il titolo o l'oggetto della riunione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Immettere o mappare il testo della descrizione o dei dettagli della riunione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>Immettere o mappare l'ora di inizio della riunione come timestamp UNIX.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Ora di fine</td> 
   <td>Immettere o mappare l'ora di fine della riunione come timestamp UNIX.</td> 
  </tr> 
 </tbody> 
</table>

##### Campi attività

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>Immettere o mappare il titolo o l'oggetto dell'attività.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Immettere o mappare il testo della descrizione o dei dettagli dell'attività.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stato</td> 
   <td>Selezionare lo stato dell'attività.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>Immettere <code>CONTACT</code> o <code>COMPANY</code>.
  </td> 
   </tr> 
 </tbody> 
</table>

#### Eliminare un coinvolgimento

Questo modulo di azione elimina un coinvolgimento in base al relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Immettere o mappare l'ID del progetto che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Guarda le interazioni

Questo modulo di attivazione avvia uno scenario quando viene creato un nuovo impegno in un portale. Questo modulo restituisce solo i record creati negli ultimi 30 giorni o gli ultimi 10.000 record creati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di società [!DNL Workfront Fusion] deve essere restituito durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Immetti o mappa la prima data per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Eventi e notifiche**

### Eventi e notifiche

* [Creare o aggiornare un evento timeline](#create--update-a-timeline-event)
* [Elencare i tipi di evento Timeline](#list-timeline-event-types)
* [Guarda gli eventi del calendario](#watch-calendar-events)
* [Notifiche Watch](#watch-notifications)

#### Creare o aggiornare un evento timeline

Questo modulo di azione crea o aggiorna un evento timeline. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Immetti o mappa l’ID dell’applicazione a cui appartiene questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Immetti o mappa un ID per questo evento. Gli ID evento non vengono generati dal sistema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>Inserisci o mappa l’ID del tipo di evento di questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Inserisci o mappa l’indirizzo e-mail del contatto per il quale stai creando l’evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>Inserisci o mappa l’ID del contatto per il quale stai creando l’evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>Immetti o mappa la marca temporale per questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>Per ogni elemento di dati personalizzati che si desidera aggiungere all'evento, fare clic su <b>Aggiungi elemento</b> e immettere il nome e il valore dell'elemento.</td> 
  </tr> 
 </tbody> 
</table>

#### Elencare i tipi di evento Timeline

Questo modulo di ricerca restituisce un elenco di tutti gli eventi della timeline per un’applicazione specifica. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Immetti o mappa l’ID dell’applicazione a cui appartengono questi eventi. </td> 
  </tr> 
 </tbody> 
</table>

#### Guarda gli eventi del calendario

Questo modulo di attivazione avvia uno scenario quando un nuovo evento viene aggiunto a un calendario. Include fino a 500 attività nell&#39;intervallo tra la data di inizio e la data di fine. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>Seleziona se desideri guardare eventi social, eventi di contenuto o tutti gli eventi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Immettere o mappare la data di inizio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Immettere o mappare la data di fine.</td> 
  </tr> 
 </tbody> 
</table>

#### Notifiche Watch

Questo modulo di attivazione avvia uno scenario quando viene inviata una nuova notifica sulle modifiche.  Include fino a 500 attività nell&#39;intervallo tra la data di inizio e la data di fine. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client. In HubSpot puoi avere un solo URL webhook per applicazione per sviluppatori.

Per creare un webhook per questo modulo, fai clic su **Aggiungi** accanto al campo del webhook e compila i campi seguenti:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Immettere l'ID applicazione da utilizzare per questo webhook. Puoi trovare l’ID nel portale per sviluppatori HubSpot.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Per ogni tipo di notifica che si desidera controllare, fare clic su <b>Aggiungi elemento</b> e selezionare il tipo di sottoscrizione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>Abilita questa opzione per scollegare o eliminare le vecchie sottoscrizioni associate a questo webhook.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**File**

### File

* [[!UICONTROL Create a Folder]](#create-a-folder)
* [Eliminare un file](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [File di elenco](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [Carica un file](#upload-a-file)
* [Guarda i file](#watch-files)

#### [!UICONTROL Create a Folder]

Questo modulo crea una cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>Immettere o mappare un nome per la nuova cartella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>Seleziona l’ID della cartella principale per la cartella che stai creando. </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un file

Questo modulo di azione elimina definitivamente un file e tutti i dati e le miniature correlati dal file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Immetti o mappa l’ID del file da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

Contrassegna una cartella come eliminata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID della cartella da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### File di elenco

Questo modulo di ricerca restituisce un elenco di file memorizzati nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Immettere o mappare l'ID della cartella contenente i file che si desidera elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Per includere solo i file che contengono caratteri specifici nel nome file, immettere o mappare i caratteri che si desidera includere nel nome file.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

Sposta un file in un&#39;altra cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>Immetti o mappa l’ID del file da spostare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Selezionare l'ID della cartella in cui si desidera spostare il file. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere un nome per il file spostato.</td> 
  </tr> 
 </tbody> 
</table>

#### Carica un file

Questo modulo di azione carica un file nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>Seleziona se desideri che il file sia privato, pubblico ma non indicizzabile, o pubblico e indicizzabile. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Seleziona l’ID della cartella in cui desideri caricare il file. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Abilita questa opzione per sovrascrivere il file se esiste già nella cartella.</td> 
  </tr> 
 </tbody> 
</table>

### File di controllo

Questo modulo di attivazione avvia uno scenario quando un nuovo file viene salvato nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Immetti o mappa l’ID della cartella che contiene i file che desideri guardare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Per includere solo i file che contengono caratteri specifici nel nome file, immettere o mappare i caratteri che si desidera includere nel nome file.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Attività**

### Attività

* [Creare un’attività Calendario](#create-a-calendar-task)
* [Eliminare un’attività Calendario](#create-a-calendar-task)
* [Osserva eventi attività](#watch-task-events)

#### Creare un’attività Calendario

Questo modulo di azione crea una nuova attività per un calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per la nuova attività calendario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione per la nuova attività calendario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>Immettere o mappare l'ID proprietario dell'utente assegnato a questa attività.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Immettere o mappare la data per l'attività.<p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Seleziona il tipo di evento.<ul><li><b>Post di blog</b><p>Immetti l’ID del gruppo di contenuti. Questo è l'ID della pagina del blog.</p></li><li><b>E-mail</b><p>Inserisci o mappa il percorso del modello e-mail che desideri utilizzare.</li><li><b>Pagina di destinazione</b><p>Inserisci o mappa il percorso del modello della pagina di destinazione che desideri utilizzare.</li><li><b>Personalizzato</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Specifica se l'evento si trova nello stato "To do" (Da fare) o "Done" (Fine).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>Inserisci o mappa l’ID HubSpot interno della campagna di cui fa parte questo evento.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un’attività Calendario

Questo modulo di azione elimina un’attività calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID dell'attività che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Osserva eventi attività

Questo modulo di attivazione avvia uno scenario quando è presente un nuovo evento attività in un calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento. Il modulo restituisce fino a 500 eventi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Immetti o mappa la prima data per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Immetti o mappa la data più recente per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Utenti**

### Utenti

* [Ottieni un proprietario](#get-an-owner)
* [Proprietari elenco](#list-owners)

#### Ottieni un proprietario

Questo modulo di azione restituisce i dettagli di un proprietario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Immetti o mappa l’ID del proprietario per il quale desideri restituire i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Proprietari elenco

Questo modulo di ricerca restituisce un elenco di tutti i proprietari di un account HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Ticket**

### Biglietti

<!--* [Create a Ticket]-->
* [Elimina ticket](#delete-a-ticket)
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

#### [!UICONTROL Delete a Ticket]

Elimina un ticket esistente in base al suo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti l’ID del ticket da eliminare. </td> 
  </tr> 
 </tbody> 
</table>

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Aggiornare un ticket Necessità di trovare una connessione funzionante —>

<!-- Watch Tickets Need to find a working connection-->

+++

+++**Forms**

### Moduli

* [Ottieni un file caricato tramite modulo](#get-a-file-uploaded-via-form)
* [Elenca Forms](#list-forms)
  <!--* [Submit Data to a Form]-->
  <!--* [Watch Submissions for a Form]-->

#### Ottieni un file caricato tramite modulo

Questo modulo di azione restituisce un file caricato tramite un modulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>Immetti o mappa l’URL del file da recuperare. Questo si trova nei metadati del modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### Elenca Forms

Questo modulo di azione restituisce tutti i moduli creati nell&#39;account associato alla connessione utilizzata per questo modulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di moduli restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Osserva gli invii per un modulo—È necessario trovare una connessione funzionante>—>

+++

+++**Social media (broadcast)**

### Social media (broadcast)

* [Annullare un messaggio di trasmissione](#cancel-a-broadcast-message)
* [Creare un messaggio di trasmissione](#create-a-broadcast-message)
* [Guarda i messaggi broadcast](#watch-broadcast-messages)

#### Annullare un messaggio di trasmissione

Questo modulo di azione annulla una trasmissione pianificata, ad esempio un tweet o un post di Facebook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Immetti o mappa l’ID della trasmissione che desideri annullare.</td> 
  </tr> 
 </tbody> 
</table>

#### Creare un messaggio di trasmissione

Questo modulo di azione crea e pubblica immediatamente un messaggio sul canale social media specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>Immetti o mappa l’ID del canale che desideri utilizzare per questa trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Inserisci o mappa un titolo per la trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Inserisci o mappa il testo della trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>Inserisci o mappa l’URL di una foto da includere nella trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>Immettere o mappare l'URL di una miniatura che si desidera utilizzare per la trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Immetti o mappa la data e l’ora in cui desideri inviare la trasmissione. Se questo campo viene lasciato vuoto, la trasmissione viene inviata immediatamente.<p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Guarda i messaggi broadcast

Questo modulo di attivazione avvia uno scenario quando un messaggio viene inviato da HubSpot al canale di social media specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>Per avviare lo scenario solo quando il messaggio si trova in uno stato specifico, seleziona lo stato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>Per avviare lo scenario solo quando il messaggio si trova su un canale specifico, seleziona il canale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Per avviare lo scenario solo quando il messaggio è in corrispondenza o dopo una data specifica, immettere o mappare la data nel formato <code>MM/DD/YYYY</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Post di blog**

### Post di blog

<!--* [Create a Blog Post]-->
* [Elimina post di blog](#delete-a-blog-post)
  <!--* [List Blog Posts]-->
* [Publish/Annulla pubblicazione post di blog](#publish--unpublish-a-blog-post)
  <!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


#### Eliminare un post di blog

Questo modulo di azione elimina un singolo post di blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettete o mappate l'ID del post di blog da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

#### Publish/Annulla pubblicazione post di blog

Questo modulo di azione pianifica o annulla la pubblicazione di un post di blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l'ID del post di blog che desideri pianificare o annullare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Seleziona se desideri pianificare il post di blog o annullare un post di blog pianificato in precedenza.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Watch Blog PostsMay need connection-->

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

+++**Iscrizioni**

### Abbonamenti

* [Aggiorna iscrizione e-mail](#update-email-subscription)
* [Controllo della sequenza temporale degli abbonamenti per un portale](#watch-subscriptions-timeline-for-a-portal)

#### Aggiorna iscrizione e-mail

Questo modulo di azione aggiorna un abbonamento e-mail in HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Inserisci o mappa l’indirizzo e-mail dell’abbonamento che desideri aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>Per ogni stato per il quale si desidera aggiornare l'abbonamento, fare clic su <b>Aggiungi elemento</b>, immettere l'ID dello stato e specificare se l'indirizzo di posta elettronica sarà abbonato a tale stato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Per registrare la base legale per questa sottoscrizione al RGPD, seleziona lo stato legale della sottoscrizione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>Per aggiungere una nota relativa alla base giuridica per questa sottoscrizione al RGPD, immetti o mappa il testo della nota.</td> 
  </tr> 
 </tbody> 
</table>

#### Controllo della sequenza temporale degli abbonamenti per un portale

Questo modulo di attivazione avvia uno scenario quando al portale viene aggiunta una nuova sottoscrizione della timeline e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>Per restituire i risultati da una data specifica o da una data successiva, immettere la data nel formato <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>Per restituire i risultati in una data specifica o prima di essa, immettere la data nel formato <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

+++**Altro**

### Altro

#### [!UICONTROL Make an API Call]

Consente di eseguire una chiamata API personalizzata.

>[!NOTE]
>
>I seguenti endpoint sono stati dichiarati obsoleti nell’API HubSpot il 31 agosto 2023 e non possono più essere utilizzati nei moduli Fusion.
>
>* Elencare eventi di contenuto
>* Elencare eventi social
>* Elencare eventi attività calendario
>* Elenca tutti gli eventi calendario
>* Crea attività calendario
>* Ottieni attività calendario per ID
>* Aggiorna attività calendario
>* Eliminare un’attività calendario

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immetti un percorso relativo a https://api.hubapi.com/. Ad esempio, /contacts/v1/LISTS/all/contacts/all</p> <p>Per l'elenco degli endpoint disponibili, fare riferimento alla documentazione API <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selezionare il metodo HTTP che si desidera utilizzare:</p> <p>[!UICONTROL GET]</p> <p>per recuperare informazioni per una voce.</p> <p>[!UICONTROL POST]</p> <p>per creare una nuova voce.</p> <p>[!UICONTROL PUT]</p> <p>per aggiornare o sostituire una voce esistente.</p> <p>[!UICONTROL PATCH]</p> <p>per aggiornare una voce parziale.</p> <p>[!UICONTROL DELETE]</p> <p>per eliminare una voce.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> Inserisci le intestazioni di richiesta desiderate. Non è necessario aggiungere intestazioni di autorizzazione; l’abbiamo già fatto per te.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Immettere la stringa di query richiesta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard. Quando utilizzi istruzioni condizionali come <code>if</code> nel JSON, inserisci le virgolette al di fuori dell'istruzione condizionale.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** La seguente chiamata API restituisce tutti i contatti nel tuo account [!DNL HubSpot]:
>
>**URL**: `/contacts/v1/lists/all/contacts/all`
>
>**Metodo**: `GET`
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Le corrispondenze della ricerca si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts].
>
>Nel nostro esempio, sono stati restituiti 3 contatti:
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Crea una nuova applicazione

1. Accedi al tuo account sviluppatore [!DNL HubSpot].
1. Selezionare l&#39;opzione **[!UICONTROL Create an App]**.
1. Immettere il nome dell&#39;app e [!UICONTROL Save] la finestra di dialogo.
1. Seleziona gli ambiti necessari per il webhook.

   Ad esempio, aggiungi gli ambiti dei contatti per attivare il modulo quando viene creato o eliminato un nuovo contatto.

   [!UICONTROL contacts scope] è tutto ciò di cui hai bisogno per ricevere contatti, offerte e webhook di eventi aziendali.

   >[!IMPORTANT]
   >
   >Non compilare il campo [!UICONTROL Redirect URL].
