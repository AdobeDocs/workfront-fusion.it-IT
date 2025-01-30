---
title: Moduli Workfront Proof
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Workfront Proof], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2668'
ht-degree: 0%

---

# [!DNL Workfront Proof] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Workfront Proof] e collegarlo a più applicazioni e servizi di terze parti.

Questa opzione è utile se devi eseguire attività attualmente non supportate nella verifica in [!DNL Workfront] o in [!DNL Workfront Proof], ad esempio l&#39;aggiornamento delle bozze in base a determinati eventi e la ricerca dei destinatari di una bozza.

Il connettore [!DNL Workfront Proof] non viene conteggiato rispetto al numero di app attive disponibili per l&#39;organizzazione. Tutti gli scenari, anche se utilizzano solo l&#39;app [!DNL Workfront Proof], vengono conteggiati rispetto al numero totale di scenari dell&#39;organizzazione.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
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

## Informazioni su Workfront Proof

Il connettore Workfront Proof utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Workfront Proof] a [!DNL Workfront Fusion]

Puoi creare una connessione al tuo account [!DNL Workfront Proof] direttamente da un modulo [!DNL Workfront Fusion].

1. In qualsiasi modulo [!DNL Workfront Fusion], fai clic su [!UICONTROL **Aggiungi**] accanto al campo [!UICONTROL Connection]

2. Compila i campi seguenti:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Immetti un nome per la connessione</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Environment]</td>
                <td>Seleziona se si tratta di un ambiente di produzione o non di produzione, ad esempio Anteprima o Sandbox.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Type]</td>
                <td>Specificare se si tratta di un account di servizio o di un account personale.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Email / Username]</td>
                <td>Immettere il nome utente per l'account [!DNL Workfront Proof].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Password]</td>
                <td>Immettere la password per l'account [!DNL Workfront Proof].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant ID]</td>
                <td><strong>Nota</strong>: i clienti che non utilizzano BYOK devono lasciare vuoto questo campo. <p>Immetti l’ID tenant per questo account. Se hai bisogno di aiuto per trovare l’ID tenant, contatta l’Assistenza clienti Workfront.</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain Extension]</td>
                <td>Immetti l’estensione per l’URL utilizzato per accedere al tuo account. <p>Esempio: <code>com</code> o <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Production, Preview, or Custom Environment]</td>
                <td>L’ambiente di produzione, anteprima o personalizzato a cui desideri connetterti.</td>
            </tr>
        </tbody>
    </table>


3. Fai clic su [!UICONTROL **Continua**] per salvare la connessione e tornare al modulo

## [!DNL Workfront Proof] moduli e relativi campi

