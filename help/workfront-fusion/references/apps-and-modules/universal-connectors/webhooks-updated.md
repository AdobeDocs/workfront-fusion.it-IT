---
title: Webhook
description: Un webhook è una chiamata HTTP attivata da un evento. Puoi utilizzare i webhook per attivare moduli di attivazione istantanea. Qualsiasi applicazione connessa a Internet e che consenta le richieste HTTP può inviare webhook ad Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 8e415378-e9c1-4b49-874b-6d38aba0c303
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 0%

---

# Webhook



<!--This information moved to the webhooks article in the create scenarios folders in the new repo-->

Un webhook è una chiamata HTTP attivata da un evento. Puoi utilizzare i webhook per attivare moduli di attivazione istantanea. Qualsiasi applicazione connessa a Internet e che consenta le richieste HTTP può inviare webhook ad Adobe Workfront Fusion.

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

## Utilizza un webhook in [!DNL Workfront Fusion]

>[!NOTE]
>
>Per chiamare un webhook di terze parti (un webhook in uscita) utilizza uno dei moduli HTTP. Per ulteriori informazioni, vedere [Moduli HTTP](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

Per utilizzare un webhook per connettere un&#39;app a [!DNL Workfront Fusion]:

1. Aggiungi il modulo trigger istantaneo **[!UICONTROL Webhooks]** >**[!UICONTROL Custom Webhook]** allo scenario.

1. Fare clic su **[!UICONTROL Add]** accanto al campo Webhook e immettere un nome per il nuovo webhook.
1. (Facoltativo) Fare clic su **[!UICONTROL Advanced Settings]**.
1. Nel campo **[!UICONTROL IP restrictions]** immettere un elenco separato da virgole degli indirizzi IP da cui il modulo può accettare i dati.
1. Fai clic su **[!UICONTROL Save]**

Dopo aver creato un webhook, viene visualizzato un URL univoco. Questo è l’indirizzo a cui il webhook invia i dati. Workfront Fusion convalida i dati inviati a questo indirizzo, quindi li trasmette per l’elaborazione nello scenario.

>[!NOTE]
>
>Una volta creato un webhook, puoi utilizzarlo in più scenari alla volta.

### Configurare la struttura dati del webhook {#configure-the-webhook-s-data-structure}

Per riconoscere la struttura dati del payload in ingresso, [!DNL Workfront Fusion] analizza i dati di esempio inviati all&#39;indirizzo visualizzato. Puoi fornire i dati di esempio apportando una modifica al servizio o all’app che farà sì che il servizio o l’app chiamino il webhook. Ad esempio, puoi rimuovere un file.

In alternativa, è possibile inviare i dati di esempio tramite il modulo [!UICONTROL HTTP] > [!UICONTROL Make a request]:

1. Crea un nuovo scenario con il modulo **[!UICONTROL HTTP]** > **[!UICONTROL Make a request]**

1. Configura il modulo con i seguenti valori:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"><p>[!UICONTROL URL] </p></td> 
      <td>Immetti l’URL del webhook. È possibile trovare questo URL nel modulo [!UICONTROL Webhooks] utilizzato per configurare il webhook.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method] </td> 
      <td><p>[!UICONTROL POST]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td><p> [!UICONTROL Raw]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td><p> JSON (application/json)</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Request content]</td> 
      <td><p>JSON non elaborato previsto nel webhook</p></td> 
     </tr> 
    </tbody> 
   </table>

   ![Configurazione nuovo scenario](/help/workfront-fusion/references/apps-and-modules/assets/new-scenario-set-up-like-this-350x446.png)

1. Aprire lo scenario con il modulo [!UICONTROL Webhooks] in una scheda o finestra del browser separata.
1. Nel modulo webhook fare clic su **[!UICONTROL Redetermine data structure]**.

   Non è necessario scollegare altri moduli dal modulo webhooks.

1. Passare allo scenario con il modulo [!UICONTROL HTTP] ed eseguirlo.
1. Torna allo scenario con il modulo Webhooks.

   Un messaggio &quot;[!UICONTROL Successfully determined]&quot; indica che il modulo ha determinato correttamente la struttura dati.

   ![Determinato correttamente](/help/workfront-fusion/references/apps-and-modules/assets/successfully-determined-350x175.png)

1. Fare clic su **[!UICONTROL OK]** per salvare la struttura dati.

   Gli elementi del webhook sono ora disponibili nel pannello di mappatura per l’utilizzo con i moduli successivi nello scenario.

## La coda del webhook

