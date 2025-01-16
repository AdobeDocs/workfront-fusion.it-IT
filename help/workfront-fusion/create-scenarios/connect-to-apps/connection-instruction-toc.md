---
title: Creare connessioni
description: Una connessione deve rispettare i requisiti impostati dall’API dell’app o del servizio web a cui si connette. Per questo motivo, le istruzioni per la configurazione di una connessione variano a seconda dell’app o del servizio web. Questo articolo ti aiuta a identificare e individuare le istruzioni per la connessione di [!DNL Adobe Workfront Fusion] all'app o al servizio Web scelto.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Creare connessioni

Una connessione deve rispettare i requisiti impostati dall’API dell’app o del servizio web a cui si connette. Per questo motivo, le istruzioni per la configurazione di una connessione variano a seconda dell’app o del servizio web. Questo articolo consente di identificare e individuare le istruzioni per la connessione di [!DNL Adobe Workfront Fusion] all&#39;app o al servizio Web scelto.

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

## Connettersi a un&#39;app o a un servizio Web che non richiede configurazione

Nella maggior parte dei casi, è possibile utilizzare il modulo per creare una connessione con poche o nessuna informazione aggiuntiva. [!DNL Workfront Fusion] gestisce automaticamente l&#39;autenticazione.

Per istruzioni sulla creazione di una connessione senza considerazioni particolari, vedere [Creare una connessione - istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Connettersi a un’app o a un servizio Adobe

Per connetterti a un’app o a un servizio di Adobe, potresti aver bisogno di informazioni provenienti da Adobe Admin Console, ad esempio l’ID organizzazione o l’ID account tecnico.

Puoi anche utilizzare il modulo Adobe Authenticator per connetterti a qualsiasi API Adobe, utilizzando una singola connessione. Questo consente di connettersi più facilmente a prodotti Adobe che non dispongono ancora di un connettore Fusion dedicato.

Per istruzioni specifiche, vedere [l&#39;articolo relativo al connettore](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Connetti a un&#39;app o a un servizio Web [!DNL Microsoft]

La maggior parte delle app [!DNL Microsoft] in [!DNL Workfront Fusion] consente di creare una connessione senza informazioni aggiuntive.

Nelle circostanze seguenti sono necessari ulteriori passaggi per la creazione di una connessione:

* Utilizzo dei moduli Microsoft Dynamics 365.

  Per istruzioni, vedere [Moduli Microsoft Dynamics 365](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Connessione all’API del grafico Microsoft tramite un modulo HTTP

  Per istruzioni, consulta [Chiamare l&#39;API REST di MS Graph](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Connetti a un&#39;app o a un servizio Web [!DNL Google]

Il processo di connessione alle app [!DNL Google] può variare in base al tipo di account [!DNL Google] utilizzato. Inoltre, [!DNL Google] misure di sicurezza potrebbero richiedere una configurazione aggiuntiva durante la connessione a [!DNL Workfront Fusion].

Per ulteriori informazioni, consulta:

* [Connettere Adobe Workfront Fusion a Google Services utilizzando un client OAuth personalizzato](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Connettere Adobe Workfront Fusion a Google Services con misure di sicurezza aggiornate](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Altre app che richiedono una configurazione aggiuntiva

Alcune app e servizi non seguono la configurazione di base per le connessioni [!DNL Workfront Fusion]. Le istruzioni per la connessione di queste app sono disponibili nell’articolo relativo all’app.

Per istruzioni specifiche, vedere [l&#39;articolo relativo al connettore](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
