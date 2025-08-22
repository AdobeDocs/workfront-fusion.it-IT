---
title: Moduli Adobe Acrobat Sign
description: Con i moduli  [!DNL Adobe Acrobat Sign] , puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell'account Acrobat Sign [!DNL Adobe] , creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '6790'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign] moduli

Con i moduli [!DNL Adobe Acrobat Sign], è possibile avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell&#39;account [!DNL Adobe Acrobat Sign], creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.

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

![Raccomandazioni per Adobe Sign](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign] moduli e relativi campi

Quando si configurano [!DNL Adobe Acrobat Sign] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Acrobat Sign], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

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

+++ **[!UICONTROL Verifica accordi]**

Questo modulo di attivazione avvia uno scenario quando viene creato o aggiornato un accordo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Specificare se si desidera controllare i nuovi record, i record aggiornati o entrambi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record] </td> 
   <td>Selezionare il tipo di record che si desidera controllare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trova testo]</td> 
   <td> <p>Immettere i termini che si desidera cercare. Il modulo restituisce record che includono questi termini come valori di campo.</p> <p>Per ulteriori informazioni sulla ricerca dei campi in [!DNL Adobe Acrobat Sign], vedere "Funzionamento della ricerca di testo" in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Ricerca di Adobe Sign - Funzionamento</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di contratti restituiti]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Controlla eventi]**

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
   <td role="rowheader">[!UICONTROL Nome webhook]</td> 
   <td> <p>Immetti un nome per il webhook</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ambiti]</td> 
   <td> 
    <ul> 
     <li> <p>Account </p> </li> 
     <li> <p>[!UICONTROL Group]</p> </li> 
     <li> <p>[!UICONTROL Utente]</p> </li> 
     <li> <p>[!UICONTROL Resource]</p> <p>Se si seleziona [!UICONTROL Risorsa], immettere l'ID risorsa e il tipo di risorsa.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Livello di risorsa]</td> 
   <td> <p>Seleziona il tipo di risorsa da monitorare.</p> 
    <ul> 
     <li> <p>[!UICONTROL Contratti]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL Megasigns]</p> </li> 
     <li> <p>[!UICONTROL Documenti Libreria]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook subscription events]</td> 
   <td>Selezionare gli eventi [!DNL Adobe Sign] che si desidera controllare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome visualizzato applicazione]</td> 
   <td>Il nome visualizzato dell’applicazione attraverso la quale viene creato il webhook.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome applicazione]</td> 
   <td>Il nome visualizzato dell’applicazione attraverso la quale viene creato il webhook.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-mail di notifica problema]</td> 
   <td> <p>Questa impostazione funziona solo per gli account amministratore</p> <p>Per ogni indirizzo di posta elettronica a cui si desidera inviare le e-mail di notifica del problema, fare clic su <b>[!UICONTROL Add]</b> e immettere l'indirizzo di posta elettronica.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parametri condizionali dell'accordo]</td> 
   <td>Se si desidera aggiungere parametri condizionali, selezionare <b>[!UICONTROL Sì]</b> nel tipo di record a cui si desidera aggiungere i parametri, quindi selezionare <b>[!UICONTROL Sì]</b> in tutti i parametri che si desidera abilitare.</td> 
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

+++ **[!UICONTROL Crea un record]**

