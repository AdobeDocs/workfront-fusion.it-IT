---
title: Moduli Gmail
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Gmail e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: e14f49dbb7b57a7247a62a27205df1b6da11a259
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---

# [!DNL Gmail] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Gmail] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Gmail], è necessario disporre di un account [!DNL Gmail].

## Connetti [!DNL Gmail] a [!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [Connetti [!DNL Gmail] a [!DNL Workfront Fusion] utilizzando [!DNL gmail.com] or [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL &#x200B; Google Workspace]

Per istruzioni sulla connessione dell&#39;account [!DNL Google Workspace] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Connetti [!DNL Gmail] a [!DNL Workfront Fusion] tramite [!DNL gmail.com] o [!DNL googlemail].com

Se sei [!DNL @gmail.com] o [!DNL @googlemail.com] utente, devi creare un client OAuth su [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) per ottenere un [!UICONTROL ID client] e un [!UICONTROL Segreto client].

Per istruzioni dettagliate su come creare il client OAuth e ottenere un [!UICONTROL ID client] e un [!UICONTROL segreto client], vedere [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] moduli e relativi campi

Quando configuri [!DNL Gmail] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Gmail], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Iteratori](#iterators)

### Trigger

#### [!UICONTROL Controlla le e-mail]

Questo modulo trigger esegue uno scenario quando viene ricevuto un nuovo messaggio e-mail da elaborare.

Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Seleziona la cartella e-mail da guardare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di filtro] </td> 
   <td> <p>Seleziona il tipo di filtro da utilizzare per guardare le e-mail</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Filtro semplice]</strong> </p> <p>Compila i campi [!UICONTROL Criteri], [!UICONTROL Indirizzo e-mail mittente], [!UICONTROL Oggetto] e [!UICONTROL Frase di ricerca]</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>Nel campo [!UICONTROL Query] immettere la query che si desidera utilizzare per filtrare le e-mail.</p> <p>Per ulteriori informazioni sui filtri [!DNL Gmail], vedere <a href="https://support.google.com/mail/answer/7190">Perfezionare le ricerche</a> nella documentazione di [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Seleziona se desideri guardare le e-mail di [!UICONTROL all email], [!UICONTROL only read email] o [!UICONTROL only unread].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Indirizzo e-mail mittente]</td> 
   <td> <p> Immetti un indirizzo e-mail per controllare solo le e-mail inviate da tale indirizzo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Inserisci una stringa di testo per guardare solo le e-mail che hanno quella stringa di testo nell’oggetto.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Frase di ricerca]</td> 
   <td>Inserisci una stringa di testo per guardare solo le e-mail che contengono tale stringa di testo in un punto qualsiasi dell’e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Contrassegna messaggi e-mail come letti al recupero]</td> 
   <td> <p> Abilita questa opzione per contrassegnare le e-mail recuperate come lette.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di risultati]</td> 
   <td> <p> Impostare il numero massimo di risultati con cui [!DNL Workfront Fusion] lavorerà durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL Copia un&#39;e-mail]](#copy-an-email)
