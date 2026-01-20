---
title: Moduli Frame.io
description: I [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] account.
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 3cb613c11500dfc94774783ee0b38e6f1768de20
workflow-type: ht
source-wordcount: '4539'
ht-degree: 100%

---

# Moduli [!DNL Frame.io] V4

>[!IMPORTANT]
>
>Questo articolo descrive la nuova versione del connettore Frame.io. Questo connettore viene utilizzato per connettersi alla versione 4 di Frame.io.
>
>Per istruzioni sulla versione legacy del connettore Frame.io, consulta [Connettore legacy Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

I moduli [!DNL Frame.io] di Adobe Workfront Fusion consentono di monitorare, creare, aggiornare, recuperare o eliminare risorse e commenti nel tuo account [!DNL Frame.io].

Workfront offre due connettori Frame.io, in base alla versione di Frame.io a cui ti stai connettendo.

| Connettore | Versione Frame.io |
|---|---|
| Frame.io | V4 |
| Frame.io (legacy) | V3 |

Per istruzioni sulla versione legacy del connettore Frame.io, consulta [Connettore legacy Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Per un video introduttivo sul connettore Frame.io, consulta:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Per utilizzare i moduli [!DNL Frame.io], devi disporre di un account [!DNL Frame.io]

## Informazioni sull’API di Frame.io

Il connettore Frame.io utilizza quanto riportato di seguito:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.frame.io/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL Frame.io] ad [!UICONTROL Adobe Workfront Fusion]

Puoi connetterti automaticamente con le credenziali utente, creare manualmente una connessione con le credenziali utente oppure creare una connessione da server a server.

* [Connessione automatica con le credenziali utente](#connect-automatically-with-user-credentials#)
* [Creazione manuale di una connessione con le credenziali utente](#create-a-user-credentials-connection-manually)
* [Creazione di una connessione da server a server](#create-a-server-to-server-connection)

### Connessione automatica con le credenziali utente

Questo metodo crea automaticamente una connessione se hai effettuato l’accesso a Frame.io oppure ti connette alla pagina di accesso di Frame.io per consentirti di accedere.

1. In qualsiasi modulo Frame.io, fai clic su **[!UICONTROL Add]** (Aggiungi) accanto alla casella Connessione.
1. Specifica un nome per la connessione.
1. Fai clic su **Continue** (Continua).
1. Se ti viene richiesto, accedi all’account Frame.io.
1. Se fai parte di più organizzazioni Frame.io, seleziona quella che desideri utilizzare per questa connessione.

La connessione viene creata.

### Creazione manuale di una connessione con le credenziali utente

Puoi creare una connessione con credenziali utente accedendo a Frame.io oppure specificando un ID client o un Segreto client.

Per creare una connessione da server a server, devi innanzitutto configurare un’applicazione in Adobe Developer Console.

* [Creare le credenziali utente in Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Configurare una connessione di autenticazione utente](#configure-a-user-authentication-connection)

#### Creare le credenziali utente in Adobe Developer Console

Se non disponi già di credenziali da server a server per un progetto Adobe Developer Console, puoi crearle.

1. Apri [Adobe Developer Console](https://developer.adobe.com/).
1. Seleziona un progetto esistente in Adobe Developer Console da utilizzare per questa connessione

   Oppure

   Crea un nuovo progetto in Adobe Developer Console. Per istruzioni, consulta [Creare un progetto vuoto](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Nella pagina Project overview (Panoramica del progetto) o Get started with your new project (Inizia un nuovo progetto), fai clic su **Add API** (Aggiungi API).
1. Nella pagina visualizzata individua e fai clic su **Frame.io API**.
1. Nella pagina Select authentication type (Seleziona tipo di autenticazione), seleziona **User Authentication** (Autenticazione utente) e fai clic su **Next** (Avanti).
1. Nella pagina Add a user authentication credential (Aggiungi credenziali di autenticazione utente), seleziona **OAuth Web App** e fai clic su **Next** (Avanti).
1. Nella pagina Configure OAuth Web App credential (Configura credenziali web app OAuth) inserisci quanto segue:   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Default redirect URI] (URI di reindirizzamento predefinito)</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Modello URI di reindirizzamento]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. Fai clic su **Next** (Avanti).
1. Fai clic su **Save configured API** (Salva API configurata).
1. Nella pagina di prodotto, fai clic sulla scheda delle credenziali appena create.

   Qui puoi trovare l’ID client e il Segreto client.

>[!NOTE]
>
> È consigliabile lasciare aperta questa finestra quando inizi a configurare la connessione in Adobe Workfront Fusion. Puoi copiare l’ID client, quindi recuperare e copiare il Segreto client da questa pagina per incollarlo nei campi della connessione.


#### Configurare una connessione di autenticazione utente

1. In qualsiasi modulo Frame.io, fai clic su **[!UICONTROL Add]** (Aggiungi) accanto alla casella Connection (Connessione).
1. Nella casella Create a connection (Crea connessione), fai clic su **Show advanced settings** (Mostra impostazioni avanzate).

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
          <td>
            <p>Seleziona <b>IMS User authentication</b> (Autenticazione utente IMS).</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
          <td>
            <p>Specifica un nome per questa connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]</td>
          <td>Inserisci il tuo [!UICONTROL Client ID] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].<p>Per istruzioni su come creare le credenziali, consulta <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Creare credenziali utente in Adobe Developer Console</a> in questo articolo.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
          <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].<p>Per istruzioni su come creare le credenziali, consulta <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Creare le credenziali utente in Adobe Developer Console</a>, in questo articolo.</p>
        </tr>
       </tbody>
    </table>
1. Se ti viene richiesto, accedi all’account Frame.io.
1. Se fai parte di più organizzazioni Frame.io, seleziona quella che desideri utilizzare per questa connessione.

La connessione viene creata.


### Creazione di una connessione da server a server

Per creare una connessione da server a server, devi innanzitutto configurare un’applicazione in Adobe Developer Console.

* [Creare le credenziali da server a server in Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Configurare una connessione da server a server](#configure-a-server-to-server-connection)

#### Creare le credenziali da server a server in Adobe Developer Console

Se non disponi già di credenziali da server a server per un progetto Adobe Developer Console, puoi crearle.

1. Apri [Adobe Developer Console](https://developer.adobe.com/).
1. Seleziona un progetto esistente in Adobe Developer Console da utilizzare per questa connessione

   Oppure

   Crea un nuovo progetto in Adobe Developer Console. Per istruzioni, consulta [Creare un progetto vuoto](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Nella pagina Project overview (Panoramica del progetto) o Get started with your new project (Inizia un nuovo progetto), fai clic su **Add API** (Aggiungi API).
1. Nella pagina visualizzata individua e fai clic su **Frame.io API**.
1. Nella pagina Select authentication type (Seleziona tipo di autenticazione), seleziona **Autenticazione da server a server** (Server-to-Server Authentication) e fai clic su **Next** (Avanti).
1. Inserisci un nome per le credenziali. Questa operazione ti consente di identificare le credenziali in un secondo momento nell’area delle credenziali API in Adobe Admin Console.
1. Fai clic su **Next** (Avanti).
1. Nella pagina Select product profiles (Seleziona profili di prodotto), seleziona il profilo di prodotto che include l’account Frame.io a cui desideri connetterti.
1. Fai clic su **Save configured API** (Salva API configurata).
1. Nella pagina di prodotto, fai clic sulla scheda delle credenziali appena create.

   Qui puoi trovare l’ID client e il Segreto client.

>[!NOTE]
>
> È consigliabile lasciare aperta questa finestra quando inizi a configurare la connessione in Adobe Workfront Fusion. Puoi copiare l’ID client, quindi recuperare e copiare il Segreto client da questa pagina per incollarlo nei campi della connessione.


#### Configurare una connessione da server a server

1. In qualsiasi modulo Frame.io, fai clic su **[!UICONTROL Add]** (Aggiungi) accanto alla casella Connection (Connessione).

1. Compila i campi obbligatori:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
          <td>
            <p>Seleziona <b>IMS Server to Server</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
          <td>
            <p>Specifica un nome per questa connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]</td>
          <td>Inserisci il tuo [!UICONTROL Client ID] [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come creare le credenziali, consulta <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Creare le credenziali da server a server in Adobe Developer Console</a>, in questo articolo.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
          <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come creare le credenziali, consulta <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Creare le credenziali da server a server in Adobe Developer Console</a>, in questo articolo.</p>
        </tr>
       </tbody>
    </table>
1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.




## Moduli [!DNL Frame.io] e relativi campi

Quando configuri i moduli [!DNL Frame.io], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Frame.io], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Risorse](#assets)
* [Commenti](#comments)
* [Cartelle](#folders)
* [Progetti](#projects)
* [Condivisioni](#shares)
* [Aree di lavoro](#workspaces)
* [Metadati](#metadata)
* [Altro](#other)

### Risorse

* [[!UICONTROL Crea una risorsa]](#create-an-asset)
* [[!UICONTROL Elimina una risorsa]](#delete-an-asset)
* [[!UICONTROL Ottieni una risorsa]](#get-an-asset)
* [[!UICONTROL Elenca le risorse]](#list-assets)
* [Osserva risorsa eliminata](#watch-asset-deleted)
* [Osserva nuova risorsa](#watch-new-asset)

#### [!UICONTROL Crea una risorsa] <!--different for v4-->

Questo modulo di azione crea una nuova risorsa. Puoi caricare un file locale o fornire l’URL da cui creare la risorsa in un file remoto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente il progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona l’area di lavoro oppure mappa l’ID dell’area di lavoro contenente il progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto oppure mappa l’ID del progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso in cui desideri creare una risorsa.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">Tipo di caricamento </td> 
    <td> <p>Seleziona se creare una risorsa da un file locale o da un file remoto.</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">Dimensione file </td> 
    <td> <p>Se stai caricando un file locale, inserisci o mappa la dimensione del file in byte.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL URL di origine] </td> 
   <td> <p>Se stai creando la risorsa da un file remoto, inserisci l’URL del file da caricare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome del file di origine.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL Crea una risorsa (legacy)] <!--different for v4-->

Questo modulo di azione crea una nuova risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente il progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona l’area di lavoro oppure mappa l’ID dell’area di lavoro contenente il progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto oppure mappa l’ID del progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso in cui desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome file] </td> 
   <td> <p>Specifica il nome del file da utilizzare per questa risorsa.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Dimensione file </td> 
    <td> <p>Inserisci oppure mappa la dimensione del file in byte.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL URL di origine] </td> 
   <td> <p>Se stai creando un file, inserisci l’URL del file da caricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di file multimediale] </td> 
   <td> <p>Seleziona il tipo di file multimediale per questa risorsa.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Elimina una risorsa]

Questo modulo di azione elimina una risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente la risorsa da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Seleziona oppure mappa la risorsa da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni una risorsa]

Questo modulo di azione recupera i dettagli della risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente la risorsa da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Seleziona o esegui il mapping della risorsa da recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca le risorse]

Questo modulo di ricerca recupera tutte le risorse nella cartella del progetto specificato.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente le risorse da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di risorse restituite] </td> 
   <td> <p>Inserisci oppure mappa il numero massimo di risorse che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva risorsa eliminata

Questo modulo trigger avvia uno scenario quando una risorsa viene eliminata.

Seleziona il webhook da utilizzare per questo modulo oppure fai clic su Add (Aggiungi) accanto al campo Webhook e inserisci le informazioni seguenti:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook] </td> 
   <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account da controllare per rilevare le risorse eliminate.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva nuova risorsa

Questo modulo trigger avvia uno scenario quando viene creata una nuova risorsa.

Seleziona il webhook da utilizzare per questo modulo oppure fai clic su Add (Aggiungi) accanto al campo Webhook e inserisci le informazioni seguenti:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook] </td> 
   <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account da controllare per rilevare nuove risorse.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Commenti

* [[!UICONTROL Crea un commento]](#create-a-comment)
* [[!UICONTROL Elimina un commento]](#delete-a-comment)
* [[!UICONTROL Ottieni un commento]](#get-a-comment)
* [[!UICONTROL Elenca commenti]](#list-comments)
* [[!UICONTROL Aggiorna un commento]](#update-a-comment)
* [Osserva commento aggiornato](#watch-comment-updated)
* [Osserva nuovo commento](#watch-new-comment)

#### [!UICONTROL Crea un commento]

Questo modulo di azione aggiunge un nuovo commento o una nuova risposta alla risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente la risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’area di lavoro contenente la risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto oppure mappa l’ID del progetto contenente la risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso della risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo]</td> 
   <td> <p> Inserisci il contenuto del testo del commento o della risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marca temporale] </td> 
   <td> <p>Inserisci il numero del fotogramma nel video a cui collegare il commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pagina] </td> 
   <td> <p>Se la risorsa è un PDF, inserisci oppure mappa la pagina a cui allegare il commento.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un commento]

Questo modulo di azione elimina un commento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente il commento da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID commento] </td> 
   <td> <p>Inserisci oppure mappa l’ID del commento da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un commento]

Questo modulo di azione recupera i dettagli del commento specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account contenente il commento di cui recuperare i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID commento] </td> 
   <td> <p>Seleziona il commento di cui recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca commenti]

Questo modulo di ricerca recupera tutti i commenti della risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente la risorsa da cui recuperare i commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro contenente la risorsa da cui recuperare i commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto contenente la risorsa da cui recuperare i commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso che porta alla risorsa di cui elencare i commenti.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di commenti restituiti] </td> 
   <td> <p>Inserisci oppure mappa il numero massimo di commenti che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un commento]

Questo modulo di azione modifica un commento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente il progetto che include la risorsa di cui aggiornare un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID commento] </td> 
   <td> <p>Seleziona il commento da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo]</td> 
   <td> <p> Inserisci il contenuto del testo del commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Marca temporale] </td> 
   <td> <p>Inserisci il numero del fotogramma nel video a cui è collegato il commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pagina] </td> 
   <td> <p>Se la risorsa è un PDF, inserisci oppure mappa la pagina a cui è allegato il commento.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva commento aggiornato

