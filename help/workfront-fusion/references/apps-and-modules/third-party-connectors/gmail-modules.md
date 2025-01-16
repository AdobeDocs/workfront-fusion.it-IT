---
title: Moduli Gmail
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Gmail e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 0581601a254a9492f4166d78eb0f11868d390f24
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# [!DNL Gmail] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Gmail] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Per utilizzare i moduli [!DNL Gmail], è necessario disporre di un account [!DNL Gmail].

## Connetti [!DNL Gmail] a [!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usingg-suite)
* [Connetti [!DNL Gmail] a [!DNL Workfront Fusion] utilizzando [!DNL gmail.com] or [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL  Google Workspace] {#connect-gmail-to-workfront-fusion-using-g-suite}

Per istruzioni sulla connessione dell&#39;account [!DNL Google Workspace] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL gmail.com] o [!DNL googlemail].com {#connect-gmail-to-workfront-fusion-using-gmail-com-or-googlemail-com}

Se sei un utente [!DNL @gmail.com] o [!DNL @googlemail.com] devi creare un client OAuth su [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) per ottenere un [!UICONTROL Client ID] e un [!UICONTROL Client Secret].

Per istruzioni dettagliate su come creare il client OAuth e ottenere [!UICONTROL Client ID] e [!UICONTROL Client Secret], vedere [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] moduli e relativi campi

Quando configuri [!DNL Gmail] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Gmail], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Azioni](#actions)
* [Iteratori](#iterators)

### Triggers

#### [!UICONTROL Watch emails]

Questo modulo trigger esegue uno scenario quando viene ricevuto un nuovo messaggio e-mail da elaborare.

Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Seleziona la cartella e-mail da guardare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Seleziona il tipo di filtro da utilizzare per guardare le e-mail</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Compila i campi [!UICONTROL Criteria], [!UICONTROL Sender Email Address], [!UICONTROL Subject] e [!UICONTROL Search Phrase]</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>Nel campo [!UICONTROL Query], immettere la query che si desidera utilizzare per filtrare le e-mail.</p> <p>Per ulteriori informazioni sui filtri [!DNL Gmail], vedere <a href="https://support.google.com/mail/answer/7190">Operatori di ricerca</a> nella documentazione di [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Seleziona se desideri guardare [!UICONTROL all email], [!UICONTROL only read emails] o [!UICONTROL only unread] e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Immetti un indirizzo e-mail per controllare solo le e-mail inviate da tale indirizzo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Inserisci una stringa di testo per guardare solo le e-mail che hanno quella stringa di testo nell’oggetto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Inserisci una stringa di testo per guardare solo le e-mail che contengono tale stringa di testo in un punto qualsiasi dell’e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Abilita questa opzione per contrassegnare le e-mail recuperate come lette.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Impostare il numero massimo di risultati con cui [!DNL Workfront Fusion] lavorerà durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Send an email]](#send-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Delete an email]](#delete-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)

#### [!UICONTROL Send an email]

Questo modulo di azione invia una nuova e-mail.

Specifica il destinatario dell’e-mail.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Inserisci o mappa un indirizzo e-mail del mittente.</p> <p>Nota: se immetti un indirizzo e-mail errato, potrebbe verificarsi un errore durante l’invio di un messaggio, perché il tuo account potrebbe non disporre dell’autorizzazione per inviare e-mail da un indirizzo diverso dal tuo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Inserisci o mappa l’oggetto dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Inserisci o mappa il contenuto dell’e-mail (corpo del messaggio). I tag HTML sono consentiti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere un allegato. È possibile mappare un file dai moduli precedenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario della copia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario della copia nascosta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

Questo modulo di azione crea una nuova bozza e-mail e la aggiunge a una cartella specificata.

Specificate la cartella in cui desiderate creare una bozza.

Il modulo restituisce l’ID della bozza e-mail e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] in cui si desidera creare una bozza.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Inserisci o mappa l’oggetto dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Inserisci o mappa il contenuto dell’e-mail (corpo del messaggio). I tag HTML sono consentiti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere un allegato. È possibile mappare un file dai moduli precedenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario della copia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ciascun destinatario della copia nascosta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as read]

Questo modulo di azione contrassegna un messaggio e-mail come letto.

Specifica l’ID dell’e-mail e della relativa cartella.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] che contiene l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

Questo modulo di azione contrassegna un’e-mail o una bozza e-mail come non letta.

Specifica l’ID dell’e-mail e della relativa cartella.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] che contiene l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail che desideri contrassegnare come non letta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an email]

Questo modulo di azione sposta un’e-mail o una bozza e-mail in una cartella specificata.

Puoi specificare la cartella, la cartella di destinazione e l’ID dell’e-mail.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella di origine [!DNL Gmail] contenente l'e-mail che si desidera spostare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Selezionare la cartella di destinazione [!DNL Gmail] in cui si desidera spostare l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail dell’e-mail che desideri spostare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an email]

Questo modulo di azione copia una bozza e-mail o e-mail in una cartella specificata.

Puoi specificare la cartella, la cartella di destinazione e l’ID dell’e-mail.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella di origine [!DNL Gmail] contenente l'e-mail che si desidera copiare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Selezionare la cartella di destinazione [!DNL Gmail] in cui copiare l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail da copiare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

Questo modulo di azione rimuove un’e-mail o una bozza e-mail da una cartella specificata.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] ID messaggio]</p> </td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Abilita questa opzione per consentire al modulo di eliminare definitivamente l’e-mail, invece di spostarla nella cartella del cestino.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

Questo modulo di azione modifica l’etichetta di un messaggio e-mail specificato.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] ID messaggio]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail dell’e-mail da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Seleziona o mappa l’etichetta da aggiungere al messaggio e-mail selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Seleziona o mappa l’etichetta da rimuovere dal messaggio e-mail selezionato.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>I campi [!UICONTROL Label to add] e [!UICONTROL Label to remove] caricano solo le etichette create dall&#39;utente.

### Iteratori

#### [!UICONTROL Iterate attachments]

È possibile iterare gli allegati e-mail. Ogni allegato è un bundle separato nell&#39;output del modulo. Per ulteriori informazioni, vedere [Modulo Iterator](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Selezionare il modulo da cui si desidera iterare gli allegati. </p> </td> 
  </tr> 
 </tbody> 
</table>
