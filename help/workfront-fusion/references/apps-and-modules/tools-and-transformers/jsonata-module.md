---
title: Moduli JSONata
description: Il connettore JSONata di Adobe Workfront Fusion fornisce un modulo per elaborare i dati in formato JSON in modo che Adobe Workfront Fusion possa lavorare ulteriormente con il contenuto dei dati.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: da3bf98f8254228598372fed8c06d6318718721f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# [!UICONTROL Moduli JSONata]

Il connettore [!DNL Adobe Workfront Fusion] [!UICONTROL JSONata] consente di eseguire query sugli oggetti JSON. Questo modulo non richiede una connessione.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza</td> 
   <td> <p>Nuovo: [!UICONTROL Standard]</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront]: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>Il piano [!UICONTROL Ultimate] [!DNL Workfront]: [!DNL Workfront Fusion] è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
