---
title: Usa pacchetti di funzioni personalizzati
description: Durante la mappatura degli elementi, puoi utilizzare funzioni per la creazione di formule semplici o complesse.
author: Becky
feature: Workfront Fusion
source-git-commit: ac7190293e7c4b3bb9bfd48d73cd59ad687690e6
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 5%

---


# Utilizzare pacchetti di funzioni personalizzati

I pacchetti consentono di creare ed eseguire una logica personalizzata all’interno di Adobe Workfront Fusion, senza uscire dall’interfaccia di Fusion. Quando i moduli standard non eseguono esattamente le operazioni necessarie, è possibile utilizzare una funzione per trasformare i dati, eseguire un calcolo, chiamare un servizio esterno o racchiudere una routine che si desidera riutilizzare. Puoi testarlo, renderlo live e utilizzarlo dai tuoi scenari.

Le funzioni complesse possono richiedere risorse come variabili e dipendenze come le librerie. Per queste funzioni, puoi creare un pacchetto che include la funzione e le relative risorse.

Un pacchetto può includere:

* **Funzioni**: logica che viene eseguita durante l&#39;esecuzione di uno scenario.
* **Variabili**: valori riutilizzabili, ad esempio un URL di base o una chiave API, utilizzati dalla funzione nel pacchetto.
* **Dipendenze**: fuori dalle librerie su cui le tue funzioni possono fare affidamento.
* **Cronologia**: versioni precedenti di ogni funzione, salvate automaticamente, a cui è possibile fare riferimento.


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
   <p><ul><li>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li><li>Per utilizzare le funzioni personalizzate è necessario disporre di una licenza Adobe App Builder.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Configurare la connessione all’ambiente di runtime

>[!NOTE]
>
>Questa è una configurazione unica.

La prima volta che il team utilizza questa funzione, devi impostare l’ambiente che esegue le funzioni. Questa operazione viene eseguita solo una volta per team.

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.

   Se l&#39;ambiente non è stato configurato, viene visualizzata la schermata **Ambiente runtime non configurato**.

1. Fare clic su **Inizializza runtime**.

1. Per immettere un nome diverso da quello predefinito, digitare il nome nel campo **Nome connessione**.

1. Seleziona il progetto Adobe App Builder a cui apparterrà questo pacchetto:

   * Per selezionare un progetto esistente, inizia a digitare il nome del progetto e, quando viene visualizzato, selezionalo.
   * Per creare un nuovo progetto, immetti un nome che non esiste già e fai clic su **Crea nuovo**.
   * Se si lascia vuoto questo campo, Fusion utilizza un progetto predefinito.

1. Seleziona **Continua**.

   Fusion completa la configurazione e si è pronti a creare i pacchetti.

   L’ambiente viene visualizzato come scheda di connessione nella parte superiore della pagina.

   ![Ambiente come scheda connessione](assets/package-environment-as-connection.png)

1. (Condizionale) Per aggiungere un ambiente aggiuntivo, fai clic sull’icona Più e segui le istruzioni riportate in questa sezione.

1. (Condizionale) Per rimuovere un ambiente esistente, passa il puntatore del mouse sulla scheda della connessione dell&#39;ambiente e fai clic su **X** quando viene visualizzato.

   >[!WARNING]
   >
   >La rimozione di una connessione disconnette Fusion da tale ambiente. I pacchetti in esso contenuti non sono più disponibili in Fusion tramite tale connessione.

## Creare e aprire un pacchetto

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.

1. Selezionare la scheda della connessione in cui si desidera lavorare.

1. Fare clic su **Crea pacchetto**.

1. Immetti un nome e seleziona **Crea**.

   Il pacchetto si apre automaticamente.

1. Per riaprire un pacchetto in seguito, selezionarlo dall&#39;elenco Pacchetti e selezionare **Visualizza**.
1. Per eliminare un pacchetto, selezionarlo dall&#39;elenco Pacchetti e scegliere **Elimina**.

   >[!WARNING]
   >
   >L’eliminazione di un pacchetto lo rimuove definitivamente e tutto ciò che contiene.

## Gestire un pacchetto

Un pacchetto aperto è organizzato in quattro aree:

* **Funzioni**: crea, verifica e pubblica la funzione.
* **Variabili**: configurare le variabili per la funzione.
* **Dipendenze**: installa le dipendenze, ad esempio le librerie esterne, per questa funzione.
* **Cronologia**: visualizza le versioni precedenti di ciascuna funzione.

Oltre a queste quattro aree, un misuratore di spazio di archiviazione nella parte superiore mostra la quantità di spazio utilizzato. Ogni pacchetto ha un limite di dimensione totale di **21 MB**. Ciò include funzioni, variabili e dipendenze, incluse le versioni salvate.

Se lo spazio è esaurito, è consigliabile rimuovere le dipendenze, le variabili o le versioni precedenti inutilizzate per liberarne alcune.

Per tornare all&#39;elenco dei pacchetti, selezionare la freccia indietro accanto al nome del pacchetto.

<!--Create toc here-->

### Funzioni

