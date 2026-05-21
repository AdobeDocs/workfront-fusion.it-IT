---
title: Moduli Microsoft SQL Server
description: È possibile utilizzare Adobe Workfront Fusion per connettersi a Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
TQID: https://experienceleague.adobe.com/etKUNkjJF0UreB6qI-ckU0tOF96RY6Yey1ADVcpOWfo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 531
ht-degree: 24%

---

# Moduli [!DNL Microsoft SQL Server]

È possibile utilizzare Adobe Workfront Fusion per connettersi a [!UICONTROL Microsoft SQL Server].

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

## Connessione del servizio [!DNL Microsoft SQL Server] a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account [!DNL Microsoft SQL Server] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## Utilizzo di [!DNL Microsoft SQL Server] moduli

È possibile eseguire la logica personalizzata direttamente sul server di database tramite stored procedure. Adobe Workfront Fusion carica dinamicamente l&#39;interfaccia dei parametri di input/output e del recordset in modo che ogni parametro o valore possa essere mappato singolarmente. Prima di iniziare a configurare lo scenario, verificare che l&#39;account utilizzato per la connessione al database disponga dell&#39;accesso in lettura a `INFORMATION_SCHEMA.ROUTINES` e `INFORMATION_SCHEMA.PARAMETERS` visualizzazioni.

Quando [!DNL Fusion] stabilisce la connessione alla destinazione [!DNL SQL server], l&#39;utente [!DNL Fusion] identifica l&#39;host (il nome di dominio o l&#39;indirizzo IP in cui è ospitato il server) e la porta. [!DNL Fusion] può connettersi a qualsiasi host e porta disponibile.

Per informazioni su indirizzi IP specifici utilizzati da Workfront Fusion, vedere [Indirizzi IP per l&#39;accesso ad Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Per ulteriori informazioni sulla creazione di una stored procedure, vedere la documentazione di [!DNL Microsoft SQL Server].

>[!NOTE]
>
>Workfront Fusion non supporta più recordset. Viene elaborato solo il primo.

## Risoluzione dei problemi errore [!UICONTROL ER_LOCK_WAIT_TIMEOUT: timeout di attesa blocco superato; provare a riavviare la transazione]

Questo errore si verifica quando si modificano gli stessi dati utilizzando più moduli. È causata da transazioni SQL.

Quando viene eseguito un modulo SQL, viene avviata una transazione. La transazione è terminata dopo che lo scenario è stato completamente eseguito.

Se un altro modulo tenta di accedere agli stessi dati, deve attendere il completamento della transazione precedente. Poiché la prima transazione verrà completata al termine dello scenario, la seconda transazione non potrà mai iniziare.

### Soluzione:

Attiva il commit automatico. Il commit automatico termina (esegue il commit) ogni transazione subito dopo l&#39;esecuzione del modulo.

1. Fai clic sull&#39;icona [!UICONTROL Impostazioni scenario] ![Icona Impostazioni scenario](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)nella parte inferiore della schermata.
1. Selezionare la casella di controllo **[!UICONTROL Auto commit]**.
1. Fare clic su **[!UICONTROL OK]** per salvare le impostazioni dello scenario.
