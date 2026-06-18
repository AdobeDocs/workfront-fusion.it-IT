---
title: Moduli Adobe Photoshop
description: Con i moduli di Adobe Photoshop, puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell’account Adobe Photoshop, creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
TQID: https://experienceleague.adobe.com/RratZmko93V0LMxJ6qTy6cNvRqgPNvNgHTflRngE6BI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ce3fb5604ac4ed85af1bcc51143732499dfb0404
workflow-type: tm+mt
source-wordcount: 7285
ht-degree: 12%

---

# Moduli [!DNL Adobe Photoshop]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Photoshop], nonché collegarli a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>Adobe Photoshop ha dichiarato obsoleti alcuni elementi della sua API, che Fusion utilizza per eseguire azioni in Photoshop.
>
>**Di conseguenza, alcuni dei moduli Photoshop esistenti non funzioneranno dopo il 30 luglio 2026.**
>
>È consigliabile aggiornare il prima possibile gli scenari che utilizzano questi moduli nei moduli aggiornati.
>
>Per un elenco dei moduli interessati, vedere [Aggiornamenti deprecazione API Adobe Photoshop](#adobe-photoshop-api-deprecation-updates).
>
>Per una spiegazione di come le modifiche API influiscono su Workfront Fusion, vedere [Panoramica delle API in Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

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

Prima di poter utilizzare il connettore [!DNL Adobe Photoshop], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Photoshop] attivo.
* È necessario disporre di una licenza Firefly Services.
* È necessario disporre di un ID client e di un segreto client. Puoi acquistarli da Adobe Developer Console.

## Aggiornamenti obsoleti delle API di Adobe Photoshop

Adobe Photoshop ha dichiarato obsoleti alcuni elementi della sua API, che Fusion utilizza per eseguire azioni in Photoshop.

**Di conseguenza, alcuni dei moduli Photoshop esistenti non funzioneranno dopo il 30 luglio 2026.**

In questa tabella vengono indicati i moduli interessati da questa deprecazione e il modulo in cui eseguire l&#39;aggiornamento.

| Modulo legacy obsoleto | Aggiornamento al nuovo modulo |
|---|---|
| Applicare le modifiche PSD | Creare o modificare un elemento composito |
| Converti formato immagine | Creare o modificare un elemento composito |
| Creare un elemento composito | Creare o modificare un elemento composito |
| Crea un nuovo PSD | Creare o modificare un elemento composito |
| Creare rappresentazioni | Creare o modificare un elemento composito |
| Modificare i livelli di testo | Eseguire azioni, script e trasformazioni di Photoshop |
| Modificare i livelli di testo 2 | Eseguire azioni, script e trasformazioni di Photoshop |
| Esegui un’azione JSON | Eseguire azioni, script e trasformazioni di Photoshop |
| Esegui sfocatura profondità | (Non disponibile) |
| Eseguire azioni Photoshop | Eseguire azioni, script e trasformazioni di Photoshop |
| Esegui ritaglio prodotto | Eseguire azioni, script e trasformazioni di Photoshop |
| Ottieni informazioni livello | Generare un manifesto |
| Ridimensionare un’immagine | Creare o modificare un elemento composito |
| Sostituisci oggetto avanzato | Creare o modificare un elemento composito |
| Sostituisci oggetto avanzato 2 | Creare o modificare un elemento composito |
| Ruotare un’immagine | Eseguire azioni, script e trasformazioni di Photoshop |
| Filigrana di un’immagine | Creare o modificare un elemento composito |

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

## Creare una connessione ad [!DNL Adobe Photoshop]

Per creare una connessione per i moduli [!DNL Adobe Photoshop]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

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
          <p>Seleziona se desideri utilizzare una connessione JWT o una connessione server-to-server.</p>
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
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Adobe]. Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID account tecnico]</td>
        <td>Se utilizzi una connessione JWT, immetti l’ID dell’account tecnico [!DNL Adobe] . Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID organizzazione]</td>
        <td>Se utilizzi una connessione JWT, immetti l'ID organizzazione [!DNL Adobe] . Questo si trova nella sezione dei dettagli [!UICONTROL Credentials] del [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Chiave privata]</td>
        <td>
          <p>Se utilizzi una connessione JWT, immetti la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fai clic su <b>[!UICONTROL Estrai]</b>.</p>
            </li>
            <li value="2">
              <p>Seleziona il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Inserisci la password per il file.</p>
            </li>
            <li value="5">
              <p>Fai clic su <b>Salva</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.

## Moduli [!DNL Adobe Photoshop] e relativi campi

Quando configuri i moduli [!DNL Adobe Photoshop], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Adobe Photoshop], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

