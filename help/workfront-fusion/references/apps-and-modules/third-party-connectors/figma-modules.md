---
title: Moduli Figma
description: Con i moduli Adobe Workfront Fusion Figma è possibile recuperare elenchi di commenti, file, versioni di file o progetti. Puoi anche pubblicare un commento o effettuare una chiamata all’API Figma.
author: Becky
feature: Workfront Fusion
exl-id: 1220460b-1957-4dfc-b7c1-4c97b36ea061
source-git-commit: 545bc38a619c44dd39bb746d751775f63e7aa16d
workflow-type: tm+mt
source-wordcount: '2638'
ht-degree: 14%

---

# [!DNL Figma] moduli

Con i moduli di Adobe Workfront Fusion [!DNL Figma] è possibile recuperare elenchi di commenti, file, versioni di file o progetti. È inoltre possibile pubblicare un commento o effettuare una chiamata all&#39;API [!DNL Figma].

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze di Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza di Workfront Fusion</p>
   <p>Basata sul connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
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

Per utilizzare i moduli [!DNL Figma], è necessario disporre di un account [!DNL Figma].

## Informazioni API Figma

Il connettore Figma utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.figma.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.8.25</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione a Figma

>[!IMPORTANT]
>
>* Figma ha modificato i requisiti di autenticazione nel gennaio 2025. Il tipo di connessione `Figma` soddisfa i nuovi requisiti. Il tipo di connessione `Figma (Legacy)` è stato dichiarato obsoleto e verrà rimosso nel prossimo futuro.
>* Se si utilizza un reindirizzamento, URL, utilizzare `https://oauth.app.workfrontfusion.com/oauth/cb/figma3`.

Per creare una connessione per i moduli Figma:

1. In qualsiasi modulo Figma, fare clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi obbligatori:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
        <td>
          <p> Seleziona <code>Figma</code> senza il tag legacy. </p><p>Figma ha modificato i requisiti di autenticazione nel gennaio 2025. Il tipo di connessione <code>Figma</code> soddisfa i nuovi requisiti. Il tipo di connessione <code>Figma (Legacy)</code> è stato dichiarato obsoleto e verrà rimosso in futuro.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immetti il [!UICONTROL Figma] [!UICONTROL Client ID].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Immetti il segreto client Figma [!UICONTROL].</td>
        </tr>
        <tr>
        <td role="rowheader">Ambiti personalizzati</td>
        <td>Immettere gli ambiti personalizzati necessari per la connessione.</td>
        </tr>
        <tr>
        <td role="rowheader">URL di verifica connessione personalizzato</td>
        <td>L'endpoint predefinito per verificare che la connessione sia stata creata correttamente è: <code>https://api.figma.com/v1/me</code> Se questo URL non è supportato per l'ambito personalizzato, fornire un URL di verifica personalizzato.</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.



## Moduli [!DNL Figma] e relativi campi

