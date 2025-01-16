---
title: Moduli Power BI
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2082'
ht-degree: 0%

---

# [!DNL Power BI] moduli

[!DNL Power BI] è un&#39;applicazione che consente di visualizzare e presentare dati alle parti interessate. Può acquisire dati da diverse fonti.

>[!NOTE]
>
>[!DNL Workfront Fusion] non è un&#39;origine dati. [!DNL Workfront Fusion] può creare e utilizzare origini dati, ma non memorizza i dati.


## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td> 
   <td> <p>[!DNL Pro] o superiore</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td> 
   <td> <p>[!DNL Plan], [!DNL Work]</p> </td> 
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

&#42;Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore [!DNL Workfront].

&#42;&#42;Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Informazioni API di Microsoft Power BI

Il connettore Microsoft Power BI utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI] moduli e relativi campi

Quando configuri [!DNL Power BI], [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo all&#39;altro in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Dashboard](#dashboards)
* [Report](#reports)
* [Set di dati](#dataset)
* [App](#apps)
* [Altro](#other)

### Dashboard

* [Creare un dashboard](#create-a-dashboard)
* [Ottieni un dashboard](#get-a-dashboard)
* [Ottieni sezione dashboard](#get-a-dashboard-tile)
* [Elencare riquadri del dashboard](#list-dashboard-tiles)
* [Elenca dashboard](#list-dashboards)

#### [!UICONTROL Create a Dashboard]

Questo modulo di azione crea un nuovo dashboard.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Immettete o mappate un nome per il dashboard.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo proprietario del nuovo dashboard.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard]

Questo modulo di azione recupera i metadati di un dashboard specificato.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il dashboard per il quale desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del dashboard per cui desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartengono le dashboard per le quali desideri recuperare i metadati.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard Tile]

Questo modulo di azione recupera i metadati di una sezione del dashboard specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere i dettagli del dashboard da recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Immetti o mappa l’ID del dashboard per il quale desideri recuperare i dettagli.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tile ID]</td>
      <td>Immettere o mappare l'ID del riquadro [!DNL Power BI] per il quale si desidera recuperare i dettagli.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartiene la sezione da recuperare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Dashboard Tiles]

Questo modulo di ricerca recupera un elenco di riquadri del dashboard.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
    <td>
      <p>Seleziona o mappa l’opzione per scegliere il dashboard di cui desideri elencare le tessere.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Dashboard ID]</td>
    <td>
      <p>Inserisci o mappa l’ID del dashboard contenente le tessere che desideri elencare.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Group ID]  </td>
    <td>Seleziona o mappa l’ID del Gruppo a cui appartengono le dashboard contenenti le tessere che desideri elencare.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]  </td>
    <td>
      <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL List Dashboards]

Questo modulo di ricerca recupera un elenco di dashboard.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Seleziona o mappa l’ID del gruppo a cui appartengono le dashboard che desideri elencare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

### Report

* [Copiare un rapporto](#copy-a-report)
* [Eliminare un rapporto](#delete-a-report)
* [Ottieni un rapporto](#get-a-report)
* [Elencare rapporti](#list-reports)

#### [!UICONTROL Copy a Report]

Questo modulo di azione copia un rapporto esistente.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il rapporto da copiare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del rapporto da copiare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartiene il rapporto da copiare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL New Copied Report Name]</td>
      <td>Immettere o mappare un nome per il nuovo rapporto.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Report]

Questo modulo di azione elimina un rapporto.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il rapporto da eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del rapporto da eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo proprietario del rapporto che desideri eliminare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Report]

Questo modulo di azione recupera i metadati di un rapporto specificato.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il rapporto per il quale desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del rapporto per il quale desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartiene il rapporto per il quale desideri recuperare i metadati.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Reports]

Questo modulo di ricerca recupera un elenco di rapporti.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Seleziona o mappa l’ID del gruppo a cui appartengono i rapporti che desideri elencare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>


### Set di dati

* [Aggiungere/eliminare righe in una tabella di set di dati](#add-or-delete-rows-in-a-dataset-table)
* [Creare un set di dati](#create-a-dataset)
* [Eliminare un set di dati](#delete-a-dataset)
* [Ottenere un set di dati](#get-a-dataset)
* [Elencare set di dati](#list-datasets)
* [Aggiornare un set di dati](#refresh-a-dataset)

#### [!UICONTROL Add or Delete Rows in a Dataset Table]

Questo modulo di azione aggiunge o elimina righe di una tabella di set di dati push specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a table]</td>
      <td>Seleziona o mappa l’opzione per selezionare il set di dati contenente la tabella da regolare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Inserisci o mappa l’ID del set di dati contenente le righe da aggiungere o eliminare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Immettere o mappare il nome della tabella contenente le righe che si desidera aggiungere o eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Inserisci o mappa l’ID del gruppo proprietario del set di dati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Select the Action]</td>
      <td>
        <p>Seleziona o mappa l’azione da eseguire.</p>
        <ul>
          <li>
            <p>[!UICONTROL Add rows]</p>
          </li>
          <li>
            <p>[!UICONTROL Delete All Rows]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>
        <p>Aggiungi i campi riga.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Key]</b>
            </p>
            <p>Immetti o mappa il nome della chiave.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Field Type]</b>
            </p>
            <p>Seleziona o mappa il tipo di campo:</p>
            <ul>
              <li>
                <p>Booleano</p>
              </li>
              <li>
                <p>Data</p>
              </li>
              <li>
                <p>Testo</p>
              </li>
              <li>
                <p>Numero</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL Value]</p>
            <p>Immetti o mappa il valore chiave.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Create a Dataset]

Questo modulo di azione crea un nuovo set di dati.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Inserisci o mappa un nome per il set di dati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo proprietario del nuovo set di dati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default Mode]</td>
      <td>
        <p>Seleziona o mappa la modalità predefinita per il set di dati:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL As Azure]</b>: set di dati con una connessione live a [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL As on Prem]</b>: set di dati con una connessione live al servizio [!DNL On-premise Analysis]</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>: set di dati che consente l’accesso programmatico per la trasmissione di dati in [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>: set di dati che supporta lo streaming di dati e consente l’accesso programmatico per la trasmissione di dati in [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>: set di dati che supporta lo streaming di dati</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tables]</td>
      <td>Aggiungi tabelle al set di dati. Per i campi, vedere <a href="#Table" class="MCXref_0">Campi tabella</a></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>Aggiungi le origini dati. Per i campi, vedere <a href="#Data" class="MCXref_0">Campi origini dati</a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>Seleziona o mappa il criterio intenzionale per il set di dati:</p>
        <ul>
          <li>
            <p>[!UICONTROL None]</p>
          </li>
          <li>
            <p>[!UICONTROL Basic FIFO]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Campi tabella

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>  Immettere o mappare un nome per la tabella.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Columns]</td>
      <td>
        <p>Aggiungi le colonne:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Immetti (mappare) un nome di colonna.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Data Type]</b>
            </p>
            <p>Selezionare o mappare il tipo di dati:</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL Integer]</p>
              </li>
              <li>
                <p>[!UICONTROL Boolean]</p>
              </li>
              <li>
                <p>[!UICONTROL Date Time]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Format String]</b>
            </p>
            <p>Immetti (mappa) la stringa di formato.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>Immetti o mappa i dettagli della riga.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Measures]</td>
      <td>Aggiungere la misura per le tabelle.</td>
    </tr>
  </tbody>
