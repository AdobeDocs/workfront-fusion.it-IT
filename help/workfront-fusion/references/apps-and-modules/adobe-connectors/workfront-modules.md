---
title: Moduli Adobe Workfront
description: Puoi utilizzare il connettore Adobe Workfront Fusion Adobe Workfront per automatizzare i processi all’interno di Workfront. Se disponi di una licenza di Workfront Fusion for Work Automation and Integration, puoi utilizzarla anche per connettersi ad app e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '8067'
ht-degree: 6%

---

# Moduli Adobe Workfront

Puoi utilizzare il connettore Adobe Workfront Fusion Adobe Workfront per automatizzare i processi all’interno di Workfront. È inoltre possibile collegare Workfront ad altre applicazioni e servizi.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).


>[!NOTE]
>
>* Se la tua organizzazione utilizza il pacchetto di licenze legacy (basato sui connettori), deve disporre di una licenza Workfront Fusion for Work Automation and Integration per connettersi ad app e servizi di terze parti. Il connettore Workfront non viene conteggiato rispetto al numero di app attive disponibili per l’organizzazione. Tutti gli scenari, anche se utilizzano solo l’app Workfront, vengono conteggiati in base al numero totale di scenari della tua organizzazione.

+++

## Connessione di Workfront a Workfront Fusion

Il connettore Workfront utilizza OAuth 2.0 per connettersi a Workfront.

Puoi creare una connessione al tuo account Workfront direttamente dall’interno di un modulo Workfront Fusion.

1. In qualsiasi modulo di Adobe Workfront, fai clic su **Aggiungi** accanto al campo Connessione.
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
          <p>Immettere un nome per la nuova connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo di connessione]</td>
        <td>
          <p>Specificare se ci si connette a un account di servizio o a un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti l'ID client di Workfront. È disponibile nell’area Applicazioni OAuth2 dell’area Configura di Workfront. Apri l’applicazione specifica a cui ti stai connettendo per visualizzare l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti il segreto del client Workfront. È disponibile nell’area Applicazioni OAuth2 dell’area Configura di Workfront. Se non disponi di un segreto client per l’applicazione OAuth2 in Workfront, puoi generarne un altro. Per istruzioni, consulta la documentazione di Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL autenticazione]</td>
        <td>Questo può rimanere il valore predefinito, oppure puoi immettere l'URL dell'istanza Workfront, seguito da <code>/integrations/oauth2</code>. <p>Esempio: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Prefisso host]</td>
        <td>Nella maggior parte dei casi, questo valore deve essere <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

   Se non hai effettuato l’accesso a Workfront, vieni indirizzato a una schermata di accesso. Dopo aver effettuato l’accesso, puoi consentire la connessione.

>[!NOTE]
>
>* Le connessioni OAuth 2.0 all’API Workfront non si basano più sulle chiavi API.
>* Per creare una connessione a un ambiente Sandbox Workfront, è necessario creare un&#39;applicazione OAuth2 in tale ambiente e quindi utilizzare l&#39;ID client e il segreto client generati da tale applicazione nella connessione.

## Moduli Workfront e relativi campi

Quando configuri i moduli di Workfront, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi Workfront aggiuntivi, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Se non trovi i campi più aggiornati in un modulo Workfront, potrebbe trattarsi di un problema di caching. Attendi un’ora e riprova.
>* I codici di stato HTTP 429 di Adobe Workfront non dovrebbero causare disattivazioni, ma attivare invece una breve pausa di esecuzione nello scenario.

* [Triggers](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Guarda gli eventi]**

Questo modulo trigger esegue uno scenario in tempo reale quando in Workfront vengono aggiunti, aggiornati o eliminati oggetti di un tipo specifico

Il modulo restituisce tutti i campi standard associati al record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

1. Fai clic su **[!UICONTROL Aggiungi]** a destra della casella **Webhook**.

