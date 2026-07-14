---
title: Moduli Adobe Workfront - Pianificazione
description: Con i moduli  [!DNL Adobe Workfront Planning] , puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nell'account Workfront Planning  [!DNL Adobe] , creare, leggere o aggiornare contratti e altri record, cercare i record utilizzando i criteri impostati e caricare i documenti.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 35%

---


# Moduli Adobe Workfront - Pianificazione

Con i moduli [!DNL Adobe Workfront Planning] è possibile attivare uno scenario quando si verificano eventi in Workfront Planning. È inoltre possibile creare, leggere, aggiornare ed eliminare record oppure eseguire una chiamata API personalizzata all&#39;account [!DNL Adobe Workfront Planning].

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

## Prerequisiti

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
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Connessione di Workfront Planning a Workfront Fusion

Il connettore Workfront Planning utilizza OAuth 2.0 per connettersi a Workfront Planning.

È possibile creare una connessione all&#39;account Workfront Planning direttamente da un modulo Workfront Planning Fusion.

* [Connessione a Workfront Planning tramite ID client e segreto client](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Connettersi a Workfront Planning utilizzando una connessione server-to-server](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Connessione a Workfront Planning tramite ID client e segreto client

1. In qualsiasi modulo di Adobe Workfront Planning, fare clic su **Aggiungi** accanto al campo Connessione.
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
          <p>Seleziona la connessione <b>Adobe Workfront auth</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Inserisci un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Inserisci il tuo ID client. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Apri l’applicazione specifica a cui ti stai connettendo per visualizzare l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il Segreto client di Workfront. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Se non disponi di un Segreto client per l’applicazione OAuth2 in Workfront, puoi generarne un altro. Per istruzioni, consulta la documentazione di Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL di autenticazione]</td>
        <td>Questo può rimanere il valore predefinito, oppure puoi inserire l’URL dell’istanza Workfront, seguito da <code>/integrations/oauth2</code>. <p>Esempio: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Prefisso host]</td>
        <td>Nella maggior parte dei casi, questo valore deve essere <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

   Se non si è connessi a Workfront Planning, viene visualizzata una schermata di accesso. Dopo aver effettuato l’accesso, puoi autorizzare la connessione.

>[!NOTE]
>
>* Le connessioni OAuth 2.0 all’API Workfront non sono più basate sulle chiavi API.
>* Per creare una connessione a un ambiente sandbox di Workfront, è necessario creare un’applicazione OAuth2 in tale ambiente e quindi utilizzare l’ID client e il Segreto client generati da tale applicazione nella connessione.

### Connettersi a Workfront Planning utilizzando una connessione server-to-server

1. In qualsiasi modulo di Adobe Workfront Planning, fare clic su **Aggiungi** accanto al campo Connessione.
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
          <p>Seleziona <b>Connessione da server a server Adobe Workfront</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Inserisci un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Nome istanza]</td>
        <td>
          <p>Inserisci i il nome dell’istanza, noto anche come dominio.</p><p>Esempio: se l’URL è <code>https://example.my.workfront.com</code>, inserisci <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Percorso dell’istanza]</td>
        <td>
          <p>Inserisci il tipo di ambiente della connessione.</p><p>Esempio: se l’URL è <code>https://example.my.workfront.com</code>, inserisci <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Inserisci il tuo ID client. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Apri l’applicazione specifica a cui ti stai connettendo per visualizzare l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Inserisci il Segreto client di Workfront. Questo è disponibile nell’area Applicazioni OAuth2 in Configurazione di Workfront. Se non disponi di un Segreto client per l’applicazione OAuth2 in Workfront, puoi generarne un altro. Per istruzioni, consulta la documentazione di Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiti]</td>
        <td>Inserisci gli ambiti applicabili per questa connessione.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Prefisso host]</td>
        <td>Nella maggior parte dei casi, questo valore deve essere <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

   Se non si è connessi a Workfront Planning, viene visualizzata una schermata di accesso. Dopo aver effettuato l’accesso, puoi autorizzare la connessione.

