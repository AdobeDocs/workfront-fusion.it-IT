---
title: Moduli Eventi Adobe I/O
description: Con i moduli Adobe I/O Events, puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nelle applicazioni Adobe.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 1%

---

# Moduli Eventi Adobe I/O

Con i moduli Adobe I/O Events, puoi avviare uno scenario Adobe Workfront Fusion basato su eventi negli account e nei servizi di Adobe che non dispongono di un connettore Workfront Fusion dedicato.

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Piano Adobe Workfront*</td> 
   <td> <p>Pro o superiore</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront*</td> 
   <td> <p>Piano, Lavoro</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td> <p>Workfront Fusion per l'automazione e l'integrazione del lavoro </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>Per utilizzare le funzionalità descritte in questo articolo, la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront.</td> 
  </tr> 
 </tbody> 
</table>

&#42;Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore di Workfront.

&#42;&#42;Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Prerequisiti

Prima di poter utilizzare il connettore Adobe I/O Events, è necessario assicurarsi che siano soddisfatti i seguenti prerequisiti:

* Devi disporre di un account Adobe attivo.

## Informazioni API per eventi di Adobe I/O

Il connettore Adobe I/O Events utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione a eventi Adobe I/O

Per creare una connessione per i moduli Adobe I/O Events:

1. Fare clic su Aggiungi accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Specificare se si desidera connettersi a un account di servizio o a un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Ambiti aggiuntivi</td>
        <td>Per aggiungere altri ambiti, fare clic su <b>Aggiungi elemento</b> e immettere l'ambito.</td>
      </tr>
      <tr>
        <td role="rowheader">ID client</td>
        <td>Immetti l'ID client di Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
      </tr>
      <tr>
        <td role="rowheader">Segreto client</td>
        <td>Immetti il segreto client di Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">ID organizzazione consumatore</td>
        <td>Immetti l'ID organizzazione consumer. Questo si trova nell’URL delle credenziali del progetto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">ID credenziali</td>
        <td>Immetti l'ID delle credenziali. Questo si trova nell’URL delle credenziali del progetto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">ID organizzazione IMS</td>
        <td>Immetti l'ID organizzazione Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
      </tr>
        <tr>
        <td role="rowheader">ID progetto</td>
        <td>Inserisci l'ID progetto. Questo si trova nell’URL delle credenziali del progetto: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">ID WORKSPACE</td>
        <td>Per visualizzare il Workspace ID del progetto, scarica i dettagli del progetto dalla pagina di panoramica del progetto in Adobe Developer Console. </td>
      </tr>
    </tbody>
    </table>

1. Fai clic su **Continua** per salvare la connessione e tornare al modulo.

## Moduli Adobe I/O Events e relativi campi

Quando configuri [!DNL Adobe I/O Events] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Adobe I/O Events], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Triggers

#### Creare una registrazione evento

Questo modulo di azione utilizza un webhook per creare una descrizione dell’evento. Puoi configurare un webhook qui. Se utilizzi un webhook esistente, i campi in questo modulo sono di sola lettura.

Per creare un webhook:

1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Compila i campi seguenti:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>Immettere un nome per il webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], vedere <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook description]
         </td>
         <td>
           Immettere una descrizione per il webhook.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Seleziona il prodotto o l’account da cui desideri creare gli eventi.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
           Seleziona gli eventi che desideri che il webhook guardi. Lo scenario si attiva quando si verificano questi eventi.
         </td>
       </tr>
     </tbody>
   </table>

1. Fai clic su Salva per salvare il webhook e tornare al modulo.

### Azioni

#### Ottieni tutti gli eventi da un giornale di registrazione

Questo modulo di ricerca recupera tutti gli eventi per una registrazione da un giornale di registrazione.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], vedere <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Registration ID]
         </td>
         <td>
           Seleziona la registrazione per la quale desideri recuperare gli eventi.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Maximum number of returned records]
         </td>
         <td>
              Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Return events that occur after]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Latest]
         </td>
         <td>
         Abilita questa opzione per restituire l’evento più recente.
         </td>
       </tr>
     </tbody>
   </table>

#### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata API personalizzata all&#39;API [!DNL Adobe I/O Events]

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], vedere <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
  <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione e le intestazioni di x-api-key.</p>
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

### Ricerche

#### Ottieni ID provider ed evento

Questo modulo di ricerca ottiene gli ID evento Adobe I/O per il provider e gli eventi specificati.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], vedere <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Seleziona il provider per il quale desideri recuperare l’ID.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
              Seleziona gli eventi per i quali desideri fornire gli ID. Gli eventi sono disponibili in base al provider di eventi. 
         </td>
       </tr>
     </tbody>
   </table>

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->