1. Configura il webhook nella casella **[!UICONTROL Aggiungi un hook]** visualizzato.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Nome webhook]</td> 
      <td>Immetti un nome per il webhook</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Tipo di record]</td> 
      <td>Selezionare il tipo di record Workfront che si desidera controllare nel modulo.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL State]</td> 
      <td>Seleziona se desideri controllare lo stato precedente o quello nuovo.<ul><li><p><b>[!UICONTROL Nuovo stato]</b></p><p>Attiva uno scenario quando il record cambia <b>in</b> un valore specificato.</p><p>Ad esempio, se lo stato è impostato su [!UICONTROL Nuovo stato] e il filtro è impostato su [!UICONTROL Stato] [!UICONTROL È uguale a] [!UICONTROL In corso], il webhook attiva uno scenario quando lo stato [!UICONTROL Stato] diventa [!UICONTROL In corso], indipendentemente dallo stato precedente. </p></li><li><p><b>[!UICONTROL Old State]</b></p><p>Attiva uno scenario quando il record cambia <b> da</b> a un determinato valore.</p><p>Ad esempio, se lo stato è impostato su [!UICONTROL Old State] e il filtro è impostato su [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In corso], il webhook attiva uno scenario quando uno stato [!UICONTROL Status] attualmente [!UICONTROL In corso] passa a un altro stato. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>È possibile impostare i filtri per controllare solo i record che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND.</p> <p><b>NOTA</b>: non è possibile modificare i filtri nei webhook di Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni di eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.</p> <p>Per ulteriori informazioni sui filtri eventi, vedere <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtri di sottoscrizione eventi nei moduli Workfront &gt; [!UICONTROL Watch Events]</a> in questo articolo.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Escludi eventi creati da questa connessione</td> 
      <td>Abilita questa opzione per escludere gli eventi creati o aggiornati utilizzando lo stesso connettore utilizzato dal modulo di attivazione. Questo può evitare situazioni in cui uno scenario potrebbe attivarsi da solo, causandone la ripetizione in un ciclo infinito.<p><b>NOTA</b>: il tipo di record Assegnazione non include questa opzione.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Origine record]</td> 
      <td>
       <p>Scegliere se si desidera che lo scenario controlli [!UICONTROL Solo nuovi record], [!UICONTROL Solo record aggiornati], [!UICONTROL Record nuovi e aggiornati] o [!DNL Deleted Records Only].</p>
       <p><b>NOTA</b>: se si sceglie [!UICONTROL Record nuovi e aggiornati], la creazione del webhook crea 2 sottoscrizioni di eventi (per lo stesso indirizzo del webhook).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Dopo la creazione del webhook, puoi visualizzare l’indirizzo dell’endpoint a cui vengono inviati gli eventi.

Per ulteriori informazioni, consulta la sezione [Esempi di payload degli eventi](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) nell&#39;articolo API di sottoscrizione eventi nella documentazione di Workfront.

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Campo di controllo]**

Questo modulo trigger esegue uno scenario quando viene aggiornato un campo specificato. Il modulo restituisce sia il vecchio che il nuovo valore del campo specificato. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera controllare nel modulo.</p> <p>Selezionare ad esempio [!UICONTROL Attività] se si desidera avviare l'esecuzione dello scenario ogni volta che viene aggiornato un campo record in un'attività.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td>Seleziona il campo che desideri che il modulo controlli per gli aggiornamenti. Questi campi riflettono i campi impostati dall’amministratore di Workfront per il tracciamento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Output]</td> 
   <td>Seleziona i campi oggetto da includere nel bundle di output per questo modulo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Osserva record]**

Questo modulo trigger esegue uno scenario quando vengono aggiunti, aggiornati o entrambi gli oggetti di un tipo specifico. Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Nell’output, il modulo indica se ogni record è nuovo o aggiornato.

I record aggiunti e aggiornati dall&#39;ultima esecuzione dello scenario vengono restituiti come nuovi record.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Scegliere se si desidera che lo scenario controlli [!UICONTROL Solo nuovi record], [!UICONTROL Solo record aggiornati] o [!UICONTROL Record nuovi e aggiornati].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera controllare nel modulo.</p> <p>Ad esempio, se si desidera avviare lo scenario ogni volta che viene creato un nuovo progetto, selezionare [!UICONTROL Progetto]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference]</td> 
   <td> <p>Seleziona i campi di riferimento da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Seleziona i campi della raccolta da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro facoltativo]</td> 
   <td> <p>(Avanzata) Digita una stringa di codice API per definire eventuali parametri o codice aggiuntivi che definiranno meglio i criteri. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

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
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di oggetto]</td> 
   <td> <p>Selezionare il tipo di oggetto da convertire. Questo è il tipo di oggetto prima della conversione.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Converti in]</td> 
   <td>Selezionare l'oggetto in cui si desidera convertirlo. Questo è il tipo di oggetto dopo la conversione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;ID Oggetto&gt;]</td> 
   <td> <p>Immettere l'ID dell'oggetto. </p> <p>Nota: quando si immette l'ID di un oggetto, è possibile iniziare a digitare il nome dell'oggetto, quindi selezionarlo dall'elenco. Il modulo immette quindi l’ID appropriato nel campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID modello [!UICONTROL]</td> 
   <td> <p>Per la conversione in progetto, seleziona l’ID modello da utilizzare per il progetto.</p> <p>Nota: quando si immette l'ID di un oggetto, è possibile iniziare a digitare il nome dell'oggetto, quindi selezionarlo dall'elenco. Il modulo immette quindi l’ID appropriato nel campo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Moduli personalizzati]</td> 
   <td>Seleziona i moduli personalizzati da aggiungere all’oggetto appena convertito, quindi immetti i valori per i campi del modulo personalizzato.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>Abilitare le opzioni desiderate durante la conversione dell'oggetto. Sono disponibili opzioni a seconda dell’oggetto da o verso il quale si sta eseguendo la conversione.</p> </td> 
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

