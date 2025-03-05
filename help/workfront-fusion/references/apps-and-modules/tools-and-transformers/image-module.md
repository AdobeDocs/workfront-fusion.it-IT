---
title: Moduli immagine
description: I moduli immagine di Adobe Workfront Fusion consentono di ottenere informazioni su un’immagine specifica (dimensioni, tipo e così via), convertire un’immagine in un altro formato di file e modificare direttamente le dimensioni dell’immagine.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 3834bb9c7f07e0097783c44558fd656d455337b4
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Moduli immagine

I moduli [!DNL Adobe Workfront Fusion] [!UICONTROL Immagine] ti consentono di ottenere informazioni su un&#39;immagine specifica (dimensioni, tipo e così via), convertire un&#39;immagine in un altro formato di file e modificare direttamente le dimensioni dell&#39;immagine.

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
   <p>Nessuna licenza Workfront Fusion richiesta.</p>
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

## [!UICONTROL Moduli immagine] e relativi campi

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti. Un titolo in grassetto in un modulo indica un campo obbligatorio.

* [[!UICONTROL Convertire un formato]](#convert-a-format)
* [[!UICONTROL Estrai metadati]](#extract-metadata)
* [[!UICONTROL Ridimensiona]](#resize)

### [!UICONTROL Convertire un formato]

Questo modulo di trasformazione modifica il formato di un file di immagine. Questo modulo è compatibile con i seguenti formati:

* PNG
* JPG
* GIF
* BMP

Sia il file di origine che l&#39;output devono essere in uno di questi formati. Ad esempio, il modulo [!UICONTROL Immagine] >[!UICONTROL Converti un formato] può trasformare un file PNG in un file BMP o un BMP in un JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Formato di output]</td> 
   <td>Selezionare il formato in cui convertire il file di origine nel modulo. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Estrai metadati]

Questo modulo di trasformazione restituisce informazioni di base su un modulo.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Ridimensiona]

Questo modulo di trasformazione modifica l’altezza e la larghezza di un’immagine in base ai criteri specificati.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL che desidero]</td> 
   <td>Selezionate se desiderate mantenere le proporzioni tra altezza e larghezza oppure modificate le quote impostandole su un valore specificato per altezza e larghezza.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Secondo]</td> 
   <td> <p>Seleziona la modalità con cui vuoi che il modulo determini le nuove dimensioni dell'immagine. Questo campo viene visualizzato se si è selezionato di mantenere il rapporto altezza-larghezza nel campo che si desidera visualizzare. Altri campi vengono visualizzati in base alla selezione effettuata in questo campo.</p> 
    <ul> 
     <li> <p>[!UICONTROL Larghezza massima]</p> <p>Riduce l'immagine alla larghezza specificata. L'altezza viene calcolata automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altezza massima]</p> <p>Riduce l'altezza di un'immagine specificata. La larghezza viene calcolata automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altezza o larghezza massima]</p> <p>Riduce un'immagine in modo che la sua altezza e larghezza non superino i valori specificati. Poiché questa opzione mantiene il rapporto altezza-larghezza, una delle quote potrebbe essere inferiore a quella specificata. Ad esempio, se altezza e larghezza sono entrambe specificate come 40, un'immagine 400x300 verrà ridotta a 40x30.</p> </li> 
     <li> <p>[!UICONTROL larghezza minima]</p> <p>Ingrandisce un'immagine alla larghezza specificata. L'altezza viene calcolata automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altezza minima]</p> <p>Ingrandisce l'immagine all'altezza specificata. La larghezza viene calcolata automaticamente.</p> </li> 
     <li> <p>[!UICONTROL Altezza o larghezza minima]</p> <p>Ingrandisce un'immagine in modo che l'altezza e la larghezza non siano inferiori ai valori specificati. Poiché questa opzione mantiene il rapporto altezza-larghezza, una delle dimensioni potrebbe essere maggiore di quella specificata. Ad esempio, se altezza e larghezza sono entrambe specificate come 300, un'immagine 40x30 verrà ingrandita a 400X300.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>Modifica le dimensioni dell'immagine in base a una percentuale in base al valore specificato. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>Inserisci o mappa la larghezza desiderata dell’immagine ridimensionata in pixel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>Inserisci o mappa l’altezza desiderata dell’immagine ridimensionata in pixel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cambia per percentuale]</td> 
   <td>Se si è scelto di modificare l'immagine in percentuale, immettere o mappare la percentuale in base alla quale si desidera modificare l'immagine.</td> 
  </tr> 
 </tbody> 
</table>

## Risoluzione dei problemi

### Azione terminata con un errore

un&#39;azione può terminare con un errore a causa di una delle seguenti cause:

* I dati ricevuti non sono nel formato JPG/GIF/PNG/BMP
* È stato superato il limite massimo di larghezza/altezza durante la modifica delle dimensioni dell&#39;immagine. La dimensione dell&#39;immagine non deve superare i 3840 px di larghezza e 2160 px di altezza
* È stata superata la dimensione massima consentita per un’immagine durante la modifica delle dimensioni o del formato dell’immagine.
