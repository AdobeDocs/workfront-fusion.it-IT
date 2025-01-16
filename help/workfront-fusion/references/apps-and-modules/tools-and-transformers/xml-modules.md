---
title: XML
description: L'app XML consente di analizzare un testo in formato XML tramite il modulo XML &gt; Analizza XML e convertirlo in un bundle per rendere i dati disponibili ad altri moduli. È inoltre possibile convertire un bundle in un testo in formato XML tramite il modulo &gt; Crea XML
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 2%

---

# XML

L&#39;app [!UICONTROL XML] consente di analizzare un testo in formato XML tramite il modulo [!UICONTROL XML] > [!UICONTROL Parse XML] e convertirlo in un bundle per rendere i dati disponibili ad altri moduli. È inoltre possibile convertire un bundle in un testo in formato XML tramite il modulo [!UICONTROL XML] > [!UICONTROL Create XML]

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
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
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

## [!UICONTROL Parse XML]

Il modulo [!UICONTROL XML] > [!UICONTROL Parse XML] analizza un testo in formato XML e restituisce un singolo bundle contenente tutte le informazioni estratte dal codice XML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>La struttura dati descrive la struttura del codice XML per rendere disponibile l'output del modulo nel pannello di mappatura per i moduli seguenti.</p> <p>Se si dispone di un esempio del codice XML che si desidera analizzare, è possibile utilizzarlo per generare la struttura dati:</p> 
    <ol> 
     <li value="1">Fare clic sul pulsante <strong>[!UICONTROL Add]</strong>.</li> 
     <li value="2">Fare clic sul pulsante <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Copiare e incollare l'esempio XML nel campo <strong>[!UICONTROL Sample data]</strong>.</li> 
     <li value="4">Fare clic su <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Verifica che la struttura dati sia stata generata correttamente.</li> 
     <li value="6"> <p>Fare clic sul pulsante <strong>[!UICONTROL Save]</strong> per salvare la struttura dati.</p> <p>Puoi saltare i passaggi da 2 a 5 per fornire una struttura di dati vuota. Se la struttura dati è vuota, l’output del modulo non è disponibile nel pannello di mappatura finché il modulo non viene eseguito almeno una volta.</p> </li> 
    </ol> <p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Strutture dati in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>Abilita questa opzione per garantire che i numeri rimangano come valori di testo (stringa). In caso contrario, i numeri vengono assegnati ai valori numerici.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Immettere o associare il testo in formato XML da analizzare.</p> <p>Se si utilizza una formula, verificare che il tipo di valore del risultato sia o possa essere automaticamente forzato a [!UICONTROL Text]. </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Se il tipo di valore del risultato è [!UICONTROL Buffer] (dati binari), utilizzare la funzione <code>toString()</code> per convertirlo nel tipo di dati Testo. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo coercizione in [!DNL Adobe Workfront Fusion]</a> e <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipi di dati elemento in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Esempio:** Per scaricare un file XML da un URL e analizzarne il contenuto:
>
>1. Crea un nuovo scenario.
>1. Inserisci modulo [!UICONTROL HTTP] > [!UICONTROL Get a file]
>1. Apri la configurazione del modulo e configurala come segue:
>
>   **URL**: URL del file XML (esempio: `https://siftrss.com/f/rqLy05ayMBJ`)
>
>   ![](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)
>
>1. Fare clic su **[!UICONTROL OK]** &#x200B; salvare e chiudere la configurazione del modulo.
1. Aggiungi il modulo [!UICONTROL XML] > [!UICONTROL Parse XML], connettilo dopo il modulo [!UICONTROL HTTP] > [!UICONTROL Get a file] e configuralo come segue:
>
<table style="table-layout:auto"> 
&gt;    <col> 
&gt;    <col> 
&gt;    <tbody> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL Data structure]</td> 
&gt;      <td> 
&gt;       <ol> 
&gt;        <li value="1">Fare clic sul pulsante <strong>[!UICONTROL Add]</strong>.</li> 
&gt;        <li value="2">Fare clic sul pulsante <strong>[!UICONTROL Generator]</strong>.</li> 
&gt;        <li value="3">Nel browser Web aprire una nuova scheda o finestra.</li> 
&gt;        <li value="4">Inserisci l’URL utilizzato nel terzo passaggio nella barra degli indirizzi e recupera il file XML.</li> 
&gt;        <li value="5">Selezionare tutto il testo XML e copiarlo negli Appunti.</li> 
&gt;        <li value="6">Chiudi la scheda o la finestra e torna allo scenario.</li> 
&gt;        <li value="7">Incollare il testo XML copiato nel campo Dati di esempio.</li> 
&gt;        <li value="8">Fare clic su <strong>[!UICONTROL Save]</strong>.</li> 
&gt;        <li value="9">Verifica che la struttura dati sia stata generata correttamente.</li> 
&gt;        <li value="10">Fare clic su <strong>[!UICONTROL Save]</strong> per salvare la struttura dati.</li> 
&gt;       </ol> <p>Puoi saltare i passaggi da 2 a 9 per fornire una struttura di dati vuota. Se la struttura dati è vuota, l’output del modulo non è disponibile nel pannello di mappatura finché il modulo non viene eseguito almeno una volta.</p> </td> 
&gt;     </tr> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL XML]</td> 
&gt;      <td> <p>Mappa l'elemento <code>Data </code> dall'output del modulo [!UICONTROL HTTP] &gt; [!UICONTROL Get a file] nel campo. Utilizzare la funzione <code>toString()</code> per convertire il relativo valore dal tipo [!UICONTROL Buffer] (dati binari) al tipo di dati [!UICONTROL Text].</p> <p>È possibile copiare e incollare il codice della formula nel campo: <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Per ulteriori informazioni sui tipi di dati Buffer e Testo, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Tipi di dati elemento in Adobe Workfront Fusion</a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png" style="width: 350;height: 99;"> </p> </td> 
&gt;     </tr> 
&gt;    </tbody> 
&gt;   </table>

## [!UICONTROL Parsing XML attributes]

Per impostazione predefinita, il modulo [!UICONTROL XML] > [!UICONTROL Parse XML] inserisce gli attributi in una raccolta speciale `_attributes` come figlio del nodo che ha questi attributi. Se il nodo è un nodo di testo e dispone di attributi, vengono aggiunte due proprietà speciali: `_attributes` per gli attributi e `_value` per il contenuto di testo del nodo.

>[!INFO]
>
**Esempio:** Questo XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

viene convertito in questo bundle:

