---
title: Moduli CRM HubSpot
description: I moduli CRM HubSpot di Adobe Workfront Fusion ti consentono di monitorare eventi, record, contatti, progetti, invii di file e moduli oppure di creare, recuperare, aggiornare ed eliminare record, contatti, progetti, eventi o file nel tuo account [!DNL HubSpot CRM] .
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '7323'
ht-degree: 0%

---

# [!DNL HubSpot CRM] moduli

I moduli di Adobe Workfront Fusion [!DNL HubSpot CRM] consentono di monitorare eventi, record, contatti, accordi, invii di file e moduli oppure di creare, recuperare, aggiornare ed eliminare record, contatti, accordi, eventi o file nell&#39;account [!DNL HubSpot CRM].

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
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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

## Connetti Adobe Workfront Fusion a [!DNL HubSpot CRM]

Per istruzioni sulla connessione dell&#39;account [!DNL HubSpot CRM] a Workfront Fusion, vedere [Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Durante la configurazione di una connessione, selezionare il tipo di connessione **CRM HubSpot**. Il tipo di CRM HubSpot (obsoleto) supporta le connessioni esistenti, ma si sconsiglia di utilizzarlo per creare nuove connessioni.

## [!DNL HubSpot CRM] moduli e relativi campi

Quando si configurano [!DNL Hubspot CRM] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Hubspot CRM], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

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
  <!--* [Workflows]()-->
* [Abbonamenti](#subscriptions)
  <!--* [Associations]()-->
* [Altro](#other)

### Oggetti CRM

+++ **[!UICONTROL Cerca oggetti CRM]**

Questo modulo di ricerca cerca oggetti CRM per proprietà personalizzate o per query. Per cercare prodotti o elementi riga, utilizza una connessione speciale con un ambito personalizzato richiesto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type da cercare]</td> 
   <td>Selezionare il tipo di oggetto CRM Hubspot che si desidera cercare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Proprietà output]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. I campi disponibili dipendono dall’oggetto selezionato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtra per] </td> 
   <td> <p>Seleziona la modalità di filtro della ricerca</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Immettere o mappare la query</p> </li> 
     <li> <p><strong>[!UICONTROL Proprietà]</strong> </p> <p>Immetti i gruppi o i filtri per la ricerca.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Fai clic su per ordinare i risultati. Se si sceglie di ordinare i risultati, vengono visualizzati i campi riportati di seguito. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome proprietà]</strong> </p> <p>Selezionare la proprietà in base alla quale si desidera ordinare i risultati</p> </li> 
     <li> <p><strong>[!UICONTROL Direzione]</strong> </p> <p>Scegliere se si desidera ordinare i risultati in senso crescente o decrescente.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset iniziale</td> 
    <td>Immetti o mappa l’ID del primo elemento per il quale desideri recuperare i dettagli. Questo modulo restituisce solo fino a 5000 risultati alla volta. Impostate un offset iniziale per recuperare elementi diversi dai primi 5000. Se l'offset iniziale è 5000, il modulo restituirà gli elementi da 5000 a 9999.</td> 
   </tr>
 </tbody> 
</table>

+++

+++ **Osserva oggetti CRM**

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un oggetto CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di oggetto da cercare]</td> 
   <td> <p>Selezionare il tipo di oggetto che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà output di </td> 
   <td>Selezionare le proprietà che si desidera includere nell'output per questo modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Creato/Aggiornato]</td> 
   <td>Seleziona se desideri guardare gli oggetti creati (nuovi) o aggiornati (modificati).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtra per]</td> 
   <td>Puoi aggiungere un filtro per garantire che lo scenario inizi solo quando vengono soddisfatte determinate condizioni.<ul><li><b>Query</b><p>Immettere la query in base alla quale si desidera filtrare.</li><li><b>Proprietà</b><p>Per ogni proprietà che si desidera utilizzare per filtrare i risultati, fare clic su <b>Aggiungi elemento</b> e immettere il nome, l'operatore e il valore della proprietà.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Record (offerte, contatti e società)