Questo modulo di azione crea un nuovo record del tipo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da creare.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Documento libreria]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Utente]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Modulo Web] ([!UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group info]</td> 
   <td> <p>Immetti o mappa il [!UICONTROL Name] e il [!UICONTROL ID] del gruppo e indica se questo gruppo è il gruppo predefinito per l'account.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni documento libreria]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File da inviare]</b> </p> <p>Per ogni file da aggiungere, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi.</p> 
      <ul> 
       <li><b>[!UICONTROL ID documento transitorio]</b> <p>Immettere l'ID del documento transitorio</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL MIME-Type]</b> </p> <p>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere un nome per il file.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL del file che si desidera inviare.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Seleziona se il documento deve essere autenticato o meno.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Nome modello libreria]</b> </p> <p>Inserisci o mappa il nome del modello della libreria</p> </li> 
     <li> <p><b>[!UICONTROL Modalità di condivisione]</b> </p> <p>Specificare gli utenti a cui assegnare l'accesso al documento della raccolta.</p> </li> 
     <li> <p><b>[!UICONTROL Stato documento libreria]</b> </p> <p>Specificare se il documento è in stato di creazione o attivo.</p> </li> 
     <li> <p><b>[!UICONTROL Tipo di modello libreria]</b> </p> <p>Per ogni tipo di modello di libreria che si desidera utilizzare, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il tipo di modello.</p> </li> 
     <li> <p><b>[!UICONTROL Data ultimo evento]</b> </p> <p>Immettere l'ultima data in cui si è verificato un evento nel documento di libreria.</p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Stato documento libreria]</b> </p> <p>Selezionare lo stato del documento della raccolta.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni utente]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-Mail]</b> </p> <p>Inserisci l’indirizzo e-mail dell’utente.</p> </li> 
     <li> <p><b>[!UICONTROL È l'amministratore dell'account]</b> </p> <p>Seleziona questa opzione se l’utente creato è un amministratore account.</p> </li> 
     <li> <p><b>[!UICONTROL ID utente]</b> </p> <p>Inserisci l’ID univoco dell’utente</p> </li> 
     <li> <p><b>[!UICONTROL ID account]</b> </p> <p>Immettere l'ID univoco dell'account [!DNL Adobe Acrobat Sign] associato a questo utente.</p> </li> 
     <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere il nome dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Cognome]</b> </p> <p>Inserisci il cognome dell’utente</p> </li> 
     <li> <p><b>[!UICONTROL Company]</b> </p> <p>Immettere il nome dell'azienda dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Iniziali]</b> </p> <p>Immettere le iniziali dell'utente.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
     <li> <p><b>[!UICONTROL Telefono]</b> </p> <p>Immettere il numero di telefono dell'utente</p> </li> 
     <li> <p><b>ID gruppo primario</b> </p> <p>Immettere il gruppo a cui viene aggiunto il nuovo utente. Se non viene immesso alcun valore, l'utente verrà aggiunto al gruppo predefinito per l'account.</p> </li> 
     <li> <p><b>[!UICONTROL Titolo processo]</b> </p> <p>Immetti la qualifica dell’utente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni modulo Web]</td> 
   <td> <p>Compila i campi seguenti</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Informazioni file]</b> </p> <p>Per ogni file che si desidera aggiungere al modulo Web, fare clic su Aggiungi e compilare i campi seguenti:</p> 
      <ul> 
       <li> <p>[!UICONTROL Tipo di file]</p> <p>[!UICONTROL Documento]</p> </li> 
       <li> <p>[!UICONTROL Documento transitorio]</p> </li> 
       <li> <p>[!UICONTROL URL file info]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Nome modulo Web]</b> </p> <p>Immettere un nome per il modulo Web. Questo nome viene utilizzato per identificare il modulo web in luoghi quali e-mail e siti web.</p> </li> 
     <li> <p><b>[!UICONTROL Stato modulo Web]</b> </p> <p>Seleziona lo stato in cui creare il nuovo modulo web.</p> </li> 
     <li> <p><b>[!UICONTROL Informazioni sul set di partecipanti al modulo Web]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Informazioni membro]</b> </p> <p>Per ogni membro che si desidera aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL E-Mail]</b> </p> <p>Lascia vuota questa opzione.</p> </li> 
         <li> <p><b>[!UICONTROL Opzione di sicurezza]</b> </p> <p>Se si desidera aggiungere un'opzione di protezione per l'autenticazione dell'utente, selezionare <b>[!UICONTROL Sì]</b>, quindi selezionare l'opzione di protezione e compilare i campi necessari.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Ruolo]</b> </p> <p>Seleziona il ruolo. Tutti i membri di questo set di partecipanti condividono il ruolo.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Modulo Web aggiuntivo Informazioni sul partecipante]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Informazioni membro]</b> </p> <p>Per ogni membro che si desidera aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL E-Mail]</b> </p> <p>Lascia vuota questa opzione.</p> </li> 
         <li> <p><b>[!UICONTROL Opzione di sicurezza]</b> </p> <p>Se si desidera aggiungere un'opzione di protezione per l'autenticazione dell'utente, selezionare <b>[!UICONTROL Sì]</b>, quindi selezionare l'opzione di protezione e compilare i campi necessari.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Ruolo]</b> </p> </li> 
       <li> <p><b>[!UICONTROL ID partecipante al modulo Web] </b> </p> <p>Immetti l’ID del partecipante al modulo web.</p> </li> 
       <li> <p><b>[!UICONTROL Ordine]</b> </p> <p>Specifica l’ordine in cui il set di partecipanti deve interagire con il modulo web. Ad esempio, il gruppo di partecipanti con un valore di ordine pari a 1 deve andare per primo, 2 deve andare per secondo e così via. I numeri di ordine devono iniziare con uno e non devono presentare spazi vuoti nella serie. </p> </li> 
       <li> <p><b>[!UICONTROL Informazioni sul set di partecipanti al provider]</b> </p> <p>Se il partecipante è sconosciuto, specificare se il provider deve fornire i dettagli per il partecipante e immettere un messaggio con i dettagli richiesti per il partecipante sconosciuto.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Informazioni sull'errore di autenticazione]</b> </p> <p>Se si desidera fornire una pagina di errore o di errore per gli utenti, selezionare <b>[!UICONTROL Sì]</b>, quindi compilare i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL per la pagina di errore</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Abilita questa opzione se desideri che la pagina di errore venga visualizzata nel modulo web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Immettere il ritardo, in secondi, prima che l'utente venga reindirizzato alla pagina di errore.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Informazioni CC]</b> </p> <p>Per ogni indirizzo e-mail a cui si desidera inviare un messaggio e-mail al momento della firma del contratto finale nel modulo Web, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo e-mail.</p> </li> 
     <li> <p><b>[!UICONTROL informazioni di completamento]</b> </p> <p style="font-style: normal;">Se desideri fornire una pagina di successo per i tuoi utenti, seleziona <b>[!UICONTROL Sì]</b>, quindi compila i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Inserisci l’URL per la pagina di successo</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Abilita questa opzione se desideri che la pagina di successo venga visualizzata all’interno del modulo web</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Immetti il ritardo, in secondi, prima che l’utente venga reindirizzato alla pagina di successo.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL ID gruppo]</b> </p> <p>Immetti l’ID del gruppo a cui appartiene il modulo web. Se non viene immesso alcun valore, il modulo web appartiene al gruppo principale dell’utente dell’account.</p> </li> 
     <li> <p><b>[!UICONTROL Data ultimo evento]</b> </p> <p>Immettere la data in cui si è verificato l'ultimo evento nel modulo Web. Utilizza il formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
     <li> <p><b>[!UICONTROL Opzione di sicurezza]n</b> </p> <p>Immettere la password utilizzata per proteggere il documento. Devi comunicare separatamente questa password a tutte le parti interessate.</p> </li> 
     <li> <p><b>[!UICONTROL Informazioni archiviazione]</b> </p> <p>Se l'account è impostato per il vaulting dei documenti e l'opzione per l'abilitazione per ogni contratto, è possibile abilitare questa opzione per il vaulting del contratto.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea un contratto]**