![](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

## Crea XML

Il modulo [!UICONTROL XML] > [!UICONTROL Create XML] converte un bundle in un testo in formato XML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>La struttura Dati descrive la struttura del codice XML risultante. Se si dispone di un esempio del codice XML che si desidera creare, è possibile utilizzarlo per generare la struttura dati:</p> 
    <ol> 
     <li value="1">Fare clic sul pulsante <strong>[!UICONTROL Add]</strong>.</li> 
     <li value="2">Fare clic sul pulsante <strong>[!UICONTROL Generator]</strong>.</li> 
     <li value="3">Copiare e incollare l'esempio XML nel campo Dati di esempio.</li> 
     <li value="4">Fare clic sul pulsante <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Verifica che la struttura dati sia stata generata correttamente.</li> 
     <li value="6">Fare clic su <strong>[!UICONTROL Save]</strong> per salvare la struttura dati.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>Immettere il nome dell'elemento principale dell'XML. Il valore predefinito è <code>root</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td>Immettere il nome del file da utilizzare nella dichiarazione <code> !DOCTYPE SYSTEM</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td>Immettere il nome del file da utilizzare nella dichiarazione <code> !DOCTYPE PUBLIC</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>Abilitare questa opzione per rimuovere la dichiarazione XML <code>&lt;?xml ... ?&gt;</code> e <code>&lt;!DOCTYPE ... &gt;</code> e lasciare solo l'elemento radice XML e il relativo contenuto.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
**Esempio:**
>
Un caso d&#39;uso tipico consiste nel trasformare i dati da un foglio di calcolo [!DNL Google] in XML.
>
1. Inserisci il modulo [!DNL Google Sheets] > [!UICONTROL Select rows] nello scenario per recuperare i dati. Configurare il modulo per recuperare le righe dal foglio di calcolo [!DNL Google]. Impostare il valore&#x200B;**[!UICONTROL Maximum number of returned rows]** su un numero piccolo, ma maggiore di uno a scopo di test (ad esempio, tre). Eseguire il modulo [!DNL Google Sheets] facendo clic con il pulsante destro del mouse su di esso e scegliendo &quot;**[!UICONTROL Run this module only]**&quot;. Verifica l’output del modulo.
1. Connetti il modulo [!UICONTROL Array Aggregator] dopo il modulo [!DNL Google Sheets]. Nella configurazione del modulo, scegliere il modulo [!DNL Google Sheets] nel campo **[!UICONTROL Source node]**. Lascia gli altri campi così come sono per il momento.
1. Connetti il modulo [!UICONTROL XML] > [!UICONTROL Create XML] dopo il modulo [!UICONTROL Array Aggregator].
>
La configurazione del modulo richiede una struttura di dati che descriva la struttura dell&#39;output XML. Fare clic sul pulsante **[!UICONTROL Add]** per aprire la configurazione della struttura dati. Il modo più semplice per creare questa struttura dati consiste nel generarla automaticamente da un esempio XML.
>
1. Fai clic sul pulsante **[!UICONTROL Generator]** e incolla l&#39;esempio XML nel campo [!UICONTROL Sample data]:
>
![](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)
>
1. Fare clic su **[!UICONTROL Save]**. Il campo Specification (Specifica) nella struttura Data (Dati) ora contiene la struttura generata.
1. Modificare il nome della struttura dati in un nome più specifico e fare clic su **[!UICONTROL Save]**. Un campo corrispondente all’attributo dell’array principale viene visualizzato come campo mappabile nella configurazione del modulo JSON.
1. Fare clic sul pulsante **[!UICONTROL Map]** accanto al campo e mappare l&#39;elemento `Array[]` dell&#39;output [!UICONTROL Array aggregator] su di esso:
1. Fare clic su **[!UICONTROL OK]** per chiudere la configurazione del modulo XML.
1. Aprire la configurazione del modulo [!UICONTROL Array Aggregator]. Modificare **[!UICONTROL Target structure]** da Personalizzato nel campo di un modulo XML corrispondente agli elementi XML padre.Map del modulo [!DNL Google Sheets] nei campi appropriati.
1. Fare clic su **[!UICONTROL OK]** per chiudere la configurazione del modulo Aggregator di array.
1. Esegui lo scenario.
>
Il modulo XML restituisce il file XML corretto.
>
1. Aprire la configurazione del modulo [!DNL Google Sheets] e aumentare il numero di [!UICONTROL Maximum number of returned rows] affinché sia maggiore del numero di righe nel foglio di calcolo per elaborare tutti i dati.
>
L&#39;XML risultante può essere salvato in [!DNL Dropbox], inviato come allegato tramite e-mail, caricato tramite FTP su un server e così via.

## Aggiunta di attributi XML

Se si desidera aggiungere attributi a un nodo complesso (un nodo che conterrà altri nodi), è necessario aggiungere una raccolta con il nome `_attributes` per la nota complessa nella struttura dati personalizzata. Questa raccolta verrà mappata agli attributi del nodo. Se si desidera aggiungere attributi a un nodo di testo (ad esempio: `<node attr="1">abc</node>`), è necessario aggiungere una raccolta `_attributes` per gli attributi e una proprietà di testo `_value` per il valore del nodo per questo nodo nella struttura dati personalizzata.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## Risoluzione dei problemi: impossibile mappare i dati dal modulo [!UICONTROL Parse XML]

Assicurati che la struttura dati sia definita correttamente. In alternativa, è possibile utilizzare una struttura dati vuota ed eseguire il modulo almeno una volta per elaborare un input XML.