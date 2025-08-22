---
title: Moduli Adobe Firefly
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Adobe Firefly], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2482'
ht-degree: 0%

---

# [!DNL Adobe Firefly] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Firefly] e collegarlo a più applicazioni e servizi di terze parti.

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

## Crea una connessione a [!DNL Adobe Firefly]

Per creare una connessione per i moduli [!DNL Adobe Firefly]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

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
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## [!DNL Adobe Firefly] moduli e relativi campi

Quando si configurano [!DNL Adobe Firefly] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Firefly], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Espandere un&#39;immagine

Questo modulo di azione espande un’immagine, facoltativamente con il contenuto di un prompt fornito.

Questo modulo funziona con Firefly API V3 Async. La versione precedente di questo modulo è stata dichiarata obsoleta e verrà rimossa a breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Campaign], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
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
   <td role="rowheader">[!UICONTROL Source]</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Campaign], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
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

### Generare un’immagine

Questo modulo di azione genera un’immagine e in base a un prompt fornito. È inoltre possibile fornire un&#39;immagine di riferimento facoltativa. L&#39;immagine generata corrisponderà allo stile dell&#39;immagine di riferimento.

Questo modulo funziona con Firefly API V3 Async. La versione precedente di questo modulo è stata dichiarata obsoleta e verrà rimossa a breve.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Campaign], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Campaign], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
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

### Genera immagini simili

Questo modulo di azione genera immagini simili all’immagine di origine specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Campaign], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td> 
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


### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Firefly.

Per le API disponibili specifiche, vedi [API Adobe Firefly](https://developer.adobe.com/firefly-services/docs/firefly-api/) nella documentazione di Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Firefly], vedere <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Creare una connessione a [!DNL Adobe Firefly]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Immettere un percorso relativo a <code>https://firefly-api.adobe.io/</code>.</p>
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
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