Questo modulo di azione crea un oggetto, ad esempio un progetto, un’attività o un problema in Workfront, e consente di aggiungere un modulo personalizzato al nuovo oggetto. Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Assicurati di fornire il numero minimo di campi di input. Ad esempio, se desideri creare un problema, devi fornire un ID progetto principale valido nel campo ID progetto per indicare dove il problema dovrebbe risiedere in Workfront. Puoi utilizzare il pannello di mappatura per mappare queste informazioni da un altro modulo dello scenario, oppure puoi immetterle manualmente digitando il nome e selezionandolo dall’elenco.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera venga creato dal modulo.</p> <p>Se ad esempio si desidera creare un progetto, selezionare [!UICONTROL Project] dall'elenco a discesa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Seleziona campi da mappare]</td> 
   <td> <p>Selezionare i campi che si desidera rendere disponibili per l'immissione dei dati. Questo consente di utilizzare questi campi senza dover scorrere quelli non necessari. È quindi possibile immettere o mappare i dati in questi campi.</p> <p>Per i campi nei moduli personalizzati, utilizza il campo <b>[!UICONTROL Allega modulo personalizzato]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allega Modulo Personalizzato]</td> 
   <td>Selezionare i moduli personalizzati che si desidera aggiungere al nuovo oggetto, quindi immettere o mappare i valori per tali campi.</td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Quando si immette l&#39;ID di un oggetto, è possibile iniziare a digitare il nome dell&#39;oggetto, quindi selezionarlo dall&#39;elenco. Il modulo immette quindi l’ID appropriato nel campo.
>* Quando immetti il testo per un campo personalizzato o un oggetto [!UICONTROL Note] (Commento o risposta), puoi utilizzare i tag di HTML nel campo [!UICONTROL Testo nota] per creare testo RTF, ad esempio testo in grassetto o corsivo.
>



>[!NOTE]
>
>Gli utenti vengono creati con lo stato Disattivato e In attesa di approvazione. Se la tua organizzazione è stata migrata al Adobe Admin Console e il badge In attesa di approvazione non viene rimosso in pochi minuti, puoi approvare l’utente.
>
>* **Risolvi singoli utenti**
>
>      È possibile risolvere singoli utenti nell&#39;elenco Utenti.
>
>      1. Selezionare uno o più utenti nell&#39;elenco Utenti.
>      1. Fai clic sul menu a tre punti nell’intestazione dell’elenco.
>      1. Seleziona **Approva**.
>      1. Dopo alcuni minuti, aggiorna la pagina.
>
>* **Risolvi utenti aggiunti in un batch di grandi dimensioni**
>
>   Per risolvere gli utenti che sono stati aggiunti in un batch di grandi dimensioni, puoi aggiungere direttamente il batch di utenti a Adobe Admin Console.
>
>   Per istruzioni, vedere [Gestione di più utenti | Caricamento CSV in blocco](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) nella documentazione di Adobe.

+++

+++ **[!UICONTROL Crea record (legacy)]**

>[!IMPORTANT]
>
>Questo modulo è stato sostituito con il modulo Crea un record. È consigliabile utilizzare tale modulo in nuovi scenari.
>>Gli scenari esistenti che utilizzano questo modulo continueranno a funzionare come previsto. Questo modulo verrà rimosso dal selettore dei moduli a maggio 2025.

Questo modulo di azione crea un oggetto, ad esempio un progetto, un’attività o un problema in Workfront. Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Assicurati di fornire il numero minimo di campi di input. Ad esempio, se desideri creare un problema, devi fornire un ID progetto principale valido nel campo ID progetto per indicare dove il problema dovrebbe risiedere in Workfront. Puoi utilizzare il pannello di mappatura per mappare queste informazioni da un altro modulo dello scenario, oppure puoi immetterle manualmente digitando il nome e selezionandolo dall’elenco.

Questo modulo non allega moduli personalizzati durante la creazione dell’oggetto. Per allegare moduli personalizzati durante la creazione di un oggetto, utilizzare il modulo [!UICONTROL Crea un record (allegare moduli personalizzati)].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera venga creato dal modulo.</p> <p>Se ad esempio si desidera creare un progetto, selezionare [!UICONTROL Project] dall'elenco a discesa.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Seleziona campi da mappare]</td> 
   <td>Selezionare i campi che si desidera rendere disponibili per l'immissione dei dati. Questo consente di utilizzare questi campi senza dover scorrere quelli non necessari.</td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Quando si immette l&#39;ID di un oggetto, è possibile iniziare a digitare il nome dell&#39;oggetto, quindi selezionarlo dall&#39;elenco. Il modulo immette quindi l’ID appropriato nel campo.
>* Quando immetti il testo per un campo personalizzato o un oggetto [!UICONTROL Note] (Commento o risposta), puoi utilizzare i tag di HTML nel campo [!UICONTROL Testo nota] per creare testo RTF, ad esempio testo in grassetto o corsivo.

+++

+++ **[!UICONTROL Chiamata API personalizzata]**

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API Workfront. In questo modo, puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli di Workfront.

