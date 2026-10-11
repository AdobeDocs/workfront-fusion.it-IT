---
title: HTTP > Creare un modulo di richiesta JWT
description: Il modulo di richiesta Adobe Workfront Fusion HTTP > Make a JWT invia una richiesta HTTP(S) a un URL e la autorizza con un token web JSON che Fusion firma automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/it'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 11%
---
# [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta JWT] modulo

Il modulo [!UICONTROL HTTP] > [!UICONTROL Effettua una richiesta JWT] di Adobe Workfront Fusion invia una richiesta HTTP(S) a un URL e la autorizza con un JSON Web Token (JWT) che il modulo firma per te in ogni chiamata. La risposta viene quindi elaborata nello stesso modo del modulo standard [!UICONTROL HTTP] > [!UICONTROL Effettua una richiesta].

Questo modulo si comporta come il modulo standard [!UICONTROL Crea una richiesta], con una differenza principale: firma automaticamente un JWT dalle attestazioni fornite e lo aggiunge alla richiesta, per impostazione predefinita come `Authorization: Bearer <token>`.

Utilizza questo modulo per richiamare qualsiasi API che preveda un JWT firmato per l’autenticazione, ad esempio i servizi che richiedono un token Bearer di breve durata firmato con un segreto condiviso (HMAC) o una chiave privata (RSA/ECDSA), senza creare il token in un passaggio separato.

Se l’API utilizza OAuth 2.0, l’autenticazione di base, una chiave API o un certificato client, utilizza invece il modulo HTTP dedicato corrispondente.

