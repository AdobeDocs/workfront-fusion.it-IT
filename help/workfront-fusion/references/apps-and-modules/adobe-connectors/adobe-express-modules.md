---
title: Moduli Adobe Express
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Express.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 17%

---

# Moduli Adobe Express

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Express e collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Prima di poter utilizzare il connettore Adobe Express, è necessario assicurarsi che siano soddisfatti i seguenti prerequisiti:

* Devi disporre di un account Adobe Express attivo.

## Creare una connessione ad Adobe Express

Per creare una connessione per i moduli Adobe Express:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">ID client</td>
        <td>Immetti l'ID client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segreto client</td>
        <td>Immetti il segreto client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## Moduli Adobe Express e relativi campi

Quando configuri i moduli di Adobe Express, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di Adobe Express, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

#### Esportare una rappresentazione

Questo modulo esporta un documento in formato JPG o PNG. Può fornire URL prefirmati per le rappresentazioni delle pagine, validi per quattro ore.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Express, vedere <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Creare una connessione ad Adobe Express</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selezionare il documento per il quale si desidera esportare una rappresentazione.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Numeri di pagina</td> 
   <td>Immettere o mappare i numeri di pagina che si desidera includere nella rappresentazione. Una stringa di numeri di pagina separati da virgole per cui viene effettuata la richiesta di rendering. Ad esempio, "1,2,3". È inoltre possibile specificare gli intervalli di pagine. Ad esempio, "1-3" include le pagine 1, 2 e 3. Un altro esempio è "1,3-5", che include le pagine 1, 3, 4 e 5. "1-" può essere utilizzato per specificare tutte le pagine, mentre "5-" indica la pagina 5 all'ultima pagina. Se non viene fornita, la prima pagina viene considerata per impostazione predefinita. I numeri di pagina iniziano da 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo di rappresentazione</td> 
   <td>Seleziona il tipo di rappresentazione da esportare: immagine, video o PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">Formato</td> 
   <td>Selezionare il formato di file per la copia trasformata.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tipo di PDF</td> 
   <td>Se si sta esportando un PDF, selezionare se esportare un PDF standard o di stampa.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Dimensione</td> 
   <td>Se state esportando un'immagine o un video, immettete o mappate la dimensione in pixel del lato più lungo. Le proporzioni vengono mantenute. Per le immagini, la dimensione minima supportata è 1 px e la dimensione massima supportata è 8192 px. Se non specificato, viene considerata la dimensione predefinita della pagina.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Scaricare singoli file PDF</td> 
   <td>Se si esporta un PDF, selezionare se le pagine vengono scaricate come file PDF separati. Se è true, ogni pagina viene scaricata come proprio file PDF. Se è false, tutte le pagine vengono combinate in un singolo file PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurazione</td> 
   <td>Se si sta esportando un PDF, selezionare se si desidera che il PDF sia nella configurazione standard o di stampa.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Fase di accessibilità</td> 
   <td>Se si sta esportando un PDF standard, selezionare se includere i tag di accessibilità in PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sanguinamento</td> 
   <td>Se si sta esportando un PDF di stampa, selezionare se includere le impostazioni di smarginatura nell'esportazione</td> 
  </tr>
  <tr> 
   <td role="rowheader">Impostazioni pagina al vivo &gt; Importo</td> 
   <td>Immettere l'importo del margine al vivo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Impostazioni pagina al vivo &gt; Unità</td> 
   <td>Seleziona se la quantità si riferisce a pollici o millimetri.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ritaglio</td> 
   <td>Se si sta esportando un PDF di stampa, selezionare se includere le impostazioni di ritaglio nell'esportazione</td> 
  </tr>
  <tr> 
   <td role="rowheader">Impostazioni ritaglio &gt; Importo</td> 
   <td>Immettere l'importo del margine di ritaglio.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Impostazioni ritaglio &gt; Unità</td> 
   <td>Seleziona se la quantità si riferisce a pollici o millimetri.</td> 
  </tr>
 </tbody> 
