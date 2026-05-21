---
title: Moduli Widen
description: In uno scenario di Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!UICONTROL Widen], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
TQID: https://experienceleague.adobe.com/joW38nxn0gj6qr1bd1RMS2RT2xOd2KgUsA-M8l57-ys
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1673
ht-degree: 30%

---

# Moduli [!DNL Widen]

In uno scenario di Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!UICONTROL Widen], nonché collegarli a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Per utilizzare i moduli [!UICONTROL Widen], è necessario disporre di un account [!UICONTROL Widen].

## Informazioni API Widen

Il connettore Widen utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL Widen] a Workfront Fusion  {#connect-widen-to-workfront-fusion}

Puoi creare una connessione al tuo account [!DNL Widen] direttamente da un modulo [!DNL Widen].

1. In qualsiasi modulo [!DNL Widen], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Seleziona l’ambiente e il tipo di account a cui ti stai connettendo. Questo è solo a scopo informativo e viene visualizzato nell&#39;area Connessioni di Fusion.
1. Selezionare il dominio [!DNL Widen] a cui connettersi.
1. Immetti il token per l&#39;account [!DNL Widen]. Per istruzioni su come individuare questo token, consulta le [[!DNL Widen] domande frequenti sulle API](https://community.widen.com/collective/s/article/API-FAQs).
1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## Moduli [!DNL Widen] e relativi campi

Quando configuri i moduli [!DNL Widen], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Widen], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Moduli trigger](#trigger-modules)
* [Moduli azione](#action-modules)
* [Cerca moduli](#search-modules)

### Moduli trigger

#### [!UICONTROL Risorse da controllare]

Questo modulo di attivazione avvia uno scenario quando una risorsa viene creata o aggiornata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo evento]</td> 
   <td> <p>Seleziona se desideri controllare le nuove risorse o le risorse aggiornate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Seleziona le proprietà da includere nell’output del modulo oltre ai campi della risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi da includere nell'output del modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Immettere o mappare il numero massimo di risorse con cui si desidera che il modulo funzioni durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Moduli azione

* [[!UICONTROL Aggiungere risorse alle raccolte]](#add-assets-to-collections)
* [[!UICONTROL Chiamata API personalizzata]](#custom-api-call)
* [[!UICONTROL Scarica file]](#download-file)
* [[!UICONTROL Leggi informazioni risorsa]](#read-asset-info)
* [[!UICONTROL Rimuovi risorse dalla raccolta]](#remove-assets-from-collection)
* [[!UICONTROL Aggiorna metadati risorsa]](#update-asset-metadata)
* [[!UICONTROL Caricare un file]](#upload-a-file)

#### [!UICONTROL Aggiungere risorse alle raccolte]

Questo modulo di azione aggiunge una o più risorse alle raccolte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Raccolte]</td> 
   <td>Per ogni raccolta a cui si desidera aggiungere le risorse, fare clic su <strong>[ID raccolta]</strong> e immettere o mappare l'ID raccolta .</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Per ogni risorsa da aggiungere a una raccolta, fai clic su <strong>[!UICONTROL Assets ID]</strong> e immetti o mappa l'ID risorsa.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Immettere o mappare il numero massimo di risorse con cui si desidera che il modulo funzioni durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Widen]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Widen].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL versione API]</td> 
   <td>Specificare se si desidera utilizzare la versione più recente dell'API [!DNL Widen] o la versione 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci o mappa l’URL per la chiamata API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica file]

Questo modulo di azione scarica una risorsa dal tuo account [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa]</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa da scaricare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi informazioni risorsa]

Questo modulo di azione recupera una singola risorsa in base al suo ID univoco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa]</td> 
   <td> <p>Immetti o mappa l’ID della risorsa per la quale desideri leggere le informazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Seleziona le proprietà da includere nell’output del modulo oltre ai campi della risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi da includere nell'output del modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rimuovi risorse dalla raccolta]

Questo modulo di azione rimuove una o più risorse dalle raccolte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Raccolte]</td> 
   <td>Per ogni raccolta da cui si desidera rimuovere le risorse, fare clic su <strong>[ID raccolta]</strong> e immettere o mappare l'ID raccolta .</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> Per ogni risorsa da rimuovere da una raccolta, fai clic su <strong>[!UICONTROL Assets ID]</strong> e immetti o mappa l'ID risorsa.</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Immettere o mappare il numero massimo di risorse con cui si desidera che il modulo funzioni durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna metadati risorsa]

Questo modulo di azione aggiorna i campi di metadati di una risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa]</td> 
   <td> <p>Inserisci o mappa l’ID della risorsa in cui desideri aggiornare i metadati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo metadati]</td> 
   <td> <p>Seleziona il tipo di metadati per i metadati da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metadati di </td> 
   <td>Seleziona i campi di metadati da aggiornare. Immettere il nuovo valore per ogni campo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Immettere o mappare il numero massimo di risorse con cui si desidera che il modulo funzioni durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Caricare un file]

