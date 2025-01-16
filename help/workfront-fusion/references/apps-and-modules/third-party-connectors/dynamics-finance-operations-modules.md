---
title: Moduli finanziari e operativi di Microsoft Dynamics 365
description: In uno scenario  [!DNL Adobe Workfront Fusion] , è possibile automatizzare i flussi di lavoro che utilizzano Microsoft Dynamics 365 Finance and Operations, nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft Dynamics 365] e collegarlo a più applicazioni e servizi di terze parti.

>[!NOTE]
>
>Il connettore [!DNL Microsoft Dynamics 365 Finance and Operations] non supporta [!DNL Dynamics 365].
>
>Per i moduli di Microsoft Dynamics 365, vedere [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Creare una connessione

Per creare una connessione per i moduli Finanza e Operazioni di Microsoft Dynamics 365:

1. In qualsiasi modulo Microsoft Dynamics 365 Finance and Operations, fare clic su **[!UICONTROL Add]** accanto alla casella Connection.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Specificare se si sta creando una connessione standard di Dynamics Finance e Operations o una connessione utilizzando un codice di autorizzazione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Immettere Dynamics Finance e Operations [!UICONTROL Client ID].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Immettere Dynamics Finance e Operations [!UICONTROL Client Secret]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>Immettere l'ID tenant di Dynamics Finance e Operations.</td>
        </tr>
        <tr>
        <td role="rowheader">Risorsa</td>
        <td>Immetti l’URL dell’account Dynamics Finance and Operations (senza https://)</td>
        </tr>
      </tbody>
    </table>

1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.



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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a [!DNL Workfront Fusion], vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera creare.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a [!DNL Workfront Fusion], vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera eliminare.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> I campi Chiave primaria identificano l'elemento. Per ogni campo chiave primaria che si desidera fornire, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la chiave e il valore univoci che identificano l'elemento. </td> 
  </tr> 
 </tbody> 
</table>

### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API Dynamics Finance and Operations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a [!DNL Workfront Fusion], vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Immettere un percorso relativo all'URL di Dynamics Finance e Operations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> {"Content-type":"application/json"}</code></p> <p>Nota: se ricevi errori ed è difficile determinarne l'origine, puoi modificare le intestazioni in base alla documentazione di [!DNL Workfront]. Se la chiamata API personalizzata restituisce un errore di richiesta HTTP 422, provare a utilizzare un'intestazione <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> <p>Suggerimento: è consigliabile inviare informazioni tramite il corpo JSON anziché come parametri di query.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a [!DNL Workfront Fusion], vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera leggere.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
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
    <td>[!UICONTROL Connection]</td>
    <td> <p>Per istruzioni sulla connessione di Microsoft Dynamics 365 Finance and Operations a [!DNL Workfront Fusion], vedere <a href="#create-a-connection" class="MCXref xref">Creare una connessione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations da aggiornare.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> I campi Chiave primaria identificano l'elemento. Per ogni campo chiave primaria che si desidera fornire, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la chiave e il valore univoci che identificano l'elemento. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
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
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL Workfront] a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>Immettere o mappare il tipo di entità Dynamics Finance and Operations che si desidera cercare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Immettere il campo in base al quale si desidera eseguire la ricerca, l'operatore che si desidera utilizzare nella query e il valore ricercato nel campo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
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
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
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
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of [!DNL Workfront] record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to [!DNL Workfront] logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
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
