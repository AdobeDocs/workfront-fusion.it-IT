---
title: 'Creare una connessione: istruzioni di base'
description: Molti  [!DNL Adobe Workfront Fusion]  connettori non richiedono una configurazione personalizzata durante la creazione di una connessione. Questo articolo descrive il processo predefinito di creazione della connessione.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: ef1a96d9ef4c2c82eaf376c84188e3ed6ea7b2cf
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Creare una connessione: istruzioni di base

Molti connettori [!DNL Adobe Workfront Fusion] non richiedono una configurazione personalizzata durante la creazione di una connessione. Questo articolo descrive il processo predefinito di creazione della connessione.

>[!NOTE]
>
>
>Se Adobe Workfront Fusion non offre un&#39;app per il servizio Web che si desidera utilizzare nello scenario, è possibile connettersi al servizio Web utilizzando i moduli HTTP e Webhook di [!DNL Workfront Fusion], come spiegato nei seguenti articoli:
>
>* [Connettere Adobe Workfront Fusion a un servizio Web che utilizza l&#39;autorizzazione token API](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configurare un webhook per un servizio Web senza un connettore](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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

## Creare una connessione

Per creare una connessione all&#39;interno di un modulo [!DNL Workfront Fusion]:

1. Fare clic su **[!UICONTROL Add]** accanto alla casella [!UICONTROL Connection] per aprire il pannello **[!UICONTROL Create a connection]**.
1. (Facoltativo) Modificare il valore predefinito **[!UICONTROL Connection name]**.
1. Nel campo Ambiente, seleziona se si tratta di un ambiente di produzione o non di produzione. Queste informazioni vengono visualizzate nell&#39;area Connessioni di Fusion.
1. Nel campo Tipo selezionare se si tratta di un account di servizio o personale. Queste informazioni vengono visualizzate nell&#39;area Connessioni di Fusion.
1. (Condizionale) Se l&#39;app richiede impostazioni di connessione avanzate, ad esempio un ID, una chiave o [!UICONTROL secret], immetti tali informazioni.

   Potrebbe essere necessario fare clic su **[!UICONTROL Show advanced settings]** per visualizzare i campi in cui è possibile immettere questo tipo di informazioni.

1. Fare clic su **[!UICONTROL Continue]**.
1. Nella finestra di accesso visualizzata, inserisci le credenziali per accedere all’app, se non lo hai già fatto.
1. (Condizionale) Se viene visualizzato un pulsante **[!UICONTROL Allow]**, esamina le azioni che il connettore potrà eseguire, quindi fai clic sul pulsante per connettere l&#39;app a [!DNL Workfront Fusion].

   >[!NOTE]
   >
   >Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
   >
   >Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.
