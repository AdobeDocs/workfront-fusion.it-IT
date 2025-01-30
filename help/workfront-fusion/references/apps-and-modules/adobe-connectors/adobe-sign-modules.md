---
title: Moduli Adobe Acrobat Sign
description: Con i  [!DNL Adobe Acrobat Sign] moduli, puoi avviare uno  [!DNL Adobe Workfront Fusion] scenario basato sugli eventi nell'account di  [!DNL Adobe] Acrobat Sign, creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '5501'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign] moduli

Con i moduli [!DNL Adobe Acrobat Sign], è possibile avviare uno scenario [!DNL Adobe Workfront Fusion] basato sugli eventi nell&#39;account [!DNL Adobe Acrobat Sign], creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.

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

## Informazioni API di [!DNL Adobe Acrobat Sign]

Il connettore Adobe Acrobat Sign utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## [!DNL Adobe Acrobat Sign] consigli per l&#39;utilizzo del connettore

L&#39;app [!DNL Adobe Sign] rende l&#39;automazione dei processi aziendali di eSignature in [!DNL Fusion] molto più semplice e potente.

I nuovi utenti di [!DNL Adobe Sign] devono prestare particolare attenzione ad alcuni dei vincoli relativi all&#39;aggiornamento dei contratti. Gli accordi non vengono in genere modificati una volta avviati. È consigliabile che i nuovi utenti di [!DNL Adobe Sign] si concentrino sulla creazione di nuovi contratti utilizzando il modulo di creazione del contratto. In questo modo [!DNL Fusion] automazioni saranno più semplici e funzioneranno meglio con [!DNL Adobe Sign].

[!DNL Adobe Sign] contratti richiedono l&#39;utilizzo di un campo. Sono disponibili alcune opzioni per eseguire questa operazione, ma la più semplice e comune consiste nel caricare un documento transitorio e quindi mapparlo all&#39;accordo.

![Consigli di Adobe Sign](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign] moduli e relativi campi

Quando configuri [!DNL Adobe Acrobat Sign] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Acrobat Sign], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL Watch for agreements]**

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un accordo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Specificare se si desidera controllare i nuovi record, i record aggiornati o entrambi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type] </td> 
   <td>Selezionare il tipo di record che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Find text]</td> 
   <td> <p>Immettere i termini che si desidera cercare. Il modulo restituisce record che includono questi termini come valori di campo.</p> <p>Per ulteriori informazioni sulla ricerca dei campi in [!DNL Adobe Acrobat Sign], vedere "Funzionamento della ricerca di testo" in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Adobe Sign Search - Funzionamento</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned agreements]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch for events]**

Questo modulo di attivazione avvia uno scenario quando si verifica un evento selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td>Selezionare il webhook che si desidera utilizzare oppure fare clic su <b>[!UICONTROL Add]</b> e compilare i campi seguenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Immetti un nome per il webhook</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scopes]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Account]</p> </li> 
     <li> <p>[!UICONTROL Group]</p> </li> 
     <li> <p>[!UICONTROL User]</p> </li> 
     <li> <p>[!UICONTROL Resource]</p> <p>Se si seleziona [!UICONTROL Resource], immettere l'ID risorsa e il tipo di risorsa.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource level]</td> 
   <td> <p>Seleziona il tipo di risorsa da monitorare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agreements]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL Megasigns]</p> </li> 
     <li> <p>[!UICONTROL Library Documents]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook subscription events]</td> 
   <td>Selezionare gli eventi [!DNL Adobe Sign] che si desidera controllare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application display name]</td> 
   <td>Il nome visualizzato dell’applicazione attraverso la quale viene creato il webhook.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application name]</td> 
   <td>Il nome visualizzato dell’applicazione attraverso la quale viene creato il webhook.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem notification emails]</td> 
   <td> <p>Questa impostazione funziona solo per gli account amministratore</p> <p>Per ogni indirizzo di posta elettronica a cui si desidera inviare le e-mail di notifica del problema, fare clic su <b>[!UICONTROL Add]</b> e immettere l'indirizzo di posta elettronica.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement conditional parameters]</td> 
   <td>Se si desidera aggiungere parametri condizionali, selezionare <b>[!UICONTROL Yes]</b> nel tipo di record a cui si desidera aggiungere i parametri, quindi selezionare <b>[!UICONTROL Yes]</b> in tutti i parametri che si desidera abilitare.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Azioni

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL Create a record]**

