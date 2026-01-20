---
title: Moduli Adobe Workfront
description: Per automatizzare i processi all’interno di Workfront, puoi utilizzare il connettore Adobe Workfront Fusion. Se disponi di una licenza di Workfront Fusion for Work Automation and Integration, puoi utilizzarla anche per connetterti ad app e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: tm+mt
source-wordcount: '7366'
ht-degree: 99%

---

# Moduli Adobe Workfront

>[!IMPORTANT]
>
>Questo articolo contiene istruzioni per la nuova versione del connettore Workfront, rilasciata il 22 ottobre 2025. Questo nuovo connettore rispecchia le modifiche apportate all’API Workfront.
>
>Il nuovo connettore è etichettato come “Workfront”, quello precedentemente disponibile come “Workfront (legacy)”.
>
>È consigliabile:
>
>* Utilizzare il nuovo connettore durante la creazione o l’aggiornamento di uno scenario.
>* Aggiornare i moduli esistenti al nuovo connettore.
>
>Il connettore Workfront legacy utilizza la versione 20 dell’API Workfront, che diventerà obsoleta con la versione 28.4 (aprile 2028). I moduli nel connettore legacy continueranno a funzionare fino a quel momento.
>
>Per istruzioni sull’aggiornamento dei moduli esistenti, consulta [Aggiornare un modulo di Workfront a una nuova versione](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md) nell’articolo Aggiornare un modulo a una nuova versione.
>
>Per informazioni sui motivi per cui talvolta è necessario un nuovo connettore, consulta [Panoramica delle API in Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

Per automatizzare i processi all’interno di Workfront, puoi utilizzare il connettore Adobe Workfront Fusion. È inoltre possibile collegare Workfront ad altre applicazioni e servizi.

Per istruzioni su come creare uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Connessione di Workfront a Workfront Fusion

Il connettore Workfront utilizza OAuth 2.0 per connettersi a Workfront.

Puoi creare una connessione al tuo account Workfront direttamente dall’interno di un modulo Workfront Fusion.

* [Connettersi a Workfront utilizzando l’ID client e il Segreto client](#connect-to-workfront-using-client-id-and-client-secret)
* [Connettersi a Workfront utilizzando una connessione da server a server](#connect-to-workfront-using-a-server-to-server-connection)

### Connettersi a Workfront utilizzando l’ID client e il Segreto client

1. In qualsiasi modulo di Adobe Workfront, fai clic su **Aggiungi** accanto al campo Connessione.
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
          <p>Seleziona <b>Connessione di autenticazione Adobe Workfront</b>.</p>
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

   Se non hai effettuato l’accesso a Workfront, verrà aperta una schermata di accesso. Dopo aver effettuato l’accesso, puoi autorizzare la connessione.

>[!NOTE]
>
>* Le connessioni OAuth 2.0 all’API Workfront non sono più basate sulle chiavi API.
>* Per creare una connessione a un ambiente sandbox di Workfront, è necessario creare un’applicazione OAuth2 in tale ambiente e quindi utilizzare l’ID client e il Segreto client generati da tale applicazione nella connessione.

### Connettersi a Workfront utilizzando una connessione da server a server

1. In qualsiasi modulo di Adobe Workfront, fai clic su **Aggiungi** accanto al campo Connessione.
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

   Se non hai effettuato l’accesso a Workfront, verrà aperta una schermata di accesso. Dopo aver effettuato l’accesso, puoi autorizzare la connessione.

>[!NOTE]
>
>* Le connessioni OAuth 2.0 all’API Workfront non sono più basate sulle chiavi API.
>* Per creare una connessione a un ambiente sandbox di Workfront, è necessario creare un’applicazione OAuth2 in tale ambiente e quindi utilizzare l’ID client e il Segreto client generati da tale applicazione nella connessione.

## Moduli Workfront e relativi campi

Quando configuri i moduli di Workfront, Workfront Fusion mostra i campi elencati di seguito. Oltre a questi campi potrebbero essere mostrati campi di Workfront aggiuntivi, in base a fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se non visualizzi i campi più aggiornati in un modulo Workfront, potrebbe dipendere da un problema di caching. Attendi un’ora e riprova.
>* I codici di stato HTTP 429 di Adobe Workfront non dovrebbero causare disattivazioni, ma piuttosto attivare una breve pausa di esecuzione nello scenario.

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Osserva eventi]**

Questo modulo trigger esegue uno scenario in tempo reale quando in Workfront vengono aggiunti, aggiornati o eliminati oggetti di un tipo specifico.

Il modulo visualizza tutte le sottoscrizioni a eventi correlate al webhook. Sono incluse le sottoscrizioni a eventi create tramite Fusion e quelle create direttamente tramite l’API. Questa vista di sottoscrizione a eventi non è disponibile nella versione legacy del modulo Osserva eventi.

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

1. Fai clic su **[!UICONTROL Aggiungi]** a destra della casella **Webhook**.

1. Configura il webhook nella casella **[!UICONTROL Aggiungi un webhook]** visualizzata.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome webhook]</td> 
      <td>Specifica un nome per il webhook.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connessione]</td> 
      <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Tipo di record]</td> 
      <td>Seleziona il tipo di record Workfront che il modulo deve controllare.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Stato]</td> 
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL Nuovo stato]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p><p>Se ad esempio lo stato è [!UICONTROL Nuovo stato] e il filtro è impostato su [!UICONTROL Stato] [!UICONTROL Uguale a] [!UICONTROL In corso], il webhook attiva uno scenario quando [!UICONTROL Stato] diventa [!UICONTROL In corso], indipendentemente dal valore precedente dello stato. </p></li><li><p><b>[!UICONTROL Stato precedente]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> un determinato valore.</p><p>Se ad esempio lo stato è [!UICONTROL Stato precedente] e il filtro è impostato su [!UICONTROL Stato] [!UICONTROL Uguale a] [!UICONTROL In corso], il webhook attiva uno scenario quando [!UICONTROL Stato] attualmente impostato su [!UICONTROL In corso] passa a uno stato diverso. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Filtri eventi]</p> </td> 
      <td> <p>Puoi impostare filtri per controllare solo i record che soddisfano i criteri da te selezionati.</p> <p>Per ogni filtro, inserisci il campo che desideri venga valutato dal filtro, l’operatore e il valore che desideri sia consentito dal filtro. Puoi utilizzare più di un filtro aggiungendo regole di tipo AND.</p> <p><b>NOTA</b>: non puoi modificare filtri nei webhook di Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.</p> <p>Per ulteriori informazioni sui filtri degli eventi, consulta <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri per le sottoscrizioni eventi nei moduli Workfront &gt; [!UICONTROL Osserva eventi]</a> in questo articolo.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Escludi eventi creati da questa connessione</td> 
      <td>Abilita questa opzione per escludere gli eventi creati o aggiornati con lo stesso connettore utilizzato da questo modulo trigger. Questo può evitare situazioni in cui uno scenario potrebbe attivarsi da solo e ripetersi in un ciclo infinito.<p><b>NOTA</b>: il tipo di record Assegnazione non include questa opzione.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Origine record]</td> 
      <td>
       <p>Scegli se desideri che lo scenario controlli [!UICONTROL Solo i record nuovi], [!UICONTROL Solo i record aggiornati], [!UICONTROL Record nuovi e aggiornati] oppure [!DNL Deleted Records Only].</p>
       <p><b>NOTA</b>: se scegli [!UICONTROL Record nuovi e aggiornati], la creazione del webhook crea due sottoscrizioni eventi (per lo stesso indirizzo del webhook).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Dopo la creazione del webhook puoi visualizzare l’indirizzo dell’endpoint al quale vengono inviati gli eventi.

