---
filename: workday-modules
title: Moduli Workday
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Workday], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: 5967d83107337e6567c0bb3974ba4047ed520f11
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 52%

---

# Moduli [!DNL Workday]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Workday], nonché collegarli a più applicazioni e servizi di terze parti.

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
   <td><pre><code>https://&#123;&#123;connection.servicesUrl&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Connettere [!DNL Workday] a Workfront Fusion

1. In qualsiasi modulo di Workfront Fusion, fai clic su [!UICONTROL Aggiungi] accanto al campo [!UICONTROL Connessione]

2. Compila i seguenti campi:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</p>
                </td>
                <td>Specifica un nome per la connessione.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>Immettere l'indirizzo dell'host [!DNL Workday] senza <code>https://</code>. Ad esempio: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL URL servizi]</td>
                <td>Immettere l'indirizzo dei servizi Web [!DNL Workday] senza <code>https://</code>. Ad esempio: <code>mycompany-services.workday.com</code>.</td>
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
                <td  role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
                <td>Immettere il segreto client per l'applicazione [!DNL Workday] utilizzata dalla connessione. Otteni questo risultato quando crei l'applicazione in [!DNL Workday].</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Session timeout (min)]</td>
                <td >Immetti il numero di minuti dopo i quali scade il token di autorizzazione.</td>
            </tr>
        </tbody>
    </table>


3. Fai clic su [!UICONTROL Continua] per salvare la connessione e tornare al modulo

## Moduli [!DNL Workday] e relativi campi

Quando configuri i moduli [!DNL Workday], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Workday], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azione](#action)

* [Ricerca](#search)


### Azione

* [[!UICONTROL Crea un record]](#create-a-record)

* [[!UICONTROL Eliminare un record]](#delete-a-record)

* [[!UICONTROL Effettua chiamata API personalizzata]](#make-a-custom-api-call)

* [[!UICONTROL Aggiorna un record]](#update-a-record)


#### [!UICONTROL Crea un record]

Questo modulo di azione crea un singolo record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connessione]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Seleziona il tipo di ambiente da creare.</td>
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
            <td role="rowheader">[!UICONTROL Connessione]</td>
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


### [!UICONTROL Effettua chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Workday]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Workday].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

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
   <td>Inserisci un percorso relativo a <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Aggiorna un record]

Questo modulo di azione aggiorna un singolo record in [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connessione]</td>
            <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >[!UICONTROL Connetti [!DNL Workday] a Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Tipo di record]</td>
            <td>Selezionare il tipo di record da aggiornare.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Inserisci oppure mappa l’ID del record da aggiornare.</td>
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
            <td role="rowheader">[!UICONTROL Connessione]</td>
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
              <td role="rowheader">[!UICONTROL Connessione]</td>
              <td>Per istruzioni sulla connessione dell'account [!DNL Workday] a Workfront Fusion, vedere <a href="#Connect" class="MCXref xref" >Connessione di [!DNL Workday] a Workfront Fusion</a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Tipo di record]</td>
              <td>Selezionare il tipo di record da recuperare.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Limite]</td>
              <td >
                  <p>Immettere o mappare il numero massimo di record che il modulo deve recuperare durante ogni ciclo di esecuzione dello scenario.</p>
              </td>
          </tr>
      </tbody>
  </table>
