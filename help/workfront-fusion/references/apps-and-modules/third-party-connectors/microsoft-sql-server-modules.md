---
title: Moduli di Microsoft SQL Server
description: È possibile utilizzare  [!DNL Adobe Workfront Fusion]  per connettersi a Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server] moduli

È possibile utilizzare [!DNL Adobe Workfront Fusion] per connettersi a [!UICONTROL Microsoft SQL Server].

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Connessione del servizio [!DNL Microsoft SQL Server] a [!DNL Workfront Fusion]

Per istruzioni sulla connessione dell&#39;account [!DNL Microsoft SQL Server] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## Utilizzo di [!DNL Microsoft SQL Server] moduli

È possibile eseguire la logica personalizzata direttamente sul server di database tramite stored procedure. [!DNL Adobe Workfront Fusion] carica dinamicamente l&#39;interfaccia dei parametri di input/output e del recordset in modo che ogni parametro o valore possa essere mappato singolarmente. Prima di iniziare a configurare lo scenario, verificare che l&#39;account utilizzato per la connessione al database disponga dell&#39;accesso in lettura a `INFORMATION_SCHEMA.ROUTINES` e `INFORMATION_SCHEMA.PARAMETERS` visualizzazioni.

Quando [!DNL Fusion] stabilisce la connessione alla destinazione [!DNL SQL server], l&#39;utente [!DNL Fusion] identifica l&#39;host (il nome di dominio o l&#39;indirizzo IP in cui è ospitato il server) e la porta. [!DNL Fusion] può connettersi a qualsiasi host e porta disponibile.

Per informazioni sugli indirizzi IP specifici utilizzati da [!DNL Workfront Fusion], vedere [Indirizzi IP per l&#39;accesso [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Per ulteriori informazioni sulla creazione di una stored procedure, vedere la documentazione di [!DNL Microsoft SQL Server].

>[!NOTE]
>
>[!DNL Workfront Fusion] non supporta più recordset. Viene elaborato solo il primo.

## Risoluzione dei problemi errore [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

Questo errore si verifica quando si modificano gli stessi dati utilizzando più moduli. È causata da transazioni SQL.

Quando viene eseguito un modulo SQL, viene avviata una transazione. La transazione è terminata dopo che lo scenario è stato completamente eseguito.

Se un altro modulo tenta di accedere agli stessi dati, deve attendere il completamento della transazione precedente. Poiché la prima transazione verrà completata al termine dello scenario, la seconda transazione non potrà mai iniziare.

### Soluzione:

Attiva il commit automatico. Il commit automatico termina (esegue il commit) ogni transazione subito dopo l&#39;esecuzione del modulo.

1. Fai clic sull&#39;icona [!UICONTROL Scenario settings] ![icona Impostazioni scenario](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)nella parte inferiore della schermata.
1. Selezionare la casella di controllo **[!UICONTROL Auto commit]**.
1. Fare clic su **[!UICONTROL OK]** per salvare le impostazioni dello scenario.
