---
title: Moduli Adobe Photoshop
description: Con i moduli di Adobe Photoshop, puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell’account Adobe Photoshop, creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: 95d52f8227c8a40c0db165eea9d2877e60446de9
workflow-type: tm+mt
source-wordcount: '5392'
ht-degree: 0%

---

# [!DNL Adobe Photoshop] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Photoshop] e collegarlo a più applicazioni e servizi di terze parti.


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

## Prerequisiti

Prima di poter utilizzare il connettore [!DNL Adobe Photoshop], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Photoshop] attivo.
* È necessario disporre di una licenza Firefly Services.
* È necessario disporre di un ID client e di un segreto client. Puoi acquistarli da Adobe Developer Console.

## Informazioni API di Adobe Photoshop

Il connettore Adobe Photoshop utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Crea una connessione a [!DNL Adobe Photoshop]

Per creare una connessione per i moduli [!DNL Adobe Photoshop]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo di connessione]</td>
        <td>
          <p>Seleziona se desideri utilizzare una connessione JWT o una connessione server-to-server.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Nome connessione]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID account tecnico]</td>
        <td>Se utilizzi una connessione JWT, immetti l’ID dell’account tecnico [!DNL Adobe] [!UICONTROL]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID organizzazione]</td>
        <td>Se utilizzi una connessione JWT, immetti l'ID organizzazione [!DNL Adobe] [!UICONTROL]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Chiave privata]</td>
        <td>
          <p>Se utilizzi una connessione JWT, immetti la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
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
              <p>Fai clic su <b>Salva</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## [!DNL Adobe Photoshop] moduli e relativi campi