Questo modulo di azione crea un accordo, lo invia per la firma e restituisce l’ID dell’accordo.

>[!NOTE]
>
>È consigliabile caricare il documento per firmarlo come documento transitorio, quindi eseguirne il mapping al campo [!UICONTROL File da inviare] nel modulo [!UICONTROL Crea accordo]. Ad esempio, consulta &quot;Caricare un documento&quot; in questo articolo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Files to send]</td> 
   <td> <p>Per ogni elemento che si desidera includere nel contratto, fare clic su <b>[!UICONTROL Add Item]</b> e compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Tipo di file]</b> </p> 
      <ul> 
       <li> <p><b></b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Data di creazione]</b> </p> <p>Immettere o mappare la data di creazione del documento nel formato <code>yyyy-MM-dd'T'HH:mm:ssZ</code>. Ad esempio, <code>2016-02-25T18:46:19Z</code> rappresenta l'ora UTC.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Immettere o mappare l'ID del documento.</p> </li> 
         <li> <p><b>[!UICONTROL Etichetta]</b> </p> <p>Immettere o mappare un'etichetta univoca per il file. In caso di flusso di lavoro personalizzato, questo mapperà un file all’elemento file corrispondente nella definizione del flusso di lavoro. Questo deve essere specificato in caso di richiesta di creazione di accordi di flusso di lavoro personalizzati.</p> </li> 
         <li> <p><b>[!UICONTROL Numero di pagine]</b> </p> <p>Immettere o mappare il numero di pagine nel documento.</p> </li> 
         <li> <p><b>[!UICONTROL MIME-Type]</b> </p> <p>Immetti o mappa il tipo MIME del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere o associare un nome per il documento.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL ID documento libreria]</b> </p> <p>Immettere l'ID del documento di libreria</p> </li> 
       <li> <p><b>[!UICONTROL ID documento transitorio]</b> </p> <p>Immettere l'ID del documento transitorio</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Compila i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL MIME-Type]</b> </p> <p>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere un nome per il file.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Immettere l'URL del file che si desidera inviare.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Etichetta]</b> </p> <p>Immettere un'etichetta per il file.</p> </li> 
     <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Abilita questa opzione per indicare che il file deve essere notarizzato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome accordo]</td> 
   <td>Immettere un nome per il nuovo contratto. Questo nome viene utilizzato per identificare l’accordo in luoghi quali e-mail e siti web.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant imposta le informazioni]</td> 
   <td> <p>Per ogni set di partecipanti che si desidera aggiungere, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi seguenti.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Membri]</b> </p> <p>Per ogni persona che si desidera aggiungere al set di partecipanti, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo e-mail della persona.</p> </li> 
     <li> <p><b>[!UICONTROL Ordine]</b> </p> <p>Specificare l'ordine di firma del contratto da parte del set di partecipanti. Ad esempio, il gruppo di partecipanti con valore di ordine 1 deve firmare per primo, 2 deve firmare per secondo e così via. I numeri di ordine devono iniziare con uno e non devono presentare spazi vuoti nella serie. </p> </li> 
     <li> <p><b>[!UICONTROL Ruolo]</b> </p> <p>Selezionare un ruolo per questo set di partecipanti. Tutti i partecipanti al set ricevono questo ruolo.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Immetti o mappa l'ID di questo set di partecipanti.</p> </li> 
     <li> <p><b>[!UICONTROL Etichetta]</b> </p> <p>Immettere o mappare un'etichetta univoca per il set di partecipanti. Per i flussi di lavoro personalizzati, l’etichetta specificata nel set di partecipazione deve mapparla sul passaggio di partecipazione nel flusso di lavoro personalizzato.</p> </li> 
     <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere un nome per il set di partecipanti. Il nome deve essere univoco all'interno del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Messaggio privato]</b> </p> <p>Immettere o mappare un messaggio per questo set di partecipanti. Tutti i partecipanti al set ricevono questo messaggio.</p> </li> 
     <li> <p><b>[!UICONTROL Pagine visibili]</b> </p> <p>Se per questo contratto è abilitata la visibilità limitata dei documenti, specificare quali file sono visibili a questo set di partecipanti. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di firma]</td> 
   <td> <p>Selezionare il tipo di firma richiesto dal contratto.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>La convenzione deve essere firmata elettronicamente.</p> </li> 
     <li> <p><b>[!UICONTROL Scritto]</b> </p> <p>Il contratto deve essere firmato manualmente e deve essere analizzato e caricato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>Selezionare uno stato per il contratto.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>È comunque possibile modificare o aggiungere campi al contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Bozza]</b> </p> <p>Puoi creare questo contratto in modo incrementale prima di inviarlo.</p> </li> 
     <li> <p><b>[!UICONTROL In Corso]</b> </p> <p>L'accordo sarà inviato immediatamente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CCs]</td> 
   <td> <p>Puoi inviare il presente contratto a parti interessate che non hanno bisogno di firmare, ad esempio le parti interessate. Ricevono un’e-mail all’inizio del processo di firma e un’altra all’atto della ricezione della firma finale. Inoltre, ricevono una copia PDF del contratto. </p> <p>Per ogni persona che si desidera inserire nel contratto, fare clic su <b>[!UICONTROL Aggiungi elemento]</b> e compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-Mail]</b> </p> <p>Immetti o mappa l’indirizzo e-mail che desideri usare come CC nel contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Etichetta]</b> </p> <p>Immetti o mappa un’etichetta per questo indirizzo e-mail, come mostrato nella descrizione del flusso di lavoro</p> </li> 
     <li> <p><b>[!UICONTROL Pagine visibili]</b> </p> </li> 
     <li> <p>Se per questo contratto è abilitata la visibilità limitata dei documenti, specificare quali file sono visibili a questo set di partecipanti. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Per ogni tipo di e-mail, seleziona se il tipo di e-mail viene inviato a tutti i partecipanti o se non ne viene inviato alcuno.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Completion Email]</b> </p> <p>Invia un messaggio di posta elettronica quando il contratto viene completato, annullato, scaduto o rifiutato.</p> </li> 
     <li> <p><b>[!UICONTROL E-Mail In-Flight]</b> </p> <p>Inviato un messaggio e-mail quando il contratto viene delegato o sostituito.</p> </li> 
     <li> <p><b>[!UICONTROL E-mail di avvio contratto]</b> </p> <p>Invia un messaggio di posta elettronica quando viene creato il contratto o quando viene richiesta un'azione.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID esterno]</td> 
   <td> <p>Immettere o mappare un ID per il contratto. È possibile specificare questo valore al momento della creazione dell'accordo e utilizzarlo per individuare l'accordo nei moduli o nelle query successive.</p> <p>Nota: il valore ID esterno è visibile a tutti i partecipanti tramite l’API, pertanto non deve essere utilizzato per contenere un token sensibile.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Unisci informazioni campo]</td> 
   <td> <p>Per ogni campo del contratto per cui si desidera inserire un valore predefinito, fare clic su <b>[!UICONTROL Add item]</b> e immettere il valore predefinito e il nome del campo.</p> <p>I valori verranno presentati ai firmatari per i campi modificabili. Per i campi di sola lettura, i valori forniti non saranno modificabili durante il processo di firma.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni notaio]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Appuntamento]</b> </p> <p>Immettere o mappare un'ora e una data proposte per l'appuntamento per la registrazione del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Nota]</b> </p> <p>Immettere o mappare le note da includere sulla sessione notarile.</p> </li> 
     <li> <p><b>[!UICONTROL Pagamento]</b> </p> <p>Seleziona se il notaio è pagato dal firmatario o dal mittente del contratto.</p> </li> 
     <li> <p><b>[!UICONTROL Notary Type]</b> </p> <p>Seleziona il tipo di notaio</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider notary]</p> <p>Il notaio è prestato dal notaio.</p> </li> 
       <li> <p>[!UICONTROL BYON notary]</p> <p>Il notaio è fornito dal cliente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Opzione firma post]</td> 
   <td> <p>Selezionare se si desidera che i firmatari vengano indirizzati a una pagina di successo dopo la firma del contratto. Se si seleziona <b>[!UICONTROL Sì]</b>, compilare i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Ritardo reindirizzamento]</b> </p> <p>Inserisci o mappa un numero che rappresenta il numero di secondi prima che il firmatario venga reindirizzato alla pagina riuscita. Se questo valore è maggiore di 0, l'utente visualizzerà prima il messaggio di successo standard di [!DNL Adobe Sign] e quindi, dopo un ritardo, verrà reindirizzato alla pagina di successo.</p> </li> 
     <li> <p><b>[!UICONTROL URL reindirizzamento]</b> </p> <p>Immetti o mappa un URL accessibile al pubblico a cui l’utente verrà inviato dopo aver completato correttamente il processo di firma.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL opzione di protezione]</td> 
   <td> <p>Immettere o mappare la password secondaria che verrà utilizzata per proteggere il documento PDF. </p> <p>Importante: [!DNL Adobe Sign] non condividerà mai questa password, pertanto devi comunicarla separatamente a tutte le parti interessate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni archiviazione]</td> 
   <td>Se l'account è impostato per il vaulting dei documenti e l'opzione per l'abilitazione per ogni contratto, è possibile abilitare questa opzione per il vaulting del contratto.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea record correlati]**