</table>

##### Campi origini dati

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Database]  </td>
      <td>
        <p>Immettere o mappare il database che si desidera utilizzare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>Immettere o mappare il nome del server che si desidera utilizzare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>Inserisci o mappa l’URL da utilizzare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source ID]</td>
      <td>
        <p>  Immetti o mappa l’ID dell’origine dati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source Type]  </td>
      <td>
        <p>Selezionare o mappare il tipo di origine dati. Esempio: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gateway ID]  </td>
      <td>Immettere o mappare l'ID del gateway che si desidera utilizzare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Dataset]

Questo modulo di azione elimina un set di dati.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il set di dati da eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del set di dati da eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo proprietario del set di dati da eliminare.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dataset]

Questo modulo di azione recupera i metadati di un set di dati specificato.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Seleziona o mappa l’opzione per scegliere il rapporto per il quale desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Inserisci o mappa l’ID del set di dati per il quale desideri recuperare i metadati.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartiene il set di dati per il quale desideri recuperare i metadati.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Datasets]

Questo modulo di ricerca recupera un elenco di set di dati.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Seleziona o mappa l’ID del gruppo a cui appartiene il rapporto per il quale desideri recuperare i metadati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>
        <p>Immettere o mappare il numero massimo di record che si desidera vengano inseriti nel modulo in [action] durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Refresh a Dataset]