Per ulteriori informazioni, consulta la sezione [Esempi di payload di eventi](https://experienceleague.adobe.com/it/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) nell’articolo API sottoscrizione eventi della documentazione di Workfront.

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Osserva campo]**

Questo modulo trigger esegue uno scenario quando viene aggiornato un campo che hai specificato. Il modulo restituisce sia il valore precedente sia il nuovo valore del campo specificato. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record Workfront che il modulo deve controllare.</p> <p>Seleziona ad esempio [!UICONTROL Attività] se desideri avviare l’esecuzione dello scenario ogni volta che un campo record viene aggiornato in un’attività.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campo]</td> 
   <td>Seleziona il campo che il modulo deve controllare per gli aggiornamenti. Questi campi riflettono i campi impostati per il tracciamento dall’amministratore di Workfront.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Output]</td> 
   <td>Seleziona i campi oggetto da includere nel bundle di output per questo modulo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Osserva record]**

Questo modulo trigger esegue uno scenario quando gli oggetti di un tipo specifico vengono aggiunti, aggiornati o entrambi. Il modulo restituisce tutti i campi standard associati al record oppure ai record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Nell’output, il modulo indica se ciascun record è nuovo o aggiornato.

I record aggiunti o aggiornati dall’ultima esecuzione dello scenario vengono restituiti come record nuovi.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Scegli se desideri che lo scenario controlli [!UICONTROL Solo i record nuovi], [!UICONTROL Solo i record aggiornati], [!UICONTROL Record nuovi e aggiornati].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record Workfront che il modulo deve controllare.</p> <p>Se ad esempio desideri avviare lo scenario ogni volta che viene creato un nuovo progetto, seleziona [!UICONTROL Progetto]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Riferimento]</td> 
   <td> <p>Seleziona i campi di riferimento da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi raccolta da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro opzionale]</td> 
   <td> <p>(Avanzato) Digita una stringa di codice API per definire eventuali parametri o codice aggiuntivo che definiranno ulteriormente i criteri. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++