Quando configuri i moduli [!DNL Figma], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Figma], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione mappatura](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Commenti](#comments)

* [Progetti e file](#projects-and-files)

* [Componenti e stili](#components-and-styles)

* [Altro](#other)


### Commenti

* [Eliminare un commento](#delete-a-comment)

* [Elenca commenti](#list-comments)

* [Pubblica un commento](#post-a-comment)


#### [!UICONTROL Elimina un commento]

Questo modulo elimina un singolo commento da un file.

<table style="table-layout:auto"> 
  <col/>
  <col />
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID file]</td>
      <td>Immettere o mappare l'ID file del file da cui si desidera aggiungere un commento. </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID commento]</td>
      <td>Immettere il testo del commento che si desidera eliminare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Elenca commenti]

Questo modulo di ricerca elenca tutti i commenti allegati a un singolo file in [!DNL Figma].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID file]</td>
      <td>
        <p>Immettere o mappare l'ID file per il quale si desidera recuperare i commenti. </p>
        <ul>
          <li>
            <p>Se non si conosce l'ID, fare clic su <b>[!UICONTROL Trova file]</b> e immettere o mappare l'ID del progetto a cui è associato il file, quindi selezionare il file.</p>
          </li>
          <li>
            <p>Se non si conosce l'ID del progetto, fare clic su <b>[!UICONTROL Trova progetti]</b> e immettere o mappare l'ID del team a cui appartiene il progetto a cui è associato il file, quindi selezionare il progetto e selezionare il file.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di commenti restituiti]</td>
      <td>Inserisci oppure mappa il numero massimo di commenti che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Pubblica un commento]

Questo modulo di azione pubblica un commento su un file Figma.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td  role="rowheader">[!UICONTROL ID file]</td>
      <td>
        <p>Immettere o mappare l'ID file del file in cui si desidera inserire un commento. </p>
        <ul>
          <li>
            <p>Se non si conosce l'ID del file, fare clic su <b>[!UICONTROL Trova file]</b> e immettere o mappare l'ID del progetto a cui è associato il file, quindi selezionare il file.</p>
          </li>
          <li>
            <p>Se si sta tentando di trovare l'ID del file e non si conosce l'ID del progetto, fare clic su <b>[!UICONTROL Trova progetti]</b> e immettere o mappare l'ID del team proprietario del progetto a cui è associato il file. Seleziona il progetto, quindi il file.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment]</td>
      <td>Immettere il testo del commento.</td>
    </tr>
  </tbody>
</table>


### Progetti e file

* [Ottenere un file o un&#39;immagine](#get-a-file-or-image)

* [Elencare la cronologia delle versioni dei file](#list-file-version-history)

* [Elencare file di progetto](#list-project-files)

* [Elenca progetti](#list-projects)


#### [!UICONTROL Ottieni un file o un&#39;immagine]

Questo modulo di azione recupera un singolo file o immagine da una libreria Figma

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di oggetto]</td>
      <td>
        <p>Selezionare il tipo di oggetto da recuperare.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL File]</b>
            </p>
            <p>Il modulo restituisce il documento a cui fa riferimento [!UICONTROL Key] come oggetto JSON. La chiave del file può essere analizzata da qualsiasi URL di file Figma.</p>
            <p>Per i campi, vedere <a href="#get-a-file-or-image-file" class="MCXref xref" >[!UICONTROL Ottenere un file o un'immagine: File]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Nodi file]</b>
            </p>
            <p>Restituisce i nodi a cui fanno riferimento gli ID come oggetto JSON. I nodi vengono recuperati dal file [!DNL Figma] a cui fa riferimento [!UICONTROL Key].</p>
            <p>Per i campi, vedere <a href="#get-a-file-or-image-file-nodes" class="MCXref xref" >[!UICONTROL Ottenere un file o un'immagine: Nodi di file]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image]</b>
            </p>
            <p>Il modulo esegue il rendering delle immagini da un file.</p>
            <p>Per i campi, vedere <a href="#get-a-file-or-image-image" class="MCXref xref" >[!UICONTROL Ottenere un file o un'immagine: Image]</a>.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Riempimenti immagine]</b>
            </p>
            <p>Il modulo restituisce i collegamenti di download per tutte le immagini presenti nei riempimenti immagine di un documento. I riempimenti di immagini rappresentano il modo in cui [!DNL Figma] rappresenta qualsiasi immagine fornita dall'utente. Quando si trascina un'immagine in [!DNL Figma], [!DNL Figma] crea un rettangolo con un singolo riempimento che rappresenta l'immagine e l'utente è in grado di trasformare il rettangolo (e le proprietà sul riempimento).</p>
            <p>Per i campi, vedere <a href="#get-a-file-or-image-image-fills" class="MCXref xref" >[!UICONTROL Ottenere un file o un'immagine: riempimenti immagine]</a>.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


##### Ottieni un file o un&#39;immagine: File

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File Key]</td>
      <td>Seleziona il file da cui vuoi restituire il JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID versione]</td>
      <td>Immettere o mappare la versione del file che si desidera venga restituita dal modulo. Per il modulo corrente, lascia vuoto questo campo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID nodo]</td>
      <td>
        <p>Per restituire solo un sottoinsieme del documento, immettere i nodi che si desidera restituire al modulo. Il modulo restituisce i nodi elencati, i relativi nodi secondari e qualsiasi cosa tra il nodo principale e i nodi elencati.</p>
        <p>Per ogni nodo da restituire, fare clic su <b>[!UICONTROL Add]</b> e immettere il testo del nodo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Immettere o mappare un numero intero che rappresenta la profondità nella struttura del documento per la quale si desidera restituire i risultati. </p>
        <div class="example"><span class="autonumber"><span><b>Esempio: </b></span></span>
          <ul>
            <li>
              <p>Per restituire solo le pagine, immettere <code>1</code>.</p>
            </li>
            <li>
              <p>Per restituire pagine e oggetti di primo livello, immettere <code>2</code>.</p>
            </li>
          </ul>
        </div>
        <p>Per restituire tutti i nodi, lascia vuoto questo campo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Per restituire dati vettoriali, immettere <code>paths</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Elenco separato da virgole di ID plug-in e/o stringa "[!UICONTROL shared]". Tutti i dati presenti nel documento scritto da tali plug-in verranno inclusi nel risultato nelle proprietà <code>pluginData</code> e <code>sharedPluginData</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Branch data]</td>
      <td>Abilita questa opzione per restituire i metadati del ramo per il file richiesto. Se il file è un ramo, la chiave del file principale viene inclusa nella risposta restituita. Se il file presenta rami, i relativi metadati vengono inclusi nella risposta restituita. Impostazione predefinita: <code>false</code>.</td>
    </tr>
  </tbody>
</table>

##### Ottenere un file o un&#39;immagine: Nodi di file

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File Key]</td>
      <td>Seleziona il file da cui vuoi restituire il JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID nodo]</td>
      <td>
        <p>Immettere i nodi che si desidera vengano restituiti e convertiti dal modulo</p>
        <p>Per ogni nodo da restituire, fare clic su <b>[!UICONTROL Add]</b> e immettere il testo del nodo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID versione]</td>
      <td>Immettere o mappare la versione del file che si desidera venga restituita dal modulo. Per il modulo corrente, lascia vuoto questo campo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>Immettere o mappare un numero intero che rappresenta la profondità nella struttura del documento per la quale si desidera restituire i risultati. </p>
        <div class="example"><span class="autonumber"><span><b>Esempio: </b></span></span>
          <ul>
            <li>
              <p>Per restituire solo le pagine, immettere <code>1</code>.</p>
            </li>
            <li>
              <p>Per restituire pagine e oggetti di primo livello, immettere <code>2</code>.</p>
            </li>
          </ul>
        </div>
        <p>Per restituire tutti i nodi, lascia vuoto questo campo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>Per restituire dati vettoriali, immettere <code>paths</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>Elenco separato da virgole di ID plug-in e/o stringa "shared" (condiviso). Tutti i dati presenti nel documento scritto da tali plug-in verranno inclusi nel risultato nelle proprietà pluginData e sharedPluginData.</td>
    </tr>
  </tbody>
</table>


##### Ottieni un file o un’immagine: immagine

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File Key]</td>
      <td>Seleziona il file da cui vuoi restituire il JSON.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID nodo]</td>
      <td>
        <p>Immetti i nodi di cui vuoi eseguire il rendering nel modulo.</p>
        <p>Per ogni nodo di cui si desidera eseguire il rendering, fare clic su <b>[!UICONTROL Add]</b> e immettere il testo del nodo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Scale]</td>
      <td>Per ridimensionare l'immagine, immettete o mappate il fattore di scala. Questo numero deve essere compreso tra 0,01 e 4.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Format]</td>
      <td>
        <p>Selezionate il formato per l'output dell'immagine.</p>
        <ul>
          <li>
            <p>JPG</p>
          </li>
          <li>
            <p>PNG</p>
          </li>
          <li>
            <p>SVG</p>
          </li>
          <li>
            <p>PDF</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - ID inclusione]</td>
      <td>Abilita questa opzione per includere gli attributi ID per tutti gli elementi SVG. Impostazione predefinita: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Tratto semplificato]</td>
      <td>Abilita questa opzione per semplificare i tratti interni ed esterni e se possibile utilizza l'attributo tratto anziché &lt;mask&gt;. Impostazione predefinita: [!UICONTROL true].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Usa limiti assoluti]</td>
      <td>Abilita questa opzione per utilizzare le dimensioni complete del nodo indipendentemente dal fatto che sia ritagliato o meno o che lo spazio intorno a esso sia vuoto. Utilizzare questa opzione per esportare nodi di testo senza ritaglio. Impostazione predefinita: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL versione]</td>
      <td>Immettere o mappare la versione del file che si desidera venga restituita dal modulo. Per il modulo corrente, lascia vuoto questo campo.</td>
    </tr>
  </tbody>