Il modulo restituisce le seguenti informazioni:

* **[!UICONTROL Codice di stato]** (numero): indica il completamento o l&#39;errore della richiesta HTTP. Si tratta di codici standard che puoi cercare su Internet.
* **[!UICONTROL Intestazioni]** (oggetto): contesto più dettagliato per il codice di risposta/stato che non è correlato al corpo dell&#39;output. Non tutte le intestazioni visualizzate in un’intestazione di risposta sono intestazioni di risposta, quindi alcune potrebbero non essere utili.

  Le intestazioni di risposta dipendono dalla richiesta HTTP scelta durante la configurazione del modulo.

* **[!UICONTROL Corpo]** (oggetto): a seconda della richiesta HTTP scelta durante la configurazione del modulo, è possibile che alcuni dati vengano restituiti. Tali dati, ad esempio i dati di una richiesta GET, sono contenuti in questo oggetto.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Immettere un percorso relativo a <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL versione API]</td> 
   <td>Seleziona la versione dell’API Workfront che desideri venga utilizzata dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> <p>Nota: se ricevi errori ed è difficile determinarne l’origine, puoi modificare le intestazioni in base alla documentazione di Workfront. Se la chiamata API personalizzata restituisce un errore di richiesta HTTP 422, provare a utilizzare un'intestazione <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> <p>Suggerimento: è consigliabile inviare informazioni tramite il corpo JSON anziché come parametri di query.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Elimina record]**

Questo modulo di azione elimina un oggetto, ad esempio un progetto, un’attività o un problema in Workfront.

Specifica l’ID del record.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Forza eliminazione]</td> 
   <td>Abilita questa opzione per garantire che il record venga eliminato, anche se l’interfaccia utente di Workfront richiede la conferma dell’eliminazione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL eliminazione asincrona]</td> 
   <td>Abilita questa opzione per consentire al modulo di eliminarlo in modo asincrono.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Immettere l'ID Workfront univoco del record che si desidera eliminare dal modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td>Selezionare il tipo di record Workfront da eliminare dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Per evitare che i record vengano eliminati a causa di operazioni asincrone, è consigliabile effettuare la configurazione dello scenario seguente.
>
>1. Eliminare il record in modo sincrono.
>1. Aggiungi la gestione degli errori al modulo Elimina record per ignorare l’errore causato dal timeout di 40 secondi.


+++

+++ **[!UICONTROL Scarica documento]**

Questo modulo di azione scarica un documento da Workfront.

Specifica l’ID del record.

Il modulo restituisce il contenuto, il nome, l&#39;estensione e la dimensione del file del documento. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID documento]</td> 
   <td> <p>Mappa o immetti manualmente l’ID Workfront univoco del documento che desideri scaricare dal modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Azione Varia]**

Questo modulo di azione consente di eseguire azioni sull’API.

>[!NOTE]
>
>A luglio 2024, l&#39;azione `convertToProject` include il campo `copyCategories`. Se è impostato su `TRUE`, tutti i moduli personalizzati verranno inclusi nel progetto in cui viene convertito il problema.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront con cui si desidera interagire il modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Action]</td> 
   <td> <p>Selezionare l'azione che si desidera venga eseguita dal modulo.</p> <p>Potrebbe essere necessario compilare ulteriori campi, a seconda del tipo di record [!UICONTROL] e dell'azione [!UICONTROL] scelti. Alcune combinazioni di queste due impostazioni possono richiedere solo un ID record, mentre altre (come Project per il tipo di record <strong>[!UICONTROL]</strong> e [!UICONTROL Allega modello] per l'azione <strong>[!UICONTROL]</strong>) richiedono informazioni aggiuntive (ad esempio un ID oggetto e un ID modello).</p><p>Per le opzioni disponibili per alcune azioni, vedere <a href="#misc-action-options" class="MCXref xref">Opzioni di azioni varie</a> in questo articolo.</p> <p>Per informazioni dettagliate sui singoli campi, consulta la <a href="http://developer.workfront.com/">documentazione per gli sviluppatori di Workfront</a>. <p><strong>Nota</strong>: il sito della documentazione per gli sviluppatori include informazioni solo tramite la versione 14 dell'API, ma contiene comunque informazioni importanti per le chiamate API. </p> 
    <ol> 
     <li value="1"> <p>Seleziona il tipo di record nella barra di navigazione a sinistra, nella pagina della documentazione per gli sviluppatori di Workfront. I seguenti tipi hanno pagine proprie:</p> 
      <ul> 
       <li> <p>[!UICONTROL Progetti]</p> </li> 
       <li> <p>[!UICONTROL Attività]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL Utenti]</p> </li> 
       <li> <p>[!UICONTROL Documenti]</p> </li> 
      </ul> <p>Per tutti gli altri tipi di record, selezionare <b>[!UICONTROL Altri oggetti ed endpoint]</b> e individuare il tipo di record nelle pagine ordinate alfabeticamente.</p> </li> 
     <li value="2"> <p>Nella pagina del tipo di record appropriato, cercare l'azione (Ctrl+F o Comando+F).</p> </li> 
     <li value="3"> <p>Visualizza le descrizioni dei campi disponibili nell'azione selezionata.</p> </li> 
    </ol> <p>Nota:  <p>Durante la creazione di una bozza tramite il modulo [!UICONTROL Misc Action] di Workfront, è consigliabile creare una bozza senza opzioni avanzate, quindi aggiornarla utilizzando l'API SOAP [!DNL Workfront Proof].</p><p>Per ulteriori informazioni sulla creazione di una bozza con l'API Workfront (utilizzata da questo modulo), vedere <a href="https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Aggiungere opzioni di bozza avanzate durante la creazione di una bozza tramite l'API Adobe Workfront</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Immetti o mappa l’ID Workfront univoco del record con cui desideri interagire il modulo.<p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