### Azioni

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Converti oggetto]**

Questo modulo di azione effettua una delle seguenti conversioni:

* Converti problema in progetto
* Converti problema in attività
* Converti attività in progetto

>[!NOTE]
>
>A partire da luglio 2024, i moduli personalizzati possono essere inclusi durante la conversione di un oggetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di oggetto]</td> 
   <td> <p>Seleziona il tipo di oggetto da convertire. Questo è il tipo dell’oggetto prima della conversione.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Converti in]</td> 
   <td>Seleziona l’oggetto che desideri convertire. Questo è il tipo dell’oggetto dopo la conversione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID &lt;Object&gt;]</td> 
   <td> <p>Inserisci l’ID dell’oggetto. </p> <p>Nota: quando inserisci l’ID di un oggetto, puoi iniziare a digitare il nome dell’oggetto, quindi selezionarlo dall’elenco. Il modulo inserisce quindi l’ID appropriato nel campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID modello]</td> 
   <td> <p>Se stai eseguendo la conversione a un progetto, seleziona l’ID modello da utilizzare per il progetto.</p> <p>Nota: quando inserisci l’ID di un oggetto, puoi iniziare a digitare il nome dell’oggetto, quindi selezionarlo dall’elenco. Il modulo inserisce quindi l’ID appropriato nel campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Moduli personalizzati]</td> 
   <td>Seleziona i moduli personalizzati da aggiungere all’oggetto appena convertito, quindi inserisci i valori per i campi del modulo personalizzato.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Opzioni]</td> 
   <td> <p>Abilita le opzioni desiderate per la conversione dell’oggetto. Le opzioni disponibili dipendono dall’oggetto da o verso il quale stai eseguendo la conversione.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copia campi nativi]</td> 
   <td> <p>Abilita questa opzione per copiare tutti i campi nativi dall’oggetto originale al nuovo oggetto.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copia moduli personalizzati]</td> 
   <td> <p>Abilita questa opzione per copiare tutti i campi nativi dall’oggetto originale al nuovo oggetto.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea un record]** 

Questo modulo di azione crea un oggetto, tra cui un progetto, un’attività o un problema in Workfront, e ti consente di aggiungere un modulo personalizzato al nuovo oggetto. Il modulo ti consente di selezionare i campi dell’oggetto disponibili nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Assicurati di fornire il numero minimo di campi di input. Se ad esempio desideri creare un problema, devi fornire un ID progetto principale valido nel campo ID progetto per indicare la posizione del problema in Workfront. Per mappare queste informazioni da un altro modulo allo scenario puoi utilizzare il pannello di mappatura, oppure puoi inserirle manualmente digitando il nome e selezionandolo nell’elenco.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record di Workfront che il modulo deve creare.</p> <p>Se ad esempio desideri creare un progetto, seleziona [!UICONTROL Progetto] dall’elenco a discesa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Seleziona i campi da mappare]</td> 
   <td> <p>Seleziona i campi che desideri rendere disponibili per l’input di dati. Questo ti consente di utilizzare tali campi senza dover scorrere quelli non necessari. Quindi puoi inserire o mappare i dati in questi campi.</p> <p>Per i campi nei moduli personalizzati, utilizza il campo <b>[!UICONTROL Allega modulo personalizzato]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allega modulo personalizzato]</td> 
   <td>Seleziona i moduli personalizzati da aggiungere al nuovo oggetto, seleziona i campi per i quali inserire i valori, quindi inserisci oppure mappa i valori per tali campi.</td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Quando inserisci l’ID di un oggetto, puoi iniziare a digitare il nome dell’oggetto, quindi selezionarlo dall’elenco. Il modulo inserisce quindi l’ID appropriato nel campo.
>* Quando inserisci il testo per un campo personalizzato o un oggetto [!UICONTROL Nota] (commento o risposta), puoi utilizzare tag HTML nel campo [!UICONTROL Testo nota] per creare testo formattato, ad esempio testo in grassetto o corsivo.
>



>[!NOTE]
>
>Gli utenti vengono creati con gli stati Disattivato e In attesa di approvazione. Se la tua organizzazione ha effettuato la migrazione ad Adobe Admin Console e il badge In attesa di approvazione non viene rimosso entro pochi minuti, puoi approvare l’utente.
>
>* **Risolvi singoli utenti**
>
>      Puoi risolvere singoli utenti nell’elenco Utenti.
>
>      1. Seleziona uno o più utenti nell’elenco Utenti.
>      1. Fai clic sul menu con i tre punti nell’intestazione dell’elenco.
>      1. Seleziona **Approva**.
>      1. Dopo alcuni minuti, aggiorna la pagina.
>
>* **Risolvi utenti aggiunti in un batch grande**
>
>   Per risolvere gli utenti aggiunti in un batch di grandi dimensioni, puoi aggiungere direttamente il batch di utenti ad Adobe Admin Console.
>
>   Per istruzioni, consulta [Gestire più utenti   Caricamento in blocco di CSV](https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html) nella documentazione di Adobe.

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Chiamata API personalizzata]**