+++ **Crea un record**

Questo modulo di azione crea un contatto, una società o un&#39;offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppi di proprietà </td> 
   <td>Per ogni proprietà che si desidera aggiungere durante la creazione del record, selezionare il gruppo in cui si trova la proprietà. Il gruppo di proprietà si aprirà e potrai quindi inserire il valore delle proprietà. I gruppi di proprietà e le proprietà disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea un record (legacy)]**

Questo modulo di azione crea un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà </td> 
   <td>Immettere le proprietà che si desidera impostare per il record. I campi disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Eliminare un record]**

Questo modulo di azione elimina un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record che si desidera eliminare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'offerta che si desidera eliminare. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ [!UICONTROL Ottieni un record]

Questo modulo di azione ottiene i dettagli di un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record.</p> 
    <ul> 
     <li>[!UICONTROL Contatto]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di ricerca </td> 
   <td>Se stai ricevendo un contatto, seleziona se desideri identificarlo per ID o per indirizzo e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'operazione che si desidera recuperare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail]</td> 
   <td>Immetti l’indirizzo e-mail del contatto di cui desideri recuperare i dettagli. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni una proprietà record]**

Questo modulo di azione ottiene i metadati per una proprietà record specifica in base al nome (interno).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record con la proprietà per cui si desidera recuperare i metadati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome proprietà </td> 
   <td>Seleziona la proprietà per la quale desideri recuperare i metadati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID opzione]</td> 
   <td> <p> Alcune proprietà dispongono di un set di opzioni disponibili che un utente può selezionare come valore della proprietà. Immetti l’ID dell’opzione che rappresenta il valore della proprietà da recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elenca record**

Questo modulo di ricerca restituisce un elenco di contatti, aziende o offerte. La produzione è limitata a 5000 contatti, 12.500 aziende o 12.500 offerte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selezionare il tipo di record che si desidera restituire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà output di </td> 
   <td>Selezionare le proprietà che si desidera includere nell'output per questo modulo.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aggiorna un record]**

Questo modulo di azione aggiorna un contatto, un’azienda o un’offerta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di ricerca </td> 
   <td> <p>Se si sta ottenendo un contatto, selezionare la modalità di identificazione del record:</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL E-Mail]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID del contatto, della società o dell'offerta che si desidera aggiornare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail]</td> 
   <td>Immettere l'indirizzo di posta elettronica del contatto di cui si desidera aggiornare i dettagli. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà </td> 
   <td>Immettere le proprietà che si desidera impostare per il record. I campi disponibili dipendono dal tipo di record che si desidera creare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Osserva record]**

Questo modulo di attivazione avvia uno scenario in cui un contatto, una società o un&#39;offerta è stata modificata o creata negli ultimi 30 giorni. L&#39;output è limitato a 10.000 record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record con la proprietà che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Ricerca]</td> 
   <td>Specificare se si desidera controllare i record modificati di recente o creati di recente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà output di </td> 
   <td>Selezionare le proprietà da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Conttati

+++ **[!UICONTROL Aggiungi contatti a un elenco]**

Questo modulo aggiunge a un elenco contatti i record contatto già creati nel sistema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco] </td> 
   <td>Selezionare l'ID dell'elenco a cui si desidera aggiungere il contatto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/E-mail] </td> 
   <td> <p>Selezionare la modalità di identificazione dei contatti che si desidera aggiungere all'elenco:</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Aggiungere gli ID dei contatti che si desidera aggiungere all'elenco.</p> </li> 
     <li> <p>[!UICONTROL E-Mail]</p> <p>Aggiungere gli indirizzi di posta elettronica dei contatti che si desidera aggiungere all'elenco.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Crea/aggiorna un contatto**

