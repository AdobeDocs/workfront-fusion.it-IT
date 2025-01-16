---
title: Moduli di Adobe Workfront Planning
description: Con i  [!DNL Adobe Workfront Planning] moduli, puoi avviare uno  [!DNL Adobe Workfront Fusion] scenario basato sugli eventi nel tuo [!DNL Adobe] account Workfront Planning, creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 1972e445e7d4d3e4441feeda72ba9523fd1d9ff4
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning] moduli

Con i moduli [!DNL Adobe Workfront Planning] è possibile attivare uno scenario quando si verificano eventi in Workfront Planning. È inoltre possibile creare, leggere, aggiornare ed eliminare record oppure eseguire una chiamata API personalizzata all&#39;account [!DNL Adobe Workfront Planning].

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informazioni API di Adobe Workfront Planning

Il connettore Adobe Workfront Planning utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Crea una connessione a [!DNL Adobe Workfront Planning] {#create-a-connection-to-adobe-workfront-planning}

Puoi creare una connessione al tuo account [!DNL Workfront Planning] direttamente da un modulo [!DNL Workfront Fusion].

1. In qualsiasi modulo [!DNL Adobe Workfront Planning], fare clic su **[!UICONTROL Add]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
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
          <td>Seleziona se ti interessa la connessione a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Facoltativo)</p></td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client ID]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Facoltativo)</p></td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Facoltativo)</p></td>
          <td>Immetti l’URL che verrà utilizzato dall’istanza di Workfront per autenticare questa connessione. <p>Il valore predefinito è <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Immetti il prefisso host.<p>Il valore predefinito è <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.

## [!DNL Adobe Workfront Planning] moduli e relativi campi

### Triggers

#### Guarda gli eventi

Questo modulo di attivazione avvia uno scenario quando un record, un tipo di record o un&#39;area di lavoro viene creata, aggiornata o eliminata in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selezionare il webhook che si desidera utilizzare o fare clic su Aggiungi per crearne uno nuovo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Specificare se si desidera controllare record, tipi di record o aree di lavoro.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> a un determinato valore.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Se si desidera controllare i record, selezionare il Workspace che si desidera controllare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Se si desidera controllare i record, selezionare il tipo di record che si desidera controllare.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>È possibile impostare i filtri per controllare solo i record che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND.</p> <p>Nota: non è possibile modificare i filtri nei webhook [!DNL Workfront] esistenti. Per impostare filtri diversi per le sottoscrizioni di eventi [!DNL Workfront], rimuovere il webhook corrente e crearne uno nuovo.</p> <p>Per ulteriori informazioni sui filtri eventi, vedere <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri sottoscrizioni eventi nell'articolo [!DNL Workfront] &gt; [!UICONTROL Watch Events] moduli</a> nei moduli di Workfront.</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Seleziona se desideri controllare le nuove. record aggiornati, nuovi e aggiornati o eliminati.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Abilita questa opzione per impedire che lo scenario venga attivato quando viene apportata una modifica dalla connessione utilizzata da questo modulo. Questo impedisce l’attivazione di un’altra istanza dello scenario se questo esegue un’azione di attivazione.</td> 
      </tr>
  </tbody>
</table>

### Azioni

* [Eliminare un tipo di record](#delete-a-record-type)
* [Effettuare una chiamata AI personalizzata](#make-a-custom-api-call)

#### Eliminare un tipo di record

Questo modulo di azione elimina un singolo tipo di record in Workfront Planning dal relativo ID.

>[!WARNING]
>
>L&#39;eliminazione di un tipo di record in Workfront Planning comporta anche l&#39;eliminazione di tutti i record nella tabella dei tipi di record.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Immetti o mappa l’ID del campo da eliminare.</td> 
      </tr>
  </tbody>
</table>

#### Effettuare una chiamata API personalizzata

Questo modulo effettua una chiamata API personalizzata all&#39;API [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Per ogni coppia chiave/valore che si desidera aggiungere alla stringa di query, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore.</p>
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

<!--
### Searches

#### Search records

This action module retrieves a list of records based on criteria you specify.

-->

### Non categorizzato


#### Creare un record

Questa azione consente di creare un singolo record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Immettere o mappare il tipo di record che si desidera creare. I tipi di record disponibili sono basati sull'account Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Questi campi si basano sul tipo di record selezionato.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### Eliminare un record

Questo modulo di azione elimina il record specificato in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Immettere o mappare l'ID del record che si desidera eliminare.</td> 
      </tr>
  </tbody>
</table>

<!--

### Get all records

This action module retrieves all records from an [!DNL Adobe Workfront Planning] account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

-->

### Ottieni un record

Questo modulo azioni recupera un singolo record da [!DNL Adobe Workfront Planning], specificato dal relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record ID]</td>
      <td>Immettere o mappare l'ID del record che si desidera recuperare.</td>
    </tr>
  </tbody>
</table>

### Ottieni record per tipo di record

Questo modulo di azione recupera tutti i record del tipo specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selezionare o mappare l'area di lavoro contenente i record da recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Selezionare il tipo di record da recuperare.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tbody>
</table>

### Recupera tipi di record

Questo modulo di azione recupera un elenco di tipi di record in un account [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
  </tbody>
</table>

### Aggiorna record

Questa azione aggiorna un singolo record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], vedere <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Immettere o mappare il tipo di record che si desidera aggiornare. I tipi di record disponibili sono basati sull'account Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Questi campi si basano sul tipo di record selezionato.</td> 
      </tr>
     <tr>
  </tbody>
</table>
