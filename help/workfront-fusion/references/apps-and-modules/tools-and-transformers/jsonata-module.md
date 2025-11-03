---
title: Moduli JSONata
description: Il connettore JSONata di Adobe Workfront Fusion fornisce un modulo per elaborare i dati in formato JSON in modo che Adobe Workfront Fusion possa lavorare ulteriormente con il contenuto dei dati.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL Moduli JSONata]

Il connettore [!UICONTROL JSONata] di Adobe Workfront Fusion consente di eseguire query sugli oggetti JSON. Questo modulo non richiede una connessione.

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

+++



## Moduli JSONata e relativi campi

### Valuta

Questo modulo di azione esegue una query su un oggetto JSON e restituisce un array.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expression]</td> 
   <td>Immetti l’espressione da utilizzare per valutare l’oggetto JSON. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data] </td> 
   <td> Inserisci l’oggetto JSON da valutare.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringivy output] </td> 
   <td> Abilita questa opzione per convertire l’output in una stringa.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Esempio**:

L’obiettivo è quello di restituire un array di nomi dal seguente oggetto JSON:

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. Nel campo espressione immettere `people.name`.
1. Nel campo dati, immetti l’oggetto JSON.

Il modulo restituisce un array di nomi estratti dall’oggetto JSON.

>[!ENDSHADEBOX]



### MCP JSONata

Questo modulo di azione genera espressioni JSONata analizzando gli schemi di input e output specificati. Vengono forniti gli schemi utilizzati da MCP (Model Context Protocol) per generare l&#39;espressione che trasforma l&#39;input nell&#39;output.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selezionare la connessione da utilizzare per connettersi al modello di lingua di grandi dimensioni (LLM) che si desidera utilizzare per questo modulo.</p> <p>Attualmente, è supportata solo la chiave API antropica.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schema di input]</td> 
   <td> <p>Immetti o mappa lo schema di input da utilizzare per questa espressione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schema di output]</td> 
   <td> <p>Immetti o mappa lo schema di output da utilizzare per questa espressione.</p> </td> 
  </tr> 
 </tbody> 
</table>