Quando configuri [!DNL Workfront Proof] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Workfront Proof], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [Osserva riepilogo PDF](#watch-for-pdf-summary)
* [[!UICONTROL Watch Proof Activity]](#watch-proof-activity)
* [Guarda le bozze](#watch-proofs)

#### [!UICONTROL Watch for PDF Summary]

Questo modulo di attivazione immediata esegue uno scenario quando un utente crea un riepilogo di PDF per una bozza.

In questo modulo è necessario un webhook.

Il modulo restituisce tutti i campi standard associati alla bozza, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Viene inoltre creata una nuova sottoscrizione di evento per i riepiloghi PDF e viene restituito il contenuto dall&#39;attributo `pdf_url` inviato nel payload. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook name]</td> 
   <td>Immetti o mappa un nome per il nuovo webhook</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proof Activity]

Questo modulo di attivazione esegue uno scenario quando si verifica un’attività specificata su una bozza di bozza.

Il modulo restituisce tutti i campi standard associati alla bozza, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Viene inoltre creata una nuova sottoscrizione di evento per i riepiloghi PDF e viene restituito il contenuto dall&#39;attributo `pdf_url` inviato nel payload. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Activity type]</td> 
   <td>Seleziona se desideri controllare le nuove decisioni (comprese le modifiche dello stato della bozza) o solo le modifiche generali dello stato della bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proofs]

Questo modulo di attivazione pianificato esegue uno scenario quando un utente crea o prende una decisione su una bozza.

Il modulo restituisce un elenco di tutti i record trovati durante il periodo specificato, insieme ai relativi tipi. Restituisce anche i valori dei campi specificati. Se il modulo ha trovato decisioni prese sulla bozza, include sia i valori precedenti che quelli correnti in campi separati. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Questo si verifica in un intervallo pianificato regolare specificato.

Per recuperare queste informazioni, è necessario disporre delle autorizzazioni necessarie per accedere alla bozza o alle bozze in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td>Seleziona se desideri controllare le nuove bozze o le decisioni globali relative alle nuove bozze.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Limite</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Elementi per pagina</td> 
   <td> <p>Per impaginare i risultati, immettere o mappare il numero di risultati restituiti da visualizzare in ogni pagina dei risultati. Questo numero deve essere minore o uguale a 100.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Create Proof]](#create-proof)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download Proof]](#download-proof)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Request PDF Summary]](#request-pdf-summary)
* [[!UICONTROL Update Proof]](#update-proof)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Proof]

<!--Cannot test Jan 2025-->

Questo modulo di azione crea una nuova bozza o una nuova versione di una bozza in [!DNL Workfront Proof].

Puoi specificare i parametri per la nuova bozza e la bozza sorgente se stai creando una nuova versione.

Il modulo restituisce l’ID della nuova bozza o versione della bozza. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Type]</td> 
   <td> <p>Specificare se si desidera che la bozza creata abbia un flusso di lavoro di base o un [!UICONTROL Automated Workflow].</p> <p>Compila quindi i campi visualizzati per il tipo di bozza scelto. Ad esempio, se hai scelto [!UICONTROL Automated Workflow], compila il campo <strong>[!UICONTROL Workflow Stages]</strong> per configurare le fasi.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allow original file to be downloaded]</td> 
   <td>Seleziona se desideri consentire il download del file originale da cui è stata creata la bozza.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>Seleziona se utilizzi il visualizzatore di bozze classico.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Combine all files into single proof]</td> 
   <td>Abilita questa opzione per combinare tutti i file in un’unica bozza multipagina.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create a new proof version]</td> 
   <td>Seleziona questa opzione se desideri che il modulo crei una nuova versione di una bozza esistente. Quindi, nel campo <strong>[!UICONTROL Existing Proof ID]</strong> visualizzato, mappa o immetti l'ID univoco della bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link Label]</td> 
   <td>Inserisci o mappa un’etichetta per il collegamento della bozza personalizzata.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link URL]</td> 
   <td>Inserisci o mappa l’URL del collegamento personalizzato.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Digita uno dei seguenti numeri per indicare quale delle seguenti impostazioni predefinite di notifica e-mail desideri utilizzare per la bozza creata.
    <ul>
     <li><strong>1</strong> - Tutti i nuovi commenti e risposte</li>
     <li><strong>2</strong> - Risposte ai commenti</li>
     <li><strong>3</strong> - Riepilogo giornaliero</li>
     <li><strong>4</strong> - Riepilogo orario</li>
     <li><strong>5</strong> - Solo decisioni</li>
     <li><strong>9</strong> - Disabilitato</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Excel Summary]</td> 
   <td>Seleziona se vuoi disabilitare la possibilità di scaricare i commenti della bozza in un file Excel.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable PDF Summary]</td> 
   <td>Seleziona se vuoi disabilitare la possibilità di scaricare i commenti della bozza in un file PDF.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Seleziona se vuoi disabilitare l’e-mail di abbonamento per questa bozza.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Embed Player]</td> 
   <td>Seleziona se desideri abilitare il lettore incorporato per questa bozza.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Seleziona se consentire agli utenti non partecipanti di abbonarsi alla bozza.<br>Se si seleziona questa opzione, è anche possibile selezionare il Ruolo predefinito per i sottoscrittori, come descritto in questa tabella.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Specificare se si desidera abilitare la convalida e-mail dell'abbonamento. Se questa opzione è abilitata, l’abbonato deve fare clic su un collegamento in un messaggio e-mail per accedere a una bozza.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Seleziona se desideri che la bozza creata nasconda o mostri l’URL del team.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Hash] <span style="font-weight: normal;">oppure</span> [!UICONTROL File Hashes]</td> 
   <td>Aggiungi l’ID del file o dei file da cui desideri creare una bozza o delle bozze.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Names]</td> 
   <td>Aggiungi il nome o i nomi del file per la bozza creata Questo campo è obbligatorio.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Specifica se desideri che la bozza creata venga bloccata dopo aver preso tutte le decisioni necessarie.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Notify recipients about this proof]</td> 
   <td>Seleziona un’opzione per indicare se desideri che i destinatari ricevano una notifica al momento della creazione della bozza.&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof name]</td> 
   <td>Digita un nome per la bozza creata Questo è un campo obbligatorio. Utilizza un simbolo di barra verticale (|) per separare i nomi per più bozze.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof owner ID]</td> 
   <td>Inserisci o mappa l’ID del proprietario della bozza. Se questo campo viene lasciato vuoto, il proprietario della bozza viene impostato sull’utente corrente.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reference ID]</td> 
   <td>Immetti l’ID di riferimento per la bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require electronic signature]</td> 
   <td>Seleziona se desideri richiedere a chiunque prenda una decisione su una bozza di inviare una firma elettronica.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Specifica se la bozza creata deve richiedere l’accesso. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Resolution ID]</td> 
   <td>Immetti l’ID della risoluzione da utilizzare per la bozza. Per un elenco degli ID risoluzione, consulta la [!DNL Workfront Proof] <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html">documentazione API</a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>Immetti il tipo di bozza SWF.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Show] [elemento]</td> 
   <td>Per ogni elemento, seleziona se desideri visualizzarlo nella bozza.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>Immetti l’ID dell’area di lavoro in cui desideri creare la bozza. </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Recipients]</td> 
   <td>Aggiungi gli indirizzi e-mail dei destinatari desiderati per la bozza creata.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Specifica la scadenza desiderata per la bozza creata. Utilizza il seguente formato data:</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Custom API Call]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Workfront Proof]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Workfront Proof].

