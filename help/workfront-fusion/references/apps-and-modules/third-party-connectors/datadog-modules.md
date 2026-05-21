---
title: Moduli Datadog
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Datadog, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
TQID: https://experienceleague.adobe.com/DM-90ye4UKybFarHch-ubk4vOt4Ofh69EBXTmAO-Hmw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 959
ht-degree: 47%

---

# Moduli [!DNL Datadog]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Datadog], nonché collegarli a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Prerequisiti

Per utilizzare i moduli [!DNL Datadog], è necessario disporre di un account [!DNL Datadog].

## Informazioni API Datadog

Il connettore Datadog utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL Datadog] a Workfront Fusion {#connect-datadog-to-workfront-fusion}

### Recuperare la chiave API e la chiave dell’applicazione {#retrieve-your-api-key-and-application-key}

Per collegare l&#39;account [!DNL Datadog] a Workfront Fusion è necessario recuperare una chiave API e una chiave dell&#39;applicazione dall&#39;account [!DNL Datadog].

1. Accedi al tuo account [!DNL Datadog].
1. Nel pannello di navigazione a sinistra, fai clic su **[!UICONTROL Integrazioni]**, quindi su **[!UICONTROL API]**.
1. Nella schermata principale, fai clic su **[!UICONTROL Chiavi API]**.
1. Passa il puntatore del mouse sulla barra viola per visualizzare la chiave API.
1. Copia la chiave API in un percorso sicuro.
1. Nella schermata principale, fai clic su **[!UICONTROL Chiavi applicazione]**.
1. Passa il cursore del mouse sulla barra viola per visualizzare il tasto dell’applicazione.
1. Copiare la chiave dell&#39;applicazione in un percorso sicuro.

### Crea una connessione a [!DNL Datadog] in Workfront Fusion

Puoi creare una connessione al tuo account [!DNL Datadog] direttamente da un modulo [!UICONTROL Datadog].

1. In qualsiasi modulo [!UICONTROL Datadog], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Compila i campi del modulo come segue:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome connessione]</td> 
      <td> <p> Specifica un nome per la connessione.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Seleziona se la connessione è per un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Seleziona il dominio a cui desideri connetterti (USA o UE).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Posizione chiave API  </td> 
      <td> <p>Seleziona se includere la chiave API nell’intestazione o nella stringa di query.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Immetti la tua chiave API [!DNL Datadog]. </p> <p>Per istruzioni sul recupero della chiave API, consulta <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperare la chiave API e la chiave dell'applicazione</a> in questo articolo.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## Moduli [!DNL Datadog] e relativi campi

Quando configuri i moduli [!DNL Datadog], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Datadog], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)
* [[!UICONTROL Pubblica punti serie temporali]](#post-timeseries-points)

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Datadog] a Workfront Fusion, consulta <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Datadog] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usa dominio dedicato]</td> 
   <td>Alcuni degli endpoint API di Datadog che prevedono molto traffico in arrivo sono in esecuzione sui loro domini dedicati. Seleziona questa casella per utilizzare il dominio dedicato per la chiamata API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci un percorso relativo a <code>https://api.datadoghq.com/api/</code>. Esempio:<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio:** La seguente chiamata API restituisce tutti i dashboard nel tuo account [!DNL Datadog]:

URL: `/v1/dashboard`

Metodo: `GET`

![Esempio di chiamata API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

Il risultato si trova nell’Output del modulo in Bundle > Corpo > dashboard.

Nel nostro esempio, sono state restituite 3 dashboard:

![Risposta API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL Pubblica punti serie temporali]

Il modulo ti consente di pubblicare dati di serie temporali che possono essere tracciati nei dashboard di [!DNL Datadog].

Il limite per i payload compressi è di 3,2 megabyte (3200000) e 62 megabyte (62914560) per i payload decompressi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’account [!DNL Datadog] a Workfront Fusion, consulta <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Datadog] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo]</td> 
   <td> Seleziona il tipo di metrica da utilizzare. 
   <ul>
   <li>Indicatori</li>
   <li>Tasso</li>
   <li>Conteggio</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> Se il tipo di metrica è tasso o conteggio, definisci l’intervallo corrispondente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Punti]</td> 
   <td><p>Aggiungere punti relativi a una metrica.</p> <p>Questo è un array JSON di punti. Ogni punto ha il formato: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Nota:  <p>Il timestamp deve essere in secondi.</p> <p>Il timestamp deve essere corrente. Corrente è definita come non più di 10 minuti nel futuro o più di 1 ora nel passato.</p> <p> Il formato del valore numerico deve essere un valore mobile.</p> </p> <p>Questo campo deve contenere almeno 1 elemento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Immetti il nome dell’host che ha prodotto la metrica. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag]</td> 
   <td> Per ogni tag che desideri aggiungere alla metrica, fai clic su <b>Aggiungi elemento</b> e immetti il valore del tag.</td> 
  </tr> 
 </tbody> 
</table>
