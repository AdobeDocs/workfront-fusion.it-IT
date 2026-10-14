---
title: Moduli AWS S3
description: I moduli S3 di [!DNL Adobe Workfront Fusion AWS] consentono di eseguire operazioni sui bucket S3.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
TQID: 'https://experienceleague.adobe.com/FDkre6osF2kT7Kz-5VGradQLa7GPSJ6MHPH9-FgM-ag'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 7c25013f7a94000651e8331199ad985d40651ae3
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 16%
---
# Moduli AWS S3

I moduli S3 di [!DNL Adobe Workfront Fusion AWS] consentono di eseguire operazioni sui bucket S3.

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

Per utilizzare i moduli [!UICONTROL AWS S3], è necessario disporre di un account [!DNL Amazon Web Service].

## Informazioni sull’API di AWS S3

Il connettore AWS S3 utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td><pre><code>https://s3.&#123;&#123;parameters.region&#125;&#125;.amazonaws.com</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL AWS] a Workfront Fusion {#connect-aws-to-workfront-fusion}

* [Connettere AWS a Workfront Fusion utilizzando una connessione federata](#connect-aws-to-workfront-fusion-using-a-federated-connection)
* [Connettere AWS a Workfront Fusion utilizzando un utente API](#connect-aws-to-workfront-fusion-using-an-api-user)

### Connettere AWS a Workfront Fusion utilizzando una connessione federata

+++ Espandere per visualizzare le istruzioni per questo tipo di connessione.

* [Prerequisiti per la connessione di AWS a Workfront Fusion tramite una connessione federata](#prerequisites-to-connecting-aws-to-workfront-fusion-using-a-federated-connection)
* [Aggiungere Workfront Fusion come provider di identità in AWS](#add-workfront-fusion-as-an-identity-provider-in-aws)
* [Creare il ruolo IAM](#create-the-iam-role)
* [Creare la connessione in Workfront Fusion](#create-the-connection-in-workfront-fusion)
* [Aggiungere la connessione al criterio di attendibilità del ruolo](#add-the-connection-to-the-roles-trust-policy)
* [Verificare la connessione](#verify-the-connection)
* [Risoluzione dei problemi](#troubleshooting)

Una connessione federata consente a Workfront Fusion di accedere all’account AWS senza dover creare un utente IAM o archiviare una chiave di accesso in Fusion.
Al contrario, si registra Workfront Fusion come provider di identità attendibile nell&#39;account AWS e si configura quale singola connessione Fusion è autorizzata a utilizzare un particolare ruolo IAM. Quando la connessione viene eseguita, Fusion presenta una prova di identità di breve durata e AWS restituisce credenziali temporanee che scadono autonomamente. Non viene mai creata, memorizzata o ruotata alcuna chiave di lunga durata.

>[!NOTE]
>
>La configurazione di questa connessione richiede due visite alla console AWS. È innanzitutto necessario creare il ruolo, quindi creare la connessione in Workfront Fusion, quindi tornare ad AWS per completare il criterio di attendibilità. Questo perché parte del criterio di attendibilità identifica una connessione specifica e tale identificatore non esiste finché non viene creata la connessione.

#### Prerequisiti per la connessione di AWS a Workfront Fusion tramite una connessione federata

Per creare questa connessione, è necessario disporre dei seguenti elementi:

* Autorizzazione in AWS IAM per creare un provider di identità e per creare e modificare ruoli. Questo di solito significa la polizza o equivalente. Se non disponi di questo accesso, chiedi a qualcuno sul tuo cloud o
team di sicurezza per completare i passaggi di AWS.
* Possibilità di creare connessioni in Workfront Fusion.


#### Aggiungere Workfront Fusion come provider di identità in AWS

Questo passaggio indica ad AWS che i token rilasciati da Workfront Fusion possono essere considerati attendibili. Puoi eseguire questa operazione una volta per ogni account AWS. Se un utente dell&#39;organizzazione ha già aggiunto questo provider, passa a [Crea il ruolo IAM](#create-the-iam-role).

1. Accedi alla console AWS e passa a **IAM** > **Provider di identità**.
1. Selezionare **Aggiungi provider**.
1. Per Tipo provider, selezionare **Connessione OpenID**.
1. Nell&#39;URL del provider, immetti quanto segue, quindi seleziona **Ottieni identificazione personale**:

   ```
   https://oidc.automations.adobe.com
   ```

1. In Pubblico, immetti quanto segue:

   ```
   sts.amazonaws.com
   ```

1. Selezionare **Aggiungi provider**.
1. Continuare a [Creare il ruolo IAM](#create-the-iam-role).

#### Creare il ruolo IAM

Il ruolo definisce l’operazione che la connessione può eseguire nell’account AWS. È possibile creare un ruolo per ogni connessione, in modo che l&#39;accesso di ogni connessione possa essere concesso e revocato in modo indipendente.

1. In IAM, vai a **Ruoli** e seleziona **Crea ruolo**.
1. Per Tipo di entità attendibile, selezionare **Identità Web**.
1. Nel provider di identità, selezionare `oidc.automations.adobe.com`.
1. In Pubblico, selezionare `sts.amazonaws.com`.
1. Seleziona **Avanti**, quindi allega i criteri di autorizzazione necessari per la connessione.
Concedi solo le autorizzazioni effettivamente utilizzate dalla connessione. Ad esempio, una connessione che legge solo da
per un bucket non è necessario `AmazonS3FullAccess`.
1. Assegna al ruolo un nome chiaro e riconoscibile. Ad esempio, `WorkfrontFusionFederatedConnection`.
1. Seleziona **Crea ruolo**.
1. Aprire il ruolo appena creato e copiare il relativo ARN dall&#39;area Riepilogo. Si presenta così: `arn:aws:iam::123456789012:role/WorkfrontFusionFederatedConnection`

1. Continua con [Crea la connessione in Workfront Fusion](#create-the-connection-in-workfront-fusion).

#### Creare la connessione in Workfront Fusion

1. Nella schermata di configurazione della connessione del modulo, seleziona il tipo di connessione federata.
1. Immettere il ruolo ARN copiato in [Creare il ruolo IAM](#create-the-iam-role).
1. Seleziona **Crea**.
In Workfront Fusion vengono visualizzati tre valori. Utilizzale nella procedura successiva.

<table>
  <tr>
    <td>Emittente</td>
    <td>Sempre <code>https://oidc.automations.adobe.com</code>. Corrisponde al provider di identità aggiunto in AWS.</td>
  </tr>
  <tr>
    <td>Soggetto</td>
    <td>Identifica questa connessione. È <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>. È diversa per ogni connessione creata.</td>
  </tr>
  <tr>
    <td>Pubblico</td>
    <td>Sempre <code>sts.amazonaws.com</code>.</td>
  </tr>
</table>

1. Lasciate aperto questo pannello e copiate il valore Oggetto.

   >[!NOTE]
   >
   >Non chiudere il pannello e non selezionare Annulla. La connessione non viene completata fino a quando non vengono completate le procedure rimanenti. Se chiudi il pannello, devi eliminare la connessione e riavviarla, perché a una nuova connessione viene assegnato un nuovo Oggetto.

1. Continua con [Aggiungi la connessione al criterio di attendibilità del ruolo](#add-the-connection-to-the-roles-trust-policy).

#### Aggiungere la connessione al criterio di attendibilità del ruolo

Fino a quando non si completa questa procedura, il ruolo considera attendibile Workfront Fusion in generale, ma non consente ancora l&#39;utilizzo di questa connessione specifica.

1. In una nuova scheda del browser, torna alla console AWS e apri il ruolo creato.
1. Selezionare la scheda **Relazioni di trust**, quindi selezionare **Modifica criterio di attendibilità**.
1. Sostituisci il criterio con il seguente, sostituendo i tuoi valori:

   * Sostituisci `123456789012` con il tuo ID account AWS
   * Sostituire il valore `sub` con l&#39;oggetto copiato da Workfront Fusion.


   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow", 
         "Principal": {
           "Federated": "arn:aws:iam::123456789012:oidc-provider/oidc.automations.adobe.com"
       },
       "Action": "sts:AssumeRoleWithWebIdentity", "Condition": {
        "StringEquals": {
          "oidc.automations.adobe.com:sub": "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", 
          "oidc.automations.adobe.com:aud": "sts.amazonaws.com"
        }
       }
      }
    ]
   }
   ```

1. Seleziona **Aggiorna criterio**.
1. Continua con [Verifica la connessione](#verify-the-connection).

>[!TIP]
>
>Per consentire a più connessioni di utilizzare lo stesso ruolo, elencare i soggetti come un array. AWS consente di utilizzare il ruolo se il token corrisponde a qualsiasi valore nell’elenco:
>
>```
>"oidc.automations.adobe.com:sub": [ "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:29011"
>]
>```
>
>Non sostituire il valore secondario con un carattere jolly. In questo modo qualsiasi connessione dell’organizzazione può utilizzare il ruolo, incluse le connessioni create in seguito da altri utenti


#### Verificare la connessione

1. Tornare alla scheda del browser Workfront Fusion, dove il pannello di connessione è ancora aperto.
1. Fai clic su **Salva**.

   Workfront Fusion contatta AWS, che controlla il criterio di attendibilità e restituisce credenziali temporanee. Se tutto è configurato correttamente, la connessione viene convalidata correttamente e puoi procedere con la configurazione del modulo.
   Se la verifica non riesce, il pannello rimane aperto e visualizza l’errore. Correggi il problema in AWS e seleziona nuovamente Salva. Non è necessario ricreare la connessione e l&#39;oggetto non cambia.

Da questo punto in poi, la connessione rinnova le proprie credenziali. Non c&#39;è alcuna chiave da ruotare e non c&#39;è nessuna scadenza da mantenere.

#### Risoluzione dei problemi


<table>
  <tr>
    <th>Errore</th>
    <th>Che cosa significa</th>
    <th>Cosa controllare</th>
  </tr>
  <tr>
    <td>InvalidIdentityToken</td>
    <td>AWS non è riuscito a far corrispondere il token con un provider di identità registrato.</td>
    <td>Verifica di aver aggiunto il provider di identità descritto in Aggiungere Workfront Fusion come provider di identità in AWS e che il relativo URL sia esattamente https://oidc.automations.adobe.com, senza barra finale.</td>
  </tr>
  <tr>
    <td>Accesso negato quando si assume il ruolo</td>
    <td>Il provider di identità è registrato, ma i criteri di attendibilità non corrispondono a questa connessione.</td>
    <td>Verificare che il valore secondario nel criterio di attendibilità sia identico a carattere per carattere all'oggetto visualizzato in Workfront Fusion e che il valore aud sia sts.amazonaws.com. La causa più comune è un oggetto copiato da una connessione diversa.</td>
  </tr>
  <tr>
    <td>La connessione funziona, quindi ha esito negativo in un secondo momento</td>
    <td> </td>
    <td>Verificare se i criteri di autorizzazione del ruolo sono stati modificati o se il ruolo è stato eliminato e ricreato. La ricreazione di un ruolo non modifica il relativo ARN, ma reimposta i criteri di attendibilità.</td>
  </tr>
</table>

+++

### Connettere AWS a Workfront Fusion utilizzando un utente API

+++ Espandere per visualizzare le istruzioni per questo tipo di connessione.

Per connettere [!DNL AWS S3] a Workfront Fusion è necessario connettere l&#39;account [!DNL AWS] a Workfront Fusion. A tale scopo, è innanzitutto necessario creare un utente API in [!DNL AWS] [!UICONTROL IAM].

1. Accedi al tuo account [!DNL AWS] [!UICONTROL IAM].
1. Passa a **[!UICONTROL Gestione identità e accessi]** > **[!UICONTROL Gestione accessi]** > **[!UICONTROL Utenti]**.

1. Fare clic su **[!UICONTROL Aggiungi utente]**.
1. Immettere il nome del nuovo utente e selezionare l&#39;opzione **[!UICONTROL Accesso a livello di codice]** nella sezione [!UICONTROL Tipo di accesso].
1. Fai clic su **[!UICONTROL Allega direttamente i criteri esistenti]**, quindi cerca **[!UICONTROL AmazonS3FullAccess]** nella barra di ricerca. Fare clic su di esso quando viene visualizzato, quindi fare clic su **[!UICONTROL Avanti]**.

1. Passare alle altre finestre di dialogo, quindi fare clic su **[!UICONTROL Crea utente]**.
1. Copia l&#39;**[!UICONTROL ID chiave di accesso]** e la **[!UICONTROL Chiave di accesso segreta]** forniti.

1. Passare a Workfront Fusion e aprire la finestra di dialogo **[!UICONTROL Crea connessione]** del modulo [!DNL AWS S3].
1. Immetti l&#39;[!UICONTROL ID chiave di accesso] e la [!UICONTROL Chiave di accesso segreta] dal passaggio 7 ai rispettivi campi e fai clic su **[!UICONTROL Continua]** per stabilire la connessione.

La connessione è stata stabilita. Puoi procedere con la configurazione del modulo.

+++

## Moduli [!DNL AWS S3] e relativi campi

* [Azioni](#actions)
* [Ricerche](#searches)

Quando configuri i moduli [!DNL AWS S3], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL AWS S3], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Ricerche](#searches)

### Azioni

* [[!UICONTROL Crea bucket]](#create-bucket)
* [[!UICONTROL Ottieni file]](#get-file)
* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)
* [[!UICONTROL Carica file]](#upload-file)

#### [!UICONTROL Crea bucket]

Questo modulo di azione crea un bucket in AWS.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Immetti il nome del nuovo bucket.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni file]

Questo modulo di azione scarica un file da un bucket.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Seleziona il bucket da cui desideri scaricare il file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Percorso]</p> </td> 
   <td> <p>Immettere il percorso del file. Esempio: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione effettua una chiamata personalizzata all’API AWS S3.

Per informazioni dettagliate sull&#39;API [!DNL Amazon S3], vedere [[!DNL Amazon S3] [!UICONTROL REST] Introduzione all&#39;API](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Immetti un URL host. Il percorso deve essere relativo a <code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta [!UICONTROL HTTP] necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] metodi di richiesta in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi un’intestazione di richiesta. Per ogni intestazione che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere l'intestazione. Puoi utilizzare le seguenti intestazioni di richiesta comuni. Per ulteriori intestazioni di richiesta fare riferimento alla documentazione API <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3]</a>.</p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Nome intestazione</th> 
       <th> <p> Descrizione</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Lunghezza del messaggio (senza intestazioni) in base alla RFC 2616. Questa intestazione è necessaria per [!UICONTROL PUT]s e le operazioni di caricamento di XML, ad esempio log e ACL.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>Il tipo di contenuto della risorsa, nel caso in cui il contenuto della richiesta sia nel corpo. Esempio: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>Il digest MD5 a 128 bit codificato in base a base64 del messaggio (senza le intestazioni) in base alla RFC 1864. Questa intestazione può essere utilizzata come controllo di integrità del messaggio per verificare che i dati siano gli stessi dati inviati originariamente. Sebbene sia opzionale, si consiglia di utilizzare il meccanismo [!UICONTROL Content-MD5] come controllo di integrità end-to-end. Per ulteriori informazioni sull'autenticazione delle richieste REST, vedere <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">Firma e autenticazione delle richieste REST</a> nella documentazione di AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>Data e ora correnti in base al richiedente. Esempio: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Quando si specifica l'intestazione <code>Authorization </code>, è necessario specificare l'intestazione <code>x-amz-date</code> o <code>Date </code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL expected]</p> </td> 
       <td> <p>Quando l'applicazione utilizza [!UICONTROL 100-continue], non invia il corpo della richiesta finché non riceve una conferma. Se il messaggio viene rifiutato in base alle intestazioni, il corpo del messaggio non viene inviato. Questa intestazione può essere utilizzata solo se invii un corpo.</p> <p>Valori validi: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Per le richieste di tipo percorso, il valore è <code>s3.amazonaws.com</code>. Per le richieste in stile virtuale, il valore è <code>BucketName.s3.amazonaws.com</code>. Per ulteriori informazioni, vedi <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Hosting virtuale</a> nella documentazione di AWS.</p> <p>Questa intestazione è obbligatoria per HTTP 1.1 (la maggior parte dei toolkit aggiunge questa intestazione automaticamente); facoltativa per le richieste HTTP/1.0.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Quando si utilizza la firma versione 4 per autenticare la richiesta, questa intestazione fornisce un hash del payload della richiesta. Quando si carica un oggetto in blocchi, impostare il valore su <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> per indicare che la firma copre solo le intestazioni e che non è presente alcun payload. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Calcoli della firma per l'intestazione di autorizzazione</a> nella documentazione di AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>Data e ora correnti in base al richiedente. Esempio: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Quando si specifica l'intestazione <code>Authorization </code>, è necessario specificare l'intestazione <code>x-amz-date</code> o <code>Date </code>. Se si specificano entrambi, il valore specificato per l'intestazione <code>x-amz-date</code> ha la precedenza.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Questa intestazione può essere utilizzata nei seguenti scenari:</p> 
        <ul> 
         <li>Fornire token di sicurezza per le operazioni [!DNL Amazon DevPay]. Ogni richiesta che utilizza [!DNL Amazon DevPay] richiede due intestazioni <code>x-amz-security-token</code>: una per il token di prodotto e una per il token utente. Quando [!DNL Amazon S3] riceve una richiesta autenticata, confronta la firma calcolata con la firma fornita. Le intestazioni con più valori formattate in modo non corretto utilizzate per calcolare una firma possono causare problemi di autenticazione.</li> 
         <li>Fornisci un token di sicurezza quando utilizzi credenziali di sicurezza temporanee. Quando effettui richieste utilizzando le credenziali di sicurezza temporanee ottenute da IAM, devi fornire un token di sicurezza utilizzando questa intestazione. Per ulteriori informazioni sulle credenziali di sicurezza temporanee, vedere Creazione di richieste.</li> 
        </ul> <p>Questa intestazione è necessaria per le richieste che utilizzano [!DNL Amazon DevPay] e per le richieste firmate utilizzando credenziali di sicurezza temporanee.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi le stringhe di query desiderate, ad esempio parametri o campi modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:   <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica file]

Questo modulo di azione carica un file in un bucket AWS S3.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Cartella] </p> </td> 
   <td> <p>Specificare la cartella di destinazione in cui si desidera caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (facoltativo)</p> </td> 
   <td> <p> Per ogni intestazione da aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore dell'intestazione.</p><p> Per le intestazioni disponibili, vedi <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a> nella documentazione di AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL File di elenco]](#list-files)
* [[!UICONTROL Cartelle elenco]](#list-folders)

#### [!UICONTROL File di elenco]

Restituisce un elenco di file da una posizione specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selezionare il bucket [!DNL Amazon S3] in cui cercare i file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix]</p> </td> 
   <td> <p> Immetti il percorso di una cartella in cui cercare i file, ad esempio <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cartelle elenco]

Restituisce un elenco di cartelle da una posizione specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL AWS] a Workfront Fusion, consulta <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connettere [!DNL AWS] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Seleziona l’endpoint regionale. Per ulteriori informazioni, consulta <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">endpoint regionali</a> nella documentazione di [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Selezionare il bucket [!DNL Amazon S3] in cui si desidera cercare le cartelle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (facoltativo)</p> </td> 
   <td> <p> Percorso di una cartella in cui cercare le cartelle, ad esempio <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