* [Converti HEX in RGB](#convert-hex-to-rgb)
* [Creare una tavola da disegno](#create-an-artboard)
* [Creare o modificare un elemento composito](#create-or-edit-a-composite)
* [Modificare un’immagine con varie regolazioni](#edit-an-image-with-various-adjustments)
* [Eseguire azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations)
* [Generare un manifesto](#generate-a-manifest)
* [Rimuovi sfondo](#remove-background)

#### Converti HEX in RGB

Questo modulo converte un codice colore HEX in colore RGB.



Questo modulo apporta le regolazioni di un&#39;immagine in stile Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL HEX]</td>
      <td>Immetti o mappa il codice HEX da convertire in RGB.</td>
    </tr>
    </tbody>
</table>

#### Creare una tavola da disegno

Questo modulo crea una nuova tavola da disegno in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Immagini]</td>
      <td>
        <p>Per ogni immagine da aggiungere alla tavola da disegno, fare clic su <b>Aggiungi elemento</b> e immettere il tipo e il percorso di origine dell'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Spaziatura tavola da disegno]</p>
      </td>
   <td>Immettete o mappate la spaziatura, in pixel, che desiderate avere tra ciascuna tavola da disegno.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file convertito che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e altre opzioni elencate.</p>
      </td>
    </tr>
    </tbody>
</table>

#### Creare o modificare un elemento composito

Questo modulo crea o modifica un composito in Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Immagini]</td>
      <td>
        <p>Per ogni immagine da aggiungere alla tavola da disegno, fare clic su <b>Aggiungi elemento</b> e immettere il tipo e il percorso di origine dell'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td>Se state creando un'immagine, immettete la larghezza dell'immagine in pixel.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Height]</td>
      <td>
        <p>Se state creando un'immagine, immettete l'altezza dell'immagine in pixel.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mode]</td>
      <td>
        <p>Selezionare la modalità colore per l'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fill]</td>
      <td>
        <p>Selezionate il tipo di riempimento per il livello di sfondo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nome]</td>
      <td>
        <p>Immettere o mappare un nome per la nuova immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Pixel scale factor]</td>
      <td>
        <p>Immettete o mappate il fattore di scala pixel. Deve essere un numero compreso tra 0,1 e 1.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p>Nel campo <b>Valore</b> immettere il valore della risoluzione in unità di densità (pixel per pollice). Il valore predefinito è 72.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Profile Type]</td>
      <td>
        <p>Se desiderate sostituire il profilo colore predefinito, selezionate un tipo di profilo e immettete i dettagli elencati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ritaglio &gt; Superiore / Sinistro / Inferiore / Destro]</td>
      <td>
        <p>Immettete i limiti ai quali desiderate ritagliare l'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nascondi]</td>
      <td>
        <p>Selezionate Sì per nascondere i pixel al di fuori dei limiti di ritaglio. Se è impostato su false, i pixel al di fuori dei limiti di ritaglio vengono eliminati. Il valore predefinito è false.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ridimensiona &gt; Larghezza]</td>
      <td>
        <p>Selezionare l'unità da utilizzare per la larghezza, quindi selezionare il valore che rappresenta la larghezza desiderata. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ridimensiona &gt; Altezza]</td>
      <td>
        <p>Selezionare l'unità da utilizzare per l'altezza, quindi selezionare il valore che rappresenta l'altezza desiderata. </p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p>Selezionare l'unità da utilizzare per la risoluzione, quindi selezionare il valore che rappresenta la risoluzione desiderata.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Ricampionamento]</td>
      <td>
        <p>Selezionate il metodo di ricampionamento da utilizzare per il ridimensionamento.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Vincola proporzioni]</td>
      <td>
        <p>Selezionare Sì per mantenere le proporzioni tra larghezza e altezza. Selezionate No per consentire la regolazione indipendente di larghezza e altezza.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Rasterizza]</td>
      <td>
        <p>Selezionare se si desidera rasterizzare l'immagine.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Scala stili]</td>
      <td>
        <p>Selezionate se desiderate applicare il ridimensionamento agli stili quando ridimensionate l'immagine.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Rifila su]</td>
      <td>
        <p>Selezionate se desiderate tagliare i pixel trasparenti.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Livelli]</td>
      <td>
        <p>Per ogni elemento che si desidera aggiungere in un secondo momento, fare clic su <b>Aggiungi elemento</b> e immettere i dettagli del livello. </p><p>Per informazioni dettagliate, vedere <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Creare o modificare un elemento composito</a> nella documentazione di Adobe.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Default font PostScript name]</td>
      <td>
        <p>Immettere o mappare il nome PostScript del carattere predefinito che si desidera utilizzare.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Strategia font mancante]</td>
      <td>
        <p>Specificare se si desidera che la creazione o la modifica non riesca o se si desidera utilizzare il tipo di carattere predefinito, qualora non sia disponibile.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Caratteri aggiuntivi]</td>
      <td>
        <p>Per ogni tipo di carattere che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere l'URL di origine del tipo di carattere. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file modificato che si desidera creare, fare clic su Aggiungi elemento e immettere i dettagli di output. </p><p>Per informazioni dettagliate, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">Creare o modificare un elemento composito</a> nella documentazione di Adobe.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di risultati]</td>
      <td>
        <p>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.</p>
      </td>
      </tr>
      </tbody>