Questo modulo di azione carica un file nel tuo account [!DNL Widen].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Carica profilo]</td> 
   <td> <p>Seleziona il profilo di caricamento che desideri utilizzare per il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>Seleziona la modalità di caricamento del file.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Dal File]</strong> </p> <p>Seleziona o mappa il file di origine da un modulo precedente.</p> </li> 
     <li> <p><strong>[!UICONTROL Per URL]</strong> </p> <p>Inserisci o mappa l’URL del file da caricare.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome file]</td> 
   <td>Inserisci o mappa un nome per il file caricato.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo metadati]</td> 
   <td>Seleziona il tipo di metadati per il file da caricare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metadati di </td> 
   <td>Seleziona i campi di metadati da includere nel caricamento del file. Per ogni campo, immettere il valore  per il campo.</td> 
  </tr> 
 </tbody> 
</table>

### Cerca moduli

* [[!UICONTROL Leggi risorse raccolta]](#read-collection-assets)
* [[!UICONTROL Cerca risorse]](#search-assets)

#### [!UICONTROL Leggi risorse raccolta]

Questo modulo di azione recupera un elenco di risorse all’interno di una raccolta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID raccolta]</td> 
   <td> <p>Inserisci o mappa l’ID della raccolta che contiene le risorse da leggere.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Immettere o mappare il numero del primo elemento da elencare. Questo è un modo per impaginare i record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Seleziona la proprietà in base alla quale desideri ordinare le risorse. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Seleziona se desideri ordinare le risorse in modo crescente o decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi da includere nell'output del modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca risorse]

Questo modulo di ricerca recupera un elenco di risorse che corrispondono ai criteri di ricerca specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
  <td> <p>Per istruzioni sulla connessione dell'account [!DNL Widen] a Workfront Fusion, vedere <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">Connettere [!DNL Widen] a Workfront Fusion </a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Query di ricerca </td> 
   <td> <p>Inserire i criteri in base ai quali si desidera cercare le risorse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Seleziona la modalità di ordinamento delle risorse. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>Seleziona se desideri ordinare le risorse in modo crescente o decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include eliminato]</td> 
   <td>Abilita questa opzione per includere le risorse eliminate nella ricerca.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archiviato]</p> </td> 
   <td> <p>Abilita questa opzione per includere le risorse archiviate nella ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cerca testo documento]</td> 
   <td>Abilita questa opzione per includere il testo del documento nella ricerca oppure imposta questa opzione su false per includere solo le risorse il cui titolo corrisponde ai criteri di ricerca.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>Immettere o mappare il numero del primo elemento per il quale si desidera recuperare i dettagli. Questo è un modo per impaginare i record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>Abilita questa opzione per consentire lo scorrimento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>Seleziona le proprietà da includere nell’output del modulo oltre ai campi della risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td>Selezionare i campi da includere nell'output del modulo.</td> 
  </tr> 
 </tbody> 
</table>
