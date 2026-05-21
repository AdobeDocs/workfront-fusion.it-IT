---
title: Moduli Adobe Firefly
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Adobe Firefly], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
TQID: https://experienceleague.adobe.com/1hI4NuUl2eEAgWyXRKLHQ3-6MM9-2tFyujGbRfHSBmU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 3886
ht-degree: 15%

---

# Moduli [!DNL Adobe Firefly]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Firefly], nonché collegarli a più applicazioni e servizi di terze parti.

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

Prima di poter utilizzare il connettore [!DNL Adobe Firefly], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Firefly] attivo.

## Informazioni API di Adobe Firefly

Il connettore Adobe Firefly utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione ad [!DNL Adobe Firefly]

Per creare una connessione per i moduli [!DNL Adobe Firefly]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Adobe]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.

## Moduli [!DNL Adobe Firefly] e relativi campi

Quando configuri i moduli [!DNL Adobe Firefly], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Adobe Firefly], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Espandere un&#39;immagine

Questo modulo di azione espande un’immagine, facoltativamente con il contenuto di un prompt fornito.

Questo modulo funziona con Firefly API V3 Async. La versione precedente di questo modulo è stata dichiarata obsoleta e verrà rimossa a breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immetti o mappa un prompt per il contenuto con cui desideri espandere l’immagine. Se non viene fornito alcun prompt, l’immagine viene espansa con contenuto corrispondente all’immagine originale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 4. Il modulo genera questo numero di varianti di immagine espanse.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Origine]</td> 
   <td>Seleziona la modalità di fornitura del file di origine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>Selezionare il formato di file con cui verrà salvata l'immagine espansa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand by]</td> 
   <td>  <p>Seleziona se desideri espandere l’immagine utilizzando il posizionamento dell’immagine o una maschera.</p> 
   <ul>
   <li><b>Posizionamento</b><p>Immettete l'allineamento orizzontale e verticale e l'inizio dell'immagine posizionata dai bordi.</p></li>
   <li><b>Maschera</b><p>Selezionate il file di origine per la maschera e specificate se la maschera deve essere invertita.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selezionate l'altezza e la larghezza desiderate per l'immagine espansa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Per ogni immagine generata dal modulo, fare clic su <b>Aggiungi elemento</b> e immettere o mappare un numero intero. Puoi utilizzare lo stesso valore di inizializzazione in un altro modulo Espandi un’immagine per generare un’immagine simile con stili diversi. Il numero di seed aggiunti deve essere uguale al campo Numero di varianti.</td> 
  </tr> 
 </tbody> 
</table>

### Espandere un’immagine (obsoleto)

Questo modulo è stato dichiarato obsoleto e verrà rimosso a breve. Utilizza invece il modulo Espandi immagine.

### Riempi un’immagine

Questo modulo di azione riempie l’area nascosta di un’immagine, facoltativamente con il contenuto di un prompt fornito dall’utente.

Questo modulo funziona con Firefly API V3 Async. La versione precedente di questo modulo è stata dichiarata obsoleta e verrà rimossa a breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
   <td>Selezionare la modalità di fornitura del file di origine dell'immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask &gt; Source]</td> 
   <td>Selezionare la modalità di fornitura del file di origine della maschera:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immetti o mappa un prompt per il contenuto con cui desideri riempire l’immagine. Se non viene fornito alcun prompt, l’immagine verrà riempita con contenuto corrispondente all’immagine originale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 4. Il modulo genera questo numero di varianti di immagine riempite.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato immagine riempita]</td> 
   <td>Selezionate il formato di file con cui verrà salvata l'immagine riempita.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Per ogni immagine generata dal modulo, fare clic su <b>Aggiungi elemento</b> e immettere o mappare un numero intero. Puoi utilizzare lo stesso valore di inizializzazione in un altro modulo Espandi un’immagine per generare un’immagine simile con stili diversi. Il numero di seed aggiunti deve essere uguale al campo Numero di varianti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selezionate la dimensione desiderata per l'immagine riempita.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Se viene fornita una lingua, il modulo genera contenuto più pertinente alla lingua specificata. <p>Le impostazioni internazionali devono essere specificate nel codice della lingua ISO 639-1 e nell'area geografica ISO 3166-1.</p><p> Esempio: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Riempire un’immagine (obsoleto)

Questo modulo è stato dichiarato obsoleto e verrà rimosso a breve. Utilizza invece il modulo Riempi immagine.