Questo modulo di azione crea un contatto se non esiste in un portale. Se il contatto esiste nel portale, questo modulo lo aggiorna con i valori forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gruppi di proprietà </td> 
   <td>Per ogni proprietà che si desidera aggiungere durante la creazione del contatto, selezionare il gruppo in cui si trova la proprietà. Il gruppo di proprietà si aprirà e sarà quindi possibile inserire i valori delle proprietà.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea/aggiorna un contatto (legacy)]**

Crea un contatto se non esiste già in un portale, oppure lo aggiorna con i valori delle proprietà più recenti se esiste già in un portale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà </td> 
   <td>Specificare le proprietà che si desidera impostare o aggiornare per il contatto. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea/aggiorna un gruppo di contatti]** 

Crea un gruppo di contatti o li aggiorna se esistono già. Le prestazioni sono migliori quando la dimensione del batch è limitata a un massimo di 100 contatti. Le modifiche apportate tramite questo endpoint vengono elaborate in modo asincrono, pertanto l&#39;applicazione delle modifiche ai record dei contatti potrebbe richiedere alcuni minuti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch di contatti da creare/aggiornare] </td> 
   <td> <p>Aggiungi il batch di contatti.</p> <p>Fare clic su <strong>[!UICONTROL Add item]</strong> per aggiungere un nuovo contatto. Nella finestra visualizzata, inserire o mappare le seguenti informazioni:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Tipo di ricerca]</strong> </p> <p>Selezionare la modalità di identificazione del contatto:</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Immettere l'ID del contatto che si desidera creare o aggiornare. </p> </li> 
       <li> <p>[!UICONTROL E-Mail]</p> <p>Immetti l’indirizzo e-mail del contatto da creare o aggiornare. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Proprietà]</strong> </p> <p>Specificare le proprietà che si desidera impostare o aggiornare per il contatto.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca contatti]**

Restituisce tutti i contatti creati nel portale. L&#39;output è limitato a 5000 contatti. Per elencare i contatti precedenti o successivi, puoi utilizzare il parametro [!UICONTROL advanced] per impostare l&#39;offset dell&#39;elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di contatti che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Proprietà output]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID contatto [offset inizio] </td> 
    <td>Immetti o mappa l’ID dell’utente che desideri avviare l’elenco. Ad esempio, se si imposta l'ID contatto come ID del 101° contatto, il modulo potrà elencare i contatti 101-5100 anziché 1-5000. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca contatti di un&#39;azienda]**

Recupera un elenco di contatti della società. L&#39;output è limitato a 5000 contatti. Per elencare i contatti precedenti o successivi, puoi utilizzare il parametro [!UICONTROL advanced] per impostare l&#39;offset dell&#39;elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere l'ID della società di cui si desidera elencare i contatti. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di contatti che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID contatto [offset inizio] </td> 
    <td>Immetti o mappa l’ID dell’utente che desideri avviare l’elenco. Ad esempio, se si imposta l'ID contatto come ID del 101° contatto, il modulo potrà elencare i contatti 101-5100 anziché 1-5000. </td> 
   </tr>
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unisci contatti]**

Questo modulo di azione unisce i contatti

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
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

+++

+++ **[!UICONTROL Rimuovere un contatto da un elenco]**

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco] </td> 
   <td>Selezionare l'ID dell'elenco da cui si desidera rimuovere il contatto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID contatto] </td> 
   <td>Immettere l'ID del contatto da rimuovere dall'elenco. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cerca contatti]**

Recupera un elenco di contatti utilizzando la query di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Immettere la query di ricerca.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Immettere o mappare il numero massimo di contatti che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Controlla i contatti aggiunti a un elenco]**

Questo modulo di attivazione avvia uno scenario quando un nuovo contatto viene aggiunto a un elenco. È disponibile solo per gli utenti con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td>Immettere o mappare l'ID dell'elenco contenente i contatti che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà output di </td> 
   <td>Selezionare le proprietà da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Offerte

