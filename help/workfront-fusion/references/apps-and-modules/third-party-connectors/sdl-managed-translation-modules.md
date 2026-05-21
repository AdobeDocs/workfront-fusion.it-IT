---
title: Moduli SDL Managed Translation
description: In uno scenario Adobe Workfront Fusion, è possibile collegare l'account SDL Managed Translation a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
TQID: https://experienceleague.adobe.com/J6v5bxEi3MzcrkaiQQFOpToDzon0K-BhpmuJQe8sdgY
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 567
ht-degree: 24%

---

# Moduli [!DNL SDL Managed Translation]

In uno scenario Adobe Workfront Fusion, è possibile collegare l&#39;account [!DNL SDL Managed Translation] a più applicazioni e servizi di terze parti.

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
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Informazioni sulle API SDL Managed Translation

Il connettore SDL Managed Translation utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation] moduli

>[!NOTE]
>
>Il timeout dell&#39;operazione per le chiamate a [!DNL SDL Managed Translation] è di **120 secondi**.

### File

#### [!UICONTROL Scarica file tradotto]

Questo modulo recupera il contenuto di un singolo file tradotto, contenuto all’interno del progetto specificato. Se il file richiesto non è ancora nello stato Downland, è possibile che il contenuto del file non sia ancora stato tradotto completamente. Se il file è nello stato Download e il recupero è stato completato correttamente, contrassegnarlo come completato utilizzando il metodo `Cancel or Complete File`.

#### [!UICONTROL Carica un file]

Questo modulo consente il caricamento di file da tradurre o includere in un progetto di traduzione come materiale di riferimento. I caricamenti devono essere inviati utilizzando dati multipart/form e possono contenere più file. Specificare `ProjectOptionId` da utilizzare per valutare i file caricati. Questo determina se ogni file che carichi è un possibile candidato per la traduzione o deve essere gestito come materiale di riferimento. Nel caso di archivi (`zip `, `rar`, `7z`, `tar` file), l&#39;app esamina il contenuto dell&#39;archivio e indica se l&#39;archivio nel suo insieme può essere tradotto o se contiene una combinazione di file traducibili e non traducibili.

>[!NOTE]
>
>Il caricamento di più file alla volta non è consigliato, in quanto può aumentare l’impatto di eventuali errori.

#### [!UICONTROL Aggiungi un file di riferimento]

Questo modulo aggiunge un file di riferimento.

### Progetti

#### [!UICONTROL Crea un progetto]

Questo modulo crea il progetto specificato.

#### Annullare o completare un progetto

Questo modulo annulla o completa il progetto specificato. Se il progetto è in attesa di essere scaricato, il progetto passa attraverso gli eventuali passaggi finali del flusso di lavoro e alla fine si sposta per essere completato. Se il progetto è in attesa di approvazione o la selezione del fornitore è annullata. Se il progetto si trova in un altro stato, la richiesta non riuscirà.

#### [!UICONTROL Scarica ZIP progetto]

Questo modulo ottiene il file `zip` dei file tradotti per il progetto specificato.

#### [!UICONTROL Leggi un progetto]

Questo modulo ottiene il progetto specificato.

#### [!UICONTROL Ottieni progetti allo stato]

Questo modulo ottiene tutti i progetti disponibili nello stato specificato. Questo metodo consente di impaginare i risultati specificando `$top`, `$skip` e `$orderby` parametri di query.

#### [!UICONTROL Ottieni elenco progetti]

Ottiene un semplice elenco di tutti i progetti, fornendo informazioni generali su ciascun progetto. Questo metodo consente di impostare i risultati come pagine specificando `$top`, `$skip` e `$orderby` parametri di query.

#### [!UICONTROL Opzioni di creazione progetto di ricerca]

Questo modulo ottiene le opzioni di creazione del progetto.

### Altro

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo esegue una chiamata API autorizzata arbitraria.
