---
title: HTTP &gt; altri moduli
description: L'app HTTP  [!DNL Adobe Workfront Fusion] fornisce vari moduli per le comunicazioni basate sul protocollo HTTP (Hypertext Transfer Protocol). HTTP è la base della comunicazione dei dati per il World Wide Web. Puoi utilizzare i moduli per scaricare pagine web e file, chiamare webhook, endpoint API e così via.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# HTTP > Altri moduli

>[!NOTE]
>
>[!UICONTROL Adobe Workfront Fusion] richiede una licenza [!UICONTROL Adobe Workfront Fusion] oltre a una licenza [!UICONTROL Adobe Workfront].

L&#39;app [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] fornisce vari moduli per le comunicazioni basate sul protocollo HTTP (Hypertext Transfer Protocol). HTTP è la base della comunicazione dei dati per il World Wide Web. Puoi utilizzare i moduli per scaricare pagine web e file, chiamare webhook, endpoint API e così via.

La scelta giusta del modulo dipende dal meccanismo di autenticazione/autorizzazione della risorsa a cui desideri accedere. Di seguito sono riportati alcuni esempi di moduli

* Richiesta:modulo universale destinato principalmente a risorse che non utilizzano alcun tipo di autenticazione/autorizzazione
* Effettuare una richiesta di autenticazione di base:per le risorse che utilizzano l&#39;autenticazione di base (BA) di [!DNL HTTP]
* Effettuare una richiesta OAuth 2.0: per risorse che utilizzano il protocollo di autorizzazione OAuth 2.0
* Effettuare una richiesta di autenticazione certificato client: per le risorse che utilizzano un protocollo di autorizzazione che richiede un certificato lato client.
* Effettuare una richiesta di autorizzazione della chiave API: per le risorse che utilizzano le chiavi API per l’autorizzazione.

>[!NOTE]
>
>Se ti connetti a un prodotto Adobe che al momento non dispone di un connettore dedicato, ti consigliamo di utilizzare il modulo Adobe Authenticator.
>
>Per ulteriori informazioni, vedere [Modulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Moduli di richiesta

Per istruzioni specifiche sul modulo di richiesta, consulta i seguenti articoli:

* [Modulo [!UICONTROL HTTP] > [!UICONTROL Make a request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [Modulo [!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [Modulo [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [Modulo [!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Altri moduli di azione

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

Questo modulo di azione scarica un file dall’URL specificato. Una volta scaricato il file, puoi elaborarlo ulteriormente (mappare i dati del file) utilizzando altri moduli nello scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Inserisci o mappa l’URL del file da scaricare. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

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

### [!UICONTROL Retrieve headers]

Questo modulo restituisce ogni intestazione (nome e valore) dal modulo HTTP specificato in un bundle separato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Seleziona il modulo da cui desideri recuperare le intestazioni.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Generazione di token web JSON (JWT)

È possibile generare un token JWT con l’aiuto di funzioni integrate:

Intestazione

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