+++ **[!UICONTROL Ottieni pipeline CRM dell&#39;offerta]**

Restituisce una pipeline di offerta specifica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID pipeline di  </td> 
   <td>Immetti o mappa l’ID della pipeline per la quale desideri recuperare i dettagli. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID fase] </td> 
   <td>Immetti o mappa l’ID della fase per cui desideri recuperare i dettagli. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elencare le pipeline di offerte/biglietti]**

Restituisce tutte le pipeline di offerte e biglietti per un determinato portale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di oggetto  </td> 
   <td>Seleziona se desideri elencare offerte o biglietti.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Aziende

+++ **[!UICONTROL Cerca società per dominio]**

Recupera un elenco di aziende in base a una corrispondenza esatta con la proprietà del dominio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Immettere il dominio delle società da cercare, ad esempio <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di società che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Proprietà output]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Coinvolgimenti

+++ **Associa un accordo a un oggetto CRM**

Questo modulo di azione associa un coinvolgimento a un contatto, a una società o a un affare.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL ID record]</td> 
  <td>Immettere o mappare l'ID del record a cui si desidera associare il coinvolgimento.</td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Crea un coinvolgimento**

Questo modulo di azione crea un coinvolgimento (ad esempio una nota, un’attività o un’attività) con un oggetto di gestione delle relazioni con i clienti in HubSpot. Gli engagement sono qualsiasi interazione con un contatto che deve essere registrato nel CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL È Attivo?]</td> 
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
   <td role="rowheader">Marca temporale</td> 
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

#### Metadati e-mail

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Da &gt; E-mail]</p> </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail da cui verrà inviata l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Inserisci o mappa il nome della persona da cui verrà inviata l’e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cognome]</td> 
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
   <td>Per inviare un messaggio e-mail in formato HTML, immetti o mappa il corpo del messaggio, inclusi i tag HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Testo</td> 
   <td>Per inviare un messaggio e-mail di solo testo, immetti o mappa il testo del corpo del messaggio.</td> 
  </tr> 
 </tbody> 
</table>

#### Metadati della chiamata

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL A Numero]</p> </td> 
   <td> <p>Immettere o mappare il numero di telefono a cui verrà effettuata la chiamata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da Numero]</td> 
   <td>Immettere o mappare il numero di telefono da cui verrà effettuata la chiamata.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stato]</td> 
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

#### Campi riunione

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
   <td role="rowheader">[!UICONTROL Ora di inizio]</td> 
  <td>Immettere o mappare l'ora di inizio della riunione come timestamp UNIX.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Ora di fine</td> 
   <td>Immettere o mappare l'ora di fine della riunione come timestamp UNIX.</td> 
  </tr> 
 </tbody> 
</table>

#### Campi attività

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
   <td role="rowheader">[!UICONTROL Per Tipo Di Oggetto]</td> 
  <td>Immettere <code>CONTACT</code> o <code>COMPANY</code>.
  </td> 
   </tr> 
 </tbody> 
</table>

+++

+++ **Eliminare un accordo**

Questo modulo di azione elimina un coinvolgimento in base al relativo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Immettere o mappare l'ID del progetto che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Coinvolgimenti di controllo**

Questo modulo di attivazione avvia uno scenario quando viene creato un nuovo impegno in un portale. Questo modulo restituisce solo i record creati negli ultimi 30 giorni o gli ultimi 10.000 record creati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Il numero massimo di società che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da]</td> 
   <td>Immetti o mappa la prima data per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Eventi e notifiche

+++ **Crea/aggiorna un evento sequenza temporale**

Questo modulo di azione crea o aggiorna un evento timeline. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID applicazione]</td> 
   <td>Immetti o mappa l’ID dell’applicazione a cui appartiene questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td>Immetti o mappa un ID per questo evento. Gli ID evento non vengono generati dal sistema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID tipo evento]</td> 
   <td>Inserisci o mappa l’ID del tipo di evento di questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail]</td> 
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
   <td role="rowheader">[!UICONTROL Dati personalizzati]</td> 
   <td>Per ogni elemento di dati personalizzati che si desidera aggiungere all'evento, fare clic su <b>Aggiungi elemento</b> e immettere il nome e il valore dell'elemento.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elenca tipi di evento sequenza temporale**