Questo modulo di azione crea un nuovo record del tipo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group info]</td> 
   <td> <p>Immettere o mappare [!UICONTROL Name] e [!UICONTROL ID] del gruppo e indicare se questo gruppo è il gruppo predefinito per l'account.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library document info]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Files to send]</b> </p> <p>Per ogni file da aggiungere, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi.</p> 
      <ul> 
       <li><b>[!UICONTROL Transient document ID]</b> <p>Immettere l'ID del documento transitorio</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immettere un nome per il file.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL del file che si desidera inviare.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Seleziona se il documento deve essere autenticato o meno.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Library template name]</b> </p> <p>Inserisci o mappa il nome del modello della libreria</p> </li> 
     <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Specificare gli utenti a cui assegnare l'accesso al documento della raccolta.</p> </li> 
     <li> <p><b>[!UICONTROL Library document state]</b> </p> <p>Specificare se il documento è in stato di creazione o attivo.</p> </li> 
     <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Per ogni tipo di modello di libreria che si desidera utilizzare, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il tipo di modello.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Immettere l'ultima data in cui si è verificato un evento nel documento di libreria.</p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Library document status]</b> </p> <p>Selezionare lo stato del documento della raccolta.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User info]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Inserisci l’indirizzo e-mail dell’utente.</p> </li> 
     <li> <p><b>[!UICONTROL Is account admin]</b> </p> <p>Seleziona questa opzione se l’utente creato è un amministratore account.</p> </li> 
     <li> <p><b>[!UICONTROL User ID]</b> </p> <p>Inserisci l’ID univoco dell’utente</p> </li> 
     <li> <p><b>[!UICONTROL Account ID]</b> </p> <p>Immettere l'ID univoco dell'account [!DNL Adobe Acrobat Sign] associato a questo utente.</p> </li> 
     <li> <p><b>[!UICONTROL First name]</b> </p> <p>Immettere il nome dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Inserisci il cognome dell’utente</p> </li> 
     <li> <p><b>[!UICONTROL Company]</b> </p> <p>Immettere il nome dell'azienda dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Initials]</b> </p> <p>Immettere le iniziali dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
     <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Immettere il numero di telefono dell'utente</p> </li> 
     <li> <p><b>ID gruppo primario</b> </p> <p>Immettere il gruppo a cui viene aggiunto il nuovo utente. Se non viene immesso alcun valore, l'utente verrà aggiunto al gruppo predefinito per l'account.</p> </li> 
     <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Immetti la qualifica dell’utente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Web form info]</td> 
   <td> <p>Compila i campi seguenti</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File info]</b> </p> <p>Per ogni file che si desidera aggiungere al modulo Web, fare clic su Aggiungi e compilare i campi seguenti:</p> 
      <ul> 
       <li> <p>[!UICONTROL File type]</p> <p>[!UICONTROL Document]</p> </li> 
       <li> <p>[!UICONTROL Transient document]</p> </li> 
       <li> <p>[!UICONTROL URL file info]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form name]</b> </p> <p>Immettere un nome per il modulo Web. Questo nome viene utilizzato per identificare il modulo web in luoghi quali e-mail e siti web.</p> </li> 
     <li> <p><b>[!UICONTROL Web form state]</b> </p> <p>Seleziona lo stato in cui creare il nuovo modulo web.</p> </li> 
     <li> <p><b>[!UICONTROL Web form participant set info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Per ogni membro da aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Lascia vuota questa opzione.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Se si desidera aggiungere un'opzione di protezione per l'autenticazione dell'utente, selezionare <b>[!UICONTROL Yes]</b>, quindi selezionare l'opzione di protezione e compilare i campi necessari.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> <p>Seleziona il ruolo. Tutti i membri di questo set di partecipanti condividono il ruolo.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form additional participant sets info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Per ogni membro da aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Lascia vuota questa opzione.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Se si desidera aggiungere un'opzione di protezione per l'autenticazione dell'utente, selezionare <b>[!UICONTROL Yes]</b>, quindi selezionare l'opzione di protezione e compilare i campi necessari.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Web form participant ID] </b> </p> <p>Immetti l’ID del partecipante al modulo web.</p> </li> 
       <li> <p><b>[!UICONTROL Order]</b> </p> <p>Specifica l’ordine in cui il set di partecipanti deve interagire con il modulo web. Ad esempio, il gruppo di partecipanti con un valore di ordine pari a 1 deve andare per primo, 2 deve andare per secondo e così via. I numeri di ordine devono iniziare con uno e non devono presentare spazi vuoti nella serie. </p> </li> 
       <li> <p><b>[!UICONTROL Provider participant set info]</b> </p> <p>Se il partecipante è sconosciuto, specificare se il provider deve fornire i dettagli per il partecipante e immettere un messaggio con i dettagli richiesti per il partecipante sconosciuto.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Authentication failure info]</b> </p> <p>Se si desidera fornire agli utenti una pagina di errore o di errore, selezionare <b>[!UICONTROL Yes]</b>, quindi compilare i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL per la pagina di errore</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Abilita questa opzione se desideri che la pagina di errore venga visualizzata nel modulo web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Immettere il ritardo, in secondi, prima che l'utente venga reindirizzato alla pagina di errore.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL CC info]</b> </p> <p>Per ogni indirizzo e-mail a cui si desidera inviare un messaggio e-mail al momento della firma del contratto finale sul modulo Web, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo e-mail.</p> </li> 
     <li> <p><b>[!UICONTROL Completion info]</b> </p> <p style="font-style: normal;">Se desideri fornire una pagina di successo per i tuoi utenti, seleziona <b>[!UICONTROL Yes]</b>, quindi compila i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Inserisci l’URL per la pagina di successo</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Abilita questa opzione se desideri che la pagina di successo venga visualizzata all’interno del modulo web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Immetti il ritardo, in secondi, prima che l’utente venga reindirizzato alla pagina di successo.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Group ID]</b> </p> <p>Immetti l’ID del gruppo a cui appartiene il modulo web. Se non viene immesso alcun valore, il modulo web appartiene al gruppo principale dell’utente dell’account.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Immettere la data in cui si è verificato l'ultimo evento nel modulo Web. Utilizza il formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
     <li> <p><b>[!UICONTROL Security optio]n</b> </p> <p>Immettere la password utilizzata per proteggere il documento. Devi comunicare separatamente questa password a tutte le parti interessate.</p> </li> 
     <li> <p><b>[!UICONTROL Vaulting info]</b> </p> <p>Se l'account è impostato per il vaulting dei documenti e l'opzione per l'abilitazione per ogni contratto, è possibile abilitare questa opzione per il vaulting del contratto.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create an agreement]**

