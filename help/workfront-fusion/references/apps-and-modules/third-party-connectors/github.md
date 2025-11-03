---
title: Moduli GitHub
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano GitHub e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1959'
ht-degree: 0%

---

# [!DNL GitHub] moduli

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!UICONTROL GitHub], nonché collegarlo a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL GitHub], è necessario disporre di un account [!DNL GitHub].

## Connetti [!DNL GitHub] a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account [!DNL GitHub] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub] moduli e relativi campi.

Quando si configurano [!DNL GitHub] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL GitHub], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)

### Trigger

* [[!UICONTROL Osserva commenti]](#watch-comments)
* [[!UICONTROL Forchette di controllo]](#watch-forks)
* [[!UICONTROL Problemi di controllo]](#watch-issues)
* [[!UICONTROL Osserva richieste pull]](#watch-pull-requests)
* [[!UICONTROL Esaminare gli archivi]](#watch-repositories)

#### [!UICONTROL Osserva commenti]

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un nuovo commento o viene modificato un commento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio che desideri monitorare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero problema]</td> 
   <td>Se desideri limitare la ricerca cercando solo i nuovi commenti su un problema specifico, inserisci il numero del problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di problemi restituiti]</td> 
   <td> <p> Impostare il numero massimo di commenti restituiti da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Specificare se si desidera controllare solo i nuovi commenti o i commenti e tutte le modifiche.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Forchette di controllo]

Questo modulo di attivazione avvia uno scenario quando viene creato un nuovo fork.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio da controllare per i fork.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di fork restituiti]</td> 
    <td>Immettere o mappare il numero massimo di fork che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Problemi di controllo]

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un nuovo problema o viene modificato un problema esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Voglio guardare]</td> 
   <td>Seleziona se desideri controllare tutti gli archivi associati a questo account o un solo archivio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Se hai scelto di monitorare i problemi in un solo archivio, seleziona l’archivio che desideri monitorare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di problemi restituiti]</td> 
   <td> <p> Impostare il numero massimo di problemi restituiti da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Seleziona se desideri controllare solo i nuovi problemi, i nuovi problemi e tutte le modifiche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Puoi filtrare i problemi che desideri controllare in base alla modalità di associazione.</p> 
    <ul> 
     <li>[!UICONTROL Tutti i problemi]</li> 
     <li>[!UICONTROL Solo i problemi assegnati a me]</li> 
     <li>[!UICONTROL Solo problemi creati dall'utente]</li> 
     <li>[!UICONTROL Solo problemi che mi menzionano]</li> 
     <li>[!UICONTROL Solo i problemi per i quali sono abbonato agli aggiornamenti]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Seleziona se desideri guardare solo i problemi aperti o solo i problemi chiusi. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette]</td> 
   <td>Per ogni tag che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere il tag. Il modulo verifica la presenza di eventuali problemi con questi tag.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Osserva richieste pull]

Questo modulo si attiva quando viene aggiunta una nuova richiesta di pull o viene modificata una richiesta di pull esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio che desideri monitorare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di richieste pull restituite]</td> 
   <td> <p> Imposta il numero massimo di richieste pull restituite da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Seleziona se desideri controllare le richieste [!UICONTROL only open pull], [!UICONTROL only closed ones] o tutte le richieste pull. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Seleziona se desideri controllare solo le nuove richieste pull, le nuove richieste pull e tutte le modifiche.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Esaminare gli archivi]