Il modulo restituisce il codice di stato, le intestazioni e il corpo. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Method]</td> 
   <td>Imposta l’azione per la chiamata API. Per informazioni sulle azioni disponibili, consulta la <a href="https://api.proofhq.com/">documentazione dell'API Proof</a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Body (XML)]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:**
>
>![Esempio di modulo API di bozza](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Download Proof]

Questo modulo di azione scarica il file sorgente di una particolare bozza che identifichi utilizzando il relativo ID.

Specifica l’ID della bozza.

Il modulo restituisce il contenuto del file di origine utilizzato per creare la bozza.È possibile mappare queste informazioni nei moduli successivi nello scenario.

Per recuperare queste informazioni, è necessario disporre di autorizzazioni sufficienti per accedere al record in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Digitare l'ID univoco della bozza, disponibile nella pagina [!UICONTROL Proof Details].  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

Questo modulo di azione legge i dati da una singola bozza in [!DNL Workfront Proof].

Puoi specificare l’ID della bozza e le informazioni che desideri ricavare dalla bozza.

Il modulo restituisce i valori dei campi scelti per la bozza, insieme ai relativi tipi. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Per recuperare queste informazioni, è necessario disporre di autorizzazioni sufficienti per accedere al record in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Seleziona se desideri leggere una bozza, i commenti della bozza o i revisori della bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID [!DNL Workfront Proof] univoco del record che si desidera venga letto dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Request PDF Summary]

Questo modulo richiede il riepilogo PDF per una determinata bozza in [!DNL Workfront Proof].

Specifica l’ID della bozza.

Il modulo restituisce informazioni di riepilogo PDF. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Per recuperare queste informazioni, è necessario disporre di autorizzazioni sufficienti per accedere al record in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Immettere l'ID [!DNL Workfront Proof] univoco della bozza per la quale si desidera richiedere un riepilogo dei PDF.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback URL]</td> 
   <td>Inserisci o mappa l’URL in cui desideri inviare il riepilogo dei PDF.</td> 
  </tr> 
 </tbody> 
</table>

##### Possibile errore

* **Errore**: &quot;[!UICONTROL You do not have privilege to perform this request. The stage must contain at least one recipient.]&quot;
* **Soluzione**: assicurati di non essere l&#39;unico assegnato alle fasi del flusso di lavoro. Un altro utente deve essere assegnato alle fasi del flusso di lavoro.