* [[!UICONTROL Crea una bozza]](#create-a-draft)
* [[!UICONTROL Eliminare un&#39;e-mail]](#delete-an-email)
  <!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL Contrassegna un&#39;e-mail come già letta]](#mark-an-email-as-read)
* [[!UICONTROL Contrassegna un&#39;e-mail come non letta]](#mark-an-email-as-unread)
* [[!UICONTROL Spostare un&#39;e-mail]](#move-an-email)
* [[!UICONTROL Modifica etichette e-mail]](#modify-email-labels)
* [[!UICONTROL Invia un&#39;e-mail]](#send-an-email)
  <!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL Copia un&#39;e-mail]

Questo modulo di azione copia una bozza e-mail o e-mail in una cartella specificata.

Puoi specificare la cartella, la cartella di destinazione e l’ID dell’e-mail.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella di origine [!DNL Gmail] contenente l'e-mail che si desidera copiare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella di destinazione]</td> 
   <td> <p>Selezionare la cartella di destinazione [!DNL Gmail] in cui copiare l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID e-mail (UID)]</td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail da copiare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea una bozza]

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] in cui si desidera creare una bozza.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL A] </td> 
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
   <td>[!UICONTROL Allegati] </td> 
   <td> <p>Fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere un allegato. È possibile mappare un file dai moduli precedenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copia destinatari]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ogni destinatario della copia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destinatari copia nascosta]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ogni destinatario della copia nascosta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un&#39;e-mail]

Questo modulo di azione rimuove un’e-mail o una bozza e-mail da una cartella specificata.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] ID messaggio]</p> </td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL in modo permanente] </td> 
   <td> <p>Abilita questa opzione per consentire al modulo di eliminare definitivamente l’e-mail, invece di spostarla nella cartella del cestino.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL Contrassegna un&#39;e-mail come già letta]

Questo modulo di azione contrassegna un messaggio e-mail come letto.

Specifica l’ID dell’e-mail e della relativa cartella.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] che contiene l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID e-mail (UID)]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Contrassegna un&#39;e-mail come non letta]

Questo modulo di azione contrassegna un’e-mail o una bozza e-mail come non letta.

Specifica l’ID dell’e-mail e della relativa cartella.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella [!DNL Gmail] che contiene l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID e-mail (UID)] </td> 
   <td> <p>Inserisci o mappa l’ID e-mail dell’e-mail che desideri contrassegnare come non letta.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modifica etichette e-mail]

Questo modulo di azione modifica l’etichetta di un messaggio e-mail specificato.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] ID messaggio]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail dell’e-mail da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Etichette da aggiungere]</p> </td> 
   <td> <p>Seleziona o mappa l’etichetta da aggiungere al messaggio e-mail selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL etichette da rimuovere]</td> 
   <td> <p> Seleziona o mappa l’etichetta da rimuovere dal messaggio e-mail selezionato.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Etichetta da aggiungere] e [!UICONTROL Etichetta da rimuovere] campi caricano solo le etichette create dall&#39;utente.

#### [!UICONTROL Spostare un&#39;e-mail]

Questo modulo di azione sposta un’e-mail o una bozza e-mail in una cartella specificata.

Puoi specificare la cartella, la cartella di destinazione e l’ID dell’e-mail.

Il modulo restituisce l’ID dell’e-mail e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Gmail] a [!DNL Workfront Fusion], vedere <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Gmail] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selezionare la cartella di origine [!DNL Gmail] contenente l'e-mail che si desidera spostare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cartella di destinazione]</td> 
   <td> <p> Selezionare la cartella di destinazione [!DNL Gmail] in cui si desidera spostare l'e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID e-mail (UID)]</td> 
   <td> <p> Inserisci o mappa l’ID e-mail dell’e-mail che desideri spostare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Invia un&#39;e-mail]

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
   <td>[!UICONTROL Da]</td> 
   <td> <p>Inserisci o mappa un indirizzo e-mail del mittente.</p> <p>Nota: se immetti un indirizzo e-mail errato, potrebbe verificarsi un errore durante l’invio di un messaggio, perché il tuo account potrebbe non disporre dell’autorizzazione per inviare e-mail da un indirizzo diverso dal tuo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL A] </td> 
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
   <td>[!UICONTROL Allegati] </td> 
   <td> <p>Fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere un allegato. È possibile mappare un file dai moduli precedenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copia destinatari]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ogni destinatario della copia.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destinatari copia nascosta]</td> 
   <td> <p> Fai clic su <strong>[!UICONTROL Add]</strong>, quindi immetti o mappa l'indirizzo e-mail per ogni destinatario della copia nascosta.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### Iteratori

#### [!UICONTROL Itera allegati]

È possibile iterare gli allegati e-mail. Ogni allegato è un bundle separato nell&#39;output del modulo. Per ulteriori informazioni, vedere [Modulo Iterator](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Modulo Source] </td> 
   <td> <p>Selezionare il modulo da cui si desidera iterare gli allegati. </p> </td> 
  </tr> 
 </tbody> 
</table>
