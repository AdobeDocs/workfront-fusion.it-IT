---
title: Moduli software Jira
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano il software  [!DNL Jira] e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2208'
ht-degree: 1%

---

# [!DNL Jira Software] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Jira Software] e collegarlo a più applicazioni e servizi di terze parti.

Queste istruzioni sono valide per i moduli Jira Cloud e Jira Server.

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

Per utilizzare i moduli [!DNL Jira] è necessario disporre di un account [!DNL Jira].

## Informazioni API Jira

Il connettore Jira utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Server Jira</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1,0 </td> 
   <td> 1,0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>1.7.29</td> 
   <td>1.0.19</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Jira Software] a [!DNL Workfront Fusion]

Il metodo di connessione si basa sull&#39;utilizzo di [!DNL Jira Cloud] o [!DNL Jira Server].

* [Connetti [!DNL Jira Cloud] a Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Connetti [!DNL Jira Server] a [!DNL Workfront Fusion]](#connect-jira-server-to-workfront-fusion)

### Connetti [!DNL Jira Cloud] a [!DNL Workfront Fusion]

Connetti [!DNL Jira Cloud] a [!DNL Workfront Fusion]

Per connettere [!DNL Jira Software] a [!DNL Workfront Fusion], è necessario creare un token API e inserirlo insieme all&#39;URL del servizio e al nome utente nel campo [!UICONTROL Crea una connessione] in [!DNL Workfront Fusion].

#### Crea un token API in [!DNL Jira]

1. Crea un token API in Jira.

   Per istruzioni, consigliamo di cercare &quot;Crea un token API&quot; nella documentazione di Jira.
1. Dopo aver creato il token, copialo in un percorso sicuro.

   >[!IMPORTANT]
   >
   >Impossibile visualizzare di nuovo il token dopo aver chiuso questa finestra di dialogo.
1. Memorizza il token generato in un luogo sicuro.
1. Continua con [Configura il token API [!DNL Jira] in [!DNL Workfront Fusion]](#configure-the-jira-api-token-in-workfront-fusion).

#### Configura il token API [!DNL Jira] in [!DNL Workfront Fusion]

1. In qualsiasi modulo di [!DNL Jira Cloud] in [!DNL Workfront Fusion], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL connessione].
1. Specifica le seguenti informazioni:

   * **Ambiente**
   * **Tipo**
   * **[!UICONTROL URL servizio]:** Questo è l&#39;URL di base utilizzato per accedere al tuo account Jira. Esempio: `yourorganization.atlassian.net`
   * **[!UICONTROL Nome utente]**
   * **[!UICONTROL Token API]:** Questo è il token API creato nella sezione [Creare un token API in [!DNL Jira]](#create-an-api-token-in-jira) di questo articolo.

1. Fai clic su [!UICONTROL Continua] per creare la connessione e tornare al modulo.

### Connetti [!DNL Jira Server] a [!DNL Workfront Fusion]

Per autorizzare una connessione tra [!DNL Workfront Fusion] e [!DNL Jira Server], sono necessari la chiave consumer, la chiave privata e l&#39;URL del servizio. Potrebbe essere necessario contattare l&#39;amministratore [!DNL Jira] per ottenere queste informazioni.

* [Genera chiavi pubbliche e private per la connessione  [!DNL Jira] ](#generate-public-and-private-keys-for-your-jira-connection)
* [Configura l&#39;app client come consumer in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Crea una connessione al server  [!DNL Jira] o al centro dati Jira in [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Genera chiavi pubbliche e private per la connessione [!DNL Jira]

Per acquisire una chiave privata per la connessione [!DNL Workfront Fusion Jira], è necessario generare chiavi pubbliche e private. Questa operazione viene eseguita tramite il terminale del computer. È possibile individuare il terminale ricercando il terminale nel menu Start o nella barra di ricerca del computer (non nella barra di ricerca del browser).

1. Nel terminale, eseguire i seguenti `openssl` comandi.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Questo comando genera una chiave privata a 1024 bit.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Questo comando crea un certificato X509.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Questo comando estrae la chiave privata (formato PKCS8) nel file `jira_privatekey.pcks8`.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     Questo comando estrae la chiave pubblica dal certificato al file `jira_publickey.pem`.

     >[!NOTE]
     >
     >Se si utilizza Windows, potrebbe essere necessario salvare manualmente la chiave pubblica nel file `jira_publickey.pem`:
     >
     >1. Nel terminale, eseguire il comando seguente:
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. Copia l&#39;output del terminale, inclusi `-------BEGIN PUBLIC KEY--------` e `-------END PUBLIC KEY--------`.
     >   
     >1. Incollare l&#39;output del terminale in un file denominato `jira_publickey.pem`.


1. Continua a [Configurare l&#39;app client come consumer in [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)

#### Configurare l&#39;app client come consumer in [!DNL Jira]

1. Accedi all&#39;istanza [!DNL Jira].
1. Nel pannello di navigazione a sinistra, fai clic su **[!UICONTROL [!DNL Jira]Impostazioni]** ![Icona impostazioni Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applicazioni]**> **[!UICONTROL Collegamenti applicazioni]**.
1. Nel campo **[!UICONTROL Immettere l&#39;URL dell&#39;applicazione da collegare]**, immettere:

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Fai clic su **[!UICONTROL Crea nuovo collegamento]**. Ignora il messaggio di errore &quot;Nessuna risposta ricevuta dall’URL immesso&quot;.
1. Nella finestra **[!UICONTROL Collega applicazioni]**, immetti i valori nei campi **[!UICONTROL Chiave consumer]** e **[!UICONTROL Segreto condiviso]**.

   È possibile scegliere i valori per questi campi.

1. Copia i valori dei campi **[!UICONTROL Chiave consumer]** e **[!UICONTROL Segreto condiviso]** in un percorso sicuro.

   Questi valori saranno necessari più avanti nel processo di configurazione.

1. Compila i campi URL come segue:

   | Campo | Descrizione |
   |---|---|
   | [!UICONTROL URL token richiesta] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL URL autorizzazione] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL URL token di accesso] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Selezionare la casella di controllo **[!UICONTROL Crea collegamento in ingresso]**.
1. Fai clic su **[!UICONTROL Continua]**.
1. Nella finestra **[!UICONTROL Collega applicazioni]**, compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Chiave consumer]</p> </td> 
      <td> Incolla la chiave consumer copiata in un percorso sicuro.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome consumer]</td> 
      <td>Immettere un nome a scelta. Questo nome serve come riferimento.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public Key]</td> 
      <td>Incolla la chiave pubblica dal file <code>[!DNL jira_publickey.pem]</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]**.