Questo modulo di azione crea un accordo, lo invia per la firma e restituisce l’ID dell’accordo.

>[!NOTE]
>
>È consigliabile caricare il documento per firmarlo come documento transitorio, quindi eseguirne il mapping al campo [!UICONTROL File to send] nel modulo [!UICONTROL Create an agreement]. Ad esempio, consulta &quot;Caricare un documento&quot; in questo articolo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Files to send]</td> 
   <td> <p>Per ogni elemento che si desidera includere nel contratto, fare clic su <b>[!UICONTROL Add Item]</b> e compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File Type]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Document]</b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Immettere o mappare la data di creazione del documento nel formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>. Ad esempio, <code>2016-02-25T18:46:19Z</code> rappresenta l'ora UTC.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Immettere o mappare l'ID del documento.</p> </li> 
         <li> <p><b>[!UICONTROL Label]</b> </p> <p>Immettere o mappare un'etichetta univoca per il file. In caso di flusso di lavoro personalizzato, questo mapperà un file all’elemento file corrispondente nella definizione del flusso di lavoro. Questo deve essere specificato in caso di richiesta di creazione di accordi di flusso di lavoro personalizzati.</p> </li> 
         <li> <p><b>[!UICONTROL Number of pages]</b> </p> <p>Immettere o mappare il numero di pagine nel documento.</p> </li> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Immetti o mappa il tipo MIME del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immettere o associare un nome per il documento.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Library document ID]</b> </p> <p>Immettere l'ID del documento di libreria</p> </li> 
       <li> <p><b>[!UICONTROL Transient document ID]</b> </p> <p>Immettere l'ID del documento transitorio</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immettere un nome per il file.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL del file che si desidera inviare.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Immettere un'etichetta per il file.</p> </li> 
     <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Abilita questa opzione per indicare che il file deve essere notarizzato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement name]</td> 
   <td>Immettere un nome per il nuovo contratto. Questo nome viene utilizzato per identificare l’accordo in luoghi quali e-mail e siti web.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant sets info]</td> 
   <td> <p>Per ogni set di partecipanti che si desidera aggiungere, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi seguenti.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Members]</b> </p> <p>Per ogni persona che si desidera aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo di posta elettronica della persona.</p> </li> 
     <li> <p><b>[!UICONTROL Order]</b> </p> <p>Specificare l'ordine di firma del contratto da parte del set di partecipanti. Ad esempio, il gruppo di partecipanti con valore di ordine 1 deve firmare per primo, 2 deve firmare per secondo e così via. I numeri di ordine devono iniziare con uno e non devono presentare spazi vuoti nella serie. </p> </li> 
     <li> <p><b>[!UICONTROL Role]</b> </p> <p>Selezionare un ruolo per questo set di partecipanti. Tutti i partecipanti al set ricevono questo ruolo.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Immetti o mappa l'ID di questo set di partecipanti.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Immettere o mappare un'etichetta univoca per il set di partecipanti. Per i flussi di lavoro personalizzati, l’etichetta specificata nel set di partecipazione deve mapparla sul passaggio di partecipazione nel flusso di lavoro personalizzato.</p> </li> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immettere un nome per il set di partecipanti. Il nome deve essere univoco all'interno del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Immettere o mappare un messaggio per questo set di partecipanti. Tutti i partecipanti al set ricevono questo messaggio.</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> <p>Se per questo contratto è abilitata la visibilità limitata dei documenti, specificare quali file sono visibili a questo set di partecipanti. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Signature type]</td> 
   <td> <p>Selezionare il tipo di firma richiesto dal contratto.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>La convenzione deve essere firmata elettronicamente.</p> </li> 
     <li> <p><b>[!UICONTROL Written]</b> </p> <p>Il contratto deve essere firmato manualmente e deve essere analizzato e caricato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>Selezionare uno stato per il contratto.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>È comunque possibile modificare o aggiungere campi al contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Draft]</b> </p> <p>Puoi creare questo contratto in modo incrementale prima di inviarlo.</p> </li> 
     <li> <p><b>[!UICONTROL In Process]</b> </p> <p>L'accordo sarà inviato immediatamente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CCs]</td> 
   <td> <p>Puoi inviare il presente contratto a parti interessate che non hanno bisogno di firmare, ad esempio le parti interessate. Ricevono un’e-mail all’inizio del processo di firma e un’altra all’atto della ricezione della firma finale. Essi ricevono inoltre una copia PDF dell'accordo. </p> <p>Per ogni persona che si desidera inserire nel contratto, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Immetti o mappa l’indirizzo e-mail che desideri usare come CC nel contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Immetti o mappa un’etichetta per questo indirizzo e-mail, come mostrato nella descrizione del flusso di lavoro</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> </li> 
     <li> <p>Se per questo contratto è abilitata la visibilità limitata dei documenti, specificare quali file sono visibili a questo set di partecipanti. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Per ogni tipo di e-mail, seleziona se il tipo di e-mail viene inviato a tutti i partecipanti o se non ne viene inviato alcuno.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Completion emails]</b> </p> <p>Invia un messaggio di posta elettronica quando il contratto viene completato, annullato, scaduto o rifiutato.</p> </li> 
     <li> <p><b>[!UICONTROL In-Flight emails]</b> </p> <p>Inviato un messaggio e-mail quando il contratto viene delegato o sostituito.</p> </li> 
     <li> <p><b>[!UICONTROL Agreement initiation emails]</b> </p> <p>Invia un messaggio di posta elettronica quando viene creato il contratto o quando viene richiesta un'azione.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p>Immettere o mappare un ID per il contratto. È possibile specificare questo valore al momento della creazione dell'accordo e utilizzarlo per individuare l'accordo nei moduli o nelle query successive.</p> <p>Nota: il valore ID esterno è visibile a tutti i partecipanti tramite l’API, pertanto non deve essere utilizzato per contenere un token sensibile.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Merge field info]</td> 
   <td> <p>Per ogni campo del contratto per cui si desidera inserire un valore predefinito, fare clic su <b>[!UICONTROL Add item]</b> e immettere il valore predefinito e il nome del campo.</p> <p>I valori verranno presentati ai firmatari per i campi modificabili. Per i campi di sola lettura, i valori forniti non saranno modificabili durante il processo di firma.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Notary info]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Appointment]</b> </p> <p>Immettere o mappare un'ora e una data proposte per l'appuntamento per la registrazione del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Note]</b> </p> <p>Immettere o mappare le note da includere sulla sessione notarile.</p> </li> 
     <li> <p><b>[!UICONTROL Payment]</b> </p> <p>Seleziona se il notaio è pagato dal firmatario o dal mittente del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Notary Type]</b> </p> <p>Seleziona il tipo di notaio</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider notary]</p> <p>Il notaio è prestato dal notaio.</p> </li> 
       <li> <p>[!UICONTROL BYON notary]</p> <p>Il notaio è fornito dal cliente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Post sign option]</td> 
   <td> <p>Selezionare se si desidera che i firmatari vengano indirizzati a una pagina di successo dopo la firma del contratto. Se si seleziona <b>[!UICONTROL Yes]</b>, compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Redirect delay]</b> </p> <p>Inserisci o mappa un numero che rappresenta il numero di secondi prima che il firmatario venga reindirizzato alla pagina riuscita. Se questo valore è maggiore di 0, l'utente visualizzerà prima il messaggio di successo standard di [!DNL Adobe Sign] e quindi, dopo un ritardo, verrà reindirizzato alla pagina di successo.</p> </li> 
     <li> <p><b>[!UICONTROL Redirect URL]</b> </p> <p>Immetti o mappa un URL accessibile al pubblico a cui l’utente verrà inviato dopo aver completato correttamente il processo di firma.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Security option]</td> 
   <td> <p>Immettere o mappare la password secondaria che verrà utilizzata per proteggere il documento PDF. </p> <p>Importante: [!DNL Adobe Sign] non condividerà mai questa password, pertanto devi comunicarla separatamente a tutte le parti interessate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vaulting info]</td> 
   <td>Se l'account è impostato per il vaulting dei documenti e l'opzione per l'abilitazione per ogni contratto, è possibile abilitare questa opzione per il vaulting del contratto.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create related records]**

