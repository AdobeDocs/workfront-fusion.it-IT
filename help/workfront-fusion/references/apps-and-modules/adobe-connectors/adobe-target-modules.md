---
title: Moduli Adobe Target
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target] moduli per creare, leggere, aggiornare o eliminare record, elencare tutti i record di un determinato tipo, cercare i record in base ai criteri specificati o eseguire una chiamata API personalizzata all'API [!DNL Adobe Target] API.
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1923'
ht-degree: 0%

---

# [!DNL Adobe Target] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Target] e collegarlo a più applicazioni e servizi di terze parti. I moduli [!DNL Adobe Target] consentono di creare, leggere, aggiornare o eliminare record, elencare tutti i record di un determinato tipo, cercare i record in base ai criteri specificati o eseguire una chiamata API personalizzata all&#39;API [!DNL Adobe Target].


Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
      <td>
        <p>[!UICONTROL Pro] o superiore</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
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
    </tr>
  </tbody>
</table>


Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Prima di poter utilizzare il connettore [!DNL Adobe Target], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Target] attivo.

## Informazioni API di Adobe Target

Il connettore Adobe Target utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.7.33</td> 
  </tr>
 </tbody> 
 </table>

## Crea una connessione a [!DNL Adobe Target]

>[!IMPORTANT]
>
>Le connessioni create dopo il 3 giugno 2024 richiedono una connessione server-to-server di Adobe Target.
>
>* Le connessioni degli account di servizio esistenti continueranno a funzionare fino a gennaio 2025. È necessario sostituire le connessioni dell’account di servizio con le connessioni server-to-server di Adobe Target entro gennaio 2024.
>* Per creare una connessione server-to-server di Adobe Target, è necessario essere uno sviluppatore dell’organizzazione. Il ruolo sviluppatore è impostato in Adobe Admin Console.

Per creare una connessione per i moduli [!DNL Adobe Target]:

1. Fare clic su **[!UICONTROL Add]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Specificare se si sta creando una connessione dell'account di servizio o una connessione server-to-server di Adobe Target.<p><b>IMPORTANTE</b>: le connessioni create dopo il 3 giugno 2024 richiedono una connessione server-to-server di Adobe Target. Le connessioni degli account di servizio esistenti continueranno a funzionare fino a gennaio 2025. È necessario sostituire le connessioni dell’account di servizio con le connessioni server-to-server di Adobe Target entro gennaio 2024.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Specificare se ci si connette a un account di servizio o a un account personale.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immetti l'ID client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Immetti il segreto client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Immetti l'ID account tecnico [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Immetti l'ID organizzazione [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tenant]</td>
        <td>
          <p> Per individuare il tenant, accedere a [!DNL Adobe Experience Cloud], aprire [!DNL Target] e fare clic sulla scheda [!DNL Target]. Utilizza il valore ID tenant indicato nel sottodominio URL.</p>
          <p>Ad esempio, se l'URL al momento dell'accesso a [!DNL Adobe Target] è <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code>, l'ID tenant sarà "mycompany".</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Immetti <code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Immettere la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fare clic su <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selezionare il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Immettere la password per il file.</p>
            </li>
            <li value="5">
              <p>Fare clic su <b>[!UICONTROL Save]</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.

## [!DNL Adobe Target] moduli e relativi campi

Quando configuri [!DNL Adobe Target] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Target], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)

