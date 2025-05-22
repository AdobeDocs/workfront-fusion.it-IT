---
title: Moduli Adobe Lightroom
description: Con i moduli di Adobe Lightroom, puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nel tuo account Adobe Lightroom.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 420665071db63954bce14b2011c5ecdb97403fd1
workflow-type: tm+mt
source-wordcount: '3187'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Lightroom] e collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Prima di poter utilizzare il connettore [!DNL Adobe Lightroom], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Lightroom] attivo.
* In Adobe Admin Console deve essere configurata un&#39;app Web OAuth. Per informazioni dettagliate, vedere [Configurare un&#39;applicazione OAuth in Adobe Admin Console](#configure-an-oauth-application-in-the-adobe-admin-console) in questo articolo.

## Informazioni API di Adobe Lightroom

Il connettore Adobe Lightroom utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Creare una connessione ad Adobe Lightroom

Per connetterti ad Adobe Lightroom, devi prima configurare un’app OAuth in Adobe Admin Console. Dopo aver configurato l&#39;app, puoi creare connessioni da Workfront Fusion.

### Configurare un’applicazione OAuth in Adobe Admin Console

1. Inizia la configurazione di un&#39;app Web OAuth in Adobe Admin Console.

   Per istruzioni, consulta [User Authentication Implementation Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation) nella documentazione per gli sviluppatori di Adobe.
1. Durante la configurazione dell&#39;app Web OAuth, immetti i seguenti valori:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Ambiti]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_apis</li>
            <li>openid</li>
            <li>offline_access</li>
            <li>lr_partner_apis</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL URI reindirizzamento]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Schema URI di reindirizzamento]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### Creare una connessione ad Adobe Lightroom da Workfront Fusion

Per creare una connessione per i moduli [!DNL Adobe Lightroom]:

1. In qualsiasi modulo di Adobe Lightroom, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Nome connessione]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Specificare se ci si connette a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## Moduli Adobe Lightroom e relativi campi