Questo modulo di azione ti consente di effettuare una chiamata autenticata personalizzata all’API Workfront. In questo modo puoi creare un’automazione del flusso di dati che non è possibile ottenere con gli altri moduli di Workfront.

Il modulo restituisce le informazioni seguenti:

* **[!UICONTROL Codice di stato]** (numero): indica il completamento o il mancato completamento della richiesta HTTP. I valori restituiti sono codici standard che puoi cercare su Internet.
* **[!UICONTROL Intestazioni]** (oggetto): un contesto più dettagliato per il codice di risposta/stato non correlato al corpo dell’output. Non tutte le intestazioni visualizzate in una risposta sono intestazioni di risposta, pertanto alcune potrebbero non risultarti utili.

  Le intestazioni di risposta dipendono dalla richiesta HTTP che hai scelto durante la configurazione del modulo.

* **[!UICONTROL Corpo]** (oggetto): a seconda della richiesta HTTP che hai scelto al momento della configurazione del modulo, potresti ricevere alcuni dati. Tali dati, ad esempio i dati di una richiesta GET, sono contenuti in questo oggetto.

Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

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
   <td> <p>Inserisci un percorso relativo a <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
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
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Questo determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> <p>Nota: se vengono restituiti errori ed è difficile determinarne l’origine, prendi in considerazione la modifica delle intestazioni in base alla documentazione di Workfront. Se la chiamata API personalizzata restituisce un errore di richiesta HTTP 422, prova a utilizzare un’intestazione <code>"Content-Type":"text/plain"</code>.</p> </td> 
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

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Elimina record]**

Questo modulo di azione elimina un oggetto, ad esempio un progetto, un’attività o un problema in Workfront.

Specifica l’ID del record.

Il modulo restituisce l’ID del record e gli eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Forza eliminazione]</td> 
   <td>Abilita questa opzione per garantire che il record venga eliminato, anche nel caso in cui l’interfaccia utente di Workfront richieda conferma dell’eliminazione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Eliminazione asincrona]</td> 
   <td>Abilita questa opzione per consentire al modulo l’eliminazione in modo asincrono.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Inserisci l’ID Workfront univoco del record che il modulo deve eliminare.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td>Seleziona il tipo di record Workfront che il modulo deve eliminare.</td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Per evitare che i record non vengano eliminati a causa di operazioni asincrone, consigliamo la configurazione dello scenario seguente.
>
>1. Elimina il record in modo sincrono.
>1. Aggiungi la gestione errori al modulo Elimina record in modo da ignorare l’errore causato dal timeout di 40 secondi.


+++

+++ **[!UICONTROL Scarica documento]**

Questo modulo di azione scarica un documento da Workfront.

Specifica l’ID del record.

Il modulo restituisce il contenuto, il nome, l’estensione e la dimensione del file del documento. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID documento]</td> 
   <td> <p>Mappa oppure inserisci manualmente l’ID Workfront univoco del documento che il modulo deve scaricare.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

### **Ottieni un URL prefirmato del file**

Questo modulo di azione ottiene URL prefirmati di file che possono essere utilizzati successivamente da altre API.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID documento]</td> 
   <td> <p>Mappa oppure inserisci manualmente l’ID Workfront univoco del documento per il quale desideri ottenere un URL prefirmato.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tempo alla scadenza dell’URL]</td> 
   <td> <p>Inserisci oppure mappa il numero di minuti di esistenza dell’URL prima della scadenza. Il valore predefinito è 1 minuto.</p><p>Per cambiare questo valore, è necessario che il team di Workfront Fusion abiliti questo parametro. Se non è abilitato, il valore rimarrà 1 minuto indipendentemente dal numero che inserisci.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL Azioni varie]**

Questo modulo di azione consente di eseguire azioni sull’API.