Quando si configurano [!DNL Adobe Photoshop] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Photoshop], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Applicare le modifiche PSD](#apply-psd-edits)
* [Correzione automatica del colore di un&#39;immagine](#auto-color-correct-an-image)
* [Converti formato immagine](#convert-image-format)
* [Creare una maschera](#create-a-mask)
* [Crea un nuovo PSD](#create-a-new-psd)
* [Modificare i livelli di testo](#edit-text-layers)
* [Modifica livelli di testo (legacy)](#edit-text-layers-legacy)
* [Esegui un’azione JSON](#execute-an-action-json)
* [Esegui sfocatura profondità](#execute-depth-blur)
* [Eseguire azioni Photoshop](#execute-photoshop-actions)
* [Esegui ritaglio prodotto](#execute-product-crop)
* [Ottieni informazioni livello](#get-layer-info)
* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [Rimuovi sfondo](#remove-background)
* [Sostituire un oggetto avanzato](#replace-a-smart-object)
* [Sostituire un oggetto avanzato (legacy)](#replace-a-smart-object-legacy)
* [Ridimensionare un’immagine](#resize-an-image)
* [Filigrana di un’immagine](#watermark-an-image)

### Applicare le modifiche PSD

Questo modulo di azione applica una serie di modifiche a livello di documento e di livello.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni immagine) Altezza]</p>
      </td>
      <td> Immettete o mappate l'altezza dell'immagine in pixel. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni immagine) Larghezza]</p>
      </td>
      <td> Immettete o mappate la larghezza dell'immagine in pixel. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni area di lavoro) In alto]</p>
      </td>
   <td> Immettere o mappare, in pixel, la coordinata y dell'angolo superiore sinistro del documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni area di lavoro) Inferiore]</p>
      </td>
   <td> Immettere o mappare, in pixel, la coordinata y dell'angolo inferiore destro del documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni area di lavoro) A sinistra]</p>
      </td>
   <td> Immettere o mappare, in pixel, la coordinata x dell'angolo superiore sinistro del documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni area di lavoro) a destra]</p>
      </td>
   <td> Immettere o mappare, in pixel, la coordinata x dell'angolo inferiore destro del documento. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento) Rifila]</p>
      </td>
   <td> Selezionate Pixel trasparenti (Transparent pixels) per basare il ritaglio su pixel trasparenti nell'immagine. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Carattere predefinito]</p>
      </td>
   <td> Immettere il nome postscript completo del tipo di carattere da utilizzare come predefinito globale per il documento. Questo tipo di carattere verrà utilizzato per qualsiasi livello di testo con un tipo di carattere mancante e nessun altro tipo di carattere è stato specificato per tale livello. Se questo tipo di carattere non è presente, verrà applicata l'opzione specificata in Gestione tipi di carattere mancanti. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Caratteri]</p>
      </td>
   <td> Per ogni tipo di carattere necessario per il documento, fare clic su Aggiungi elemento e immettere la posizione di memorizzazione e il percorso del file del tipo di carattere. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Gestisci tipi di carattere mancanti]</p>
      </td>
   <td> Selezionare l'azione da eseguire se nel documento mancano uno o più tipi di carattere. <ul><li><code>fail</code>: il processo non verrà eseguito correttamente e lo stato verrà impostato su Non riuscito con i dettagli dell’errore forniti nella sezione dei dettagli dello stato.</li><li><code>useDefault</code>: il processo avrà esito positivo e tutti i font mancanti verranno sostituiti con ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Livelli]</p>
      </td>
   <td> Per ogni livello che desiderate aggiungere, fate clic su Aggiungi elemento (Add item) e inserite i dettagli del livello. <p>Per informazioni dettagliate sulle opzioni dei livelli, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync">Applica modifiche PSD</a> nella documentazione di Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file modificato che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati nella tabella.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selezionare il tipo di file in cui convertire il file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (output) Rifila su area di lavoro]</p>
      </td>
   <td>Seleziona se le rappresentazioni devono essere di dimensioni Canvas. Se ha valore True, le rappresentazioni verranno ridotte alle dimensioni dell'area di lavoro, mentre se ha valore False le dimensioni del livello delle rappresentazioni verranno ridotte</td> 
    </tr>
    </tbody>
</table>

### Correzione automatica del colore di un&#39;immagine

Il colore automatico di questo modulo di azione corregge l’immagine specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da correggere.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file di cui desideri correggere il colore. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selezionare il tipo di file in cui convertire il file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

### Converti formato immagine

Questo modulo di azione converte un file in JPEG, PNG, PSD o TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da cui si desidera rimuovere lo sfondo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso del file da cui si desidera rimuovere lo sfondo. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file convertito che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati nella tabella.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selezionare il tipo di file in cui convertire il file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

### Creare una maschera

Questo modulo di azione restituisce un file PNG con una maschera applicata attorno all&#39;oggetto.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da cui si desidera creare una maschera.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso del file da cui desideri creare una maschera. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file di maschera.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file della maschera. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Spazio colore]</p>
      </td>
   <td>Seleziona se l'immagine di output utilizza il colore RGB o RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato maschera]</p>
      </td>
   <td>Seleziona se la maschera deve essere morbida (sfumata) o binaria. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ottimizza]</p>
      </td>
   <td>Selezionare Prestazioni per ottimizzare la velocità oppure Batch per consentire il tempo di attesa. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Seleziona se abilitare la post-elaborazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL versione]</p>
      </td>
   <td>Il valore predefinito è 4,0</td> 
    </tr> 
    </tbody>
</table>

### Crea un nuovo PSD

Questo modulo di azione crea un nuovo PSD con livelli opzionali e genera rappresentazioni o salvataggi come PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni immagine) Altezza]</p>
      </td>
      <td> Immettete o mappate l'altezza dell'immagine in pixel. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento &gt; Dimensioni immagine) Larghezza]</p>
      </td>
      <td> Immettete o mappate la larghezza dell'immagine in pixel. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Risoluzione [!UICONTROL (Opzioni &gt; Documento)]</p>
      </td>
   <td> Immettete o mappate la risoluzione dell'immagine in pixel per pollice. Deve essere compreso tra 72 e 300. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Modalità [!UICONTROL (Opzioni &gt; Documento)]</p>
      </td>
   <td> Seleziona la modalità per l’immagine. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni &gt; Documento) Riempimento]</p>
      </td>
   <td> Selezionate se desiderate che il riempimento per il livello di sfondo sia trasparente, bianco o il colore di sfondo dell'immagine. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Profondità [!UICONTROL (Opzioni &gt; Documento)]</p>
      </td>
   <td> Selezionate la profondità di bit dell'immagine. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Livelli]</p>
      </td>
   <td> Per ogni livello che desiderate aggiungere, fate clic su Aggiungi elemento (Add item) e inserite i dettagli del livello. <p>Per informazioni dettagliate sulle opzioni dei livelli, vedi <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Creare PSD</a> nella documentazione di Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Carattere globale]</p>
      </td>
   <td> Immettere il nome postscript completo del tipo di carattere da utilizzare come predefinito globale per il documento. Questo tipo di carattere verrà utilizzato per qualsiasi livello di testo con un tipo di carattere mancante e nessun altro tipo di carattere è stato specificato per tale livello. Se questo tipo di carattere non è presente, verrà applicata l'opzione specificata in Gestione tipi di carattere mancanti. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Caratteri]</p>
      </td>
   <td> Per ogni tipo di carattere necessario per il documento, fare clic su Aggiungi elemento e immettere la posizione di memorizzazione e il percorso del file del tipo di carattere. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Gestisci tipi di carattere mancanti]</p>
      </td>
   <td> Selezionare l'azione da eseguire se nel documento mancano uno o più tipi di carattere. <ul><li><code>fail</code>: il processo non verrà eseguito correttamente e lo stato verrà impostato su Non riuscito con i dettagli dell’errore forniti nella sezione dei dettagli dello stato.</li><li><code>useDefault</code>: il processo avrà esito positivo e tutti i font mancanti verranno sostituiti con ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati nella tabella.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selezionare il tipo di file in cui convertire il file. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Altri campi]</td>
      <td>
        <p><p>Per informazioni dettagliate sulle opzioni di output, vedere <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">Creare PSD</a> nella documentazione di Adobe Photoshop.  </p>
      </td>
    </tr>
    </tbody>
</table>

### Modificare i livelli di testo

Questo modulo di azione modifica i livelli di testo in un file Photoshop. Potete immettere dettagli di modifica separati per più livelli nello stesso file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gestisci tipi di carattere mancanti]</td>
      <td>
        <p>Selezionare l'azione da eseguire se nel documento mancano uno o più tipi di carattere. Se il font non viene fornito, il modulo utilizza il font predefinito.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Immettere il nome postscript completo del tipo di carattere da utilizzare come predefinito globale per il documento. Questo tipo di carattere verrà utilizzato per qualsiasi livello di testo con un tipo di carattere mancante e nessun altro tipo di carattere è stato specificato per tale livello. Se questo tipo di carattere non è presente, verrà applicata l'opzione specificata in Gestione tipi di carattere mancanti.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Caratteri]</p>
      </td>
   <td> Immettere la posizione di memorizzazione e la posizione del file del carattere. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Livelli]</td>
   <td> <p>Per ogni livello di testo che si desidera modificare, fare clic su <b>Aggiungi elemento</b> e immettere le opzioni di livello.<p>Per informazioni dettagliate sulle opzioni dei livelli, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Modifica testo</a> nella documentazione di Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
  </tbody>