### Genera composito adattivo

Questo modulo d&#39;azione associa perfettamente un&#39;immagine del soggetto a un&#39;immagine di sfondo in un luogo mascherato. È possibile controllare il grado di intensità delle ombre applicate, l&#39;armonizzazione dell&#39;illuminazione e del colore dell&#39;oggetto con lo sfondo e se i dettagli dello sfondo originale vengono mantenuti all&#39;interno dell&#39;area mascherata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sfondo &gt; Immagine &gt; Source]</td> 
   <td>Seleziona la modalità di creazione dell'immagine di sfondo. L'immagine di sfondo è la scena di destinazione in cui verrà composto l'oggetto.<ul><li><p><b>Carica immagine</b></p><p>Carica l’immagine di sfondo o mappa il file immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Inserisci o mappa l’URL dell’immagine di sfondo.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sfondo &gt; Maschera area di riempimento &gt; Source]</td> 
   <td>Selezionate la modalità di creazione della maschera dell'area di riempimento. La maschera dell'area di riempimento indica l'area dello sfondo in cui verrà posizionato l'oggetto.<ul><li><p><b>Carica immagine</b></p><p>Caricate l'immagine della maschera dell'area di riempimento o mappate il file di immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Immettere o mappare l'URL dell'immagine della maschera dell'area di riempimento.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object &gt; Image &gt; Source]</td> 
   <td>Selezionare la modalità di creazione dell'immagine oggetto. L'immagine oggetto è l'immagine sorgente dell'oggetto da comporre sullo sfondo.<ul><li><p><b>Carica immagine</b></p><p>Carica l’immagine oggetto o mappa il file immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Immettere o mappare l'URL dell'immagine oggetto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object &gt; Mask &gt; Source]</td> 
   <td>Selezionare la modalità di creazione della maschera oggetto. La maschera oggetto è la maschera di segmentazione dell'oggetto.<ul><li><p><b>Carica immagine</b></p><p>Caricate l'immagine della maschera oggetto o mappate il file immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Immettere o mappare l'URL dell'immagine della maschera oggetto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 3. Il modulo genera questo numero di varianti composite.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Fare clic su <b>Aggiungi elemento</b> per aggiungere un valore di inizializzazione, quindi immettere o mappare un numero intero. Utilizza un valore di inizializzazione per variante. Il conteggio dei valori iniziali deve corrispondere al valore [!UICONTROL Number of Variations], se vengono forniti entrambi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Harmonization]*</td> 
   <td>Immettete un numero compreso tra 0 e 1 per controllare in che misura i colori e l'illuminazione dell'oggetto vengono regolati in modo da corrispondere allo sfondo. <code>0.0</code> applica un'armonizzazione minima e <code>1.0</code> applica l'armonizzazione massima.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Intensità ombreggiatura]*</td> 
   <td>Immettete un numero compreso tra 0 e 1 per controllare l'intensità dell'ombreggiatura nel risultato composto. I valori più bassi riducono l'ombra.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mantieni sfondo]*</td> 
   <td>Selezionate se mantenere i dettagli di sfondo originali all'interno dell'area mascherata durante la composizione. <ul><li><b>Sì</b><p>I dettagli originali dello sfondo all'interno dell'area mascherata vengono mantenuti durante la composizione.</p></li><li><b>No</b><p>I dettagli di sfondo originali all'interno dell'area mascherata non vengono mantenuti durante la composizione.</p></li><li><b>Non definito</b><p>Utilizza il comportamento predefinito per questa opzione.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output &gt; Tipo di file multimediale]*</td> 
   <td>Selezionare il formato di file con cui verrà salvato il composito generato.</td> 
  </tr> 
 </tbody> 
</table>

* Questi campi sono campi avanzati e vengono visualizzati solo se si seleziona **[!UICONTROL Mostra impostazioni avanzate]**.

### Generare un’immagine

Questo modulo di azione genera un’immagine e in base a un prompt fornito. È inoltre possibile fornire un&#39;immagine di riferimento facoltativa. L&#39;immagine generata corrisponderà allo stile dell&#39;immagine di riferimento.