#### Opzioni di azione varie

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
   <li>clearFinancials<p>Cancella i dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella le notifiche promemoria</p></li>
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
   <li>clearFinancials<p>Cancella i dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella le notifiche promemoria</p></li>
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
   <li>clearFinancials<p>Cancella i dati finanziari</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Cancella le notifiche promemoria</p></li>
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
   <li>clearDeliverables<p>Cancella gli obiettivi</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Cancella i dati finanziari</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Cancella la configurazione delle proprietà e dei problemi della coda</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Cancella le notifiche promemoria</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Leggi un record]**

Questo modulo di azione recupera i dati da un singolo record.

Specifica l’ID del record. È inoltre possibile specificare quali record correlati si desidera che vengano letti dal modulo.

Ad esempio, se il record che il modulo sta leggendo è un progetto, è possibile specificare che si desidera che le attività del progetto vengano lette.

Il modulo restituisce un array di dati dai campi di output specificati.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Tipo di record]</td>

<td>Scegliere il tipo di oggetto Workfront che si desidera venga letto dal modulo.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output]</td>

<td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
    <td>Modulo personalizzato di output [!UICONTROL]</td>
     <td> <p>Seleziona i moduli personalizzati da includere nel bundle di output per questo modulo, quindi seleziona i campi specifici dai moduli personalizzati da includere nell’output.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Riferimenti]</td>
   <td>Selezionare i campi di riferimento da includere nell'output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Raccolte]</td>
   <td>Selezionare i campi di riferimento da includere nell'output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Immettere l'ID Workfront univoco del record che si desidera venga letto dal modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Leggi record (legacy)]**

>[!IMPORTANT]
>
>Questo modulo è stato sostituito dal modulo Leggi record. È consigliabile utilizzare tale modulo in nuovi scenari.
>>Gli scenari esistenti che utilizzano questo modulo continueranno a funzionare come previsto. Questo modulo verrà rimosso dal selettore dei moduli a maggio 2025.

Questo modulo di azione recupera i dati da un singolo record.

Specifica l’ID del record. È inoltre possibile specificare quali record correlati si desidera che vengano letti dal modulo.

Ad esempio, se il record che il modulo sta leggendo è un progetto, è possibile specificare che si desidera che le attività del progetto vengano lette.

Il modulo restituisce un array di dati dai campi di output specificati.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Tipo di record]</td>

<td>Scegliere il tipo di oggetto Workfront che si desidera venga letto dal modulo.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output]</td>

<td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Riferimenti]</td>
   <td>Selezionare i campi di riferimento da includere nell'output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Raccolte]</td>
   <td>Selezionare i campi di riferimento da includere nell'output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Immettere l'ID Workfront univoco del record che si desidera venga letto dal modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **Aggiorna versione payload eventi**

Workfront ha recentemente rilasciato una nuova versione del suo servizio di abbonamento agli eventi. La nuova versione non è una modifica all’API Workfront, ma piuttosto una modifica alla funzionalità di abbonamento agli eventi. Questo modulo di azione aggiorna la versione del payload dell’evento utilizzata per questo scenario.

Per ulteriori informazioni sulla nuova versione della sottoscrizione dell&#39;evento, vedere [Controllo delle versioni della sottoscrizione dell&#39;evento](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) nella documentazione di Workfront

Per le risorse sulla conservazione degli scenari di Workfront Fusion durante l&#39;aggiornamento dell&#39;abbonamento agli eventi, inclusa la registrazione di un webinar, consulta [Conservazione degli scenari di Fusion durante l&#39;aggiornamento V2 degli abbonamenti agli eventi](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL versione]</td> 
   <td> Seleziona la versione della sottoscrizione evento da utilizzare per questo payload. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Aggiorna un record**


