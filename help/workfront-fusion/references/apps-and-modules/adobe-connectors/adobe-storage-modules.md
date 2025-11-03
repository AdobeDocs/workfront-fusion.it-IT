---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Moduli di storage Adobe
description: In uno scenario Adobe Workfront Fusion, puoi creare e gestire progetti in Adobe Admin Console.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 3%

---

# Moduli di storage Adobe

In uno scenario Adobe Workfront Fusion, puoi creare e gestire progetti in Adobe Admin Console.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

## Creare una connessione ad Adobe Storage

La creazione di una connessione a Adobe Storage richiede una certa configurazione sia in Adobe Developer Console che in Fusion.

### Configurare il progetto in Adobe Developer Console

Devi aggiungere l’API al progetto in Adobe Developer Console.

1. Apri il progetto in Adobe Developer Console.
1. Fai clic su **Aggiungi al progetto** e seleziona **API**.
1. Dall&#39;elenco delle API disponibili, selezionare **Adobe Cloud Platform e Collaboration API**.
1. Nella schermata Seleziona tipo di autenticazione, seleziona **OAuth Server-to-Server** e fai clic su **Avanti**.
1. Aggiungi un nome per la rappresentazione.
1. Fai clic su **Avanti**, quindi fai clic su **Salva API configurata**.
1. Prendi nota delle credenziali fornite, che utilizzerai durante la configurazione della connessione in Workfront Fusion.
1. Continua con [Rendi il tuo account tecnico amministratore in Adobe Admin Console](#make-your-technical-account-an-admin-in-the-adobe-admin-console).

### Imposta il tuo account tecnico come amministratore in Adobe Admin Console

Dalla pagina Adobe Admin Console, seleziona la scheda Prodotti nella barra di navigazione superiore, quindi seleziona Workfront Fusion

1. Individua e copia l’indirizzo e-mail dell’utente dell’account tecnico nella tua organizzazione.
1. Se viene visualizzato un elenco, seleziona il collegamento in alto.
1. Questa è l’istanza di produzione in cui lavorano gli utenti.
1. Nell&#39;elenco visualizzato, con la scheda Profili di prodotto selezionata, fare clic sul collegamento Profilo di prodotto Workfront.

   Questo elenco include tutti gli utenti già assegnati all’istanza Production di Workfront.

1. Seleziona la scheda **Amministratori** sopra l&#39;elenco degli utenti.
1. Selezionare **Aggiungi amministratore**.
1. Nella casella Aggiungi amministratori profilo prodotto, inserisci gli indirizzi e-mail dell&#39;account tecnico, quindi seleziona **Salva**.

   L’account tecnico viene impostato come amministratore.

1. Continua con [Crea la connessione in Workfront Fusion](#create-the-connection-in-workfront-fusion).

### Creare la connessione in Workfront Fusion

Per creare una connessione per i moduli [!DNL Adobe Storage]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo di connessione]</td>
        <td>Seleziona <code>Server to server</code>.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Nome connessione]</td>
        <td>
          <p>Immettere un nome per la connessione.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti [!UICONTROL Adobe] [!UICONTROL ID client]. È disponibile nella sezione [!UICONTROL Credential details] del progetto in [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Segreto client]</td>
        <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credential details] del progetto in [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Inserisci o mappa l’ID organizzazione Adobe IMS. Questa è una stringa con il formato <code> 123abc@AdobeOrg</code>, dove la sezione prima della @ è un numero esadecimale. Puoi trovare questo valore come parte del percorso URL per la tua organizzazione in Adobe Admin Console o nella console Adobe.IO per l’integrazione di gestione utenti.</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## Moduli di storage Adobe e relativi campi

Quando configuri i moduli di Gestione utenti di Adobe, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati altri campi di Gestione utente di Adobe, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Archivi ESM](#esm-stores)
* [Inviti](#invitations)
* [Altro](#other)

### Archivi ESM

* [Creare un archivio ESM](#create-an-esm-store)
* [Eliminare un archivio ESM](#delete-an-esm-store)
* [Eliminare un archivio ESM](#discard-an-esm-store)
* [Ripristinare un archivio ESM](#restore-an-esm-store)

#### Creare un archivio ESM

Questo modulo di azione consente di configurare un nuovo archivio ESM (Enterprise Storage Management) per organizzare e gestire le risorse business-critical.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome progetto</td> 
   <td>Inserisci o mappa un nome per il nuovo progetto.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un archivio ESM

Questo modulo di azione rimuove definitivamente un archivio ESM esistente e tutti i dati associati. Questa azione non può essere annullata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID store</td> 
   <td>Immetti o mappa l’ID dello store da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un archivio ESM

Questo modulo di azione contrassegna un archivio EMS per l&#39;eliminazione, consentendo un periodo di tolleranza prima della rimozione definitiva.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID store</td> 
   <td>Immetti o mappa l’ID dell’archivio da eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### Ripristinare un archivio ESM

Questo modulo di azione recupera un archivio ESM precedentemente eliminato e ripristina l’accesso ai relativi dati e configurazioni.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID store</td> 
   <td>Immetti o mappa l’ID dell’archivio da ripristinare.</td> 
  </tr> 
 </tbody> 
</table>

### Inviti

#### Invita utente

Questo modulo di azione invia un invito a concedere a un nuovo utente l’accesso a uno specifico archivio ESM, abilitando la collaborazione e la gestione dei file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Indirizzo e-mail</td> 
   <td>Immetti o mappa l’indirizzo e-mail dell’utente che desideri invitare nel negozio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID risorsa</td> 
   <td>Inserisci o mappa l’ID della risorsa a cui desideri invitare l’utente.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ruolo</td> 
   <td>Seleziona il ruolo che desideri assegnare alla risorsa al nuovo utente invitato.<ul><li>Proprietario</li><li>Editor</li><li>Visualizzatore</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Può commentare</td> 
   <td>Abilita questa opzione per consentire all’utente di aggiungere un commento alla risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Può condividere</td> 
   <td>Abilita questa opzione per consentire agli utenti di condividere la risorsa con altri utenti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Accettazione richiesta</td> 
   <td>Abilita questa opzione per garantire che l’utente accetti l’invito prima di poter collaborare alla risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Usa supporti</td> 
   <td>Abilita questa opzione se è necessario creare un punto di montaggio per la risorsa per l’invitato. Per abilitare questa opzione, è necessario abilitare l'opzione Accettazione richiesta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di notifica</td> 
   <td>Immetti o mappa il tipo di notifica di Adobe che desideri utilizzare per notificare l’invito all’utente. Se questo campo viene lasciato vuoto, il tipo di notifica si basa sul tipo mime della risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome modello</td> 
   <td>Inserisci o mappa l’ID Adobe Post Office del modello da utilizzare per l’e-mail di invito.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lingua</td> 
   <td>Immettere le impostazioni locali dell'utente sotto forma di codice della lingua e codice del paese. <p>Esempio: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Esterno</td> 
   <td>Imposta questa opzione su true se desideri inviare notifiche utilizzando un sistema esterno al servizio Adobe Invitations. La notifica esterna è supportata solo quando non è richiesta l’accettazione.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di risorsa</td> 
   <td>Inserisci o mappa il tipo di risorsa.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Messaggio</td> 
   <td>Immettere o mappare un messaggio da includere nell'e-mail di invito.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL di destinazione</td> 
   <td>Inserisci o mappa l’URL che l’invitato può utilizzare per visualizzare la risorsa.</td> 
  </tr> 
 </tbody> 
</table>

### Altro

#### Effettuare una chiamata API personalizzata

Questo modulo di azione invia una richiesta HTTP personalizzata all’API di archiviazione Adobe.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connessione</td>
   <td>Per istruzioni sulla creazione di una connessione ad Adobe Storage, vedere <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Creare una connessione ad Adobe Storage</a> in questo articolo.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Inserisci un percorso relativo a <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Metodo</p>
      </td>
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Intestazioni</td>
      <td>
        <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p>
        <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione e le intestazioni di x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Stringa di query  </td>
      <td>
        <p>Immettere la stringa di query richiesta.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Corpo</td>
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
