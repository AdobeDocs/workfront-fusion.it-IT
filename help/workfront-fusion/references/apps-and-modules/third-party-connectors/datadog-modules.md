---
title: Moduli Datadog
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Datadog, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 7edfe4a7b19597ea6e56bb2ca3969d742dbaf999
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 1%

---

# [!DNL Datadog] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Datadog] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Connetti [!DNL Datadog] a [!DNL Workfront Fusion] {#connect-datadog-to-workfront-fusion}

### Recuperare la chiave API e la chiave dell’applicazione {#retrieve-your-api-key-and-application-key}

Per connettere l&#39;account [!DNL Datadog] a [!DNL Workfront Fusion] è necessario recuperare una chiave API e una chiave applicazione dall&#39;account [!DNL Datadog].

1. Accedi al tuo account [!DNL Datadog].
1. Nel pannello di navigazione a sinistra, fai clic su **[!UICONTROL Integrazioni]**, quindi su **[!UICONTROL API]**.
1. Nella schermata principale, fai clic su **[!UICONTROL Chiavi API]**.
1. Passa il puntatore del mouse sulla barra viola per visualizzare la chiave API.
1. Copia la chiave API in un percorso sicuro.
1. Nella schermata principale, fai clic su **[!UICONTROL Chiavi applicazione]**.
1. Passa il cursore del mouse sulla barra viola per visualizzare il tasto dell’applicazione.
1. Copiare la chiave dell&#39;applicazione in un percorso sicuro.

### Crea una connessione a [!DNL Datadog] in [!DNL Workfront Fusion]

Puoi creare una connessione al tuo account [!DNL Datadog] direttamente da un modulo [!UICONTROL Datadog].

1. In qualsiasi modulo [!UICONTROL Datadog], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Compila i campi del modulo come segue:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Tipo di connessione [!UICONTROL]</td> 
      <td> <p> Selezionare l'opzione [!UICONTROL [!DNL Datadog] Application] per accedere completamente all'API [!DNL Datadog].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome connessione]</td> 
      <td> <p> Immettere un nome per la connessione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Seleziona il dominio a cui desideri connetterti (USA o UE).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Immetti la tua chiave API [!DNL Datadog]. </p> <p>Per istruzioni sul recupero della chiave API, consulta <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperare la chiave API e la chiave dell'applicazione</a> in questo articolo.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chiave Applicazione]</td> 
      <td> <p> Immetti la chiave dell'applicazione [!DNL Datadog]. </p> <p>Per istruzioni sul recupero della chiave dell'applicazione, vedere <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Recuperare la chiave dell'API e la chiave dell'applicazione</a> in questo articolo.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## [!DNL Datadog] moduli e relativi campi

Quando configuri [!DNL Datadog] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Datadog], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Datadog] a [!DNL Workfront Fusion], vedere <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Datadog] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usa dominio dedicato]</td> 
   <td>Alcuni degli endpoint API di Datadog che prevedono molto traffico in arrivo sono in esecuzione sui loro domini dedicati. Seleziona questa casella per utilizzare il dominio dedicato per la chiamata API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://api.datadoghq.com/api/</code>. Esempio:<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Datadog] a [!DNL Workfront Fusion], vedere <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Datadog] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> Seleziona il tipo di metrica da utilizzare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Series]</td> 
   <td> <p>Aggiungere serie temporali da inviare a [!DNL Datadog].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Metrica]</strong> </p> <p>Immetti il nome della serie temporale.</p> </li> 
     <li> <p><strong>[!UICONTROL Type]</strong> </p> <p>Seleziona il tipo di metrica.</p> </li> 
     <li> <p><strong>[!UICONTROL Interval]</strong> </p> <p> Se il tipo di metrica è tasso o conteggio, definisci l’intervallo corrispondente.</p> </li> 
     <li> <p><strong>[!UICONTROL Punti]</strong> </p> <p>Aggiungere punti relativi a una metrica.</p> <p>Questo è un array JSON di punti. Ogni punto ha il formato: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Nota:  <p>Il timestamp deve essere in secondi.</p> <p>Il timestamp deve essere corrente. Corrente è definita come non più di 10 minuti nel futuro o più di 1 ora nel passato.</p> <p> Il formato del valore numerico deve essere un valore mobile.</p> </p> <p>Questo campo deve contenere almeno 1 elemento.</p> </li> 
     <li> <p><strong>[!UICONTROL Host]</strong> </p> <p>Immetti il nome dell’host che ha prodotto la metrica.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
