---
title: CSV
description: I moduli CSV di Adobe Workfront Fusion consentono di creare file CSV e analizzare il testo CSV da un valore di testo ricevuto o da un file.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---

# CSV

I moduli [!DNL Adobe Workfront Fusion] [!UICONTROL CSV] consentono di creare file CSV e analizzare il testo CSV da un valore di testo ricevuto o da un file.

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisito licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione lavoro, [!UICONTROL [!DNL Workfront Fusion] per automazione lavoro</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL Create CSV]

L&#39;aggregatore [!UICONTROL Create CSV] consente di creare un testo CSV dai valori di testo ricevuti.

Per ulteriori informazioni sugli aggregatori, vedere [Modulo aggregatore](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Seleziona il modulo utilizzato per aggregare i campi necessari.</td>
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

Per ulteriori informazioni sugli aggregatori, vedere [Modulo Aggregator in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Seleziona il modulo app che utilizzi per aggregare i campi necessari.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Seleziona la struttura dati per aggregare i campi nel modo desiderato. Dopo aver definito la struttura dati, puoi mappare gli elementi ai campi corrispondenti.</p> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Strutture dati in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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


<p>Supponiamo che tu voglia esportare i tuoi contatti Google in un file CSV con due colonne "Nome completo" e "E-mail". Il bundle di output del modulo [!UICONTROL Google Contacts] &gt;[!UICONTROL Get contacts from a group] presenta la seguente struttura. Gli indirizzi e-mail sono archiviati all'interno dell'elemento <code>[!UICONTROL Emails[]]</code>, che è un array di raccolte, ciascuna delle quali contiene due elementi: <code>Label</code> e <code>Email</code>.</p>
<p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png" style="width: 350;height: 546;"> </p>
<p>Se utilizzi il semplice modulo [!DNL Create CSV], ti verrà offerto un elenco di caselle di controllo corrispondenti agli elementi di primo livello di un bundle. Se si tenta di contrassegnare <code>Full name</code> e <code>Emails</code> elementi, il modulo [!UICONTROL Create CSV] produce il seguente output, che probabilmente non è quello desiderato:</p>
<p>"emails","fullName"</p>
<p>"[oggetto oggetto]","Shon Winer"</p>
<p>"[oggetto]","Lizeth Fulmore"</p>
<p>"[oggetto]","Hilario Gullatt"</p>
<p>"[oggetto]","Abby Eisenbarth"</p>
<p>Poiché l'elemento <code>Full Name</code> è di tipo semplice Testo, l'esportazione è corretta. Tuttavia, l'elemento <code>Emails</code>, che è di tipo complesso Array di raccolte, viene esportato come [oggetto Object], ovvero nel modo in cui le raccolte e le matrici vengono trasformate in testo per impostazione predefinita. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipi di dati degli elementi in Adobe Workfront Fusion</a>.</p>
<p>Per esportare il contenuto dell'elemento <code>Email </code> della prima raccolta dell'array <code>Emails[]</code>, è necessario utilizzare il modulo [!UICONTROL Create CSV (advanced)]. Il modulo ti consente di definire singole colonne del file CSV e di mappare ad esse gli elementi, inclusi quelli nidificati.</p>
<ol>
<li value="1">Inserire il modulo [!UICONTROL Create CSV (advanced)] in uno scenario e aprirne la configurazione.</li>
<li value="2">Fare clic sul pulsante <strong>[!UICONTROL Add]</strong> accanto al campo [!UICONTROL Data structure] per creare una nuova struttura dati.</li>
<li value="3"> <p>Scrivere un nome per la struttura dati e fare clic sul pulsante <strong>[!UICONTROL Add item]</strong> per aggiungere le singole colonne. Se desideri esportare due colonne: "Nome completo" e "E-mail", la struttura dati risultante sarà simile alla seguente:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png" style="width: 350;height: 524;"> </p> </li>
<li value="4"> <p>Dopo aver definito correttamente la struttura dati, i campi corrispondenti a ogni singola colonna devono essere visualizzati nella configurazione del modulo [!UICONTROL Create CSV (advanced)] per consentire la mappatura degli elementi. Prendere il primo elemento dall'array <code>[!UICONTROL Emails[]]</code> e mappare il relativo elemento <code>Email </code> al campo/colonna E-mail:</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png" style="width: 350;height: 308;"> </p> </li>
<li value="5"> <p>Esegui lo scenario. Poiché l'elemento <code>Emails[1]: Email</code> mappato alla colonna "E-mail" è di tipo semplice Testo, ora viene esportato correttamente:</p> <p>"Nome completo","E-mail"</p> <p>"Shon Winer","Shon@Winer.com"</p> <p>"Lizeth Fulmore","Lizeth@Fulmore.com"</p> <p>"Hilario Gullatt","Hilario@Gullatt.com"</p> <p>"Abby Eisenbarth","Abby@Eisenbarth.com"</p> </li>
</ol>
</div>

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
   <td>Immetti o mappa il file CSV da analizzare.<p>Nota: <p>Se i dati sono in formato binario (in genere da un file), è necessario utilizzare la funzione `toString()` per convertire i dati binari in [!UICONTROL String]:</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png" style="width: 350;height: 123;"></p></p></td> 
  </tr> 
 </tbody> 
</table>