</table>

### Modifica livelli di testo (legacy)

Questo modulo di azione modifica un livello di testo su un file Photoshop.

Per modificare più livelli, utilizzare il modulo [Modifica livelli di testo](#edit-text-layers).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gestisci tipi di carattere mancanti]</td>
      <td>
        <p>Selezionare l'azione da eseguire se nel documento mancano uno o più tipi di carattere. Se il font non viene fornito, il modulo utilizza il font predefinito.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Immettere il nome postscript completo del tipo di carattere da utilizzare come predefinito globale per il documento. Questo tipo di carattere verrà utilizzato per qualsiasi livello di testo con un tipo di carattere mancante e nessun altro tipo di carattere è stato specificato per tale livello. Se questo tipo di carattere non è presente, verrà applicata l'opzione specificata in Gestione tipi di carattere mancanti.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Opzioni) Caratteri]</p>
      </td>
   <td> Immettere la posizione di memorizzazione e la posizione del file del carattere. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Livelli]</td>
   <td> <p>Per informazioni dettagliate sulle opzioni dei livelli, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">Modifica livello testo</a> nella documentazione di Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">Archiviazione file di output di [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
  </tbody>
</table>


### Esegui un’azione JSON

Questo modulo di azione esegue azioni Photoshop utilizzando comandi JSON.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action JSON]</td>
      <td>
        <p>Immetti il comando JSON per l’azione da eseguire.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipi di carattere / Motivi / Pennelli / Immagini aggiuntive]</td>
      <td>
        <p>Per ogni tipo di carattere, motivo, pennello o immagine aggiuntiva che si desidera utilizzare in questa azione, fare clic su Aggiungi elemento e immettere la posizione di archiviazione e file dell'elemento.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / URL file pennello]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso del file che desideri utilizzare. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file che si desidera creare, fare clic su Aggiungi elemento e immettere l'opzione di archiviazione, posizione, tipo e sovrascrittura indicata nella tabella.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File URL]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
      </tbody>
</table>

### Esegui sfocatura profondità

