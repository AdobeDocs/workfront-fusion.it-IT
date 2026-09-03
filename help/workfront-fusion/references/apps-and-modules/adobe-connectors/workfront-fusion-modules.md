---
title: Moduli Workfront Fusion
description: Con il connettore Workfront Fusion, puoi gestire la tua organizzazione Fusion dall’interno di uno scenario, inclusi record, hook, scenari e connessioni.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 1665553df806ba49ee9b52199fdcc587a5bb6337
workflow-type: tm+mt
source-wordcount: 1374
ht-degree: 21%

---

# Moduli Workfront Fusion

Con il connettore Workfront Fusion, puoi gestire la tua organizzazione Fusion dall’interno di uno scenario. A differenza di altri connettori, che collegano Fusion a un’app o a un servizio di terze parti, questo connettore consente a una chiamata di scenario dell’API di Fusion, in modo simile a come il connettore Adobe Workfront consente a uno scenario di gestire Workfront.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Collegare Workfront Fusion a Workfront Fusion

1. In qualsiasi modulo di Workfront Fusion, fai clic su **[!UICONTROL Aggiungi]** accanto al campo Connessione.
1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td> 
      <td>Selezionare il tipo di connessione da creare.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td> 
      <td>Specifica un nome per la connessione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID client]</td> 
      <td>Inserisci il tuo [!UICONTROL Client ID] [!DNL Adobe]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td> 
      <td>Inserisci il tuo [!UICONTROL Client Secret] (Segreto client) [!DNL Adobe]. Questo è disponibile nella sezione dei dettagli [!UICONTROL Credentials] di [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID organizzazione]</td> 
      <td>Immetti l'ID organizzazione IMS [!DNL Adobe].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Region]</td> 
      <td>Selezionare l'area Fusion per la connessione.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## Moduli Workfront Fusion e relativi campi

