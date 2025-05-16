---
title: Moduli Adobe Experience Manager Assets
description: Con il connettore  [!DNL Adobe Experience Manager Assets]  per  [!DNL Adobe Workfront Fusion], puoi creare, caricare e aggiornare risorse e copiare o spostare cartelle e risorse.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: 40470e5d2183f690ad65f5e1170f78c37dee8603
workflow-type: tm+mt
source-wordcount: '1727'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Assets] moduli

Con il connettore [!DNL Adobe Experience Manager Assets] per [!DNL Adobe Workfront Fusion], puoi creare, caricare e aggiornare risorse e copiare o spostare cartelle e risorse.

Per un video introduttivo sul connettore Adobe Experience Manager Assets, vedi:

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione </p>
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

* Per utilizzare questi moduli è necessario disporre di un account [!DNL Adobe Experience Manager Assets].
* È necessario configurare il flusso [!UICONTROL Server-to-server] in [!DNL Adobe Developer console].

  Per istruzioni sulla configurazione del flusso [!UICONTROL Server-to-server] in [!DNL Adobe Developer console], vedere [Generazione dei token di accesso per le API lato server](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=it#the-server-to-server-flow).
* L&#39;account tecnico Adobe Experience Manager deve disporre di autorizzazioni di scrittura.

  Per istruzioni sull&#39;aggiunta di autorizzazioni di scrittura all&#39;account tecnico Adobe Experience Manager, vedere [Credenziali di servizio](https://experienceleague.adobe.com/it/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) nella documentazione di Adobe Experience Manager.

## Informazioni API di Adobe Experience Manager Assets

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

## Connetti [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion] {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Per creare una connessione per i moduli [!DNL Adobe Experience Manager Assets]:

1. Fai clic su [!UICONTROL Aggiungi] accanto alla casella [!UICONTROL Connessione].

2. Selezionare il tipo di connessione che si sta creando:

   * **[!DNL AEM Assets as a Cloud Service]**

     Questa configurazione richiede informazioni da [!DNL Adobe Admin Console].

   * **[!DNL AEM Assets Basic] ([!DNL Adobe Managed Services])**

     Questa configurazione richiede un nome utente e una password.

3. Compila i campi per il tipo di connessione che stai creando.

   Per [!DNL AEM Assets as a Cloud Service], vedere [Configurare la connessione per [!DNL AEM Assets as a Cloud Service]](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Per [!UICONTROL AEM Assets Basic] ([!DNL Adobe Managed Services]), vedere [Configurare la connessione per [!UICONTROL AEM Assets Basic]](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


### Configura la connessione per [!DNL AEM Assets as a Cloud Service]

>[!NOTE]
>
>* Le informazioni per questi campi vengono generate durante la configurazione del flusso [!UICONTROL Server-to-server] in [!DNL Adobe Developer Console]. Questi valori si trovano nel file JSON delle credenziali del servizio generato come parte di tale configurazione.
>
>   Per istruzioni sulla configurazione del flusso [!UICONTROL Server-to-server] in [!UICONTROL Adobe Developer Console], vedere [Generazione dei token di accesso per le API lato server](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=it#the-server-to-server-flow).
>
>* L&#39;account tecnico Adobe Experience Manager deve disporre di autorizzazioni di scrittura.
>
>   Per istruzioni sull&#39;aggiunta di autorizzazioni di scrittura all&#39;account tecnico Adobe Experience Manager, vedere [Credenziali di servizio](https://experienceleague.adobe.com/it/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) nella documentazione di Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">[!UICONTROL Nome connessione]</td>
                  <td>
                      <p>Immettere un nome per la connessione.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL URL istanza senza una barra finale]</td>
                  <td>Immettere l'URL per l'istanza [!DNL Adobe Experience Manager]. Non includere una barra <code>/</code> alla fine dell'URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Opzioni di compilazione dettagli account]</td>
                  <td>Seleziona se desideri fornire il codice JSON che descriva i dettagli dell’account o se desideri immettere i dettagli manualmente.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Dettagli account tecnico in formato JSON]</td>
                  <td>Se fornisci JSON, immetti o incolla il JSON che descrive i dettagli dell’account.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID client]</td>
                  <td>Se si immettono i dettagli manualmente, immettere l'ID client generato nell'installazione di [!UICONTROL Server-to-server].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Segreto client]</td>
                  <td>Se si immettono i dettagli manualmente, immettere il segreto client generato nell'installazione di [!UICONTROL Server-to-server].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID account tecnico]</td>
                  <td>Se inserisci i dettagli manualmente, immetti l’ID dell’account tecnico. Campo "[!UICONTROL id]" nel file JSON delle credenziali client.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL ID organizzazione]</td>
                  <td class="">Se inserisci i dettagli manualmente, inserisci l’ID della tua organizzazione. Campo "[!UICONTROL org]" nel file JSON delle credenziali client.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Meta Ambiti]</td>
                  <td>Immettere i metadati generati nella configurazione di [!UICONTROL Server-to-server].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Chiave privata]</td>
                  <td>Immetti la chiave privata generata per vincere l'installazione di [!UICONTROL Server-to-Server]. Per estrarre la chiave privata, fare clic su [!UICONTROL Extract], quindi immettere il file da estrarre e la password per il file.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL URL autenticazione]</td>
                  <td>Immetti l’URL di autenticazione per questo account.</td>
              </tr>
          </tbody>
      </table>


