---
title: Moduli GitLab
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '4095'
ht-degree: 1%

---

# [!UICONTROL Moduli GitLab]

Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!UICONTROL GitLab], nonché collegarlo a più applicazioni e servizi di terze parti.

>[!NOTE]
>
>Questo articolo richiede una certa familiarità con la documentazione API e con la funzionalità [!DNL GitLab] in generale.

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

## Connetti [!DNL GitLab] a Workfront Fusion {#connect-gitlab-to-workfront-fusion}

1. In qualsiasi modulo di Workfront Fusion [!DNL Gitlab], fai clic su **[!UICONTROL Aggiungi]** accanto al campo di connessione.
1. Configura i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Nome connessione]</td> 
      <td> <p>Immettere un nome per la connessione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>Immettere l'URL dell'istanza [!DNL GitLab].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token di accesso]</td> 
      <td><p>Immetti il [!UICONTROL Private Token] o [!UICONTROL Personal Access Token].</p><p>Per informazioni su come individuare o creare un token di accesso personale in [!DNL GitLab], vedere "Creare un token di accesso personale" in <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Token di accesso personali</a> nella documentazione di [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Fai clic su **[!UICONTROL Continua]**.
1. Fai clic su **[!UICONTROL Autorizza]** per creare la connessione e tornare al modulo.

## [!DNL GitLab] moduli e relativi campi

Quando si configurano [!DNL GitLab] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL GitLab], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trigger

+++**[!UICONTROL Verifica stato compilazione]**

Questo modulo di attivazione immediata avvia uno scenario quando lo stato di una build cambia.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto per il quale si desidera che il webhook controlli le modifiche di stato della build</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Osserva commenti commit/MR/issue/snippet]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento su un commit, una richiesta di unione, un problema o uno snippet di codice.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Conferme di controllo (push)]**

Questo modulo di attivazione immediata avvia uno scenario quando un commit viene inviato a un archivio. Questo modulo non avvia uno scenario quando viene inviato un tag.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commit</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Osserva commento problema]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento su un problema.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che desideri venga controllato dal webhook per i commenti sui problemi</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Problemi di controllo]**

Questo modulo [!UICONTROL Instant trigger] avvia uno scenario quando viene creato un problema o quando un problema esistente viene aggiornato, chiuso o riaperto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto che desideri che il webhook controlli per i problemi</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Controlla le richieste di unione]**

Questo modulo di attivazione immediata avvia uno scenario quando si verifica una delle seguenti situazioni:

* Viene creata una nuova richiesta di unione
* Una richiesta di unione esistente viene aggiornata, unita o chiusa
* Viene aggiunto un commit nel ramo di origine


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che il webhook deve controllare per le richieste di unione</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Osserva i commenti della richiesta di unione]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento a una richiesta di unione.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti della richiesta di unione</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Controlla lo stato della pipeline]**

Questo modulo di attivazione immediata avvia uno scenario quando lo stato di una pipeline cambia.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto per il quale si desidera che il webhook controlli le modifiche di stato della pipeline</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Guarda i progetti]**

Questo modulo di attivazione pianificato avvia uno scenario quando viene aggiunto un nuovo progetto di cui l’utente autenticato è membro.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a Workfront Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a Workfront Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Risultati Max</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve controllare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Controlla rami dell&#39;archivio]**

Questo modulo di trigger pianificato avvia uno scenario quando viene aggiunto un nuovo ramo a un archivio.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a Workfront Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a Workfront Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Risultati Max</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve controllare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Osserva i tag del repository]**

Questo modulo di attivazione immediata avvia uno scenario quando un tag viene creato o eliminato in un archivio.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i tag</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Osserva commenti frammento]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un nuovo commento su uno snippet.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Guarda le attività]**

Questo modulo di attivazione pianificato avvia uno scenario quando viene aggiunto un nuovo oggetto. Se non viene applicato alcun filtro, il trigger viene eseguito quando viene aggiunto un nuovo oggetto in sospeso.

Per informazioni sui campi, vedere [Ottenere un elenco di cose da fare](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Guarda la pagina wiki]**

