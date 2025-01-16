---
title: Moduli SDL Managed Translation
description: In uno scenario  [!DNL Adobe Workfront Fusion] , è possibile collegare l'account SDL Managed Translation a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# [!DNL SDL Managed Translation] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile collegare l&#39;account [!DNL SDL Managed Translation] a più applicazioni e servizi di terze parti.

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

#### [!UICONTROL Download Translated File]

Questo modulo recupera il contenuto di un singolo file tradotto, contenuto all’interno del progetto specificato. Se il file richiesto non è ancora nello stato Downland, è possibile che il contenuto del file non sia ancora stato tradotto completamente. Se il file è nello stato Download e il recupero è stato completato correttamente, contrassegnarlo come completato utilizzando il metodo `Cancel or Complete File`.

#### [!UICONTROL Upload a File]

Questo modulo consente il caricamento di file da tradurre o includere in un progetto di traduzione come materiale di riferimento. I caricamenti devono essere inviati utilizzando dati multipart/form e possono contenere più file. Specificare `ProjectOptionId` da utilizzare per valutare i file caricati. Questo determina se ogni file che carichi è un possibile candidato per la traduzione o deve essere gestito come materiale di riferimento. Nel caso di archivi (`zip `, `rar`, `7z`, `tar` file), l&#39;app esamina il contenuto dell&#39;archivio e indica se l&#39;archivio nel suo insieme può essere tradotto o se contiene una combinazione di file traducibili e non traducibili.

>[!NOTE]
>
>Il caricamento di più file alla volta non è consigliato, in quanto può aumentare l’impatto di eventuali errori.

#### [!UICONTROL Add a Reference File]

Questo modulo aggiunge un file di riferimento.

### Progetti

#### [!UICONTROL Create a project]

Questo modulo crea il progetto specificato.

#### Annullare o completare un progetto

Questo modulo annulla o completa il progetto specificato. Se il progetto è in attesa di essere scaricato, il progetto passa attraverso gli eventuali passaggi finali del flusso di lavoro e alla fine si sposta per essere completato. Se il progetto è in attesa di approvazione o la selezione del fornitore è annullata. Se il progetto si trova in un altro stato, la richiesta non riuscirà.

#### [!UICONTROL Download Project Zip]

Questo modulo ottiene il file `zip` dei file tradotti per il progetto specificato.

#### [!UICONTROL Read a Project]

Questo modulo ottiene il progetto specificato.

#### [!UICONTROL Get Projects at Status]

Questo modulo ottiene tutti i progetti disponibili nello stato specificato. Questo metodo consente di impaginare i risultati specificando `$top`, `$skip` e `$orderby` parametri di query.

#### [!UICONTROL Get Projects List]

Ottiene un semplice elenco di tutti i progetti, fornendo informazioni generali su ciascun progetto. Questo metodo consente di impostare i risultati come pagine specificando `$top`, `$skip` e `$orderby` parametri di query.

#### [!UICONTROL Search Project Creation Options]

Questo modulo ottiene le opzioni di creazione del progetto.

### Altro

#### [!UICONTROL Make an API Call]

Questo modulo esegue una chiamata API autorizzata arbitraria.
