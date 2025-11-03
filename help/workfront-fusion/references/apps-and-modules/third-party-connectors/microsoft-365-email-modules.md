---
title: E-mail Microsoft Office 365
description: In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano Microsoft Office 365 Email, nonché collegarla a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2921'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Email] moduli

In uno scenario di Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL Microsoft Office 365 Email], nonché collegarli a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL Microsoft Office 365 Email], è necessario disporre di un account [!DNL Microsoft Office 365 Email].

## Informazioni API e-mail di Microsoft Office 365

Il connettore e-mail di Microsoft Office 365 utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Connessione del servizio [!DNL Office 365 Email] a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account [!DNL Office 365 Email] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## [!DNL Microsoft Office 365 Email] moduli e relativi campi

Quando si configurano [!DNL Microsoft Office 365 Email] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Microsoft Office 365 Email], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messaggio](#message)
* [Bozza di messaggio](#draft-message)
* [Allegato](#attachment)
* [Altro](#other)

### Messaggio

* [[!UICONTROL Crea e invia un messaggio (legacy)]](#create-and-send-a-message)
* [[!UICONTROL Elimina messaggio]](#delete-a-message)
* [[!UICONTROL Ricevi un messaggio]](#get-a-message)
* [[!UICONTROL Sposta un messaggio]](#move-a-message)
* [[!UICONTROL Cerca messaggi]](#search-messages)
* [[!UICONTROL Messaggi da guardare]](#watch-messages)



#### [!UICONTROL Crea e invia un messaggio (legacy)]

Questo modulo di azione crea e invia un messaggio e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Inserisci o mappa l’oggetto del messaggio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td> <p>Inserisci o mappa il testo del corpo del messaggio dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza dell’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Normale]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Per Destinatari]</p> </td> 
   <td> <p>Per ogni destinatario a cui desideri inviare l'e-mail, fai clic su <b>Aggiungi elemento</b> e immetti quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatari Ccn]</p> </td> 
   <td> <p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, senza consentire ad altri destinatari di visualizzare i propri nomi o indirizzi e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere all'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni messaggi Internet]</td> 
   <td> <p>Per ogni intestazione che si desidera aggiungere all'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Inserisci il nome dell’intestazione</p> </li> 
     <li> <p><strong>[!UICONTROL Valore]</strong> </p> <p>Immettere un valore per l'intestazione.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina messaggio]

Questo modulo elimina un messaggio e-mail esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio da eliminare.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ricevi un messaggio]

Questo modulo ottiene i metadati di un messaggio specifico

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio per cui desideri recuperare i metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Ottieni contenuti MIME]</td> 
   <td>Abilita questa opzione per recuperare i dati sul contenuto MIME del messaggio. Il contenuto [!UICONTROL MIME] può includere immagini, audio, video o altri tipi di file.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Sposta un messaggio]

Questo modulo di azione sposta un messaggio e-mail in una cartella selezionata nella cassetta postale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio da spostare in un’altra cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL cartella di posta] </td> 
   <td> <p>Seleziona o mappa l’ID della cartella in cui desideri spostare il messaggio.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca messaggi]

Questo modulo di ricerca cerca i messaggi in base a criteri specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL cartella di posta]</td> 
   <td> <p>Selezionare la cartella contenente i messaggi che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Ricerca]</td> 
   <td>Immettere la query di ricerca. Per informazioni su come scrivere una query di ricerca, vedere l'articolo di supporto [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Cerca posta e persone in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Selezionare la modalità di ordinamento dei risultati:</p> 
    <ul> 
     <li>[!UICONTROL Subject (Crescente o Decrescente)]</li> 
     <li>Data e ora di creazione [!UICONTROL (crescente o decrescente)]</li> 
     <li>[!UICONTROL Data e ora ultima modifica (crescente o decrescente)]</li> 
     <li>[!UICONTROL Received Date Time (Ascending o descending)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere il numero massimo di messaggi che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Messaggi da guardare]

Questo modulo di attivazione avvia uno scenario quando viene inviato o ricevuto un nuovo messaggio e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Guarda i messaggi]</p> </td> 
   <td> <p>Seleziona i messaggi da guardare:</p> 
    <ul> 
     <li>[!UICONTROL Solo Non Letto]</li> 
     <li>[!UICONTROL Only read]</li> 
     <li>[!UICONTROL Tutto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL cartella di posta]</td> 
   <td> <p>Selezionare la cartella contenente i messaggi che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Ricerca]</td> 
   <td>Immettere la query di ricerca. Il modulo restituisce messaggi che corrispondono a questa query. Per informazioni su come scrivere una query di ricerca, vedere l'articolo di supporto [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Cerca posta e persone in [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere il numero massimo di messaggi che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Bozza di messaggio