Questo modulo di azione crea record collegati a un modulo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record originale a cui si desidera associare i record creati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera associare il record creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campo correlato all'accordo]</td> 
   <td> <p>Seleziona il tipo di campo correlato da creare</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Campi modulo]</b> </p> <p>Immettere l'ID modello del modello contenente i campi che si desidera creare</p> </li> 
     <li> <p><b>[!UICONTROL Promemoria]</b> </p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL ID partecipante destinatario]</b> </p> <p>Per ogni partecipante a cui si desidera inviare un promemoria, fare clic su [!UICONTROL Aggiungi elemento] e immettere l'ID del partecipante.</p> </li> 
       <li> <p><b>[!UICONTROL Stato]</b> </p> <p>Per i nuovi record, lo stato deve essere [!UICONTROL Attivo].</p> </li> 
       <li> <p><b>[!UICONTROL Primo ritardo promemoria]</b> </p> <p>Immetti il ritardo in ore prima di inviare il primo promemoria. Il valore minimo consentito è di 1 ora e il valore massimo non può essere maggiore della differenza tra la creazione del contratto e la scadenza del contratto espressa in ore. Se questo ritardo non è impostato, il primo promemoria sarà basato sulla frequenza.</p> </li> 
       <li> <p><b>[!UICONTROL Frequenza promemoria]</b> </p> <p>Impostare la frequenza di invio del promemoria. Se non viene specificata la frequenza, il promemoria verrà inviato una volta.</p> </li> 
       <li> <p><b>[!UICONTROL Data ultimo invio]</b> </p> <p>Questo campo viene impostato dal sistema.</p> </li> 
       <li> <p><b>[!UICONTROL Next sent date]</b> </p> <p>Questo campo deve essere vuoto o impostato su [!UICONTROL ONCE].</p> </li> 
       <li> <p><b>[!UICONTROL Nota]</b> </p> <p>Immettere una nota da includere nel promemoria. Questo è utile per spiegare al partecipante perché è necessaria la sua partecipazione.</p> </li> 
       <li> <p><b>[!UICONTROL Avvia contatore promemoria da]</b> </p> <p>Selezionare se il promemoria viene inviato in base alla data di creazione dell'accordo quando diventa disponibile.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Rapporto identità firmatario]</b> </p> <p>Immettere la password utilizzata per proteggere il documento PDF.</p> </li> 
     <li> <p><b>[!UICONTROL Viste]</b> </p> <p>Immetti i campi seguenti</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Selezionate il nome della vista da creare.</p> </li> 
       <li> <p><b>[!UICONTROL Utente di accesso automatico]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'URL restituito.</p> </li> 
       <li> <p><b>[!UICONTROL Frame Parent]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
       <li> <p><b>[!UICONTROL Nessun flag Chrome]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
       <li> <p><b>[!UICONTROL può modificare i file]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera modificare la sezione di caricamento dei file aggiungendo o rimuovendo file. Questo non è un meccanismo di controllo degli accessi. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Documento libreria]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera che i collegamenti ai documenti della raccolta siano visibili. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL File locale]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera visualizzare il pulsante Caricamento file locale. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Connettori Web]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera visualizzare i collegamenti per allegare i documenti da origini Web. Il valore predefinito è Sì.</p> </li> 
       <li> <p><b>[!UICONTROL è selezionato in anteprima]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per impostare la pagina di composizione in modalità di creazione.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Condivisione membro]</b> </p> <p>Per ogni membro con cui si desidera condividere il contratto, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo di posta elettronica del membro e un messaggio per tale membro.</p> </li> 
     <li> <p>[!UICONTROL Delega set partecipanti]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL ID set partecipanti]</b> </p> <p>Inserisci l'ID del set di partecipanti</p> </li> 
       <li> <p><b>[!UICONTROL Informazioni membro]</b> </p> <p>Per ogni membro che si desidera aggiungere, fare clic su [!UICONTROL Aggiungi elemento] e immettere l'indirizzo di posta elettronica e le informazioni relative al telefono per il membro.</p> </li> 
       <li> <p><b>[!UICONTROL Messaggio privato]</b> </p> <p>Immetti un messaggio. Tutti i membri del set di partecipanti ricevono questo messaggio.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni vista libreria]</td> 
   <td> <p>Compila i campi seguenti:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immetti un nome per il modello della libreria. Questo nome viene utilizzato nelle e-mail e nei siti web.</p> </li> 
     <li> <p><b>[!UICONTROL Utente di accesso automatico]</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per accedere automaticamente all'URL restituito.</p> </li> 
     <li> <p><b>[!UICONTROL Frame principale]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
     <li> <p><b>[!UICONTROL Nessun flag Chrome]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
     <li> <p><b>[!UICONTROL Invia configurazione visualizzazione]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera configurare la visualizzazione [!UICONTROL Invia], quindi compilare i campi seguenti.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Nome accordo]</b> </p> <p>Immettere o mappare il nome del contratto per il documento di libreria nella pagina di composizione.</p> </li> 
       <li> <p><b>[!UICONTROL può modificare i file]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera modificare la sezione di caricamento dei file aggiungendo o rimuovendo file. Questo non è un meccanismo di controllo degli accessi. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL File locale]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera che i collegamenti ai documenti della raccolta siano visibili. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Connettori Web]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera visualizzare i collegamenti per allegare i documenti da origini Web. Il valore predefinito è [!UICONTROL Yes].</p> </li> 
       <li> <p><b>Anteprima selezionata</b> </p> <p>Selezionare <b>[!UICONTROL Yes]</b> per impostare la pagina di composizione in modalità di creazione.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Informazioni visualizzazione utente]</td> 
   <td> <p>Compila i campi seguenti</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Seleziona il nome della visualizzazione utente richiesta.</p> </li> 
     <li> <p><b>[!UICONTROL Utente di accesso automatico]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per accedere automaticamente all'utente. Selezionare <b>[!UICONTROL No]</b> per richiedere le credenziali. Il valore predefinito è [!UICONTROL No].</p> </li> 
     <li> <p><b>[!UICONTROL Frame principale]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
     <li> <p><b>Nessun flag Chrome</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Campi correlati a [!UICONTROL Widget]</td> 
   <td> <p>Selezionare il record correlato da creare.</p> 
    <ul> 
     <li> <p>Visualizzazioni di </p> <p>Compila i campi seguenti.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Seleziona il nome della visualizzazione del modulo web richiesta</p> </li> 
       <li> <p><b>[!UICONTROL Utente di accesso automatico]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per accedere automaticamente all'utente. Selezionare <b>[!UICONTROL No]</b> per richiedere le credenziali. Il valore predefinito è [!UICONTROL No].</p> </li> 
       <li> <p><b>[!UICONTROL Frame principale]</b> </p> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere la lingua in cui si desidera creare la visualizzazione. </p> </li> 
       <li> <p><b>[!UICONTROL Nessun flag Chrome]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per visualizzare la pagina incorporata senza intestazione o piè di pagina di navigazione.</p> </li> 
       <li> <p>[!UICONTROL Configurazione della vista di firma personalizzata]</p> <p>Se si desidera configurare una visualizzazione della firma personalizzata, selezionare <b>[!UICONTROL Sì]</b> e compilare i campi seguenti:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL E-Mail]</b> </p> <p>Immetti l’indirizzo e-mail della persona che riceve il modulo web appena creato</p> </li> 
         <li> <p><b>[!UICONTROL Comment]</b> </p> <p>Inserisci un commento che descrive come il chiamante API ha stabilito l’identità del firmatario. Queste informazioni vengono visualizzate nell'audit trail [!DNL Adobe Acrobat Sign].</p> </li> 
         <li> <p><b>[!UICONTROL Scadenza]</b> </p> <p>Immetti una data di scadenza per la personalizzazione del modulo web. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Riutilizzabile]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> se si desidera che il firmatario desiderato sia in grado di firmare il modulo più di una volta.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Condivisione membro]</b> </p> <p>Per ogni membro con cui si desidera condividere il contratto, fare clic su <b>[!UICONTROL Add item]</b> e immettere l'indirizzo di posta elettronica del membro e un messaggio per tale membro.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Chiamata API personalizzata]**
Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
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
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query] </td> 
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
   <td role="rowheader">[!UICONTROL Carica un documento transitorio]</td> 
   <td> <p>Se si desidera caricare un documento transitorio, immettere il file di origine del documento che si desidera caricare.</p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca record]**

