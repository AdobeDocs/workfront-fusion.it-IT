---
title: HTTP > Creare un modulo di richiesta di autorizzazione di base
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: e544768e-7023-473f-8d51-631b04183743
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 0%

---

# [!UICONTROL HTTP] > [!UICONTROL Crea un modulo di richiesta di autorizzazione di base]

Questo modulo di Adobe Workfront Fusion consente di configurare una richiesta HTTP con l’autorizzazione HTTP di base e di inviarla a un server. La risposta HTTP ricevuta è quindi contenuta nel bundle di output.

>[!NOTE]
>
>Se ti connetti a un prodotto Adobe che al momento non dispone di un connettore dedicato, ti consigliamo di utilizzare il modulo Adobe Authenticator.
>
>Per ulteriori informazioni, vedere [Modulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta di autorizzazione di base] configurazione modulo

Quando configuri il modulo [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta di autorizzazione di base], Adobe Workfront Fusion visualizza i campi elencati di seguito. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo all&#39;altro in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Credentials]</td> 
   <td> <p>Selezionare la chiave che contiene le credenziali di autenticazione di base oppure fare clic su <strong>[!UICONTROL Add]</strong> per aggiungere le credenziali a una nuova chiave. </p> <p>Nota: puoi aggiungere più credenziali per passare facilmente da una connessione all’altra.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valuta tutti gli stati come errori (tranne 2xx e 3xx )] </td> 
   <td> <p>Utilizza questa opzione per configurare la gestione degli errori.</p> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Gestione degli errori</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Immetti l’URL a cui desideri inviare una richiesta, ad esempio un endpoint API, un sito web, ecc.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p> Immetti le coppie chiave-valore di query desiderate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di corpo]</p> </td> 
   <td> <p>Il corpo HTTP è costituito dai byte di dati trasmessi in un messaggio di transazione HTTP immediatamente dopo le intestazioni, se ve ne sono altre da utilizzare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Il tipo di corpo Raw è generalmente adatto per la maggior parte delle richieste HTTP body, anche in situazioni in cui la documentazione per gli sviluppatori non specifica i dati da inviare.</p> <p>Specificare un tipo di analisi dei dati nel campo [!UICONTROL Content type].</p> <p>Nonostante il tipo di contenuto selezionato, i dati vengono immessi in qualsiasi formato stabilito o richiesto dalla documentazione per gli sviluppatori.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Questo tipo di corpo è nei dati [!UICONTROL POST] che utilizzano <code>application/x-www-form-urlencoded</code>.</p> <p>Per <code>[!UICONTROL application/x-www-form-urlencoded]</code>, il corpo del messaggio HTTP inviato al server è essenzialmente una stringa di query. Le chiavi e i valori sono codificati in coppie chiave-valore separate da <code>&amp;</code> e con un <code>=</code> tra la chiave e il valore. </p> <p>Per i dati binari, utilizzare <code>[!UICONTROL multipart/form-data]</code>.</p> <p>Per ogni coppia chiave-valore che si desidera aggiungere, nel campo Campi fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore.</p>
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Esempio: </b></span></span> 
       <p>Esempio del formato di richiesta HTTP risultante:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] è una richiesta multipart HTTP utilizzata per inviare file e dati. Viene comunemente utilizzato per caricare file sul server.</p> <p>Aggiungi i campi da inviare nella richiesta. Ogni campo deve contenere una coppia chiave-valore.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Testo]</strong> </p> <p>Immetti la chiave e il valore da inviare nel corpo della richiesta.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Immetti la chiave e specifica il file di origine da inviare nel corpo della richiesta. Selezionare un file di origine da un modulo precedente o mapparne il nome e i dati.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Analizza risposta]</p> </td> 
   <td> <p>Abilita questa opzione per analizzare automaticamente le risposte e convertire le risposte JSON e XML in modo da non dover utilizzare i moduli [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] o [!UICONTROL XML] &gt; [!UICONTROL Parse XML].</p> <p>Prima di poter utilizzare contenuti JSON o XML analizzati, esegui il modulo una volta manualmente in modo che possa riconoscere il contenuto della risposta e consentirti di mapparlo nei moduli successivi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Specifica il timeout della richiesta in secondi (1-300). Il valore predefinito è 40 secondi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Condividi i cookie con altri moduli HTTP]</td> 
   <td> <p> Abilita questa opzione per condividere i cookie dal server con tutti i moduli HTTP nel tuo scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>Per aggiungere un certificato autofirmato:</p>
          <ol>
            <li value="1">
              <p>Fare clic su <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selezionare il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene il certificato o.</p>
            </li>
            <li value="4">
              <p>Immettere la password per il file.</p>
            </li>
            <li value="5">
              <p>Fare clic su <b>[!UICONTROL Salva]</b> per estrarre il file e tornare alla configurazione del modulo.</p>
            </li>
          </ol>
</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rifiuta le connessioni che utilizzano certificati non verificati (autofirmati)] </td> 
   <td> <p>Abilita questa opzione per rifiutare le connessioni che utilizzano certificati TLS non verificati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Abilita questa opzione per seguire i reindirizzamenti URL con risposte 3xx.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Segui tutti i reindirizzamenti] </td> 
   <td> <p>Abilita questa opzione per seguire i reindirizzamenti URL con tutti i codici di risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disattiva la serializzazione di più chiavi di stringa di query come matrici]</p> </td> 
   <td> <p>Per impostazione predefinita, Workfront Fusion gestisce più valori per la stessa chiave di parametro della stringa di query URL come array. Ad esempio, <code>www.test.com?foo=bar&amp;foo=baz</code> verrà convertito in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Attiva questa opzione per disabilitare questa funzione. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Richiedi contenuto compresso]</td> 
   <td> <p> Abilita questa opzione per richiedere una versione compressa del sito web.</p> <p>Aggiunge un'intestazione <code>[!UICONTROL Accept-Encoding]</code> per richiedere contenuto compresso.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Usa TLS reciproco]</td> 
   <td> <p>Abilita questa opzione per utilizzare Mutual TLS nella richiesta HTTP.</p> <p>Per ulteriori informazioni su Mutual TLS, vedere <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Utilizzare Mutual TLS nei moduli HTTP</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