Se un webhook riceve dati e non esiste uno scenario attivo che preveda tali dati, questi vengono memorizzati nella coda. Una volta attivato lo scenario, elabora in sequenza tutti i bundle in attesa nella coda.

>[!IMPORTANT]
>
>Le code dei webhook sono condivise tra scenari che utilizzano lo stesso webhook. Se uno degli scenari è disattivato, tutti i dati in arrivo vengono mantenuti nella coda.

## Formati di dati in arrivo supportati

[!DNL Workfront Fusion] supporta 3 formati di dati in ingresso: [!UICONTROL Query String], [!UICONTROL Form Data] e [!UICONTROL JSON].

[!DNL Workfront Fusion] convalida tutti i dati in arrivo in base alla struttura dati selezionata. Quindi, a seconda delle impostazioni dello scenario, i dati vengono memorizzati nella coda per l’elaborazione o vengono elaborati immediatamente.

Se una parte qualsiasi dei dati non supera la convalida, [!DNL Workfront Fusion] restituisce un codice di stato HTTP 400 e specifica, nel corpo della risposta HTTP, il motivo per cui i dati in arrivo non hanno superato i controlli di convalida. Se la convalida dei dati in arrivo viene eseguita correttamente, Workfront Fusion restituirà lo stato &quot;[!UICONTROL 200 Accepted]&quot;.

