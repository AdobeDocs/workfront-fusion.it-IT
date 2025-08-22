---
title: HTTP > Altri moduli
description: L'app HTTP di Adobe Workfront Fusion fornisce vari moduli per la comunicazione basata sul protocollo HTTP (Hypertext Transfer Protocol). HTTP è la base della comunicazione dei dati per il World Wide Web. Puoi utilizzare i moduli per scaricare pagine web e file, chiamare webhook, endpoint API e così via.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# HTTP > Altri moduli

L&#39;app Adobe Workfront Fusion [!UICONTROL HTTP] fornisce vari moduli per la comunicazione basata sul protocollo HTTP (Hypertext Transfer Protocol). HTTP è la base della comunicazione dei dati per il World Wide Web. Puoi utilizzare i moduli per scaricare pagine web e file, chiamare webhook, endpoint API e così via.

La scelta giusta del modulo dipende dal meccanismo di autenticazione/autorizzazione della risorsa a cui desideri accedere. Di seguito sono riportati alcuni esempi di moduli

* **Fai una richiesta**: destinato principalmente a risorse che non utilizzano alcun tipo di autenticazione o autorizzazione
* **Crea una richiesta di autenticazione di base**: per le risorse che utilizzano [!DNL HTTP] autenticazione di base (BA)
* **Richiesta OAuth 2.0**: per risorse che utilizzano il protocollo di autorizzazione OAuth 2.0
* **Crea una richiesta di autenticazione certificato client**: per le risorse che utilizzano un protocollo di autorizzazione che richiede un certificato lato client
* **Richiesta di autorizzazione di una chiave API**: per le risorse che utilizzano chiavi API per l&#39;autorizzazione

>[!NOTE]
>
>Se ti connetti a un prodotto Adobe che al momento non dispone di un connettore dedicato, ti consigliamo di utilizzare il modulo Adobe Authenticator.
>
>Per ulteriori informazioni, vedere [Modulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## Moduli di richiesta

Per istruzioni specifiche sul modulo di richiesta, consulta i seguenti articoli:

* [[!UICONTROL HTTP] > [!UICONTROL Richiedi un modulo]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Crea un modulo di richiesta di autorizzazione di base]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Crea una richiesta OAuth 2.0]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Crea una richiesta di autorizzazione del certificato client] modulo](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Crea una richiesta di autorizzazione della chiave API]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Altri moduli di azione

* [[!UICONTROL Ottieni un file]](#get-a-file)
* [[!UICONTROL Risolvere un URL di destinazione]](#resolve-a-target-url)

### [!UICONTROL Ottieni un file]

Questo modulo di azione scarica un file dall’URL specificato. Una volta scaricato il file, puoi elaborarlo ulteriormente (mappare i dati del file) utilizzando altri moduli nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valuta tutti gli stati come errori (tranne 2xx e 3xx )] </td> 
   <td> <p>Utilizza questa opzione per configurare la gestione degli errori.</p> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Gestione degli errori in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Inserisci o mappa l’URL del file da scaricare. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Condividi i cookie con altri moduli HTTP] </td> 
   <td> <p>Abilita questa opzione se desideri che i cookie di questo sito siano disponibili per altri moduli. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Risolvere un URL di destinazione]

Questo modulo di azione risolve una catena di reindirizzamenti HTTP e restituisce un URL di destinazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Immettere o mappare l'URL da risolvere, ad esempio un URL [!DNL bit.ly].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>Specificare se si desidera utilizzare il metodo [!UICONTROL HEAD] o il metodo [!UICONTROL GET].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Moduli iteratori

### [!UICONTROL Recupera intestazioni]

Questo modulo restituisce ogni intestazione (nome e valore) dal modulo HTTP specificato in un bundle separato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo Source]</td> 
   <td> <p> Seleziona il modulo da cui desideri recuperare le intestazioni.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Generazione di token web JSON (JWT)

È possibile generare un token JWT con l’aiuto di funzioni integrate:

Intestazione:

![Intestazione JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Codice per copia&amp;incolla:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload:

![Payload JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Codice per copia&amp;incolla:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![Token JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Codice per copia&amp;incolla:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