Questo modulo funziona con Firefly API V3 Async. La versione precedente di questo modulo è stata dichiarata obsoleta e verrà rimossa a breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immettete o mappate un prompt per l'immagine da generare. Un maggior numero di dettagli nel prompt consente un maggiore controllo su ciò che appare nell'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Seleziona la versione del modello Firefly da utilizzare per generare l’immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 4. Il modulo genera questo numero di varianti di immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selezionare il formato di file con cui verrà salvata l'immagine espansa. Se si seleziona predefinito, il formato del file sarà JPEG se non viene fornita alcuna immagine di riferimento. Se viene fornita un’immagine di riferimento, il formato del file dell’immagine generata sarà lo stesso dell’immagine di riferimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Riferimento immagine]</td> 
    <td>Selezionare la modalità di creazione del file di origine per la struttura della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struttura &gt; Forza]</td> 
    <td>Immettete un numero compreso tra 0 e 100 per controllare il rigoroso rispetto di Firefly alla struttura dell'immagine sorgente. Numeri più alti indicano che Firefly segue l'immagine in modo più rigoroso.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Riferimento immagine]</td> 
    <td>Selezionare la modalità di creazione del file di origine per lo stile della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struttura &gt; Forza]</td> 
    <td>Immettete un numero compreso tra 0 e 100 per controllare in che modo Firefly rispetta rigorosamente lo stile dell'immagine sorgente. Numeri più alti indicano che Firefly segue l'immagine in modo più rigoroso.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Predefiniti]</td> 
   <td>Se si desidera utilizzare uno stile predefinito, fare clic su Aggiungi elemento e immettere o mappare lo stile che si desidera utilizzare.<p>Per un elenco degli stili predefiniti, consulta <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Stili modello immagine</a> nella documentazione per gli sviluppatori di Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative prompt]</td> 
   <td>Immetti o mappa le parole da evitare nel contenuto generato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Classe Content]</td> 
   <td>Seleziona se desideri che l'immagine generata sia più simile a una foto o più simile a un'immagine creata. <ul><li><b>Foto</b><p>Immettete i valori per l'apertura, la velocità dell'otturatore (in secondi) e il campo visivo (in millimetri).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>Per ogni immagine generata dal modulo, fare clic su <b>Aggiungi elemento</b> e immettere o mappare un numero intero. Puoi utilizzare lo stesso valore di inizializzazione in un altro modulo Espandi un’immagine per generare un’immagine simile con stili diversi. Il numero di seed aggiunti deve essere uguale al campo Numero di varianti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Seleziona la dimensione desiderata per l'immagine generata.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Intensità visiva]</td> 
   <td>Immettere o mappare un numero intero che rappresenta l'intensità complessiva delle caratteristiche visive esistenti della foto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Se viene fornita una lingua, il modulo genera contenuto più pertinente alla lingua specificata. <p>Le impostazioni internazionali devono essere specificate nel codice della lingua ISO 639-1 e nell'area geografica ISO 3166-1.</p><p> Esempio: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Affiancabile]</td> 
   <td>Abilita questa opzione per generare un’immagine che possa essere ripetuta all’infinito in ogni direzione.</td> 
  </tr> 
 </tbody> 
</table>

### Genera un’immagine (obsoleto)

Questo modulo è stato dichiarato obsoleto e verrà rimosso a breve. Al suo posto, utilizza il modulo Genera un’immagine.

### Generare un oggetto composito

Questo modulo di azione combina immagini generate da Firefly per creare un’immagine composita.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immettete o mappate un prompt per l'immagine da generare. Un maggior numero di dettagli nel prompt consente un maggiore controllo su ciò che appare nell'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 4. Il modulo genera questo numero di varianti di immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content Classs]</td> 
   <td>Seleziona se desideri che l'immagine generata sia più simile a una foto o a un'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
    <td>Selezionare la modalità di creazione del file di origine per la struttura della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selezionare il formato di file con cui verrà salvata l'immagine espansa. Se si seleziona predefinito, il formato del file sarà JPEG se non viene fornita alcuna immagine di riferimento. Se viene fornita un’immagine di riferimento, il formato del file dell’immagine generata sarà lo stesso dell’immagine di riferimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Riferimento immagine]</td> 
    <td>Selezionare la modalità di creazione del file di origine per lo stile della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Struttura &gt; Forza]</td> 
    <td>Immettete un numero compreso tra 0 e 100 per controllare in che modo Firefly rispetta rigorosamente lo stile dell'immagine sorgente. Numeri più alti indicano che Firefly segue l'immagine in modo più rigoroso.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Predefiniti]</td> 
   <td>Se si desidera utilizzare uno stile predefinito, fare clic su Aggiungi elemento e immettere o mappare lo stile che si desidera utilizzare.<p>Per un elenco degli stili predefiniti, consulta <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Stili modello immagine</a> nella documentazione per gli sviluppatori di Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selezionare la dimensione desiderata per il composito generato. </td> 
  </tr> 
 </tbody> 