* [Ricerche](#searches)


### Azioni

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

Questo modulo di azione crea un’attività AB o XT, un’offerta o un pubblico.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>
      <p>Selezionare il tipo di record da creare.</p>
      <ul>
        <li>
        <b>Proprietà</b><p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty">Creare una proprietà</a> nella documentazione dell'API di Adobe Target.</p>
        </li>
        <li>
        <b>Consiglio offerta</b><p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer">Creare una nuova offerta Recs</a> nella documentazione API di Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer JSON]</b>
          <p>Continua con <a href="#offer-fields" class="MCXref xref" >Campi offerta</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer Content]</b>
          <p>Continua con <a href="#offer-fields" class="MCXref xref" >Campi offerta</a>.</p>
        </li>
        <li>
        <b>Ambiente</b><p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">Creare l'ambiente</a> nella documentazione dell'API di Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Audience]</b>
          <p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">Creare un pubblico</a> nella documentazione dell'API di Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity]</b>
          <p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Creare un'attività AB</a> nella documentazione API di Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity]</b>
          <p>Continua con <a href="#xt-activity-fields" class="MCXref xref" >XT campi attività</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL AP Activity]</b>
          <p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">Creare un'attività di Personalizzazione automatizzata</a> nella documentazione delle API di Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Response Token]</b>
          <p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken">Creare un token di risposta</a> nella documentazione dell'API di Adobe Target.</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### Campi di attività XT

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Immetti o mappa un nome per questa attività. Il nome non può contenere più di 250 caratteri.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>Per ogni opzione che si desidera aggiungere all'attività, fare clic su <b>[!UICONTROL Add item]</b> e compilare i campi seguenti:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Immetti o mappa una stringa da utilizzare per tenere traccia dell’opzione nelle diverse richieste API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Immetti o mappa un nome per l’opzione. Il nome non può contenere più di 250 caratteri.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Seleziona o mappa l’Offerta associata all’opzione.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locations]</td>
      <td>
        <p>Per ogni Mbox che desideri aggiungere all'attività, fai clic su <b>[!UICONTROL Add item]</b> e compila i campi seguenti:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>Per ogni pubblico che desideri aggiungere alla Mbox, fai clic su <b>[!UICONTROL Add item]</b> e seleziona l'ID pubblico.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Immetti o mappa una stringa da utilizzare per monitorare la posizione nelle diverse richieste API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Immetti o mappa un nome per la posizione. Il nome non può contenere più di 250 caratteri.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>Un elenco di posizioni sulla pagina in cui viene distribuita l’offerta di contenuti. Una posizione contiene quanto segue:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Inserisci o mappa l'ID dell'esperienza</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Inserisci o mappa il nome dell’esperienza

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Per ogni pubblico che desideri visualizzare l'esperienza, fai clic su <b>[!UICONTROL Add item]</b> e immetti l'ID del pubblico.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Immetti o mappa la percentuale di visitatori allocata all'esperienza</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Immetti o mappa un ID per identificare questa attività. Puoi scegliere questo ID. Questo ID non deve essere lo stesso di un’altra attività e non può superare i 250 caratteri.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Immettere o mappare la data e l'ora di inizio dell'attività nel formato <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Immettere o mappare la data e l'ora di fine dell'attività nel formato <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Inserisci o mappa lo stato dell’attività.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Immetti un numero che definisce la priorità dell’attività. I numeri più alti hanno priorità più alta. Questo valore deve essere compreso tra 0 e 999. Il valore predefinito è 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Abilita questa opzione per allocare automaticamente il traffico. L’allocazione automatica invia più traffico all’esperienza di maggior successo.</p>
        <p>Seleziona o mappa i criteri di valutazione in base ai quali giudicare quale esperienza ha più successo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Inserisci o mappa l’area di lavoro a cui è associata l’attività</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>Per ogni proprietà che desideri aggiungere all'attività, fai clic su <b>[!UICONTROL Add item]</b> e seleziona o mappa l'ID della proprietà.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>Per ogni pubblico di reportistica che desideri aggiungere all'attività, fai clic su [!UICONTROL Add item] e immetti le seguenti informazioni:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Immetti o mappa una stringa da utilizzare per monitorare il pubblico di reportistica nelle diverse richieste API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Inserisci o mappa il segmento da utilizzare nel reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Inserisci o mappa una stringa da utilizzare per monitorare la metrica nelle richieste API.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Campi offerta

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Immetti o mappa un nome per questa attività. Il nome non può contenere più di 250 caratteri.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content]</td>
      <td>
        <p>Inserisci o mappa il contenuto dell’offerta che verrà mostrato all’utente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Inserisci o mappa l’ID dell’area di lavoro associata all’offerta. Se non specificata, l’offerta viene associata all’area di lavoro predefinita dell’account. Questa funzionalità si applica solo agli account Premium [!DNL Target].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Immetti o mappa la data e l’ora in cui l’offerta è stata modificata.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Make a custom API call]

