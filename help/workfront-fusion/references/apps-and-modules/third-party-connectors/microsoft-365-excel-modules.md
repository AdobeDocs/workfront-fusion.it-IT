---
title: Moduli Excel di Microsoft Office 365
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Microsoft 365 Excel, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2693'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Excel] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft 365 Excel] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare [!DNL Microsoft office 365 Excel], è necessario disporre di un account Microsoft.

## Informazioni API di Microsoft Office 365 Excel

Il connettore Microsoft Office 365 Excel utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## Connessione del servizio [!DNL Office 365 Excel] a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account [!DNL Office 365 Excel] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## [!DNL Microsoft Office 365 Excel] moduli e relativi campi

Quando si configurano [!DNL Microsoft 365 Excel] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Microsoft 365 Excel], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Cartella di lavoro](#workbook)
* [Foglio di lavoro](#worksheet)
* [Tabella](#table)
* [Altro](#other)

### Cartella di lavoro

* [Scaricare una cartella di lavoro](#download-a-workbook)
* [Cerca cartelle di lavoro](#search-workbooks)
* [Cartelle di lavoro di controllo](#watch-workbooks)

#### [!UICONTROL Scarica una cartella di lavoro]

Questo modulo di azione scarica il contenuto della cartella di lavoro di Excel specificata.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scarica una cartella di lavoro]</td> 
   <td> <p>Selezionare la modalità di identificazione della cartella di lavoro per il modulo da scaricare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immettendo manualmente un ID]</strong> </p> <p>Nel campo [!UICONTROL ID cartella di lavoro] immettere o mappare l'ID della cartella di lavoro specifica che si desidera scaricare dal modulo.</p> </li> 
     <li> <p><strong>[!UICONTROL Selezionando dal percorso]</strong> </p> <p>Nel campo [!UICONTROL Cartella di lavoro] selezionare la cartella di lavoro che si desidera scaricare dal modulo, incluso il relativo percorso se non si trova nella cartella principale.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca cartelle di lavoro]

Questo modulo di azione cerca [!DNL Excel] cartelle di lavoro.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selezionare la cartella in cui si desidera cercare le cartelle di lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filtro]</p> </td> 
   <td> <p>È possibile impostare un filtro per cercare solo le cartelle di lavoro che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND o OR.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di fogli di lavoro che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Cartelle di lavoro osservate]

Questo modulo di attivazione avvia uno scenario quando viene creata una cartella di lavoro.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selezionare la cartella da controllare per le nuove cartelle di lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filtro]</p> </td> 
   <td> <p>È possibile impostare un filtro per controllare solo le cartelle di lavoro che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND o OR.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di cartelle di lavoro che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Foglio di lavoro

* [[!UICONTROL Aggiungi un foglio di lavoro]](#add-a-worksheet)
* [[!UICONTROL Aggiungi riga foglio di lavoro]](#add-a-worksheet-row)
* [[!UICONTROL Elimina riga foglio di lavoro]](#delete-a-worksheet-row)
* [[!UICONTROL Elenca righe foglio di lavoro]](#list-worksheet-rows)
* [[!UICONTROL Elenca fogli di lavoro]](#list-worksheets)
* [[!UICONTROL Aggiorna riga foglio di lavoro]](#update-a-worksheet-row)
* [[!UICONTROL Righe foglio di lavoro di controllo]](#watch-worksheet-rows)

#### [!UICONTROL Aggiungi un foglio di lavoro]

Questo modulo di azione crea un nuovo foglio di lavoro all’interno della cartella di lavoro selezionata.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro in cui si desidera aggiungere un foglio di lavoro, incluso il percorso se la cartella di lavoro non si trova nella directory principale.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Name] </td>
   <td> <p>Immettere o associare un nome per il nuovo foglio di lavoro.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiungi riga foglio di lavoro]

Questo modulo di azione aggiunge una nuova riga al foglio di lavoro selezionato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro in cui si desidera aggiungere una riga, incluso il percorso se la cartella di lavoro non si trova nella directory principale.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro in cui aggiungere una riga.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di valori immessi]</p> </td> 
   <td> <p>Selezionare il tipo di valore da immettere nel foglio di lavoro. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formule]</strong> </p> <p> Excel tenta di valutare l'espressione specificata. I nomi delle funzioni in una formula sono in inglese. Esempio: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formule locali]</strong> </p> <p>Excel tenta di valutare l'espressione specificata. I nomi delle funzioni sono nella lingua dell'applicazione Excel. Esempio: <code>=SUM(A1, 1.5)</code> vs. <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Valore]</strong> </p> <p>Excel non valuta il valore. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Riga]</td>
    <td>Per ogni colonna, immettere il valore desiderato per la colonna nella nuova riga.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina riga foglio di lavoro]

Questo modulo di azione elimina una riga da un foglio di lavoro.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro che include la riga che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet]</td>
   <td> <p> Selezionare il foglio di lavoro contenente la riga che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row ID]</td>
   <td>Inserisci o mappa l’ID della riga da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca righe foglio di lavoro]

