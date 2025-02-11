---
title: Chiamare l’API REST di MS Graph
description: Chiamare l’API REST di MS Graph tramite Adobe Workfront Fusion HTTP &> Creare un modulo di richiesta OAuth 2.0
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# Chiamare l’API REST di MS Graph

Molti servizi web di Microsoft sono accessibili tramite l’API di Microsoft Graph. Puoi creare una connessione all’API di Microsoft Graph utilizzando Workfront Fusion HTTP > Creare un modulo di richiesta OAuth 2.0.

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
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

## Registrazione di Workfront Fusion nel portale di registrazione delle applicazioni Microsoft

Per creare una connessione all’API REST di Microsoft Graph, devi prima registrare Adobe Workfront Fusion.

1. Inizia a registrare una nuova applicazione come descritto in [Registra un&#39;applicazione con Microsoft identity platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) nella documentazione di Microsoft.

   Come parte della registrazione, Microsoft richiede le seguenti informazioni:

   <table style="table-layout:auto">
      <tr>
        <td>Nome applicazione</td>
        <td>Immettere un nome per l'applicazione, ad esempio "Applicazione Workfront Fusion personale".</td>
      </tr>
      <tr>
        <td>Reindirizza URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. Dopo aver completato la registrazione dell’app, annota l’ID applicazione.

   >[!IMPORTANT]
   >
   >Per configurare la connessione in Workfront Fusion è necessario disporre dell&#39;ID applicazione.

1. Genera un segreto client. Prendi nota di questo segreto.

   Per istruzioni, vedere [Registrare un&#39;applicazione con Microsoft identity platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) nella documentazione di Microsoft.

   >[!IMPORTANT]
   >
   >Per configurare la connessione in Workfront Fusion è necessario il segreto client.

1. Configura le autorizzazioni per l’applicazione.

   Per informazioni specifiche su come individuare e configurare questi campi, vedere la sezione &quot;Configurare le autorizzazioni per Microsoft Graph&quot; in [Ottenere l&#39;accesso senza un utente](https://docs.microsoft.com/en-us/graph/auth-v2-service) nella documentazione di Microsoft.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Che tipo di autorizzazioni richiede l’applicazione?</td> 
      <td>Selezionare <code>Delegated permissions</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Seleziona autorizzazioni</td> 
      <td> <p>Seleziona le seguenti autorizzazioni:</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Qualsiasi altra autorizzazione richiesta dalle integrazioni (Esempio: <code>User.Read</code>)</p> </li> 
       </ul> <p><b>Importante</b>: per configurare la connessione in Workfront Fusion sono necessarie le autorizzazioni selezionate.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Continua con [Configurare la connessione API di MS Graph in Workfront Fusion](#configure-your-ms-graph-api-connection-in-workfront-fusion).

## Configurare la connessione API di MS Graph in Workfront Fusion

Dopo aver registrato Workfront Fusion come descritto in [Registrare Workfront Fusion nel portale di registrazione delle applicazioni Microsoft](#register-workfront-fusion-in-the-microsoft-application-registration-portal), è possibile configurare la connessione nel modulo di richiesta HTTP > Crea OAuth 2.0.

1. Aggiungi un HTTP > Effettua una chiamata OAuth 2.0 al tuo scenario.
1. Fai clic su **Aggiungi** accanto al campo di connessione.
1. Configura i campi di connessione come segue:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Nome connessione</td> 
      <td>Immettere un nome per la connessione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Ambiente</p> </td> 
      <td>Seleziona se ti connetti a un account di produzione o non di produzione. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Tipo</p> </td> 
      <td>Specificare se ci si connette a un account di servizio o a un account personale. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Tipo di flusso</p> </td> 
      <td>Selezionare <code>Authorization Code</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autorizza URI</td> 
      <td>Immettere <code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">URI token</td> 
      <td>Immettere <code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Limite</td> 
      <td> <p>Immettere le autorizzazioni selezionate durante la registrazione, come descritto in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registra Workfront Fusion nel portale di registrazione applicazioni di Microsoft</a>.</p> <p>Per ogni ambito, fare clic su <b>Aggiungi</b> e digitare l'autorizzazione.</p> <p>Esempio: <code>offline_access</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Separatore ambito</td> 
      <td>Selezionare <code>SPACE</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">ID client</td> 
      <td>Immettere l'ID applicazione dal passaggio 2 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registra Workfront Fusion nel portale di registrazione applicazioni Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Segreto client</td> 
      <td>Immettere il segreto client generato al passaggio 3 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Registra Workfront Fusion nel portale di registrazione applicazioni Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autorizza parametri</td> 
      <td> <p>Aggiungi i seguenti parametri di autorizzazione. Per ogni parametro che si sta aggiungendo, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue: </p> 
       <ul> 
        <li> <p>Chiave:<code> response_mode</code> Valore: <code>query</code></p> </li> 
        <li> <p>Chiave: <code>prompt </code>Valore: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Parametri del token di accesso</td> 
      <td>Non è necessario immettere alcun valore in questo campo.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Aggiorna parametri token</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Fare clic su <b>Aggiungi elemento</b>.</p> </li> 
        <li value="2"> <p>Nel campo <b>Chiave</b> immettere <code>scope</code>.</p> </li> 
        <li value="3"> <p>Nel campo <b>Valore</b> immettere tutti gli ambiti immessi nel campo di ambito, separati da spazi.</p> <p>Esempio: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Intestazioni personalizzate</td> 
      <td>Non è necessario immettere alcun valore in questo campo.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Posizionamento token</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **Continua**.
1. Nella finestra visualizzata, fai clic su **Accetta** per completare la connessione e tornare al modulo.
