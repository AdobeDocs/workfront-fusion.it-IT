---
title: Configurare gli indirizzi IP per Fusion nell’elenco Consentiti della tua organizzazione
description: Fusion utilizza indirizzi IP e domini specifici per la comunicazione web. Per poter utilizzare Workfront nell’organizzazione, è necessario aggiungerle al inserisco nell'elenco Consentiti di dell’organizzazione.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
TQID: https://experienceleague.adobe.com/-ogVZgc8Jan8jmPV-l8PzajHzJrZ1np6dS-h7OAYY10
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 569
ht-degree: 8%

---

# Configurare gli indirizzi IP per Fusion nell’elenco Consentiti della tua organizzazione

Poiché Adobe Workfront Fusion comunica con la rete della tua organizzazione, il firewall di quest’ultima deve essere configurato in modo da consentire tale comunicazione. I firewall sono misure di sicurezza altamente efficaci che funzionano separando la rete di un&#39;organizzazione da Internet. Garantiscono che solo i dati e il traffico di rete selezionati possano essere spostati all’interno o all’esterno della rete dell’organizzazione. Il firewall consente o blocca i dati in base al sito che invia o riceve i dati. In qualità di amministratore di Fusion, devi assicurarti che i dati inviati a o da Fusion possano passare attraverso il firewall dell’organizzazione.

Ciò viene realizzato attraverso un inserisco nell&#39;elenco Consentiti di, che è essenzialmente un &quot;elenco&quot; di siti che sono &quot;autorizzati&quot; a inviare o ricevere dati tramite il firewall. I siti possono essere identificati in due modi:

* **Indirizzo IP**: una serie di numeri come 52.31.132.175
* **Dominio**: parte di un URL, ad esempio `thisdomain` in `www.thisdomain.com`

Fusion utilizza indirizzi IP e domini specifici per la comunicazione web. Per poter utilizzare Workfront nell’organizzazione, è necessario aggiungerle al inserisco nell&#39;elenco Consentiti di dell’organizzazione.

In genere, un amministratore di rete configura un inserisco nell&#39;elenco Consentiti di accesso a un sistema di rete. Rivolgiti all’amministratore di rete della tua organizzazione per assicurarti che il firewall consenta tali indirizzi IP. Se non si conosce il nome dell&#39;amministratore di rete, il reparto IT dell&#39;organizzazione può indirizzare l&#39;utente nella giusta direzione.

>[!IMPORTANT]
>
>In qualità di amministratore di Fusion, devi assicurarti che tali indirizzi IP e domini vengano aggiunti al inserisco nell&#39;elenco Consentiti di della tua organizzazione. Questo vale anche se non li aggiungi tu stesso. Fusion non può configurare il inserisco nell&#39;elenco Consentiti di della tua organizzazione.

È possibile aggiungere tutti gli indirizzi IP e i domini di Fusion al inserisco nell&#39;elenco Consentiti di oppure individuare il cluster di Fusion e aggiungere solo gli indirizzi IP e i domini per tale cluster.

## Aggiungere tutti gli indirizzi IP e i domini di Fusion

Aggiungi i seguenti indirizzi IP al tuo inserisco nell&#39;elenco Consentiti di:

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

Inoltre, se l’organizzazione utilizza il filtro di rete in uscita, aggiungi il seguente dominio al tuo elenco Consentiti di accesso a Workfront Fusion per consentire l’accesso al sistema.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Aggiungere indirizzi IP e domini Fusion solo per il cluster

### Identificare il datacenter

Gli indirizzi IP variano in base alla posizione in cui vengono memorizzati i dati.

Se accedi a Fusion tramite un URL, puoi esaminarlo per individuare il tuo datacenter.

| URL | Datacenter |
| --- | --- |
| `https://app.workfrontfusion.com` | Datacenter USA |
| `https://app-eu.workfrontfusion.com` | Datacenter UE |
| `https://app-az.workfrontfusion.com` | Cluster Azure |

Se si accede a Fusion tramite `experience.adobe.com`, è possibile controllare la scheda di rete nel browser per identificare il datacenter.

| URL | Datacenter |
| --- | --- |
| Chiamate a `https://fusion.adobe.com` | Datacenter USA |
| Chiamate a `https://eu.fusion.adobe.com` | Datacenter UE |
| Chiamate a `https://az.fusion.adobe.com` | Cluster Azure |

### Aggiungere indirizzi IP e domini per il centro dati

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Centro dati Adobe Workfront EU</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Centro dati Adobe Workfront USA</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion sul cluster Microsoft Azure</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Inoltre, se l’organizzazione utilizza il filtro di rete in uscita, aggiungi il seguente dominio al tuo elenco Consentiti di accesso a Workfront Fusion per consentire l’accesso al sistema. Questi vengono utilizzati per i webhook

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Centro dati Adobe Workfront EU</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Centro dati Adobe Workfront USA</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront Fusion sul cluster Microsoft Azure</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il filtro di rete in uscita non è comune. Rivolgersi all&#39;amministratore di rete per verificare se è necessario aggiornare il inserisco nell&#39;elenco Consentiti di accesso a un&#39;istanza di accesso a un&#39;istanza di rete.
