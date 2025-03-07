---
title: Utilizzo di Mutual TLS nei moduli HTTP in Adobe Workfront Fusion
description: Puoi utilizzare Mutual TLS nei moduli HTTP di Adobe Workfront Fusion, consentendo a entrambi i lati della transazione di informazioni di verificare l’identità dell’altro.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 1fa1ef68267d971a2769400a031b333de2f684ce
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Usa TLS reciproco nei moduli HTTP in [!DNL Adobe Workfront Fusion]

## Panoramica di Mutual TLS

Quando invii dati tramite Internet, è importante assicurarsi che arrivino o provengano dalla posizione corretta e che solo il destinatario previsto possa leggerli. Con TLS abilitato, il client (computer che richiede informazioni) utilizza i certificati per verificare l&#39;identità del server (computer che fornisce informazioni). Questo rende sicure le connessioni HTTP.

Il TLS reciproco consente di confermare l’identità in entrambi i modi. Quando il server invia il proprio certificato per verificarne l’identità al client, richiede anche il certificato del client. In questo modo il server non invia informazioni a un sito o a un utente che potrebbero utilizzarle in modo improprio.

>[!INFO]
>
>**Esempio:**
>
>* **TLS**: quando una persona digita &quot;MyGreatBank.com&quot; in un browser, vuole essere sicura di andare nella Mia Grande Banca, non in un sito web che potrebbe abusare o vendere le proprie informazioni bancarie. Vogliono anche essere sicuri che le informazioni del loro conto bancario siano crittografate.
>
>   Quando il browser (il client) si connette a MyGreatBank.com (il server), TLS richiede un certificato da MyGreatBank.com per verificarne l’identità. Il certificato è fornito da un&#39;autorità di certificazione come [!DNL DigiCert] o [!DNL Thawte]. Poiché il browser considera attendibile l&#39;autorità di certificazione, consente la connessione.
>
>* **TLS reciproco**: MySoftware.com è un client software che richiede informazioni dall&#39;API MyGreatBank.com. MyGreatBank consente solo ai client attendibili di connettersi ai propri server. Quindi, oltre alla verifica TLS regolare dell’identità di MyGreatBank.com, il processo TLS/autorità di certificazione verifica anche la richiesta da MySoftware.com.

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
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Inserimento del certificato pubblico [!DNL Workfront Fusion]

Quando ci si connette a un servizio Web con una richiesta HTTP, il servizio Web richiede in genere un certificato pubblico [!DNL Workfront Fusion] per la verifica. Questo consente al servizio web di confrontare il certificato presentato nella richiesta HTTP con quello presente nel file, in modo da garantire che il certificato si trovi nel inserisco nell&#39;elenco Consentiti di del servizio web.

Per istruzioni sul caricamento del certificato pubblico [!DNL Adobe Workfront Fusion] in un servizio Web, vedere la documentazione del servizio Web.

>[!NOTE]
>
>In aggiunta al certificato, potrebbe essere necessario fornire altre informazioni. Per informazioni sulle esigenze di un servizio web, consulta la documentazione API del servizio web.

È possibile utilizzare i seguenti collegamenti per scaricare i certificati pubblici di Workfront Fusion:

### Certificati per il 23 aprile 2024 - 7 maggio 2025

>[!IMPORTANT]
>
>* Questi [!DNL Workfront Fusion] certificati pubblici scadono il 7 maggio 2025. Dopo la scadenza, dovrai caricare un nuovo certificato nel servizio web. Si consiglia di:
>
>   * Prendi nota della data di scadenza e imposta un promemoria per te stesso per caricare il certificato nel servizio web.
>   * Aggiungi ai segnalibri questa pagina per trovare facilmente i nuovi certificati.
>
>* Si tratta di certificati mTLS non jolly.

* [Scarica [!DNL Workfront Fusion] Certificato 2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem)
* [Scarica [!DNL Workfront Fusion] Certificato UE 2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem)

  Per l&#39;uso nell&#39;UE


## Abilitazione del TLS reciproco nei moduli HTTP [!DNL Workfront Fusion]

Tutti i [!DNL Workfront Fusion] [!UICONTROL moduli di richiesta HTTP] dispongono dell&#39;opzione per abilitare Mutual TLS.

Per abilitare Mutual TLS in un modulo di richiesta [!UICONTROL HTTP]:

1. Aggiungi un modulo di richiesta [!UICONTROL HTTP] allo scenario.
1. Inizia la configurazione del modulo.

   Per istruzioni sulla configurazione di un modulo di richiesta [!UICONTROL HTTP], vedere l&#39;articolo appropriato in [Connettori universali](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Abilita **[!UICONTROL Mostra impostazioni avanzate]** nella parte inferiore del modulo.
1. Abilita **[!UICONTROL Usa TLS reciproco]**.