Questo modulo trigger avvia uno scenario quando un commento viene aggiornato.

Seleziona il webhook da utilizzare per questo modulo oppure fai clic su Add (Aggiungi) accanto al campo Webhook e inserisci le informazioni seguenti:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook] </td> 
   <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account che desideri controllare per rilevare i commenti aggiornati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva nuovo commento

Questo modulo trigger avvia uno scenario quando viene creato un commento.

Seleziona il webhook da utilizzare per questo modulo oppure fai clic su Add (Aggiungi) accanto al campo Webhook e inserisci le informazioni seguenti:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook] </td> 
   <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account che desideri controllare per rilevare nuovi commenti.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Cartelle

#### Crea una cartella

Questo modulo di azione crea una nuova cartella in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro in cui creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto in cui creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso in cui creare una cartella.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa un nome per la nuova cartella.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Progetti

* [Crea un progetto](#create-a-project)
* [Invita utenti a progetto Frame.io](#invite-users-to-frameio-project)
* [Elenca progetti](#list-projects)

#### Crea un progetto

Questo modulo di azione crea un nuovo progetto in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare un progetto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro in cui creare un progetto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa un nome per il nuovo progetto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Invita utenti a progetto Frame.io

Questo modulo di azione invita degli utenti al progetto Frame.io specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente il progetto a cui invitare un utente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro contenente il progetto a cui invitare un utente.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID progetto </td> 
   <td> <p>Seleziona oppure mappa il progetto a cui invitare un utente.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">ID utente </td> 
   <td> <p>Seleziona oppure mappa l’utente da invitare al progetto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca progetti]

Questo modulo di ricerca recupera tutti i progetti per il team specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente la risorsa da cui recuperare i progetti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro contenente la risorsa da cui recuperare i progetti.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di progetti restituiti] </td> 
   <td> <p>Inserisci oppure mappa il numero massimo di progetti che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Condivisioni

* [Aggiungi una risorsa a un collegamento di condivisione](#add-an-asset-to-a-share-link)
* [Crea un collegamento di condivisione](#create-a-share-link)

#### Aggiungi una risorsa a un collegamento di condivisione

Questo modulo di azione aggiunge una risorsa a un collegamento di condivisione in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente il collegamento di condivisione a cui aggiungere una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID link di condivisione] </td> 
   <td> <p>Seleziona oppure mappa il collegamento di condivisione a cui aggiungere una risorsa.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Inserisci oppure mappa l’ID della risorsa da aggiungere al collegamento di condivisione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Crea un collegamento di condivisione

Questo modulo di azione crea un nuovo collegamento di condivisione in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare un collegamento di condivisione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona oppure mappa l’area di lavoro in cui creare un collegamento di condivisione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona oppure mappa il progetto in cui creare un collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Accesso </td> 
   <td> <p>Seleziona se questo collegamento consente l’accesso pubblico o limitato.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Risorse </td> 
   <td> <p>Per ciascuna risorsa da aggiungere al collegamento di condivisione, fai clic su <b>Add item</b> (Aggiungi elemento) e inserisci l’ID della risorsa.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Descrizione </td> 
   <td> <p>Inserisci oppure mappa una descrizione per il collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa la data di scadenza del collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa un nome per il nuovo collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa una passphrase per il collegamento di condivisione.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aree di lavoro

#### Crea un’area di lavoro

Questo modulo di azione crea una nuova area di lavoro in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare un’area di lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome] </td> 
   <td> <p>Inserisci oppure mappa un nuovo nome per l’area di lavoro.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elenca aree di lavoro

Questo modulo elenca tutte le aree di lavoro di un account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente la risorsa da cui recuperare le aree di lavoro.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di aree di lavoro restituite] </td> 
   <td> <p>Inserisci oppure mappa il numero massimo di aree di lavoro che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Metadati

