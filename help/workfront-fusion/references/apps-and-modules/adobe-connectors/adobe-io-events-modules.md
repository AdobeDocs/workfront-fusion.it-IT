---
title: Moduli Adobe I/O Events
description: Con i moduli Adobe I/O Events puoi avviare uno scenario Adobe Workfront Fusion basato sugli eventi nelle applicazioni Adobe.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 44%

---

# Moduli Adobe I/O Events

Con i moduli Adobe I/O Events, puoi avviare uno scenario Adobe Workfront Fusion basato su eventi negli account e nei servizi Adobe che non dispongono di un connettore Workfront Fusion dedicato.

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

## Prerequisiti

Prima di poter utilizzare il connettore Adobe I/O Events, è necessario assicurarsi che siano soddisfatti i seguenti prerequisiti:

* Devi disporre di un account Adobe attivo.

## Informazioni API di Adobe I/O Events

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

## Creare una connessione a Adobe I/O Events

Per creare una connessione per i moduli Adobe I/O Events:

1. Fai clic su Aggiungi accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Ambiente</td>
        <td>
          <p>Seleziona se desideri connetterti a un ambiente di produzione o non di produzione.</p>
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

Quando configuri i moduli [!DNL Adobe I/O Events], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Adobe I/O Events], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Trigger](#triggers)
* [Azioni](#actions)
* [Ricerche](#searches)

### Trigger

#### Creare una registrazione evento

Questo modulo di azione utilizza un webhook per creare una descrizione dell’evento. Puoi configurare un webhook qui. Se utilizzi un webhook esistente, i campi in questo modulo sono di sola lettura.

Per creare un webhook:

1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Compila i seguenti campi:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Nome webhook]</td>
        <td>Specifica un nome per il webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connessione]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], consulta <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Descrizione webhook]
         </td>
         <td>
           Immettere una descrizione per il webhook.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event Provider]
         </td>
         <td>
           Seleziona il prodotto o l’account da cui desideri creare gli eventi.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Tipo evento]
         </td>
         <td>
           Seleziona gli eventi che desideri che il webhook guardi. Lo scenario si attiva quando si verificano questi eventi.
         </td>
       </tr>
     </tbody>
   </table>

1. Fai clic su Salva per salvare il webhook e tornare al modulo.

### Azioni

* [Ottieni ID provider ed evento](#get-provider-and-event-ids)
* [Effettua chiamata API personalizzata](#make-a-custom-api-call)

#### Ottieni ID provider ed evento

Questo modulo di ricerca ottiene gli ID Adobe I/O Events per il provider e gli eventi specificati.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connessione]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], consulta <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event Provider]
         </td>
         <td>
           Seleziona il provider per il quale desideri recuperare l’ID.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Tipo evento]
         </td>
         <td>
              Seleziona gli eventi per i quali desideri fornire gli ID. Gli eventi sono disponibili in base al provider di eventi. 
         </td>
       </tr>
     </tbody>
   </table>


#### Effettua chiamata API personalizzata

Questo modulo di azione effettua una chiamata API personalizzata all&#39;API [!DNL Adobe I/O Events]

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connessione]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], consulta <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Percorso]</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Metodo]</p>
      </td>
      <td>
  <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Intestazioni]</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione e le intestazioni di x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stringa di query]  </td>
      <td>
        <p>Inserisci la stringa di query della richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Corpo]</td>
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Ricerche

#### Ottieni tutti gli eventi da un giornale di registrazione

Questo modulo di ricerca recupera tutti gli eventi per una registrazione da un giornale di registrazione.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connessione]</td>
        <td>Per istruzioni sulla creazione di una connessione a [!DNL Adobe I/O Events], consulta <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Creare una connessione a [!DNL Adobe I/O Events]</a> in questo articolo.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL ID registrazione]
         </td>
         <td>
           Seleziona la registrazione per la quale desideri recuperare gli eventi.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Numero massimo di eventi restituiti]
         </td>
         <td>
              Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Restituisce eventi che si verificano dopo]
         </td>
         <td>Immettere o mappare una data. Il modulo restituisce eventi che si sono verificati dopo tale data.
         </td>
       </tr>
<!--
<tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
-->
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

Osserva eventi

Questo modulo di attivazione avvia uno scenario quando si verifica un evento nel prodotto o servizio Adobe scelto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fai clic su <b>Aggiungi</b> accanto al campo webhook.</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Origine degli eventi che si desidera visualizzare</li></ul></li><li>Fai clic su <b>Salva</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

-->