Quando configuri [!DNL Adobe Lightroom] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Lightroom], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Altro](#other)
* [Risorse](#assets)
* [Album](#albums)

### Altro

* [Verifica stato](#health-check)
* [Recuperare i metadati del catalogo utente](#retrieve-user-catalog-metadata)

#### Verifica stato

Questo modulo di azione recupera un ID di versione del server Lightroom, verificando se il servizio Lightroom è attualmente in esecuzione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Se si desidera fornire credenziali specifiche per garantire l'esecuzione di un server specifico, fare clic su <b>Aggiungi elemento</b> e immettere le credenziali.</p><p>Le intestazioni di autorizzazione vengono aggiunte automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperare i metadati del catalogo utente

Questo modulo di azione recupera i metadati da un catalogo in Adobe Lightroom. Un catalogo contiene risorse, album o altre risorse.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Se si desidera fornire credenziali specifiche per garantire l'accesso all'account utente corretto, fare clic su Aggiungi elemento e immettere le credenziali.</p><p>Le intestazioni di autorizzazione vengono aggiunte automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

### Risorse

* [Creare un file originale della risorsa](#create-an-asset-original-file)
* [Creare una risorsa](#create-an-asset)
* [Creazione di una risorsa esterna XMP sviluppo file di impostazione](#create-an-asset-external-xmp-develop-setting-file)
* [Generare copie trasformate per un file originale](#generate-renditions-for-an-original-file)
* [Ottieni una risorsa catalogo](#get-a-catalog-asset)
* [Ottieni l’impostazione di sviluppo XMP esterna per la risorsa più recente](#get-the-latest-asset-external-xmp-develop-setting-file)
* [Ottieni la rappresentazione più recente delle risorse](#get-the-latest-asset-rendition)
* [Recuperare le risorse](#retrieve-assets)

#### Creare un file originale della risorsa

Questo modulo di azione crea e carica un file originale per una risorsa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Immetti o mappa l’ID della risorsa per cui desideri creare e caricare un file.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Lunghezza del contenuto in byte]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Intervallo byte]</td>
      <td>
        <p>Immettere o mappare l'intervallo di byte per la richiesta, inclusi il primo e l'ultimo byte e la lunghezza dell'entità come definito nella RFC 2616. Queste informazioni devono essere incluse solo quando i dati sono troppo grandi per essere caricati in una singola chiamata.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di contenuto]</td>
      <td>
        <p>Selezionare il tipo di contenuto per il nuovo file.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Creare una risorsa

Questo modulo di azione crea una nuova risorsa con metadati iniziali e informazioni di importazione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo in cui verrà creata la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa l’ID della nuova risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo risorsa]</td>
      <td>
        <p>Seleziona se la risorsa è un’immagine o un video.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data acquisita]</td>
      <td>
        <p>Immetti o mappa la data di acquisizione della risorsa nel formato <code>YYYY-MM-DDT00:00:00-00:00</code>. Questo verrà impostato dal server se la data acquisita è impostata su <code>0000-00-00T00:00:00</code>. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome file]</td>
      <td>
        <p>Immetti o mappa il nome file della risorsa da importare in Lightroom.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome del dispositivo importato su]</td>
      <td>
        <p>Inserisci o mappa il nome del dispositivo che importa la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID account dell'utente importato]</td>
      <td>
        <p>Inserisci o mappa l’ID dell’utente che importa la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Timestamp di importazione]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Creazione di una risorsa esterna XMP sviluppo file di impostazione

Questo modulo di azione supporta due flussi di lavoro: il caricamento del file delle impostazioni di sviluppo XMP esterno per la risorsa o la creazione di un file delle impostazioni di sviluppo XMP esterno tramite la copia dal file delle impostazioni di sviluppo xmp esterno di un’altra risorsa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Lunghezza contenuto in byte]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Carica nuovo o copia file XMP/di sviluppo]</td>
      <td>
        <p>Seleziona se stai caricando un nuovo file o copiando un file da una risorsa esistente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo in cui desideri creare la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa in cui desideri caricare o copiare un file.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Collega a XMP/file di sviluppo]</td>
      <td>
        <p>Inserisci o mappa un collegamento al file da caricare o copiare.</p><p>Questo file deve essere JSON se si copia un file, o XML se si carica un file.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Generare copie trasformate per un file originale

Questo modulo di azione genera in modo asincrono le rappresentazioni di un file originale.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo/i di rappresentazione (separati da punto e virgola)]</td>
      <td>
        <p>Immettere il tipo di rappresentazione da creare. Se si immettono più tipi, separarli con un punto e virgola (;). <p>Tipi possibili:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Lunghezza del contenuto in byte]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo in cui desideri generare le rappresentazioni.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Immetti o mappa l’ID della risorsa per la quale desideri creare una rappresentazione di un file.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Ottieni una risorsa catalogo

Questo modulo di azione recupera informazioni su una singola risorsa in un catalogo. Il catalogo deve essere di proprietà dell&#39;utente le cui credenziali sono rappresentate nella connessione utilizzata in questo modulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa per la quale desideri recuperare le informazioni.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Ottieni la risorsa più recente dal file delle impostazioni di sviluppo XMP esterno

Questo modulo di azione recupera il file di impostazione XMP esterno della risorsa più recente.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immetti o mappa l’ID del catalogo che contiene la risorsa associata al file delle impostazioni di sviluppo di XMP.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Immetti o mappa l’ID della risorsa associata al file delle impostazioni di sviluppo di XMP.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Ottieni rappresentazione più recente delle risorse

Questo modulo di azione recupera la rappresentazione più recente della risorsa del tipo specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immetti o mappa l’ID del catalogo contenente la risorsa per la quale desideri recuperare una rappresentazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Immetti o mappa l’ID della risorsa per la quale desideri recuperare una rappresentazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Tipo di rappresentazione </td>
      <td>
        <p>Selezionare il tipo di rappresentazione da recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperare le risorse

Questo modulo di azione recupera le risorse di proprietà dell’utente le cui credenziali sono rappresentate nella connessione utilizzata in questo modulo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Timestamp iniziale]</td>
      <td>
        <p>Immetti o mappa un timestamp. Il modulo restituisce i record che sono stati aggiornati dopo questa marca temporale.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Restituisce le risorse acquisite prima dell'ora specificata]</td>
      <td>
        <p>Immettere una data in formato <code>YYYY-MM-DDT00:00:00</code>. Il modulo restituisce i risultati acquisiti prima di questa data.</p><p> Questo campo non può essere utilizzato con il campo <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Restituisci risorse acquisite dopo il tempo specificato]</td>
      <td>
        <p>Immettere una data in formato <code>YYYY-MM-DDT00:00:00</code>. Il modulo restituisce i risultati acquisiti prima di questa data.</p><p> Questo campo non può essere utilizzato con il campo <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di risorse restituite]</td>
      <td>
        <p>Immettere il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Valore hash del file originale]</td>
      <td>
        <p>Immetti o mappa il valore hash del file originale. Viene restituito Assets con un hash corrispondente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nascondi le risorse che si trovano all'interno di pile?"]</td>
      <td>
        <p>Selezionate Sì per nascondere le risorse all'interno delle pile (le risorse all'interno delle pile non vengono restituite). Seleziona No per includere nei risultati le risorse all’interno delle pile.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Valori sottotipo risorsa]</td>
      <td>
        <p>Immettere o mappare un elenco separato da punto e virgola dei valori dei sottotipi da restituire.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa fino a 100 ID di risorse, separati da virgole.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipi di risorse da escludere]</td>
      <td>
        <p>Seleziona questa opzione per escludere le risorse complete o incomplete. Per includere tutte le risorse, lascia vuoto questo campo.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Valori gruppo]</td>
      <td>
        <p>Immettere o mappare un elenco di valori di gruppo separati da punto e virgola.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p>Immettere o mappare un elenco di valori nome separati da punto e virgola.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stato preferito]</td>
      <td>
        <p>Immetti o mappa lo stato preferito per il quale desideri restituire i risultati.</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

