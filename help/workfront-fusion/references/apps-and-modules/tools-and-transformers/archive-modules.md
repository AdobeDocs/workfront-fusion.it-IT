---
title: Moduli per archivi
description: In uno scenario Adobe Workfront Fusion, è possibile collegare un archivio, ad esempio un file compresso, a più applicazioni e servizi di terze parti. Ad esempio, puoi configurare uno scenario che
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
TQID: https://experienceleague.adobe.com/hcfjBqNDF3zEVJMLmekD-O8lmzMLyKk6Xp9JKTXcVWc
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 651
ht-degree: 32%

---

# [!UICONTROL Archivia] moduli

In uno scenario Adobe Workfront Fusion, puoi utilizzare un archivio, ad esempio un file compresso, per utilizzarlo nelle automazioni o nelle integrazioni.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## [!UICONTROL Archivia] moduli e relativi campi

Quando configuri i moduli [!UICONTROL Archivio], Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!UICONTROL Archivio], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Aggregatori](#aggregators)
* [Trasformatori](#transformers)

## Azioni

### [!UICONTROL Estrarre un archivio]

Questo modulo estrae un file identificato da un archivio.

Il modulo restituisce l’ID del file e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL File di origine]</td> 
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

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Modulo Source]</td> 
   <td> <p> Selezionare il modulo da cui si desidera recuperare i file.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo] </td> 
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
   <td>[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
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
