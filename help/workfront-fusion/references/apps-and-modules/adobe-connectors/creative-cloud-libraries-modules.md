---
title: Moduli di Adobe Creative Cloud Libraries
description: Con i moduli Libraries  [!DNL Adobe Workfront Fusion Adobe Creative Cloud] , puoi avviare uno scenario quando viene creato o aggiornato un elemento o una libreria. Puoi anche caricare, recuperare, archiviare o elencare elementi oppure effettuare una chiamata all'API  [!DNL Adobe Creative Cloud Libraries] .
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 1%

---

# Moduli Adobe Creative Cloud Libraries

Con i moduli di Adobe Workfront Fusion [!DNL Adobe Creative Cloud Libraries], puoi avviare uno scenario quando viene creato o aggiornato un elemento o una libreria. È inoltre possibile caricare, recuperare, archiviare o elencare elementi oppure effettuare una chiamata all&#39;API [!DNL Adobe Creative Cloud Libraries].

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

>[!IMPORTANT]
>
>La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.

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
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Adobe Creative Cloud Libraries], è necessario disporre di un account [!UICONTROL Adobe Creative Cloud].

## Informazioni API sulle librerie Adobe Creative Cloud

Il connettore Adobe Creative Cloud Libraries utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://cc-libraries.adobe.io/api/v1</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.1.7</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Moduli Librerie Adobe Creative Cloud] e relativi campi

Quando configuri [!UICONTROL moduli Librerie Adobe Creative Cloud], Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Creative Cloud Libraries], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Elementi](#elements)

* [Librerie](#libraries)

* [Altro](#other)


### Elementi

* [[!UICONTROL Archivia un elemento]](#archive-an-element)

* [[!UICONTROL Ottieni un elemento]](#get-an-element)

* [[!UICONTROL Elementi elenco]](#list-elements)

* [[!UICONTROL Carica un elemento]](#upload-an-element)

* [!UICONTROL [Guarda il nuovo elemento nella libreria]](#watch-new-element-in-library)

* [[!UICONTROL Guarda gli elementi aggiornati]](#watch-updated-elements)


#### [!UICONTROL Archivia un elemento]

Questo modulo di azione archivia un elemento da una libreria.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td >Seleziona o mappa la libreria che contiene l’elemento da archiviare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID elemento]</td>
      <td>Seleziona o mappa l’elemento da archiviare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Ottieni un elemento]

Questo modulo di azione restituisce un singolo elemento da una libreria.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td>Seleziona o mappa la libreria che contiene l’elemento da recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID elemento]</td>
      <td>Inserisci o mappa l’ID dell’elemento che desideri recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Seleziona il tipo di informazioni restituito dal modulo. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Predefinito]</b>
            </p>
            <p>Dati base</p>
          </li>
          <li>
            <p><b>[!UICONTROL Dettagli]</b>
            </p>
            <p>Tutti i dati disponibili</p>
          </li>
          <li>
            <p><b>[!UICONTROL Rappresentazioni]</b>
            </p>
            <p>Un elenco ridotto di risorse associate all’elemento libreria</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Elementi elenco]

Questo modulo di azione recupera un elenco di elementi in una libreria.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td >Seleziona o mappa la libreria da cui desideri elencare gli elementi.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ordina per]</td>
      <td>Seleziona se desideri ordinare i risultati per nome o in base all'ultima data in cui l'elemento è stato modificato.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type]</td>
      <td >Immetti o mappa un tipo MIME per limitare i risultati agli elementi identificati con il tipo MIME specificato. Esempio: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>Seleziona il tipo di informazioni restituito dal modulo. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL Predefinito]</b>
            </p>
            <p>Dati base</p>
          </li>
          <li>
            <p><b>[!UICONTROL Dettagli]</b>
            </p>
            <p>Tutti i dati disponibili</p>
          </li>
          <li>
            <p><b>[!UICONTROL Rappresentazioni]</b>
            </p>
            <p>Un elenco ridotto di risorse associate all’elemento libreria</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Guarda il nuovo elemento nella libreria]