Questo modulo di azione esegue Sfocatura profondità sul file selezionato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File URL]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Altri campi]</td>
      <td>
        <p>Per informazioni dettagliate su altre opzioni di Sfocatura profondità, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Eseguire Sfocatura profondità </a> nella documentazione dell'API di Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Esegui azioni Photoshop

Questo modulo di azione esegue un’azione Photoshop sull’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera modificare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso del file da modificare. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Archiviazione file azioni]</td>
      <td>
        <p>Selezionare il file service in cui è memorizzato il file di azioni.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file azioni]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso del file delle azioni. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome azione]</p>
      </td>
   <td> Se si desidera eseguire solo una determinata azione, è possibile specificare l'azione da eseguire dal set di azioni. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Font / Pattern / Archiviazione pennello]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file che si desidera utilizzare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / URL file pennello]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso del file che desideri utilizzare. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File URL]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Altri campi]</td>
      <td>
        <p>Per informazioni dettagliate su altre opzioni di Sfocatura profondità, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Eseguire Sfocatura profondità </a> nella documentazione dell'API di Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Esegui ritaglio prodotto

Questo modulo di azione esegue il ritaglio prodotto sull’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da ritagliare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso del file da ritagliare. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unit]</p>
      </td>
   <td> Selezionate se desiderate descrivere la regolazione di altezza e larghezza in pixel o come percentuale. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Immettete o mappate la spaziatura che desiderate aggiungere. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Height]</p>
      </td>
   <td> Immettete o mappate la quantità di spazio per l'altezza che desiderate aggiungere. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file modificato.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File URL]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il file modificato.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Altri campi]</td>
      <td>
        <p>Per informazioni dettagliate su altre opzioni di Sfocatura profondità, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">Eseguire Sfocatura profondità </a> nella documentazione dell'API di Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ottieni informazioni livello

Questo modulo di azione recupera le informazioni sui livelli dal file PSD specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input [!UICONTROL]</td>
      <td>
        <p>Selezionate il servizio file da cui memorizzare il file da cui desiderate recuperare le informazioni sui livelli.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL file di input]</p>
      </td>
   <td> Immettete o mappate l'URL o il percorso del file da cui desiderate recuperare le informazioni sui livelli. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL miniature]</p>
      </td>
   <td> Selezionare il tipo di file che si desidera vengano visualizzate le miniature. Le miniature sono anteprime di piccole dimensioni per qualsiasi livello renderizzabile.</td> 
    </tr>
  </tbody>
</table>

### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Immettere un percorso relativo a <code>https://image.adobe.io/pie/psdService</code>. Esempio: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
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
      <td role="rowheader">[!UICONTROL Stringa Di Query]  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Rimuovi sfondo

Questo modulo di azione identifica il soggetto principale dell&#39;immagine e rimuove lo sfondo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da cui si desidera rimuovere lo sfondo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso del file da cui si desidera rimuovere lo sfondo. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Spazio colore]</p>
      </td>
   <td>Seleziona se l'immagine di output utilizza il colore RGB o RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Formato maschera]</p>
      </td>
   <td>Seleziona se i bordi dell'immagine devono essere morbidi (sfumati) o binari. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ottimizza]</p>
      </td>
   <td>Selezionare Prestazioni per ottimizzare la velocità oppure Batch per consentire il tempo di attesa. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Seleziona se abilitare la post-elaborazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL versione]</p>
      </td>
   <td>Il valore predefinito è 4,0</td> 
    </tr> 
    </tbody>
</table>

### Sostituire un oggetto avanzato

Questo modulo di azione sostituisce un oggetto avanzato all’interno di un livello PSD e genera nuove rappresentazioni.

Questo modulo utilizza Smart Object API versione 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato l'oggetto avanzato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso dell'oggetto avanzato. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Livelli]</p>
      </td>
   <td>Per ogni livello che si desidera aggiungere all'oggetto avanzato, fare clic su Aggiungi elemento e immettere il nome o l'ID dell'oggetto, il servizio file in cui è memorizzato l'oggetto avanzato e l'URL o il percorso del livello.<p>Per le descrizioni delle impostazioni avanzate in quest'area, vedere <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Sostituire un oggetto avanzato</a> nella documentazione dell'API di Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Ridimensiona immagine durante il posizionamento]</p>
      </td>
   <td> Seleziona se desideri ridimensionare l'immagine.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni nuova copia trasformata che si desidera venga prodotta dal modulo, fare clic su Aggiungi elemento e compilare i campi seguenti. Puoi avere un massimo di 25 file di output.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selezionare il tipo di file per il file modificato. </td> 
    </tr>
     </tbody>