</table>

### Genera immagini con Image5

Questo modulo di azione genera un&#39;immagine utilizzando il modello di immagine [!DNL Adobe Firefly] Image5. Viene visualizzato un prompt di testo e, facoltativamente, un&#39;immagine di riferimento per guidare la generazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immettere o mappare una descrizione dell'immagine che si desidera generare. Il prompt deve contenere tra 1 e 1500 caratteri. Un maggior numero di dettagli nel prompt consente un maggiore controllo su ciò che appare nell'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Proporzioni]</td> 
   <td>Seleziona la forma dell’immagine generata. Se viene fornita un'immagine di riferimento, selezionare <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resolution]</td> 
   <td>Seleziona la risoluzione dell'immagine generata. La generazione di risoluzioni più elevate richiede più tempo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference Image]</td> 
   <td>Facoltativamente, fornisci un’immagine di riferimento per guidare la generazione. Fai clic su <b>Aggiungi elemento</b> e fornisci l'immagine. Quando si utilizza un'immagine di riferimento, impostare [!UICONTROL Aspect Ratio] su <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]*</td> 
   <td>Fai clic su <b>Aggiungi elemento</b> e immetti o mappa un numero intero per riprodurre un risultato di generazione specifico. Lascia vuoto per generare un risultato casuale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Motivo del prompt di [!UICONTROL]*</td> 
   <td>Selezionare la strategia di ragionamento rapida utilizzata durante la generazione.<ul><li><p><b>Qualità: genera la descrizione dell’immagine</b></p><p>Genera una descrizione immagine nell’output del modulo.</p></li><li><p><b>Velocità - Generazione più rapida, nessuna descrizione</b></p><p>Genera l’immagine più rapidamente, ma lascia vuota la descrizione dell’immagine.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]*</td> 
   <td>Immetti o mappa un codice di lingua e area geografica per adattare il contenuto generato a un paese e una lingua specifici. <p>Le impostazioni internazionali devono essere specificate nel codice della lingua ISO 639-1 e nell'area geografica ISO 3166-1.</p><p>Esempio: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]*</td> 
   <td>Immetti il numero di immagini da generare per richiesta. Attualmente, è supportato solo 1. Per generare più immagini, invia richieste separate.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]*</td> 
   <td>Selezionare il modello [!DNL Firefly] da utilizzare per generare l'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

*Questi campi sono avanzati e non vengono visualizzati se non si seleziona **[!UICONTROL Mostra impostazioni avanzate]**.

### Genera composito preciso

Questo modulo d&#39;azione colloca un soggetto nella regione mascherata di un&#39;immagine di sfondo e applica l&#39;armonizzazione generativa in modo che il soggetto si fonda naturalmente con lo sfondo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sfondo &gt; Immagine &gt; Source]</td> 
   <td>Seleziona la modalità di creazione dell'immagine di sfondo. L'immagine di sfondo è la scena di destinazione in cui verrà composto l'oggetto.<ul><li><p><b>Carica immagine</b></p><p>Carica l’immagine di sfondo o mappa il file immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Inserisci o mappa l’URL dell’immagine di sfondo.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sfondo &gt; Maschera area di riempimento &gt; Source]</td> 
   <td>Selezionate la modalità di creazione della maschera dell'area di riempimento. La maschera dell'area di riempimento indica l'area dello sfondo in cui verrà posizionato l'oggetto.<ul><li><p><b>Carica immagine</b></p><p>Caricate l'immagine della maschera dell'area di riempimento o mappate il file di immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Immettere o mappare l'URL dell'immagine della maschera dell'area di riempimento.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object &gt; Image &gt; Source]</td> 
   <td>Selezionare la modalità di creazione dell'immagine oggetto. L'immagine oggetto è l'immagine sorgente dell'oggetto da comporre sullo sfondo.<ul><li><p><b>Carica immagine</b></p><p>Carica l’immagine oggetto o mappa il file immagine da un modulo precedente.</p></li><li><p><b>URL immagine</b></p><p>Immettere o mappare l'URL dell'immagine oggetto.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 3. Il modulo genera questo numero di varianti composite.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Fare clic su <b>Aggiungi elemento</b> per aggiungere un valore di inizializzazione, quindi immettere o mappare un numero intero. Utilizza un valore di inizializzazione per variante. Il conteggio dei valori iniziali deve corrispondere al valore [!UICONTROL Number of Variations], se vengono forniti entrambi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blend]*</td> 
   <td>Immettere un numero compreso tra 0 e 1 per controllare la fusione tra l'aspetto armonizzato e originale dell'oggetto. <code>0.0</code> applica l'armonizzazione completa e <code>1.0</code> mantiene l'aspetto dell'oggetto originale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output &gt; Tipo di file multimediale]*</td> 
   <td>Selezionare il formato di file con cui verrà salvato il composito generato.</td> 
  </tr> 
 </tbody> 