>[!NOTE]
>
>A partire da luglio 2024, l’azione `convertToProject` include il campo `copyCategories`. Se è impostata su `TRUE`, tutti i moduli personalizzati verranno inclusi nel progetto in cui viene convertito il problema.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record Workfront con cui il modulo deve interagire.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Azione]</td> 
   <td> <p>Seleziona l’azione che il modulo deve eseguire.</p> <p>Potresti dover compilare altri campi, a seconda di [!UICONTROL Tipo di record] e [!UICONTROL Azione] che hai scelto. Alcune combinazioni di queste due impostazioni possono richiedere solo un ID record, mentre altre (come Progetto per <strong>[!UICONTROL Tipo di record]</strong> e [!UICONTROL Allega modello] per <strong>[!UICONTROL Azione]</strong>) richiedono informazioni aggiuntive quali un ID oggetto e un ID modello.</p><p>Per le opzioni disponibili per alcune azioni, consulta <a href="#misc-action-options" class="MCXref xref">Opzioni per azioni varie</a> in questo articolo.</p> <p>Per informazioni dettagliate sui singoli campi, consulta la <a href="http://developer.workfront.com/">documentazione per gli sviluppatori di Workfront</a>. <p><strong>Nota</strong>: il sito della documentazione per gli sviluppatori include informazioni solo fino alla versione 14 dell’API, ma contiene comunque informazioni importanti sulle chiamate API. </p> 
    <ol> 
     <li value="1"> <p>Seleziona il tipo di record nella barra di navigazione a sinistra della pagina di documentazione per sviluppatori di Workfront. Per i seguenti tipi esistono pagine specifiche:</p> 
      <ul> 
       <li> <p>[!UICONTROL Progetti]</p> </li> 
       <li> <p>[!UICONTROL Attività]</p> </li> 
       <li> <p>[!UICONTROL Problemi]</p> </li> 
       <li> <p>[!UICONTROL Utenti]</p> </li> 
       <li> <p>[!UICONTROL Documenti]</p> </li> 
      </ul> <p>Per tutti gli altri tipi di record, seleziona <b>[!UICONTROL Altri oggetti e endpoint]</b> e individua il tipo di record nelle pagine organizzate in ordine alfabetico.</p> </li> 
     <li value="2"> <p>Nella pagina del tipo di record appropriato, cerca l’azione (Ctrl + F o Comando + F).</p> </li> 
     <li value="3"> <p>Visualizza le descrizioni dei campi disponibili nell’azione selezionata.</p> </li> 
    </ol> <p>Nota:  <p>Quando crei una bozza tramite il modulo [!UICONTROL Azioni varie] di Workfront, la best practice prevede di creare una bozza senza opzioni avanzate, quindi di aggiornarla utilizzando l’API SOAP [!DNL Workfront Proof].</p><p>Per ulteriori informazioni sulla creazione di una bozza con l’API Workfront (utilizzata da questo modulo), consulta <a href="https://experienceleague.adobe.com/it/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Aggiungere opzioni di bozza avanzate durante la creazione di una bozza con l’API Adobe Workfront</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Inserisci oppure mappa l’ID Workfront univoco del record con cui il modulo deve interagire.<p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

#### Opzioni per azioni varie

##### Attività

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Azione</th> 
   <th>Opzioni</th> 
  </tr> 
  <tr> 
   <td>Copia</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Cancella dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella notifiche di promemoria</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Sposta</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Cancella dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella notifiche di promemoria</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### Problema

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Azione</th> 
   <th>Opzioni</th> 
  </tr> 
  <tr> 
   <td>Copia</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Converti in attività</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Mantieni il problema originale e collegane la risoluzione a questa attività</p></li>
   <li>preservePrimaryContact<p>Consenti al contatto principale del problema di accedere a questa attività</p></li>
   <li>preserveCompletionDate<p>Mantieni la data di completamento pianificata del problema</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Converti in progetto</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Mantieni il problema originale e collegane la risoluzione a questa attività</p></li>
   <li>preservePrimaryContact<p>Consenti al contatto principale del problema di accedere a questa attività</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### Progetto

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Azione</th> 
   <th>Opzioni</th> 
  </tr> 
  <tr> 
   <td>Copia</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Cancella dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella notifiche di promemoria</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Allega modello/Salva come modello</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Cancella obiettivi</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Cancella dati finanziari</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Cancella la configurazione dei problemi e le proprietà della coda</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Cancella notifiche di promemoria</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Leggi un record]**

Questo modulo di azione recupera i dati da un singolo record.

Specifica l’ID del record. Puoi anche specificare quali record correlati deve leggere il modulo.

Ad esempio, se il record che il modulo sta leggendo è un progetto, puoi specificare che ne vengano lette le attività.

Il modulo restituisce un array di dati dai campi di output specificati.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connessione]</td>
    <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Tipo di record]</td>

<td>Scegli il tipo di oggetto Workfront che il modulo deve leggere.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output]</td>

<td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Modulo di output personalizzato]</td>
     <td> <p>Seleziona i moduli personalizzati che desideri includere nel bundle di output per questo modulo, quindi i campi specifici dei moduli personalizzati da includere nell’output.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Riferimenti]</td>
   <td>Seleziona i campi di riferimento che desideri includere nell’output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Raccolte]</td>
   <td>Seleziona i campi di riferimento che desideri includere nell’output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Inserisci l’ID Workfront univoco del record che il modulo deve leggere.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **Aggiornamento alla versione del payload degli eventi**

Workfront ha recentemente rilasciato una nuova versione del servizio di sottoscrizione eventi. Questa nuova versione non cambia l’API Workfront, ma la funzionalità di sottoscrizione eventi. Questo modulo di azione aggiorna la versione del payload dell’evento utilizzata per questo scenario.

