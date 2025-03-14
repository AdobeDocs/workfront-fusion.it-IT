---
title: Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato
description: È possibile utilizzare Adobe Workfront Fusion per connettersi ai servizi Google utilizzando un client OAuth personalizzato. Questa procedura richiede un account Google esistente.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 1%

---

# Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato

È possibile utilizzare Adobe Workfront Fusion per connettersi ai servizi Google utilizzando un client OAuth personalizzato. Questa procedura richiede un account Google esistente.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront 
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
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Selezionare o Prime Workfront Plan: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Ultimate Workfront: Workfront Fusion è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per effettuare questa connessione è necessario un account Google esistente.

## Connettere Fusion ai servizi Google utilizzando un client OAuth personalizzato

Per creare questa connessione, devi creare e configurare un progetto sulla piattaforma Google Cloud, quindi configurare la connessione in Fusion in base a tale progetto.

>[!NOTE]
>
>Questa procedura è destinata:
>
>* Uso personale (`@gmail.com` e `@googlemail.com` utenti)
>* Uso interno (utenti di Google Workspace che preferiscono utilizzare un client OAuth personalizzato)

* [Creare un progetto su Google Cloud Platform](#create-a-project-on-google-cloud-platform)
* [Configura impostazioni consenso OAuth](#configure-oauth-consent-settings)
* [Crea credenziali OAuth](#create-oauth-credentials)
* [Connessione a Google in Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Creare un progetto su Google Cloud Platform

Per creare un progetto su Google Cloud Platform:

1. Inizia a creare un progetto su Google Cloud Platform.

   Per istruzioni, consulta [Creare un progetto Google Cloud](https://developers.google.com/workspace/guides/create-project) nella documentazione di Google.
1. Quando abiliti le API, devi abilitare sia l’API di Google Drive che l’API di tutte le app Google che desideri utilizzare (come l’API dei fogli di Google).
1. Termina la creazione del progetto.
1. Passa alla sezione [Configurare le impostazioni del consenso OAuth](#configure-oauth-consent-settings) in questo articolo.

### Configurare le impostazioni di consenso OAuth

1. Inizio della configurazione di OAuth per il progetto

   Per istruzioni, consulta [Configurare la schermata di consenso OAuth e scegliere gli ambiti](https://developers.google.com/workspace/guides/configure-oauth-consent) nella documentazione di Google.
1. Seleziona **External**, quindi fai clic su **Create**.

   >[!NOTE]
   >
   >Selezionando questa opzione non verrà addebitato alcun importo. Per ulteriori informazioni, vedere Informazioni di Google sulle eccezioni ai requisiti di verifica.

1. Compila i campi obbligatori come segue:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Nome app</p> </td> 
      <td> <p>Inserisci il nome dell’app che richiede il consenso.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mail di supporto utente</td> 
      <td>Immetti un indirizzo e-mail che gli utenti dovranno contattare per eventuali domande sul consenso durante la connessione a questa app.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Indirizzi e-mail</td> 
      <td>Immetti uno o più indirizzi e-mail che Google può utilizzare per informarti di eventuali modifiche al progetto.</td> 
     </tr> 
    </tbody> 
   </table>

1. In Domini autorizzati, fare clic su **Aggiungi dominio** e immettere `workfrontfusion.com`.
1. Aggiungi i seguenti ambiti:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Servizio/API</th> 
      <th>Ambiti richiesti</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   Potrebbe essere necessario espandere l&#39;elenco o passare alla pagina successiva dell&#39;elenco per visualizzarli tutti.

1. (Facoltativo) Aggiungi eventuali utenti di test al progetto.
1. Verifica la precisione delle informazioni, quindi fai clic su **Torna al dashboard**.

   >[!NOTE]
   >
   >Non è necessario inviare la schermata di consenso e la richiesta di verifica per Google.

1. Continua con [Crea credenziali OAuth](#create-oauth-credentials).

### Crea credenziali OAuth

1. Inizia a creare le credenziali ID client OAuth.

   Per istruzioni, vedere [Creare le credenziali di accesso](https://developers.google.com/workspace/guides/create-credentials) nella documentazione di Google.

   >[!NOTE]
   >
   >Se non si tratta della prima API o del primo servizio (Gmail o Google Drive) attivato, non è necessario creare nuove credenziali.

1. Compila i campi obbligatori come segue:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Tipo di applicazione</td> 
      <td> <p> Applicazione web</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nome</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. In URI di reindirizzamento autorizzati immettere **uno** dei seguenti valori:

   * Per unità Gmail o Google: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * Per altre app Google: `https://app.workfrontfusion.com/oauth/cb/google`

1. Fai clic su **Crea**.

   Vengono visualizzati l’ID client e il segreto client.

1. Copia l’ID client e il segreto client in una posizione sicura. Le utilizzerai per stabilire una connessione in Workfront Fusion.
1. Continua con [Connetti a Google in Workfront Fusion](#connect-to-google-in-workfront-fusion).

### Connessione a Google in Workfront Fusion

Il processo di creazione di una connessione a Google varia a seconda che si utilizzi un modulo di un servizio Google (ad esempio Google Sheets o Google Docs) o che si stia effettuando la connessione a Google tramite HTTP > Creare un modulo di richiesta OAuth2.0.

* [Connessione a Google in un servizio Google](#connect-to-google-in-a-google-service)
* [Connettiti a Google nel HTTP > Creare un modulo di richiesta OAuth2.0](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Connessione a Google in un servizio Google

1. In Workfront Fusion, individua il modulo Google necessario per la creazione di una connessione.
1. Fai clic su **Crea una connessione**, quindi su **Mostra impostazioni avanzate**.
1. Compila i campi Nome connessione, Ambiente e Tipo, a seconda dei casi.
1. Immetti l&#39;ID client e il segreto client recuperati in [Crea credenziali OAuth](#create-oauth-credentials) nei rispettivi campi, quindi fai clic su **Continua**.

1. Accedi con il tuo account Google.

   Viene visualizzata la finestra **L&#39;app non è verificata**. Tieni presente che l’&quot;app&quot; indicata nel titolo della finestra è il client OAuth creato in precedenza.

1. Fai clic su **Avanzate**, quindi su **Vai a Workfront Fusion (unsafe)** per consentire l&#39;accesso utilizzando il client OAuth personalizzato.

1. Fare clic su **Consenti** per concedere l&#39;autorizzazione di Workfront Fusion.
1. Nella finestra visualizzata, fai di nuovo clic su **Consenti** per confermare le scelte effettuate.

   Viene stabilita la connessione al servizio Google desiderato utilizzando un client OAuth personalizzato.

#### Connettiti a Google nel HTTP > Creare un modulo di richiesta OAuth2.0 {#connect-to-google-in-the-http--make-an-oauth20-request-module}

Per istruzioni sulla connessione a Google in HTTP > Creare un modulo di richiesta OAuth2.0, consulta [Istruzioni per la creazione di una connessione a Google in HTTP > Creare un modulo di richiesta OAuth 2.0](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) nell&#39;articolo HTTP > Creare un modulo di richiesta OAuth 2.0.

## Possibile messaggio di errore:[Accesso 403 non configurato]

Se viene visualizzato il messaggio di errore `403 Access Not Configured`, è necessario abilitare l&#39;API corrispondente nella piattaforma Google Cloud. Per abilitare l&#39;API, segui i passaggi descritti nella sezione [Creare un progetto su Google Cloud Platform](#create-a-project-on-google-cloud-platform) in questo articolo.