Questo modulo di azione crea record collegati a un modulo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record originale a cui si desidera associare i record creati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera associare il record creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement related field]</td> 
   <td> <p>Seleziona il tipo di campo correlato da creare</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Form fields]</b> </p> <p>Immettere l'ID modello del modello contenente i campi che si desidera creare</p> </li> 
     <li> <p><b>[!UICONTROL Reminders]</b> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Recipient participant ID]</b> </p> <p>Per ogni partecipante a cui si desidera inviare un promemoria, fare clic su [!UICONTROL Add item] e immettere l'ID del partecipante.</p> </li> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Per i nuovi record, lo stato deve essere [!UICONTROL Active].</p> </li> 
       <li> <p><b>[!UICONTROL First reminder delay]</b> </p> <p>Immetti il ritardo in ore prima di inviare il primo promemoria. Il valore minimo consentito è di 1 ora e il valore massimo non può essere maggiore della differenza tra la creazione del contratto e la scadenza del contratto espressa in ore. Se questo ritardo non è impostato, il primo promemoria sarà basato sulla frequenza.</p> </li> 
       <li> <p><b>[!UICONTROL Reminder frequency]</b> </p> <p>Impostare la frequenza di invio del promemoria. Se non viene specificata la frequenza, il promemoria verrà inviato una volta.</p> </li> 
       <li> <p><b>[!UICONTROL Last sent date]</b> </p> <p>Questo campo viene impostato dal sistema.</p> </li> 
       <li> <p><b>[!UICONTROL Next sent date]</b> </p> <p>Questo campo deve essere vuoto o impostato su [!UICONTROL ONCE].</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Immettere una nota da includere nel promemoria. Questo è utile per spiegare al partecipante perché è necessaria la sua partecipazione.</p> </li> 
       <li> <p><b>[!UICONTROL Start reminder counter from]</b> </p> <p>Selezionare se il promemoria viene inviato in base alla data di creazione dell'accordo quando diventa disponibile.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Signer identity report]</b> </p> <p>Immettere la password utilizzata per proteggere il documento PDF.</p> </li> 
     <li> <p><b>[!UICONTROL Views]</b> </p> <p>Immetti i campi seguenti</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selezionate il nome della vista da creare.</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'URL restituito.</p> </li> 
       <li> <p><b>[!UICONTROL Frame Parent]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera modificare la sezione di caricamento dei file aggiungendo o rimuovendo file. Questo non è un meccanismo di controllo degli accessi. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera che i collegamenti dei documenti della raccolta siano visibili. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera visualizzare il pulsante Caricamento file locale. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera visualizzare i collegamenti per allegare documenti da origini Web. Il valore predefinito è Sì.</p> </li> 
       <li> <p><b>[!UICONTROL Is preview selected]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per impostare la pagina Componi in modalità Creazione.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Per ogni membro con cui si desidera condividere il contratto, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo di posta elettronica del membro e un messaggio per tale membro.</p> </li> 
     <li> <p>[!UICONTROL Delegate participant set]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Participant set ID]</b> </p> <p>Inserisci l'ID del set di partecipanti</p> </li> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Per ogni membro che si desidera aggiungere, fare clic su [!UICONTROL Add item] e immettere l'indirizzo di posta elettronica e le informazioni di telefono per il membro.</p> </li> 
       <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Immetti un messaggio. Tutti i membri del set di partecipanti ricevono questo messaggio.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library view info]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immetti un nome per il modello della libreria. Questo nome viene utilizzato nelle e-mail e nei siti web.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'URL restituito.</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
     <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
     <li> <p><b>[!UICONTROL Send view configuration]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera configurare la visualizzazione [!UICONTROL Send], quindi compilare i campi seguenti.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Agreement name]</b> </p> <p>Immettere o mappare il nome del contratto per il documento di libreria nella pagina di composizione.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera modificare la sezione di caricamento dei file aggiungendo o rimuovendo file. Questo non è un meccanismo di controllo degli accessi. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera che i collegamenti dei documenti della raccolta siano visibili. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera visualizzare i collegamenti per allegare documenti da origini Web. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>Anteprima selezionata</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per impostare la pagina Componi in modalità Creazione.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User view info]</td> 
   <td> <p>Compila i campi seguenti</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Seleziona il nome della visualizzazione utente richiesta.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'utente. Selezionare <b>[!UICONTROL No]</b> per richiedere le credenziali. Il valore predefinito è [!UICONTROL No].</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
     <li> <p><b>Nessun flag Chrome</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Widget related fields]</td> 
   <td> <p>Selezionare il record correlato da creare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Views]</p> <p>Compila i campi seguenti.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Seleziona il nome della visualizzazione del modulo web richiesta</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'utente. Selezionare <b>[!UICONTROL No]</b> per richiedere le credenziali. Il valore predefinito è [!UICONTROL No].</p> </li> 
       <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
       <li> <p>[!UICONTROL Personalized signing view configuration]</p> <p>Se si desidera configurare una visualizzazione della firma personalizzata, selezionare <b>[!UICONTROL Yes]</b> e compilare i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Immetti l’indirizzo e-mail della persona che riceve il modulo web appena creato</p> </li> 
         <li> <p><b>[!UICONTROL Comment]</b> </p> <p>Inserisci un commento che descrive come il chiamante API ha stabilito l’identità del firmatario. Queste informazioni vengono visualizzate nell'audit trail [!DNL Adobe Acrobat Sign].</p> </li> 
         <li> <p><b>[!UICONTROL Expiration]</b> </p> <p>Immetti una data di scadenza per la personalizzazione del modulo web. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Reusable]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> se si desidera che il firmatario desiderato possa firmare il modulo più di una volta.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Per ogni membro con cui si desidera condividere il contratto, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo di posta elettronica del membro e un messaggio per tale membro.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Custom API Call]**
Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Inserisci un percorso relativo a <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>Nota: per l'elenco degli endpoint disponibili, fare riferimento al riferimento API [!DNL Adobe Sign].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Immettere la stringa di query richiesta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a transient document]</td> 
   <td> <p>Se si desidera caricare un documento transitorio, immettere il file di origine del documento che si desidera caricare.</p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List records]**