#### [!UICONTROL Update Proof]

Questo modulo di azione aggiorna una bozza esistente in [!DNL Workfront Proof].

Puoi specificare l’ID della bozza e il tipo di record, nonché i campi da includere nell’output.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Per recuperare queste informazioni, è necessario disporre di autorizzazioni sufficienti per accedere al record in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Digitare l'ID univoco della bozza, disponibile nella pagina [!UICONTROL Proof Details]. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Specifica la scadenza desiderata per la bozza creata. Utilizza il formato data <code>YYYY-MM-DD hh:mm</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Seleziona una delle seguenti impostazioni predefinite di notifica e-mail da utilizzare per la bozza creata.
    <ul>
     <li> [!UICONTROL All new comments and replies]</li>
     <li>[!UICONTROL Replies to my comments]</li>
     <li>[!UICONTROL Daily summary]</li>
     <li> [!UICONTROL Hourly summary]</li>
     <li> [!UICONTROL Decisions only]</li>
     <li> [!UICONTROL Disabled]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default Role]</td> 
   <td>Seleziona il ruolo predefinito per la bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Seleziona se vuoi disabilitare l’e-mail di abbonamento per questa bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Seleziona se consentire agli utenti non partecipanti di abbonarsi alla bozza.<br>Se si seleziona questa opzione, è anche possibile selezionare un'opzione nel campo [!UICONTROL Default Role].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Specificare se si desidera abilitare la convalida e-mail dell'abbonamento. Se questa opzione è abilitata, l’abbonato deve fare clic su un collegamento in un messaggio e-mail per accedere a una bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Seleziona se desideri che la bozza creata nasconda o mostri l’URL del team.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Specifica se desideri che la bozza creata venga bloccata dopo aver preso tutte le decisioni necessarie.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Message]</td> 
   <td>Immetti o mappa un messaggio da allegare alla bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID] </td> 
   <td>Inserisci o mappa l’ID della bozza da aggiornare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Name]</td> 
   <td>Inserisci o mappa il nome della bozza da aggiornare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Specifica se la bozza creata deve richiedere l’accesso. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show Versions Like]</td> 
   <td>Seleziona se desideri visualizzare un collegamento ad altre versioni di questa bozza.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Inserisci o mappa l’oggetto della bozza</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

Questo modulo di azione carica un file da utilizzare con il modulo [!UICONTROL Create Proof] in [!DNL Workfront Proof].

Il modulo restituisce un ID hash per il file caricato. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL List Workflow Templates]](#list-workflow-templates)
* [[!UICONTROL Search]](#search)

#### [!UICONTROL List Workflow Templates]

Questo modulo di ricerca elenca tutti i modelli di flusso di lavoro disponibili.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di modelli che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

Questo modulo di ricerca cerca i record in un oggetto in [!DNL Workfront Proof] che corrispondono alla query di ricerca specificata.

Il modulo restituisce l’ID della bozza se sta cercando una bozza. In alternativa, restituisce gli ID utente, le e-mail, i nomi, le posizioni e gli alias e-mail dei destinatari, se è in corso la ricerca dei destinatari. È possibile mappare queste informazioni nei moduli successivi nello scenario.

Per recuperare queste informazioni, è necessario disporre di autorizzazioni sufficienti per accedere al record in [!DNL Workfront Proof].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Workfront Proof] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Search for]</td> 
   <td> <p>Selezionare il tipo di record da cercare nel modulo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Proof]</strong> </p> <p>Immetti il Nome bozza della bozza da cercare.</p> </li> 
     <li> <p><strong>[!UICONTROL Recipient]</strong> </p> <p>Immetti l’indirizzo e-mail del destinatario da cercare.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Indica se il modulo cercherà <strong>[!UICONTROL All Matching Records]</strong> o solo <strong>[!UICONTROL First Matching Record]</strong>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort By]</td> 
   <td>Selezionare il campo in base al quale ordinare i risultati.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sorting Direction]</td> 
   <td> <p>Seleziona se desideri ordinare i risultati in modo crescente o decrescente.</p> </td> 
  </tr> 
 </tbody> 
</table>

