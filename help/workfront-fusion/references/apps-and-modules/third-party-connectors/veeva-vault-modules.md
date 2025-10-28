---
title: Moduli Veeva Vault
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Veeva Vault e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
source-git-commit: 4f5a4cf8691e5bb47eec6f6b2842369c5c6fbad8
workflow-type: tm+mt
source-wordcount: '1516'
ht-degree: 3%

---

# Moduli Veeva Vault

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Veeva Vault e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Per utilizzare i moduli Veeva Vault, è necessario disporre di un account Veeva Vault.

## Moduli Veeva Vault e relativi campi

Quando si configurano i moduli Veeva Vault, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di Veeva Vault, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Documento

* [Creare un singolo documento](#create-a-single-document)
* [Creazione di più documenti](#create-multiple-documents)
* [Eliminare un singolo documento](#delete-a-single-document)
* [Esporta documenti](#export-documents)
* [Ottieni un singolo documento](#get-a-single-document)
* [Avvia azione utente](#initiate-user-action)
* [Elencare documenti](#list-documents)
* [Recuperare i risultati di esportazione del documento](#retrieve-document-export-results)
* [Aggiornare più documenti](#update-multiple-documents)
* [Aggiornare un singolo documento](#update-a-single-document)

#### Creare un singolo documento

Questo modulo crea un singolo documento, raccoglitore o modello.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera creare un documento, un raccoglitore o un modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Seleziona campi</p> </td> 
   <td> <p>Selezionare i campi per i quali si desidera immettere i dati, quindi immettere i dati in tali campi.</td> 
  </tr> 
 </tbody> 
</table>

#### Creazione di più documenti

Questo modulo crea più documenti o modelli utilizzando un file CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera creare modelli o documenti</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dati dei file</p> </td> 
   <td> <p>Mappa il file CSV che verrà utilizzato per creare i documenti.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un singolo documento

Questo modulo elimina un singolo documento, raccoglitore o modello.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera eliminare un documento, un raccoglitore o un modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID documento / ID raccoglitore / Nome modello</p> </td> 
   <td> <p>Selezionare i campi da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Esporta documenti

Questo modulo esporta i documenti specificati, incluse le origini, le rappresentazioni e il testo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera eliminare un documento, un raccoglitore o un modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Origine</p> </td> 
   <td> <p>Abilita questa opzione per includere i file di origine nell’esportazione.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Rappresentazioni</p> </td> 
   <td> <p>Abilita questa opzione per includere i file delle rappresentazioni nell’esportazione.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Tutte le versioni</p> </td> 
   <td> <p>Abilitare questa opzione per includere nell'esportazione tutte le versioni dei file di documento.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Testo</p> </td> 
   <td> <p>Abilitare questa opzione per includere il testo del documento di origine nell'esportazione.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni un singolo documento

Questo modulo recupera i metadati per un singolo documento, raccoglitore o modello.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera recuperare i dati per un documento, un raccoglitore o un modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID documento / ID raccoglitore / Nome modello</p> </td> 
   <td> <p>Selezionare i campi per i quali si desidera recuperare i dati.</td> 
  </tr> 
 </tbody> 
</table>

#### Avvia azione utente

Questo modulo avvia azioni su documenti e raccoglitori, ad esempio l&#39;invio di un documento per la revisione o la modifica del relativo stato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Selezionare se si desidera eseguire un'azione su un documento o un raccoglitore.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Documento/Raccoglitore</p> </td> 
   <td> <p>Selezionare il documento o il raccoglitore su cui si desidera eseguire l'azione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versione documento/versione del Raccoglitore</p> </td> 
   <td> <p>Selezionare il documento o il raccoglitore su cui si desidera eseguire l'azione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Azione</p> </td> 
   <td> <p>Selezionare l'azione da eseguire sul documento o sul raccoglitore.</td> 
  </tr> 
 </tbody> 
</table>

#### Elencare documenti

Questo modulo elenca tutti i documenti del tipo selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera elencare documenti, raccoglitori o modelli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### Recuperare i risultati di esportazione del documento

Questo modulo restituisce i risultati di un’esportazione di documenti richiesta in precedenza.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID processo</p> </td> 
   <td> <p>Immetti o mappa l’ID del processo per il quale desideri restituire i risultati. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Aggiornare più documenti

Questo modulo aggiorna più documenti o modelli utilizzando un file CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera creare modelli o documenti</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dati dei file</p> </td> 
   <td> <p>Mappa il file CSV che verrà utilizzato per creare i documenti.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un singolo documento

Questo modulo aggiorna un singolo documento, raccoglitore o modello.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera creare un documento, una versione del documento, un raccoglitore o un modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID/Nome</p> </td> 
   <td> <p>Se si sta aggiornando un modello, immettere un nuovo nome per il modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nome nuovo modello</p> </td> 
   <td> <p>Immettere o mappare l'ID o il nome dell'oggetto da aggiornare.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Seleziona campi</p> </td> 
   <td> <p>Selezionare i campi per i quali si desidera immettere i dati, quindi immettere i dati in tali campi.</td> 
  </tr> 
 </tbody> 
</table>

### Oggetto



#### Elencare oggetti

Questo modulo recupera tutti gli oggetti Vault nel Vault autenticato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Recupera etichette localizzate</p> </td> 
   <td> <p>Selezionate Sì (Yes) per recuperare le stringhe localizzate (tradotte) per i campi dell'oggetto label e label_plural.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [Creare una query VQL](#make-a-vql-query)
* [Leggi registri](#read-logs)

#### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Immettere un percorso relativo a <code>baseurl/api/v</code>.  Esempio: <code>/objects/documents</code>. Non includere <code>baseurl/api/v/</code>, poiché è già incluso.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Metodo</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Intestazioni</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stringa di query</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Creare una query VQL

Questo modulo effettua una query utilizzando Vault Query Language (VQL).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo</p> </td> 
   <td> <p>Specificare se si desidera creare modelli o documenti</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Dati dei file</p> </td> 
   <td> <p>Mappa il file CSV che verrà utilizzato per creare i documenti.</td> 
  </tr> 
 </tbody> 
</table>

#### Leggi registri

Questo modulo restituisce i dati dagli audit trail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Veeva Vault a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tipo di controllo</p> </td> 
   <td> <p>Seleziona il tipo di controllo per il quale desideri recuperare i dati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data di inizio</p> </td> 
   <td> <p>Immetti o mappa la data di inizio per i controlli di audit che desideri recuperare.</p><p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data di fine</p> </td> 
   <td> <p>Immetti o mappa la data di fine per i controlli di audit che desideri recuperare.</p><p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL risultato </p> </td> 
   <td> <p>Seleziona CSV se desideri ottenere l’URL per scaricare un CSV del risultato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>