Questo modulo di azione aggiorna un oggetto, ad esempio un progetto, un’attività o un problema. Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID dell’oggetto ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Immettere l'ID Workfront univoco del record che si desidera aggiornare nel modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera aggiornare nel modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selezionare i campi che si desidera rendere disponibili per l'immissione dei dati. Questo consente di utilizzare questi campi senza dover scorrere quelli non necessari. È quindi possibile immettere o mappare i dati in questi campi.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Selezionare i moduli personalizzati per i quali si desidera specificare i valori dei campi nel nuovo record. Dopo aver selezionato il modulo, immettere i dati per i campi del modulo.<p> Per fornire i valori dei campi per un modulo che si sta allegando in questo modulo, includere l'ID del modulo personalizzato nella sezione campi da mappare.</td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Quando immetti il testo per un campo personalizzato o un oggetto [!UICONTROL Note] (Commento o risposta), puoi utilizzare i tag di HTML nel campo [!UICONTROL Testo nota] per creare testo RTF, ad esempio testo in grassetto o corsivo.


+++

+++ **[!UICONTROL Aggiorna record (legacy)]**

>[!IMPORTANT]
>
>Questo modulo è stato sostituito dal modulo Aggiorna record. È consigliabile utilizzare tale modulo in nuovi scenari.
>>Gli scenari esistenti che utilizzano questo modulo continueranno a funzionare come previsto. Questo modulo verrà rimosso dal selettore dei moduli a maggio 2025.

Questo modulo di azione aggiorna un oggetto, ad esempio un progetto, un’attività o un problema. Il modulo consente di selezionare quale dei campi dell’oggetto è disponibile nel modulo.

Specifica l’ID del record.

Il modulo restituisce l’ID dell’oggetto ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Immettere l'ID Workfront univoco del record che si desidera aggiornare nel modulo.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera aggiornare nel modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Selezionare i campi che si desidera rendere disponibili per l'immissione dei dati. Questo consente di utilizzare questi campi senza dover scorrere quelli non necessari. È quindi possibile immettere o mappare i dati in questi campi.</td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Quando si immette l&#39;ID di un oggetto, è possibile iniziare a digitare il nome dell&#39;oggetto, quindi selezionarlo dall&#39;elenco. Il modulo immette quindi l’ID appropriato nel campo.
>* Quando immetti il testo per un campo personalizzato o un oggetto [!UICONTROL Note] (Commento o risposta), puoi utilizzare i tag di HTML nel campo [!UICONTROL Testo nota] per creare testo RTF, ad esempio testo in grassetto o corsivo.

+++

+++ **[!UICONTROL Carica documento]**

Questo modulo di azione carica un documento in un oggetto Workfront, ad esempio un progetto, un’attività o un problema. Questo modulo carica il documento in blocchi, rendendo il processo di caricamento più semplice per Workfront.

Questo modulo può gestire file di dimensioni maggiori rispetto al modulo legacy e fa parte di un rollout graduale per le organizzazioni con un pacchetto Ultimate Workfront.

È possibile specificare la posizione del documento, il file da caricare e un nuovo nome facoltativo per il file.

Il modulo restituisce l’ID del documento e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID record correlato]</td> 
   <td>Immettere l'ID Workfront univoco del record in cui si desidera caricare il documento.</td> 
  </tr> 
  <tr> 
   <td>Tipo di record correlato a [!UICONTROL]</td> 
   <td>Seleziona il tipo di record Workfront in cui vuoi che il modulo carichi il documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID cartella]</td> 
   <td>A seconda del tipo di record correlato, potrebbe essere necessario immettere o mappare un ID cartella.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Carica documento (legacy)]**

Questo modulo di azione carica un documento in un oggetto Workfront, ad esempio un progetto, un’attività o un problema. Carica l’intero documento contemporaneamente.

È possibile specificare la posizione del documento, il file da caricare e un nuovo nome facoltativo per il file.

Il modulo restituisce l’ID del documento e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID record correlato]</td> 
   <td>Immettere l'ID Workfront univoco del record in cui si desidera caricare il documento.</td> 
  </tr> 
  <tr> 
   <td>Tipo di record correlato a [!UICONTROL]</td> 
   <td>Seleziona il tipo di record Workfront in cui vuoi che il modulo carichi il documento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID cartella]</td> 
   <td>A seconda del tipo di record correlato, potrebbe essere necessario immettere o mappare un ID cartella.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

Visualizzare un elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in [tipi di oggetto Workfront disponibili per ogni modulo di Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

### Ricerche

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Leggi record correlati]**

Questo modulo di ricerca legge i record corrispondenti alla query di ricerca specificata, in un particolare oggetto padre.

È possibile specificare quali campi includere nell&#39;output. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record padre (oggetto Workfront) di cui si desidera leggere i record associati.</p> <p>Vedere l'elenco dei tipi di oggetto Workfront per i quali è possibile utilizzare questo modulo in <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">tipi di oggetto Workfront disponibili per ogni modulo Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID record padre]</td> 
   <td> <p>Immettere o mappare l'ID del record padre di cui si desidera leggere i record associati.</p> <p>Per ottenere l’ID, apri l’oggetto Workfront nel browser e copia il testo alla fine dell’URL dopo "ID=". Ad esempio: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Raccolte]</td> 
   <td>Selezionare o mappare il tipo di record figlio che si desidera leggere nel modulo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Seleziona le informazioni da includere nel bundle di output per questo modulo.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ricerca]**