### Album

* [Aggiungere risorse a un album](#add-assets-to-an-album)
* [Creare un album](#create-an-album)
* [Eliminare un album](#delete-an-album)
* [Ottieni un album](#get-an-album)
* [Elencare le risorse di un album](#list-assets-of-an-album)
* [Recupera album](#retrieve-albums)
* [Aggiornare un album](#update-album)

#### Aggiungere risorse a un album

Questo modulo di azione aggiunge una o più risorse all’album specificato. Puoi aggiungere fino a 50 risorse in un ciclo di esecuzione.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo contenente l’album a cui desideri aggiungere le risorse.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Inserisci o mappa l’ID dell’album a cui desideri aggiungere le risorse.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>Per ogni risorsa da aggiungere all'album, fare clic su <b>Aggiungi elemento</b> e immettere i campi seguenti.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa da aggiungere all’album</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL La risorsa è una copertina per album?]</td>
      <td>
        <p>Seleziona se desideri che questa risorsa venga visualizzata come immagine che rappresenta l'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p>Specifica l’ordine della risorsa.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Immetti o mappa i metadati che desideri includere nella risorsa. Deve essere una singola stringa di testo con una lunghezza massima di 1-24 caratteri.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID remoto]</td>
      <td>
        <p>Immetti un identificatore per la risorsa.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Creare un album

Questo modulo di azione crea un nuovo album in Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo in cui si desidera creare un album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Immettere o mappare un ID per il nuovo album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Sottotipo </td>
      <td>
        <p>Selezionare il sottotipo dell'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID servizio]</td>
      <td>
        <p>Immettere la chiave API del servizio che sta creando l'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Data creazione utente]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data aggiornamento utente]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome Album]</td>
      <td>
        <p>Immettere o mappare un nome per il nuovo album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID copertina]</td>
      <td>
        <p>Inserisci o mappa l’ID di una risorsa da utilizzare come copertina dell’album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">ID padre </td>
      <td>
        <p>Immettere o mappare l'ID dell'elemento padre per l'album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Immettete o mappate i metadati dell'album come stringa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID remoto]</td>
      <td>
        <p>Immetti un identificatore per la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data di creazione]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Data di aggiornamento]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL L'album è stato eliminato?]</td>
      <td>
        <p>Abilita questa opzione se il contenuto affiliato esternamente è stato eliminato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL della posizione in cui modificare il contenuto affiliato]</td>
      <td>
        <p>Se è presente un URL in cui gli utenti possono modificare il contenuto dell'album, immettere l'URL qui.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL della posizione per visualizzare il contenuto affiliato]</td>
      <td>
        <p>Se è presente un URL in cui gli utenti possono visualizzare il contenuto dell'album, immettere l'URL qui.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Eliminare un album

Questo modulo di azione elimina un album.

L&#39;album eliminato deve essere stato creato dalla stessa app client che lo sta eliminando e deve essere di sottotipo `project` o `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Eliminare gli album secondari?]</td>
      <td>
        <p>Selezionare se si desidera eliminare gli album secondari dell'album eliminato.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ottieni un album

Questo modulo di azione recupera l&#39;album specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Elencare le risorse di un album

Questo modulo di azione recupera un elenco di risorse nell’album specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo che contiene l'album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Inserisci o mappa l’ID dell’album per il quale desideri elencare le risorse.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Acquisisci Assets prima dell'ora]</td>
      <td>
        <p>Immettere una data in formato <code>YYYY-MM-DDT00:00:00</code>. Il modulo restituisce i risultati acquisiti prima di questa data.</p><p> Questo campo non può essere utilizzato con il campo <code>Return assets captured after given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Acquisisci Assets Dopo Il Tempo]</td>
      <td>
        <p>Immettere una data in formato <code>YYYY-MM-DDT00:00:00</code>. Il modulo restituisce i risultati acquisiti prima di questa data.</p><p> Questo campo non può essere utilizzato con il campo <code>Return assets captured before given time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL - Valore ordine cespite finale]</td>
      <td>
        <p>Immettere o mappare il valore dell'ordine del cespite finale.</p><p> Questo campo può essere utilizzato solo con il campo <code>Capture Assets After Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Valore ordine risorse iniziale]</td>
      <td>
        <p>Immettere o mappare il valore dell'ordine del cespite iniziale.</p><p> Questo campo può essere utilizzato solo con il campo <code>Capture Assets BEfore Time</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero di Assets da restituire (1-500)]</td>
      <td>
        <p>Immettere il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. Questo numero deve essere compreso tra 1 e 500.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nascondi le risorse che si trovano all'interno di pile?"]</td>
      <td>
        <p>Selezionate Sì per nascondere le risorse all'interno delle pile (le risorse all'interno delle pile non vengono restituite). Seleziona No per includere nei risultati le risorse all’interno delle pile.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype Values (separati da punto e virgola)]</td>
      <td>
        <p>Immettere o mappare un elenco separato da punto e virgola dei valori dei sottotipi da restituire.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Flag Values (separati da punto e virgola)]</td>
      <td>
        <p>Immettere o mappare un elenco di valori dei flag separati da punto e virgola da restituire.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Campi dati aggiuntivi da includere (separati da punto e virgola)]</td>
      <td>
        <p>Se la risorsa è inclusa, vengono inclusi tutti i campi; in caso contrario, vengono restituiti solo l’ID e il collegamento href autonomo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipi di risorse da escludere]</td>
      <td>
        <p>Seleziona questa opzione per escludere le risorse complete o incomplete. Per includere tutte le risorse, lascia vuoto questo campo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID risorsa]</td>
      <td>
        <p>Inserisci o mappa fino a 100 ID di risorse, separati da virgole.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Escludi risorse album in base ai filtri di presentazione]</td>
      <td>
        <p>Quando questo campo è impostato su "true", tutte le risorse dell'album vengono escluse in base ai filtri di presentazione impostati sull'album. Con questo parametro, le risorse rifiutate vengono sempre filtrate, a prescindere dalle impostazioni nei filtri di presentazione. I filtri di presentazione non vengono applicati quando per album_filters è impostato un valore diverso da "true". Il comportamento predefinito consiste nel visualizzare tutte le risorse. Questo parametro non può essere utilizzato insieme al parametro flag. </p>
      </td>
    </tr>
  </tbody>