Questo modulo di ricerca restituisce un elenco di tutti gli eventi della timeline per un’applicazione specifica. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID applicazione]</td> 
   <td>Immetti o mappa l’ID dell’applicazione a cui appartengono questi eventi. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Guarda gli eventi del calendario**

Questo modulo di attivazione avvia uno scenario quando un nuovo evento viene aggiunto a un calendario. Include fino a 500 attività nell&#39;intervallo tra la data di inizio e la data di fine. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di eventi]</td> 
   <td>Seleziona se desideri guardare eventi social, eventi di contenuto o tutti gli eventi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Inizio]</td> 
   <td>Immettere o mappare la data di inizio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
   <td>Immettere o mappare la data di fine.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Osserva le notifiche**

Questo modulo di attivazione avvia uno scenario quando viene inviata una nuova notifica sulle modifiche.  Include fino a 500 attività nell&#39;intervallo tra la data di inizio e la data di fine. Questo modulo può essere utilizzato solo con una connessione per sviluppatori che includa l’identificatore utente, la chiave API HubSpot, l’ID client e il segreto client. In HubSpot puoi avere un solo URL webhook per applicazione per sviluppatori.

Per creare un webhook per questo modulo, fai clic su **Aggiungi** accanto al campo del webhook e compila i campi seguenti:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID applicazione]</td> 
   <td>Immettere l'ID applicazione da utilizzare per questo webhook. Puoi trovare l’ID nel portale per sviluppatori HubSpot.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Per ogni tipo di notifica che si desidera controllare, fare clic su <b>Aggiungi elemento</b> e selezionare il tipo di sottoscrizione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Forza la rimozione delle vecchie sottoscrizioni]</td> 
   <td>Abilita questa opzione per scollegare o eliminare le vecchie sottoscrizioni associate a questo webhook.</td> 
  </tr> 
 </tbody> 
</table>

+++

### File

+++ **[!UICONTROL Creare una cartella]**

Questo modulo crea una cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome cartella] </td> 
   <td>Immettere o mappare un nome per la nuova cartella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella padre] </td> 
   <td>Seleziona l’ID della cartella principale per la cartella che stai creando. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elimina un file**

Questo modulo di azione elimina definitivamente un file e tutti i dati e le miniature correlati dal file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Immetti o mappa l’ID del file da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elimina cartella]**

Contrassegna una cartella come eliminata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID della cartella da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **File di elenco** 

Questo modulo di ricerca restituisce un elenco di file memorizzati nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Immettere o mappare l'ID della cartella contenente i file che si desidera elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Per includere solo i file che contengono caratteri specifici nel nome file, immettere o mappare i caratteri che si desidera includere nel nome file.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Sposta un file]**

Sposta un file in un&#39;altra cartella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file] </td> 
   <td>Immetti o mappa l’ID del file da spostare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella] </td> 
   <td>Selezionare l'ID della cartella in cui si desidera spostare il file. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere un nome per il file spostato.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Carica un file** 

Questo modulo di azione carica un file nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di accesso] </td> 
   <td>Seleziona se desideri che il file sia privato, pubblico ma non indicizzabile, o pubblico e indicizzabile. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella] </td> 
   <td>Seleziona l’ID della cartella in cui desideri caricare il file. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Abilita questa opzione per sovrascrivere il file se esiste già nella cartella.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **File di controllo**

Questo modulo di attivazione avvia uno scenario quando un nuovo file viene salvato nel file manager.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td>Immetti o mappa l’ID della cartella che contiene i file che desideri guardare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Per includere solo i file che contengono caratteri specifici nel nome file, immettere o mappare i caratteri che si desidera includere nel nome file.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Attività

