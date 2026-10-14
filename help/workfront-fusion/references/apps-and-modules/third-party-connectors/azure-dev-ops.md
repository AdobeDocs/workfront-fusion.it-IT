---
title: Moduli Azure DevOps
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Azure DevOps], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
TQID: 'https://experienceleague.adobe.com/RFI6MFgF-C1Cnn0bvjOLVf3qahyRblEp4dtypNrxqzE'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0922a5503bbeded91ae116849465d0f898ef4686
workflow-type: tm+mt
source-wordcount: '3789'
ht-degree: 17%
---
# Moduli [!DNL Azure DevOps]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Azure DevOps], nonché collegarli a più applicazioni e servizi di terze parti.

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
   <p>Basato su operazioni: disponibile per le organizzazioni con licenze basate su operazioni</p>
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

Per utilizzare i moduli [!DNL Azure DevOps], è necessario disporre di un account DevOps [!DNL Azure].

## Informazioni API di [!DNL Azure DevOps]

Il connettore Azure DevOps utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Connettere [!DNL Azure DevOps] a Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

* [Connettere Azure DevOps a Workfront Fusion utilizzando una connessione federata](#connect-azure-devops-to-workfront-fusion-using-a-federated-connection)
* [Collegare Azure DevOps a Workfront Fusion utilizzando EntraApp](#connect-azure-devops-to-workfront-fusion-using-entraapp)
* [Connettere Azure DevOps a Workfront Fusion utilizzando un’entità servizio](#connect-azure-devops-to-workfront-fusion-using-a-service-principal)

### Connettere Azure DevOps ad Adobe Workfront Fusion utilizzando una connessione federata

Una connessione federata funziona come la connessione dell&#39;entità servizio, con la differenza che non utilizza un segreto client.

Invece di memorizzare un segreto, si consiglia a Microsoft Entra ID di considerare attendibili i token che Workfront Fusion ha problemi per una connessione specifica. Quando la connessione viene eseguita, Fusion presenta una prova di identità di breve durata e Microsoft Entra ID restituisce un token di accesso. Poiché non esiste alcun segreto client, non esiste nulla che scada e nessun segreto da ruotare o archiviare.

+++ Espandi per visualizzare le istruzioni per la connessione di Azure DevOps ad Adobe Workfront Fusion tramite una connessione federata.

>[!NOTE]
>
>* La configurazione di questa connessione richiede due visite al centro di amministrazione di Microsoft Entra. Registra prima l’app, quindi crea la connessione in Workfront Fusion, quindi torna a Microsoft Entra ID per aggiungere le credenziali federate. Ciò si verifica perché le credenziali federate hanno identificato una connessione specifica e tale identificatore non esiste fino alla creazione della connessione.
>* A questa connessione si applicano gli stessi limiti della connessione dell&#39;entità servizio. Un numero limitato di azioni a livello di amministratore, come la gestione delle licenze utente, richiede ancora una connessione a un account personale.

* [Prerequisiti per la connessione di Azure DevOps a Workfront Fusion tramite una connessione federata](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-federated-connection)
* [Creare la registrazione dell’app in Microsoft Entra ID (connessione federata)](#create-the-app-registration-in-microsoft-entra-id-federated-connection)
* [Raccogliere i dettagli di connessione (connessione federata)](#collect-your-connection-details-federated-connection)
* [Creare la connessione in Workfront Fusion (connessione federata)](#create-the-connection-in-workfront-fusion-federated-connection)
* [Aggiungere le credenziali federate in Microsoft Entra ID](#add-the-federated-credential-in-microsoft-entra-id)
* [Verifica la connessione (connessione federata)](#verify-the-connection-federated-connection)

#### Prerequisiti per la connessione di Azure DevOps a Workfront Fusion tramite una connessione federata


Per creare questa connessione, è necessario disporre dei seguenti elementi:

* Accesso Amministratore globale o Amministratore applicazione in Microsoft Entra ID, per registrare l’app e aggiungere le credenziali federate. Se non disponi di questo accesso, chiedi a qualcuno del tuo team IT o di identità di completare questi passaggi al posto tuo.
* Accesso amministratore della raccolta di progetti nell’organizzazione Azure DevOps, per aggiungere l’entità servizio come membro. Spesso si tratta di una persona diversa da quella che gestisce l’Entra ID di Microsoft.
* Nome dell’organizzazione Azure DevOps. È possibile trovarlo nell&#39;URL di Azure DevOps: `dev.azure.com/<your organization name>`.

#### Creare la registrazione dell’app in Microsoft Entra ID (connessione federata)

1. Accedi al centro di amministrazione di Microsoft Entra.
1. Vai a Registrazioni app > Nuova registrazione.
1. Assegna all’app un nome chiaro e riconoscibile. Ad esempio, `Workfront Fusion Azure DevOps Integration`.
1. Lascia vuoto URI di reindirizzamento. Questa connessione non comporta l’accesso tramite un browser.
1. Seleziona Registra.
1. Non creare un segreto client. Una connessione federata non ne utilizza una.
1. Continua con [Raccogliere i dettagli della connessione](#collect-your-connection-details-federated-connection).


#### Raccogliere i dettagli di connessione (connessione federata)

1. Nella pagina Panoramica della registrazione dell’app, prendi nota dei seguenti valori. Immetti questi valori durante la creazione della connessione nel modulo.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL ID tenant]</td>
      <td>Nella pagina Panoramica, con etichetta <b>ID directory (tenant)</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL ID client]</td>
      <td>Nella pagina Panoramica, etichettato <b>ID applicazione (client)</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Organizzazione]</td>
      <td>Il nome della tua organizzazione Azure DevOps. Ad esempio, se l'URL è <code>dev.azure.com/yourorg</code>, immettere <code>yourorg</code>.</td>
     </tr>
    </tbody>
   </table>

1. Continua con [Crea la connessione in Workfront Fusion](#create-the-connection-in-workfront-fusion-federated-connection).

>[!NOTE]
>
>Come per la connessione dell’entità servizio, puoi saltare l’area delle autorizzazioni API per la registrazione dell’app. Nella procedura successiva, l’accesso ad Azure DevOps viene concesso all’interno di Azure DevOps.

#### Creare la connessione in Workfront Fusion (connessione federata)

1. Nella schermata di configurazione della connessione del modulo, seleziona il tipo di connessione federata.
1. Immetti il codice seguente:

   * ID tenant
   * ID client
   * Organizzazione

1. Seleziona **Crea**.

   In Workfront Fusion vengono visualizzati tre valori. Lascia aperta questa pagina, poiché questi valori saranno necessari in un secondo momento durante la creazione della connessione.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Emittente]</td>
      <td><code>https://oidc.automations.adobe.com</code>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Subject]</td>
      <td>Questo identifica questa connessione. È <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>. È diversa per ogni connessione creata.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Audience]</td>
      <td><code>api://AzureADTokenExchange</code>.</td>
     </tr>
    </tbody>
   </table>

   >[!IMPORTANT]
   >
   >Non chiudere il pannello e non selezionare Annulla. La connessione non viene completata fino a quando non si completa il resto della procedura. Se chiudi il pannello, devi eliminare la connessione e riavviarla, perché a una nuova connessione viene assegnato un nuovo Oggetto.

1. Copia il valore **Subject**.
1. Continuare con [Aggiungere le credenziali federate nell&#39;ID Entra di Microsoft](#add-the-federated-credential-in-microsoft-entra-id).

#### Aggiungere le credenziali federate in Microsoft Entra ID

Questa procedura sostituisce il segreto client. Indica a Microsoft Entra ID di accettare i token che Workfront Fusion genera per questa connessione.

1. In una nuova scheda del browser, torna al centro di amministrazione di Microsoft Entra e apri la registrazione all’app.
1. Vai a Certificati e segreti > Credenziali federate.
1. Seleziona Aggiungi credenziali.
1. In Scenario credenziali federate selezionare Altro emittente.
1. Immetti il codice seguente:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Emittente]</td>
      <td><code>https://oidc.automations.adobe.com</code></td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Subject identifier]</td>
      <td>Oggetto copiato da Workfront Fusion. Incollalo esattamente, senza spazi aggiunti.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>Un nome che identifica la connessione, in modo da poterla trovare in un secondo momento. Ad esempio, <code>workfront-fusion-connection-28964</code>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Audience]</td>
      <td><code>api://AzureADTokenExchange</code>. Questo di solito è compilato per te. Lascia il valore predefinito.</td>
     </tr>
    </tbody>
   </table>

1. Fai clic su **Aggiungi**.
1. Continua con [Verifica la connessione](#verify-the-connection-federated-connection).

>[!NOTE]
>
>Microsoft Entra ID consente un massimo di 20 credenziali federate in una singola registrazione di app e l’identificatore Subject deve corrispondere esattamente. I caratteri jolly non sono supportati. Poiché ogni connessione Workfront Fusion ha il proprio oggetto, ogni connessione ha bisogno delle proprie credenziali federate. Se prevedi più di 20 connessioni, registra più di un’app e distribuisci le connessioni tra di esse.


#### Verifica la connessione (connessione federata)

1. Tornare alla scheda del browser Workfront Fusion, dove il pannello di connessione è ancora aperto.
1. Fai clic su **Salva**.

   * Se tutto è configurato correttamente, la connessione viene convalidata correttamente e puoi procedere con la configurazione del modulo.
   * Se la verifica non riesce, il pannello rimane aperto e visualizza l’errore. Correggi il problema in Microsoft Entra ID o Azure DevOps e seleziona nuovamente Salva. Non è necessario ricreare la connessione e l&#39;oggetto non cambia.

>[!NOTE]
>
>L&#39;attivazione di una credenziale federata aggiunta in Microsoft Entra ID può richiedere un breve tempo. Se la verifica non riesce subito dopo aver aggiunto le credenziali, attendi un minuto e seleziona nuovamente Salva prima di approfondire l’analisi.


Risoluzione dei problemi

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader">Impossibile verificare la connessione a causa di un client non valido o di un errore di richiesta non valido</td>
   <td>L’ID dell’endpoint Microsoft non può corrispondere al token per una credenziale federata. Verificare che l'autorità emittente sia esattamente <code>https://oidc.automations.adobe.com</code> senza barra finale e che l'identificatore dell'oggetto sia identico al carattere indicato in Workfront Fusion. La causa più comune è un oggetto copiato da una connessione diversa.</td>
  </tr>
  <tr>
   <td role="rowheader">La connessione viene verificata, ma i moduli restituiscono 401 o 403 da Azure DevOps</td>
   <td>L’identità è attendibile, ma non ha accesso ai dati Azure DevOps. Conferma di aver completato <a href="#add-the-service-principal-to-your-azure-devops-organization">Aggiungere l'entità servizio all'organizzazione Azure DevOps</a> e che l'entità servizio è assegnata al progetto specifico utilizzato dal modulo.</td>
  </tr>
  <tr>
   <td role="rowheader">Impossibile aggiungere un'altra credenziale federata</td>
   <td>Hai raggiunto il limite di 20 credenziali federate per la registrazione dell’app. Registra un’app aggiuntiva e crea ulteriori connessioni.</td>
  </tr>
 </tbody>
</table>

+++

### Collegare Azure DevOps a Workfront Fusion utilizzando EntraApp

Puoi collegare Azure DevOps a Workfront Fusion utilizzando EntraApp.

+++ Espandi per visualizzare le istruzioni per la connessione di Azure DevOps a Workfront Fusion tramite EntraApp

1. Aggiungi un modulo [!DNL Azure DevOps] allo scenario.
1. Fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Nel campo [!UICONTROL Tipo di connessione], selezionare il tipo di connessione che si desidera utilizzare.

   >[!NOTE]
   >
   >[!UICONTROL [!DNL Azure DevOps] (EntraApp)] consente di richiedere tutti gli ambiti per la connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Connection name] (Nome della connessione)</td>
            <td>Immettere un nome per la connessione che si sta creando.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organizzazione]</td>
            <td>Immettere il nome dell'organizzazione con cui è stata creata l'applicazione [!DNL Azure DevOps].</td>
      </tr>
      <tr>
            <td>[!UICONTROL ID app]</td>
            <td>Immettere l'ID dell'applicazione DevOps a cui ci si connette.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Client Secret] (Segreto client)</td>
            <td>Immettere il segreto client per le applicazioni DevOps a cui ci si connette.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Richiedi tutti gli ambiti]</td>
            <td>Se si utilizza il tipo di connessione [!DNL Azure DevOps] (EntraApp), abilitare questa opzione per richiedere tutti gli ambiti per la connessione.</td>
      </tr>
   </table>

1. Per immettere un ID app Azure DevOps o un segreto client, fai clic su <b>Mostra impostazioni avanzate</b> e immettili nei campi aperti.
1. Fai clic su **[!UICONTROL Continua]** per completare la configurazione della connessione e continuare a creare lo scenario.

+++

### Connettere Azure DevOps a Workfront Fusion utilizzando un’entità servizio

È possibile creare una connessione che utilizza un&#39;entità servizio (una connessione API dell&#39;applicazione) invece di un account personale. Questa opzione è utile quando si desidera che la connessione venga eseguita come identità di un&#39;applicazione o di un servizio anziché come persona specifica. Questo può essere utile in modo che l’integrazione non si interrompa se, ad esempio, quella persona lascia l’azienda o modifica la propria password.

Questo tipo di connessione è disponibile per tutti i moduli DevOps di Azure.

+++ Espandi per visualizzare le istruzioni per la connessione di Azure DevOps ad Adobe Workfront Fusion utilizzando un’entità servizio.


>[!NOTE]
>
>L’autenticazione dell’entità servizio non supporta tutte le funzioni DevOps di Azure. Un numero limitato di azioni a livello di amministratore, come la gestione delle licenze utente, richiede ancora una connessione a un account personale. Utilizza l’autenticazione dell’entità servizio se è necessaria solo per elementi di lavoro, bacheche, repository o pipeline.

* [Prerequisiti per la connessione di Azure DevOps a Workfront Fusion tramite un’entità servizio](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-service-principal)
* [Creare la registrazione dell’app in Microsoft Entra ID](#create-the-app-registration-in-microsoft-entra-id-service-principal)
* [Creare un segreto client](#create-a-client-secret)
* [Raccogliere i dettagli di connessione](#collect-your-connection-details-service-principal)
* [Aggiungere l’entità servizio all’organizzazione Azure DevOps](#add-the-service-principal-to-your-azure-devops-organization)
* [Creare la connessione](#create-the-connection)

#### Prerequisiti per la connessione di Azure DevOps a Workfront Fusion tramite un’entità servizio

Per creare questa connessione, è necessario disporre dei seguenti elementi:

* Accesso **Amministratore globale** o **Amministratore applicazioni** in Microsoft Entra ID, per registrare l&#39;app. Se non disponi di questo accesso, chiedi a qualcuno del tuo team IT o di identità di completare quel passaggio al posto tuo.
* Accesso **Amministratore raccolta progetti** nell&#39;organizzazione Azure DevOps per aggiungere l&#39;entità servizio come membro. Spesso si tratta di una persona diversa da quella che gestisce l’Entra ID di Microsoft.
* Nome dell’organizzazione Azure DevOps. È possibile trovarlo nell&#39;URL di Azure DevOps: `dev.azure.com/<your organization name>`.

#### Creare la registrazione dell’app in Microsoft Entra ID (entità servizio)

1. Accedere al centro di amministrazione [!DNL Microsoft Entra].
1. Vai a **[!UICONTROL Registrazioni app]** > **[!UICONTROL Nuova registrazione]**.
1. Assegna all’app un nome chiaro e riconoscibile. Ad esempio, `Workfront Fusion Azure DevOps Integration`.
1. Lascia vuoto **[!UICONTROL URI reindirizzamento]**. Questa connessione non comporta l’accesso tramite un browser.
1. Seleziona **[!UICONTROL Registra]**.
1. Continua con [Crea un segreto client](#create-a-client-secret).

#### Creare un segreto client

1. Nella tua nuova registrazione all&#39;app, vai a **[!UICONTROL Certificati e segreti]**.
1. Seleziona **[!UICONTROL Nuovo segreto client]**, aggiungi una descrizione e scegli un periodo di scadenza.
1. Seleziona **[!UICONTROL Aggiungi]**.
1. Copia immediatamente il **[!UICONTROL Valore]** del segreto. Viene visualizzato una sola volta. Se esci prima di copiarlo, devi crearne uno nuovo.
1. Continua con [Raccogliere i dettagli della connessione](#collect-your-connection-details).

#### Raccogliere i dettagli di connessione (entità servizio)

1. Nella pagina **[!UICONTROL Panoramica]** della registrazione dell&#39;app, prendi nota dei seguenti valori. Immetti questi valori durante la creazione della connessione nel modulo.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL ID tenant]</td>
      <td>Nella pagina Panoramica, con etichetta <b>ID directory (tenant)</b>.</td>
      </tr>
     <tr>
      <td role="rowheader">[!UICONTROL ID client]</td>
      <td>Nella pagina Panoramica, etichettato <b>ID applicazione (client)</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
      <td>Il valore copiato in <a href="#create-a-client-secret" class="MCXref xref">Crea un segreto client</a>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Organizzazione]</td>
      <td>Il nome della tua organizzazione Azure DevOps. Ad esempio, se l'URL è <code>dev.azure.com/yourorg</code>, immettere <code>yourorg</code>.</td>
     </tr>
    </tbody>
   </table>

   >[!NOTE]
   >
   >Puoi saltare l&#39;area **Autorizzazioni API** della registrazione dell&#39;app. Se aggiungi Azure DevOps, sono disponibili solo **autorizzazioni delegate**. Le **autorizzazioni dell&#39;applicazione** sono visualizzate in grigio. Ciò è previsto, perché Azure DevOps non supporta questa modalità di concessione dell’accesso. Nella parte successiva, l’accesso viene concesso direttamente all’interno di Azure DevOps.

1. Continua con [Aggiungi l&#39;entità servizio alla tua organizzazione Azure DevOps](#add-the-service-principal-to-your-azure-devops-organization).

#### Aggiungere l’entità servizio all’organizzazione Azure DevOps

La registrazione dell’app in Microsoft Entra ID ne crea solo l’identità. Non fornisce ancora all’app alcun accesso ai dati Azure DevOps. Questa procedura consente l&#39;accesso.

1. Accedi alla tua organizzazione Azure DevOps all&#39;indirizzo `dev.azure.com/<your organization name>`.
1. Seleziona **[!UICONTROL Impostazioni organizzazione]** in basso a sinistra, quindi seleziona **[!UICONTROL Utenti]**.
1. Selezionare **[!UICONTROL Aggiungi utenti]**.
1. Nella casella di ricerca, cerca in base al nome visualizzato dell’app, che è il nome che le hai assegnato quando hai registrato l’app. Non eseguire ricerche in base all’ID client.
1. Selezionare un livello di accesso:

   * **[!UICONTROL Base]** è in genere sufficiente per leggere e scrivere elementi di lavoro, bacheche e repository.
   * Se il flusso di lavoro deve sfogliare i processi disponibili, ad esempio i modelli Agile, Scrum o personalizzati, come parte della configurazione, aggiungi l&#39;entità servizio al gruppo **[!UICONTROL Amministratori raccolta progetti]**. Si tratta di un livello di accesso più ampio, quindi concedilo solo se hai bisogno di tale funzionalità.

1. Assegna l’entità servizio al progetto o ai progetti specifici necessari, seguendo le consuete procedure di accesso dell’organizzazione.
1. Seleziona **[!UICONTROL Aggiungi]**.
1. Continua con [Crea la connessione in Workfront Fusion](#create-the-connection-in-workfront-fusion-service-principal).

#### Creare la connessione in Workfront Fusion (entità servizio)

1. Nella schermata di configurazione della connessione del modulo, selezionare il tipo di connessione **[!UICONTROL Entità servizio]**.
1. Immetti il codice seguente:

   * [!UICONTROL ID tenant]
   * [!UICONTROL ID client]
   * [!UICONTROL Segreto client]
   * [!UICONTROL Organizzazione]

1. Salva la connessione.

   Se tutto è configurato correttamente, la connessione viene convalidata correttamente.

+++

## [!UICONTROL Moduli DevOps] di Azure e relativi campi

Quando configuri i moduli [!DNL Azure DevOps], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Azure DevOps], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### [!UICONTROL Controlla elementi di lavoro]

Questo modulo di attivazione immediata esegue uno scenario quando un record viene aggiunto, aggiornato o eliminato in [!UICONTROL Azure DevOps].

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona o aggiungi un webhook per il modulo.</p> <p>Per ulteriori informazioni sui webhook nei moduli trigger, vedere <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Trigger istantanei (webhook)</a>.</p> <p>Per informazioni su come creare un webhook, vedere <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [Crea un record](#create-a-record)
* [Chiamata API personalizzata](#custom-api-call)
* [Scaricare un allegato](#download-an-attachment)
* [Collega elementi di lavoro](#link-work-items)
* [Leggi record](#read-record)
* [Aggiornare un elemento di lavoro](#update-a-work-item)
* [[!UICONTROL Carica un allegato]](#upload-an-attachment)

#### [!UICONTROL Crea un record]

Questo modulo di azione crea un nuovo progetto o elemento di lavoro.

Il modulo restituisce l’ID oggetto per il nuovo elemento di lavoro creato oppure l’URL e il codice di stato di un progetto appena creato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Specificare se si desidera creare un elemento di lavoro o un progetto.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Progetto]</strong> </p> <p>Compila i seguenti campi:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: immettere o mappare un nome per il nuovo progetto.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: immettere o mappare una descrizione per il nuovo progetto. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: specificare se il progetto deve essere pubblico o privato. Per interagire con un progetto privato, gli utenti devono aver effettuato l’accesso alla tua organizzazione e disporre dell’accesso al progetto. I progetti pubblici sono visibili agli utenti che non hanno effettuato l'accesso all'organizzazione.</p> </li> 
       <li> <p><strong>[!UICONTROL Controllo della versione]</strong>: specificare se si desidera che il progetto utilizzi [!DNL Git] o [!UICONTROL Controllo della versione di Team Foundation (TFCV)] per il controllo della versione.</p> </li> 
       <li> <p><strong>[!UICONTROL Processo elemento di lavoro]</strong>: selezionare il processo di lavoro da utilizzare per il progetto. Le opzioni sono [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] e [!UICONTROL Agile].</p> <p>Per ulteriori informazioni sui processi [!DNL Azure DevOps], vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=basic-process">Processi predefiniti e modelli di processo</a> nella documentazione di [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Elemento di lavoro]</strong> </p> <p>Compila i seguenti campi:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: selezionare il progetto in cui si desidera creare l'elemento di lavoro.</p> </li> 
       <li> <p><strong>[!UICONTROL Tipo di elemento di lavoro]</strong>: selezionare il tipo di elemento di lavoro da creare.</p> </li> 
       <li> <p><strong>[!UICONTROL Altri campi]</strong>: in questi campi immettere il valore desiderato per l'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Azure DevOps]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Azure DevOps].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL di base]</td> 
   <td> <p>Selezionare o mappare l'URL di base utilizzato per connettersi all'account [!DNL Azure DevOps]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL relativo]</td> 
   <td> <p>Immetti l’URL relativo a cui desideri connetterti per questa chiamata API.</p> <p><b>Esempio: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Versione API]</td> 
   <td>Selezionare o mappare la versione dell'API [!DNL Azure DevOps] a cui connettersi per questa chiamata API. Se non è selezionata alcuna versione, Workfront Fusion si connette alla versione 5.1 dell'API [!DNL Azure DevOps].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
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

#### [!UICONTROL Scarica un allegato]

Questo modulo di azione scarica un allegato.

Il modulo restituisce il contenuto del file dell’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL allegato]</td> 
   <td> <p>Inserisci o mappa l’URL dell’allegato da scaricare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Collega elementi di lavoro]

Questo modulo di azione collega due elementi di lavoro e definisce la relazione tra di essi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro principale a cui si desidera collegare un altro elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked Work Item ID]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera collegare all'elemento di lavoro principale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di collegamento]</td> 
   <td> <p>Definire la relazione tra gli elementi di lavoro da collegare.</p> <p>Per ulteriori informazioni, vedere <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">Guida di riferimento per i tipi di collegamento</a> nella documentazione di [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Immettere o mappare il testo di un commento. Ciò è utile per spiegare il ragionamento o l’intenzione del collegamento.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi record]

Questo modulo di azione legge i dati da un singolo record in [!DNL Azure DevOps].

Specifica l’ID del record.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri leggere un progetto o un elemento di lavoro</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: selezionare il progetto che si desidera leggere.</p> </li> 
     <li> <p><strong>[!UICONTROL Elemento di lavoro]</strong>: selezionare il progetto che contiene l'elemento di lavoro che si desidera leggere, quindi selezionare il tipo di elemento di lavoro.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID del record da leggere.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un elemento di lavoro]

Questo modulo di azione aggiorna un elemento di lavoro esistente utilizzando il relativo ID.

Il modulo restituisce l’ID dell’elemento di lavoro aggiornato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Progetto]</td> 
   <td>Selezionare il progetto contenente l'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di elemento di lavoro </td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Altri Campi]</td> 
   <td>In ciascuno di questi campi immettere il valore che si desidera assegnare all'elemento di lavoro per una determinata proprietà. I campi disponibili dipendono dal tipo di elemento di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td>Immettere o mappare l'ID dell'elemento di lavoro che si desidera aggiornare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un allegato]

Questo modulo di azione carica un file e lo allega a un elemento di lavoro.

Il modulo restituisce l’ID dell’allegato e un URL di download per l’allegato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Progetto] </td> 
   <td> <p>Seleziona il progetto in cui desideri caricare un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elemento di lavoro]</td> 
   <td> <p>Inserisci o mappa l’ID dell’elemento di lavoro in cui desideri caricare un allegato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Immettere il testo di un commento da aggiungere all'allegato caricato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine] </td> 
   <td>Selezionare un file di origine da un modulo precedente oppure immettere o mappare il nome e il contenuto del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Elencare elementi di lavoro]

Questo modulo di azione recupera tutti gli elementi di lavoro di un tipo specifico in un progetto [!DNL Azure DevOps].

Il modulo restituisce l’ID dell’elemento di lavoro principale e di tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Azure DevOps] a Workfront Fusion, vedere <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Azure DevOps] a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Progetto]</td> 
   <td>Selezionare il progetto dal quale si desidera recuperare gli elementi di lavoro.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di elemento di lavoro]</td> 
   <td> <p>Selezionare il tipo di elemento di lavoro da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare le proprietà che si desidera visualizzare nell'output del modulo. I campi disponibili dipendono dal tipo di elemento di lavoro che si desidera recuperare. Selezionare almeno una proprietà.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Immettere o mappare il numero massimo di elementi di lavoro restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>
