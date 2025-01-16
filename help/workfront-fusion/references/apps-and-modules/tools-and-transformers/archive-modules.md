---
title: Moduli di archiviazione
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi collegare un archivio, ad esempio un file compresso, a più applicazioni e servizi di terze parti. Ad esempio, puoi configurare uno scenario che
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Archive] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile utilizzare un archivio, ad esempio un file compresso, nel proprio scenario, per utilizzarlo nelle automazioni o nelle integrazioni.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## [!UICONTROL Archive] moduli e relativi campi

Quando configuri [!UICONTROL Archive] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!UICONTROL Archive], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Extract an archive]](#extract-an-archive)
* [[!UICONTROL Create an archive]](#create-an-archive)
* [[!UICONTROL Inflate]](#inflate)
* [[!UICONTROL Deflate]](#deflate)

## [!UICONTROL Extract an archive]

Questo modulo estrae un file identificato da un archivio.

Il modulo restituisce l’ID del file e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p> Selezionate il file da estrarre. Questo file può essere mappato da un modulo precedente (ad esempio il modulo [!DNL Workfront] &gt;[!UICONTROL Download a document]).</p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** Ottieni il file ZIP dalla cartella [!DNL Dropbox] definita (ad esempio, Archivi), estrailo utilizzando il modulo [!UICONTROL Archive] e invia i file estratti all&#39;indirizzo e-mail desiderato come allegati con il modulo [!UICONTROL Email] o [!DNL Gmail].
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

## [!UICONTROL Create an archive]

Questo modulo aggregatore aggiunge i file desiderati a un archivio [!UICONTROL ZIP] o [!UICONTROL TAR].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Selezionare il modulo da cui si desidera recuperare i file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Specificare se si desidera aggiungere file a un archivio [!UICONTROL ZIP] o [!UICONTROL TAR].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Inserisci un commento da aggiungere all’archivio.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Definire un'espressione in base alla quale raggruppare l'output aggregato. Questa espressione può contenere uno o più elementi mappati. I dati aggregati verranno quindi separati in gruppi utilizzando il valore di questa espressione. Ogni gruppo produce come bundle separato con una chiave (l’espressione valutata) e un valore (il testo aggregato). Puoi utilizzare la chiave come filtro nei moduli successivi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Selezionare questa opzione per interrompere lo scenario quando non sono presenti risultati.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Immetti un nome per l’archivio creato. Non aggiungere un'estensione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** controlla le e-mail in arrivo utilizzando il modulo [!DNL Gmail] >[!UICONTROL Watch emails]. Se viene ricevuto un messaggio e-mail, gli allegati vengono iterati in singoli bundle, quindi archiviati nel file [!DNL ZIP] e salvati nella cartella di Dropbox definita.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

## [!UICONTROL Inflate]

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

## [!UICONTROL Deflate]

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
