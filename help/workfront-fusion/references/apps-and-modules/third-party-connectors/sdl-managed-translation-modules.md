---
title: Moduli SDL Managed Translation
description: In uno scenario Adobe Workfront Fusion, è possibile collegare l'account SDL Managed Translation a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---

# [!DNL SDL Managed Translation] moduli

In uno scenario Adobe Workfront Fusion, è possibile collegare l&#39;account [!DNL SDL Managed Translation] a più applicazioni e servizi di terze parti.

## Requisiti di accesso

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
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore Workfront.

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