Questo modulo di azione elenca tutti i record del tipo selezionato a cui l’account ha accesso.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td>Immettere o mappare l'ID esterno (un ID assegnato all'esterno di [!DNL Adobe Acrobat Sign]) per i contratti che si desidera restituire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td>Immettere l'ID del gruppo associato ai record da elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden (records)]</td> 
   <td>Abilitare questa opzione se si desidera includere i record nascosti nei risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start index]</td> 
   <td> <p>Immettere il numero del primo record restituito dal modulo. </p> <p>Nota: questo campo è combinato con il campo [!UICONTROL Maximum number of returned records] per l'impaginazione. Ad esempio, se [!UICONTROL Maximum number of returned events] è 100 e [!UICONTROL Start index] è 101, il modulo restituisce i record 101-200 o la seconda pagina di risultati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned records]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che si desidera vengano inseriti nel modulo in [action] durante ogni ciclo di esecuzione dello scenario.</p> <p>Nota: questo campo è combinato con il campo [!UICONTROL Cursor] o [!UICONTROL Start Index] per l'impaginazione. Ad esempio, se [!UICONTROL Maximum number of returned events] è 100 e [!UICONTROL Start index] è 101, il modulo restituisce i record 101-200 o la seconda pagina di risultati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent domain URLs]</td> 
   <td> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read a record]**