+++ **Crea un&#39;attività Calendario**

Questo modulo di azione crea una nuova attività per un calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per la nuova attività calendario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td>Immettere o mappare una descrizione per la nuova attività calendario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID proprietario]</td> 
   <td>Immettere o mappare l'ID proprietario dell'utente assegnato a questa attività.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Immettere o mappare la data per l'attività.<p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categoria]</td> 
   <td>Seleziona il tipo di evento.<ul><li><b>Post di blog</b><p>Immetti l’ID del gruppo di contenuti. Questo è l'ID della pagina del blog.</p></li><li><b>E-mail</b><p>Inserisci o mappa il percorso del modello e-mail che desideri utilizzare.</li><li><b>Pagina di destinazione</b><p>Inserisci o mappa il percorso del modello della pagina di destinazione che desideri utilizzare.</li><li><b>Personalizzato</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Specifica se l'evento si trova nello stato "To do" (Da fare) o "Done" (Fine).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL GUID campagna]</td> 
   <td>Inserisci o mappa l’ID HubSpot interno della campagna di cui fa parte questo evento.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Eliminare un&#39;attività calendario**

Questo modulo di azione elimina un’attività calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID dell'attività che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Guarda gli eventi attività**

Questo modulo di attivazione avvia uno scenario quando è presente un nuovo evento attività in un calendario. La connessione utilizzata in questo modulo deve utilizzare le credenziali di un utente con un account Marketing a pagamento. Il modulo restituisce fino a 500 eventi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Inizio]</td> 
   <td>Immetti o mappa la prima data per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
   <td>Immetti o mappa la data più recente per la quale desideri guardare gli eventi. Utilizza il formato <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Utenti

+++ **Ottieni un proprietario**

Questo modulo di azione restituisce i dettagli di un proprietario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID proprietario]</td> 
   <td> <p>Immetti o mappa l’ID del proprietario per il quale desideri restituire i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Proprietari elenco**

Questo modulo di ricerca restituisce un elenco di tutti i proprietari di un account HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Biglietti

<!-- Create a Ticket Need to find a working connection-->

+++ **[!UICONTROL Elimina ticket]**

Elimina un ticket esistente in base al suo ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti l’ID del ticket da eliminare. </td> 
  </tr> 
 </tbody> 
</table>

+++

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Aggiornare un ticket Necessità di trovare una connessione funzionante —>

<!-- Watch Tickets Need to find a working connection-->

### Moduli

+++ **Ottieni un file caricato tramite modulo**

Questo modulo di azione restituisce un file caricato tramite un modulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL file]</td> 
   <td>Immetti o mappa l’URL del file da recuperare. Questo si trova nei metadati del modulo.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elenca Forms**

Questo modulo di azione restituisce tutti i moduli creati nell&#39;account associato alla connessione utilizzata per questo modulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di moduli restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—#### Osserva gli invii per un modulo—È necessario trovare una connessione funzionante>—>

### Social media (broadcast)

+++ **Annullare un messaggio di trasmissione**

Questo modulo di azione annulla una trasmissione pianificata, ad esempio un tweet o un post su Facebook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID trasmissione]</td> 
   <td>Immetti o mappa l’ID della trasmissione che desideri annullare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Crea un messaggio di trasmissione**

Questo modulo di azione crea e pubblica immediatamente un messaggio sul canale social media specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID canale]</td> 
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
   <td role="rowheader">[!UICONTROL URL foto]</td> 
   <td>Inserisci o mappa l’URL di una foto da includere nella trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL miniatura]</td> 
   <td>Immettere o mappare l'URL di una miniatura che si desidera utilizzare per la trasmissione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Immetti o mappa la data e l’ora in cui desideri inviare la trasmissione. Se questo campo viene lasciato vuoto, la trasmissione viene inviata immediatamente.<p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Messaggi broadcast**