Questo modulo di attivazione avvia uno scenario quando viene creato o modificato un archivio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di archivi restituiti]</td> 
   <td> <p> Imposta il numero massimo di archivi restituiti da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Seleziona se desideri controllare i nuovi archivi e tutte le modifiche o solo i nuovi archivi.</td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Aggiungi assegnatari]](#add-assignees)
* [[!UICONTROL Aggiungere etichette a un problema]](#add-labels-to-an-issue)
* [[!UICONTROL Crea un commento]](#create-a-comment)
* [[!UICONTROL Crea un problema]](#create-an-issue)
* [[!UICONTROL Segnala un problema]](#get-an-issue)
* [[!UICONTROL Elenca commenti]](#list-comments)
* [[!UICONTROL Rimuovere un&#39;etichetta da un problema]](#remove-a-label-from-an-issue)
* [[!UICONTROL Rimuovi assegnatari]](#remove-assignees)
* [[!UICONTROL Ricerca di un problema]](#search-for-an-issue)
* [[!UICONTROL Aggiorna un problema]](#update-an-issue)

#### [!UICONTROL Aggiungi assegnatari]

Questo modulo aggiunge gli assegnatari al problema specificato

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio contenente il problema a cui desideri aggiungere gli assegnatari.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL assegnatario]</td> 
   <td>Seleziona le persone da assegnare al problema. Gli assegnatari disponibili includono tutti coloro che dispongono di autorizzazioni di scrittura per il repository e i membri dell'organizzazione con autorizzazioni di lettura per il repository. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Inserisci o mappa il numero del problema a cui desideri aggiungere gli assegnatari. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiungere etichette a un problema]

Questo modulo aggiunge etichette a un problema. Le etichette sono definite a livello di repository e possono essere create solo da utenti con accesso in scrittura al repository.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio contenente il problema a cui desideri aggiungere le etichette.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette]</td> 
   <td>Seleziona le etichette da aggiungere al problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Inserisci o mappa il numero del problema a cui desideri aggiungere le etichette.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un commento]

Questo modulo crea un commento sul problema specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Selezionare l'archivio contenente il problema per il quale si desidera creare un commento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Inserisci o mappa il numero del problema sul quale desideri creare un commento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Inserisci o mappa il contenuto del commento.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un problema]

Questo modulo crea un nuovo problema nell’archivio selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio in cui desideri creare un problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL assegnatario]</td> 
   <td>Seleziona le persone da assegnare al problema. Gli assegnatari disponibili includono tutti coloro che dispongono di autorizzazioni di scrittura per l'archivio e i membri dell'organizzazione con autorizzazioni di lettura per l'archivio. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Seleziona la milestone da associare al nuovo problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette]</td> 
   <td>Seleziona le etichette da applicare al nuovo problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Inserisci o mappa un titolo per il nuovo problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Inserisci o mappa il corpo del problema, ad esempio una descrizione o informazioni aggiuntive</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Segnala un problema]

Questo modulo recupera i dettagli del problema specificato

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio contenente il problema di cui desideri recuperare i dettagli.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Inserisci o mappa il numero del problema di cui desideri recuperare i dettagli. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca commenti]

In questo modulo sono elencati tutti i commenti relativi al problema specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio contenente il problema da cui desideri elencare i commenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Inserisci o mappa il numero del problema dal quale desideri elencare i commenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da]</td> 
   <td>Il modulo restituirà i commenti creati dopo tale data. Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di commenti restituiti]</td> 
   <td> <p> Impostare il numero massimo di commenti restituiti da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rimuovere un&#39;etichetta da un problema]

Questo modulo rimuove una singola etichetta da un problema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Selezionare l'archivio contenente il problema da cui si desidera rimuovere un'etichetta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette]</td> 
   <td>Seleziona l’etichetta da rimuovere dal problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Immettere o mappare il numero del problema da cui si desidera rimuovere un'etichetta.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rimuovi assegnatari]

Questo modulo rimuove gli assegnatari dal problema specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Selezionare l'archivio contenente il problema da cui si desidera rimuovere gli assegnatari.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL assegnatario]</td> 
   <td>Seleziona le persone da rimuovere dal problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Immettere o mappare il numero del problema da cui si desidera rimuovere gli assegnatari. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ricerca di un problema]

Questo modulo cerca i problemi che corrispondono ai criteri di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di problemi restituiti]</td> 
   <td> <p> Impostare il numero massimo di problemi restituiti da Workfront Fusion durante un ciclo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Selezionare la modalità di ordinamento dei risultati della ricerca.</p> 
    <ul> 
     <li> <p>[!UICONTROL Corrispondenza migliore] </p> </li> 
     <li>[!UICONTROL Date created]</li> 
     <li>[!UICONTROL Date updated]</li> 
     <li>[!UICONTROL Numero di commenti]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina direzione]</td> 
   <td> <p>Seleziona crescente o decrescente. </p> <p>Per le date, selezionando <strong>[!UICONTROL discendente]</strong> verrà restituita prima la data più recente. </p> <p>Per [!UICONTROL numero di commenti], selezionando <strong>[!UICONTROL discendente]</strong> verrà restituito il problema con il numero più alto di commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Immettere o mappare la query di ricerca. Per una descrizione dettagliata delle opzioni di ricerca, vedere <a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests">Ricerca di problemi e richieste pull</a> nel sito della Guida di [!DNL GitHub].</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un problema]

Questo modulo aggiorna un problema [!DNL GitHub] esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL GitHub] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Archivio [!UICONTROL]</td> 
   <td>Seleziona l’archivio in cui desideri aggiornare un problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL assegnatario]</td> 
   <td>Seleziona le persone da assegnare al problema. Gli assegnatari disponibili includono tutti coloro che dispongono di autorizzazioni di scrittura per il repository e i membri dell'organizzazione con autorizzazioni di lettura per il repository. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Seleziona l’attività cardine da associare al problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette]</td> 
   <td>Seleziona le etichette da applicare al problema. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Immetti o mappa il numero del problema da aggiornare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Seleziona lo stato in cui desideri aggiornare il problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Inserisci o mappa un nuovo titolo per il problema.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Immettere o mappare un nuovo corpo per il problema, ad esempio una descrizione o informazioni aggiuntive</td> 
  </tr> 
 </tbody> 
</table>
