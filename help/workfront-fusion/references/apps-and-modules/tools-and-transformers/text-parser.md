---
title: Parser testo
description: È possibile utilizzare lo strumento parser di testo per analizzare il testo da utilizzare in altri [!DNL Adobe Workfront Fusion]  moduli scenario. Il parser di testo non richiede una connessione.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: 4fa892b7875af2fcabaf26b375925af7a8cad2a0
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 0%

---

# [!UICONTROL Text parser]

È possibile utilizzare [!UICONTROL Text parser tool] per analizzare il testo da utilizzare in altri moduli scenario [!DNL Adobe Workfront Fusion]. [!UICONTROL Text parser] non richiede una connessione.

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
   <p>Nessuna licenza Workfront Fusion richiesta.</p>
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

## Informazioni API parser di testo

Il connettore parser di testo utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Text parser] moduli e relativi campi

Quando configuri [!UICONTROL Text parser] moduli, [!DNL Adobe Workfront Fusion] visualizza i campi elencati di seguito. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trasformatori

* [[!UICONTROL Get Elements from HTML]](#get-elements-from-html)
* [[!UICONTROL Get Elements from text]](#get-elements-from-text)
* [[!UICONTROL HTML to Text]](#html-to-text)
* [[!UICONTROL Match Pattern]](#match-pattern)
* [[!UICONTROL Replace]](#replace)

#### [!UICONTROL Get Elements from HTML]

Recupera gli elementi desiderati dal codice HTML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module finds no matches]</td> 
   <td> <p>Abilita questa opzione per garantire che il modulo non interrompa lo scenario se non restituisce alcun risultato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Element type]</td> 
   <td> <p> Seleziona il tipo di elemento da recuperare dal codice HTML. </p> 
    <ul> 
     <li>[!UICONTROL Image]</li> 
     <li>[!UICONTROL Link]</li> 
     <li>[!UICONTROL iFrame element(s)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Immettere o mappare il codice HTML da cui si desidera recuperare i tipi di elemento specificati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Elements from text]

Analizza gli elementi dal testo in base al pattern specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Input text]</td> 
   <td> <p>Immettere o mappare il testo che si desidera analizzare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pattern]</td> 
   <td> <p>Selezionate il motivo che riflette gli elementi da analizzare dal testo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ignore Duplicate Occurrences]</td> 
   <td> <p>Selezionare questa casella per ignorare le occorrenze duplicate di un elemento di testo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML to Text]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Immettere il codice HTML che si desidera convertire in testo normale.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Line break] </td> 
   <td> <p>Seleziona il tipo di nuova riga (interruzione di riga).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Uppercase headings]</p> </td> 
   <td> <p>Abilita questa opzione per convertire in testo maiuscolo il testo racchiuso nei tag di intestazione (ad esempio &lt;h2&gt; &lt;/h2&gt;).</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Match Pattern]

Il modulo [!UICONTROL Match pattern] consente di trovare ed estrarre elementi stringa corrispondenti a un pattern di ricerca da un determinato testo. Questo modulo utilizza espressioni regolari (note anche come regex o regexp).

Un’espressione regolare è una sequenza di caratteri in cui ogni carattere è un metacarattere, con un significato speciale, o un carattere regolare con un significato letterale. Questi caratteri e metacaratteri identificano un pattern che può essere utilizzato per la ricerca di testo. Ad esempio, se si desidera cercare i nomi, è possibile impostare un&#39;espressione regolare per cercare un motivo costituito da due parole consecutive che iniziano con lettere maiuscole. Le espressioni regolari sono uno strumento utile per la ricerca e la manipolazione del testo.

Una discussione sulle espressioni regolari va oltre lo scopo di questo articolo. Si consiglia di utilizzare le risorse seguenti:

* Per l&#39;elenco completo dei metacaratteri, vedere [Espressioni regolari](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) nei documenti Web MDN.
* Per un&#39;esercitazione sulla creazione di espressioni regolari, consigliamo [RegexOne](https://regexone.com/).
* Per la sperimentazione con espressioni regolari, consigliamo il sito Web [Espressioni regolari 101](https://regex101.com/). Selezionare ECMAScript (JavaScript) FLAVOR nel pannello sinistro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Immettete il pattern di espressione regolare. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code> estrae tutti i numeri nel testo specificato.</p> <p>Nota:  <p>Il modello deve contenere almeno un gruppo di acquisizione tra parentesi <code>()</code>. Se il modello non contiene gruppi di acquisizione, il bundle di output è vuoto.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Abilita questa opzione per recuperare tutte le corrispondenze nel testo. Ogni corrispondenza viene generata in un bundle separato. Se questa opzione è disattivata, il modulo recupera solo la prima voce.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Abilita questa opzione per questo modulo per trattare il testo con distinzione tra maiuscole e minuscole.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Abilitare questa opzione per assicurarsi che i metacaratteri iniziale e finale (<code>^</code> e <code>$</code>) corrispondano all'inizio o alla fine di ogni riga, non solo all'inizio o alla fine dell'intera stringa di input.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Abilitare questa opzione per assicurarsi che il punto (.) corrisponda ai caratteri di nuova riga (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p>Abilita questa opzione per garantire che il modulo non interrompa lo scenario se non restituisce alcun risultato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Immettere o mappare il testo che si desidera associare al motivo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace]

Cerca un valore o un&#39;espressione regolare specificata nel testo immesso e sostituisce il risultato con il nuovo valore.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Immettere il termine di ricerca. È inoltre possibile utilizzare un'espressione regolare. Per ulteriori dettagli sull'espressione regolare, fare riferimento al modulo <a href="#match-pattern" class="MCXref xref">[!UICONTROL Match Pattern]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New value]</td> 
   <td> <p> Immettere il valore che si desidera sostituire al termine di ricerca.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Abilita questa opzione per recuperare tutte le corrispondenze nel testo. Ogni corrispondenza viene generata in un bundle separato. Se questa opzione è disattivata, il modulo recupera solo la prima voce.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Abilita questa opzione per questo modulo per trattare il testo con distinzione tra maiuscole e minuscole.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Abilitare questa opzione per assicurarsi che i metacaratteri iniziale e finale (<code>^</code> e <code>$</code>) corrispondano all'inizio o alla fine di ogni riga, non solo all'inizio o alla fine dell'intera stringa di input.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Abilitare questa opzione per assicurarsi che il punto (.) corrisponda ai caratteri di nuova riga (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Immettere il testo in cui eseguire la ricerca.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Scraping dei dati

Il raschiamento dei dati, a volte chiamato web scraping, estrazione dei dati o web harvesting, è il processo di raccolta dei dati dai siti web e di archiviazione nel database locale o nei fogli di calcolo. Se desideri estrarre i dati da un sito web e non hai familiarità con le espressioni regolari, puoi utilizzare uno strumento di raschiamento dei dati.

Se lo strumento di scarto dati fornisce un&#39;API REST, puoi connetterti tramite i nostri moduli universali [[!UICONTROL HTTP]](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors) e [Webhook](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

## Risoluzione dei problemi relativi al parser di testo

Utilizza queste informazioni se non riesci a ottenere un parser di testo per produrre alcun output.

>[!BEGINSHADEBOX]

Esempio:

Il modulo deve analizzare il tipo di file di un documento di file &quot;filename.docx&quot; e l’estensione del nome file varia da DOCX a PDF a CSV.

L&#39;espressione che si può scegliere di utilizzare in questo caso è [!DNL \..+]

Questa espressione regolare normalmente darebbe luogo a una corrispondenza completa.

Tuttavia, l’implementazione di questa espressione nel parser di testo non produce una corrispondenza:

![](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

Il motivo è che la &quot;i&quot; mostra solo il numero di corrispondenze per partita, quindi in questo caso abbiamo 2 corrispondenze, quindi dopo la &quot;i&quot; c&#39;è un valore numerico 1 e 2. Il caso d’uso prevede che, se dovesse essere necessario far corrispondere o trasmettere dati attraverso un filtro, solo il secondo valore corrispondente sia possibile specificare quale valore è rappresentato dal valore numerico.

![](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

Per ottenere i valori di corrispondenza necessari per aggiungere parentesi alla parte che si desidera analizzare, ad esempio per estrarre da &quot;filename.docx&quot; - solo &quot;docx&quot;, in base all&#39;espressione regex utilizzata per questo scenario, le parentesi devono essere applicate a \.(.+)

Questo acquisisce il DOCX, lo inserisce in un gruppo e lascia il &quot;.&quot; fuori di esso.

![](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

Nell&#39;output mostrato nell&#39;immagine seguente, il gruppo di cattura corrisponderà a qualsiasi carattere (ad eccezione dei terminatori di riga).

![](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

Un’altra soluzione alternativa che incorpora anche regex è l’utilizzo della funzione replace

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

Quindi sostituisci `abcdefghijklmno pqr stuvw xyz.docx` con la tua effettiva variabile di nome file.

>[!ENDSHADEBOX]