>[!NOTE]
>
>Se ti connetti a un prodotto Adobe che al momento non dispone di un connettore dedicato, ti consigliamo di utilizzare il modulo Adobe Authenticator.
>
>Per ulteriori informazioni, vedere [Modulo Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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
   <p>Basato su operazioni: disponibile per le organizzazioni con licenze basate su operazioni</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Creare una connessione JWT

Il modulo richiede una connessione JWT. La connessione memorizza il materiale per la firma in modo che il segreto o la chiave privata non debbano essere visualizzati nello scenario.

### Creare una connessione JWT in Fusion

1. Aggiungi il modulo [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta JWT] allo scenario.
1. Fai clic su **[!UICONTROL Aggiungi]** accanto al campo **[!UICONTROL Connessione]**.
1. Configura i campi di connessione:

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>Nome connessione</p></td>
      <td><p>Specifica un nome per la connessione.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>Algoritmo</p></td>
      <td>
       <p>Seleziona l’algoritmo di firma per la connessione.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Segreto</p></td>
      <td>
       <p>Immetti la chiave per la firma.</p>
       <ul>
        <li>Per gli algoritmi <code>HS*</code>, utilizzare la stringa segreta condivisa.</li>
        <li>Per gli algoritmi <code>RS*</code>, <code>PS*</code> e <code>ES*</code>, utilizza la chiave privata con codifica PEM.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

>[!IMPORTANT]
>
>Una connessione JWT firma con un solo algoritmo. Se lo scenario richiede più di un algoritmo di firma, crea una connessione separata per ciascun algoritmo. Corrisponde al comportamento dell’app JWT autonoma esistente.

## [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta JWT] modulo e relativi campi

Quando configuri il modulo [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta JWT], Adobe Workfront Fusion visualizza i campi elencati di seguito nello stesso ordine in cui compaiono nell&#39;interfaccia utente del modulo. Un titolo in grassetto in un modulo indica un campo obbligatorio. I campi contrassegnati come avanzati sono nascosti a meno che non si selezioni **[!UICONTROL Mostra impostazioni avanzate]**.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Connessione]</p></td>
   <td><p>Seleziona una connessione JWT esistente o creane una nuova.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>URL di destinazione della richiesta.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Metodo]</p></td>
   <td><p>Metodo HTTP come GET, POST, PUT, PATCH o DELETE.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Intestazioni]</p></td>
   <td><p>Intestazioni di richiesta personalizzate in formato chiave/valore.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Stringa di query]</p></td>
   <td><p>Parametri stringa di query in formato chiave/valore.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Tipo di corpo]</p></td>
   <td><p>Codifica del corpo della richiesta. Le opzioni disponibili sono Raw, application/x-www-form-urlencoded e multipart/form-data.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Analizza risposta]</p></td>
   <td><p>Quando è abilitato, Fusion analizza il corpo della risposta in base al tipo di contenuto della risposta.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>Payload JWT di [!UICONTROL (Attestazioni)]</p></td>
   <td><p>Coppie chiave/valore incluse come attestazioni nel payload JWT. Le attestazioni riservate <code>exp</code>, <code>iat</code> e <code>nbf</code> devono essere NumericDate, ovvero un numero di secondi dall'epoca Unix. I valori delle attestazioni mantengono il loro tipo JSON, pertanto i numeri rimangono numeri e i booleani rimangono booleani.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Timeout] (avanzato)</p></td>
   <td><p>Specifica il timeout della richiesta in secondi (1-300). Il valore predefinito è 40 secondi.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Conteggio tentativi] (avanzato)</p></td>
   <td><p>Specifica quante volte la richiesta deve ritentare se non riesce a causa di un errore ripetibile.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Codici di stato dei tentativi aggiuntivi] (avanzato)</p></td>
   <td><p>Specificare codici di stato HTTP aggiuntivi da considerare come ripetibili.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Condividere cookie con altri moduli HTTP] (modalità avanzata)</p></td>
   <td><p>Abilita questa opzione per condividere i cookie dal server con tutti i moduli HTTP nel tuo scenario.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Self-signed certificate] (avanzato)</p></td>
   <td><p>Carica il certificato se desideri utilizzare TLS con il certificato autofirmato.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Rifiuta connessioni che utilizzano certificati non verificati (autofirmati)] (avanzate)</p></td>
   <td><p>Abilita questa opzione per rifiutare le connessioni che utilizzano certificati TLS non verificati.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Follow redirect] (avanzato)</p></td>
   <td><p>Abilita questa opzione per seguire i reindirizzamenti URL con risposte 3xx.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Disattiva la serializzazione di più chiavi di stringa di query come matrici] (modalità avanzata)</p></td>
   <td><p>Per impostazione predefinita, Workfront Fusion gestisce più valori per la stessa chiave di parametro della stringa di query URL come array. Ad esempio, <code>www.test.com?foo=bar&amp;foo=baz</code> verrà convertito in <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Attiva questa opzione per disabilitare questa funzione.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Richiedi contenuto compresso] (avanzato)</p></td>
   <td><p>Abilita questa opzione per richiedere una versione compressa del sito web. Aggiunge un'intestazione <code>[!UICONTROL Accept-Encoding]</code> per richiedere contenuto compresso.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Use Mutual TLS] (avanzato)</p></td>
   <td><p>Abilita questa opzione per utilizzare Mutual TLS nella richiesta HTTP.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options] (avanzate)</p></td>
   <td><p>Per ogni opzione di firma che si desidera aggiungere alla richiesta, fare clic su <b>Aggiungi elemento</b> e immettere il nome e il valore del parametro.</p><p>Opzioni aggiuntive passate al firmatario JWT, ad esempio <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code> e <code>keyid</code>. I valori di durata come <code>expiresIn</code> vengono interpretati dalla libreria <code>jsonwebtoken</code>. Un numero normale viene considerato come millisecondi, pertanto utilizza una stringa di unità come <code>"1h"</code> o <code>"3600s"</code> per essere esplicito. L’algoritmo proviene dalla connessione e non può essere sovrascritto qui.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header Name] (avanzate)</p></td>
   <td><p>Inserisci o mappa il nome dell’intestazione della richiesta che riceve il JWT firmato. Impostazione predefinita: <code>Authorization</code>. Il nome dell'intestazione non deve contenere un punto (<code>.</code>), perché i nomi punteggiati sono rifiutati e non possono essere mascherati nei log delle richieste.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Token Type] (avanzato)</p></td>
   <td><p>Immettere o mappare lo schema di autenticazione inserito prima del token, ad esempio <code>Bearer</code>. Lascia vuoto questo campo per inviare il token non elaborato senza prefisso.</p></td>
  </tr>
 </tbody>
