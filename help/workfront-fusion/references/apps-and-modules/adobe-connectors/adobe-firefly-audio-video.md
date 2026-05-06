---
title: Moduli audio e video di Adobe Firefly
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Firefly Audio and Video, nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 14%

---

# Moduli audio e video di Adobe Firefly

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Firefly Audio and Video, nonché collegarli a più applicazioni e servizi di terze parti.

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

Prima di poter utilizzare il connettore Adobe Firefly Audio and Video, è necessario assicurarsi che siano soddisfatti i seguenti prerequisiti:

* Devi disporre di un account Adobe Firefly Audio and Video attivo.

## Creare una connessione ad Adobe Firefly Audio and Video

Per creare una connessione per i moduli audio e video di Adobe Firefly:

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


## Moduli audio e video di Adobe Firefly e relativi campi

Quando configuri i moduli audio e video di Adobe Firefly, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati campi audio e video aggiuntivi di Adobe Firefly, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

* [Descrivi modello](#describe-template)
* [Dub audio o video](#dub-audio-or-video)
* [Genera video avatar da testo o audio](#generate-avatar-video-from-text-or-audio)
* [Genera riconoscimento vocale da testo](#generate-speech-from-text)
* [Rielabora video](#reframe-video)
* [Rendering modello](#render-template)
* [Trascrizione file multimediali](#transcribe-media)

#### Descrivi modello

Questo modulo di azione analizza un file MOGRT (modello video) e restituisce un manifesto di controlli modificabili, font, immagini, audio, video e altri valori supportati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Inserisci o mappa l’URL prefirmato che punta al file del modello di input.</td> 
  </tr>
 </tbody> 
</table>

#### Dub audio o video

Questo modulo di azione genera audio o video duplicati. Può anche includere la sincronizzazione labiale nel video generato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di duplicato</td> 
   <td>Seleziona se desideri generare un duplicato audio o video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">URL preceduto</td> 
   <td>Inserisci o mappa l’URL preceduto che il modulo utilizzerà per l’input.<p>I seguenti domini per l'archiviazione dei contenuti multimediali sono accettati da Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo di file multimediale</td> 
   <td>Selezionare il tipo di supporto del file di input</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sincronizzazione delle labbra</td> 
   <td>Seleziona se generare una sincronizzazione labiale composita di alta qualità per l'output video.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Codici delle impostazioni internazionali di destinazione</td> 
   <td>Per ogni codice locale che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e selezionare il codice locale.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Trascrizioni</td> 
   <td>Per ogni trascrizione che desideri aggiungere, fai clic su <b>Aggiungi elemento</b> e immetti o mappa gli URL predefiniti per la trascrizione.</td> 
  </tr>
 </tbody> 
</table>

#### Genera video avatar da testo o audio

Questo modulo di azione genera un video avatar da una trascrizione o da un file audio fornito.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Inserisci o mappa l’URL preceduto che il modulo utilizzerà per l’input.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">Codice lingua</td> 
   <td>Selezionare il codice locale che rappresenta la lingua che si desidera utilizzare nel risultato.</td> 
  </tr>
   <td role="rowheader">Tipo di file multimediale (Source)</td> 
   <td>Selezionare il tipo di supporto del file di input</td> 
  </tr>
  <tr> 
   <td role="rowheader">Avatar</td> 
   <td>Seleziona l’avatar da utilizzare per il video generato.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo di file multimediale</td> 
   <td>Seleziona il tipo di supporto di output per il video generato.</td> 
  </tr>
  <tr> 
   <td role="rowheader">larghezza</td> 
   <td>Immetti o mappa la larghezza del video generato.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Height</td> 
   <td>Inserisci o mappa l’altezza del video generato.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Informazioni di base</td> 
   <td>Seleziona il tipo di sfondo da utilizzare per il video generato:
   <ul>
   <li><b>Video</b>: immetti o mappa l'URL del video di sfondo.</li> 
   <li><b>Immagine</b>: immetti o mappa l'URL dell'immagine di sfondo.</li>
   <li><b>Colore</b>: immetti o mappa il valore esadecimale del colore da utilizzare per lo sfondo del video.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### Genera riconoscimento vocale da testo

Questo modulo di azione genera il riconoscimento vocale da una trascrizione. Puoi fornire una trascrizione in testo normale o un URL prefirmato. La risposta include un ID processo e un URL di stato per il tracciamento del processo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Script</td> 
   <td>Seleziona il tipo di script che desideri fornire.
   <ul>
   <li><b>Testo</b>: immettere o associare il testo di origine nel campo Testo.</li>
   <li><b>File di testo</b>: immettere o mappare l'URL del file di testo nel campo URL.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Codice lingua</td> 
   <td>Selezionare il codice locale che rappresenta la lingua che si desidera utilizzare nel risultato.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo di file multimediale</td> 
   <td>Deve essere <code>text/plain</code>.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Voce</td> 
   <td>Selezionare la voce che si desidera utilizzare. Le voci disponibili sono incluse nel catalogo di voci di Adobe Firefly.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Output</td> 
   <td>Deve essere <code>audio/wav</code>.</td> 
  </tr>
 </tbody> 
</table>

#### Rielabora video

Questo modulo ridefinisce il supporto fornito. Il contenuto multimediale viene fornito tramite un URL prefirmato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL preceduto</td> 
   <td>Inserisci o mappa l’URL preceduto che il modulo utilizzerà per l’input.<p>I seguenti domini per l'archiviazione dei contenuti multimediali sono accettati da Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Rilevamento modifica scena</td> 
   <td>Seleziona se applicare il rilevamento di modifica della scena prima di ridefinire il frame. </td> 
  </tr>
  <tr> 
   <td role="rowheader">Punto focale</td> 
   <td>Per ogni punto focale che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere o l'identificatore della parola chiave per il punto focale.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sovrapposizioni</td> 
   <td>Per ogni sovrapposizione che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere le informazioni di sovrapposizione.
   <ul>
   <li><b>Source</b>: immetti o mappa l'URL che punta al supporto di origine.</li> 
   <li><b>Ora di inizio</b>: immettere o mappare l'ora di inizio.</li>
   <li><b>Durata</b>: inserisci o mappa la durata della sovrapposizione.</li> 
   <li><b>Larghezza</b>: immetti o mappa la larghezza della sovrapposizione ridimensionata.</li> 
   <li><b>Altezza</b>: immetti o mappa l'altezza della sovrapposizione ridimensionata.</li> 
   <li><b>Punto di ancoraggio</b>: selezionare il punto di ancoraggio per la sovrapposizione.</li> 
   <li><b>Offset X</b>: immettere o mappare l'offset orizzontale per la sovrapposizione.</li> 
   <li><b>Offset Y</b>: immettere o mappare l'offset verticale per la sovrapposizione.</li> 
   <li><b>Ripeti</b>: immetti <code>loop</code> per generare un ciclo GIF.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato file multimediale</td> 
   <td>Selezionate il formato per il video con riframe.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato sidecar</td> 
   <td>Seleziona il formato per i metadati aggiuntivi.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Rappresentazioni</td> 
   <td>Per aggiungere altre copie trasformate, fare clic su <b>Aggiungi elemento</b> e immettere le informazioni relative alla copia trasformata.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### Rendering modello

Questo modulo esegue il rendering di una o più varianti video applicando sostituzioni ed esporta predefiniti.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL file modello di input</td> 
   <td>Inserisci o mappa l’URL preceduto che rappresenta il modello da riprodurre.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Font</td> 
   <td>Per ogni tipo di carattere che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere il nome postscript del tipo di carattere e l'URL del file del tipo di carattere.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Quando manca un font</td> 
   <td>Seleziona se non eseguire il rendering o se utilizzi il font predefinito, se manca un font.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Risorse multimediali</td> 
   <td>Per ogni risorsa multimediale che desideri aggiungere, fai clic su <b>Aggiungi elemento</b> e immetti o mappa l'URL predefinito che rappresenta la risorsa.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Esporta predefiniti</td> 
   <td>Per ogni predefinito di esportazione che desideri aggiungere, fai clic su <b>Aggiungi elemento</b> e seleziona il predefinito per video, quindi immetti o mappa l'URL predefinito che rappresenta il predefinito.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Varianti</td> 
   <td>Per ogni variante che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli per la variante. Immetti i dettagli per almeno una variante.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">Definizioni di output</td> 
   <td>Definire gli output facendo clic su <b>Aggiungi elemento</b> e selezionando le varianti e i predefiniti aggiunti che si desidera utilizzare e aggiungendo un nome file. Le varianti e i predefiniti sono indicizzati su 0 (il primo elemento nell’elenco delle varianti è 0, il successivo è 1 e così via).</td> 
  </tr>
 </tbody> 
</table>

#### Trascrizione file multimediali

Questo modulo trascrive audio o video.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Firefly, vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione ad Adobe Firefly</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di trascrizione</td> 
   <td>Seleziona se desideri trascrivere audio o video.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">URL preceduto</td> 
   <td>Inserisci o mappa l’URL preceduto che il modulo utilizzerà per l’input.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">Tipo di file multimediale </td> 
   <td>Selezionare il tipo di supporto del file di input</td> 
  </tr>
  <tr> 
   <td role="rowheader">Codici delle impostazioni internazionali di destinazione</td> 
   <td>Per ogni codice delle impostazioni locali che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e selezionare il codice delle impostazioni locali che rappresenta la lingua che si desidera utilizzare nel risultato.</td> 
  <tr> 
   <td role="rowheader">Formato didascalia</td> 
   <td>Immettere <code>SRT</code> per includere i sottotitoli o lasciare vuoto se non si desidera utilizzare i sottotitoli.</td> 
  </tr>
 </tbody> 
</table>