</table>

#### Recupera album

Questo modulo di azione recupera un elenco di album nel catalogo specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente gli album che si desidera recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sottotipi]</td>
      <td>
        <p>Immettere o mappare un elenco separato da punto e virgola dei valori dei sottotipi da restituire.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome dell'album da anteporre ai risultati correnti]</td>
      <td>
        <p>Se si sta impaginando i risultati, immettere o mappare il nome dell'ultimo album nella pagina precedente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero di album da restituire]</td>
      <td>
        <p>Impostare il numero massimo di risorse che [!DNL Workfront Fusion] restituirà durante un ciclo di esecuzione. Il valore predefinito per questo campo è 100. Questo modulo può restituire più album oltre questo limite se più album al limite del limite hanno lo stesso valore <code>name_after</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Aggiorna album

Questo modulo di azione aggiorna l&#39;album specificato.

L&#39;album aggiornato deve essere stato creato dalla stessa app client che lo sta aggiornando e deve essere di sottotipo `project` o `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID catalogo]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera aggiornare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID album]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera aggiornare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
      <td>
      <td>Per le descrizioni di altri campi di questo modulo, vedere <a href="#create-an-album" class="MCXref xref" >Creare un album</a> in questo articolo.</td>
      </td>
    </tr>
  </tbody>
</table>
