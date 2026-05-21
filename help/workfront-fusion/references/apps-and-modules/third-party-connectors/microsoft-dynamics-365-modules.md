---
title: Moduli Microsoft Dynamics 365
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Microsoft Dynamics 365 e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
TQID: https://experienceleague.adobe.com/hugbkrxjvBcwIiPQMfM9VIcRby-zpFK6U5hRmrF38Lc
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1884
ht-degree: 44%

---

# [!DNL Microsoft Dynamics 365 modules]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft Dynamics 365], nonché collegarli a più applicazioni e servizi di terze parti.

>[!NOTE]
>
>Il connettore [!DNL Microsoft Dynamics 365] non supporta [!DNL Dynamics Finance and Operations].
>
>Per informazioni sul connettore [!DNL Microsoft Dynamics 365 Finance and Operations], vedere [[!DNL Microsoft Dynamics 365 Finance and Operations] moduli](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/dynamics-finance-operations-modules.md).

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

Per usare [!DNL Microsoft Dynamics] 365, devi avere un account [!DNL Microsoft Dynamics 365].

## Collegare Microsoft Dynamics 365 a Workfront Fusion

Puoi creare una connessione al tuo account [!DNL Microsoft Dynamics 365] direttamente dall&#39;interno di un modulo [!DNL Microsoft Dynamics 365].

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

1. In qualsiasi modulo [!DNL Microsoft Dynamics 365], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].


1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
          <td>
            <p>Specifica un nome per questa connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Ambiente]</td>
          <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo]</td>
          <td>Seleziona se ti interessa la connessione a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]<p>(Facoltativo)</p></td>
          <td>Inserisci il tuo [!UICONTROL Client ID] [!DNL Microsoft Dynamics].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)<p>(Facoltativo)</p></td>
          <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Microsoft Dynamics].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL URL di autenticazione]</td>
          <td>Immetti l’URL che verrà utilizzato dall’istanza di Workfront per autenticare questa connessione. <p>Il valore predefinito è <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Risorsa]</td>
          <td>immetti l'indirizzo del tuo account [!DNL Dynamics 365], senza <code>>https://</code>.</p>
        </tr>
      </tbody>
    </table>
1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

>[!NOTE]
>
>Quando si registra Workfront Fusion nel portale [!DNL Microsoft Azure], utilizzare il seguente URI di reindirizzamento:
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## Moduli [!DNL Microsoft Dynamics 365] e relativi campi

Quando configuri i moduli [!DNL Microsoft Dynamics 365], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Microsoft Dynamics 365], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