Questo modulo di azione recupera le informazioni da un singolo record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Immettere o mappare l'ID del record che si desidera recuperare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read related records]**

Leggi le informazioni aggiuntive relative a un singolo record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] (Esempio: [!UICONTROL Account ID])</td> 
   <td>Immettere o mappare l'ID del record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a record]**

Questo modulo di azione aggiorna un singolo record in [!DNL Adobe Acrobat Sign].

>[!IMPORTANT]
>
>* Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.
>* Alcuni aggiornamenti presentano campi obbligatori. Quando configuri l’aggiornamento, assicurati di compilare tutti i campi obbligatori. I campi obbligatori sono in grassetto nei moduli [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] </td> 
   <td>Immetti o mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Selezionare il nuovo stato per il documento di libreria.</p> </li> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Inserisci o mappa il nome del modello della libreria</p> </li> 
       <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Specificare gli utenti a cui assegnare l'accesso al documento della raccolta.</p> </li> 
       <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Per ogni tipo di modello di libreria che si desidera utilizzare, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il tipo di modello.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL First name]</b> </p> <p>Immettere il nome dell'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Inserisci il cognome dell’utente</p> </li> 
       <li> <p><b>[!UICONTROL Company]</b> </p> <p>Immettere il nome dell'azienda dell'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Immettere il numero di telefono dell'utente</p> </li> 
       <li> <p><b>[!UICONTROL Primary group ID]</b> </p> <p>Immettere il gruppo a cui viene aggiunto il nuovo utente. Se non viene immesso alcun valore, l'utente verrà aggiunto al gruppo predefinito per l'account.</p> </li> 
       <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Immetti la qualifica dell’utente.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update related record]**