1. Continua a [Creare una connessione a [!DNL Jira Server] or [!DNL Jira Data Center] in [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Crea una connessione a [!DNL Jira Server] o [!DNL Jira Data Center] in [!DNL Workfront Fusion]

>[!NOTE]
>
>Utilizzare l&#39;app [!DNL Jira Server] per connettersi a [!DNL Jira Server] o [!DNL Jira Data Center].

1. In qualsiasi modulo di [!DNL Jira Server] in [!DNL Workfront Fusion], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL connessione].
1. Nel pannello [!UICONTROL Crea una connessione], compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome connessione]</p> </td> 
      <td> <p>Immetti un nome per la connessione</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Seleziona se utilizzi un ambiente di produzione o non di produzione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Seleziona se utilizzi un account di servizio o un account personale.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Chiave consumer]</td> 
      <td>Incolla la chiave consumer copiata in una posizione sicura in <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">Configura l'app client come consumer in [!DNL Jira]</a></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>Incolla la chiave privata dal file <code>[!DNL jira_privatekey.pcks8]</code> creato in <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">Genera chiavi pubbliche e private per la connessione [!DNL Jira]</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>Immetti l'URL dell'istanza [!DNL Jira]. Esempio: <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## [!DNL Jira Software] moduli e relativi campi

Quando configuri [!DNL Jira Software] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Jira Software], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### [!UICONTROL Verifica i record]