Questo modulo effettua una chiamata API personalizzata all&#39;API [!DNL Adobe Target].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] URL di base]</td>
      <td>Immetti o mappa l'URL di base di [!DNL Target].</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Immettere un percorso relativo a {baseURL}/</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione e le intestazioni x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a record]

Questo modulo di azione elimina una singola attività AB, un’attività XT, un’offerta o un pubblico.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selezionare il tipo di record che si desidera eliminare.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Immettere o mappare l'ID del record che si desidera eliminare.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Read a record]

Questo modulo di azione recupera i dati per una singola attività, offerta, pubblico, proprietà o rapporto.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selezionare il tipo di record che si desidera leggere.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Immetti o mappa l’ID del record da leggere.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Update a record]

Questo modulo di azione aggiorna un record in Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>Selezionare il tipo di record da aggiornare.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Field names]</td>
      <td>Seleziona i campi da aggiornare. I campi vengono visualizzati di seguito.
          <p>Per informazioni dettagliate sui campi, consulta <a href="https://developer.adobe.com/target/administer/admin-api/">la documentazione sulle API di Adobe Target</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ricerche

* [[!UICONTROL Get records]](#get-records)

* [[!UICONTROL Search]](#search)


#### [!UICONTROL Get records]

Questo modulo di ricerca recupera un elenco di record del tipo selezionato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selezionare il tipo di record da aggiornare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sort by]</td>
      <td>Per ogni campo in base al quale si desidera eseguire l'ordinamento, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il campo e specificare se i risultati restituiti devono essere in ordine crescente o decrescente.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts At]</td>
      <td>
        <p>Immettere la prima data per la quale si desidera recuperare i record. </p>
        <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends At]</td>
      <td>
        <p>Immettere l'ultima data per la quale si desidera recuperare i record. </p>
        <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Search]

Questo modulo di ricerca cerca attività, offerte o tipi di pubblico in base ai criteri specificati.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Target], vedere <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Creare una connessione a [!DNL Adobe Target]</a> in questo articolo.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Selezionare il tipo di record da aggiornare.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Sort by]</td>
    <td>Per ogni campo in base al quale si desidera eseguire l'ordinamento, fare clic su <b>[!UICONTROL Add item]</b> e selezionare il campo e specificare se i risultati restituiti devono essere in ordine crescente o decrescente.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Search criteria]</td>
    <td>Per ogni regola che desideri impostare, seleziona il campo, l’operatore e il valore. Fare clic su <b>[!UICONTROL Add AND rule]</b> per creare regole aggiuntive.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Offset]</td>
    <td>
      <p>Immettere il numero della prima risposta che si desidera venga restituita dal modulo. La prima risposta restituita ha un offset di <code>0</code>. Utilizzare questo campo in combinazione con il campo [!UICONTROL Maximum number of returned results] per impaginare le risposte.</p>
      <p>Ad esempio, per visualizzare la terza pagina di risposte, quando ogni pagina contiene dieci risposte, impostare [!UICONTROL Offset] su 20 e [!UICONTROL Maximum number of returned] risultati su 10.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. Utilizzare questo campo in combinazione con il campo [!UICONTROL Offset] per impaginare le risposte.</p>
      <p>Ad esempio, per visualizzare la terza pagina di risposte, quando ogni pagina contiene dieci risposte, impostare [!UICONTROL Offset] su 20 e [!UICONTROL Maximum number of returned] risultati su 10.</p>
    </td>
  </tr>
</tbody>
</table>