### Configurare la connessione per AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">[!UICONTROL Nome connessione]</td>
                <td>
                    <p>Immettere un nome per la connessione.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL URL istanza senza una barra finale]</td>
                <td>Immettere l'URL per l'istanza [!DNL Adobe Experience Manager]. Non includere una barra <code>/</code> alla fine dell'URL.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Username]</td>
                <td>Immettere il nome utente per l'account [!DNL AEM Assets] utilizzato dalla connessione.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Password]</td>
                <td>Immettere la password per l'account [!DNL AEM Assets] utilizzato dalla connessione.</td>
            </tr>
        </tbody>
    </table>


## [!DNL Adobe Experience Manager Assets] moduli e relativi campi

Quando configuri [!DNL Adobe Experience Manager Essentials] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Experience Manager Essentials], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Copiare una cartella o una risorsa](#copy-a-folder-or-asset)
* [Creare un record](#create-a-record)
* [Eliminare una cartella, una risorsa o una rappresentazione](#delete-a-folder-asset-or-rendition)
* [Ottieni un elenco di cartelle](#get-a-folder-listing)
* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [Spostare una cartella o una risorsa](#move-a-folder-or-asset)
* [Aggiornare un record](#update-a-record)
* [Caricare una risorsa](#upload-an-asset)

### [!UICONTROL Copia cartella o risorsa]

Questo modulo di azione copia una cartella o una risorsa in un’altra posizione nell’account Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri copiare una cartella o una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Assets]</td> 
   <td>Seleziona o mappa la cartella o la risorsa da copiare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso di destinazione]</td> 
   <td>Seleziona o mappa il percorso della nuova cartella o risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome della cartella copiata] / [!UICONTROL risorsa]</td> 
   <td>Immetti un nome per la nuova cartella o risorsa. Il nome della cartella visualizzato in [!DNL Adobe Experience Manager Assets] è uguale al nome originale. Il nome immesso viene visualizzato nell’URL della nuova cartella o risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia elementi figlio]</td> 
   <td>Se copi una cartella, abilita questa opzione per copiare eventuali sottocartelle o risorse all’interno della cartella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Abilita questa opzione per sovrascrivere eventuali cartelle o risorse nella posizione di destinazione con lo stesso nome della cartella o risorsa da copiare.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Crea un record]

Questo modulo di azione crea una cartella o un commento alla risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di oggetto]</td> 
   <td> <p>Seleziona se desideri creare una cartella o un commento su una risorsa.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p>[!UICONTROL Name]</p> <p>Immettere un nome per la cartella. Questo nome verrà visualizzato nel percorso del file, pertanto non deve includere spazi o altri caratteri. </p> </li> 
       <li> <p>[!UICONTROL Title]</p> <p>Immetti un titolo per la cartella, che può essere visualizzato al posto del nome.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Commento risorsa]</p> <p>Compila i campi seguenti:</p> 
      <ul> 
       <li> <p>[!UICONTROL Selezione risorsa]</p> <p>Seleziona o mappa l’ID della risorsa a cui desideri aggiungere un commento.</p> </li> 
       <li> <p>[!UICONTROL Comment]</p> <p>Immettere il testo del commento.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Eliminare una cartella, una risorsa o una rappresentazione]

