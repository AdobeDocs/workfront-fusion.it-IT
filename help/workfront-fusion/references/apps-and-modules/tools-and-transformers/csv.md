---
title: CSV
description: I moduli CSV di Adobe Workfront Fusion consentono di creare file CSV e analizzare il testo CSV da un valore di testo ricevuto o da un file.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 5971b2210eaac8f8a75fd7a4aac5a9f7954d27ef
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# CSV

I moduli [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] consentono di creare file CSV e analizzare il testo CSV da un valore di testo ricevuto o da un file.

Poiché si tratta di un trasformatore, questi moduli non richiedono una connessione.

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
   <p>Nessun requisito di licenza per Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL Create CSV]

L&#39;aggregatore [!UICONTROL Create CSV] consente di creare un testo CSV dai valori di testo ricevuti.

Per ulteriori informazioni sugli aggregatori, vedere [Modulo aggregatore](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Seleziona il modulo che restituisce i campi che desideri utilizzare per creare il file CSV.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Selezionare i campi da aggregare dall'elenco dei campi disponibili.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Seleziona questa opzione per includere le intestazioni nel risultato.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Immettere il filtro per raggruppare i risultati. Ad esempio, inserisci una data.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Selezionare questa opzione per interrompere lo scenario quando non sono presenti risultati.</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

L&#39;aggregatore [!UICONTROL Create CSV (advanced)] consente di creare un testo CSV dai valori di testo ricevuti. Utilizza una struttura di dati che definisce le colonne CSV nel file CSV risultante. Una volta definite, le colonne vengono visualizzate come campi nella configurazione del modulo CSV e possono essere mappate a un modulo successivo nello scenario.

Per ulteriori informazioni sugli aggregatori, vedere [Modulo aggregatore](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Seleziona il modulo che restituisce i campi che desideri utilizzare per creare il file CSV.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Seleziona la struttura dati per aggregare i campi nel modo desiderato. Dopo aver definito la struttura dati, puoi mappare gli elementi ai campi corrispondenti.</p> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Strutture dati</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Seleziona questa opzione per includere le intestazioni nel risultato. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Immettere il filtro per raggruppare i risultati. Ad esempio, inserisci una data. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Selezionare questa opzione per interrompere lo scenario quando non sono presenti risultati. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**Esempio**:

In questo esempio viene illustrato come esportare i contatti di Google in un file CSV con due colonne denominate &quot;Nome completo&quot; e &quot;E-mail&quot;. Il bundle di output del modulo [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group] presenta la seguente struttura. Gli indirizzi e-mail sono archiviati in <code>[!UICONTROL Emails[]]</code> item, un array di raccolte, ciascuna delle quali contiene due elementi: <code>Label</code> e <code>E-mail</code>.
![Trasformazione](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

Il semplice modulo [!DNL Create CSV] offre un elenco di caselle di controllo corrispondenti agli elementi di primo livello di un bundle. Se si tenta di selezionare <code>Nome completo</code> e <code> e-mail</code> elementi, il modulo [!UICONTROL Create CSV] produce il seguente output, che potrebbe non essere quello desiderato:

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Perché l&#39;elemento <code>Nome completo</code> è di tipo semplice Testo, viene esportato come previsto. L&#39;elemento <code>E-mail</code>, di tipo complesso Array of Collections, viene esportato come [oggetto], ovvero nel modo in cui le raccolte e gli array vengono trasformati in testo per impostazione predefinita.

Per ulteriori informazioni, vedere [Tipi di dati elemento](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


Per esportare il contenuto dell&#39;e-mail <code> </code>elemento della prima raccolta di <code>E-mail[]</code> al suo posto, è necessario utilizzare il modulo [!UICONTROL Create CSV (advanced)]. Questo modulo ti consente di definire singole colonne del file CSV e di mappare ad esse gli elementi, inclusi quelli nidificati.

1. Inserire il modulo [!UICONTROL Create CSV (advanced)] in uno scenario.
1. Fare clic sul pulsante <strong>[!UICONTROL Add]</strong> accanto al campo [!UICONTROL Data structure] per creare una nuova struttura dati.
1. Immettere un nome per la struttura dati e fare clic su <strong>[!UICONTROL Add item]</strong> per aggiungere le singole colonne. Per esportare due colonne: &quot;Nome completo&quot; e &quot;E-mail&quot;, la struttura dati risultante sarà simile alla seguente:

   ![Output contatti Google](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Dopo aver definito la struttura dati, i campi corrispondenti a ogni singola colonna vengono visualizzati nella configurazione del modulo [!UICONTROL Create CSV (advanced)] in modo da poter mappare gli elementi. Prendi il primo elemento da <code>[!UICONTROL Emails[]]</code> array e mappa il relativo elemento <code>E-mail </code>al campo/colonna E-mail:

   ![Crea modulo CSV avanzato](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Esegui lo scenario. Perché l&#39;elemento <code>E-mail[1]: E-mail</code> mappato alla colonna &quot;E-mail&quot; è di tipo semplice Testo, viene esportato correttamente.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL Parse CSV]

Il trasformatore [!UICONTROL Parse CSV] consente di analizzare il testo CSV da un valore di testo ricevuto o da un file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Specifica il numero di colonne nel file CSV.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Seleziona questa opzione se la prima riga del testo CSV contiene intestazioni.</p> <p>Nota: il modulo non utilizza queste intestazioni per etichettare le colonne nell’output. Questo campo assicura, invece, che le intestazioni non vengano incluse nei dati di output.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Seleziona il delimitatore per il file CSV. Il delimitatore è il carattere di testo che indica il limite tra valori o campi separati.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>Se si seleziona [!UICONTROL Other], immettere il carattere di delimitazione utilizzato dal file CSV per separare i valori. È necessario immettere esattamente un carattere.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Abilita questa opzione per mantenere le virgolette.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Immetti o mappa il file CSV da analizzare.<p>Nota: <p>Se i dati sono in formato binario (in genere da un file), è necessario utilizzare la funzione `toString()` per convertire i dati binari in [!UICONTROL String]:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