</table>

##### Ottenere un file o un’immagine: riempimenti immagine

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File Key]</td>
      <td>Seleziona il file da cui vuoi restituire il JSON.</td>
    </tr>
  </tbody>
</table>

### [!UICONTROL Elenca cronologia versioni file]

Questo modulo di ricerca restituisce la cronologia delle versioni di un singolo file in [!UICONTROL Figma].
<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    <tr>
      <td role="rowheader">[!UICONTROL ID file]</td>
      <td>
        <p>Immetti o mappa l’ID file per il quale desideri recuperare la cronologia delle versioni. </p>
        <ul>
          <li>
            <p>Se non si conosce l'ID del file, fare clic su <b>[!UICONTROL Trova file]</b> e immettere o mappare l'ID del progetto a cui è associato il file, quindi selezionare il file.</p>
          </li>
          <li>
            <p>Se si sta tentando di trovare l'ID del file e non si conosce l'ID del progetto, fare clic su <b>[!UICONTROL Trova progetti]</b> e immettere o mappare l'ID del team proprietario del progetto a cui è associato il file. Seleziona il progetto, quindi il file.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di file restituiti]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Elenca file di progetto]

Questo modulo di ricerca restituisce un elenco di tutti i file nel progetto specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID file]</td>
      <td>
        <p>Immetti o mappa l’ID del progetto per il quale desideri recuperare i file. </p>
        <ul>
          <li>
            <p>Se non conosci l'ID del progetto, fai clic su <b>[!UICONTROL Trova progetti]</b> e immetti o mappa l'ID del team a cui è associato il progetto, quindi seleziona il progetto.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di file restituiti]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Elencare progetti]

