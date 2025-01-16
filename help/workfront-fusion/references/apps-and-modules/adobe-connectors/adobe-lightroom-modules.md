---
title: Moduli Adobe Lightroom
description: Con i moduli di Adobe Lightroom, puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nel tuo account Adobe Lightroom.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2025'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Lightroom] e collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
      <td>
        <p>[!UICONTROL Pro] o superiore</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td>
      <td >
        <p>[!UICONTROL Workfront Fusion for Work Automation and Integration]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Prodotto</td>
      <td>La tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42;Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore [!DNL Workfront].

&#42;&#42;Per informazioni sulle licenze [!DNL Adobe Workfront Fusion], vedere [!DNL [Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Prima di poter utilizzare il connettore [!DNL Adobe Lightroom], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Lightroom] attivo.

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

Per creare una connessione per i moduli [!DNL Adobe Lightroom]:

1. Fare clic su **[!UICONTROL Add]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
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
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL Client ID]. È disponibile nella sezione dei dettagli [!UICONTROL Credentials] della sezione [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione dei dettagli [!UICONTROL Credentials] della sezione [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.




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
        <p>Se si desidera fornire credenziali specifiche per garantire l'esecuzione di un server specifico, fare clic su Aggiungi elemento e immettere le credenziali.</p><p>Le intestazioni di autorizzazione vengono aggiunte automaticamente.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Recuperare i metadati del catalogo utente

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

* [Creare un file originale della risorsa](#create-an-asset-external-xmp-develop-setting-file)
* [Creare una risorsa](#create-an-asset)
* [Creare una risorsa esterna XMP sviluppare un file di impostazione](#create-an-asset-external-xmp-develop-setting-file)
* [Generare copie trasformate per un file originale](#generate-renditions-for-an-original-file)
* [Ottieni una risorsa catalogo](#get-a-catalog-asset)
* [Ottieni l’impostazione di sviluppo XMP esterna più recente per le risorse](#get-the-latest-asset-external-xmp-develop-setting-file)
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Immetti o mappa l’ID della risorsa per cui desideri creare e caricare un file.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Byte range]</td>
      <td>
        <p>Immettere o mappare l'intervallo di byte per la richiesta, inclusi il primo e l'ultimo byte e la lunghezza dell'entità come definito nella RFC 2616. Deve essere incluso solo quando i dati sono troppo grandi per essere caricati in una singola chiamata.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content type]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo in cui verrà creata la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della nuova risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset type]</td>
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
      <td role="rowheader">[!UICONTROL Date captured]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Creare una risorsa esterna XMP sviluppare un file di impostazione

Questo modulo di azione supporta due flussi di lavoro. Il primo flusso di lavoro consiste nel caricare il file delle impostazioni di sviluppo XMP esterno per la risorsa. Il secondo flusso di lavoro consiste nel creare un file delle impostazioni di sviluppo XMP esterno copiando dal file delle impostazioni di sviluppo xmp esterno di un’altra risorsa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Upload new or copy XMP/develop file]</td>
      <td>
        <p>Seleziona se stai caricando un nuovo file o copiando un file da una risorsa esistente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa in cui desideri caricare o copiare un file.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Link to XMP/develop file]</td>
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
      <td role="rowheader">[!UICONTROL Rendition Type(s) (semi-colon separated)]</td>
      <td>
        <p>Immettere il tipo di rappresentazione da creare. Se si immettono più tipi, separarli con un punto e virgola (;). <p>Tipi possibili:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Immettere o mappare la lunghezza del contenuto in byte.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa per la quale desideri recuperare le informazioni.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Ottieni il file di impostazione per lo sviluppo XMP esterno più recente per la risorsa

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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa associata al file delle impostazioni per lo sviluppo dell’XMP.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Ottieni la rappresentazione più recente delle risorse

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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa associata al file delle impostazioni per lo sviluppo dell’XMP.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition type]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo che contiene la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting timestamp]</td>
      <td>
        <p>Immetti o mappa un timestamp. Il modulo restituisce i record che sono stati aggiornati dopo questa marca temporale.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured before]</td>
      <td>
        <p>Immettere una data in formato <code>YYYY-MM-DDT00:00:00</code>. Il modulo restituisce i risultati acquisiti prima di questa data.</p><p> Questo campo non può essere utilizzato con il campo <code>Return assets captured after</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned assets]</td>
      <td>
        <p>Impostare il numero massimo di risorse che [!DNL Workfront Fusion] restituirà durante un ciclo di esecuzione. Questo numero deve essere minore o uguale a 100.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Hash value of original file]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Inserisci o mappa fino a 100 ID di risorse, separati da virgole.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Seleziona questa opzione per escludere le risorse complete o incomplete. Per includere tutte le risorse, lascia vuoto questo campo.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Group values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favorite status]</td>
      <td>
        <p></p>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del catalogo contenente l’album a cui desideri aggiungere le risorse.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
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
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Inserisci o mappa l’ID della risorsa da aggiungere all’album</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Is this asset an album cover?]</td>
      <td>
        <p>Seleziona se desideri che questa risorsa venga visualizzata come immagine che rappresenta l'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p></p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Metadata]</td>
      <td>
        <p>Immetti o mappa i metadati che desideri includere nella risorsa. Deve essere una singola stringa di testo con una lunghezza massima di 1-24 caratteri.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo in cui si desidera creare un album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Immettere o mappare un ID per il nuovo album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>Selezionare il sottotipo dell'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL API key]</td>
      <td>
        <p>Immettere la chiave API del servizio che sta creando l'album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album name]</td>
      <td>
        <p>Immettere o mappare un nome per il nuovo album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Inserisci o mappa l’ID di una risorsa da utilizzare come copertina dell’album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Immetti un identificatore per la risorsa.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Created date]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Updated date]</td>
      <td>
        <p>Immettere o mappare una data con il formato <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Is the album deleted?]</td>
      <td>
        <p>Abilita questa opzione se il contenuto affiliato esternamente è stato eliminato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to edit affiliated content]</td>
      <td>
        <p>Se è presente un URL in cui gli utenti possono modificare il contenuto dell'album, immettere l'URL qui.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to view affiliated content]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Delete child albums?]</td>
      <td>
        <p>Selezionare se si desidera eliminare gli album secondari dell'album eliminato.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ottieni un album

Questo modulo di azione recupera l&#39;album specificato

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Lightroom], vedere <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Creare una connessione a [!DNL Adobe Lightroom]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Elencare le risorse di un album

Questo modulo di azione recupera un elenco di risorse nell’album specificato.



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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente gli album che si desidera recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>Immettere o mappare l'ID dell'album che si desidera recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of album to precede current results]</td>
      <td>
        <p>Se si sta impaginando i risultati, immettere o mappare il nome dell'ultimo album nella pagina precedente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned albums]</td>
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
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Immettere o mappare l'ID del catalogo contenente l'album che si desidera aggiornare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
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