Questo modulo di attivazione avvia uno scenario quando viene aggiunto, aggiornato o eliminato un record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selezionare il webhook che si desidera utilizzare per controllare i record. </p> <p>Per aggiungere un nuovo webhook:</p> 
    <ol> 
     <li value="1">Fare clic su <strong>[!UICONTROL Add]</strong></li> 
     <li value="2">Immettere un nome per il webhook.</li> 
     <li value="3"> <p>Seleziona la connessione da utilizzare per il webhook. </p> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </li> 
     <li value="4"> <p>Selezionare il tipo di record che si desidera che venga controllato dal software:</p> 
      <ul> 
       <li>[!UICONTROL Comment] </li> 
       <li>[!UICONTROL Issue]</li> 
       <li>Progetto [!UICONTROL] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Aggiungi problema a sprint]](#add-issue-to-sprint)
* [[!UICONTROL Crea un record]](#create-a-record)
* [[!UICONTROL Chiamata API personalizzata]](#custom-api-call)
* [[!UICONTROL Eliminare un record]](#delete-a-record)
* [[!UICONTROL Scarica un allegato]](#download-an-attachment)
* [[!UICONTROL Leggi un record]](#read-a-record)
* [[!UICONTROL Aggiorna un record]](#update-a-record)

#### [!UICONTROL Aggiungi problema a sprint]

Questo modulo di azione aggiunge uno o più problemi a uno sprint.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>Immetti o mappa l’ID Sprint dello sprint a cui desideri aggiungere un problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID problema o chiavi]</td> 
   <td>Per ogni problema o chiave che desideri visualizzare nell'esperienza, fai clic su <b>[!UICONTROL Add item]</b> e immetti l'ID o la chiave del problema. In un modulo è possibile immettere fino a 50 caratteri.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un record]

Questo modulo di azione crea un nuovo record in Jira.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record che si desidera venga creato dal modulo, quindi compilare gli altri campi specifici del tipo di record visualizzato nel modulo.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Jira Software]. Utilizzare questo modulo per creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Jira Software].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci un percorso relativo a<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un record]

Questo modulo di azione elimina il record specificato.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da eliminare dal modulo. </p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID o chiave]</td> 
   <td>Immetti o mappa l’ID o la chiave del record da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica un allegato]

Questo modulo di azione scarica un particolare allegato.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID dell’allegato da scaricare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge i dati da un singolo record in [!DNL Jira Software].

Specifica l’ID del record.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record [!DNL Jira] che si desidera venga letto dal modulo.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Utente]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare gli output che si desidera ricevere. Le opzioni di output sono disponibili in base al tipo di record selezionato nel campo "[!UICONTROL Tipo di record]".</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Immettere o mappare l'ID [!DNL Jira Software] univoco del record che si desidera venga letto dal modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un record esistente, ad esempio un problema o un progetto.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da aggiornare nel modulo. Quando si seleziona un tipo di record, nel modulo vengono visualizzati altri campi specifici per tale tipo di record.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Problema di transizione]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID o chiave]</td> 
   <td>Immetti o mappa l’ID o la chiave del record da aggiornare, quindi compila gli altri campi specifici di quel tipo di record che vengono visualizzati nel modulo.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [[!UICONTROL Elenca record]](#list-records)
* [[!UICONTROL Cerca record]](#search-for-records)

#### [!UICONTROL Elenca record]

Questo modulo di ricerca recupera tutti gli elementi di un tipo specifico che corrispondono alla query di ricerca

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record che si desidera elencare nel modulo. Quando si seleziona un tipo di record, nel modulo vengono visualizzati altri campi specifici per tale tipo di record.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Problema Sprint]</li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max Results]</p> </td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Cerca record]

Questo modulo di ricerca cerca i record in un oggetto in [!DNL Jira Software] che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Jira Software] a [!DNL Workfront Fusion], vedere <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connessione di [!DNL Jira Software] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record da cercare nel modulo. Quando si seleziona un tipo di record, nel modulo vengono visualizzati altri campi specifici per tale tipo di record.</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Issues by JQL (Jira Query Language)] </p> <p>Per ulteriori informazioni su JQL, vedere <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> nella Guida di Atlassian. </p> </li> 
     <li>Progetto [!UICONTROL]</li> 
     <li>[!UICONTROL Progetto per problema]</li> 
     <li>[!UICONTROL Utente]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
