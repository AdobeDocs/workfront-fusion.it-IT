---
title: Moduli Microsoft OneDrive for Business
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Microsoft OneDrive for Business], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
TQID: https://experienceleague.adobe.com/bFoOLIFIX2ml2K2I2FVSJuNCPwlhfm6sa1RXaVzUoO0
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1154
ht-degree: 30%

---

# Moduli [!DNL Microsoft OneDrive for Business]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft OneDrive for Business], nonché collegarli a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Prerequisiti

Per utilizzare [!DNL Microsoft OneDrive for Business] con Adobe Workfront Fusion, è necessario un account [!DNL Microsoft].

## Connessione del servizio [!DNL Microsoft OneDrive for Business] a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account [!DNL Microsoft OneDrive for Business] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## Moduli [!DNL Microsoft OneDrive for Business] e relativi campi

Quando configuri i moduli [!DNL Microsoft OneDrive for Business], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Microsoft OneDrive for Business], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)

### Trigger

* [[!UICONTROL File di controllo]](#watch-files)
* [[!UICONTROL Cartelle controllate]](#watch-folders)

#### [!UICONTROL File di controllo]

Questo modulo di attivazione si attiva quando viene aggiunto o aggiornato un nuovo file in una cartella controllata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID unità]</p> </td> 
   <td> <p>Selezionare l'unità che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartella]</td> 
   <td> <p> Seleziona la cartella da controllare. All’interno di uno scenario, puoi monitorare solo una cartella.</p> <p>Suggerimento: per guardare più cartelle, crea uno scenario indipendente per ciascuna di esse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voglio guardare]</p> </td> 
   <td> <p>Specificare se si desidera visualizzare i nuovi file e tutte le modifiche o solo i nuovi file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di righe restituite]</td> 
   <td> <p> Imposta il numero massimo di risultati che il modulo deve restituire durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cartelle controllate]

Questo modulo di attivazione si attiva quando si aggiunge una nuova cartella alla cartella controllata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID unità]</p> </td> 
   <td> <p>Selezionare l'unità che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartella]</td> 
   <td> <p> Seleziona la cartella da controllare. All’interno di uno scenario, puoi monitorare solo una cartella.</p> <p>Suggerimento: per tenere traccia di più cartelle, crea uno scenario indipendente per ciascuna di esse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voglio guardare]</p> </td> 
   <td> <p>Seleziona se desideri guardare le nuove cartelle e tutte le modifiche o solo le nuove cartelle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di righe restituite]</td> 
   <td> <p> Imposta il numero massimo di risultati che il modulo deve restituire durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Crea una cartella]](#create-a-folder)
* [[!UICONTROL Eliminare un file]](#delete-a-file)
* [[!UICONTROL Eliminare una cartella]](#delete-a-folder)
* [[!UICONTROL Ottieni un file]](#get-a-file)
* [[!UICONTROL Ottieni un collegamento di condivisione]](#get-a-sharing-link)
* [[!UICONTROL Caricare un file]](#upload-a-file)

#### [!UICONTROL Crea una cartella]

Crea una cartella all&#39;interno della cartella padre specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!Connessione UICONTROL]</strong> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL ID unità]</strong> </td> 
   <td> <p>Selezionare l'unità in cui creare una nuova cartella.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Cartella]</strong> </td> 
   <td> <p>Seleziona la cartella in cui desideri creare una nuova cartella.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Nome cartella]</strong> </td> 
   <td>Inserisci oppure mappa un nome per la nuova cartella.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un file]

Questo modulo di azione sposta il file specificato nel Cestino.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID unità]</td> 
   <td> <p>Selezionare l'unità da cui si desidera eliminare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td> <p>Immettere l'ID del file che si desidera eliminare. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare una cartella]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID unità]</td> 
   <td> <p>Selezionare l'unità da cui si desidera eliminare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID cartella]</td> 
   <td> <p>Immetti o mappa l’ID della cartella da eliminare. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un file]

Questo modulo di azione recupera il file con l’ID specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID unità]</td> 
   <td> <p>Selezionare l'unità da cui si desidera recuperare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID file]</td> 
   <td> <p>Immettere l'ID del file che si desidera recuperare. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un collegamento di condivisione]

Questo modulo recupera un collegamento che puoi condividere per dare accesso al file specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID unità]</td> 
   <td> <p>Selezionare l'unità in cui si desidera caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL INVIO]</td> 
   <td> <p>Seleziona se desideri scegliere un file utilizzando l’ID file o il percorso del file. Immetti l’ID o il percorso del file nel campo visualizzato.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Tipo di autorizzazione]</p> </td> 
   <td> <p>Specificare se si desidera che gli utenti che ricevono il collegamento dispongano di autorizzazioni di lettura/scrittura o di sola lettura.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ambito]</td> 
   <td> <p> Seleziona se desideri che il file sia accessibile solo da parte di chi dispone del collegamento o accessibile solo ai membri della tua organizzazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Caricare un file]

Questo modulo di azione carica un file binario o di testo in una cartella specificata

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID unità]</td> 
   <td> <p>Selezionare l'unità in cui si desidera caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella] </td> 
   <td> <p>Selezionare la cartella nell'unità.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File di origine]</p> </td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Se esiste un file con lo stesso nome]</td> 
   <td> <p> Seleziona l’operazione da eseguire se esiste già un file con lo stesso nome di quello che stai tentando di caricare.</p> 
    <ul> 
     <li>[!UICONTROL Sostituisci il file esistente]</li> 
     <li>[!UICONTROL Rinomina il nuovo file]</li> 
     <li>[!UICONTROL End with an error] (Fine con errore)</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