Per ulteriori informazioni sulla nuova versione di sottoscrizione eventi, consulta [Controllo delle versioni per sottoscrizione eventi](https://experienceleague.adobe.com/it/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) nella documentazione di Workfront

Per le risorse sulla conservazione degli scenari di Workfront Fusion durante l’aggiornamento di sottoscrizione eventi, inclusa la registrazione di un webinar, consulta [Conservazione degli scenari di Fusion durante l’aggiornamento alla versione 2 di sottoscrizione eventi](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=it).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Versione]</td> 
   <td> Seleziona la versione di sottoscrizione evento che desideri utilizzare per questo payload. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Aggiorna un record**


Questo modulo di azione aggiorna un oggetto, ad esempio un progetto, un’attività o un problema. Il modulo ti consente di selezionare i campi dell’oggetto disponibili nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID dell’oggetto ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Inserisci l’ID Workfront univoco del record che deve aggiornare il modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Seleziona il tipo di record Workfront che il modulo deve aggiornare.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Seleziona i campi che desideri rendere disponibili per l’input di dati. Questo ti consente di utilizzare tali campi senza dover scorrere quelli non necessari. Quindi puoi inserire o mappare i dati in questi campi.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Seleziona i moduli personalizzati per i quali desideri specificare i valori dei campi nel nuovo record. Dopo aver selezionato il modulo, inserisci i dati per i campi del modulo.<p> Per fornire i valori dei campi di un modulo che stai allegando in questo modulo, includi l’ID del modulo personalizzato nella sezione dei campi da mappare.</td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Quando inserisci il testo per un campo personalizzato o un oggetto [!UICONTROL Nota] (Commento o risposta), puoi utilizzare i tag di HTML nel campo [!UICONTROL Testo nota] per creare testo formattato, ad esempio in grassetto o in corsivo.


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Carica documento]**

Questo modulo di azione carica un documento in un oggetto Workfront, ad esempio un progetto, un’attività o un problema. Questo modulo carica il documento suddiviso in blocchi, rendendo il processo di caricamento più semplice per Workfront.

Questo modulo può gestire file di dimensioni maggiori rispetto al modulo legacy e fa parte di un rollout graduale per le organizzazioni che dispongono di un pacchetto Workfront Ultimate.

Puoi specificare la posizione del documento, il file che desideri caricare e un nuovo nome facoltativo per il file.

Il modulo restituisce l’ID del documento e dei campi associati, insieme a eventuali campi e valori personalizzati a cui ha accesso la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID record correlato]</td> 
   <td>Inserisci l’ID Workfront univoco del record su cui desideri caricare il documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record correlato]</td> 
   <td>Seleziona il tipo di record Workfront su cui il modulo deve caricare il documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID cartella]</td> 
   <td>A seconda del tipo di record correlato, potrebbe essere necessario inserire oppure mappare un ID cartella.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File di origine]</td> 
   <td> <p>Seleziona un file di origine da un modulo precedente oppure mappa il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta [Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### Ricerche

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Leggi record correlati]**

Questo modulo di ricerca legge i record che corrispondono alla query di ricerca specificata, in un determinato oggetto principale.

Puoi specificare quali campi includere nell’output. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record principale (oggetto Workfront) di cui desideri leggere i record associati.</p> <p>Per un elenco dei tipi di oggetto Workfront per i quali puoi utilizzare questo modulo, consulta <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID record principale]</td> 
   <td> <p>Inserisci oppure mappa l’ID del record principale di cui desideri leggere i record associati.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL, dopo “ID=”. Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Raccolte]</td> 
   <td>Seleziona o mappa il tipo di record secondario che il modulo deve leggere.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni che desideri includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ricerca]**

Questo modulo di ricerca cerca i record in un oggetto in Workfront che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record Workfront che deve ricercare il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Elenco moduli personalizzati]</td> 
   <td> <p>Seleziona almeno un modulo personalizzato. I campi di questi moduli personalizzati saranno disponibili per la query di ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Set di risultati]</td> 
   <td>Seleziona un’opzione per specificare se il modulo deve ottenere il primo risultato che corrisponde ai criteri di ricerca o tutti i risultati corrispondenti.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Massimo]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi dei criteri di ricerca]</td> 
   <td> <p>Seleziona i campi che desideri utilizzare per i criteri di ricerca. Questi campi saranno quindi disponibili nel menu a discesa Criteri di ricerca.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteri di ricerca]</td> 
   <td> <p>Inserisci il campo in base al quale desideri eseguire la ricerca, l’operatore da utilizzare nella query e il valore ricercato nel campo.</p> <p>Nota: non utilizzare <code>username </code> nei criteri di ricerca. L’inclusione di <code>username </code> in una query API per Workfront effettua l’accesso dell’utente a Workfront e la ricerca non avrà esito positivo.</p> <p>Nota: <code>In</code> e <code>NotIn</code> utilizzano gli array. Gli input devono essere in formato array.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi che desideri includere nell’output per questo modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Riferimenti]</td> 
   <td>Seleziona i campi di riferimento che desideri includere nella ricerca.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Raccolte]</td> 
   <td>Seleziona le raccolte che desideri aggiungere alla ricerca.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ricerca (legacy)]**

