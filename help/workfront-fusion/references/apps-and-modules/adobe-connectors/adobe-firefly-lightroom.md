---
title: Moduli Adobe Firefly
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Firefly Lightroom e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 16%

---

# Moduli Lightroom di Adobe Firefly

<!--add to tocs-->

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Firefly Lightroom e collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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

Prima di poter utilizzare il connettore Adobe Firefly Lightroom, è necessario assicurarsi che siano soddisfatti i seguenti prerequisiti:

* Devi disporre di un account Adobe Firefly Lightroom attivo.

## Creare una connessione ad Adobe Firefly Lightroom

Per creare una connessione per i moduli Lightroom di Adobe Firefly:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">ID client</td>
        <td>Immetti l'ID client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segreto client</td>
        <td>Immetti il segreto client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## Moduli Lightroom di Adobe Firefly e relativi campi

Quando configuri i moduli Lightroom di Adobe Firefly, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati campi Lightroom aggiuntivi di Adobe Firefly, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Aggiungi XMP all&#39;immagine](#add-xmp-to-image)
* [Applicare le modifiche Lightroom](#apply-lightroom-edits)
* [Applicare i predefiniti di Lightroom](#apply-lightroom-presets)
* [Raddrizza automaticamente](#auto-straighten)
* [Tono automatico](#auto-tone)


### Aggiungi XMP all&#39;immagine

Questo modulo applica un predefinito Lightroom basato su XMP a un’immagine.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly Lightroom, vedere <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Creare una connessione ad Adobe Firefly Lightroom</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL immagine</td> 
   <td>Inserisci o mappa un URL preceduto che rappresenta l’immagine a cui desideri applicare XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di archiviazione</td> 
   <td>Selezionare il tipo di archiviazione in cui è memorizzata l'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Contenuto XMP</td> 
   <td>Inserisci o mappa il testo del contenuto XMP che desideri aggiungere all’immagine. Deve essere una stringa XML.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Orientamento</td> 
    <td>Inserisci o mappa l'orientamento EXIF da applicare all'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archiviazione di output</td> 
    <td>Selezionare la posizione in cui si desidera memorizzare il file di output. <p>La memorizzazione interna di Fusion non memorizza l'immagine al di fuori dello scenario, ma consente ad altri moduli dello scenario di accedere all'immagine.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di output</td> 
   <td>Selezionare il tipo di file per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Seleziona sì se desideri consentire al modulo di sovrascrivere l’output se esiste già. Questo vale solo per l’archiviazione cloud Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualità</td> 
   <td>Immettete o mappate la qualità dell'immagine di output. 1 corrisponde alla qualità più bassa e 12 alla qualità più elevata. Questo vale solo per i file JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Applicare le modifiche Lightroom

Questo modulo applica una o più modifiche Lightroom a un’immagine. Le modifiche includono esposizione, contrasto, nitidezza e saturazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly Lightroom, vedere <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Creare una connessione ad Adobe Firefly Lightroom</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL immagine</td> 
   <td>Inserisci o mappa un URL preceduto che rappresenta l’immagine a cui desideri applicare XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di archiviazione</td> 
   <td>Selezionare il tipo di archiviazione in cui è memorizzata l'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Opzioni di modifica</td> 
   <td>Impostate le opzioni di modifica da applicare all'immagine.<p>Per informazioni dettagliate sulle opzioni, consulta <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Applica modifiche Lightroom</a> nella documentazione API di Adobe Firefly Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archiviazione di output</td> 
    <td>Selezionare la posizione in cui si desidera memorizzare il file di output. <p>La memorizzazione interna di Fusion non memorizza l'immagine al di fuori dello scenario, ma consente ad altri moduli dello scenario di accedere all'immagine.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di output</td> 
   <td>Selezionare il tipo di file per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Seleziona sì se desideri consentire al modulo di sovrascrivere l’output se esiste già. Questo vale solo per l’archiviazione cloud Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualità</td> 
   <td>Immettete o mappate la qualità dell'immagine di output. 1 corrisponde alla qualità più bassa e 12 alla qualità più elevata. Questo vale solo per i file JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Applicare i predefiniti di Lightroom

Questo modulo applica uno o più predefiniti di XMP Lightroom all’immagine specificata, utilizzando i file XMP predefiniti forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly Lightroom, vedere <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Creare una connessione ad Adobe Firefly Lightroom</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL immagine</td> 
   <td>Inserisci o mappa un URL preceduto che rappresenta l’immagine a cui desideri applicare XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di archiviazione</td> 
   <td>Selezionare il tipo di archiviazione in cui è memorizzata l'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Predefiniti</td> 
   <td>Per ogni predefinito che si desidera applicare, fare clic su <b>Aggiungi elemento</b>, immettere l'URL predefinito del predefinito e selezionare il relativo tipo di archiviazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archiviazione di output</td> 
    <td>Selezionare la posizione in cui si desidera memorizzare il file di output. <p>La memorizzazione interna di Fusion non memorizza l'immagine al di fuori dello scenario, ma consente ad altri moduli dello scenario di accedere all'immagine.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di output</td> 
   <td>Selezionare il tipo di file per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Seleziona sì se desideri consentire al modulo di sovrascrivere l’output se esiste già. Questo vale solo per l’archiviazione cloud Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualità</td> 
   <td>Immettete o mappate la qualità dell'immagine di output. 1 corrisponde alla qualità più bassa e 12 alla qualità più elevata. Questo vale solo per i file JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Raddrizza automaticamente

Questo modulo raddrizza automaticamente un’immagine applicando la trasformazione in posizione verticale automatica.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly Lightroom, vedere <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Creare una connessione ad Adobe Firefly Lightroom</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL immagine</td> 
   <td>Inserisci o mappa un URL preceduto che rappresenta l’immagine a cui desideri applicare XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di archiviazione</td> 
   <td>Selezionare il tipo di archiviazione in cui è memorizzata l'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Modalità verticale</td> 
   <td>Selezionare il tipo di modalità verticale che si desidera utilizzare. Se non si imposta un valore, verrà fornita automaticamente una modalità appropriata.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Vincola ritaglio</td> 
   <td>Seleziona se ritagliare l'immagine raddrizzata per rimuovere tutti gli spigoli vuoti.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">Archiviazione di output</td> 
    <td>Selezionare la posizione in cui si desidera memorizzare il file di output. <p>La memorizzazione interna di Fusion non memorizza l'immagine al di fuori dello scenario, ma consente ad altri moduli dello scenario di accedere all'immagine.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di output</td> 
   <td>Selezionare il tipo di file per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Seleziona sì se desideri consentire al modulo di sovrascrivere l’output se esiste già. Questo vale solo per l’archiviazione cloud Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualità</td> 
   <td>Immettete o mappate la qualità dell'immagine di output. 1 corrisponde alla qualità più bassa e 12 alla qualità più elevata. Questo vale solo per i file JPEG.</td> 
  </tr> 
 </tbody> 
</table>


### Tono automatico

Questo modulo corregge automaticamente l&#39;esposizione, il contrasto, la nitidezza e la saturazione di un&#39;immagine.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly Lightroom, vedere <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Creare una connessione ad Adobe Firefly Lightroom</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL immagine</td> 
   <td>Inserisci o mappa un URL preceduto che rappresenta l’immagine a cui desideri applicare XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di archiviazione</td> 
   <td>Selezionare il tipo di archiviazione in cui è memorizzata l'immagine.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Archiviazione di output</td> 
    <td>Selezionare la posizione in cui si desidera memorizzare il file di output. <p>La memorizzazione interna di Fusion non memorizza l'immagine al di fuori dello scenario, ma consente ad altri moduli dello scenario di accedere all'immagine.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di output</td> 
   <td>Selezionare il tipo di file per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sovrascrivi</td> 
   <td>Seleziona sì se desideri consentire al modulo di sovrascrivere l’output se esiste già. Questo vale solo per l’archiviazione cloud Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualità</td> 
   <td>Immettete o mappate la qualità dell'immagine di output. 1 corrisponde alla qualità più bassa e 12 alla qualità più elevata. Questo vale solo per i file JPEG.</td> 
  </tr> 
 </tbody> 
</table>