</table>

* Questi campi sono campi avanzati e vengono visualizzati solo se si seleziona **[!UICONTROL Mostra impostazioni avanzate]**.

### Genera immagini simili

Questo modulo di azione genera immagini simili all’immagine di origine specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero di varianti]</td> 
   <td>Immettere un numero compreso tra 1 e 4. Il modulo genera questo numero di varianti di immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Seleziona la versione del modello Firefly da utilizzare per generare le immagini.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selezionare il formato di file con cui verrà salvata l'immagine espansa. Se si seleziona predefinito, il formato del file sarà JPEG se non viene fornita alcuna immagine di riferimento. Se viene fornita un’immagine di riferimento, il formato del file dell’immagine generata sarà lo stesso dell’immagine di riferimento.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
    <td>Selezionare la modalità di creazione del file di origine per la struttura della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Riferimento immagine]</td> 
    <td>Selezionare la modalità di creazione del file di origine per lo stile della nuova immagine:<ul><li><p><b>File</b></p><p>Selezionate un file di origine da un modulo precedente o mappate il nome del file di immagine di riferimento e il file di immagine di riferimento del file di origine.</p></li><li><p><b>URL preceduto</b></p><p>Inserisci o mappa l’URL dell’immagine sorgente.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selezionare la dimensione desiderata per il composito generato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Per ogni immagine generata dal modulo, fare clic su <b>Aggiungi elemento</b> e immettere o mappare un numero intero. Puoi utilizzare lo stesso valore di inizializzazione in un altro modulo Espandi un’immagine per generare un’immagine simile con stili diversi. Il numero di seed aggiunti deve essere uguale al campo Numero di varianti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Affiancabile]</td> 
   <td>Abilita questa opzione per generare un’immagine che possa essere ripetuta all’infinito in ogni direzione.</td> 
  </tr> 
 </tbody> 
</table>


### Genera video

Questo modulo di azione genera un video da un prompt di testo. È inoltre possibile fornire una o più immagini di riferimento per guidare la generazione del video.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Immetti o mappa una descrizione del video che desideri generare. Un maggior numero di dettagli nel prompt consente un maggiore controllo su ciò che appare nel video.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immagine &gt; Condizioni]</td> 
   <td>È possibile fornire una o più immagini di riferimento per guidare la generazione del video. Fai clic su <b>Aggiungi elemento</b> per ogni immagine di riferimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sizes]</td> 
   <td>Fai clic su <b>Aggiungi elemento</b> e immetti o mappa le dimensioni del video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fattore di velocità in bit [!UICONTROL]*</td> 
   <td>Immettete un numero compreso tra 0 e 63 per specificare il fattore di bit rate del video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni video &gt; Movimento fotocamera]*</td> 
   <td>Selezionate il movimento della videocamera da usare nel video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni Video &gt; Stile Prompt]*</td> 
   <td>Selezionate lo stile di prompt che desiderate utilizzare per il video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni Video &gt; Angolo Di Ripresa]*</td> 
   <td>Selezionate l'angolo di ripresa da utilizzare nel video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni video &gt; Dimensioni ripresa]*</td> 
   <td>Seleziona la dimensione della ripresa da utilizzare nel video generato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

* Questi campi sono campi avanzati e vengono visualizzati solo se si seleziona **[!UICONTROL Mostra impostazioni avanzate]**.

### Effettua chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Firefly.

Per le API disponibili specifiche, vedi [API Adobe Firefly](https://developer.adobe.com/firefly-services/docs/firefly-api/) nella documentazione di Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], consulta <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://firefly-api.adobe.io/</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Metodo]</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Intestazioni]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