* [[!UICONTROL Osserva record (tempo reale)]](#watch-records-real-time)
* [[!UICONTROL Osserva record (pianificati)]](#watch-records-scheduled)

#### [!UICONTROL Osserva record (tempo reale)]

Questo modulo di attivazione immediata esegue uno scenario quando un record (oggetto) specificato viene creato o aggiornato in [!DNL Dynamics 365].

In questo modulo è necessario un webhook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook da utilizzare per questo modulo. </p> <p>Per aggiungere un nuovo webhook:</p> 
    <ol> 
     <li value="1"> <p>Fai clic su <strong>[!UICONTROL Add]</strong> a destra del campo Webhook</p> </li> 
     <li value="2"> <p>Nel campo del nome <strong>[!UICONTROL Webhook]</strong> digitare un nome descrittivo per il webhook.</p> </li> 
     <li value="3"> <p>Nel campo <strong>[!UICONTROL Connection]</strong>, selezionare la connessione che si desidera utilizzare selezionata</p> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </li> 
     <li value="4"> <p>Fai clic su <strong>[!UICONTROL Salva]</strong> per salvare il webhook e tornare al modulo.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Osserva record (pianificati)]

Questo modulo trigger pianificato esegue uno scenario quando un record nell&#39;oggetto specificato viene creato o aggiornato dopo l&#39;ultima esecuzione pianificata dello scenario.

L&#39;output del modulo indica se il record trovato è nuovo o aggiornato. Se il record è stato aggiunto e aggiornato nel periodo di tempo, viene restituito come nuovo record.

Questo si verifica in un intervallo pianificato regolare specificato.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> "
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include]</td> 
   <td>Specificare se si desidera che il modulo controlli <strong>[!UICONTROL Solo nuovi record]</strong>, <strong>[!UICONTROL Solo record aggiornati]</strong> o <strong>[!UICONTROL Record nuovi e aggiornati]</strong>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td>Scegliere il tipo di record [!UICONTROL Microsoft Dynamics 365] che si desidera controllare nello scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo. I campi sono disponibili in base al tipo di entità selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max record]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Crea record]](#create-record)
* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)
* [[!UICONTROL Elimina record]](#delete-record)
* [[!UICONTROL Leggi record]](#read-records)
* [[!UICONTROL Aggiorna record]](#update-record)


#### [!UICONTROL Crea record]

Questo modulo di azione crea un&#39;entità, ad esempio un appuntamento o un task.

È possibile specificare informazioni sull&#39;entità da creare.

Il modulo restituisce l’ID della nuova entità e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td>Selezionare il tipo di entità che si desidera creare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona campi da mappare]</td> 
   <td>Selezionare i campi per i quali si desidera includere i valori al momento della creazione del record. I campi disponibili dipendono dal tipo di entità.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Campi proprietà [!UICONTROL]</td> 
   <td> Questi sono i campi selezionati. Immettere il valore desiderato per il record per una determinata proprietà. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina record]

Questo modulo di azione elimina un’entità.

Specifica l’ID dell’entità.

Il modulo restituisce l’ID dell’entità e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td> <p>Selezionare il tipo di entità che si desidera eliminare dal modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Immettere o mappare l'ID [!DNL Microsoft Dynamics 365] univoco del record che si desidera eliminare dal modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Microsoft Dynamics 365]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Microsoft Dynamics 365].

Il modulo restituisce informazioni sul codice di stato, le intestazioni e il corpo. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Per ulteriori informazioni, vedere la documentazione di [!DNL Microsoft] sull&#39;utilizzo di [!DNL Dynamics 365 Customer Engagement Web API].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Inserisci un percorso relativo a <code>&lt;Instance URL>/api/data/v9.1/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> <p>Per ulteriori informazioni in</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi record]

Questo modulo di azione legge i dati da una singola entità in [!DNL Microsoft Dynamics 365].

Specifica l’ID dell’entità.

Il modulo restituisce l’ID dell’entità e degli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td>Selezionate il tipo di entità che desiderate che venga letta dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID [!DNL Microsoft Dynamics 365] univoco del record che si desidera venga letto dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna record]

Questo modulo di azione aggiorna un’entità.

Specifica l’ID dell’entità.

Il modulo restituisce l’ID del record aggiornato e di tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td>Selezionare il tipo di entità che si desidera aggiornare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona campi da mappare]</td> 
   <td>Selezionare i campi per i quali si desidera includere i valori al momento della creazione del record. I campi disponibili dipendono dal tipo di entità.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Campi proprietà [!UICONTROL]</td> 
   <td>Questi sono i campi selezionati. Immettere il valore desiderato per il record per una determinata proprietà.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immettere o mappare l'ID [!DNL Microsoft Dynamics] 365 univoco del record che si desidera aggiornare nel modulo.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Cerca record]

Questo modulo di ricerca cerca i record in un oggetto in [!DNL Microsoft Dynamics 365] che corrispondono alla query di ricerca specificata. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell’account [!DNL Microsoft Dynamics 365] a Workfront Fusion, consulta <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Microsoft Dynamics 365] a Workfront Fusion</a> in questo articolo. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di entità]</td> 
   <td>Selezionare il tipo di entità che si desidera aggiornare nel modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtri]</td> 
   <td> <p>Selezionare il filtro che si desidera utilizzare per la ricerca.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Filtri Standard]</strong> </p> <p>Imposta il filtro selezionando un campo e un operatore e immettendo o mappando il valore che desideri cercare. Puoi utilizzare le regole AND o OR per il filtro.</p> </li> 
     <li> <p><strong>[!UICONTROL Funzioni query]</strong> </p> <p>Immettere la funzione di query API Web [!DNL Dynamics 365] che si desidera utilizzare per la ricerca. </p> <p>Per ulteriori informazioni sulle funzioni di query, vedere <a href="https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9">Riferimento funzione query API Web</a> nella documentazione di [!DNL Microsoft].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Specificare l'ordine di restituzione degli elementi. È possibile aggiungere più ordinamenti.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Campo]</strong> </p> <p>Specificare il campo in base al quale ordinare i risultati.</p> </li> 
     <li> <p><strong>[!UICONTROL Direzione]</strong> </p> <p>Specifica la direzione dell’ordinamento (crescente o decrescente).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max record]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>
