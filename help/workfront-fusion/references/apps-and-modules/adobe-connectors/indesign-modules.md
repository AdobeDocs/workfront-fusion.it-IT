---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Moduli Adobe InDesign
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe InDesign e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 20%

---


# Moduli Adobe InDesign

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe InDesign e collegarlo a più applicazioni e servizi di terze parti.

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

Prima di poter utilizzare il connettore Adobe InDesign, è necessario disporre di un account Adobe InDesign attivo.

## Creare una connessione ad Adobe InDesign

Per creare una connessione per i moduli Adobe InDesign:

1. In qualsiasi modulo di Adobe InDesign, fai clic su **Aggiungi** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
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
          <p>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Tipo</td>
        <td>
          <p>Specifica se ti connetti a un account di servizio o a un account personale.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">ID client</td>
          <td>Immetti l'ID client di Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Segreto client</td>
          <td>Immetti il segreto client di Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">ID organizzazione IMS</td>
          <td>Immetti l'ID organizzazione Adobe. Questo problema si trova nella sezione Dettagli credenziali di Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Fai clic su **Continue** (Continua) per salvare la connessione e tornare al modulo.

## Moduli InDesign e relativi campi

Quando configuri i moduli di Adobe InDesign, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di Adobe InDesign, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

* [Crea rappresentazione](#create-rendition)
* [Eliminare uno script personalizzato](#delete-a-custom-script)
* [Unisci dati](#merge-data)
* [Rimappare i collegamenti](#remap-links)
* [Inviare una richiesta di esecuzione di script personalizzata](#submit-a-custom-script-execution-request)

#### Crea rappresentazione

Questo modulo di azione crea e restituisce una rappresentazione JPEG, PNG o PDF di un documento InDesign specifico. Per la struttura di `StatusCompletedRespons/output/data`, fare riferimento a `RenditionOutputData`. Anche per l&#39;elenco dei possibili codici di errore in `FailedEvent` fare riferimento a `RenditionFailedData`.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Tipo</p>
      </td>
      <td>Selezionare il tipo di file della rappresentazione che si desidera creare. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa da aggiungere alla rappresentazione:<ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento di destinazione</td>
      <td>Immettere o mappare il documento che verrà elaborato e sottoposto a rendering. Attualmente è supportato un solo documento alla volta.</td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

#### Eliminare uno script personalizzato

Questo modulo di azione elimina un singolo script personalizzato registrato. Tutte le versioni dello script verranno rimosse definitivamente.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nome script</p>
      </td>
      <td>Immettere o mappare il nome dello script che si desidera eliminare.</td>
    </tr>
  </tbody>
</table>

#### Unisci dati

Questo modulo crea documenti o PDF InDesign unendo i dati CSV con i modelli InDesign. I formati di output includono documenti JPEG, PNG, PDF e InDesign.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa da aggiungere all’unione dati:<ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento di destinazione</td>
      <td>Immettere o mappare il documento che verrà utilizzato come modello per l'unione.</td>
    </tr>
    <tr>
      <td role="rowheader">Origine dati</td>
      <td>Immettere o mappare i file di origine da utilizzare.</td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

#### Rimappare i collegamenti

Questo modulo sostituisce i collegamenti basati su file nei documenti di InDesign con gli URL di Adobe Experience Manager (AEM). Può essere utile per lavorare con Adobe Experience Manager utilizzando Adobe Asset Link.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
      </tr>
    <tr>
      <td role="rowheader">Token AEM</td>
      <td>Immetti o mappa il token Bearer generato per l’account tecnico AEM, senza la parola chiave Bearer.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa da aggiungere al modulo:<ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento di destinazione</td>
      <td>Immettere o mappare il documento in cui si desidera rimappare i collegamenti.</td>
    </tr>
    <tr>
      <td role="rowheader">Origine dati</td>
      <td>Immetti o mappa i file sorgente da utilizzare per l’estrazione e la corrispondenza dei tag.</td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

#### Inviare una richiesta di esecuzione di script personalizzata

Questo modulo di azione invia una richiesta di esecuzione per uno script personalizzato. Puoi definire le risorse e i parametri di input che lo script personalizzato utilizzerà durante l’esecuzione.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>ID script</p>
      </td>
      <td>Inserisci o mappa l’ID dello script personalizzato.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa per la quale desideri inviare una richiesta di esecuzione: <ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

### Ricerche

* [Ottieni dettagli script personalizzati](#get-custom-script-details)
* [Ottieni tag unione dati](#get-data-merge-tags)
* [Ottieni informazioni documento](#get-document-information)
* [Elencare script personalizzati](#list-custom-scripts)

#### Ottieni dettagli script personalizzati

Questo modulo di ricerca recupera i dettagli di un singolo script personalizzato registrato, tra cui la versione, il collegamento per il download, la data di registrazione e il nome dello script.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nome script</p>
      </td>
      <td>Immettere o mappare il nome dello script per il quale si desidera recuperare i dettagli.</td>
    </tr>
  </tbody>
</table>

#### Ottieni tag unione dati

Questo modulo recupera i tag di unione dati da un documento.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa da aggiungere al modulo:<ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento di destinazione</td>
      <td>Immettere o mappare il documento da cui si desidera recuperare i tag.</td>
    </tr>
    <tr>
      <td role="rowheader">Origine dati</td>
      <td>Immetti o mappa i file sorgente da utilizzare per l’estrazione e la corrispondenza dei tag.</td>
    </tr>
    <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

#### Ottieni informazioni documento

Questo modulo recupera informazioni complete sui documenti INDD/IDML e restituisce dati in base ai tipi di informazioni abilitati specificati nella richiesta.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Risorse</p>
      </td>
      <td>Per ogni risorsa da aggiungere al modulo:<ol><li>Fare clic su <b>Aggiungi elemento</b>.</li><li>Seleziona o mappa l’origine della risorsa.</li><li>Immetti una destinazione. La destinazione è un percorso relativo a una directory base temporanea (directory di lavoro) in cui viene scaricata la risorsa. Questo identifica le risorse all’interno dei parametri. Non può salire usando '..' o '/'. Deve essere presente un nome file valido.</td>
    </tr>
    <tr>
      <td role="rowheader">Documento di destinazione</td>
      <td>Immettere o mappare il documento da cui si desidera recuperare le informazioni.</td>
    </tr>
     <tr>
      <td role="rowheader">Altri campi</td>
   <td>Per altri campi, consulta le informazioni incluse nel modulo.</td>     </tr>
  </tbody>
</table>

#### Elencare script personalizzati

Questo modulo recupera i dettagli della versione più recente di tutti gli script personalizzati registrati, inclusi la versione, il collegamento per il download, la data di registrazione e il nome dello script. I risultati vengono impaginati in base alla lunghezza dell’elenco.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
      </tr>
    <tr>
      <td role="rowheader">Numero di pagina</td>
      <td>Immettere o mappare il numero di pagina da cui si desidera iniziare.</td>
    </tr>
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Impostare il numero massimo di team o gruppi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
  </tbody>
</table>


### Altri

#### Effettua chiamata API personalizzata

Questo modulo effettua una chiamata API personalizzata all’API Adobe InDesign

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
      <td>Per istruzioni sulla creazione di una connessione ad Adobe InDesign, vedere <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Creare una connessione ad Adobe InDesign</a> in questo articolo.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Percorso</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://indesign.adobe.io/v3</code>.</p><p> Esempio: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Metodo</p>
      </td>
      <td>
        <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere [Metodi di richiesta HTTP](/help/workfront-fusion/references/modules/http-request-methods.md).</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Intestazioni</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Stringa query  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> in JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  </tbody>
</table>
