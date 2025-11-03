---
title: Moduli di archiviazione
description: In uno scenario Adobe Workfront Fusion, è possibile collegare un archivio, ad esempio un file compresso, a più applicazioni e servizi di terze parti. Ad esempio, puoi configurare uno scenario che
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# [!UICONTROL Archivia] moduli

In uno scenario Adobe Workfront Fusion, puoi utilizzare un archivio, ad esempio un file compresso, per utilizzarlo nelle automazioni o nelle integrazioni.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## [!UICONTROL Archivia] moduli e relativi campi

Quando configuri i moduli [!UICONTROL Archivio], Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!UICONTROL Archivio], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Aggregatori](#aggregators)
* [Trasformatori](#transformers)

## Azioni

### [!UICONTROL Estrarre un archivio]

Questo modulo estrae un file identificato da un archivio.

Il modulo restituisce l’ID del file e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>  <p>Selezionare un file di origine da un modulo precedente o mappare i dati di origine.</p></p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Esempio:** Ottieni il file ZIP dalla cartella [!DNL Dropbox] definita (ad esempio, Archivi), estrailo utilizzando il modulo [!UICONTROL Archivio] e invia i file estratti all&#39;indirizzo e-mail desiderato come allegati con il modulo [!UICONTROL E-mail] o [!DNL Gmail].

![Esempio di Dropbox](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

>[!ENDSHADEBOX]

## Aggregatori

### [!UICONTROL Crea un archivio]

Questo modulo aggregatore aggiunge i file desiderati a un archivio [!UICONTROL ZIP], GZIP o [!UICONTROL TAR].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Modulo Source]</td> 
   <td> <p> Selezionare il modulo da cui si desidera recuperare i file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Seleziona se desideri aggiungere file a un archivio [!UICONTROL ZIP], GZIP o [!UICONTROL TAR].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Inserisci un commento da aggiungere all’archivio.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Raggruppa per]</td> 
   <td> <p>Definire un'espressione in base alla quale raggruppare l'output aggregato. Questa espressione può contenere uno o più elementi mappati. I dati aggregati verranno quindi separati in gruppi utilizzando il valore di questa espressione. Ogni gruppo produce come bundle separato con una chiave (l’espressione valutata) e un valore (il testo aggregato). Puoi utilizzare la chiave come filtro nei moduli successivi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Interrompi elaborazione dopo un'aggregazione vuota]</td> 
   <td>Selezionare questa opzione per interrompere lo scenario quando non sono presenti risultati.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome archivio]</td> 
   <td> <p> Immetti un nome per l’archivio creato. Non aggiungere un'estensione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Esempio:** controlla le e-mail in arrivo utilizzando il modulo [!DNL Gmail] >[!UICONTROL Controlla e-mail]. Se viene ricevuto un messaggio e-mail, gli allegati vengono iterati in singoli bundle, quindi archiviati nel file [!DNL ZIP] e salvati nella cartella Dropbox definita.

![Esempio Di Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

>[!ENDSHADEBOX]

## Trasformatori

* [[!UICONTROL Deflazione]](#deflate)
* [[!UICONTROL Gonfiare]](#inflate)

### [!UICONTROL Deflazione]

Questo modulo di trasformazione comprime i dati binari utilizzando un algoritmo di deflazione.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Immettere o mappare i dati da comprimere utilizzando la funzione di deflazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Gonfiare]

Questo modulo di trasformazione decomprime i dati binari utilizzando un algoritmo di inflazione.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Immettere o mappare i dati da decomprimere utilizzando la funzione di gonfiaggio.</p> </td> 
  </tr> 
 </tbody> 
</table>
