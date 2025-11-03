---
filename: workday-modules
title: Moduli Workday
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Workday], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 1%

---

# [!DNL Workday] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Workday] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Workday], è necessario:

* Avere un account [!DNL Workday].

* Creare un&#39;applicazione OAuth in [!DNL Workday]. Per istruzioni, vedere la documentazione di [!DNL Workday].

## Informazioni API di Workday

Il connettore Workday utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td>https://{{connection.servicesUrl}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Workday] a Workfront Fusion

1. In qualsiasi modulo di Workfront Fusion, fai clic su [!UICONTROL Aggiungi] accanto al campo [!UICONTROL Connessione]

2. Compila i campi seguenti:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Nome connessione]</p>
                </td>
                <td>Immettere un nome per la connessione.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>Immettere l'indirizzo dell'host [!DNL Workday] senza <code>https://</code>. Esempio: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL URL servizi]</td>
                <td>Immettere l'indirizzo dei servizi Web [!DNL Workday] senza <code>https://</code>. Esempio: <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Nome tenant]</td>
                <td>Immettere il tenant per l'account [!DNL Workday]. Il tenant è l'identificatore dell'organizzazione ed è visibile nell'URL utilizzato per accedere a Workday. Esempio: nell'indirizzo <code>https://www.myworkday.com/mycompany</code>, il tenant è <code>mycompany</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL ID client]</td>
                <td>Immettere l'ID client per l'applicazione [!DNL Workday] utilizzata da questa connessione. Otteni questo risultato quando crei l'applicazione in [!DNL Workday].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Segreto client]</td>
                <td>Immettere il segreto client per l'applicazione [!DNL Workday] utilizzata dalla connessione. Otteni questo risultato quando crei l'applicazione in [!DNL Workday].</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Session timeout (min)]</td>
                <td >Immetti il numero di minuti dopo i quali scade il token di autorizzazione.</td>
            </tr>
        </tbody>
    </table>


3. Fai clic su [!UICONTROL Continua] per salvare la connessione e tornare al modulo

## [!DNL Workday] moduli e relativi campi

Quando si configurano [!DNL Workday] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Workday], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azione](#action)

* [Ricerca](#search)


### Azione

* [[!UICONTROL Crea un record]](#create-a-record)

* [[!UICONTROL Eliminare un record]](#delete-a-record)

* [[!UICONTROL Effettuare una chiamata API personalizzata]](#make-a-custom-api-call)

* [[!UICONTROL Aggiorna un record]](#update-a-record)


#### [!UICONTROL Crea un record]

Questo modulo di azione crea un singolo record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Selezionare il tipo di record da creare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Inserisci o mappa l’ID del record che desideri creare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID sottorisorsa]</td>
            <td >Immetti o mappa l’ID della risorsa secondaria da creare.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Eliminare un record]

Questo modulo di azione elimina un singolo record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Selezionare il tipo di record che si desidera eliminare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Tipo di record specifico]</td>
            <td>Selezionare il tipo di record specifico che si desidera eliminare. Questi sono basati sul tipo di record scelto.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL ID sottorisorsa]</td>
            <td>Immetti o mappa l’ID della risorsa secondaria da eliminare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Immettere o mappare l'ID del record che si desidera eliminare.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL Effettuare una chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Workday]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Workday].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

Il modulo restituisce il codice di stato a, insieme alle intestazioni e al corpo della chiamata API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un singolo record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >[!UICONTROL Connetti [!DNL Workday] a Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Selezionare il tipo di record da aggiornare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Immetti o mappa l’ID del record da aggiornare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID sottorisorsa]</td>
            <td >Immetti o mappa l’ID della risorsa secondaria da aggiornare.</td>
        </tr>
    </tbody>
</table>

### Ricerca

* [[!UICONTROL Leggi un record]](#read-a-record)

* [[!UICONTROL Elenca record]](#list-records)


#### [!UICONTROL Leggi un record]

Questo modulo di azione legge un singolo record.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >[!UICONTROL Connetti [!DNL Workday] a Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Selezionare il tipo di record che si desidera eliminare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Tipo di record specifico]</td>
            <td>Selezionare il tipo di record specifico che si desidera leggere. Questi sono basati sul tipo di record scelto.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Immettere o mappare l'ID del record che si desidera eliminare.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Elenca record]

Questo modulo di ricerca recupera un elenco di record del tipo specificato.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Connection]</td>
              <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Tipo di record]</td>
              <td>Selezionare il tipo di record da recuperare.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Limit]</td>
              <td >
                  <p>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</p>
              </td>
          </tr>
      </tbody>
  </table>