Questo modulo di ricerca cerca i record in un oggetto in Workfront che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera cercare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Elenco moduli personalizzati]</td> 
   <td> <p>Seleziona almeno un modulo personalizzato. I campi di questi moduli personalizzati saranno disponibili per la query di ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selezionare un'opzione per specificare se si desidera che il modulo ottenga il primo risultato corrispondente ai criteri di ricerca o tutti i risultati corrispondenti.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL max]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi criteri di ricerca]</td> 
   <td> <p>Selezionare i campi da utilizzare per i criteri di ricerca. Questi campi saranno quindi disponibili nel menu a discesa Criteri di ricerca.</p></td> 
  </tr> 
  <tr> 
   <td>Criteri di ricerca di [!UICONTROL]</td> 
   <td> <p>Immettere il campo in base al quale si desidera eseguire la ricerca, l'operatore che si desidera utilizzare nella query e il valore ricercato nel campo.</p> <p>Nota: non utilizzare <code>username </code> nei criteri di ricerca. L'inclusione di <code>username </code> in una query API per Workfront comporta l'accesso dell'utente a Workfront e la ricerca non avrà esito positivo.</p> <p>Nota: <code>In</code> e <code>NotIn</code> funzionano con gli array. Gli input devono essere in formato array.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Selezionare i campi da includere nell'output per questo modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Riferimenti]</td> 
   <td>Selezionare i campi di riferimento da includere nella ricerca.</td> 
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
>Questo modulo è stato sostituito con il modulo Record di ricerca. È consigliabile utilizzare tale modulo in nuovi scenari.
>>Gli scenari esistenti che utilizzano questo modulo continueranno a funzionare come previsto. Questo modulo verrà rimosso dal selettore dei moduli a maggio 2025.

Questo modulo di ricerca cerca i record in un oggetto in Workfront che corrispondono alla query di ricerca specificata.

Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app Workfront a Workfront Fusion, vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tipo di record]</td> 
   <td> <p>Selezionare il tipo di record Workfront che si desidera cercare nel modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Selezionare un'opzione per specificare se si desidera che il modulo ottenga il primo risultato corrispondente ai criteri di ricerca o tutti i risultati corrispondenti.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL max]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Campi criteri di ricerca]</td> 
   <td> <p>Selezionare i campi da utilizzare per i criteri di ricerca. Questi campi saranno quindi disponibili nel menu a discesa Criteri di ricerca.</p></td> 
  </tr> 
  <tr> 
   <td>Criteri di ricerca di [!UICONTROL]</td> 
   <td> <p>Immettere il campo in base al quale si desidera eseguire la ricerca, l'operatore che si desidera utilizzare nella query e il valore ricercato nel campo.</p> <p>Nota: non utilizzare <code>username </code> nei criteri di ricerca. L'inclusione di <code>username </code> in una query API per Workfront comporta l'accesso dell'utente a Workfront e la ricerca non avrà esito positivo.</p> <p>Nota: <code>In</code> e <code>NotIn</code> funzionano con gli array. Gli input devono essere in formato array.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Output]</td> 
   <td> <p>Selezionare i campi da includere nell'output per questo modulo.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Riferimenti]</td> 
   <td>Selezionare i campi di riferimento da includere nella ricerca.</td> 
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

## Tipi di oggetto Workfront disponibili per ogni modulo Workfront

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Tipi di oggetto disponibili per ogni modulo trigger di Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Osserva Record]</th> 
   <th>[!UICONTROL Watch Field]</th> 
   <th>[!UICONTROL Osserva Eventi]</th> 
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
   <td> Fatturazione </td> 
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
   <td>Dashboard di</td> 
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
   <td>Hour</td> 
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
   <td>Ruolo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce del diario</td> 
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
   <td>Utente Progetto</td> 
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
   <td>Tipo Rischio</td> 
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
   <td>Aggiornamento</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tipi di oggetto disponibili per ogni modulo azione di Workfront**

>[!NOTE]
>
>Il modulo [!UICONTROL Scarica documento] non è incluso in questa tabella perché i tipi di oggetto Workfront non fanno parte della relativa configurazione.

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
   <th>[!UICONTROL Crea record]</th> 
   <th>[!UICONTROL Aggiorna un record]</th> 
   <th>[!UICONTROL Elimina record]</th> 
   <th>[!UICONTROL Carica documento]</th> 
   <th>[!UICONTROL Leggi un record]</th> 
   <th>Chiamata API personalizzata [!UICONTROL]</th> 
   <th>[!UICONTROL Misc Action]</th> 
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
   <td>Fatturazione</td> 
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
   <td>Hour</td> 
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
   <td>Ruolo</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce del diario</td> 
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
   <td>Utente Progetto</td> 
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
   <td>Tipo Rischio</td> 
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
   <td>Aggiornamento</td> 
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
   <th>[!UICONTROL - Ricerca]</th> 
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
   <td>Fatturazione</td> 
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
   <td>Hour</td> 
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
   <td>Ruolo</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Voce del diario</td> 
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
   <td>Utente Progetto</td> 
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
   <td>Tipo Rischio</td> 
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

