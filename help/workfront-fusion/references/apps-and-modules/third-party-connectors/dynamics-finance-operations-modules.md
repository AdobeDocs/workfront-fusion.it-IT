---
title: Moduli finanziari e operativi di Microsoft Dynamics 365
description: In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano Microsoft Dynamics 365 Finance and Operations, nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
TQID: https://experienceleague.adobe.com/MSvJMXg8hyI8piqHpn1OnEPEoCcP1Tn-za1veFtHeIo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1147
ht-degree: 39%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft Dynamics 365], nonché collegarli a più applicazioni e servizi di terze parti.

>[!NOTE]
>
>Il connettore [!DNL Microsoft Dynamics 365 Finance and Operations] non supporta [!DNL Dynamics 365].
>
>Per i moduli di Microsoft Dynamics 365, vedere [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



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
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Creare una connessione

Per creare una connessione per i moduli Finanza e Operazioni di Microsoft Dynamics 365:

1. In qualsiasi modulo Microsoft Dynamics 365 Finance and Operations, fare clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type] (Tipo di connessione)</td>
        <td>
          <p>Specificare se si sta creando una connessione standard di Dynamics Finance e Operations o una connessione utilizzando un codice di autorizzazione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immettere l'ID client di Dynamics Finance and Operations .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Immettere Dynamics Finance and Operations [!UICONTROL Client Secret]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL ID tenant]</td>
        <td>Immettere l'ID tenant di Dynamics Finance e Operations.</td>
        </tr>
        <tr>
        <td role="rowheader">Risorsa</td>
        <td>Immetti l’URL dell’account Dynamics Finance and Operations (senza https://)</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.



## Moduli finanziari e operativi Microsoft Dynamics 365 e relativi campi

>[!IMPORTANT]
>
>Le entità dati disponibili tramite l’API F&amp;O di Dynamics 365 possono variare a seconda dell’istanza. Se non sai quali entità sono disponibili tramite l’API, è utile esaminare le entità nella tua istanza utilizzando l’endpoint &quot;data&quot;. L’endpoint &quot;data&quot; in Dynamics 365 Finance and Operations è l’URL principale per accedere ai servizi OData. Questo endpoint consente di interagire con varie entità dati esposte dal sistema utilizzando protocolli OData standard.
>
>Puoi recuperare queste entità utilizzando il modulo di chiamata API personalizzato.
>
><!--For more information -->



### Crea elemento entità

Questo modulo di azione crea un nuovo elemento entità in Microsoft Dynamics 365 Finance and Operations.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connessione]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a Workfront Fusion, vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera creare.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Corpo]</td>
     <td> <p>Immetti o mappa un corpo JSON contenente i dati da includere nel nuovo elemento entità.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Elimina elemento entità

Questo modulo di azione elimina un elemento entità da Dynamics Finance e Operations. L&#39;elemento è identificato dai relativi campi chiave primaria.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connessione]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a Workfront Fusion, vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera eliminare.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Campi chiave primaria]</td>
     <td> I campi Chiave primaria identificano l'elemento. Per ogni campo chiave primaria che si desidera fornire, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la chiave e il valore univoci che identificano l'elemento. </td> 
  </tr> 
 </tbody> 
</table>

### Effettua chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Dynamics Finance and Operations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a Workfront Fusion, vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Immettere un percorso relativo all'URL di Dynamics Finance e Operations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Questo determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> <p>Nota: se vengono restituiti errori ed è difficile determinarne l’origine, prendi in considerazione la modifica delle intestazioni in base alla documentazione di Workfront. Se la chiamata API personalizzata restituisce un errore di richiesta HTTP 422, prova a utilizzare un’intestazione <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> <p>Suggerimento: è consigliabile inviare informazioni tramite il corpo JSON anziché come parametri di query.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>



### Leggi elemento entità

Questo modulo di azione restituisce dati da un elemento entità. L&#39;elemento è identificato dai relativi campi chiave primaria.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connessione]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a Workfront Fusion, vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera leggere.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Campi chiave primaria]</td>
     <td> I campi Chiave primaria identificano l'elemento. Per ogni campo chiave primaria che si desidera fornire, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la chiave e il valore univoci che identificano l'elemento. </td> 
  </tr> 
 </tbody> 
</table>

### Aggiorna elemento entità

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connessione]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a Workfront Fusion, vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations da aggiornare.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Campi chiave primaria]</td>
     <td> I campi Chiave primaria identificano l'elemento. Per ogni campo chiave primaria che si desidera fornire, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la chiave e il valore univoci che identificano l'elemento. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Corpo]</td>
     <td> <p>Immetti o mappa un corpo JSON contenente i dati da includere nel nuovo elemento entità.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerca

Questo modulo di ricerca restituisce i risultati in base ai criteri specificati.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell’app Workfront a Workfront Fusion, consulta <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connettere Workfront a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera cercare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteri di ricerca]</td> 
   <td> <p>Inserisci il campo in base al quale desideri eseguire la ricerca, l’operatore da utilizzare nella query e il valore ricercato nel campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Ordina per]</td> 
   <td> <p>Immettere o mappare il campo in base al quale ordinare i risultati.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
