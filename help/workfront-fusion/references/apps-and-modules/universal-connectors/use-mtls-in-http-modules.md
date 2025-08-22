---
title: Utilizzo di Mutual TLS nei moduli HTTP in Adobe Workfront Fusion
description: Puoi utilizzare Mutual TLS nei moduli HTTP di Adobe Workfront Fusion, consentendo a entrambi i lati della transazione di informazioni di verificare l’identità dell’altro.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Utilizzo di Mutual TLS nei moduli HTTP in Adobe Workfront Fusion

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Fornire il certificato pubblico di Workfront Fusion

Quando ci si connette a un servizio Web con una richiesta HTTP, il servizio Web richiede in genere un certificato pubblico di Workfront Fusion per la verifica. Questo consente al servizio web di confrontare il certificato presentato nella richiesta HTTP con quello presente nel file, in modo da garantire che il certificato si trovi nel inserisco nell&#39;elenco Consentiti di del servizio web.

Per istruzioni sul caricamento del certificato pubblico di Adobe Workfront Fusion in un servizio Web, consulta la documentazione del servizio Web.

>[!NOTE]
>
>In aggiunta al certificato, potrebbe essere necessario fornire altre informazioni. Per informazioni sulle esigenze di un servizio web, consulta la documentazione API del servizio web.

È possibile utilizzare i collegamenti seguenti per scaricare i certificati pubblici di Workfront Fusion. Per individuare il proprio datacenter, vedere [Identificare il datacenter](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) nell&#39;articolo Configurare gli indirizzi IP per Fusion nel inserisco nell&#39;elenco Consentiti di dell&#39;organizzazione.

### Certificati per il 2025

>[!IMPORTANT]
>
>* Questi certificati pubblici di Workfront Fusion scadono il **4 aprile 2026** (Stati Uniti e UE) o il **25 novembre 2025** (Azure). Dopo la scadenza, dovrai caricare un nuovo certificato nel servizio web. Si consiglia di:
>
>   * Prendi nota della data di scadenza e imposta un promemoria per te stesso per caricare il certificato nel servizio web.
>   * Aggiungi ai segnalibri questa pagina per trovare facilmente i nuovi certificati.
>
>* Si tratta di certificati mTLS non jolly.

| Datacenter | Collegamento di download | Date valide |
|---|---|---|
| Datacenter USA | [Scarica il certificato Workfront Fusion US 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | Dal 3 marzo 2025 al 4 aprile 2026 |
| Datacenter UE | [Scarica Workfront Fusion EU Certificate 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | Dal 3 marzo 2025 al 4 aprile 2026 |
| Cluster Azure | [Scarica il certificato di Workfront Fusion Azure 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | dal 24 ottobre 2024 al 25 novembre 2025 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These Workfront Fusion public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download Workfront Fusion Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Abilitazione del TLS reciproco nei moduli HTTP di Workfront Fusion

Tutti i moduli di richiesta [!UICONTROL HTTP] di Workfront Fusion hanno l&#39;opzione di abilitare Mutual TLS.

Per abilitare Mutual TLS in un modulo di richiesta [!UICONTROL HTTP]:

1. Aggiungi un modulo di richiesta [!UICONTROL HTTP] allo scenario.
1. Inizia la configurazione del modulo.

   Per istruzioni sulla configurazione di un modulo di richiesta [!UICONTROL HTTP], vedere l&#39;articolo appropriato in [Connettori universali](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Abilita **[!UICONTROL Mostra impostazioni avanzate]** nella parte inferiore del modulo.
1. Abilita **[!UICONTROL Usa TLS reciproco]**.