* [Crea un campo a livello di account](#create-an-account-level-field)
* [Elimina un campo a livello di account](#delete-an-account-level-field)
* [Ottieni metadati](#get-metadata)
* [Elenca campi a livello di account](#list-account-level-fields)
* [Aggiorna la definizione di un campo a livello di account](#update-an-account-level-field-definition)
* [Aggiorna i metadati in più file](#update-metadata-across-multiple-files)

#### Crea un campo a livello di account

Questo modulo di azione crea e configura un nuovo campo di metadati a livello di account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare i metadati.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Tipo di campo </td> 
   <td> <p>Seleziona il tipo di campo di metadati che desideri creare, quindi configura le opzioni per tale campo.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa un nome per il nuovo campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elimina un campo a livello di account

Questo modulo di azione elimina un singolo campo di metadati a livello di account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente il campo di metadati da eliminare.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID definizione campo </td> 
   <td> <p>Inserisci oppure mappa l’ID del campo da eliminare. Per trovare gli ID dei campi, puoi usare il modulo Elenca campi a livello di account.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni metadati

Questo modulo di azione recupera i metadati di un file in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente il file per il quale vuoi recuperare i metadati.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID file </td> 
   <td> <p>Inserisci oppure mappa l’ID del file per il quale vuoi recuperare i metadati.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Mostra nullo </td> 
   <td> <p>Abilita questa opzione per includere nell’output anche i campi con valore nullo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elenca campi a livello di account

Questo modulo recupera un elenco di campi di metadati a livello di account per l’account specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account da cui elencare i campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di accordi restituiti]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di campi che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiorna la definizione di un campo a livello di account

Questo modulo aggiorna la definizione di un singolo campo di metadati esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account in cui creare i metadati.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID definizione campo </td> 
   <td> <p>Inserisci oppure mappa l’ID del campo da aggiornare. Per trovare gli ID dei campi, puoi usare il modulo Elenca campi a livello di account.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Tipo di campo </td> 
   <td> <p>Se desideri cambiare il tipo di campo, seleziona il tipo di campo di metadati da creare, quindi configura le opzioni per tale campo.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Inserisci oppure mappa un nuovo nome per il campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiorna i metadati in più file

Questo modulo aggiorna i campi di metadati in uno o più file con i valori specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona oppure mappa l’account contenente i file per i quali vuoi aggiornare i metadati.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL ID area di lavoro] </td> 
   <td> <p>Seleziona l’area di lavoro oppure mappa l’ID dell’area di lavoro contenente il progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona il progetto oppure mappa l’ID del progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file] </td> 
   <td> <p>Per ogni file per cui desideri aggiornare i metadati, fai clic su <b>Aggiungi elemento</b> e inserisci o mappa l’ID file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Valori] </td> 
   <td> <p>Per ogni campo per cui desideri aggiornare i metadati, fai clic su <b>Aggiungi elemento</b> e immetti o mappa l’ID definizione campo e il valore da inserire in tale campo. Tutti i file specificati nel campo ID file vengono aggiornati con questo valore di campo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [Effettua chiamata API personalizzata](#make-a-custom-api-call)
* [Osserva eventi](#watch-events)
* [Controlla valore metadati aggiornato](#watch-metadata-value-updated)


#### [!UICONTROL Effettua chiamata API personalizzata]

Questo modulo ti consente di effettuare una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Inserisci un percorso relativo a <code>https://api.frame.io</code>. Esempio: <code> /v4/me</code></p> <p>Nota: per l’elenco degli endpoint disponibili, consulta la documentazione di riferimento API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metodo]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query] </td> 
   <td> <p>Inserisci la stringa di query della richiesta. Per ciascun parametro da includere nella stringa di query, fai clic su <b>[!UICONTROL Add item]</b> (Aggiungi elemento) e inserisci il nome del campo e il valore desiderato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> in JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Osserva eventi

Questo modulo di trigger istantaneo avvia uno scenario quando l’evento selezionato si verifica in Frame.io.

Puoi utilizzare un webhook esistente o crearne uno nuovo.

Per creare un nuovo webhook:

1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Compila le seguenti informazioni:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
     <td role="rowheader">Nome webhook </td> 
      <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
     </tr> 
     <tr> 
       <td role="rowheader">[!UICONTROL Connessione] </td> 
       <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
     </tr> 
     <tr> 
     <td role="rowheader">[!UICONTROL ID account] </td> 
      <td> <p>Seleziona oppure mappa l’account contenente l’area di lavoro da cui osservare gli eventi.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID area di lavoro]</td> 
      <td> <p>Inserisci l’ID dell’area di lavoro in cui osservare gli eventi.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Eventi]</td> 
      <td> <p>Seleziona gli eventi da attivare in questo modulo</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **Salva** per salvare il webhook e tornare al modulo.
1. Fai clic su **OK** nel modulo Osserva eventi per salvare la configurazione.


#### Controlla valore metadati aggiornato

Questo modulo trigger avvia uno scenario quando un commento viene aggiornato.

Seleziona il webhook da utilizzare per questo modulo oppure fai clic su Add (Aggiungi) accanto al campo Webhook e inserisci le informazioni seguenti:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook] </td> 
   <td> <p>Inserisci un nome per il nuovo webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connessione] </td> 
   <td>Per istruzioni su come creare una connessione a [!DNL Frame.io], consulta <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] ad Adobe Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account oppure mappa l’ID dell’account che desideri controllare per rilevare valori di metadati aggiornati.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