</table>

#### Genera varianti

Questo modulo crea una variante di documento in base ai parametri di input forniti. Dopo l&#39;elaborazione, il documento generato viene archiviato temporaneamente e reso disponibile all&#39;utente all&#39;interno di una cartella specifica. Il documento rimane accessibile per 30 giorni, dopo i quali il sistema lo rimuove automaticamente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Express, vedere <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Creare una connessione ad Adobe Express</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selezionare il documento per il quale si desidera generare le varianti.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Numeri di pagina</td> 
   <td>Immettere o mappare i numeri di pagina che si desidera includere nella rappresentazione. Una stringa di numeri di pagina separati da virgole per cui viene effettuata la richiesta di variante. Ad esempio, "1,2,3". È inoltre possibile specificare gli intervalli di pagine. Ad esempio, "1-3" include le pagine 1, 2 e 3. Un altro esempio è "1,3-5", che include le pagine 1, 3, 4 e 5. "1-" può essere utilizzato per specificare tutte le pagine, mentre "5-" indica la pagina 5 all'ultima pagina. Se non viene fornita, la prima pagina viene considerata per impostazione predefinita. I numeri di pagina iniziano da 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Nome documento preferito.</td> 
   <td>Immettere o associare un nome per il nuovo documento. Se non specificate un nome o se il nome è già in uso, verrà generato un nome univoco.</td> 
  </tr>
  <tr> 
   <td role="rowheader">ID progetto</td> 
   <td>Immetti l'ID del progetto in cui verranno memorizzate le varianti.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td>Immettere valori per altri campi. I campi disponibili dipendono dal documento selezionato.</td> 
  </tr>
 </tbody> 
</table>


### Ricerche

#### Recupera documenti con tag

Questo modulo recupera un elenco di documenti con tag, insieme ai metadati pertinenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Express, vedere <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Creare una connessione ad Adobe Express</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Indice iniziale</td> 
   <td>Inserisci o mappa l’indice di inizio dell’impaginazione. Utilizzare questa opzione quando è stato recuperato un altro elenco di risultati e si desidera continuare con l'elenco. L'indice predefinito è 0.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di risultati che il modulo deve restituire per ciascun ciclo di esecuzione.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ordina per</td> 
   <td>Selezionare l'attributo in base al quale ordinare i risultati.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Direzione</td> 
   <td>Seleziona se desideri ordinare i risultati in modo crescente o decrescente.</td> 
  </tr>
 </tbody> 
</table>

#### Recupera dettagli documento

Questo modulo recupera i dettagli delle pagine e degli elementi con tag all’interno di un documento specificato. Restituisce un elenco impaginato delle pagine del documento e dei metadati relativi a ciascuna pagina. Se il documento contiene elementi con tag, l’API ne include i rispettivi dettagli, ad esempio dimensioni e posizione. Se nel documento non sono presenti elementi con tag, verrà restituito un array vuoto. La risposta include informazioni sull’impaginazione che consentono agli utenti di navigare nelle pagine del documento. È possibile restituire un massimo di 10 pagine in 1 ciclo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Express, vedere <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Creare una connessione ad Adobe Express</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Documento</td> 
   <td>Selezionare il documento per il quale si desidera restituire le pagine e i dettagli.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Pagina iniziale</td> 
   <td>Immetti o mappa il numero della prima pagina da cui verranno recuperati i dettagli.</td>

#### Recuperare lo stato di un processo

Questo modulo recupera lo stato di un processo in base al relativo ID. A seconda del tipo di processo, la risposta può includere dettagli specifici per il processo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Express, vedere <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Creare una connessione ad Adobe Express</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID processo</td> 
   <td>Immetti o mappa l’ID del processo per il quale desideri recuperare i dettagli.</td> 
  </tr>