Questo modulo di azione elenca tutti i record del tipo selezionato a cui l’account ha accesso.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID esterno]</td> 
   <td>Immettere o mappare l'ID esterno (un ID assegnato all'esterno di [!DNL Adobe Acrobat Sign]) per i contratti che si desidera restituire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID gruppo]</td> 
   <td>Immettere l'ID del gruppo associato ai record da elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra elementi nascosti (record)]</td> 
   <td>Abilitare questa opzione se si desidera includere i record nascosti nei risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start Index]</td> 
   <td> <p>Immettere il numero del primo record restituito dal modulo. </p> <p>Nota: questo campo è combinato con il campo [!UICONTROL Maximum number of returned records] per l'impaginazione. Ad esempio, se il numero massimo di eventi restituiti è 100 e l'indice [!UICONTROL Start] è 101, il modulo restituisce i record 101-200 o la seconda pagina di risultati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di record restituiti]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> <p>Nota: questo campo è combinato con il campo [!UICONTROL Cursor] o [!UICONTROL Start Index] per l'impaginazione. Ad esempio, se il numero massimo di eventi restituiti è 100 e l'indice [!UICONTROL Start] è 101, il modulo restituisce i record 101-200 o la seconda pagina di risultati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL del dominio padre]</td> 
   <td> <p>Inserisci o mappa un elenco separato da virgole di URL del dominio principale in cui gli URL restituiti possono essere raggruppati. Se lasciato vuoto, le pagine [!DNL Adobe Acrobat Sign] non sono visualizzabili in iframe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Leggi un record]**