</table>

### Sostituire un oggetto avanzato (legacy)

Questo modulo di azione sostituisce un oggetto avanzato all’interno di un livello PSD e genera nuove rappresentazioni.

Questo modulo utilizza la versione legacy di Smart Objects.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato l'oggetto avanzato.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Input)]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso dell'oggetto avanzato. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Livelli]</p>
      </td>
   <td>Per ogni livello che si desidera aggiungere all'oggetto avanzato, fare clic su Aggiungi elemento e immettere il nome o l'ID dell'oggetto, il servizio file in cui è memorizzato l'oggetto avanzato e l'URL o il percorso del livello.<p>Per le descrizioni delle impostazioni avanzate in quest'area, vedere <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">Sostituire un oggetto avanzato</a> nella documentazione dell'API di Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni nuova copia trasformata che si desidera venga prodotta dal modulo, fare clic su Aggiungi elemento e compilare i campi seguenti. Puoi avere un massimo di 25 file di output.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> Larghezza in pixel del file di output. Il modulo mantiene le proporzioni originali. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tbody>
</table>

### Ridimensionare un’immagine

Questa azione ridimensiona un’immagine utilizzando le stesse proporzioni.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file da ridimensionare.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Percorso file]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso del file da ridimensionare.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file convertito che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e le altre opzioni elencate in questa tabella.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il nuovo file.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Percorso file]</p>
      </td>
   <td> Inserisci o mappa l’URL o il percorso in cui verrà memorizzato il nuovo file.  Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Larghezza in pixel del file di output. Il modulo mantiene le proporzioni originali. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Larghezza massima]</p>
      </td>
   <td>Quando la larghezza è 0, è possibile fornire il valore Max con per ottenere le dimensioni. La larghezza massima ha la precedenza e è inferiore alla larghezza del documento.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Rifila nell'area di lavoro]</p>
      </td>
   <td>Selezionare Sì per rifilare le rappresentazioni alle dimensioni dell'area di lavoro oppure No per creare le rappresentazioni Dimensione livello.</td> 
    </tr>
    </tbody>
</table>

### Filigrana di un’immagine

Questo modulo di azione aggiunge una filigrana all’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], vedere <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Base &gt; Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzato il file a cui si desidera aggiungere una filigrana.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Base &gt; Input)]</p>
      </td>
   <td> Immettere o mappare l'URL o il percorso del file a cui si desidera aggiungere una filigrana. </td> 
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Filigrana &gt; Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzata la filigrana che si desidera aggiungere.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Filigrana &gt; Input)]</td>
      <td>
        <p>Selezionare il servizio file in cui è memorizzata la filigrana che si desidera aggiungere.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrana &gt; Limiti) Altezza]</p>
      </td>
   <td>Immettete o mappate l'altezza desiderata della filigrana in pixel.</td> 
    <tr>
      <td role="rowheader">
        <p>Larghezza [!UICONTROL (Filigrana &gt; Limiti)]</p>
      </td>
   <td> Immettere o mappare la larghezza desiderata della filigrana in pixel. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrana &gt; Limiti) Sinistra]</p>
      </td>
   <td> Immettete o mappate la distanza in pixel dal lato sinistro dell'immagine da applicare alla filigrana.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrana &gt; Limiti) superiore]</p>
      </td>
   <td> Immettete o mappate la distanza in pixel dalla parte superiore dell'immagine da applicare alla filigrana.</td> 
    </tr>  
    <tr>
      <td role="rowheader">Archiviazione [!UICONTROL (Output)]</td>
      <td>
        <p>Selezionare il servizio file in cui si desidera memorizzare il file con filigrana.</p><p>Selezionando l'archiviazione interna di Fusion, il file diventa disponibile per i moduli successivi, ma non al di fuori dello scenario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Percorso file [!UICONTROL (Output)]</p>
      </td>
   <td> Immetti o mappa l’URL o il percorso in cui verrà memorizzato il file con filigrana. Questa operazione è necessaria solo se per l'archiviazione di output non è stata scelta l'archiviazione interna Fusion.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selezionare il tipo di file in cui convertire il file. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> Larghezza in pixel del file di output. Il modulo mantiene le proporzioni originali. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Seleziona se il file appena modificato sovrascriverà eventuali file di output già esistenti. Questo vale solo per i file nell’archiviazione Adobe.</p>
      </td>
    </tbody>
</table>
