---
title: Moduli Box
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Box e collegarlo a più applicazioni e servizi di terze parti. controlla una cartella specificata per verificare la presenza di modifiche ai file, modificare ed eliminare file esistenti o caricare nuovi file in una cartella.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Moduli Box

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Box] e collegarlo a più applicazioni e servizi di terze parti. controlla una cartella specificata per verificare la presenza di modifiche ai file, modificare ed eliminare file esistenti o caricare nuovi file in una cartella.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Prerequisiti

Per utilizzare i moduli [!DNL Box], è necessario disporre di un account [!DNL Box].

## Casella informazioni API

Il connettore Box utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] moduli e relativi campi

Quando configuri [!DNL Box] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Box], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)

### Trigger

* [[!UICONTROL Nuovo evento]](#new-event)
* [[!UICONTROL File di controllo]](#watch-files)

#### [!UICONTROL Nuovo evento]

Questo modulo di attivazione immediata avvia uno scenario quando un file viene aggiunto, spostato, copiato, eliminato, bloccato o sbloccato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Seleziona il webhook che desideri utilizzare per guardare i messaggi in uscita. Per aggiungere un webhook, fare clic su <strong>[!UICONTROL Add]</strong> e immettere il nome e la connessione del webhook.</p> <p> Per istruzioni sulla connessione dell'account [!UICONTROL Box] a [!UICONTROL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connessione a un servizio - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Numero massimo di eventi restituiti]</p> </td> 
   <td> <p>Immettere il numero massimo di eventi che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL File di controllo]

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un nuovo file o un file esistente viene aggiornato in una cartella controllata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Cartella</td> 
   <td> <p>Seleziona la cartella da controllare. Uno scenario può guardare una singola cartella.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Osserva</td> 
   <td> <p>Selezionare il tipo di file che si desidera controllare.</p> 
    <ul> 
     <li> <p><strong>Solo i nuovi file</strong> </p> <p>Lo scenario inizierà quando viene aggiunto un nuovo file.</p> </li> 
     <li> <p><strong>Nuovi file e tutte le modifiche</strong> </p> <p>Lo scenario inizia quando viene aggiunto un file o quando viene modificato il contenuto del file o un attributo del file (come il nome).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Numero massimo di file scaricati</p> </td> 
   <td> <p>Immettere il numero massimo di file che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Eliminare un file]](#delete-a-file)
* [[!UICONTROL Ottieni un file]](#get-a-file)
* [[!UICONTROL Aggiorna un file]](#update-a-file)
* [[!UICONTROL Carica] un file](#upload-a-file)

#### [!UICONTROL Eliminare un file]

Questo modulo di azione elimina un file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Immetti o mappa l’ID univoco del file che desideri eliminare dal modulo.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un file]

Questo modulo di azione scarica un file.

Specifica l’ID del file.

>[!NOTE]
>
>Questo modulo è utile per fornire file ai moduli successivi.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Immetti o mappa l’ID univoco del file che desideri che il modulo recuperi.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un file]

Questo modulo di azione aggiorna un file.

Specifica l’ID del file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td>Immetti o mappa l’ID univoco del file che desideri aggiornare il modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un file]

Questo modulo di azione carica un file.

Specificare il file. È inoltre possibile specificare un nuovo nome per il file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Box] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Seleziona la cartella in cui desideri caricare il file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Se questo modulo non ha esito positivo, considera quanto segue:
>
>* La dimensione del file potrebbe superare il limite massimo per la dimensione del file per il piano [!DNL Box] oppure è possibile che sia stata utilizzata tutta la quota di archiviazione dell&#39;account [!DNL Box]. Per ottenere più spazio di archiviazione, eliminare i file esistenti da [!DNL Box] o aggiornare l&#39;account [!DNL Box].
>* [!DNL Box] non carica più di un file con lo stesso nome in una singola cartella. Se la cartella di destinazione contiene un file con lo stesso nome di quello in fase di caricamento, l’esecuzione dello scenario termina con un errore. Per evitare questo problema, rinomina il file. Se si desidera aggiornare il file, utilizzare il modulo **[!UICONTROL Aggiorna file]**.
