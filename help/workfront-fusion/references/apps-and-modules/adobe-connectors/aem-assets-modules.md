---
title: Moduli Adobe Experience Manager Assets
description: Con il connettore Adobe Experience Manager Assets per Adobe Workfront Fusion, puoi creare, caricare e aggiornare risorse e copiare o spostare cartelle e risorse.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: ht
source-wordcount: '3734'
ht-degree: 100%

---

# Moduli Adobe Experience Manager Assets

Con il connettore Adobe Experience Manager Assets per Adobe Workfront Fusion, puoi creare, caricare e aggiornare risorse e copiare o spostare cartelle e risorse.

Per un video introduttivo sul connettore Adobe Experience Manager Assets, consulta:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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

* Per utilizzare questi moduli è necessario disporre di un account Adobe Experience Manager Assets.
* È necessario configurare il flusso da server a server in Adobe Developer Console.

  Per istruzioni sulla configurazione del flusso da server a server in Adobe Developer Console, consulta [Generazione dei token di accesso per le API lato server](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis#the-server-to-server-flow).
* L’account tecnico Adobe Experience Manager deve disporre di autorizzazioni di scrittura.

  Per istruzioni su come aggiungere le autorizzazioni di scrittura all’account tecnico Adobe Experience Manager, consulta [Credenziali del servizio](https://experienceleague.adobe.com/it/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) nella documentazione di Adobe Experience Manager.

## Informazioni sulle API di Adobe Experience Manager Assets

Il connettore Adobe Experience Manager Assets utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Collegare Adobe Experience Manager Assets a Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Per creare una connessione per i moduli Adobe Experience Manager Assets:

1. Fai clic su Aggiungi accanto alla casella Connessione.

2. Seleziona il tipo di connessione che vuoi creare:

   * **AEM Assets as a Cloud Service**

     Questa configurazione richiede informazioni da Adobe Admin Console.

   * **AEM Assets Basic (Adobe Managed Services)**

     Questa configurazione richiede un nome utente e una password.

3. Compila i campi per il tipo di connessione che vuoi creare.

   Per AEM Assets as a Cloud Service, consulta [Configurare la connessione per AEM Assets as a Cloud Service](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Per AEM Assets Basic (Adobe Managed Services), consulta [Configurare la connessione per AEM Assets Basic](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Fai clic su **Continua** per salvare la connessione e tornare al modulo.


### Configurare la connessione per AEM Assets as a Cloud Service

>[!NOTE]
>
>* Le informazioni per questi campi vengono generate durante la configurazione del flusso da server a server in Adobe Developer Console. Questi valori si trovano nel file JSON delle credenziali del servizio generato nel contesto di tale configurazione.
>
>   Per istruzioni sulla configurazione del flusso da server a server in Adobe Developer Console, consulta [Generare i token di accesso per le API lato server](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis#the-server-to-server-flow).
>
>* L’account tecnico Adobe Experience Manager deve disporre di autorizzazioni di scrittura.
>
>   Per istruzioni su come aggiungere le autorizzazioni di scrittura all’account tecnico Adobe Experience Manager, consulta [Credenziali del servizio](https://experienceleague.adobe.com/it/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) nella documentazione di Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Nome connessione</td>
                  <td>
                      <p>Specifica un nome per questa connessione.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">URL dell’istanza senza barra finale</td>
                  <td>Inserisci l’URL per l’istanza di Adobe Experience Manager. Non includere una barra <code>/</code> alla fine dell’URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">Opzioni di compilazione dei dettagli dell’account</td>
                  <td>Seleziona se desideri fornire il codice JSON che descriva i dettagli dell’account o se preferisci inserire i dettagli manualmente.</td>
              </tr>
              <tr>
                  <td role="rowheader">Dettagli dell’account tecnico in formato JSON</td>
                  <td>Se hai scelto di fornire il codice JSON, inserisci o incolla il codice JSON che descrive i dettagli dell’account.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID client</td>
                  <td>Se hai scelto di inserire i dettagli manualmente, inserisci l’ID client generato nella configurazione da server a server.</td>
              </tr>
              <tr>
                  <td role="rowheader">Segreto client</td>
                  <td>Se hai scelto di inserire i dettagli manualmente, inserisci il segreto client generato nella configurazione da server a server.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID account tecnico</td>
                  <td>Se hai scelto di inserire i dettagli manualmente, inserisci l’ID dell’account tecnico. Questo è il campo “id” nel file JSON delle credenziali client.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID organizzazione</td>
                  <td class="">Se hai scelto di inserire i dettagli manualmente, inserisci l’ID della tua organizzazione. Questo è il campo “org” nel file JSON delle credenziali client.</td>
              </tr>
              <tr>
                  <td role="rowheader">Ambiti Meta</td>
                  <td>Inserisci gli ambiti Meta generati nella configurazione da server a server.</td>
              </tr>
              <tr>
                  <td role="rowheader">Chiave privata</td>
                  <td>Inserisci la chiave privata generata con la configurazione da server a server. Per estrarre la chiave privata, fai clic su Estrai, quindi inserisci il file dell’estrazione e la password per il file.</td>
              </tr>
              <tr>
                  <td role="rowheader">URL autenticazione</td>
                  <td>inserisci l’URL di autenticazione per l’account corrente.</td>
              </tr>
          </tbody>
      </table>


### Configurare la connessione per AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Nome connessione</td>
                <td>
                    <p>Specifica un nome per questa connessione.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">URL dell’istanza senza barra finale</td>
                <td>Inserisci l’URL per l’istanza di Adobe Experience Manager. Non includere una barra <code>/</code> alla fine dell’URL.</td>
            </tr>
            <tr>
                <td role="rowheader">Nome utente</td>
                <td>Inserisci il nome utente per l’account AEM Assets utilizzato da questa connessione.</td>
            </tr>
            <tr>
                <td role="rowheader">Password</td>
                <td>Inserisci la password per l’account AEM Assets utilizzato da questa connessione.</td>
            </tr>
        </tbody>
    </table>


## Moduli Adobe Experience Manager Assets e relativi campi

Quando configuri i moduli di Adobe Experience Manager Assets, Workfront Fusion visualizza i campi elencati di seguito. Oltre a questi campi, è possibile che vengano visualizzati altri campi Adobe Experience Manager Assets, a seconda di fattori quali il tuo livello di accesso all’app o al servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Operazioni sui file](#files-operations)
* [Altro](#other)
* [Risorse (API di authoring)](#assets-author-api)
* [Eventi (API di authoring)](#events-author-api)
* [Metadati (API di authoring)](#metadata-author-api)
* [Importazione (API di authoring)](#import-author-api)
* [Relazioni (API di authoring)](#relations-author-api)
* [Cartelle (API cartelle)](#folders-folders-api)

### Operazioni sui file

* [Completare il caricamento](#complete-upload)
* [Ottenere l’archiviazione prefirmata](#get-presigned-storage)
* [Avviare il caricamento](#initiate-upload)
* [Caricare una risorsa](#upload-an-asset)

#### Completare il caricamento

Questo modulo di azione completa un caricamento avviato dopo che tutte le parti del file sono state caricate.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome file</td> 
   <td> <p>Inserisci o mappa un nome per il file caricato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Token di caricamento</td> 
   <td>Inserisci o mappa il token di caricamento per il file binario, come fornito dall’avvio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo MIME</td> 
   <td>Inserisci o mappa il tipo MIME per il file completato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URI completo</td> 
   <td>Inserisci o mappa l’URI completo per il file.</td> 
  </tr> 
 </tbody> 
</table>


#### Ottenere l’archiviazione prefirmata

Questo modulo di azione crea un URL prefirmato temporaneo per caricare o scaricare in modo sicuro i file da AEM senza richiedere credenziali dirette.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account  Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di ricerca</td> 
   <td> <p>Seleziona se cercare la risorsa in base al suo percorso o al suo ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Risorsa</td> 
   <td>Seleziona il percorso della risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Inserisci o mappa l’UDID della risorsa.</td> 
  </tr> 
 </tbody> 
</table>

#### Avviare il caricamento

Questo modulo di azione avvia un caricamento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destinazione</td> 
   <td> <p>Seleziona la cartella in cui desideri caricare un file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome file</td> 
   <td> <p>Inserisci o mappa un nome per il file caricato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dimensioni max file</td> 
   <td>Inserisci o mappa la dimensione in byte del file caricato.</td> 
  </tr> 
 </tbody> 
</table>


#### Caricare una risorsa

Questo modulo di azione carica una risorsa nel tuo account Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destinazione</td> 
   <td> <p>Seleziona la cartella in cui desideri caricare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">File di origine</td> 
   <td>Inserisci o mappa il nome e i dati del file di origine.</td> 
  </tr> 
 </tbody> 
</table>

### Altro


* [Copiare una cartella o una risorsa](#copy-a-folder-or-asset)
* [Creare un record](#create-a-record)
* [Eliminare una cartella, una risorsa o una rappresentazione](#delete-a-folder-asset-or-rendition)
* [Ottenere l’elenco di una cartella](#get-a-folder-listing)
* [Effettua chiamata API personalizzata](#make-a-custom-api-call)
* [Spostare una cartella o una risorsa](#move-a-folder-or-asset)
* [Aggiornare un record](#update-a-record)



#### Copiare una cartella o una risorsa

Questo modulo di azione copia una cartella o una risorsa in un’altra posizione nell’account Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Seleziona se desideri copiare una cartella o una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cartella/Risorsa</td> 
   <td>Seleziona o mappa la cartella o la risorsa da copiare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Percorso di destinazione</td> 
   <td>Seleziona o mappa il percorso della nuova cartella o risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome della cartella/risorsa copiata</td> 
   <td>Inserisci un nome per la nuova cartella o risorsa. Il nome della cartella visualizzato in Adobe Experience Manager Assets è uguale al nome originale. Il nome inserito qui viene visualizzato nell’URL della nuova cartella o risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Copia elementi figli</td> 
   <td>Se copi una cartella, abilita questa opzione per copiare eventuali sottocartelle incluse nella cartella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Abilita questa opzione per sovrascrivere eventuali cartelle o risorse nella posizione di destinazione con lo stesso nome della cartella o risorsa da copiare.</td> 
  </tr> 
 </tbody> 
</table>



#### Creare un record

Questo modulo di azione crea una cartella o un commento a una risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di oggetto</td> 
   <td> <p>Seleziona se desideri creare una cartella o un commento a una risorsa.</p> 
    <ul> 
     <li> <p>Cartella</p> <p>Compila i seguenti campi:</p> 
      <ul> 
       <li> <p>Nome</p> <p>Inserisci un nome per la cartella. Questo nome verrà visualizzato nel percorso del file, pertanto non deve includere spazi o altri caratteri. </p> </li> 
       <li> <p>Titolo</p> <p>Inserisci un titolo per la cartella, che può essere visualizzato al posto del nome.</p> </li> 
      </ul> </li> 
     <li> <p>Commento risorsa</p> <p>Compila i seguenti campi:</p> 
      <ul> 
       <li> <p>Seleziona risorsa</p> <p>Seleziona o mappa l’ID della risorsa alla quale vuoi aggiungere un commento.</p> </li> 
       <li> <p>Commento</p> <p>Digita il testo del commento.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare una cartella, una risorsa o una rappresentazione

Questo modulo di azione elimina una cartella, una risorsa o una rappresentazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Seleziona se desideri eliminare una cartella, una risorsa o una rappresentazione.</p> 
    <ul> 
     <li> <p>Cartella</p> <p>Seleziona la cartella da eliminare selezionando le cartelle nel percorso corrispondente.</p> </li> 
     <li> <p>Risorsa</p> <p>Seleziona la risorsa selezionando le cartelle nel relativo percorso, quindi la risorsa da eliminare.</p> </li> 
     <li> <p>Rappresentazione</p> <p>Seleziona la rappresentazione selezionando le cartelle nel relativo percorso.</p> <p>Inserisci o mappa il nome della rappresentazione.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottenere l’elenco di una cartella

Questo modulo di azione recupera una rappresentazione di una cartella esistente e delle relative entità figlio (cartelle o risorse).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cartella</td> 
   <td>Seleziona o mappa la cartella da recuperare. Per aggiungere sottocartelle al percorso, fai clic sull’icona con il segno più e seleziona la sottocartella.</td> 
  </tr> 
 </tbody> 
</table>

#### Effettua chiamata API personalizzata

Questo modulo di azione effettua una chiamata API personalizzata all’API Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Inserisci un percorso relativo all’URL di base di Adobe Experience Manager.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Metodo</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTPS</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Intestazioni</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stringa query</td> 
   <td> <p>Inserisci la stringa di query della richiesta. Per ogni coppia chiave/valore, fai clic su <b>Aggiungi elemento</b> e immetti la chiave e il valore.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Spostare una cartella o una risorsa

Questo modulo di azione sposta la risorsa o la cartella dal percorso specificato a una nuova posizione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Seleziona se spostare una cartella o una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cartella/Risorsa</td> 
   <td>Seleziona o mappa la cartella o la risorsa da spostare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Percorso di destinazione</td> 
   <td>Seleziona o mappa il percorso in cui spostare la cartella o la risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome della cartella/risorsa spostata</td> 
   <td>Inserisci un nuovo nome per la cartella o la risorsa spostata. Il nome della cartella visualizzato in Adobe Experience Manager Assets è uguale al nome originale. Il nome inserito viene visualizzato nell’URL della cartella o della risorsa spostata.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Abilita questa opzione per sovrascrivere nella posizione di destinazione eventuali cartelle o risorse che hanno lo stesso nome della cartella o risorsa che viene spostata.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un record

Questo modulo di azione aggiorna un record esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione del tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> <p>Seleziona se desideri eliminare i metadati o la rappresentazione di una risorsa.</p> 
    <ul> 
     <li> <p>Metadati risorsa </p> 
      <ul> 
       <li> <p>Seleziona la risorsa per la quale vuoi aggiornare i metadati.</p> </li> 
       <li> <p>Inserisci il nuovo titolo della risorsa.</p> </li> 
      </ul> </li> 
     <li> <p>Rappresentazione risorsa</p> 
      <ul> 
       <li> <p>Seleziona la risorsa per la quale vuoi aggiornare la rappresentazione.</p> </li> 
       <li> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Risorse (API di authoring)

* [Eliminare una risorsa](#delete-asset)
* [Ottenere lo stato di un processo](#get-job-status)

#### Eliminare una risorsa

Questo modulo di azione elimina una singola risorsa in base all’ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Forza</td> 
   <td>Abilita questa opzione per forzare l’eliminazione della risorsa, anche se vi fanno riferimento altri elementi.</td> 
  </tr> 
 </tbody> 
</table>

#### Ottenere lo stato di un processo

Questo modulo ottiene lo stato corrente di un processo asincrono.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account  Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo</td> 
   <td> <p>Immetti o mappa l’ID del processo del quale desideri ottenere lo stato.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Eventi (API di authoring)

#### Osserva eventi

Questo modulo tigger avvia uno scenario quando si verifica un evento in AEM Assets.

Il modulo contiene un singolo campo: Webhook. Seleziona un webhook esistente da utilizzare per questi eventi o creane uno nuovo.

Per creare un nuovo webhook:

1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Compila i seguenti campi:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Nome webhook</td>
        <td>Specifica un nome per il webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">Connessione</td>
        <td>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</td>
       </tr>
     </tbody>
   </table>

1. Fai clic su Salva per salvare il webhook e tornare al modulo.


### Metadati (API di authoring)

* [Ottenere i metadati delle risorse](#get-asset-metadata)
* [Aggiornare i metadati delle risorse](#update-asset-metadata)

#### Ottenere i metadati delle risorse

Questo modulo di azione recupera i metadati relativi alla risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa per la quale desideri ottenere i metadati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare i metadati delle risorse

Questo modulo di azione aggiorna i metadati per la risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa per la quale desideri aggiornare i metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aggiornamenti</td> 
   <td> <p>Per ogni elemento di metadati che desideri aggiornare, fai clic su <b>Aggiungi elemento</b> e seleziona l’operazione. Gli altri campi della casella Aggiungi elemento dipendono dall’operazione selezionata.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Importazione (API di authoring)

* [Ottenere i risultati del processo di importazione](#get-import-job-results)
* [Ottenere lo stato del processo di importazione](#get-import-job-status)
* [Caricare una risorsa da un URL](#upload-an-asset-from-a-url)

#### Ottenere i risultati del processo di importazione

Questo modulo di azione recupera i risultati per il processo di importazione specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo di importazione</td> 
   <td> <p>Inserisci o mappa l’ID del processo per il quale desideri recuperare i risultati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottenere lo stato del processo di importazione

Questo modulo di azione recupera lo stato del processo di importazione specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo di importazione</td> 
   <td> <p>Inserisci o mappa l’ID del processo di cui desideri recuperare lo stato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Caricare una risorsa da un URL

Questo modulo di azione carica una nuova risorsa importando file dagli URL specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Titolo</td> 
   <td> <p>Inserisci o mappa un titolo per la risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrizione</td> 
   <td> <p>Inserisci o mappa una descrizione per la risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Soggetto</td> 
   <td> <p>Inserisci o mappa il oggetto della risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Creatore</td> 
   <td> <p>Inserisci o mappa il creatore della risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Data di scadenza</td> 
   <td> <p>Inserisci o mappa la data di scadenza della risorsa.</p><p>Per un elenco dei formati di data e ora supportati, consulta <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercizione del tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metadati personalizzati</td> 
   <td> <p>Per ogni elemento di metadati personalizzati che desideri aggiungere alla risorsa, fai clic su <b>Aggiungi elemento</b> e inserisci il nome e il valore dei metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Percorso o ID cartella</td> 
   <td> <p>Seleziona se specificare la cartella di destinazione in base al percorso o all’ID, quindi seleziona il percorso o inserisci l’ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">File da importare</td> 
   <td> <p>Per ogni file da importare, fai clic su <b>Aggiungi elemento&lt;/&gt; e inserisci i dettagli del file. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Relazioni (API di authoring)

* [Creare relazioni tra risorse](#create-asset-relations)
* [Eliminare una relazione tra risorse](#create-asset-relations)
* [Ottenere tipi di relazione tra risorse](#get-asset-relation-types)
* [Ottenere relazioni tra risorse](#get-asset-relations)

#### Creare relazioni tra risorse

Questo modulo di azione crea nuove relazioni tra risorse per la risorsa selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa alla quale vuoi correlare altre risorse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Risorse correlate</td> 
   <td> <p>Per ogni risorsa che vuoi correlare alla risorsa selezionata, fai clic su <b>Aggiungi elemento</b> e inserisci o mappa l’ID della risorsa e il tipo di relazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare una relazione tra risorse

Questo modulo di azione elimina una relazione per una risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa dalla quale vuoi eliminare una relazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Risorse correlate</td> 
   <td> <p>Immetti o mappa il tipo di relazione da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Specifica l’ID della risorsa correlata da eliminare</td> 
   <td> <p>Seleziona questa casella per eliminare una relazione specifica. Se questa casella non è selezionata, vengono eliminate tutte le relazioni del tipo selezionato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa correlata</td> 
   <td> <p>Se vuoi eliminare una relazione specifica, inserisci o mappa l’ID della relazione da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Ottenere tipi di relazione tra risorse

Questo modulo elenca i tipi di relazione esistenti per la risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa per la quale desideri elencare i tipi di relazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Ottenere relazioni tra risorse

Questo modulo elenca le relazioni tra risorse esistenti per la risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa per la quale desideri elencare le relazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipi di relazione</td> 
   <td> <p>Inserisci o mappa un elenco separato da virgole dei tipi di relazione per i quali vuoi elencare le relazioni.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Cartelle (API cartelle)

* [Creare cartelle](#create-folders)
* [Eliminare una cartella in base all’ID](#delete-a-folder-by-id)
* [Eliminare cartelle in base al percorso](#delete-folders-by-path)
* [Ottenere i risultati di un processo cartelle](#get-folders-job-results)
* [Ottenere lo stato di un processo cartelle](#get-folders-job-status)
* [Elencare le cartelle](#list-folders)

#### Creare cartelle

Questo modulo di azione crea una nuova cartella in Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cartelle da creare</td> 
   <td> <p>Per ogni cartella da creare, fai clic su <b>Aggiungi elemento</b> e inserisci le informazioni seguenti:</p>
   <ul>
   <li><b>Percorso nuova cartella</b><p>Seleziona il percorso per la nuova cartella.</p></li>
       <li> <b>Nome</b> <p>Inserisci un nome per la cartella. Questo nome verrà visualizzato nel percorso del file, pertanto non deve includere spazi o altri caratteri. </p> </li> 
       <li> <b>Titolo</b> <p>Inserisci un titolo per la cartella, che può essere visualizzato al posto del nome.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare una cartella in base all’ID

Questo modulo di azione elimina la cartella Adobe Experience Manager Assets con l’ID specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID cartella</td> 
   <td> Inserisci o mappa l’ID della cartella da eliminare.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Elimina sottocartelle</td> 
   <td> Abilita questa opzione per eliminare la cartella e tutte le relative sottocartelle.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forza</td> 
   <td> Abilita questa opzione per forzare l’eliminazione delle cartelle, anche se altri elementi vi fanno riferimento.</td>
  </tr> 
 </tbody> 
</table>

#### Eliminare cartelle in base al percorso

Questo modulo di azione elimina le cartelle di Adobe Experience Manager Assets dai percorsi specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione del tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Percorsi cartelle</td> 
   <td>Per ogni cartella da eliminare, fai clic su <b>Aggiungi elemento</b> e seleziona il percorso della cartella.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Elimina sottocartelle</td> 
   <td> Abilita questa opzione per eliminare la cartella e tutte le relative sottocartelle.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forza</td> 
   <td> Abilita questa opzione per forzare l’eliminazione della risorsa, anche se vi fanno riferimento altri elementi.</td>
  </tr> 
 </tbody> 
</table>

#### Ottenere i risultati di un processo cartelle

Questo modulo recupera i risultati di un processo asincrono creato dall’API per cartelle di Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo</td> 
   <td> Inserisci o mappa l’ID del processo per il quale desideri recuperare i risultati.</td>
  </tr> 
 </tbody> 
</table>

#### Ottenere lo stato di un processo cartelle

Questo modulo recupera i risultati di un processo asincrono creato dall’API per cartelle di Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo</td> 
   <td> Inserisci o mappa l’ID del processo del quale vuoi recuperare lo stato.</td>
  </tr> 
 </tbody> 
</table>


#### Elencare le cartelle

Questo modulo elenca le sottocartelle della cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni su come connettere il tuo account Adobe Experience Manager Assets a Workfront Fusion, consulta <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connettere Adobe Experience Manager Assets a Workfront Fusion</a> in questo articolo.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Percorso o ID cartella</td> 
   <td> <p>Seleziona se specificare la cartella di destinazione in base al percorso o all’ID, quindi seleziona il percorso o inserisci l’ID.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