Questo modulo di azione aggiorna i record relativi a un oggetto specifico.

>[!IMPORTANT]
>
>* Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.
>* Alcuni aggiornamenti presentano campi obbligatori. Quando configuri l’aggiornamento, assicurati di compilare tutti i campi obbligatori. I campi obbligatori sono in grassetto nei moduli [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selezionare il tipo di record al quale sono associati i campi correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera associare il record creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selezionare il nuovo stato per il documento di libreria.</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Immettere o mappare il testo della nota.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Specificare se visualizzare o nascondere il documento della raccolta.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Group info list]</b> </p> <p>Compila i campi seguenti</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Status]</b> </p> <p>Seleziona il nuovo stato per l’utente.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Inserisci l’ID univoco del gruppo</p> </li> 
         <li> <p><b>[!UICONTROL Is group admin]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per impostare l'utente come amministratore del gruppo.</p> </li> 
         <li> <p><b>È un gruppo primario</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per aggiornare il gruppo al gruppo principale dell'utente.</p> </li> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Immettere la data di creazione del gruppo.</p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Immettere o mappare il nome del gruppo.</p> </li> 
         <li> <p><b>[!UICONTROL Library document creation visible]</b> </p> <p>Queste impostazioni determinano se l'utente può creare documenti della libreria</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Send restricted to workflows]</b> </p> <p>Queste impostazioni determinano se l'utente può creare accordi solo utilizzando flussi di lavoro.</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL User can send]</b> </p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selezionare il nuovo stato per l'utente e immettere un commento relativo al motivo per cui si desidera attivare o disattivare l'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Upload document]**