Nell&#39;area **Funzioni** viene visualizzato un elenco di funzioni nel pacchetto, inclusi il nome, lo stato, le dimensioni e il numero di input previsti.

Per filtrare l&#39;elenco delle funzioni:

1. Filtra per stato facendo clic su **Tutti**, **Bozze** o **Pubblicato**.
1. Utilizza la barra di ricerca per cercare funzioni specifiche.

#### Stato funzione

Una funzione può avere lo stato bozza o pubblicato.

* **Bozza**: le funzioni in stato Bozza sono in esecuzione. Puoi modificare e testare liberamente senza influire sui dati live.
* **Pubblicato**: le versioni pubblicate sono live. Gli scenari eseguono versioni pubblicate delle funzioni.

L&#39;utilizzo delle bozze consente di apportare modifiche in modo sicuro. Potete perfezionare una bozza, testarla e quindi pubblicarla quando siete soddisfatti.

| Stato | Che cosa significa |
|---|---|
| **Pubblicato** | Esiste già una versione live. |
| **Bozza** | La funzione è ancora in corso oppure una funzione live presenta modifiche non ancora pubblicate. |

#### Creare o modificare una funzione nell&#39;area Pacchetti

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nell&#39;area **Funzioni**, selezionare **Crea funzione**.

   Oppure

   Fai clic sulla casella di controllo accanto a una funzione esistente e seleziona **Modifica** nella barra delle azioni nella parte inferiore della pagina.

1. (Condizionale) Se si sta creando una nuova funzione, nel campo **Nuova funzione** immettere un nome per la funzione.

1. (Facoltativo e condizionale) Per rinominare una funzione esistente, fare clic sull&#39;icona Modifica accanto al nome della funzione e immettere il nuovo nome.

1. Nella scheda **Codice** immettere la logica della funzione.

   Quando crei la funzione, tieni presente quanto segue:

   * Le funzioni devono essere scritte in JavaScript.
   * Puoi leggere gli input che definisci, riutilizzare le variabili e richiamare le altre funzioni.
   * Durante la digitazione vengono visualizzati i suggerimenti.

1. Per pulire la formattazione della funzione, fare clic su **Scolora**.