>[!IMPORTANT]
>
>Questo modulo è stato sostituito con il modulo Cerca record. È consigliato utilizzare tale modulo nei nuovi scenari.
>Gli scenari esistenti che utilizzano questo modulo continueranno a funzionare come previsto. Questo modulo verrà rimosso dal selettore di moduli a maggio 2025.

Questo modulo di ricerca cerca i record in un oggetto in Workfront che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Seleziona il tipo di record Workfront che deve ricercare il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Set di risultati]</td> 
   <td>Seleziona un’opzione per specificare se il modulo deve ottenere il primo risultato che corrisponde ai criteri di ricerca o tutti i risultati corrispondenti.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Massimo]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi dei criteri di ricerca]</td> 
   <td> <p>Seleziona i campi che desideri utilizzare per i criteri di ricerca. Questi campi saranno quindi disponibili nel menu a discesa Criteri di ricerca.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteri di ricerca]</td> 
   <td> <p>Inserisci il campo in base al quale desideri eseguire la ricerca, l’operatore da utilizzare nella query e il valore ricercato nel campo.</p> <p>Nota: non utilizzare <code>username </code> nei criteri di ricerca. L’inclusione di <code>username </code> in una query API per Workfront effettua l’accesso dell’utente a Workfront e la ricerca non avrà esito positivo.</p> <p>Nota: <code>In</code> e <code>NotIn</code> utilizzano gli array. Gli input devono essere in formato array.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi che desideri includere nell’output per questo modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Riferimenti]</td> 
   <td>Seleziona i campi di riferimento che desideri includere nella ricerca.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Raccolte]</td> 
   <td>Seleziona le raccolte che desideri aggiungere alla ricerca.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## Tipi di oggetto Workfront disponibili per ciascun modulo di Workfront

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Tipi di oggetto disponibili per ciascun modulo trigger di Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Osserva record]</th> 
   <th>[!UICONTROL Osserva campo]</th> 
   <th>[!UICONTROL Osserva eventi]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo di approvazione</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Assegnazione</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Linea di base</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Record della fatturazione </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tariffa di fatturazione</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Azienda</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dashboard</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Cartella documenti</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Richiesta documento</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Versione documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Spesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo di spesa</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gruppo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Ora</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo di ora</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iterazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mansione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce diario</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Milestone</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Percorso milestone</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tag nota</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Progetto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utente progetto</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Approvazione bozza</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tempo riservato* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Rapporto</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Rischio</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di rischio</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Approvatore passaggio</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Attività</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modello</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Attività modello</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Scheda orario</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utente</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Aggiorna</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipi di oggetto disponibili per ogni modulo di azione di Workfront**

>[!NOTE]
>
>Il modulo [!UICONTROL Scarica documento] non è incluso in questa tabella perché i tipi di oggetto Workfront non fanno parte della sua configurazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Crea un record]</th> 
   <th>[!UICONTROL Aggiorna un record]</th> 
   <th>[!UICONTROL Elimina un record]</th> 
   <th>[!UICONTROL Carica documento]</th> 
   <th>[!UICONTROL Leggi un record]</th> 
   <th>[!UICONTROL Chiamata API personalizzata]</th> 
   <th>[!UICONTROL Azioni varie]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo di approvazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Assegnazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Linea di base</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>Record della fatturazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tariffa di fatturazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Azienda</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Cartella documenti</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Versione documento</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tasso di cambio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Spesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tipo di spesa</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Documento esterno</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Gruppo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ora</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di ora</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iterazione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mansione</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce diario</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Milestone</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Percorso milestone</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tag nota</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Progetto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utente progetto</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tempo riservato* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Rischio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di rischio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Approvatore passaggio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Attività</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modello</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Attività modello</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Scheda orario</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Utente</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Aggiorna</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipi di oggetto disponibili per ogni modulo di ricerca di Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Ricerca]</th> 
   <th>[!UICONTROL Leggi record correlati]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processo di approvazione</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Assegnazione</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Record della fatturazione</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tariffa di fatturazione</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Azienda</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Documento</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Cartella documenti</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Versione documento</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Spesa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di spesa</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Gruppo</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Ora</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di ora</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problema</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Iterazione</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Mansione</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce diario</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Milestone</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Percorso milestone</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Nota</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tag nota</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programma</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Progetto</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utente progetto</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tempo riservato* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Rischio</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tipo di rischio</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Approvatore passaggio</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Attività</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Team</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modello</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Attività modello</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Scheda orario</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utente</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Delega utente</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

È consigliabile verificare che questo funzioni come previsto.

+++