Quando configuri i moduli di Workfront Fusion, Workfront Fusion visualizza i campi elencati di seguito. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Esporta](#export)
* [Varie](#misc)

### Azioni

* [Clona un record](#clone-a-record)
* [Crea un record](#create-a-record)
* [Elimina una decisione](#delete-a-record)
* [Elencare record](#list-records)
* [Leggi un record](#read-a-record)
* [Aggiorna un record](#update-a-record)

#### Clona un record

Questo modulo crea una copia del record specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Selezionare il tipo di record da clonare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID scenario</td> 
   <td> Inserisci o mappa l’ID dello scenario da clonare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Immetti o mappa un nome per il nuovo scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### Crea un record

Questo modulo crea un record con i dati specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Seleziona il tipo di ambiente da creare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> Immetti o mappa l’ID del team a cui appartiene questo record. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Immettere o mappare un nome per il nuovo record.</td> 
  </tr> 
 </tbody> 
</table>

#### Elimina una decisione

Questo modulo elimina un record specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Selezionare il tipo di record che si desidera eliminare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td>Immettere i valori per tutti gli altri campi. I campi disponibili dipendono dal tipo di record selezionato. </td> 
  </tr> 
 </tbody> 
</table>

#### Elencare record

Questo modulo restituisce un elenco di record impaginato utilizzando il paging basato su cursore e i filtri delle proprietà.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td>Selezionare il tipo di record di cui si desidera restituire un elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà</td> 
   <td>Per ogni filtro delle proprietà per cui si desidera restituire i risultati, fare clic su <b>Aggiungi elemento</b> e immettere il campo, l'operatore e il valore per cui si desidera filtrare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inizio</td> 
   <td>Immettere il percorso in cui si desidera avviare i risultati restituiti. Viene utilizzato per l’impaginazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire per ogni ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordina per</td> 
   <td>Selezionare il campo in base al quale ordinare i risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direzione</td> 
   <td>Seleziona se desideri ordinare i risultati in ordine crescente o decrescente.</td> 
  </tr> 
 </tbody> 
</table>

#### Leggi un record

Questo modulo recupera il record specificato

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Selezionare il tipo di record che si desidera eliminare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td>Immettere i valori per tutti gli altri campi. I campi disponibili dipendono dal tipo di record selezionato. </td> 
  </tr> 
 </tbody> 
</table>

#### Aggiorna un record

Aggiorna un record specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Selezionare il tipo di record da aggiornare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome</td> 
   <td> Immettere o mappare un nuovo nome per il record.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> Immetti o mappa l’ID del record da aggiornare. </td> 
  </tr> 
 </tbody> 
</table>

### Esporta

#### Esporta registri attività

Questo modulo esporta i registri attività.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di file</td> 
   <td>Selezionare il formato di file in cui si desidera esportare i registri.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà</td> 
   <td>Per ogni filtro delle proprietà per cui si desidera restituire i risultati, fare clic su <b>Aggiungi elemento</b> e immettere il campo, l'operatore e il valore per cui si desidera filtrare. Puoi anche filtrare in base all’esistenza o meno del campo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inizio</td> 
   <td>Immettere il percorso in cui si desidera avviare i risultati restituiti. Viene utilizzato per l’impaginazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire per ogni ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordina per</td> 
   <td>Selezionare il campo in base al quale ordinare i risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direzione</td> 
   <td>Seleziona se desideri ordinare i risultati in ordine crescente o decrescente.</td> 
  </tr> 
 </tbody> 
</table>

### Varie

* [Ottenere statistiche di coda per un hook](#get-queue-statistics-for-a-hook)
* [Ottieni dipendenze record](#get-record-dependencies)
* [Elencare scenari per una connessione](#list-scenarios-for-a-connection)
* [Elencare le aree geografiche e le organizzazioni di Fusion](#list-the-fusion-regions-and-organizations)

#### Ottenere statistiche di coda per un hook

Questo modulo restituisce le statistiche della coda per l&#39;hook specificato: il numero di eventi attualmente in coda, il limite di coda e se l&#39;hook è abilitato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  <tr> 
   <td role="rowheader">ID hook</td> 
   <td> Immetti o mappa l’ID dell’hook per il quale desideri restituire i dettagli.</td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni dipendenze record

Questo modulo ottiene le dipendenze del record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  <tr> 
   <td role="rowheader">Tipo di record</td> 
   <td> Selezionare il tipo di record per il quale si desidera recuperare le dipendenze. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID scenario</td> 
   <td> Immettere o mappare l'ID del record per il quale si desidera recuperare le dipendenze. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### Elencare scenari per una connessione

Questo modulo restituisce un elenco impaginato di scenari che fanno riferimento alla connessione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID connessione</td> 
   <td>Immetti o mappa l’ID della connessione per la quale desideri restituire gli scenari.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietà</td> 
   <td>Per ogni filtro delle proprietà per cui si desidera restituire i risultati, fare clic su <b>Aggiungi elemento</b> e immettere il campo, l'operatore e il valore per cui si desidera filtrare. Puoi anche filtrare in base all’esistenza o meno del campo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Inizio</td> 
   <td>Immettere il percorso in cui si desidera avviare i risultati restituiti. Viene utilizzato per l’impaginazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di record che il modulo deve restituire per ogni ciclo di esecuzione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ordina per</td> 
   <td>Selezionare il campo in base al quale ordinare i risultati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direzione</td> 
   <td>Seleziona se desideri ordinare i risultati in ordine crescente o decrescente.</td> 
  </tr> 
 </tbody> 
</table>

#### Elencare le aree geografiche e le organizzazioni di Fusion

Questo modulo restituisce l’ID di regione e organizzazione per ogni organizzazione Fusion a cui la connessione può accedere, in base alle credenziali e all’accesso nel profilo utente IMS delle credenziali utilizzate nella connessione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione di Workfront Fusion a Workfront Fusion, vedere <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connessione di Workfront Fusion a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
 </tbody> 
</table>