Questo modulo di azione recupera le informazioni da un singolo record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID record]</td> 
   <td>Immettere o mappare l'ID del record che si desidera recuperare.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Leggi record correlati]**

Leggi le informazioni aggiuntive relative a un singolo record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID record] (esempio: [!UICONTROL ID account])</td> 
   <td>Immettere o mappare l'ID del record per il quale si desidera recuperare i record correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altri campi]</td> 
   <td>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aggiorna un record]**

Questo modulo di azione aggiorna un singolo record in [!DNL Adobe Acrobat Sign].

>[!IMPORTANT]
>
>* Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.
>* Alcuni aggiornamenti presentano campi obbligatori. Quando configuri l’aggiornamento, assicurati di compilare tutti i campi obbligatori. I campi obbligatori sono in grassetto nei moduli di Workfront Fusion.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID record] </td> 
   <td>Immetti o mappa l’ID del record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altri campi]</td> 
   <td> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Contratto]</b> </p> <p>Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.</p> </li> 
     <li> <p><b>[!UICONTROL Documento libreria]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Stato]</b> </p> <p>Selezionare il nuovo stato per il documento di libreria.</p> </li> 
       <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Inserisci o mappa il nome del modello della libreria</p> </li> 
       <li> <p><b>[!UICONTROL Modalità di condivisione]</b> </p> <p>Specificare gli utenti a cui assegnare l'accesso al documento della raccolta.</p> </li> 
       <li> <p><b>[!UICONTROL Tipo di modello libreria]</b> </p> <p>Per ogni tipo di modello di libreria che si desidera utilizzare, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il tipo di modello.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Utente]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere il nome dell'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Cognome]</b> </p> <p>Inserisci il cognome dell’utente</p> </li> 
       <li> <p><b>[!UICONTROL Company]</b> </p> <p>Immettere il nome dell'azienda dell'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Telefono]</b> </p> <p>Immettere il numero di telefono dell'utente</p> </li> 
       <li> <p><b>[!UICONTROL ID gruppo primario]</b> </p> <p>Immettere il gruppo a cui viene aggiunto il nuovo utente. Se non viene immesso alcun valore, l'utente verrà aggiunto al gruppo predefinito per l'account.</p> </li> 
       <li> <p><b>[!UICONTROL Titolo processo]</b> </p> <p>Immetti la qualifica dell’utente.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Modulo Web] ([!UICONTROL widget])</b> </p> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Aggiorna record correlato]**