* [Creare una bozza di messaggio](#create-a-draft-message)
* [Invia una bozza di messaggio](#send-a-draft-message)
* [Aggiornare un messaggio](#update-a-message)

#### [!UICONTROL Crea bozza messaggio]

Questo modulo di azione crea un nuovo messaggio e-mail come bozza.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Immettere l'oggetto del messaggio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di contenuto corpo]</td> 
   <td>Seleziona se il contenuto del corpo del messaggio è HTML o Testo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td> <p>Inserisci o mappa il testo del corpo del messaggio dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza dell’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Normale]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Per Destinatari]</p> </td> 
   <td> <p>Per ogni destinatario a cui desideri inviare l'e-mail, fai clic su <b>Aggiungi elemento</b> e immetti quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatari Ccn]</p> </td> 
   <td> <p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, senza consentire ad altri destinatari di visualizzare i propri nomi o indirizzi e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere all'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Invia una bozza di messaggio]

Questo modulo di azione invia un messaggio e-mail attualmente in bozza.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bozza messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID messaggio della bozza da inviare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un messaggio]

Questo modulo di azione aggiorna un messaggio esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID messaggio]</td> 
   <td> <p>Seleziona la modalità di identificazione del messaggio da aggiornare:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti Manualmente]</strong> </p> <p>Inserisci o mappa l’ID del messaggio.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Seleziona la cartella contenente il messaggio da aggiornare, quindi fai clic sul messaggio</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Immettere l'oggetto del messaggio.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td> <p>Inserisci il testo del corpo del messaggio dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza dell’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Normale]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Per Destinatari]</p> </td> 
   <td> <p>Per ogni destinatario a cui desideri inviare l'e-mail, fai clic su <b>Aggiungi elemento</b> e immetti quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatari Ccn]</p> </td> 
   <td> <p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, senza consentire ad altri destinatari di visualizzare i propri nomi o indirizzi e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere all'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contrassegnalo come letto]</td> 
   <td>Abilita questa opzione per contrassegnare il messaggio aggiornato come letto.</td> 
  </tr> 
 </tbody> 
</table>

### Allegato

* [[!UICONTROL Scarica un allegato]](#download-an-attachment)
* [[!UICONTROL Elenca allegati]](#list-attachments)

#### [!UICONTROL Scarica un allegato]

Questo modulo scarica l’allegato specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio che contiene l’allegato da scaricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID allegato]</td> 
   <td> <p>Immetti o mappa l’ID dell’allegato da scaricare. È possibile individuare questa idea utilizzando il modulo Elenca allegati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca allegati]

Questo modulo recupera un elenco di allegati appartenenti al messaggio specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio da cui desideri recuperare gli allegati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di allegati che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Aggiungi un allegato]](#add-an-attachment)
* [Creare e inviare un messaggio](#create-and-send-a-message)
* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)

#### [!UICONTROL Aggiungi un allegato]

Questo modulo aggiunge un allegato di grandi dimensioni a un messaggio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID messaggio]</td> 
   <td> <p> Seleziona o mappa l’ID del messaggio a cui desideri aggiungere un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea e invia un messaggio]

Questo modulo di azione crea e invia un messaggio e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Inserisci o mappa l’oggetto del messaggio.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td> <p>Inserisci o mappa il testo del corpo del messaggio dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza dell’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Normale]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Per Destinatari]</p> </td> 
   <td> <p>Per ogni destinatario a cui desideri inviare l'e-mail, fai clic su <b>Aggiungi elemento</b> e immetti quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Destinatari Ccn]</p> </td> 
   <td> <p>Per ogni destinatario a cui si desidera inviare una copia dell'e-mail, senza consentire ad altri destinatari di visualizzare i propri nomi o indirizzi e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Inserisci l’indirizzo e-mail del contatto.</p> </li> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del contatto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere all'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni messaggi Internet]</td> 
   <td> <p>Aggiungi le intestazioni del messaggio per l’e-mail.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Inserisci il nome dell’intestazione</p> </li> 
     <li> <p><strong>[!UICONTROL Indirizzo E-Mail]</strong> </p> <p>Immettere un valore per l'intestazione.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Da indirizzo e-mail]</td> 
   <td> <p> Per utilizzare un indirizzo e-mail condiviso, immetti qui l’indirizzo. L'utente le cui credenziali vengono utilizzate nella connessione utilizzata per questo modulo deve avere accesso alla cartella condivisa.<p>Lascia vuoto questo campo per usare l’indirizzo e-mail del proprietario della connessione.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p> Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