## Filtri per sottoscrizione a eventi nei moduli Workfront > [!UICONTROL Osserva eventi]

>[!NOTE]
>
>* È fortemente consigliato utilizzare i filtri di sottoscrizione a eventi nei moduli [!UICONTROL Osserva eventi].
>
>* Workfront ha recentemente rilasciato una nuova versione del servizio di sottoscrizione eventi. Questa nuova versione non cambia l’API Workfront, ma la funzionalità di sottoscrizione eventi. Questo modulo di azione aggiorna la versione del payload dell’evento utilizzata per questo scenario.
>
>   Per ulteriori informazioni sulla nuova versione di sottoscrizione a eventi, consulta [Controllo delle versioni per sottoscrizioni a eventi](https://experienceleague.adobe.com/it/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) nella documentazione di Workfront
>
>   Per le risorse si come conservare gli scenari di Workfront Fusion durante l’aggiornamento della sottoscrizione a eventi, inclusa la registrazione di un webinar, consulta [Conservazione degli scenari di Fusion durante l’aggiornamento V2 delle sottoscrizioni a eventi(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=it)].

Il modulo [!UICONTROL Osserva eventi] di Workfront attiva scenari basati su un webhook che crea una sottoscrizione a eventi nell’API Workfront. La sottoscrizione a eventi consiste in un set di dati che determina quali eventi vengono inviati al webhook. Ad esempio, se imposti un modulo [!UICONTROL Osserva eventi] per rilevare eventuali problemi, la sottoscrizione a eventi invia solo eventi relativi ai problemi.

Utilizzando i filtri per le sottoscrizioni a eventi, gli utenti di Fusion possono creare sottoscrizioni a eventi più specifiche per i propri casi d’uso. Ad esempio, puoi impostare una sottoscrizione a eventi nell’API di Workfront per inviare al webhook solo i problemi che si verificano in un progetto specifico, assicurandoti che il modulo [!UICONTROL Osserva eventi] venga attivato solo per i problemi di quel progetto. La possibilità di creare trigger più limitati migliora la progettazione degli scenari riducendo il numero di trigger irrilevanti.

Questa operazione è diversa dalla configurazione di un filtro nello scenario Workfront Fusion. Senza un filtro per la sottoscrizione a eventi, il webhook riceverebbe tutti gli eventi relativi al tipo di oggetto selezionato. La maggior parte di questi eventi sarebbe irrilevante per lo scenario in question e deve quindi essere filtrata prima che lo scenario possa continuare.

Nel filtro Workfront > Osserva eventi sono disponibili i seguenti operatori:

* Uguale a
* Non uguale a
* Maggiore di
* Minore di
* È maggiore di o uguale a
* È minore di o uguale a
* Contiene
* Esiste
   * Questo operatore non richiede un valore e il campo del valore è assente.
* Non esiste
   * Questo operatore non richiede un valore e il campo del valore è assente.
* Cambiato
   * Questo operatore non richiede un valore e il campo del valore è assente.
   * Questo operatore ignora il campo Stato.
   * Quando utilizzi `Changed`, seleziona **Solo eventi aggiornati** nel campo **Origine record**.

>[!IMPORTANT]
>
>Non è possibile modificare i filtri nei webhook Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.

>[!INFO]
>
>**Esempio:** considera uno scenario che elabora nuovi problemi assegnati a un utente specifico, Ana.
>
>### Filtrare gli eventi utilizzando un filtro per la sottoscrizione a eventi (consigliato)
>
>Utilizzando il filtro eventi, puoi configurare il webhook per attivare lo scenario quando, al momento della creazione di un problema, questo viene assegnato ad Ana. Ana ha l’ID utente b378489d8f7cd3cee0539260720a84b7.
>
>![Filtro eventi](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Se vengono creati 100 problemi in un giorno, ma solo due di essi sono assegnati ad Ana, lo scenario verrebbe eseguito due volte.
>
>### Filtrare gli eventi all’interno dello scenario (non consigliato)
>
>Per filtrare gli eventi in modo che vengano elaborati solo i problemi assegnati ad Ana, puoi creare un filtro dopo il modulo [!UICONTROL Osserva eventi].
>
>![Senza filtro eventi](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Se in un giorno vengono creati 100 problemi, ma solo due di questi sono assegnati ad Ana, lo scenario verrebbe eseguito 100 volte. 98 esecuzioni si interromperebbero al filtro, ma il modulo trigger continuerebbe comunque a consumare dati e ad eseguire operazioni in tutte le esecuzioni.

Per ulteriori informazioni sulle sottoscrizioni a eventi di Workfront, consulta [Domande frequenti: sottoscrizioni a eventi](https://experienceleague.adobe.com/it/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Per ulteriori informazioni sui webhook, consulta [Trigger istantanei (webhook) in Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Per ulteriori informazioni sui filtri negli scenari, consulta [Aggiungere un filtro a uno scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