Questo modulo di attivazione immediata avvia uno scenario quando viene creata o modificata una pagina wiki.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti il codice seguente: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che si desidera che il webhook controlli per le pagine wiki</li></ul></li><li>Fai clic su <b>[!UICONTROL Salva]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Azioni

+++**[!UICONTROL Accetta richiesta di unione]**

Questo modulo di azione unisce le modifiche inviate alla richiesta di unione specificata.

Per informazioni sui campi, vedere [Accetta richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Annullare una compilazione]**

Questo modulo di azione annulla una singola build di un progetto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a Workfront Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a Workfront Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID progetto]</td> 
   <td> <p>Seleziona o mappa il progetto che contiene la build da annullare.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td>Seleziona o mappa la build da annullare.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge commit message]</td> 
   <td> Immettere o mappare un messaggio di commit per l'unione.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Deve rimuovere il ramo di origine]</td> 
   <td>Selezionare se si desidera rimuovere il ramo di origine al termine dell'unione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Unisci quando la compilazione riesce]</td> 
   <td>Seleziona se unire la richiesta di unione non appena la build viene completata.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>Se presente, questo SHA deve corrispondere al HEAD del ramo di origine. Se non corrisponde, l'unione non riesce.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Annulla le build di una pipeline]**

Questo modulo di azione annulla le build per una singola pipeline.

Per informazioni sui campi, vedere [Annullare i processi di una pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Annulla unione quando la pipeline ha esito positivo]**

Se una richiesta di unione è impostata per essere unita quando una pipeline viene eseguita correttamente, questo modulo di azione annulla l’azione.