1. (Facoltativo) Nella scheda **Parametri**, definisci gli input previsti dalla funzione.

   Per informazioni sugli input, vedere [Definire gli input](#define-inputs) in questo articolo.

1. Nella scheda **Test**, verifica la funzione.

   Per istruzioni, vedere [Verificare una funzione](#test-a-function) in questo articolo.

1. Per salvare questa funzione come bozza, fare clic su **Salva come bozza**.

   Oppure

   Per pubblicare la funzione, fai clic su **Pubblica**.

   >[!NOTE]
   >
   >La pubblicazione di una funzione cancella la cronologia delle versioni. La versione pubblicata diventa il punto di partenza corrente e le versioni precedenti delle bozze non vengono più mantenute.

##### Definire gli input

È possibile utilizzare la scheda **Parametri** per descrivere le informazioni necessarie alla funzione ogni volta che viene eseguita.

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nell&#39;area **Funzioni**, selezionare **Crea funzione**.

   Oppure

   Fai clic sulla casella di controllo accanto a una funzione esistente e seleziona **Modifica** nella barra delle azioni nella parte inferiore della pagina.

1. Fare clic sulla scheda **Parametri**.

1. Per ogni parametro che si desidera aggiungere, fare clic su **Aggiungi parametro** e configurare quanto segue:

* **Nome**: nome dell&#39;input
* **Etichetta**: nome descrittivo visualizzato durante il test della funzione
* **Tipo**: tipo di dati, ad esempio testo, numero, vero/falso o oggetto strutturato.
* **Obbligatorio**: è necessario specificare un valore.

Questi input diventano i campi compilati durante il test e i valori trasmessi dallo scenario quando esegue la funzione.

##### Testare una funzione

È consigliabile testare una funzione prima di pubblicarla.

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nell&#39;area **Funzioni**, selezionare **Crea funzione**.

   Oppure

   Fai clic sulla casella di controllo accanto a una funzione esistente e seleziona **Modifica** nella barra delle azioni nella parte inferiore della pagina.

1. Fare clic sulla scheda **Test**.

1. Immettere un valore per ogni input.

1. Esegui la funzione:

   * Seleziona **Bozza di prova** per provare la versione work-in-progress.
   * Seleziona **Esegui pubblicato** per eseguire la versione live.

1. Rivedi il risultato, specificando se ha avuto esito positivo, il tempo impiegato e l’output restituito.

>[!NOTE]
>
>**Esegui pubblicazione** è disponibile solo dopo la pubblicazione di una funzione.

#### Apportare modifiche a una funzione live

Dopo la pubblicazione di una funzione, il pulsante **Pubblica** diventa un menu:

* **Ripubblica** — invia le ultime modifiche alla bozza alla versione live.
* **Annulla pubblicazione** — elimina la funzione dal servizio. Il tuo lavoro è conservato come bozza, in modo da poterci tornare.

#### Eliminare una funzione

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Fai clic sulla casella di controllo accanto a una funzione esistente e seleziona **Elimina** nella barra delle azioni nella parte inferiore della pagina.

>[!WARNING]
>
>L’eliminazione di una funzione la rimuove completamente, insieme alla relativa cronologia. Qualsiasi scenario o funzione che la utilizza smetterà di funzionare.

## Variabili

Le variabili sono valori riutilizzabili che le funzioni possono utilizzare, ad esempio un URL di base, un ID account o una chiave API. Se si memorizzano queste variabili, si imposta un valore una volta e lo si aggiorna in un&#39;unica posizione, anziché aggiornarlo in molte funzioni.

### Creare o modificare una variabile

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nella scheda **Variabili** selezionare **Nuova variabile**.

   Oppure


   Fai clic sull&#39;icona **Modifica** accanto alla variabile da modificare.

1. Compila i dettagli:

   * **Chiave**: immettere il nome utilizzato dalle funzioni per fare riferimento al valore.

   Per rinominare questa variabile, modifica il valore Key.
   * **Valore**: immettere il valore da archiviare.
   * **Tipo**: selezionare se il tipo di valore è testo, un numero, booleano (true/false) o un oggetto strutturato.
   * **Descrizione**: inserisci una nota facoltativa per ricordarti a cosa serve.
   * **Pubblico**: attivare questa opzione se si desidera utilizzare la variabile nella finestra di progettazione degli scenari. Se è disattivata, la variabile è disponibile solo all’interno delle funzioni del pacchetto.
   * **Segreto**: attivare questa opzione per nascondere i valori sensibili, ad esempio le chiavi. Il valore è nascosto nell’elenco delle variabili ed è anche bonificato in modo da non essere esposto nella finestra di progettazione dello scenario. Le funzioni continuano a ricevere il valore reale durante l&#39;esecuzione.

1. Seleziona **Crea variabile** o **Salva modifiche**.

### Eliminare una variabile

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nella scheda **Variabili** fare clic sull&#39;icona **Elimina** accanto alla variabile che si desidera eliminare.

>[!WARNING]
>
>Le funzioni che utilizzano una variabile eliminata cesseranno di funzionare.

## Dipendenze

Alcune funzioni richiedono librerie aggiuntive per eseguire il proprio lavoro. Nella scheda **Dipendenze** è possibile aggiungere e gestire tali librerie.

### Aggiungere librerie

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nella scheda **Dipendenze** immettere uno o più nomi di libreria separati da virgole. È possibile richiedere una versione specifica aggiungendola dopo il nome, ad esempio `axios, lodash@4.17.21`.

1. Fare clic su **Installa**.

### Rimuovere una libreria

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nella scheda **Dipendenze**, fai clic sull&#39;icona **Elimina** accanto alla libreria da rimuovere.

>[!WARNING]
>
>Le funzioni che si basano su una libreria rimossa potrebbero non funzionare più.

## Cronologia

Ogni volta che salvate una bozza di una funzione, Fusion ne conserva una copia. La scheda **Cronologia** consente di visualizzare e ripristinare le versioni precedenti.

1. Fai clic sulla scheda **Pacchetti** ![Icona Pacchetti](assets/packages-icon.png) nel pannello di navigazione a sinistra.
1. Nella scheda **Cronologia**, seleziona una funzione a sinistra per visualizzare le versioni salvate, prima le più recenti.
1. Seleziona una versione per visualizzare esattamente ciò che conteneva in quel momento.
1. Per ripristinare una versione, fare clic su **Ripristina come bozza**.

   La versione viene ripristinata come nuova bozza, in modo da poterla esaminare e testare prima di pubblicarla. La versione live rimane attiva fino alla pubblicazione.
1. Per eliminare una versione, selezionarla, fare clic su **Elimina versione** e confermare.

>[!NOTE]
>
>* La pubblicazione di una funzione ne cancella la cronologia. La cronologia tiene traccia delle modifiche apportate durante l’elaborazione di una bozza, fino alla pubblicazione.
>* L&#39;eliminazione di una versione non può essere annullata.



## Utilizzare un pacchetto in uno scenario

Lo scopo di creare funzioni e variabili è di metterle in funzione nei tuoi scenari. Per utilizzare funzioni e variabili, utilizzare il connettore **Adobe App Builder**.

* **Usa funzione dal pacchetto**: questo modulo esegue una delle tue funzioni come passaggio in uno scenario. Scegli il pacchetto e la funzione, compila gli input definiti e il risultato della funzione viene trasmesso ai moduli che seguono.
* **Usa variabile da pacchetto**: questo modulo inserisce una delle variabili del pacchetto in uno scenario, in modo da poterne mappare il valore in altri moduli.

Per informazioni e istruzioni, consulta [Moduli Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

<!--

To add one:

1. In the scenario designer, add a module and choose the **Adobe App Builder** connector.

1. Select **Use function from package** or **Use variable from package**.

1. Choose the package and the function or variable you want, then map the inputs or value as needed.

>[!NOTE]
>
>Publish a function before using it in a scenario, and turn on **Public** for any variable you want to use there.

-->