Questo modulo di azione elimina una cartella, una risorsa o un rendering.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri eliminare una cartella, una risorsa o una rappresentazione.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Seleziona la cartella da eliminare selezionando le cartelle nel relativo percorso.</p> </li> 
     <li> <p>[!UICONTROL Risorsa] </p> <p>Seleziona la risorsa selezionando le cartelle nel suo percorso, quindi la risorsa da eliminare.</p> </li> 
     <li> <p>[!UICONTROL Rendering]</p> <p>Seleziona la rappresentazione selezionando le cartelle nel relativo percorso.</p> <p>Immettere o mappare il nome della rappresentazione.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Ottieni elenco cartelle]

Questo modulo di azione recupera una rappresentazione di una cartella esistente e delle relative entità secondarie (cartelle o risorse).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Seleziona o mappa la cartella da recuperare. Per aggiungere sottocartelle al percorso, fare clic sull'icona più e selezionare la sottocartella.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Effettuare una chiamata API personalizzata]

Questo modulo di azione effettua una chiamata API personalizzata all&#39;API [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo all'URL di base [!DNL Adobe Experience Manager].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query] </td> 
   <td> <p>Immettere la stringa di query richiesta. Per ogni coppia chiave/valore, fare clic su <b>[!UICONTROL Add item]</b> e immettere [!UICONTROL Key] e [!UICONTROL Value].</p> </td> 
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

### [!UICONTROL Spostare una cartella o una risorsa]

Questo modulo di azione sposta la risorsa o la cartella nel percorso specificato in una nuova posizione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri spostare una cartella o una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Assets]</td> 
   <td>Seleziona o mappa la cartella o la risorsa da spostare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso di destinazione]</td> 
   <td>Seleziona o mappa il percorso del percorso in cui desideri spostare la cartella o la risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome della cartella spostata] / [!UICONTROL risorsa]</td> 
   <td>Immetti un nuovo nome per la cartella o la risorsa spostata. Il nome della cartella visualizzato in [!DNL Adobe Experience Manager Assets] è uguale al nome originale. Il nome immesso viene visualizzato nell’URL della cartella o della risorsa spostata.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Abilita questa opzione per sovrascrivere eventuali cartelle o risorse nella posizione di destinazione con lo stesso nome della cartella o risorsa da spostare.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un record esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona se desideri eliminare i metadati di una risorsa o il rendering di una risorsa.</p> 
    <ul> 
     <li> <p>[!UICONTROL Metadati risorsa]</p> 
      <ul> 
       <li> <p>Seleziona la risorsa per la quale desideri aggiornare i metadati.</p> </li> 
       <li> <p>Immetti il nuovo titolo della risorsa.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Rendering risorsa]</p> 
      <ul> 
       <li> <p>Seleziona la risorsa per la quale desideri aggiornare la rappresentazione.</p> </li> 
       <li> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Carica una risorsa]

Questo modulo di azione carica una risorsa sul tuo account [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion], vedere <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Adobe Experience Manager Assets] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination]</td> 
   <td> <p>Seleziona la cartella in cui desideri caricare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Immettere o mappare il nome e i dati del file di origine.</td> 
  </tr> 
 </tbody> 
</table>