Carica un documento transitorio. Un documento transitorio è disponibile per 7 giorni dopo il suo caricamento.

>[!NOTE]
>
>È consigliabile caricare il documento per firmarlo come documento transitorio, quindi eseguirne il mapping al campo File da inviare nel modulo Crea un accordo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Immetti o mappa l’ID del record da aggiornare</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</td> 
  </tr> 
 </tbody> 
</table>

**Esempio:** In questo flusso di lavoro, il documento da firmare (precedentemente scaricato da Workfront) viene caricato come documento transitorio.

(/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

Il modulo [!UICONTROL Upload document] assegna al documento un ID [!DNL Adobe Acrobat Sign] a cui è possibile fare riferimento nei moduli successivi. Al momento della creazione dell&#39;accordo, l&#39;ID del documento caricato viene incluso nel campo [!UICONTROL Files to send].

![Firma esempio](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Ricerche

+++ **[!UICONTROL Search agreements]**

Questo modulo di ricerca cerca i contratti in base ai criteri specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text filter]</td> 
   <td> <p>Cercare il testo nei metadati del contratto. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Find text]</b> </p> <p>Immettere il testo da trovare nei metadati del contratto. Ogni parola viene trattata come un elemento di testo separato. </p> </li> 
     <li> <p><b>[!UICONTROL Find text in]</b> </p> <p>Selezionare i campi di metadati in cui si desidera trovare il testo. Se non si seleziona nulla, i moduli eseguiranno la ricerca in tutti i metadati.</p> </li> 
    </ul> <p>Il modulo restituisce qualsiasi accordo contenente il testo immesso in uno dei campi selezionati. Esempio: inserendo "campagna primaverile" e selezionando le opzioni Titolo e Nota, vengono restituiti tutti i contratti con le parole "Primavera" o "Campagna" in Titolo o Nota.</p> <p>Per ulteriori informazioni sulla ricerca dei campi in [!DNL Adobe Acrobat Sign], vedere "Funzionamento della ricerca di testo" in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] Ricerca - Funzionamento</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created date]</td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di creazione corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di scadenza corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Modified date]</p> </td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di modifica corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p> L’ID esterno è un ID del contratto assegnato dal mittente e che può essere in qualsiasi forma, ma in genere è un "&lt;groupID&gt;:&lt;ID&gt;".</p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td> <p>L’ID gruppo è un identificatore assegnato al momento della creazione del gruppo.</p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Questo è l’ID assegnato al contratto specifico. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent ID]</td> 
   <td> <p>Questo è l'ID assegnato all'oggetto padre dell'accordo. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant email]</td> 
   <td> <p>L’indirizzo e-mail di un partecipante. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Selezionare i ruoli da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td>Se si desidera che il modulo disponga i risultati, selezionare il campo in base al quale si desidera ordinare i risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort orde]r</td> 
   <td>Se desideri che il modulo disponga i risultati, seleziona se desideri disporre in ordine crescente o decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Selezionare gli stati da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selezionare i tipi di contratto da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subtypes]</td> 
   <td>Selezionare i sottotipi di contratto che si desidera includere nei risultati restituiti. Solo i sottotipi della funzionalità degli accordi modello di libreria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> <p>L’ID utente dell’utente con cui è condiviso l’accordo.</p> <p>Per ogni ID utente che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID utente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Selezionare il livello di visibilità che si desidera includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start index]</td> 
   <td> <p>Immettere la posizione del primo risultato che si desidera restituire. Combina questo con [!UICONTROL maximum returned results] per impaginare i risultati</p> <p>Esempio: se vengono restituiti 100 risultati alla volta, immettere 100 per restituire i risultati compresi tra 100 e 200.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che si desidera vengano inseriti nel modulo in [action] durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