</table>

#### Modificare un’immagine con varie regolazioni

Questo modulo apporta le regolazioni di un&#39;immagine in stile Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Immagini]</td>
      <td>
        <p>Immettete o mappate il tipo di origine e la posizione dell'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altri campi]</p>
      </td>
   <td><p>Per informazioni dettagliate, consulta <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/edit">Modificare un'immagine con varie regolazioni</a> nella documentazione di Adobe.</p></td> 
    </tr>
    </tbody>
</table>

#### Eseguire azioni, script e trasformazioni di Photoshop

Questo modulo esegue azioni, script e trasformazioni disponibili nell’API Photoshop di Firefly.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Immagini]</td>
      <td>
        <p>Immettete o mappate il tipo di origine e la posizione dell'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Azioni]</p>
      </td>
   <td><p>Per ogni azione che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere l'origine, l'URL e il nome dell'azione.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UXP source]</p>
      </td>
   <td><p>Se utilizzi uno script UXP, seleziona se stai fornendo un URL o contenuto in linea, quindi immetti o mappa l’URL o il contenuto.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Contenuti aggiuntivi]</p>
      </td>
   <td><p>Aggiungi fino a 25 file a cui si fa riferimento dall’azione o da UXP.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file modificato che si desidera creare, fare clic su Aggiungi elemento e immettere il formato, la destinazione e il pattern di output.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di risultati]</td>
      <td>
        <p>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Generare un manifesto

Questo modulo genera un manifesto PSD per l’immagine di input specificata.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origine]</td>
      <td>
        <p>Immettete o mappate il tipo di origine e la posizione dell'immagine.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file modificato che si desidera creare, fare clic su Aggiungi elemento e immettere i dettagli di destinazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Includi miniature livello]</p>
      </td>
   <td><p>Selezionate Sì se desiderate che il modulo generi una rappresentazione in miniatura per ciascun livello del manifesto.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Profondità massima miniature]</p>
      </td>
   <td><p>Immettete o mappate la profondità massima per le rappresentazioni delle miniature. Per nessuna profondità massima, immettere <code>0</code>.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layer thumbnail format]</p>
      </td>
   <td><p>Seleziona se desideri che le miniature siano in formato JPEG o PNG.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Estrai dati oggetto avanzato]</td>
      <td>
        <p>Seleziona se estrarre gli oggetti avanzati incorporati e includere un URL preceduto nel manifesto.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rifila in trasparenza]</td>
      <td>
        <p>Selezionate se rifilare la miniatura di ogni livello per rimuovere i pixel trasparenti.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di risultati]</td>
      <td>
        <p>Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.</p>
      </td>
      </tr>
    </tbody>
</table>

#### Rimuovi sfondo

Questo modulo di azione identifica il soggetto principale dell&#39;immagine e rimuove lo sfondo.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>[!UICONTROL Versione]</p>
      </td>
   <td>Il valore predefinito è 4,0</td> 
    </tr> 
    </tbody>
</table>


### Legacy