Questo modulo di azione aggiorna i record relativi a un oggetto specifico.

>[!IMPORTANT]
>
>* Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.
>* Alcuni aggiornamenti presentano campi obbligatori. Quando configuri l’aggiornamento, assicurati di compilare tutti i campi obbligatori. I campi obbligatori sono in grassetto nei moduli di Workfront Fusion.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record al quale sono associati i campi correlati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Immettere o mappare l'ID dell'oggetto a cui si desidera associare il record creato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altri campi]</td> 
   <td> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Contratto]</b> </p> <p>Come best practice, se si prevede di apportare modifiche sostanziali a un accordo, si consiglia di creare un nuovo accordo anziché aggiornare quello esistente.</p> </li> 
     <li> <p><b>[!UICONTROL Documento libreria]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selezionare il nuovo stato per il documento di libreria.</p> </li> 
       <li> <p><b>[!UICONTROL Nota]</b> </p> <p>Immettere o mappare il testo della nota.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Specificare se visualizzare o nascondere il documento della raccolta.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Utente]</b> </p> <p>Seleziona i campi da aggiornare, quindi compila i campi selezionati:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Elenco informazioni gruppo]</b> </p> <p>Compila i campi seguenti</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Stato]</b> </p> <p>Seleziona il nuovo stato per l’utente.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Inserisci l’ID univoco del gruppo</p> </li> 
         <li> <p><b>[!UICONTROL È amministratore gruppo]</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per impostare l'utente come amministratore del gruppo.</p> </li> 
         <li> <p><b>È un gruppo primario</b> </p> <p>Selezionare <b>[!UICONTROL Sì]</b> per aggiornare questo gruppo al gruppo primario dell'utente.</p> </li> 
         <li> <p><b>[!UICONTROL Data di creazione]</b> </p> <p>Immettere la data di creazione del gruppo.</p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Tipo di coercizione in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Nome]</b> </p> <p>Immettere o mappare il nome del gruppo.</p> </li> 
         <li> <p><b>[!UICONTROL Creazione documento libreria visibile]</b> </p> <p>Queste impostazioni determinano se l'utente può creare documenti della libreria</p> 
          <ul> 
           <li> <p>Valore </p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL ereditato]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Invio limitato a flussi di lavoro]</b> </p> <p>Queste impostazioni determinano se l'utente può creare accordi solo utilizzando flussi di lavoro.</p> 
          <ul> 
           <li> <p>Valore </p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL ereditato]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Utente può inviare]</b> </p> 
          <ul> 
           <li> <p>Valore </p> <p>Consenti</p> </li> 
           <li> <p>[!UICONTROL ereditato]</p> <p>Eredita impostazione gruppo da gruppo o account</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selezionare il nuovo stato per l'utente e immettere un commento relativo al motivo per cui si desidera attivare o disattivare l'utente.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Immettere le impostazioni locali dell'utente. Questo determina la lingua dell’interfaccia utente. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Modulo Web] ([!UICONTROL widget])</b> </p> <p>Immettere le informazioni in campi specifici in base al tipo di record e ai campi correlati.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Carica documento]**

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID record]</td> 
   <td>Immetti o mappa l’ID del record da aggiornare</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL tipo MIME]</td> 
   <td>Immetti il tipo mime del file originale. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME <code>text/html</code> verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME <code>image/jpeg</code>.</td> 
  </tr> 
 </tbody> 