Questo modulo di azione aggiorna un set di dati specificato.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a dataset]</td>
      <td>Seleziona o mappa l’opzione per selezionare il set di dati da aggiornare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Immetti o mappa l’ID del set di dati da aggiornare.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Immettere o mappare il nome della tabella contenente le righe che si desidera aggiungere o eliminare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Inserisci o mappa l’ID del gruppo proprietario del set di dati.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Notify Option]  </td>
      <td>
        <p>Seleziona o mappa l’opzione per la notifica:</p>
        <ul>
          <li>
            <p>[!UICONTROL Mail on Completion]</p>
          </li>
          <li>
            <p>[!UICONTROL Mail on Failure]</p>
          </li>
          <li>
            <p>[!UICONTROL No Notification]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### App

* [Ottieni un’app](#get-an-app)
* [Ottieni dashboard di un’app](#get-an-apps-dashboard)
* [Ottenere un rapporto dell’app](#get-an-apps-report)
* [Elencare dashboard dell’app](#list-apps-dashboards)
* [Elencare i rapporti dell’app](#list-apps-reports)
* [Elenca app](#list-apps)
* [Guarda le app](#watch-apps)

#### [!UICONTROL Get an App]

Questo modulo di azione recupera i metadati di un’app specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Seleziona o mappa l’ID dell’app da recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Dashboard]

Questo modulo di azione recupera i metadati del dashboard di un’app specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Seleziona o mappa l’ID dell’app che contiene il dashboard da recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Seleziona o mappa l’ID del dashboard che desideri recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Report]

Questo modulo di azione recupera i metadati del rapporto di un’app specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Seleziona o mappa l’ID dell’app che contiene il rapporto da recuperare.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Seleziona o mappa l’ID del rapporto che desideri recuperare.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Apps]

Questo modulo di ricerca recupera un elenco di tutte le app installate.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Dashboards]

Questo modulo di ricerca recupera un elenco di dashboard da un’app specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Seleziona o mappa l’ID dell’app da cui desideri elencare le dashboard.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Reports]

Questo modulo di ricerca recupera un elenco di tutti i rapporti dall’app specificata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Seleziona o mappa l’ID dell’app da cui desideri elencare i rapporti.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Apps]

Questo modulo di attivazione avvia uno scenario quando un’app viene aggiornata.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p>
      </td>
    </tr>
  </tbody>
</table>

### Altro

#### [!UICONTROL Make an API Call]

Questo modulo di azione esegue una chiamata API all&#39;API [!DNL Power BI].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Power BI] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Immettere un percorso relativo a <code>https://api.powerbi.com</code>. Esempio: <code>/v1.0/myorg/datasets</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
        <p>Selezionare il metodo di richiesta [!UICONTROL HTTP] necessario per configurare la chiamata API. Per ulteriori informazioni, vedere Metodi di richiesta [!UICONTROL HTTP].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione e le intestazioni x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