* [Applica modifiche PSD (legacy)](#apply-psd-edits-legacy)
* [Correzione automatica del colore di un&#39;immagine (legacy)](#auto-color-correct-an-image-legacy)
* [Converti formato immagine (legacy)](#convert-image-format-legacy)
* [Creare una maschera (legacy)](#create-a-mask-legacy)
* [Crea un nuovo PSD (legacy)](#create-a-new-psd-legacy)
* [Crea rappresentazioni (legacy)](#create-renditions-legacy)
* [Modifica livelli di testo (legacy)](#edit-text-layers-legacy)
* [Modifica livelli testo 2 (legacy)](#edit-text-layers-2-legacy)
* [Esegui un’azione JSON (legacy)](#execute-an-action-json-legacy)
* [Esegui sfocatura profondità (legacy)](#execute-depth-blur-legacy)
* [Esegui azioni Photoshop (legacy)](#execute-photoshop-actions-legacy)
* [Esegui ritaglio prodotto (legacy)](#execute-product-crop-legacy)
* [Ottieni informazioni livello (legacy)](#get-layer-info-legacy)
* [Effettuare una chiamata API personalizzata (legacy)](#make-a-custom-api-call-legacy)
* [Rimuovi sfondo (Legacy)](#remove-background-legacy)
* [Sostituire un oggetto avanzato (legacy)](#replace-a-smart-object-legacy)
* [Sostituire un oggetto avanzato 2 (legacy)](#replace-a-smart-object-2-legacy)
* [Ridimensionare un’immagine (legacy)](#resize-an-image-legacy)
* [Filigrana di un’immagine (legacy)](#watermark-an-image-legacy)

#### Applica modifiche PSD (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questo modulo di azione applica una serie di modifiche a livello di documento e di livello.

Questo modulo supporta file di grandi dimensioni. Per ulteriori informazioni sui file di grandi dimensioni, vedere [Utilizzo dei file di grandi dimensioni](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>Per ogni file modificato che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati.</p>
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

#### Correzione automatica del colore di un&#39;immagine (legacy)

Il colore automatico di questo modulo di azione corregge l’immagine specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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

#### Converti formato immagine (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questo modulo di azione converte un file in JPEG, PNG, PSD o TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>Per ogni file convertito che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati.</p>
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

#### Creare una maschera (legacy)

Questo modulo di azione restituisce un file PNG con una maschera applicata attorno all&#39;oggetto.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>[!UICONTROL Versione]</p>
      </td>
   <td>Il valore predefinito è 4,0</td> 
    </tr> 
    </tbody>
</table>

#### Crea un nuovo PSD (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questo modulo di azione crea un nuovo PSD con livelli opzionali e genera rappresentazioni o salvataggi come PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>Per ogni file che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e il tipo elencati.</p>
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

#### Crea rappresentazioni (legacy)

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
      <td role="rowheader">[!UICONTROL Output]</td>
      <td>
        <p>Per ogni file che si desidera creare, fare clic su Aggiungi elemento e immettere l'opzione di archiviazione, posizione, tipo e sovrascrittura nell'elenco.</p>
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
        <p>Percorso file [!UICONTROL (Output)]</p>
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

#### Modifica livelli di testo (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Esegui azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Questo modulo di azione modifica i livelli di testo in un file Photoshop. Potete immettere dettagli di modifica separati per più livelli nello stesso file.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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

#### Modifica livelli testo 2 (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Esegui azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Questo modulo di azione modifica un livello di testo su un file Photoshop.

Per modificare più livelli, utilizzare il modulo [Modifica livelli di testo](#edit-text-layers).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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
      <td role="rowheader">Archiviazione file di output di </td>
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


#### Esegui un’azione JSON (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Esegui azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Questo modulo di azione esegue azioni Photoshop utilizzando comandi JSON.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>Per ogni file che si desidera creare, fare clic su Aggiungi elemento e immettere l'opzione di archiviazione, posizione, tipo e sovrascrittura nell'elenco.</p>
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

#### Esegui sfocatura profondità (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.

Questo modulo di azione esegue Sfocatura profondità sul file selezionato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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

#### Esegui azioni Photoshop (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Esegui azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Questo modulo di azione esegue un’azione Photoshop sull’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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

#### Esegui ritaglio prodotto (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Esegui azioni, script e trasformazioni di Photoshop](#execute-photoshop-actions-scripts-and-transformations).

Questo modulo di azione esegue il ritaglio prodotto sull’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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

#### Ottieni informazioni livello (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo al modulo [Genera un manifesto](#generate-a-manifest).

Questo modulo di azione recupera le informazioni sui livelli dal file PSD specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">Archiviazione file di input </td>
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

#### Effettua chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://image.adobe.io/pie/psdService</code>. Esempio: <code>/photoshopActions</code></p>
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
      <td role="rowheader">[!UICONTROL Stringa di query]  </td>
      <td>
        <p>Inserisci la stringa di query della richiesta.</p>
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

#### Sostituire un oggetto avanzato (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questo modulo di azione sostituisce un oggetto avanzato all’interno di un livello PSD e genera nuove rappresentazioni.

Questo modulo utilizza Smart Object API versione 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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

#### Sostituire un oggetto avanzato 2 (legacy)

Questo modulo di azione sostituisce un oggetto avanzato all’interno di un livello PSD e genera nuove rappresentazioni.

Questo modulo utilizza la versione legacy di Smart Objects.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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

#### Ridimensionare un’immagine (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questa azione ridimensiona un’immagine utilizzando le stesse proporzioni.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
        <p>Per ogni file convertito che si desidera creare, fare clic su Aggiungi elemento e immettere l'archivio, il percorso e altre opzioni elencate.</p>
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

#### Filigrana di un’immagine (legacy)

>[!NOTE]
>
>Questo modulo è stato dichiarato obsoleto e non funzionerà più dopo il 30 luglio 2026.
>Aggiorna il modulo in [Crea o modifica un modulo composito](#create-or-edit-a-composite).

Questo modulo di azione aggiunge una filigrana all’immagine selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Photoshop], consulta <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Creare una connessione a [!DNL Adobe Photoshop]</a> in questo articolo.</td>
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