>[!NOTE]
>
>* Le connessioni OAuth 2.0 all’API Workfront non sono più basate sulle chiavi API.
>* Per creare una connessione a un ambiente sandbox di Workfront, è necessario creare un’applicazione OAuth2 in tale ambiente e quindi utilizzare l’ID client e il Segreto client generati da tale applicazione nella connessione.

## Moduli di [!DNL Adobe Workfront Planning] versione 2 e relativi campi

>[!IMPORTANT]
>
>I moduli in questa sezione appartengono al connettore Workfront Planning V2.Per i moduli nel connettore Workfront Planning V1, vedere [[!DNL Adobe Workfront Planning] Moduli versione 1 e relativi campi](#adobe-workfront-planning-version-1-modules-and-their-fields).

Quando si configurano i moduli di Workfront Planning, Workfront Fusion visualizza i campi elencati di seguito. Oltre a questi campi potrebbero essere mostrati campi di Workfront aggiuntivi, in base a fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

* [Aree di lavoro](#workspaces-v2)
* [Tipi di record](#record-types-v2)
* [Record](#records-v2)
* [Campi](#fields-v2)
* [Viste](#views-v2)
* [Autorizzazioni](#permissions-v2)
* [Altro](#other-v2)

### Aree di lavoro (V2)

* [Crea un’area di lavoro](#create-a-workspace-v2)
* [Eliminare un’area di lavoro](#delete-a-workspace-v2)
* [Ottieni tutte le aree di lavoro](#get-all-workspaces-v2)
* [Ottieni un’area di lavoro](#get-a-workspace-v2)
* [Aggiornare un’area di lavoro](#update-a-workspace-v2)

#### Creare un’area di lavoro (V2)

Questo modulo di azione crea una nuova area di lavoro in Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome Workspace]</p>
      </td>
      <td>Immettere o mappare un nome per la nuova area di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrizione</p>
      </td>
      <td>Immettere o mappare una descrizione per il nuovo workspace/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Colore</p>
      </td>
      <td>Selezionare il colore da utilizzare per rappresentare il nuovo tipo di record</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icona</p>
      </td>
      <td>Mappa l’icona che desideri utilizzare per questo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Proprietario</p>
      </td>
      <td>Immetti o mappa l’ID utente Adobe IMS dell’utente di cui desideri essere il proprietario dell’area di lavoro.</td> 
    </tr>
  </tbody>
</table>

#### Eliminare un’area di lavoro (V2)

Questo modulo di azione elimina un singolo workspace, specificato dall’ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID area di lavoro]</p>
      </td>
      <td>Immetti o mappa l’ID dell’area di lavoro da eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni tutte le aree di lavoro (V2)

Questo modulo recupera un elenco di tutte le aree di lavoro.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di aree di lavoro restituite]</p>
      </td>
      <td>Immettere o mappare il numero massimo di aree di lavoro restituite dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni un&#39;area di lavoro (V2)

Questo modulo recupera un’area di lavoro in base al relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID area di lavoro]</p>
      </td>
      <td>Immetti o mappa l’ID dell’area di lavoro da recuperare.</td> 
    </tr>
  </tbody>
</table>

#### Aggiornare un’area di lavoro (V2)

Questo modulo di azione aggiorna una nuova area di lavoro in Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Seleziona l’area di lavoro da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome Workspace]</p>
      </td>
      <td>Immettere o mappare un nome per la nuova area di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrizione</p>
      </td>
      <td>Immettere o mappare una descrizione per il nuovo workspace/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Colore</p>
      </td>
      <td>Selezionare il colore da utilizzare per rappresentare il nuovo tipo di record</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icona</p>
      </td>
      <td>Mappa l’icona che desideri utilizzare per questo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Proprietario</p>
      </td>
      <td>Immetti o mappa l’ID utente Adobe IMS dell’utente di cui desideri essere il proprietario dell’area di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Sezioni del tipo di record</p>
      </td>
      <td>Per ogni sezione del tipo di record che si desidera aggiungere all'area di lavoro, fare clic su <b>Aggiungi elemento</b> e immettere il nome della sezione, gli ID del tipo di record e se si desidera sovrascrivere gli ID del tipo di record esistente.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Sezioni tipo di record &gt; Sovrascrivi</p>
      </td>
      <td>Seleziona se sostituire le sezioni esistenti con quelle del modulo. In caso contrario, le sezioni del modulo vengono aggiunte all’elenco di sezioni esistente.</td> 
    </tr>
  </tbody>
</table>


### Tipi di record (V2)

* [Creare un tipo di record](#create-a-record-type-v2)
* [Eliminare un tipo di record](#delete-a-record-type-v2)
* [Ottieni tipi di record globali](#get-global-record-types-v2)
* [Ottieni un tipo di record](#get-a-record-type-v2)
* [Recupera tipi di record](#get-record-types-v2)
* [Aggiornare un tipo di record](#update-a-record-type-v2)

#### Creare un tipo di record (V2)

Questo modulo di azione crea un nuovo tipo di record nell&#39;area di lavoro selezionata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui creare un tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome visualizzato</p>
      </td>
      <td>Immettere o mappare un nome per il nuovo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrizione</p>
      </td>
      <td>Immettere o mappare una descrizione per il nuovo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icona</p>
      </td>
      <td>Mappa l’icona che desideri utilizzare per questo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Colore</p>
      </td>
      <td>Selezionare il colore da utilizzare per rappresentare il nuovo tipo di record</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo di record Source</p>
      </td>
      <td>Se si utilizza un altro tipo di record da copiare come punto di partenza, selezionare tale tipo di record.</td> 
    </tr>
  </tbody>
</table>

#### Eliminare un tipo di record (V2)

Questo modulo di azione elimina un singolo tipo di record, specificato dall’ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Immettere o mappare l'ID del tipo di record che si desidera eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni tipi di record globali (V2)

Questo modulo recupera un elenco di tipi di record in un account Adobe Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Seleziona un’area di lavoro. Il modulo restituirà i tipi di record globali disponibili per l'aggiunta a questa area di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di tipi di record restituiti]</p>
      </td>
      <td>Immettere o mappare il numero massimo di tipi di record restituiti dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni un tipo di record (V2)

Questo modulo recupera un tipo di record in base al relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Immettere o mappare l'ID del tipo di record che si desidera recuperare.</td> 
    </tr>
  </tbody>
</table>

#### Recupera tipi di record (V2)

Questo modulo recupera un elenco di tipi di record disponibili in una determinata area di lavoro.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro per la quale si desidera recuperare i tipi di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di tipi di record restituiti]</p>
      </td>
      <td>Immettere o mappare il numero massimo di tipi di record restituiti dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Aggiornare un tipo di record (V2)

Questo modulo aggiorna un tipo di record.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui si desidera aggiornare un tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui si desidera aggiornare un tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome visualizzato</p>
      </td>
      <td>Immettere o mappare un nome per il tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrizione</p>
      </td>
      <td>Immettere o mappare una descrizione per il tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID campo primario</p>
      </td>
      <td>Immettere o mappare l'ID del campo utilizzato come titolo del tipo di record.</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>Icona</p>
      </td>
      <td>Mappa l’icona che desideri utilizzare per questo tipo di record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Colore</p>
      </td>
      <td>Selezionare il colore da utilizzare per rappresentare il nuovo tipo di record</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Collegabile con ID Workspace</p>
      </td>
      <td>Per ogni area di lavoro a cui vuoi collegare questo tipo di record, fai clic su <b>Aggiungi elemento</b> e immetti l'ID dell'area di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Collegabile con Workspace ID &gt; Sovrascrivi</p>
      </td>
      <td>Seleziona se sostituire le aree di lavoro esistenti con quelle del modulo. In caso contrario, le aree di lavoro del modulo vengono aggiunte all’elenco esistente delle aree di lavoro.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorizzato a creare il tipo di record dinamico</p>
      </td>
      <td>Per ogni oggetto autorizzato a creare tipi di record dinamici da questo tipo di record, fare clic su <b>Aggiungi elemento</b> e immettere il tipo e l'ID del soggetto.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorizzato a creare il tipo di record dinamico &gt; Sovrascrivi</p>
      </td>
      <td>Seleziona se sostituire gli oggetti esistenti con quelli del modulo. In caso negativo, i soggetti del modulo vengono aggiunti all’elenco esistente dei soggetti.</td> 
    </tr>
  </tbody>
</table>



### Record (V2)

* [Crea un record](#create-a-record-v2)
* [Elimina una decisione](#delete-a-record-v2)
* [Ottieni un record](#get-a-record-v2)
* [Ottieni record per tipo di record](#get-records-by-record-type-v2)
* [Sposta record](#move-records-v2)
* [Cerca record](#search-records-v2)
* [Aggiorna un record](#update-a-record-v2)

#### Crea un record (V2)

Questa azione consente di creare un singolo record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui si desidera creare un record.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Seleziona il tipo di ambiente da creare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Immettere i valori desiderati per il nuovo record. Questi campi si basano sul tipo di record selezionato e sono specifici per l'organizzazione Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Eliminare un record (V2)

Questo modulo di azione elimina un singolo record, specificato dall’ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID record]</p>
      </td>
      <td>Immettere o mappare l'ID del record che si desidera eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni un record (V2)

Questo modulo di azione recupera un record, specificato dal relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID area di lavoro]</p>
      </td>
      <td>Immettere o mappare l'ID del record che si desidera recuperare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni record per tipo di record (V2)

Questo modulo recupera un elenco di tutti i record del tipo di record specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente i record da recuperare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record che si desidera restituire.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di record restituiti]</p>
      </td>
      <td>Immettere o mappare il numero massimo di record restituiti dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Sposta record (V2)

Questo modulo riordina uno o più record all&#39;interno di un tipo di record specificando dove inserirli.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente i record che si desidera spostare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record che si desidera spostare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente i record che si desidera spostare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente i record che si desidera spostare.</td> 
    </tr>
  </tbody>
</table>

#### Cerca record (V2)

Restituire i record in base ai criteri specificati

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente i record da recuperare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record contenente i record che si desidera recuperare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altri campi]</p>
      </td>
      <td>Per ogni campo in base al quale si desidera filtrare, immettere l'operatore e il valore per tale campo. Questi campi si basano sul tipo di record selezionato e sono specifici per l'organizzazione Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Aggiornare un record (V2)

Questo modulo aggiorna il record specificato.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro contenente il record che si desidera aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID record]</p>
      </td>
      <td>Immetti o mappa l’ID del record da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altri campi]</p>
      </td>
      <td>Immettere valori per altri campi. I campi disponibili dipendono dal record selezionato.</td> 
    </tr>
  </tbody>
</table>


### Campi (V2)

* [Crea un campo](#create-a-field-v2)
* [Eliminare un campo](#delete-a-field-v2)
* [Ottieni un campo](#get-a-field-v2)
* [Recupera campi per tipo di record](#get-fields-by-record-type-v2)
* [Aggiorna un campo](#update-a-field-v2)

#### Crea un campo (V2)

Questo modulo di azione crea un nuovo campo sul tipo di record specificato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Seleziona l’area di lavoro in cui desideri creare un campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record per il quale si desidera creare un campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome visualizzato</p>
      </td>
      <td>Inserisci oppure mappa un nome per il nuovo campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Descrizione</p>
      </td>
      <td>Immettere o mappare una descrizione per il nuovo campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo di campo</p>
      </td>
      <td>Selezionare il tipo di dati per il campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Altri campi</p>
      </td>
      <td>Possono essere disponibili altri campi specifici per il tipo di campo selezionato. Immettere i valori per questi campi.</td> 
    </tr>
  </tbody>
</table>

#### Eliminare un campo (V2)

Questo modulo di azione elimina un singolo campo, specificato dall’ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID campo]</p>
      </td>
      <td>Inserisci oppure mappa l’ID del campo da eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni un campo (V2)

Questo modulo recupera un campo in base al relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID campo]</p>
      </td>
      <td>Immetti o mappa l’ID del campo da recuperare.</td> 
    </tr>
  </tbody>
</table>

#### Recupera campi per tipo di record (V2)

Questo modulo recupera un elenco di campi per un tipo di record specifico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Seleziona l’area di lavoro contenente i campi che desideri restituire.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record per il quale si desidera restituire i campi.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di campi restituiti]</p>
      </td>
      <td>Immettere o mappare il numero massimo di campi restituiti dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Aggiornare un campo (V2)

Questo modulo aggiorna parzialmente un campo in base al relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Seleziona il tipo di risorsa contenente il campo da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID campo]</p>
      </td>
      <td>Seleziona il campo da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nome visualizzato]</p>
      </td>
      <td>Immettere o associare un nome per il campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Descrizione]</p>
      </td>
      <td>Immettere o mappare una descrizione per il campo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Altri parametri]</p>
      </td>
      <td>Immettere i valori per gli altri parametri del campo. I parametri disponibili dipendono dal campo selezionato.</td> 
    </tr>
  </tbody>
</table>


### Viste (V2)

* [Creare una visualizzazione](#create-a-view-v2)
* [Eliminare una visualizzazione](#delete-a-view-v2)
* [Ottenere una visualizzazione](#get-a-view-v2)
* [Ottieni visualizzazioni per tipo di record](#get-views-by-record-type-v2)
* [Aggiornare una visualizzazione](#update-a-view-v2)

#### Creare una vista (V2)

Questo modulo di azione crea una nuova visualizzazione per il tipo di record selezionato.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui si desidera creare una visualizzazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record per il quale si desidera creare una visualizzazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome vista</p>
      </td>
      <td>Immettete o mappate un nome per la nuova vista.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Tipo vista</p>
      </td>
      <td>Seleziona se la nuova vista è una vista tabella, timeline o calendario.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Campo data di inizio</p>
      </td>
      <td>Se la visualizzazione sarà una visualizzazione timeline o calendario, selezionare il campo che verrà utilizzato per inserire il record nella timeline.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Campo data di fine.</p>
      </td>
      <td>Se la visualizzazione è una visualizzazione timeline o calendario, selezionare il campo che verrà utilizzato per determinare la data di fine sulla timeline.</td> 
    </tr>
  </tbody>
</table>

#### Eliminare una vista (V2)

Questo modulo di azione elimina una singola vista, specificata dall’ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID visualizzazione]</p>
      </td>
      <td>Immetti o mappa l’ID della vista da eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni una visualizzazione (V2)

Questo modulo recupera una vista in base al relativo ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID visualizzazione]</p>
      </td>
      <td>Immetti o mappa l’ID della vista da recuperare.</td> 
    </tr>
  </tbody>
</table>

#### Ottieni visualizzazioni per tipo di record (V2)

Questo modulo recupera un elenco di visualizzazioni per il tipo di record specifico.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionate l'area di lavoro contenente le viste da recuperare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record contenente le visualizzazioni da recuperare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Numero massimo di visualizzazioni restituite]</p>
      </td>
      <td>Immettere o mappare il numero massimo di visualizzazioni restituite dal modulo durante un ciclo di esecuzione.</td> 
    </tr>
  </tbody>
</table>

#### Aggiornare una vista (V2)

Questo modulo di azione aggiorna la vista specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
      </td>
      <td>Selezionare l'area di lavoro in cui si desidera aggiornare una visualizzazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di record]</p>
      </td>
      <td>Selezionare il tipo di record per il quale si desidera aggiornare una visualizzazione.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID Vista</p>
      </td>
      <td>Selezionare la visualizzazione da aggiornare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nome vista</p>
      </td>
      <td>Immettete o mappate un nome per la nuova vista.</td> 
    </tr>
  </tbody>
</table>

### Autorizzazioni (V2)

* [Ignora richieste di accesso](#dismiss-access-requests-v2)
* [Ottenere tutti i membri e i relativi ruoli per una risorsa](#get-all-members-and-their-roles-for-a-resource-v2)
* [Ottenere le autorizzazioni effettive dell’utente corrente su una risorsa](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [Elencare le richieste di accesso in sospeso per una risorsa](#list-pending-access-requests-for-a-resource-v2)
* [Richiedere l’accesso a una risorsa](#request-access-to-a-resource-v2)

#### Ignora richieste di accesso (V2)

Questo modulo di azione ignora una o più richieste di accesso, specificate dall’ID.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Inserisci o mappa l’ID del Workspace da eliminare.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID risorsa]</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri ignorare le richieste di accesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID richiesta]</p>
      </td>
      <td>Per ogni richiesta di accesso che si desidera ignorare, fare clic su <b>Aggiungi elemento</b> e immettere l'ID della richiesta.</td> 
    </tr>
  </tbody>
</table>

#### Ottenere tutti i membri e i relativi ruoli per una risorsa (V2)

Questo modulo elenca tutti gli utenti, i gruppi e i team che hanno una relazione di condivisione esplicita sulla risorsa. Le credenziali utilizzate nella connessione per questo modulo devono disporre dell&#39;autorizzazione Gestione per la risorsa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Selezionare il tipo di risorsa per cui si desidera recuperare le informazioni.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID risorsa]</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri recuperare le informazioni.</td> 
    </tr>
  </tbody>
</table>

#### Ottenere le autorizzazioni effettive dell&#39;utente corrente per una risorsa (V2)

Questo modulo restituisce le autorizzazioni di visualizzazione, modifica, eliminazione e aggiunta dell’utente corrente per una determinata risorsa.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Seleziona il tipo di risorsa per il quale desideri recuperare le autorizzazioni.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID risorsa]</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri recuperare le autorizzazioni.</td> 
    </tr>
  </tbody>
</table>

#### Elencare le richieste di accesso in sospeso per una risorsa (V2)

Questo modulo restituisce tutte le richieste di accesso in sospeso per la risorsa specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Selezionare il tipo di risorsa per cui si desidera recuperare le informazioni.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID risorsa]</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri recuperare le informazioni.</td> 
    </tr>
  </tbody>
</table>

#### Richiedi accesso a una risorsa (V2)

Questo modulo crea o aggiorna una richiesta di accesso per l’utente corrente sulla risorsa specificata.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Tipo di risorsa]</p>
      </td>
      <td>Seleziona il tipo di risorsa per cui desideri creare o aggiornare una richiesta di accesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID risorsa]</p>
      </td>
      <td>Immetti o mappa l’ID della risorsa per la quale desideri creare o aggiornare una richiesta di accesso.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Messaggio]</p>
      </td>
      <td>Inserisci o mappa il testo di un messaggio da includere nella richiesta di accesso.</td> 
    </tr>
  </tbody>
</table>



### Altro (V2)

* [Ottieni ID autenticazione da Workfront ID](#get-auth-id-from-workfront-id-v2)
* [Effettua chiamata API personalizzata](#make-a-custom-api-call-v2)
* [Osserva eventi](#watch-events-v2)

#### Ottieni ID di autenticazione da Workfront ID (V2)

Questo modulo accetta un ID utente di Workfront e restituisce l&#39;ID di autorizzazione corrispondente utilizzato da Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID utente Workfront]</p>
      </td>
      <td>Immetti o mappa l’ID Workfront dell’utente per il quale desideri recuperare un ID autorizzazione.</td> 
    </tr>
  </tbody>
</table>

#### Effettuare una chiamata API personalizzata (V2)&lt;tabella

Questo modulo effettua una chiamata personalizzata all’API di pianificazione di Workfront.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Inserisci un percorso relativo a <code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Versione API]</td> 
   <td>Seleziona la versione dell’API Workfront che il modulo deve utilizzare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Questo determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> <p>Suggerimento: è consigliabile inviare informazioni tramite il corpo JSON anziché come parametri di query.</p> </td> 
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

#### Eventi Watch (V2)

Questo modulo di attivazione avvia uno scenario quando un record, un tipo di record o un&#39;area di lavoro viene creata, aggiornata o eliminata in Workfront Planning.

>[!IMPORTANT]
>
>Puoi modificare questo modulo in un secondo momento, per modificare il webhook.
>
>Quando si aggiorna un webhook, considera quanto segue:
>
>* Il webhook modificato viene trattato dagli abbonamenti agli eventi di Workfront come un nuovo abbonamento. La cronologia delle sottoscrizioni degli eventi non viene mantenuta per la configurazione del webhook precedente, in quanto viene considerata una sottoscrizione di evento separata.
>* Il passaggio dalla sottoscrizione precedente a quella nuova potrebbe non essere sincronizzato perfettamente. È quindi possibile ricevere un evento due volte (se il nuovo abbonamento inizia a essere eseguito prima che quello vecchio si fermi) o perdere un evento (se il vecchio abbonamento si arresta prima che quello nuovo inizi a essere eseguito).
>
>Per ulteriori informazioni sulla modifica dei webhook, vedere [Modifica webhook](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selezionare il webhook che si desidera utilizzare o fare clic su Aggiungi per crearne uno nuovo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di oggetto]</td>
      <td>Specificare se si desidera controllare record, tipi di record o aree di lavoro.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Oggetti da controllare]</td>
      <td>Specificare se si desidera controllare i nuovi record, i record aggiornati, i record nuovi e aggiornati o i record eliminati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di configurazione]</td>
      <td>Seleziona se desideri una configurazione semplice o avanzata. <p>Per ulteriori informazioni sulla configurazione avanzata, vedere <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >Esempio di logica avanzata nel modulo Watch Events</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stato]</td>
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL Nuovo stato]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p></li><li><p><b>[!UICONTROL Stato precedente]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> un determinato valore.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Area di lavoro]</td>
      <td>Se si desidera controllare i record, selezionare il Workspace che si desidera controllare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di record]</td>
      <td>Se si desidera controllare i record, selezionare il tipo di record che si desidera controllare.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Filtri eventi]</p> </td> 
      <td> <p>Puoi impostare filtri per controllare solo i record che soddisfano i criteri da te selezionati.</p> <p>Per ogni filtro, inserisci il campo che desideri venga valutato dal filtro, l’operatore e il valore che desideri sia consentito dal filtro. Puoi utilizzare più di un filtro aggiungendo regole di tipo AND.</p> <p>Nota: non è possibile modificare i filtri nei webhook Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.</p> <p>Per ulteriori informazioni sui filtri eventi, vedere <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri di sottoscrizione eventi nei moduli Workfront &gt; [!UICONTROL Watch Events]</a> nell'articolo Moduli Workfront.</p> </td> 
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

Per un esempio di utilizzo della logica avanzata in questo modulo, vedere [Esempio di logica avanzata nel modulo Watch Events](#example-of-advanced-logic-in-the-watch-events-module).






## Moduli di [!DNL Adobe Workfront Planning] versione 1 e relativi campi

>[!IMPORTANT]
>
>I moduli in questa sezione appartengono al connettore Workfront Planning V1.Per i moduli nel connettore Workfront Planning V2, vedere [[!DNL Adobe Workfront Planning] Moduli versione 2 e relativi campi](#adobe-workfront-planning-version-2-modules-and-their-fields).

Quando si configurano i moduli di Workfront Planning, Workfront Fusion visualizza i campi elencati di seguito. Oltre a questi campi potrebbero essere mostrati campi di Workfront aggiuntivi, in base a fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)
* [Non categorizzato](#uncategorized)

### Trigger

#### Osserva eventi

Questo modulo di attivazione avvia uno scenario quando un record, un tipo di record o un&#39;area di lavoro viene creata, aggiornata o eliminata in Workfront Planning.

>[!IMPORTANT]
>
>Puoi modificare questo modulo in un secondo momento, per modificare il webhook.
>
>Quando si aggiorna un webhook, considera quanto segue:
>
>* Il webhook modificato viene trattato dagli abbonamenti agli eventi di Workfront come un nuovo abbonamento. La cronologia delle sottoscrizioni degli eventi non viene mantenuta per la configurazione del webhook precedente, in quanto viene considerata una sottoscrizione di evento separata.
>* Il passaggio dalla sottoscrizione precedente a quella nuova potrebbe non essere sincronizzato perfettamente. È quindi possibile ricevere un evento due volte (se il nuovo abbonamento inizia a essere eseguito prima che quello vecchio si fermi) o perdere un evento (se il vecchio abbonamento si arresta prima che quello nuovo inizi a essere eseguito).
>
>Per ulteriori informazioni sulla modifica dei webhook, vedere [Modifica webhook](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Selezionare il webhook che si desidera utilizzare o fare clic su Aggiungi per crearne uno nuovo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di oggetto]</td>
      <td>Specificare se si desidera controllare record, tipi di record o aree di lavoro.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stato]</td>
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL Nuovo stato]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p></li><li><p><b>[!UICONTROL Stato precedente]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> un determinato valore.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Area di lavoro]</td>
      <td>Se si desidera controllare i record, selezionare il Workspace che si desidera controllare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di record]</td>
      <td>Se si desidera controllare i record, selezionare il tipo di record che si desidera controllare.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Filtri eventi]</p> </td> 
      <td> <p>Puoi impostare filtri per controllare solo i record che soddisfano i criteri da te selezionati.</p> <p>Per ogni filtro, inserisci il campo che desideri venga valutato dal filtro, l’operatore e il valore che desideri sia consentito dal filtro. Puoi utilizzare più di un filtro aggiungendo regole di tipo AND.</p> <p>Nota: non è possibile modificare i filtri nei webhook Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.</p> <p>Per ulteriori informazioni sui filtri eventi, vedere <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri di sottoscrizione eventi nei moduli Workfront &gt; [!UICONTROL Watch Events]</a> nell'articolo Moduli Workfront.</p> </td> 
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

Per un esempio di utilizzo della logica avanzata in questo modulo, vedere [Esempio di logica avanzata nel modulo Watch Events](#example-of-advanced-logic-in-the-watch-events-module).

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
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID tipo di record]</p>
      </td>
      <td>Immettere o mappare l'ID del tipo di record che si desidera eliminare.</td> 
    </tr>
  </tbody>
</table>

#### Effettua chiamata API personalizzata

Questo modulo effettua una chiamata API personalizzata all&#39;API [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
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
        <p>Per ogni coppia chiave/valore che si desidera aggiungere alla stringa di query, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore.</p>
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


### Ricerche

#### Cerca record

Questo modulo di azione recupera un elenco di record in base ai criteri specificati.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Area di lavoro]</p>
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
        <p>[!UICONTROL Limite]</p>
      </td>
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
    </tr>
  </tbody>
</table>


### Non categorizzato


#### Crea un record

Questa azione consente di creare un singolo record in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
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

### Elimina una decisione

Questo modulo di azione elimina il record specificato in Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
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
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
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
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Area di lavoro]</td>
      <td>Selezionare o mappare l'area di lavoro contenente i record da recuperare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tipo di record]</td>
      <td>Selezionare il tipo di record da recuperare.</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### Recupera tipi di record

Questo modulo di azione recupera un elenco di tipi di record in un account [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Area di lavoro]</td>
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
      <td role="rowheader">[!UICONTROL Connessione]</td>
      <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Workfront Planning], consulta <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Creare una connessione a [!DNL Adobe Workfront Planning]</a> in questo articolo.</td>
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

## Esempio di logica avanzata nel modulo Watch Events

Questo è un esempio del formato utilizzato dalla logica avanzata quando si utilizza il modulo Workfront Planning > Osserva eventi.

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

Quando utilizzi una logica avanzata nel modulo Watch Event, tieni presente quanto segue:

* La prima voce `"fieldvalue":` è l&#39;ID del tipo di record di pianificazione estratto dall&#39;URL. In questo esempio, l&#39;ID del tipo di record di pianificazione è `Rt68c886502d4b5554ee80896b`.
* I dati di Planning vengono restituiti all&#39;interno di un array denominato `data `, che in questo esempio viene visualizzato come `"fieldName": "data"`.
* I nomi dei campi di Planning vengono restituiti come ID che iniziano con `F`.
* Poiché questo esempio esegue la valutazione in base a un connettore di filtro `OR`, sono presenti due voci per lo stesso campo (`F68c886502d4b5554eec808975`).  Le due opzioni dell&#39;elenco a discesa a cui si applica il filtro del modulo sono `"planning"` e `"active"`.