Si consiglia di verificare che questo funzioni come previsto.

+++

## Filtri di abbonamento agli eventi nei moduli Workfront > [!UICONTROL Guarda gli eventi]

>[!NOTE]
>
>* Si consiglia vivamente di utilizzare i filtri di abbonamento agli eventi nei moduli [!UICONTROL Osserva eventi].
>
>* Workfront ha recentemente rilasciato una nuova versione del suo servizio di abbonamento agli eventi. La nuova versione non è una modifica all’API Workfront, ma piuttosto una modifica alla funzionalità di abbonamento agli eventi. Questo modulo di azione aggiorna la versione del payload dell’evento utilizzata per questo scenario.
>
>   Per ulteriori informazioni sulla nuova versione della sottoscrizione dell&#39;evento, vedere [Controllo delle versioni della sottoscrizione dell&#39;evento](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) nella documentazione di Workfront
>
>   Per le risorse sulla conservazione degli scenari di Workfront Fusion durante l&#39;aggiornamento dell&#39;abbonamento agli eventi, inclusa la registrazione di un webinar, vedere [Conservazione degli scenari di Fusion durante l&#39;aggiornamento V2 delle sottoscrizioni agli eventi(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182)].

Il modulo [!UICONTROL Osserva eventi] di Workfront attiva scenari basati su un webhook che crea una sottoscrizione di eventi nell&#39;API Workfront. L’abbonamento a un evento è un set di dati che determina quali eventi vengono inviati al webhook. Ad esempio, se imposti un modulo [!UICONTROL Osserva eventi] che sta monitorando la presenza di problemi, l&#39;abbonamento all&#39;evento invia solo gli eventi correlati ai problemi.

Utilizzando i filtri di abbonamento agli eventi, gli utenti di Fusion possono creare sottoscrizioni agli eventi più adatte ai loro casi d’uso. Ad esempio, puoi impostare una sottoscrizione di evento nell&#39;API di Workfront per inviare al webhook solo i problemi che si trovano in un progetto specifico, assicurandoti che il modulo [!UICONTROL Osserva eventi] venga attivato solo per i problemi di quel progetto. La possibilità di creare trigger più piccoli migliora la progettazione dello scenario riducendo il numero di trigger irrilevanti.

Questa operazione è diversa dalla configurazione di un filtro nello scenario Workfront Fusion. Senza un filtro di abbonamento agli eventi, il webhook riceve tutti gli eventi relativi al tipo di oggetto selezionato. La maggior parte di questi eventi sarebbe irrilevante per lo scenario e deve essere filtrata prima che lo scenario possa continuare.

Nel filtro Workfront > Osserva eventi sono disponibili i seguenti operatori:

* Uguale a
* Non è uguale a
* Maggiore di
* Minore di
* Maggiore o uguale a
* Minore o uguale a
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
>Non è possibile modificare i filtri nei webhook Workfront esistenti. Per impostare filtri diversi per le sottoscrizioni di eventi Workfront, rimuovi il webhook corrente e creane uno nuovo.

>[!INFO]
>
>**Esempio:** considera uno scenario che elabora nuovi problemi assegnati a un utente specifico, Ana.
>
>### Filtrare gli eventi utilizzando un filtro di abbonamento agli eventi (scelta consigliata)
>
>Utilizzando il filtro eventi, puoi impostare il webhook per attivare lo scenario quando un problema viene assegnato ad Ana al momento della creazione. Ana ha l’ID utente b378489d8f7cd3cee0539260720a84b7.
>
>![Filtro eventi](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Se vengono creati 100 problemi in un giorno, ma solo due di essi sono assegnati ad Ana, lo scenario verrebbe eseguito due volte.
>
>### Filtra gli eventi all’interno dello scenario (scelta non consigliata)
>
>Per filtrare gli eventi in modo che vengano elaborati solo i problemi assegnati ad Ana, puoi creare un filtro dopo il modulo [!UICONTROL Osserva eventi].
>
>![Senza filtro eventi](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Se vengono creati 100 problemi in un giorno, ma solo due di essi sono assegnati ad Ana, lo scenario verrebbe eseguito 100 volte. 98 esecuzioni si fermerebbero al filtro, ma il modulo trigger consuma ancora dati ed esegue operazioni in tutte le esecuzioni.

Per ulteriori informazioni sulle sottoscrizioni di eventi di Workfront, vedere [Domande frequenti - Sottoscrizioni eventi](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Per ulteriori informazioni sui webhook, vedi [Trigger istantanei (webhook) in Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Per ulteriori informazioni sui filtri negli scenari, vedere [Aggiungere un filtro a uno scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