* [[!UICONTROL Query String]](#query-string)
* [[!UICONTROL Form Data]](#form-data)
* [[!UICONTROL JSON]](#json)

### [!UICONTROL Query String]

```
GET https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>?name=<yourname>&job=automate
```

### [!UICONTROL Form Data]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/x-www-form-urlencoded

name=<yourname>&job=automate
```

#### Dati modulo multipart

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>


Content-Type: multipart/form-data; boundary=---generatedboundary

---generatedboundary

Content-Disposition: form-data; name="file"; filename="file.txt"


Content-Type: text/plain


Content of file.txt


---generatedboundary

Content-Disposition: form-data; name="name"

Workfront Fusion

---generatedboundary
```

Per ricevere i file codificati con `multipart/form-data`, è necessario configurare una struttura di dati con un campo di tipo `collection` contenente i campi nidificati `name`, `mime` e `data`. Il campo `name` è di tipo `text` e contiene il nome del file caricato. `mime` è un tipo `text` e contiene un file in formato MIME. Il campo `data` è di tipo `buffer` e contiene dati binari per il file da trasferire.

Per ulteriori informazioni sul formato MIME, vedere [Moduli MIME](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md).

### [!UICONTROL JSON]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/json

{"name": "Workfront Fusion", "job": "automate"}
```

>[!TIP]
>
>Se desideri accedere al JSON originale, abilita il pass-through JSON durante la configurazione del webhook.
>
>1. Fare clic su **[!UICONTROL Add]** per aggiungere un nuovo webhook.
>1. Fare clic su **[!UICONTROL Show advanced settings]**.
>1. Fare clic su **[!UICONTROL JSON pass-through]**.
>

## Intestazioni webhook

Per accedere alle intestazioni del webhook, abilita Ottieni intestazioni di richiesta durante la configurazione del webhook.

1. Fare clic su **[!UICONTROL Add]** per aggiungere un nuovo webhook.
1. Fare clic su **[!UICONTROL Show advanced settings]**.
1. Fare clic su **[!UICONTROL Get request headers]**.

È possibile estrarre un particolare valore di intestazione con la combinazione di `map()` e `get()` funzioni.

>[!INFO]
>
>**Esempio:**
>
>L&#39;esempio seguente mostra una formula che estrae il valore dell&#39;intestazione `authorization` dall&#39;array `Headers[]`. La formula viene utilizzata in un filtro che confronta il valore estratto con il testo specificato per trasmettere solo i webhook in caso di corrispondenza.
>
>![Configura un filtro](/help/workfront-fusion/references/apps-and-modules/assets/set-up-a-filter-350x169.png)
>
>Per ulteriori informazioni su come ottenere l&#39;elemento di un array con una chiave specificata, vedere [Mappare l&#39;elemento di un array con una chiave specificata](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md#map-an-arrays-element-with-a-given-key) nell&#39;articolo Mappare un array.

## Risposta ai webhook

La risposta predefinita a una chiamata al webhook è il testo &quot;Accepted&quot; (Accettato). La risposta viene restituita all’app che ha chiamato il webhook durante l’esecuzione del modulo Webhook personalizzato.

* [Verifica la risposta a un webhook](#test-the-response-to-a-webhook)
* [Esempio di risposta HTML](#html-response-example)
* [Esempio di reindirizzamento](#redirect-example)

### Verificare la risposta a un webhook

1. Includi il modulo **[!UICONTROL Custom Webhook]** nello scenario.
1. Aggiungi un nuovo webhook al modulo.
1. Copia l’URL del webhook negli Appunti.
1. Esegui lo scenario.

   L&#39;icona del fulmine nel modulo [!UICONTROL Custom Webhook] diventa un punto in rotazione. Questo mostra che il modulo è ora in attesa della chiamata del webhook.

1. Aprire una nuova finestra del browser, incollare l&#39;URL copiato nella barra degli indirizzi e premere **[!UICONTROL Enter]**.

   Il modulo [!UICONTROL Custom Webhook] è attivato e il browser visualizzerà una nuova pagina.

Se desideri personalizzare la risposta del webhook, utilizza il modulo Risposta del webhook.

La configurazione del modulo contiene due campi: [!UICONTROL Status] e [!UICONTROL Body].

* Il campo [!UICONTROL Status] contiene codici di stato di risposta HTTP come 2xx per l&#39;esito positivo (ad esempio, `200` per OK), 3xx per il reindirizzamento (ad esempio, `307` per il reindirizzamento temporaneo), 4xx per gli errori del client (ad esempio, `400` per la richiesta non valida) e così via.

* Il campo [!UICONTROL Body] contiene qualsiasi elemento che verrà accettato dalla chiamata del webhook. Può essere testo semplice, HTML, XML, JSON e così via.

  >[!TIP]
  >
  >È consigliabile impostare l&#39;intestazione `Content-Type` sul tipo MIME corrispondente: `text/plain` per il testo normale, `text/html` per HTML, `application/json` per JSON, `application/xml` per XML e così via. Per ulteriori informazioni sui tipi MIME, vedere [Moduli MIME](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md).

Il timeout per l’invio di una risposta è di 40 secondi. Se la risposta non è disponibile entro tale periodo, Workfront Fusion restituisce lo stato &quot;200 Accepted&quot; (Accettato).

### Esempio di risposta HTML

>[!INFO]
>
>**Esempio:**
>
>Configurare il modulo [!UICONTROL Webhook Response] come segue:
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>Codice di stato HTTP 2xx, ad esempio 200</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Body] </td> 
&gt;   <td> <p>Codice HTML</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>Chiave</strong>: tipo di contenuto</li> 
&gt;     <li><strong>Valore</strong>: text/html</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![Intestazioni personalizzate](/help/workfront-fusion/references/apps-and-modules/assets/custom-headers-350x235.png)
>
>In questo modo viene generata una risposta di HTML che viene visualizzata in un browser web:
>
>![Risposta HEML](/help/workfront-fusion/references/apps-and-modules/assets/html-response-350x70.png)

### Esempio di reindirizzamento

>[!INFO]
>
>**Esempio:** Configurare il modulo [!UICONTROL Webhook Response] come segue:
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>Codice di stato HTTP del reindirizzamento 3xx, ad esempio 303</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>[!UICONTROL Key]</strong>: Posizione</li> 
&gt;     <li><strong>[!UICONTROL Value]</strong>: URL a cui desideri reindirizzare.</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![Risposta webhook](/help/workfront-fusion/references/apps-and-modules/assets/webhook-response-350x279.png)

## Disattivazione webhook

I webhook vengono disattivati automaticamente se si applica una delle seguenti condizioni:

* Il webhook non è stato connesso ad alcuno scenario per più di 5 giorni
* Il webhook viene utilizzato solo in scenari inattivi, che sono stati inattivi per più di 30 giorni.

I webhook disattivati vengono eliminati e annullati automaticamente se non sono connessi ad alcun scenario e se sono in stato disattivato da oltre 30 giorni.


## Risoluzione dei problemi

### Elementi mancanti nel pannello di mappatura

Se nel pannello di mappatura mancano alcuni elementi nella configurazione dei moduli successivi al modulo [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook], fai clic sul modulo **[!UICONTROL Webhooks]>[!UICONTROL Custom Webhook]** per aprirne la configurazione e fai clic su **[!UICONTROL Re-determine data structure]**:

![Rideterminazione struttura dati](/help/workfront-fusion/references/apps-and-modules/assets/redetermine-data-structure-btn-350x195.png)

Segui quindi i passaggi descritti nella sezione [Configurare la struttura dati del webhook](#configure-the-webhook-s-data-structure) in questo articolo.