Questo modulo di attivazione avvia uno scenario quando un messaggio viene inviato da HubSpot al canale di social media specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtra per stato]</td> 
   <td>Per avviare lo scenario solo quando il messaggio si trova in uno stato specifico, seleziona lo stato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtra per canale]</td> 
   <td>Per avviare lo scenario solo quando il messaggio si trova su un canale specifico, seleziona il canale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID trasmissione]</td> 
   <td>Per avviare lo scenario solo quando il messaggio è in corrispondenza o dopo una data specifica, immettere o mappare la data nel formato <code>MM/DD/YYYY</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Post di blog

+++ **Crea post di blog** 

Questo modulo di azione crea un nuovo post di blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Inserisci o mappa il titolo del post (il nome interno del post).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo del post</td> 
   <td>Inserisci o mappa il corpo principale del post in formato HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pubblica riepilogo</td> 
   <td>Immettere o mappare un riepilogo del post. Questo riepilogo viene visualizzato nella pagina dell'elenco principale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID autore blog</td> 
   <td>Inserisci o mappa l'ID dell'autore associato al post.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID gruppo di contenuti</td> 
   <td>Immetti o mappa l'ID del blog a cui appartiene questo post.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML piè di pagina</td> 
   <td>Immetti o mappa il HTML per i codici da incorporare o per il codice JavaScript da inserire prima del tag della pagina.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML principale</td> 
   <td>Inserisci o mappa il HTML per i codici da incorporare o JavaScript che devono essere posizionati in alto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID campagna</td> 
   <td>Inserisci o mappa l'ID della campagna a cui è associato questo post.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Immagine in evidenza</td> 
   <td>Inserisci o mappa l'URL dell'immagine che verrà utilizzata come immagine in primo piano da questo post.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Parola chiave</td> 
   <td>Per ogni parola chiave da aggiungere al post, fare clic su <b>Aggiungi elemento</b> e immettere la parola chiave e il GUID della parola chiave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrizione Meta</td> 
   <td>Immettere o mappare il testo per il tag <code>meta</code> sulla pagina.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data pubblicazione</td> 
   <td>Immetti o mappa la data in cui il post di blog deve essere pubblicato. <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Abilita questa opzione per pubblicare il post di blog subito dopo la creazione. Se questa opzione è impostata su Sì, il campo Data pubblicazione verrà ignorato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Immettete o mappate il margine per il post. Il tag viene aggiunto alla fine del dominio per formare l'URL del post di blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID argomento</td> 
   <td>Per ogni argomento da aggiungere al post, fare clic su <b>Aggiungi elemento</b> e immettere l'ID dell'argomento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usa immagine in primo piano</td> 
   <td>Abilita questa opzione per utilizzare l'immagine in primo piano per il post di blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Widget</td> 
   <td>Immetti o mappa una struttura di dati contenente la data per tutti i moduli per questo post di blog. Questo si riferisce ai moduli del post di blog, non ai moduli di Fusion.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elimina post di blog**

Questo modulo di azione elimina un singolo post di blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettete o mappate l'ID del post di blog da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Elenca post di blog** 

Questo modulo di ricerca recupera i post da un blog HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td>Immetti o mappa il numero massimo di post di blog da restituire in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archiviato</td> 
   <td>Abilita questa opzione per includere i post archiviati nei risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID autore blog</td> 
   <td>Inserisci o mappa l'ID di un autore per restituire i post associati a tale autore.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID campagna</td> 
   <td>Immetti o mappa l'ID di una campagna per restituire i post associati a tale campagna.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID gruppo di contenuti</td> 
   <td>Immetti o mappa l'ID di un blog per restituire i post associati a quel blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Immetti un nome per il post per restituire solo i post con quel nome.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per creato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per aggiornato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo aggiornato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per eliminato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo eliminato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Inserisci o mappa un tag per restituire i post che corrispondono al tag. Il tag viene aggiunto alla fine del dominio per formare l'URL del post di blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stato</td> 
   <td>Seleziona uno stato (Bozza, Pubblicato o Pianificato) per includere solo i risultati in tale stato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordina per data di pubblicazione</td> 
   <td>Seleziona se ordinare i risultati in ordine crescente o decrescente per data di pubblicazione.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Pubblicare o annullare la pubblicazione di un post di blog**