Questo modulo di attivazione avvia uno scenario quando un elemento viene aggiunto a una libreria.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td >Seleziona la libreria di cui desideri monitorare gli elementi aggiornati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Guarda gli elementi aggiornati]

Questo modulo di attivazione avvia uno scenario quando un elemento in una libreria viene aggiornato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td >Seleziona la libreria da controllare per i nuovi elementi.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

### Librerie

* [[!UICONTROL Guarda le nuove librerie]](#watch-new-libraries)

* [[!UICONTROL Guarda le librerie aggiornate]](#watch-updated-libraries)


#### [!UICONTROL Guarda le nuove librerie]

Questo modulo di attivazione avvia uno scenario quando viene creata una nuova libreria.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Guarda le librerie aggiornate]

Questo modulo di attivazione avvia uno scenario quando viene aggiornata una libreria esistente.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

### Altro

* [Effettuare una chiamata API](#make-an-api-call)
* [Caricare una risorsa](#upload-an-asset)

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo effettua una chiamata API personalizzata all&#39;API [!DNL Adobe Creative Cloud Libraries].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Per istruzioni sulla connessione dell'account Adobe Creative Cloud a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base.</a></p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Immettere un percorso relativo a <code>https://cc-libraries.adobe.io/api</code>.</p>
    <p>Ad esempio <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL versione API]</td>
      <td>
        <p>Selezionare la versione dell'API [!DNL Adobe Analytics] a cui connettersi.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
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
      <td role="rowheader">[!UICONTROL Stringa Di Query]</td>
      <td>
        <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
       <tr>
      <td role="rowheader">[!UICONTROL Carica un documento transitorio]</td>
      <td>
      <p>Se si desidera caricare un documento transitorio, immettere il file di origine del documento che si desidera caricare.</p>
      <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p>
    </td>
    </tr>
</tbody>
</table>


#### [!UICONTROL Carica una risorsa]

Questo modulo di azione carica una risorsa di file di piccole dimensioni in una libreria esistente. La dimensione massima del file è di 1 GB.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Seleziona una connessione Creative Cloud Libraries esistente. La creazione di connessioni non è attualmente disponibile nel connettore Creative Cloud Libraries. Le connessioni esistenti funzionano come previsto.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID libreria]</td>
      <td >Seleziona la libreria in cui desideri caricare una risorsa.</td>
    </tr>
    <tr>
      <td role="rowheader">Modalità chiamata [!UICONTROL]</td>
      <td>
        <p>Seleziona la modalità di elaborazione con cui richiamare il processo di richiesta.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL sync]</b>
            </p>
            <p>La chiamata API viene elaborata in modo sincrono. La risposta viene consegnata al termine dell’elaborazione (a meno che la chiamata non venga interrotta per timeout).</p>
          </li>
          <li>
            <p><b>[!UICONTROL asincrono]</b>
            </p>
            <p>La risposta del monitoraggio asincrono viene restituita immediatamente e l’elaborazione delle richieste avviene in modo asincrono. La chiamata è responsabile del polling dell’endpoint fino al completamento.</p>
          </li>
          <li>
            <p><b>[!UICONTROL sync,async]</b> (impostazione predefinita)</p>
            <p>Tentativo di elaborazione sincrona della richiesta. Quando l’elaborazione si estende oltre 5000 ms, viene restituita la risposta del monitoraggio asincrono. L’URL di monitoraggio deve essere sottoposto a polling fino al completamento della richiesta.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Element Type]</td>
      <td >Seleziona il tipo di elemento da caricare</td>
    </tr>
    <tr>
      <td role="rowheader">Tipo di file [!UICONTROL]</td>
      <td >Immetti o mappa il tipo MIME del file caricato.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source File]</td>
      <td>
        <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p>
      </td>
    </tr>
  </tbody>
</table>