Per informazioni sui campi, vedere [Annulla unione quando la pipeline viene completata](https://docs.gitlab.com/ee/api/merge_requests.html) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Scegli una conferma]**

Questo modulo di azione seleziona un commit per un determinato ramo.

Per informazioni sui campi, vedere [Scegliere un commit](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea una nuova etichetta]**

Questo modulo di azione crea una nuova etichetta per l’archivio specificato.

Per informazioni sui campi, vedere [Creare una nuova etichetta](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea una nuova pipeline]**

Questo modulo di azione crea una nuova pipeline per il progetto specificato.

Per informazioni sui campi, consulta [Creare una nuova pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea una nuova versione]**

Questo modulo di azione aggiunge note sulla versione al tag Git esistente.

Per informazioni sui campi, consulta [Creare una versione](https://docs.gitlab.com/ee/api/releases/#create-a-release) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Creare un nuovo tag]**

Questo modulo di azione crea un nuovo tag nell’archivio che punta al riferimento fornito.

Per informazioni sui campi, vedere [Creare un nuovo tag](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea un oggetto]**

Questo modulo di azione crea una attività per l’utente corrente sul problema selezionato. L’utente corrente è l’utente identificato dalle credenziali sulla connessione utilizzata per questo modulo.

Per informazioni sui campi, consulta [Creare una attività](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Creare un&#39;attività in una richiesta di unione]**

Questo modulo di azione crea un token per l’utente corrente nella richiesta di unione selezionata. L’utente corrente è l’utente identificato dalle credenziali sulla connessione utilizzata per questo modulo.

Per informazioni sui campi, consulta [Creare una cosa da fare](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea richiesta di unione]**

Questo modulo di azione crea una nuova richiesta di unione su un progetto.

Per informazioni sui campi, vedere [Creare una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea nuovo file nel repository]**

Questo modulo di azione crea un nuovo file nell’archivio selezionato.

Per informazioni sui campi, vedere [Creare un nuovo file nel repository](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea nuova nota problema]**

Questo modulo di azione crea una nota di problema per un singolo problema di progetto.

Per informazioni sui campi, vedi [Crea nuova nota problema](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea nuova nota richiesta unione]**

Questo modulo di azione crea una nota per una singola richiesta di unione.

Per informazioni sui campi, consulta [Creare una nuova nota sulla richiesta di unione](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea una nuova milestone]**

Questo modulo di azione crea una nuova milestone per un progetto.

Per informazioni sui campi, consulta [Creare una nuova milestone](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea nuova nota frammento]**

Questo modulo di azione crea una nuova nota per un singolo frammento. Le note dello snippet sono commenti che gli utenti possono pubblicare su uno snippet.

Per informazioni sui campi, consulta [Creare una nuova nota frammento](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea ramo archivio]**

Questo modulo di azione crea un singolo ramo dell’archivio.

Per informazioni sui campi, vedere [Creare un ramo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Crea variabile di compilazione]**

Questo modulo di azione crea una nuova variabile di build.

Per informazioni sui campi, vedere [Creare la variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Eliminare una richiesta di unione]**

Questo modulo di azione è destinato solo agli amministratori e ai proprietari dei progetti. Elimina la richiesta di unione in questione

Per informazioni sui campi, vedere [Eliminare una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elimina file esistente nel repository]**

Questo modulo di azione elimina un file esistente dal repository.

Per informazioni sui campi, vedere [Eliminare il file esistente nel repository](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elimina ramo archivio]**

Questo modulo di azione elimina un ramo dall’archivio.

Per informazioni sui campi, vedere [Elimina ramo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modifica problema]**

Questo modulo di azione aggiorna un problema di progetto esistente. Questa chiamata viene utilizzata anche per contrassegnare un problema come chiuso.

Per informazioni sui campi, consulta [Modifica problema](https://docs.gitlab.com/ee/api/issues.html#edit-issue) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modifica Milestone]**
Questo modulo di azione aggiorna una milestone di progetto esistente.

Per informazioni sui campi, consulta [Modifica milestone](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Cancellare una build]**

Questo modulo di azione cancella la build di un progetto (rimuove gli artefatti del processo e il registro di processo).

Per informazioni sui campi, vedere [Cancellare un processo](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni un elenco di attività]**

Questo modulo di ricerca recupera un elenco di cose da fare.

Per informazioni sui campi, vedere [Ottenere un elenco di cose da fare](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni una singola build]**

Questo modulo di azione recupera un singolo processo di un progetto.

Per informazioni sui campi, vedere [Ottenere un singolo processo](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni un singolo tag repository]**

Questo modulo di azione recupera un tag specifico dell’archivio determinato dal suo nome.

Per informazioni sui campi, vedere [Ottenere un singolo tag repository](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni una distribuzione specifica]**

Questo modulo di azione recupera una distribuzione specifica.

Per informazioni sui campi, vedere [Ottenere una distribuzione specifica](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni tutti i problemi assegnati a un&#39;unica attività cardine]**

Questo modulo di ricerca recupera tutti i problemi assegnati a un singolo progetto milestone.

Per informazioni sui campi, vedi [Ottieni tutti i problemi assegnati a un&#39;unica attività cardine](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni file dal repository]**

Questo modulo di azione recupera informazioni su un file nell’archivio come nome, dimensione o contenuto.

Per informazioni sui campi, vedere [Ottenere il file dal repository](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni utenti progetto]**

Questo modulo di ricerca recupera gli utenti del progetto.

Per informazioni sui campi, vedere [Ottenere gli utenti del progetto](https://docs.gitlab.com/ee/api/projects.html#get-project-users) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni un singolo problema]**

Questo modulo recupera i dettagli del problema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Progetto [!UICONTROL]</td> 
   <td> <p>Seleziona il progetto contenente il problema di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID problema]</td> 
   <td> <p>Inserisci o mappa il nome del problema di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Ottieni singola nota problema]**

Questo modulo di azione recupera una singola nota per un problema di progetto specifico.

Per informazioni sui campi, consulta [Ottenere una singola nota del problema](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Richieste di unione singole]**

Questo modulo di azione recupera informazioni su una singola richiesta di unione.

Per informazioni sui campi, vedere [Ottenere una singola richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Richieste di unione singole modificate]**

Questo modulo di ricerca recupera informazioni sulla richiesta di unione, inclusi i relativi file e le modifiche.

Per informazioni sui campi, vedere [Ottenere modifiche a una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Richieste di unione singole]**

Questo modulo di azione recupera un elenco di commit di richieste di unione.

Per informazioni sui campi, vedere [Ottenere commit di richieste di unione singole](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Richieste di unione singole note]**

Questo modulo di azione restituisce una singola nota per una determinata richiesta di unione.

Per informazioni sui campi, vedere [Ottenere una richiesta di unione singola](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni un milestone]**

Questo modulo di azione recupera i dettagli delle milestone.

Per informazioni sui campi, vedi [Ottenere una singola milestone](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni progetto singolo]**

Questo modulo recupera i dettagli del progetto.

Per informazioni sui campi, vedere [Ottenere un singolo progetto](https://docs.gitlab.com/ee/api/projects.html#get-single-project) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni ramo archivio singolo]**

Questo modulo di azione recupera i dettagli del ramo dell’archivio.

Per informazioni sui campi, vedere [Ottieni ramo singolo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni nota frammento]**

Questo modulo recupera una singola nota per uno snippet specifico.

Per informazioni sui campi, vedere [Ottenere una singola nota frammento](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni i commenti di un commit]**

Questo modulo di ricerca recupera i commenti di un commit in un progetto.

Per informazioni sui campi, vedere [Ottenere i commenti di un commit](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni le differenze di un commit]**

Questo modulo di azione ottiene la differenza di un commit in un progetto.

Per informazioni sui campi, vedere [Ottenere le differenze di un commit](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Mantieni artifact]**

Impedisce l&#39;eliminazione degli artefatti quando è impostata la scadenza.

Per informazioni sui campi, vedere [Mantieni artifact](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca tutte le note della richiesta di unione]**

Questo modulo di ricerca recupera un elenco di tutte le note per una singola richiesta di unione.

Per informazioni sui campi, vedere [Elencare tutte le note sulla richiesta di unione](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca tutte le note frammento]**

Questo modulo ottiene un elenco di tutte le note per un singolo snippet. Le note dello snippet sono commenti che gli utenti possono pubblicare su uno snippet.

Per informazioni sui campi, vedere [🔗](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca le build di commit]**

Questo modulo di ricerca restituisce un elenco di build per un commit specifico in un progetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto]</td> 
   <td> <p>Selezionare il progetto contenente il commit per il quale si desidera elencare le build.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ambito]</td> 
   <td> Per limitare la ricerca alla generazione con uno stato specifico, seleziona lo stato. Se si lascia vuoto questo campo, vengono restituite tutte le build del commit.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Elenca problemi]**

Questo modulo di ricerca restituisce tutti i problemi in base alle impostazioni del filtro specificate.

Per informazioni sui campi, consulta [Elencare i problemi](https://docs.gitlab.com/ee/api/issues.html#list-issues) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca i problemi che si chiudono al momento dell&#39;unione]**

Questo modulo di ricerca recupera tutti i problemi che verrebbero chiusi unendo la richiesta di unione fornita.

Per informazioni sui campi, consulta [Elencare i problemi che si chiuderanno al momento dell&#39;unione](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Etichette elenco]**

Questo modulo di ricerca recupera tutte le etichette nel progetto.

Per informazioni sui campi, vedere [Etichette elenco](https://docs.gitlab.com/ee/api/labels.html#list-labels) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca richieste di unione]**

Questo modulo di ricerca recupera tutte le richieste di unione in base alle impostazioni del filtro.

Per informazioni sui campi, consulta [Elencare richieste di unione](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca progetti di proprietà]**

Questo modulo di ricerca recupera i progetti in cui l’utente autenticato è impostato come proprietario.

Per informazioni sui campi, consulta [Elencare i progetti utente](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca build progetto]**

Questo modulo di ricerca recupera un elenco di build in un progetto.

Per informazioni sui campi, consulta [Elencare i processi di progetto](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca distribuzioni progetti]**

Questo modulo di ricerca recupera un elenco di distribuzioni in un progetto.

Per informazioni sui campi, consulta [Elencare le distribuzioni dei progetti](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare le note sui problemi del progetto]**

Questo modulo di ricerca recupera un elenco di tutte le note per un singolo problema.

Per informazioni sui campi, consulta [Elencare le note sui problemi del progetto](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca problemi progetto]**

Questo modulo di ricerca restituisce tutti i problemi di un progetto specificato.

Per informazioni sui campi, consulta [Elencare i problemi del progetto](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare le milestone del progetto]**

Questo modulo di ricerca recupera tutte le milestone nel progetto.

Per informazioni sui campi, consulta [Elencare le milestone del progetto](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare le pipeline del progetto]**

Questo modulo di ricerca recupera tutte le pipeline per il progetto.

Per informazioni sui campi, consulta [Elencare le pipeline del progetto](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare i tag del repository dei progetti]**

Questo modulo di ricerca recupera un elenco di tag del repository da un progetto, ordinati per nome in ordine alfabetico inverso.

Per informazioni sui campi, vedere [Elencare i tag del repository dei progetti](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca variabili progetto]**

Questo modulo di ricerca recupera un elenco delle variabili di un progetto.

Per informazioni sui campi, vedere [Elencare le variabili di progetto](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare progetti]**

Questo modulo di ricerca recupera tutti i progetti di cui l’utente autenticato è membro.

Per informazioni sui campi, vedere [Elencare tutti i progetti](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca rami dell&#39;archivio]**

Questo modulo cerca i rami dell’archivio in base al termine di ricerca.

Per informazioni sui campi, consulta [Elenca rami dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenca commit repository]**

Questo modulo di ricerca recupera un elenco di commit dell’archivio in un progetto.

Per informazioni sui campi, vedere [Elenca commit repository](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elencare i collaboratori dell&#39;archivio]**

Questo modulo di ricerca recupera un elenco di collaboratori dell’archivio.

Per informazioni sui campi, vedi [Collaboratori](https://docs.gitlab.com/ee/api/repositories.html#contributors) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Elenco struttura repository]**

Questo modulo di ricerca recupera un elenco di file e directory del repository in un progetto.

Per informazioni sui campi, vedere [Elenco struttura repository](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Contrassegna un&#39;attività come completata]**

Questo modulo di azione contrassegna come completato un singolo elemento da fare in sospeso fornito dal relativo ID per l’utente corrente.

Per informazioni sui campi, vedere [Contrassegnare un elemento attività come completato](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modifica nota problema esistente]**

Modifica una nota esistente di un problema.

Per informazioni sui campi, consulta [Modificare la nota di problema esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modifica nota richiesta unione esistente]**

Modifica la nota esistente di una richiesta di unione.

Per informazioni sui campi, vedere [Modificare la nota di richiesta di unione esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modifica nota frammento esistente]**

Questo modulo modifica una nota esistente di uno snippet.

Per informazioni sui campi, vedere [Modificare la nota frammento esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Nuovo problema]**

Questo modulo di azione crea un nuovo problema di progetto.

Per informazioni sui campi, vedi [Nuovo problema](https://www.integromat.com/en/help/app/gitlab) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Riproduci una build]**

Questo modulo di azione attiva un’azione manuale per avviare un processo.

Per informazioni sui campi, consulta [Riprodurre un processo](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Pubblica commento per confermare]**

Questo modulo di azione aggiunge un commento a un commit.

Per informazioni sui campi, vedere [Pubblica commento per eseguire il commit](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Rimuovi variabile]**

Questo modulo di azione rimuove la variabile di un progetto.

Per informazioni sui campi, vedere [Rimuovi variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Riprovare una compilazione]**

Questo modulo di azione tenta nuovamente una singola build in un commit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto]</td> 
   <td> <p>Seleziona il progetto contenente la build da riprovare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> Seleziona la build da riprovare. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Ritenta processi non riusciti in una pipeline]**

Questo modulo di azione tenta nuovamente le build non riuscite in una pipeline.

Per informazioni sui campi, vedere [Riprovare i processi in una pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Ottieni variabile]**

Questo modulo recupera i dettagli della variabile specifica di un progetto.

Per informazioni sui campi, vedere [Mostra dettagli variabili](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Aggiornare una versione]**

Questo modulo di azione aggiorna una versione.

Per informazioni sui campi, consulta [Aggiornare una versione](https://docs.gitlab.com/ee/api/releases/#update-a-release) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Aggiorna richiesta di unione]**

Questo modulo di azione aggiorna una richiesta di unione esistente. È possibile modificare il ramo di destinazione, il titolo o anche chiudere MR.

Per informazioni sui campi, vedere [Aggiorna richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Aggiorna una variabile]**

Questo modulo di azione aggiorna la variabile di un progetto.

Per informazioni sui campi, vedere [Aggiorna variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) nella documentazione di [!DNL GitLab].

+++
