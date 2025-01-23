---
title: Modulo Adobe Authenticator
description: Con il modulo Adobe Authenticator, puoi connetterti a qualsiasi prodotto Adobe con un’API, utilizzando una singola connessione.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 1%

---

# Moduli Adobe Authenticator

Il modulo Adobe Authenticator ti consente di connettersi a qualsiasi API Adobe utilizzando una singola connessione. Questo consente di connettersi più facilmente a prodotti Adobe che non dispongono ancora di un connettore Fusion dedicato.

Il vantaggio rispetto ai moduli HTTP è che puoi creare una connessione, come in un’app dedicata.

Per visualizzare un elenco delle API Adobe disponibili, vedi [API Adobe](https://developer.adobe.com/apis). Puoi utilizzare solo le API a cui sei assegnato.

## Requisiti di accesso

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td>
      <td>
        <p>Nuovo: Qualsiasi</p><p>Oppure</p><p>Corrente: [!UICONTROL Pro] o versione successiva</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licenza</td>
      <td>
        <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza</td>
      <td>
   <p>Requisiti attuali della licenza Fusion: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisito licenza legacy per Fusion: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Prodotto</td>
      <td>
   <p>Nuovo piano Workfront: se disponi del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Piano Workfront corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td>
    </tr>
  </tbody>
</table>

## Prerequisiti

* Devi avere accesso al prodotto Adobe a cui desideri che il modulo si connetta.
* Devi avere accesso a Adobe Developer Console.
* In Adobe Developer Console è necessario disporre di un progetto che includa l’API a cui desideri che il modulo si connetta. È possibile:

   * Crea un nuovo progetto con l’API.

     Oppure
   * Aggiungi l’API a un progetto esistente.

  Per informazioni sulla creazione o l&#39;aggiunta di un&#39;API a un progetto in Adobe Developer Console, vedere [Creazione di un progetto](https://developer.adobe.com/dep/guides/dev-console/create-project/) nella documentazione di Adobe.

## Informazioni API di Adobe Authenticator

Il connettore Adobe Authenticator utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione

Una connessione Adobe Authenticator si connette a un singolo progetto sul Adobe Developer Console. Per utilizzare la stessa connessione per più API Adobe, aggiungi le API allo stesso progetto e crea una connessione a tale progetto.

Puoi creare connessioni separate a progetti separati, ma non puoi utilizzare una connessione per accedere a un’API che non si trova nel progetto specificato in tale connessione.

>[!IMPORTANT]
>
>Con il connettore Adobe Authenticator puoi scegliere se effettuare una connessione server-to-server OAuth o una connessione con account di servizio (JWT). Adobe ha dichiarato obsolete le credenziali JWT, che cesseranno di funzionare dopo il 1° gennaio 2025. **Si consiglia pertanto di creare connessioni OAuth.**
>
>Per ulteriori informazioni su questi tipi di connessioni, vedere [Autenticazione da server a server](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) nella documentazione di Adobe

Per creare una connessione:

1. In qualsiasi modulo di Adobe Authenticator, fai clic su **Aggiungi** accanto al campo Connessione.
1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Seleziona se desideri creare una connessione server-to-server OAuth o una connessione con un account di servizio (JWT).</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immetti l'ID client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Immetti il segreto client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Se hai selezionato una connessione OAuth, immetti gli ambiti necessari per questa connessione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Immetti l'ID account tecnico [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Se hai selezionato una connessione JWT, immetti l'ID organizzazione [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Se hai selezionato una connessione JWT, inserisci i meta-ambiti necessari per questa connessione. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Se hai selezionato una connessione JWT, immetti la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fare clic su <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selezionare il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Immettere la password per il file.</p>
            </li>
            <li value="5">
              <p>Fare clic su <b>[!UICONTROL Save]</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Base URLs]</td>
        <td>È necessario aggiungere gli URL di base consentiti dall'autenticatore. Quando utilizzi il modulo di chiamata Make a API personalizzata più avanti nello scenario, aggiungi un percorso relativo all’URL scelto. Immettendo gli URL qui, puoi controllare a cosa può connettersi il modulo di chiamata API Make a, aumentando così la sicurezza.<p>Per ogni URL di base da aggiungere all'autenticatore, fare clic su <b>Aggiungi elemento</b> e immettere l'URL di base.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Lasciare vuoto questo campo per utilizzare l'URL standard di autenticazione Adobe IMS di <code>https://ims-na1.adobelogin.com</code>. Se non utilizzi Adobe IMS per l’autenticazione, immetti l’URL da utilizzare per l’autenticazione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Specificare se ci si connette a un account di servizio o a un account personale.</td>
      </tr>
    </tbody>
    </table>

1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.

## Moduli

* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [Effettuare una chiamata API personalizzata (legacy)](#make-a-custom-api-call-legacy)

### Effettuare una chiamata API personalizzata

Questo modulo di azione ti consente di effettuare una chiamata a qualsiasi API Adobe. Supporta i file di grandi dimensioni, anziché i corpi di solo testo.

Questo modulo è stato reso disponibile il 14 novembre 2024. Qualsiasi chiamata Adobe Authenticator > Make a custom API configurata prima di questa data non gestisce file di grandi dimensioni e ora è considerata il modulo Make a custom API call (Legacy).

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Per istruzioni sulla creazione di una connessione al modulo Adobe Authenticator, vedere <a href="#create-a-connection" class="MCXref xref" >Creare una connessione</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Immetti l’URL di base del punto API a cui desideri connetterti.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Immetti il percorso relativo all’URL di base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> Seleziona il tipo di corpo per questa richiesta API:
   <ul>
   <li>application/x-www-form-urlencoded</li>
   <li>Grezzi</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Fields]  </td>
      <td>
        <p>Per ogni file da aggiungere alla richiesta APU, fare clic su <b>Aggiungi elemento</b> e immettere il testo del file (per i dati non elaborati) oppure immettere la chiave <code>uploadedFile</code> e mappare i dati del file.</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

### Effettuare una chiamata API personalizzata (legacy)

Questo modulo di azione ti consente di effettuare una chiamata a qualsiasi API Adobe.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Per istruzioni sulla creazione di una connessione al modulo Adobe Authenticator, vedere <a href="#create-a-connection" class="MCXref xref" >Creare una connessione</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Immetti l’URL di base del punto API a cui desideri connetterti.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Immetti il percorso relativo all’URL di base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere il numero massimo di risultati che il modulo deve restituire in un ciclo di esecuzione.</p>
      </td>
    </tr>
  </tbody>
</table>