Questo modulo di azione recupera un elenco di righe nel foglio di lavoro specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro che include le righe da elencare, incluso il percorso se la cartella di lavoro non si trova nella directory principale.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro contenente le righe da elencare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di righe del foglio di lavoro che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca fogli di lavoro]

Questo modulo di azione recupera un elenco di fogli di lavoro nella cartella di lavoro specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente i fogli di lavoro che si desidera elencare nel modulo.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di fogli di lavoro che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna riga foglio di lavoro]

Questo modulo di azione aggiorna una riga del foglio di lavoro esistente.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro che include la riga che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro contenente la riga da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di valori immessi]</p> </td> 
   <td> <p>Selezionare il tipo di valore da immettere nel foglio di lavoro. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formule]</strong> </p> <p> Excel tenta di valutare l'espressione specificata. I nomi delle funzioni in una formula sono in inglese. Esempio: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formule locali]</strong> </p> <p>Excel tenta di valutare l'espressione specificata. I nomi delle funzioni sono nella lingua dell'applicazione Excel. Esempio: <code>=SUM(A1, 1.5)</code> vs. <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Valore]</strong> </p> <p>Excel non valuta il valore. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row ID]</td> 
   <td>Seleziona il numero della riga da aggiornare.</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Riga]</td>
    <td>Per ogni colonna, immettere il valore desiderato per la colonna nella nuova riga.</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL Righe foglio di lavoro di controllo]

Questo modulo di attivazione avvia uno scenario quando viene aggiunta una nuova riga al foglio.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro che si desidera controllare per le nuove righe.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di Excel da controllare per le nuove righe.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Ignora righe vuote] </td>
   <td> <p>Abilita questa opzione per non restituire i bundle per le righe vuote nel foglio di lavoro.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di righe del foglio di lavoro che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Tabella

* [[!UICONTROL Aggiungi una tabella]](#add-a-table)
* [[!UICONTROL Aggiungi una riga di tabella]](#add-a-table-row)
* [[!UICONTROL Eliminare una tabella]](#delete-a-table)
* [[!UICONTROL Ottieni una tabella]](#get-a-table)
* [[!UICONTROL Elenca righe tabella]](#list-table-rows)
* [[!UICONTROL Elenca tabelle]](#list-tables)
* [[!UICONTROL Aggiorna una tabella]](#update-a-table)
* [[!UICONTROL Osserva righe tabella]](#watch-table-rows)

#### [!UICONTROL Aggiungi una tabella]

Questo modulo di azione crea un elemento tabella nel foglio di lavoro di Excel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL cartella di lavoro] </td> 
   <td> <p>Selezionare la cartella di lavoro contenente il foglio di lavoro in cui si desidera aggiungere una tabella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Selezionare il foglio di lavoro in cui aggiungere una tabella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ha Intestazioni]</td> 
   <td> <p>Abilita questa opzione per definire la prima riga come intestazioni di tabella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Address]</p> </td> 
   <td> <p>Impostare le dimensioni della tabella indicando le celle in alto a sinistra e in basso a destra. Esempio: <code>A1:C10</code> crea una tabella con 3 colonne e 10 righe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiungi una riga di tabella]

Questo modulo modifica una tabella esistente.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente la tabella in cui si desidera aggiungere una riga.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro contenente la tabella in cui si desidera aggiungere una riga.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >Tabella </td>
   <td>Selezionare la tabella in cui si desidera aggiungere una riga.</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Riga]</td>
    <td>Per ogni colonna, immettere il valore desiderato per la colonna nella nuova riga.</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row ID]</p> </td> 
   <td> <p>Per aggiungere una riga in una posizione specifica della tabella, immettere o mappare un numero di riga. Il modulo inserisce la nuova riga dopo questa riga.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare una tabella]

Questo modulo di azione elimina la tabella specificata da un foglio di lavoro [!DNL Excel].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elimina una tabella]</td> 
   <td> <p>Selezionare la modalità di identificazione della tabella da eliminare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID della cartella di lavoro contenente la tabella da eliminare, quindi immettere o mappare l'ID del foglio di lavoro contenente la tabella.</p> <p>Nel campo [!UICONTROL Nome tabella] immettere o mappare il nome della tabella che si desidera eliminare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare la cartella di lavoro e il foglio di lavoro contenenti la tabella che si desidera eliminare, quindi selezionare la tabella.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni una tabella]

