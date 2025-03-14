---
title: Connettere Adobe Workfront Fusion a Google Services con misure di sicurezza aggiornate
description: Google ha introdotto restrizioni sul modo in cui gli utenti possono utilizzare le proprie API. Questo articolo descrive come collegare Adobe Workfront Fusion a Google, tenendo conto di queste misure di sicurezza per gli aggiornamenti.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Connettere Adobe Workfront Fusion a Google Services con misure di sicurezza aggiornate

Google ha introdotto restrizioni sul modo in cui gli utenti possono utilizzare le proprie API. Questo articolo descrive come collegare Adobe Workfront Fusion a Google, tenendo conto di queste misure di sicurezza per gli aggiornamenti.

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

## Restrizioni dei servizi Google

A partire dal 1° giugno 2020, Google ha introdotto restrizioni sulle modalità di utilizzo delle API da parte degli utenti. Queste misure di sicurezza proteggono gli utenti di Google dalla perdita o dall&#39;uso improprio dei loro dati personali su Google.

Queste restrizioni sono relative alle app Gmail e Google Drive.

Per ulteriori informazioni su queste restrizioni, vedere &quot;Additional Requirements for Specific API Scopes&quot; in [Criteri per i dati utente di Google API Services](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

Per accedere agli ambiti limitati, è necessario verificare il servizio connesso (Adobe Workfront Fusion o qualsiasi altro servizio che accede ai dati dell’utente tramite l’API) e disporre di una lettera di valutazione che dimostri che il servizio è sicuro e trasparente riguardo al modo in cui utilizza i dati. Workfront Fusion è conforme a tutti i requisiti Google per l&#39;accesso agli ambiti limitati. Tuttavia, la maggior parte dei servizi connessi di terze parti in Workfront Fusion non dispone della lettera di valutazione e pertanto non è conforme ai termini di Google. Per questo motivo, a Workfront Fusion non è consentito inviare dati a questi servizi.

## Eccezioni alle restrizioni dei servizi Google

Esistono alcune eccezioni che consentono di inviare dati a un servizio di terze parti non approvato che non dispone della lettera di valutazione senza violare alcuna delle nuove restrizioni. Differiscono in base al Workspace di Google con il client OAuth di Workfront Fusion, il Workspace di Google con un altro client OAuth oppure @gmail.com e @googlemail.com.

* [Google Workspace con client Workfront Fusion OAuth](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace con un altro client OAuth](#google-workspace-with-another-oauth-client)
* [@gmail.com e @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace con client Workfront Fusion OAuth

Workfront Fusion utilizza l&#39;eccezione di installazione a livello di dominio. L&#39;installazione a livello di dominio è adatta agli utenti di Google Workspace e consente agli utenti di integrare servizi non approvati senza alcuna limitazione. Se sei un utente di Google Workspace, non devi eseguire alcun passaggio aggiuntivo e puoi connetterti direttamente a servizi non approvati.

### Google Workspace con un altro client OAuth

Gli utenti di Google Workspace che preferiscono utilizzare il proprio client OAuth invece di utilizzare il client OAuth di Workfront Fusion possono connettersi ai servizi Google tramite l’approccio per uso interno. Questa opzione è destinata agli utenti avanzati. Per istruzioni, vedere [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com e @googlemail.com {#gmailcom-and-googlemailcom}

Gli utenti che accedono ai servizi Google tramite @gmail.com o @googlemail.com possono connettersi ai servizi Google utilizzando l’approccio Personal Use (Uso personale). Questa opzione è destinata agli utenti avanzati. Per istruzioni, vedere [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Domande frequenti

* [Quali app in Adobe Workfront Fusion sono interessate?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Ho un account Google Workspace?](#do-i-have-a-g-suite-account)
* [Cosa devo fare se sono un utente @gmail.com o @googlemail.com?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [Cosa devo fare se sono un utente di Google Workspace?](#what-should-i-do-if-im-a-g-suite-user)

### Quali app in Adobe Workfront Fusion sono interessate? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail e Email (connessi all&#39;account Gmail).

### Ho un account Google Workspace? {#do-i-have-a-g-suite-account}

Se l&#39;indirizzo di posta elettronica termina con @gmail.com o @googlemail.com, l&#39;account non è un account Workspace di Google. Se l’account Google termina con un dominio personalizzato come @my-company.com, si tratta di un account Google Workspace.

### Cosa devo fare se sono un utente @gmail.com o @googlemail.com? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

Queste nuove restrizioni si applicano solo se si integra Google Drive o Gmail. Se si desidera connettersi a Google Drive o Gmail, è possibile

* Passa a Google Workspace

  oppure

* Crea un client OAuth personalizzato. Questa opzione è destinata agli utenti avanzati.

  Per istruzioni, vedere [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Se si desidera integrare un servizio diverso da Google Drive o Gmail, queste restrizioni non sono applicabili.

### Cosa devo fare se sono un utente di Google Workspace? {#what-should-i-do-if-im-a-g-suite-user}

Non è richiesta alcuna azione.