Questo modulo di ricerca restituisce un elenco di tutti i progetti all’interno del team specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID team]</td>
      <td>Immetti o mappa l’ID del progetto per il quale desideri recuperare i file. L’ID del team si trova nell’URL della pagina del team a Figma</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Numero massimo di progetti restituiti]</td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
    </tr>
  </tbody>
</table>


### Componenti e stili

#### [!UICONTROL Ottieni uno stile o un componente]

Questo modulo di azione recupera un singolo stile o componente oppure un set di stili o componenti.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">Oggetto&gt; tipo</td>
      <td>Selezionare il tipo di oggetto da recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">&lt;[!UICONTROL Object&gt; chiave]</td>
      <td>Immettere la chiave (identificatore univoco) dell'oggetto da recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL ID team]</td>
      <td>Se si recupera un componente o un set di componenti del team, immettere o mappare l'ID del team a cui sono associati il record o i record.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dimensioni Pagina]</td>
      <td>Se si recupera un componente o un set di componenti team, immettere o mappare il numero o i risultati da restituire per pagina. Predefinito: 30.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL After]</td>
      <td>
        <p>Se si recupera un componente o un set di componenti del team, immettere o mappare il numero del risultato dopo il quale iniziare a recuperare i risultati. Questo può essere combinato con il campo [!UICONTROL Dimensioni pagina] per impaginare i risultati.</p>
        <p>Questo valore non corrisponde agli ID oggetto.</p>
        <p>Questo campo non può essere utilizzato in combinazione con il campo [!UICONTROL Before].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Before]</td>
      <td>
        <p>Se si recupera un componente o un set di componenti del team, immettere o mappare il numero del risultato prima del quale iniziare a recuperare i risultati. Questo può essere combinato con il campo [!UICONTROL Dimensioni pagina] per impaginare i risultati.</p>
        <p>Questo valore non corrisponde agli ID oggetto.</p>
        <p>Questo campo non può essere utilizzato in combinazione con il campo [!UICONTROL After].</p>
      </td>
    </tr>
  </tbody>
</table>


### Altro

* [Effettuare una chiamata API](#make-an-api-call)

* [Guarda gli eventi](#watch-events)


#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API Figma senza dover ricorrere all’autenticazione. In questo modo, puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli Figma.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td> <p>Per istruzioni sulla connessione dell'account [!DNL Figma] a Workfront Fusion, vedere <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Creare una connessione a Figma</a> in questo articolo.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Immettere un percorso relativo a <code>https://api.figma.com/v1/</code>.</p>
        <p>Ad esempio: <code>[!DNL files/7179110/comments]</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metodo]</td>
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
      <td role="rowheader">[!UICONTROL Stringa Di Query]</td>
      <td>
        <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> in JSON, inserisci le virgolette al di fuori dell’istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Guarda gli eventi]

Questo modulo trigger avvia uno scenario quando si verifica uno dei seguenti eventi per un team specifico nello spazio del team [!DNL Figma]:

* Aggiornamento file

* Aggiornamento versione file

* Eliminazione file

* Pubblicazione libreria

* Commento file

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>
        <p>Seleziona il webhook controllato dal modulo.</p>
        <p>Per aggiungere un nuovo webhook:</p>
        <ol>
          <li>
            <p>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL Webhook].</p>
          </li>
          <li>
            <p>Immettere un nome per il webhook.</p>
          </li>
          <li>
            <p>Selezionare la connessione da utilizzare per questo webhook. Per istruzioni sulla connessione dell'account [!DNL Figma] a [!UICONTROL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base.</a></p>
          </li>
          <li>
            <p>Seleziona il tipo di evento che desideri che il modulo controlli.</p>
          </li>
          <li>
            <p>Immetti l’ID del team di cui desideri che il webhook guardi gli eventi.</p>
          </li>
          <li>
            <p>Seleziona se desideri che il webhook sia attivo o in pausa.</p>
          </li>
          <li>
            <p>Immettere una descrizione per il webhook.</p>
          </li>
          <li>
            <p>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo.</p>
          </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
