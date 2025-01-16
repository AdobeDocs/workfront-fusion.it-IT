---
title: Moduli Adobe Journey Optimizer
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Adobe Journey Optimizer], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '3276'
ht-degree: 0%

---

# [!DNL Adobe Journey Optimizer] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Journey Optimizer] e collegarlo a più applicazioni e servizi di terze parti. I moduli [!DNL Adobe Journey Optimizer] consentono di creare, leggere, aggiornare o eliminare record oppure di eseguire una chiamata API personalizzata all&#39;API [!DNL Adobe Journey Optimizer].


Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
      <td>
        <p>[!UICONTROL Pro] o superiore</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
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

+++

## Prerequisiti

Prima di poter utilizzare il connettore [!DNL Adobe Journey Optimizer], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Journey Optimizer] attivo.

## Informazioni API di Adobe Journey Optimizer

Il connettore Adobe Journey Optimizer utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>{{connection.url}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione a Adobe Journey Optimizer

Puoi creare una connessione in qualsiasi modulo di Adobe Journey Optimizer.

1. Fare clic su **[!UICONTROL Add]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Specificare se ci si connette a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL Client ID]. È disponibile nella sezione dei dettagli [!UICONTROL Credentials] della sezione [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione dei dettagli [!UICONTROL Credentials] della sezione [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Organization ID]. È disponibile nella sezione dei dettagli [!UICONTROL Credentials] della sezione [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Sandbox Name]</td>
        <td>Immetti il nome della sandbox che verrà utilizzata da questa connessione.</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## [!DNL Adobe Journey Optimizer] moduli e relativi campi

Quando configuri [!DNL Adobe Journey Optimizer] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe Journey Optimizer], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Gestione della configurazione](#configuration-management)
* [Gestione dei pacchetti](#package-management)
* [Gestione record](#record-management)
* [Gestione dei messaggi](#message-management)
* [Controlli di stato](#status-checks)
* [Ricerche](#searches)
* [Altro](#other)




### Gestione della configurazione

* [Creare una configurazione](#create-a-configuration)
* [Distribuire una configurazione](#deploy-a-configuration)
* [Aggiornare una configurazione](#update-a-configuration)
* [Annullare la distribuzione di una configurazione](#undeploy-a-configuration)
* [Verifica se la configurazione può essere distribuita](#check-if-configuration-can-be-deployed)
* [Eliminare una configurazione](#delete-a-configuration)
* [Ottieni una configurazione](#get-a-configuration)

#### Creare una configurazione

Questo modulo di azione crea un endpoint di limitazione o una configurazione di limitazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai creando una configurazione di limitazione o limitazione.<ul><li><p><b>Limiti</b></p>Passa a <a href="#capping-fields" class="MCXref xref" >Campi limite</a>.</li><li><p><b>Limitazione</b></p>Passa a <a href="#throttling-fields" class="MCXref xref" >Campi di limitazione</a>.</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### Campi limite

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Inserisci o mappa l’URL dell’endpoint da configurare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IMS Org ID]</td> 
   <td>Inserisci o mappa l’ID Adobe IMS dell’organizzazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>Selezionare i metodi da utilizzare in questa configurazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service]</td> 
   <td>Seleziona se utilizzi un’azione o un’origine dati per questa configurazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>Immettere o mappare il numero massimo di connessioni simultanee a questo endpoint.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>Immettere o mappare il numero massimo di chiamate da eseguire nel periodo specificato nel campo Periodo di tempo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time period (milliseconds)]</td> 
   <td>Immettere o mappare il numero di millisecondi relativi al campo Numero massimo di chiamate.</td> 
  </tr> 
 </tbody> 
</table>

##### Limitazione dei campi

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immetti o mappa un nome per questa configurazione.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immetti o mappa una descrizione per questa configurazione.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL URL pattern]</td> 
   <td>Immetti o mappa l’URL per l’endpoint da limitare.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>Selezionare i metodi da utilizzare in questa configurazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max throughput]</td> 
   <td>Seleziona se utilizzi un’azione o un’origine dati per questa configurazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>Immettere o mappare il numero massimo di connessioni simultanee a questo endpoint.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>Immetti o mappa il throughput massimo desiderato per questo endpoint. Questo valore deve essere compreso tra 200 e 5000.</td> 
  </tr> 
 </tbody> 
</table>

#### Distribuire una configurazione

Questo modulo di azione distribuisce la configurazione di limitazione o limitazione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai distribuendo una configurazione di limitazione o di limitazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Immetti o mappa l’ID della configurazione da distribuire.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare una configurazione

Questo modulo di azione aggiorna la configurazione di limitazione o limite specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai aggiornando una configurazione di limitazione o di limitazione.<ul><li><p><b>Limiti</b></p>Per i campi, vedi <a href="#capping-fields" class="MCXref xref" >Limitazione dei campi</a> nella sezione Creare una configurazione di questo articolo.</li><li><p><b>Limitazione</b></p>Per i campi, vedi <a href="#throttling-fields" class="MCXref xref" >Limitazione dei campi</a> nella sezione Creare una configurazione di questo articolo.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### Annullare la distribuzione di una configurazione

Questo modulo di azione annulla la distribuzione di una configurazione di limitazione o limitazione. Lo stato della configurazione viene ripristinato allo stato precedente alla distribuzione (`created` o `updated`).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai annullando la distribuzione di una configurazione di limitazione o di limitazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Immetti o mappa l’ID della configurazione di cui vuoi annullare la distribuzione.</td> 
  </tr> 
 </tbody> 
</table>

#### Verifica se la configurazione può essere distribuita

Questo modulo di azione verifica se è possibile distribuire una configurazione di limitazione o limitazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai controllando una configurazione di limite o una configurazione di limitazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Immetti o mappa l’ID della configurazione da controllare.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare una configurazione

Questo modulo di azione elimina un endpoint di limitazione o una configurazione di limitazione.

Se la configurazione è stata distribuita, è necessario annullarne la distribuzione prima di eliminarla.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai eliminando una configurazione di limitazione o di limitazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Inserisci o mappa l’ID della configurazione da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni una configurazione

Questo modulo di azione restituisce la configurazione di limitazione o limitazione identificata dall’ID specificato. Viene restituita la definizione più recente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se stai recuperando una configurazione di limite o una configurazione di limitazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Immetti o mappa l’ID della configurazione da recuperare.</td> 
  </tr> 
 </tbody> 
</table>




### Gestione dei pacchetti

* [Creare un pacchetto](#create-a-package)
* [Aggiornare un pacchetto](#update-a-package)
* [Eliminare un pacchetto](#delete-a-package)
* [Cercare un pacchetto](#look-up-a-package)
* [Importare un pacchetto](#import-a-package)
* [Publish un pacchetto](#publish-a-package)
* [Inviare un’importazione](#submit-an-import)



#### Creare un pacchetto

Questo modulo di azione crea un pacchetto con più artefatti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per il pacchetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione del pacchetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Immetti o mappa la marca temporale che definisce la data di scadenza per il pacchetto. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package type]</td> 
   <td>Seleziona il tipo di pacchetto da creare.<ul><li><p><b>Full</b></p>Il pacchetto includerà tutti gli artefatti</p></li><li><p><b>Parziale</b></p><p>Il pacchetto includerà solo gli artefatti aggiunti. </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>Se si sta creando un pacchetto parziale, per ogni artifact che si desidera aggiungere fare clic su <b>Aggiungi artifact</b> e specificare l'ID, il tipo e il titolo dell'artifact. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>Inserisci o mappa il Nome e l’ID dell’organizzazione IMS della sandbox che contiene gli elementi che desideri che il pacchetto contenga.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un pacchetto

Questo modulo di azione aggiunge o elimina gli artefatti da un pacchetto o aggiorna i metadati del pacchetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select action]</td> 
   <td>Seleziona l’azione da eseguire.<ul><li><p><b>Aggiungi artefatto</b></p><p>Per ogni artifact che si desidera aggiungere, fare clic su <b>Aggiungi artifact</b> e specificare l'ID, il tipo e il titolo dell'artifact, quindi immettere o mappare la data di scadenza del pacchetto. </p></li><li><p><b>Elimina artefatto</b></p><p>Per ogni elemento che si desidera eliminare, fare clic su <b>Aggiungi elemento</b> e specificare l'ID, il tipo e il titolo dell'elemento. </p></li><li><p><b>Aggiorna metadati</b></p><p>Immetti nuovi valori per il nome, la descrizione o l’ID dell’organizzazione IMS della sandbox di origine.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un pacchetto

Questo modulo di azione elimina un pacchetto con più artefatti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Cercare un pacchetto

Questo modulo di azione recupera i dettagli del pacchetto specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto per il quale desideri restituire i dettagli.</td> 
  </tr> 
 </tbody> 
</table>

#### Importare un pacchetto

Questo modulo di azione recupera gli oggetti in conflitto nella sandbox di destinazione specificata. Gli oggetti in conflitto rappresentano oggetti simili già presenti nella sandbox di destinazione.

È necessario pubblicare un pacchetto prima di poterlo importare.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto da importare.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Inserisci o mappa il nome della sandbox in cui desideri importare il pacchetto.</td> 
  </tr> 
 </tbody> 
</table>

#### Publish un pacchetto

È necessario pubblicare un pacchetto prima di poterlo importare.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto da pubblicare.</td> 
  </tr> 
 </tbody> 
</table>

#### Inviare un’importazione

Questo modulo di azione invia un&#39;importazione per un pacchetto dopo aver esaminato i conflitti e fornito le sostituzioni. Il risultato viene fornito come payload, che avvia il processo di importazione per la sandbox di destinazione come specificato nel payload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto da pubblicare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per il processo di importazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione del processo di importazione</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) Name]</td> 
   <td>Inserisci o mappa il nome della sandbox a cui stai inviando l’importazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) IMS Org ID]</td> 
   <td>Inserisci o mappa l’ID dell’organizzazione Adobe IMS per la sandbox a cui stai inviando l’importazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) ID]</td> 
   <td>Inserisci o mappa l’ID della sandbox che contiene il pacchetto da pubblicare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Type]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Link]</td> 
   <td>Immetti o mappa il collegamento per il pacchetto da pubblicare.</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### Gestione record

* [Creare un record](#create-a-record)
* [Aggiornare un record](#update-a-record)
* [Eliminare un record](#delete-a-record)
* [Applicazione di patch a un record](#patch-a-record)
* [Ottieni un record](#get-a-record)

#### Creare un record

Questo modulo di azione crea un nuovo modello di contenuto o un nuovo frammento di contenuto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se stai creando un modello di contenuto o un frammento di contenuto.<ul><li><p><b>Modello di contenuto</b></p>Passa a <a href="#template-fields" class="MCXref xref" >Campi modello</a>.</li><li><p><b>Frammento di contenuto</b></p>Passa a <a href="#fragment-fields" class="MCXref xref" >Campi frammento</a>.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### Campi modello

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per questo modello di contenuto.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione per questo modello di contenuto.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Seleziona il tipo di modello da creare.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>Seleziona i canali inclusi in questo modello.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content template origin]</td> 
   <td>Selezionare l'origine del modello.</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Per includere le proprietà personalizzate nel nuovo modello, seleziona "Aggiungi metadati" e immetti o mappa la chiave e il valore dei metadati. Ripetere l'operazione per ogni campo personalizzato che si desidera includere.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email HTML]</td> 
   <td>Inserisci o mappa il HTML dell’e-mail inclusa in questo modello.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>Per includere le proprietà personalizzate nell’e-mail, seleziona "Aggiungi contesto editor" e immetti o mappa la chiave e il valore del contesto. Ripetere l'operazione per ogni campo personalizzato che si desidera includere.</td> 
  </tr> 
 </tbody> 
</table>

##### Campi frammento

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Immetti o mappa un nome per questo frammento di contenuto.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Immetti o mappa una descrizione per questo frammento di contenuto.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Seleziona il tipo di modello da creare.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>Seleziona i canali inclusi in questo modello.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content fragment origin]</td> 
   <td>Seleziona l’origine del frammento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Per includere le proprietà personalizzate nel nuovo modello, seleziona "Aggiungi metadati" e immetti o mappa la chiave e il valore dei metadati. Ripetere l'operazione per ogni campo personalizzato che si desidera includere.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td>Inserisci o mappa il contenuto del frammento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>Per includere le proprietà personalizzate nell’e-mail, seleziona "Aggiungi contesto editor" e immetti o mappa la chiave e il valore del contesto. Ripetere l'operazione per ogni campo personalizzato che si desidera includere.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un record

Questo modulo di azione aggiorna un modello di contenuto o un frammento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se stai aggiornando una configurazione di limitazione o di limitazione.<ul><li><p><b>Modello</b></p>Per i campi, vedi <a href="#template-fields" class="MCXref xref" >Campi modello</a> nella sezione Creare un record di questo articolo.</li><li><p><b>Frammento</b></p>Per i campi, vedi <a href="#fragment-fields" class="MCXref xref" >Campi frammento</a> nella sezione Creare un record di questo articolo.</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### Eliminare un record

Questo modulo di azione elimina un modello di contenuto o un frammento di contenuto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se stai eliminando un modello di contenuto o un frammento di contenuto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Inserisci o mappa l’ID del modello o del frammento da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Applicazione di patch a un record

Questo modulo di azione aggiorna un record utilizzando PATCH con formato puntatore JSON

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se applicare la patch a un modello di contenuto o a un frammento di contenuto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Inserisci o mappa l’ID del modello o del frammento a cui desideri applicare la patch.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload data]</td> 
   <td>Per aggiungere un record al payload di questa patch: <ol><li>Fare clic su <b>Aggiungi un record</b>.</li><li>Selezionare l'operazione Aggiungi, Rimuovi o Sostituisci.</li><li>Nel campo Percorso, seleziona se desideri applicare la patch al nome o alla descrizione.</li><li> Nel campo Da, inserisci o mappa una stringa contenente un valore del puntatore JSON.</li><li>Nel campo Valore immettere il valore da utilizzare nell'operazione.</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### Ottieni un record

Questo modulo di azione restituisce il modello di contenuto o il frammento di contenuto identificato dall’ID specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se stai recuperando un modello di contenuto o un frammento di contenuto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Inserisci o mappa l’ID del modello o del frammento che desideri recuperare.</td> 
  </tr> 
 </tbody> 
</table>


### Gestione dei messaggi

* [Attivare l’esecuzione di un messaggio unitario](#trigger-a-unitary-message-execution)
* [Attivare un messaggio basato su pubblico](#trigger-an-audience-based-message)
* [Controllare lo stato di un messaggio basato su pubblico](#check-the-status-for-audience-based-message)



#### Attivare l’esecuzione di un messaggio unitario

Questo modulo di azione attiva un messaggio unitario ai destinatari specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>Immetti o mappa l’ID della richiesta associata a questo messaggio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Inserisci o mappa l’ID della campagna associata a questo messaggio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipients]</td> 
   <td>Per ogni destinatario che si desidera ricevere questo messaggio, fare clic su <b>Aggiungi destinatario</b> e immettere quanto segue:
   <ul>
   <li><p><b>Tipo</b></p>Selezionare <code>aep</code>.</li>
   <li><p><b>ID utente</b></p>Immetti o mappa l’identificatore del profilo Adobe Experience Platform del destinatario.</li>
   <li><p><b>Namespace</b></p>Inserisci o mappa il namespace del profilo Adobe Experience Platform del destinatario.</li>
   <li><p><b>Indirizzo e-mail</b></p></li>
   <li><p><b>Numero di telefono cellulare</b></p></li>
   <li><p><b>Nome</b></p></li>
   <li><p><b>Cognome</b></p></li>
   <li><p><b>Prodotto</b></p>Inserisci o mappa il prodotto associato a questo messaggio. Viene utilizzato per la sostituzione dinamica delle variabili nel contenuto del messaggio.</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### Attivare un messaggio basato su pubblico

Questo modulo di azione attiva l’esecuzione di un messaggio basato sul pubblico, in base alla richiesta e alla campagna specificate.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>Immetti o mappa l’ID della richiesta associata a questo messaggio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Inserisci o mappa l’ID della campagna associata a questo messaggio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Product]</td> 
   <td>Inserisci o mappa il prodotto associato a questo messaggio. Viene utilizzato per la sostituzione dinamica delle variabili nel contenuto del messaggio.</td> 
  </tr> 
 </tbody> 
</table>

#### Verifica lo stato del messaggio basato sul pubblico

Questo modulo di azione controlla lo stato di un messaggio batch basato su un pubblico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message execution ID]</td> 
   <td>Inserisci o mappa l’ID dell’esecuzione del messaggio che desideri controllare.</td> 
  </tr> 
 </tbody> 
</table>

### Controlli di stato

<!--* [Check service health](#check-service-health)-->
* [Controllare le dipendenze di importazione](#check-the-import-dependencies)
* [Controllare lo stato di un processo di importazione](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### Controllare le dipendenze di importazione

Questo modulo di azione controlla le dipendenze per gli artefatti del pacchetto. Ciò ti consente di verificare se disponi delle autorizzazioni necessarie per importare gli artefatti del pacchetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immetti o mappa l’ID del pacchetto di cui desideri verificare le autorizzazioni.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Inserisci o mappa il nome della sandbox in cui desideri importare il pacchetto.</td> 
  </tr> 
 </tbody> 
</table>

#### Controllare lo stato di un processo di importazione

Questo modulo di azione controlla se un processo di importazione ha avuto esito positivo o negativo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td>Immetti o mappa l’ID del processo per il quale desideri recuperare i dati.</td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

* [Elenca tutti gli oggetti dipendenti](#list-all-dependent-objects)
* [Configurazioni elenco](#list-configurations)
* [Elencare processi di esportazione e importazione](#list-export-and-import-jobs)
* [Elencare pacchetti](#list-packages)
* [Elencare record](#list-records)

#### Elenca tutti gli oggetti dipendenti

Questo modulo di ricerca elenca tutti gli oggetti dipendenti per gli oggetti nel pacchetto specificato

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package objects]</td> 
   <td>Per ogni oggetto del pacchetto per cui si desidera restituire l'oggetto dipendente, fare clic su <b>Aggiungi oggetto</b> e immettere il nome e il tipo dell'oggetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Immettere o mappare l'ID del pacchetto per il quale si desidera elencare gli oggetti dipendenti.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Inserisci o mappa il nome della sandbox che contiene il pacchetto per il quale desideri elencare gli oggetti dipendenti.</td> 
  </tr> 
 </tbody> 
</table>

#### Configurazioni elenco

Questo modulo di azione elenca tutte le configurazioni di limitazione o limitazione di limite.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Seleziona se desideri elencare le configurazioni di limite o di limitazione.</td> 
  </tr> 
 </tbody> 
</table>

#### Elencare processi di esportazione e importazione

Questo modulo di ricerca elenca i processi di esportazione e importazione correnti. Puoi utilizzare i parametri di query per filtrare l’elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>Seleziona se ordinare i risultati per data di creazione o data di modifica.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>Per ogni parametro di query in base al quale si desidera filtrare, fare clic su <b>Aggiungi parametro di query</b>, quindi selezionare il campo e l'operatore e immettere il valore del campo per il filtro.</td> 
  </tr> 
 </tbody> 
</table>



#### Elencare pacchetti

Questo modulo di ricerca elenca tutti i pacchetti dell’organizzazione. Puoi utilizzare i parametri di query per filtrare l’elenco.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>Seleziona se ordinare i risultati per data di creazione o data di modifica.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>Per ogni parametro di query in base al quale si desidera filtrare, fare clic su <b>Aggiungi parametro di query</b>, quindi selezionare il campo e l'operatore e immettere il valore del campo per il filtro.</td> 
  </tr> 
 </tbody> 
</table>

#### Elencare record

Questo modulo di ricerca elenca tutte le configurazioni di limitazione o limitazione dei limiti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Seleziona se stai recuperando un modello di contenuto o un frammento di contenuto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>Immettere o mappare il nome del parametro in base al quale si desidera ordinare l'elenco. Aggiungi <code>-</code> o <code>+</code> per ordinare in ordine decrescente o crescente. Se non viene specificato alcun segno, l'elenco viene ordinato in ordine decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Questo campo viene utilizzato per l’impaginazione. Immettere o mappare i criteri per la pagina successiva rispetto alla proprietà specificata nel campo Ordina per.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>Immettere o mappare il nome del parametro in base al quale si desidera ordinare l'elenco. Aggiungi <code>-</code> o <code>+</code> per ordinare in ordine decrescente o crescente. Se non viene specificato alcun segno, l'elenco viene ordinato in ordine decrescente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by property]</td> 
   <td>Per ogni filtro delle proprietà che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore della proprietà. I record che includono il valore specificato per la proprietà vengono inclusi nell'elenco.</td> 
  </tr> 
 </tbody> 
</table>


### Altro


#### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata API personalizzata all’API Adobe Journey Optimizer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe Journey Optimizer], vedere <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Creare una connessione a [!DNL Adobe Journey Optimizer]</a> in questo articolo.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Immetti un percorso relativo all’URL di base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] aggiunge automaticamente le intestazioni autorizzazione, <code>x-api-key</code> e <code>x-gw-ims-org-id</code>.</p>
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







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