</table>

**Esempio:** In questo flusso di lavoro, il documento da firmare (precedentemente scaricato da Workfront) viene caricato come documento transitorio.

(/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

Il modulo [!UICONTROL Carica documento] assegna al documento un ID [!DNL Adobe Acrobat Sign] a cui è possibile fare riferimento nei moduli successivi. Al momento della creazione del contratto, l&#39;ID del documento caricato viene incluso nel campo [!UICONTROL File da inviare].

![Firma esempio](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Ricerche

+++ **[!UICONTROL Cerca contratti]**

Questo modulo di ricerca cerca i contratti in base ai criteri specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Acrobat Sign] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro testo]</td> 
   <td> <p>Cercare il testo nei metadati del contratto. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Trova testo]</b> </p> <p>Immettere il testo da trovare nei metadati del contratto. Ogni parola viene trattata come un elemento di testo separato. </p> </li> 
     <li> <p><b></b> Trova testo in </p> <p>Selezionare i campi di metadati in cui si desidera trovare il testo. Se non si seleziona nulla, i moduli eseguiranno la ricerca in tutti i metadati.</p> </li> 
    </ul> <p>Il modulo restituisce qualsiasi accordo contenente il testo immesso in uno dei campi selezionati. Esempio: inserendo "campagna primaverile" e selezionando le opzioni Titolo e Nota, vengono restituiti tutti i contratti con le parole "Primavera" o "Campagna" in Titolo o Nota.</p> <p>Per ulteriori informazioni sulla ricerca dei campi in [!DNL Adobe Acrobat Sign], vedere "Funzionamento della ricerca di testo" in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] Ricerca - Funzionamento</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di creazione]</td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di creazione corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di scadenza]</td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di scadenza corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Data di modifica]</p> </td> 
   <td>Seleziona le date. Il modulo restituisce solo i record in cui la data di modifica corrisponde a questo criterio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID esterno]</td> 
   <td> <p> L’ID esterno è un ID del contratto assegnato dal mittente e che può essere in qualsiasi forma, ma in genere è un "&lt;groupID&gt;:&lt;ID&gt;".</p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID gruppo]</td> 
   <td> <p>L’ID gruppo è un identificatore assegnato al momento della creazione del gruppo.</p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa]</td> 
   <td> <p>Questo è l’ID assegnato al contratto specifico. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID padre </td> 
   <td> <p>Questo è l'ID assegnato all'oggetto padre dell'accordo. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL E-mail partecipante]</td> 
   <td> <p>L’indirizzo e-mail di un partecipante. </p> <p>Per ogni ID esterno che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID esterno.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Selezionare i ruoli da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td>Se si desidera che il modulo disponga i risultati, selezionare il campo in base al quale si desidera ordinare i risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Order]r</td> 
   <td>Se desideri che il modulo disponga i risultati, seleziona se desideri disporre in ordine crescente o decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stato]</td> 
   <td>Selezionare gli stati da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selezionare i tipi di contratto da includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sottotipi]</td> 
   <td>Selezionare i sottotipi di contratto che si desidera includere nei risultati restituiti. Solo i sottotipi della funzionalità degli accordi modello di libreria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID utente]</td> 
   <td> <p>L’ID utente dell’utente con cui è condiviso l’accordo.</p> <p>Per ogni ID utente che desideri aggiungere, fai clic su <b>[!UICONTROL Add]</b> e immetti o mappa l'ID utente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Selezionare il livello di visibilità che si desidera includere nei risultati restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start index]</td> 
   <td> <p>Immettere la posizione del primo risultato che si desidera restituire. Combina questo con il [!UICONTROL maximum returned results] per impaginare i risultati</p> <p>Esempio: se vengono restituiti 100 risultati alla volta, immettere 100 per restituire i risultati compresi tra 100 e 200.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di risultati restituiti]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
