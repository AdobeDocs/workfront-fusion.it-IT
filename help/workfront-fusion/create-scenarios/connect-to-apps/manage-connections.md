---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Gestire le connessioni
description: Per la maggior parte delle app, è necessario creare una connessione tramite la quale Adobe Workfront Fusion possa comunicare con il servizio di terze parti in base alle impostazioni dello scenario specifico.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: d13312031955a697e10ddfcdc2e64dfe198b3dac
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---

# Gestire le connessioni

Una connessione rappresenta l&#39;autorizzazione e le autorizzazioni utilizzate da Fusion per accedere all&#39;applicazione. È possibile creare una o più connessioni per ogni applicazione e utilizzare la stessa connessione in più moduli o scenari.

È possibile gestire queste connessioni nell&#39;area Connessioni.

Per ulteriori informazioni sulle connessioni, vedere [Panoramica connessione](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
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
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visualizzare e gestire le connessioni

È possibile gestire tutte le connessioni dall&#39;area Connessioni.

>[!NOTE]
>
>Le connessioni sono di proprietà dei team. Se non riesci a trovare la connessione che stai cercando, controlla che tu stia visualizzando il team corretto.
>
>Per selezionare un nuovo team, fai clic sul nome del team nell’area di navigazione a sinistra e seleziona un nuovo team.

1. Per aprire l&#39;area Connessioni, fare clic su **Connessioni** ![Icona Connessioni](assets/connections-icon.png) nell&#39;area di navigazione a sinistra.
1. Individuare la connessione che si desidera gestire, quindi eseguire uno o più dei seguenti passaggi nella riga della connessione.
1. (Facoltativo) Assegna un ambiente e un tipo di connessione facendo clic sui menu a discesa **Ambiente** e **Tipo** e selezionando un&#39;opzione.
1. (Facoltativo) Per visualizzare le autorizzazioni assegnate a Workfront Fusion per la connessione, fare clic sull&#39;icona Visualizza ![Visualizza autorizzazioni di connessione](assets/view-connection-permissions.png) per la connessione.
1. (Facoltativo) Per rinominare una connessione, evidenziarne il nome e digitare il nuovo nome.
1. (Facoltativo) Per autorizzare nuovamente una connessione, seleziona la casella di controllo accanto alla connessione, quindi fai clic su **Riautorizza** nella parte inferiore della schermata.
1. (Facoltativo) Per eliminare una connessione, seleziona la casella di controllo accanto alla connessione, fai clic su **Elimina** nella parte inferiore dello schermo, quindi fai clic su **Davvero?**.
1. (Facoltativo) Per verificare che la connessione al servizio sia stata stabilita correttamente, seleziona la casella di controllo accanto alla connessione, quindi fai clic su **Verifica** nella parte inferiore della schermata.
1. Per visualizzare gli scenari attivi che utilizzano questa connessione, selezionare la casella di controllo accanto alla connessione, quindi fare clic su **Recupera scenari attivi**. È quindi possibile fare clic su uno scenario nell&#39;elenco Scenari attivi per passare a tale scenario.

## Rinnovare una connessione

Workfront Fusion in genere ottiene i diritti di accesso a un determinato servizio per un periodo di tempo illimitato. Alcune applicazioni richiedono il rinnovo dell’autorizzazione di accesso dopo un determinato periodo di tempo. In questi casi, Workfront Fusion invia una notifica via e-mail poco prima della scadenza dei diritti di accesso.

Per rinnovare una connessione:

1. Per aprire l&#39;area Connessioni, fare clic su **Connessioni** ![Icona Connessioni](assets/connections-icon.png) nell&#39;area di navigazione a sinistra.
1. Individuare la connessione da rinnovare.
1. Nella riga della connessione, seleziona la casella di controllo accanto alla connessione, quindi fai clic su **Riautorizza** nella parte inferiore dello schermo.

## Risorse

* Per ulteriori informazioni sui metadati di connessione, ad esempio ambiente e tipo, vedere [Metadati di connessione](/help/workfront-fusion/references/connections/connection-metadata.md).