</table>

## Generazione del token

1. Il modulo raccoglie le attestazioni nel campo [!UICONTROL Payload JWT (attestazioni)].
1. Attestazioni riservate come <code>exp</code>, <code>iat</code>, e <code>nbf</code> vengono convertiti in valori NumericDate.
1. Il modulo applica le [!UICONTROL Opzioni firma] e firma il token utilizzando l&#39;algoritmo della connessione.
1. Il token firmato viene inserito nell&#39;intestazione della richiesta definita da [!UICONTROL Header Name].
1. Se [!UICONTROL Tipo di token] è impostato, il modulo aggiunge il prefisso prima del token. Ad esempio, <code>Bearer eyJ...</code>.
1. La richiesta viene inviata e la risposta viene elaborata allo stesso modo del modulo standard [!UICONTROL HTTP] > [!UICONTROL Crea una richiesta].

Il token firmato viene automaticamente mascherato nei registri di debug e di errore e non viene mai esposto.

## Esempio

### Connessione

- Algoritmo: `HS256`
- Segreto: `my-shared-secret`

### Impostazioni modulo

- URL: `https://api.example.com/v1/orders`
- Metodo: `GET`
- Payload JWT (attestazioni):
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- Opzioni di firma:
  - `expiresIn` = `1h`
- Nome intestazione: `Authorization`
- Tipo di token: `Bearer`

### Risultato

Il modulo invia la richiesta con un’intestazione simile a:

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## Domande frequenti/gotchas

### Perché il mio token è scaduto così rapidamente?

È probabile che tu abbia immesso un numero non specificato per `expiresIn`, ad esempio `3600`. La libreria `jsonwebtoken` interpreta i numeri semplici come millisecondi. Utilizzare invece una stringa di unità come `"1h"` o `"3600s"`.

### Quando viene creato il token?

Il modulo firma un nuovo JWT ogni volta che viene eseguito, non quando crei la connessione. La connessione archivia solo il materiale di firma e l&#39;algoritmo, pertanto le attestazioni come `iat` e `exp` riflettono il momento dell&#39;esecuzione del modulo.

Se la richiesta riprova all’interno della stessa esecuzione del modulo, Fusion riutilizza lo stesso token firmato per tali tentativi invece di firmare un nuovo token per ogni tentativo. Per questo motivo, un valore `expiresIn` molto breve può scadere prima che si verifichi un nuovo tentativo e causare un nuovo tentativo di inviare un token già scaduto. Per evitare questo problema, utilizzare una stringa di unità non crittografata come `"1h"` o `"3600s"` ed evitare durate dei token eccessivamente brevi.

### Posso cambiare l’algoritmo per richiesta?

No. L’algoritmo è corretto dalla connessione. Se hai bisogno di un algoritmo diverso, crea una connessione JWT diversa.

### Posso inviare il token in un’intestazione personalizzata?

Sì. Impostare il campo [!UICONTROL Nome intestazione] su un nome personalizzato, ma non può contenere un punto (`.`).

### Posso inviare il token non elaborato senza `Bearer`?

Sì. Lascia vuoto [!UICONTROL Tipo di token].

### Il token è visibile nei registri?

No. Il token firmato viene mascherato automaticamente nei registri di debug e di errore.


>[!NOTE]
>
>Nota tecnica: la firma utilizza la libreria `jsonwebtoken` e rispecchia il comportamento di firma dell’app JWT autonoma, pertanto gli stessi input producono lo stesso token dell’app JWT autonoma.
