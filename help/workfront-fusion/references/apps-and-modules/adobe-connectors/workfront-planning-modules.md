---
title: Moduli di Adobe Workfront Planning
description: Con i moduli  [!DNL Adobe Workfront Planning] , puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell'account Workfront Planning  [!DNL Adobe] , creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 1%

---

# [!DNL Adobe Workfront Planning] moduli

Con i moduli [!DNL Adobe Workfront Planning] è possibile attivare uno scenario quando si verificano eventi in Workfront Planning. È inoltre possibile creare, leggere, aggiornare ed eliminare record oppure eseguire una chiamata API personalizzata all&#39;account [!DNL Adobe Workfront Planning].

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

+++## Prerequisiti

Per accedere a Workfront Planning, è necessario disporre dei seguenti elementi:

* Un nuovo pacchetto Workfront e una nuova licenza. Workfront Planning non è disponibile per i pacchetti o le licenze legacy di Workfront.
* Un pacchetto di Workfront Planning.
* L’istanza di Workfront della tua organizzazione deve essere integrata in Adobe Unified Experience.

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

Puoi creare una connessione al tuo account [!DNL Workfront Planning] direttamente da un modulo Workfront Fusion.

1. In qualsiasi modulo di [!DNL Adobe Workfront Planning], fare clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

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
          <td>Seleziona se ti interessa la connessione a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]<p>(Facoltativo)</p></td>
          <td>Immetti l'ID client [!DNL Adobe] . È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segreto client]<p>(Facoltativo)</p></td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL URL autenticazione]</td>
          <td>Immetti l’URL che verrà utilizzato dall’istanza di Workfront per autenticare questa connessione. <p>Il valore predefinito è <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Prefisso host]</td>
          <td>Immetti il prefisso host.<p>Il valore predefinito è <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## [!DNL Adobe Workfront Planning] moduli e relativi campi

Quando configuri i moduli di Workfront, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi Workfront aggiuntivi, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)
* [Non categorizzato](#uncategorized)

### Trigger

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
      <td role="rowheader">[!UICONTROL Tipo di oggetto]</td>
      <td>Specificare se si desidera controllare record, tipi di record o aree di lavoro.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL Nuovo stato]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p></li><li><p><b>[!UICONTROL Old State]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> a un determinato valore.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Se si desidera controllare i record, selezionare il Workspace che si desidera controllare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di record]</td>
      <td>Se si desidera controllare i record, selezionare il tipo di record che si desidera controllare.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>È possibile impostare i filtri per controllare solo i record che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND.</p> <p>Nota: non è possibile modificare i filtri nei webhook Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni di eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.</p> <p>Per ulteriori informazioni sui filtri eventi, vedere <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri di sottoscrizione eventi nei moduli Workfront &gt; [!UICONTROL Watch Events]</a> nell'articolo Moduli Workfront.</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Oggetti da controllare]</td>
      <td>Seleziona se desideri controllare le nuove. record aggiornati, nuovi e aggiornati o eliminati.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Escludi aggiornamenti effettuati da questa connessione]</p>
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
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Immettere o mappare l'ID del tipo di record che si desidera eliminare.</td> 
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
      <td role="rowheader">[!UICONTROL Stringa Di Query]  </td>
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


### Ricerche

#### Cerca record

Questo modulo di azione recupera un elenco di record in base ai criteri specificati.

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
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Immettere o mappare il Workspace contenente i record che si desidera cercare.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record che si desidera cercare.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Campi Record]</p>
      </td>
      <td>Per ogni campo che si desidera utilizzare nella ricerca, individuare tale campo, selezionare l'operatore e immettere o mappare il valore che si desidera cercare. I campi sono disponibili in base al tipo di record selezionato.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Condizione [!UICONTROL per filtri]</p>
      </td>
      <td>Seleziona la condizione per i filtri:<ul><li><b>E</b><p>Il modulo restituisce record che soddisfano <b>tutti</b> i valori di campo selezionati.</p></li><li><b>O</b><p>Il modulo restituisce record che soddisfano <b>qualsiasi</b> dei valori di campo selezionati.</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
      </tr>
  </tbody>
</table>


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
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Immettere o mappare il tipo di record che si desidera creare. I tipi di record disponibili sono basati sull'account Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Immettere i valori desiderati per il nuovo record. Questi campi si basano sul tipo di record selezionato.</td> 
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
        <p>[!UICONTROL ID record]</p>
      </td>
      <td>Immettere o mappare l'ID del record che si desidera eliminare.</td> 
      </tr>
  </tbody>
</table>

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
      <td role="rowheader">[!UICONTROL ID record]</td>
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
      <td role="rowheader">[!UICONTROL Tipo di record]</td>
      <td>Selezionare il tipo di record da recuperare.</td>
    </tr>
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
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
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Selezionare o mappare l'area di lavoro contenente i tipi di record che si desidera recuperare.</td>
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
        <p>[!UICONTROL ID record]</p>
      </td>
      <td>Immettere o mappare il tipo di record che si desidera aggiornare. I tipi di record disponibili sono basati sull'account Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Immettere i nuovi valori che si desidera assegnare al record. Questi campi si basano sul tipo di record selezionato.</td> 
      </tr>
     <tr>
  </tbody>
</table>


## Usa JSONata per raggruppamenti di `record-types` leggibili

La seguente espressione JSONata crea un output leggibile della query di Planning che fornisce la suddivisione per tipi di record. In questo modo il nome del tipo di record, i nomi dei campi e i nomi delle opzioni di campo (se applicabile) sono leggibili da un nome e il resto della struttura rimane intatto.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Per informazioni sull&#39;utilizzo dei moduli JSONata, vedere [Moduli JSONata](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