Questo modulo di azione recupera i metadati per la tabella specificata.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL Connection]</p>
   </td> 
   <td> 
     <p>Per istruzioni sulla connessione dell'account di Office 365 a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p>
    --&gt; </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recupera una tabella]</td> 
   <td> <p>Selezionare la modalità di identificazione della tabella che si desidera recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID della cartella di lavoro contenente la tabella che si desidera recuperare, quindi immettere o mappare l'ID del foglio di lavoro contenente la tabella.</p> <p>Nel campo [!UICONTROL Nome tabella] immettere o mappare il nome della tabella che si desidera recuperare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare la cartella di lavoro e il foglio di lavoro contenenti la tabella che si desidera recuperare, quindi selezionare la tabella.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca righe tabella]

Questo modulo di ricerca recupera un elenco di tutte le righe di tabella in una cartella di lavoro.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente la tabella che include le righe da elencare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro contenente la tabella che include le righe da elencare</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >Tabella  </td>
   <td> <p>Selezionare la tabella contenente le righe da elencare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di righe di tabella che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca tabelle]

Questo modulo di ricerca recupera un elenco di tutti gli oggetti tabella.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL cartella di lavoro] </td>
   <td> <p>Selezionare la cartella di lavoro contenente le tabelle da elencare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selezionare il foglio di lavoro contenente le tabelle da elencare</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di tabelle che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna una tabella]

Questo modulo di azione aggiorna una tabella esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Aggiorna una tabella]</td> 
   <td> <p>Selezionare la modalità di identificazione della tabella da aggiornare.</p> 
    <ul> 
     <li> <p><strong>Immetti manualmente</strong> </p> <p>Nel campo [!UICONTROL ID cartella di lavoro] immettere o mappare l'ID della cartella di lavoro contenente la tabella che si desidera aggiornare.</p> <p>Nel campo [!UICONTROL Nome tabella] immettere o mappare il nome della tabella che si desidera aggiornare.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona dall'elenco]</strong> </p> <p>Selezionare la cartella di lavoro e il foglio di lavoro contenenti la tabella che si desidera aggiornare, quindi selezionare la tabella.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Se si desidera rinominare la tabella, immettere o mappare un nuovo nome per la tabella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra intestazioni]</td> 
   <td> <p>Abilita questa opzione per mostrare le intestazioni della tabella aggiornata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra totali]</td> 
   <td>Abilita questa opzione per visualizzare i valori totali della tabella.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style]</td> 
   <td>Scegliere uno stile per la nuova tabella.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Osserva righe tabella]

Questo trigger avvia uno scenario quando viene aggiunta una nuova riga a una tabella.

>[!NOTE]
>
>La tabella qui fa riferimento all&#39;elemento tabella incorporato nella cartella di lavoro. Non l&#39;intera tabella (cartella/foglio).

![Tabella incorporata](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL cartella di lavoro]</p> </td> 
   <td> <p>Selezionare la cartella di lavoro contenente la tabella che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p> Selezionare il foglio di lavoro contenente la tabella che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tabella </p> </td> 
   <td> <p>Selezionare la tabella che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Immettere o mappare il numero massimo di righe che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)
* [[!UICONTROL Recupera dati]](#retrieve-data)

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo di azione ti consente di effettuare una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:   <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Recupera dati]

Questa azione recupera i dati dall&#39;intervallo del foglio di lavoro definito e restituisce un bundle per ogni riga.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL cartella di lavoro] </td> 
   <td> <p>Selezionare la cartella di lavoro contenente i dati da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Selezionare il foglio di lavoro contenente i dati che si desidera recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Range] </td> 
   <td> <p>Specificare l'area del foglio da cui si desidera recuperare i dati indicando le celle in alto a sinistra e in basso a destra. Esempio: <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