Questo modulo di azione pianifica o annulla la pubblicazione di un post di blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
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

+++

+++ **Guarda post di blog**

Questo modulo trigger avvia uno scenario quando viene creato, aggiornato o eliminato un post di blog che corrisponde ai criteri impostati.



Questo modulo di ricerca recupera i post da un blog HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td>Immetti o mappa il numero massimo di post di blog da restituire in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archiviato</td> 
   <td>Abilita questa opzione per includere i post archiviati nei risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID autore blog</td> 
   <td>Inserisci o mappa l'ID di un autore per restituire i post associati a tale autore.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID campagna</td> 
   <td>Immetti o mappa l'ID di una campagna per restituire i post associati a tale campagna.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID gruppo di contenuti</td> 
   <td>Immetti o mappa l'ID di un blog per restituire i post associati a quel blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td>Immetti un nome per il post per restituire solo i post con quel nome.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per creato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per aggiornato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo aggiornato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra per eliminato</td> 
   <td>Seleziona Filtro per restituire i post in base al valore di tempo eliminato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Slug</td> 
   <td>Inserisci o mappa un tag per restituire i post che corrispondono al tag. Il tag viene aggiunto alla fine del dominio per formare l'URL del post di blog.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stato</td> 
   <td>Seleziona uno stato (Bozza, Pubblicato o Pianificato) per includere solo i risultati in tale stato.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

### Abbonamenti

+++ **Aggiorna abbonamento e-mail**

Questo modulo di azione aggiorna un abbonamento e-mail in HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-Mail]</td> 
   <td>Inserisci o mappa l’indirizzo e-mail dell’abbonamento che desideri aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stati </td> 
   <td>Per ogni stato per il quale si desidera aggiornare l'abbonamento, fare clic su <b>Aggiungi elemento</b>, immettere l'ID dello stato e specificare se l'indirizzo di posta elettronica sarà abbonato a tale stato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Per registrare la base legale per questa sottoscrizione al RGPD, seleziona lo stato legale della sottoscrizione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basation]</td> 
   <td>Per aggiungere una nota relativa alla base giuridica per questa sottoscrizione al RGPD, immetti o mappa il testo della nota.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **Controllo sequenza temporale sottoscrizioni per un portale**

Questo modulo di attivazione avvia uno scenario quando al portale viene aggiunta una nuova sottoscrizione della timeline e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di elementi restituiti dal modulo in un ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp di inizio]</td> 
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

### Altro

+++ **[!UICONTROL Effettuare una chiamata API]**

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL HubSpot CRM] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
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
>![Configurazione API Hubspot](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Le corrispondenze della ricerca si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Corpo] > [!UICONTROL Contatti].
>
>Nel nostro esempio, sono stati restituiti 3 contatti:
>
>![Output API Hubspot](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Crea una nuova applicazione

1. Accedi al tuo account sviluppatore [!DNL HubSpot].
1. Selezionare l&#39;opzione **[!UICONTROL Crea app]**.
1. Immetti il nome dell&#39;app e [!UICONTROL Salva] la finestra di dialogo.
1. Seleziona gli ambiti necessari per il webhook.

   Ad esempio, aggiungi gli ambiti dei contatti per attivare il modulo quando viene creato o eliminato un nuovo contatto.

   L&#39;ambito [!UICONTROL contatti] è tutto ciò di cui hai bisogno per ricevere contatti, offerte e webhook di eventi aziendali.

   >[!IMPORTANT]
   >
   >Non compilare il campo [!UICONTROL URL di reindirizzamento].
