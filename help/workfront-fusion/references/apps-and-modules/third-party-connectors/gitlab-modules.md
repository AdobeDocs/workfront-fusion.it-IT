---
title: Moduli GitLab
description: Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3554'
ht-degree: 0%

---

# [!UICONTROL GitLab] moduli

Adobe Workfront Fusion richiede una licenza Adobe Workfront Fusion oltre a una licenza Adobe Workfront.

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL GitLab] e collegarlo a più applicazioni e servizi di terze parti.

>[!NOTE]
>
>Questo articolo richiede una certa familiarità con la documentazione API e con la funzionalità [!DNL GitLab] in generale.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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

## Connetti [!DNL GitLab] a [!DNL Workfront Fusion] {#connect-gitlab-to-workfront-fusion}

1. In qualsiasi modulo [!DNL Workfront Fusion] [!DNL Gitlab], fai clic su **[!UICONTROL Add]** accanto al campo di connessione.
1. Configura i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td> <p>Immettere un nome per la connessione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>Immettere l'URL dell'istanza [!DNL GitLab].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Access Token]</td> 
      <td><p>Immetti [!UICONTROL Private Token] o [!UICONTROL Personal Access Token].</p><p>Per informazioni su come individuare o creare un token di accesso personale in [!DNL GitLab], vedere "Creare un token di accesso personale" in <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Token di accesso personali</a> nella documentazione di [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Fare clic su **[!UICONTROL Continue]**.
1. Fare clic su **[!UICONTROL Authorize]** per creare la connessione e tornare al modulo.

## [!DNL GitLab] moduli e relativi campi

Quando configuri [!DNL GitLab] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL GitLab], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

+++**[!UICONTROL Watch build status]**

Questo modulo di attivazione immediata avvia uno scenario quando lo stato di una build cambia.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto per il quale si desidera che il webhook controlli le modifiche di stato della build</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commit/MR/issue/snippet comments]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento su un commit, una richiesta di unione, un problema o uno snippet di codice.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commits (pushes)]**

Questo modulo di attivazione immediata avvia uno scenario quando un commit viene inviato a un archivio. Questo modulo non avvia uno scenario quando viene inviato un tag.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commit</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issue comment]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento su un problema.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che desideri venga controllato dal webhook per i commenti sui problemi</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issues]**

Questo modulo [!UICONTROL instant trigger] avvia uno scenario quando viene creato un problema o quando un problema esistente viene aggiornato, chiuso o riaperto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto che desideri che il webhook controlli per i problemi</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge requests]**

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
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che il webhook deve controllare per le richieste di unione</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge request comments]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un commento a una richiesta di unione.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti della richiesta di unione</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch pipeline status]**

Questo modulo di attivazione immediata avvia uno scenario quando lo stato di una pipeline cambia.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Il progetto per il quale si desidera che il webhook controlli le modifiche di stato della pipeline</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch projects]**

Questo modulo di attivazione pianificato avvia uno scenario quando viene aggiunto un nuovo progetto di cui l’utente autenticato è membro.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a [!DNL Workfront] Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a [!DNL Workfront] Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Risultati Max</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve controllare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository branches]**

Questo modulo di trigger pianificato avvia uno scenario quando viene aggiunto un nuovo ramo a un archivio.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a [!DNL Workfront] Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a [!DNL Workfront] Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Risultati Max</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve controllare durante ogni ciclo di esecuzione dello scenario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository tags]**

Questo modulo di attivazione immediata avvia uno scenario quando un tag viene creato o eliminato in un archivio.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i tag</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch snippet comments]**

Questo modulo di attivazione immediata avvia uno scenario quando viene aggiunto un nuovo commento su uno snippet.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto per il quale si desidera che il webhook controlli i commenti</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch todos]**

Questo modulo di attivazione pianificato avvia uno scenario quando viene aggiunto un nuovo oggetto. Se non viene applicato alcun filtro, il trigger viene eseguito quando viene aggiunto un nuovo oggetto in sospeso.

Per informazioni sui campi, vedere [Ottenere un elenco di cose da fare](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Watch wiki page]**

Questo modulo di attivazione immediata avvia uno scenario quando viene creata o modificata una pagina wiki.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Seleziona il webhook da utilizzare per questo trigger o aggiungi un nuovo webhook. </p><p>Per aggiungere un nuovo webhook: <ol><li>Fare clic su <b>[!UICONTROL Add]</b> accanto al campo [!UICONTROL webhook].</li><li>Immetti quanto segue: <ul><li>Nome del webhook</li><li>Connessione da utilizzare per questo webhook</li><li>Progetto che si desidera che il webhook controlli per le pagine wiki</li></ul></li><li>Fare clic su <b>[!UICONTROL Save]</b> per salvare il webhook e tornare al modulo. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Azioni

+++**[!UICONTROL Accept merge request]**

Questo modulo di azione unisce le modifiche inviate alla richiesta di unione specificata.

Per informazioni sui campi, vedere [Accetta richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Cancel a build]**

Questo modulo di azione annulla una singola build di un progetto.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL GitLab] a [!DNL Workfront] Fusion, vedere <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connettere [!DNL GitLab] a [!DNL Workfront] Fusion</a> in questo articolo.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
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
   <td role="rowheader">[!UICONTROL Should remove source branch]</td> 
   <td>Selezionare se si desidera rimuovere il ramo di origine al termine dell'unione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge when build succeeds]</td> 
   <td>Seleziona se unire la richiesta di unione non appena la build viene completata.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>Se presente, questo SHA deve corrispondere al HEAD del ramo di origine. Se non corrisponde, l'unione non riesce.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Cancel a pipeline's builds]**

Questo modulo di azione annulla le build per una singola pipeline.

Per informazioni sui campi, vedere [Annullare i processi di una pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Cancel merge when pipeline succeeds]**

Se una richiesta di unione è impostata per essere unita quando una pipeline viene eseguita correttamente, questo modulo di azione annulla l’azione.

Per informazioni sui campi, vedere [Annulla unione quando la pipeline viene completata](https://docs.gitlab.com/ee/api/merge_requests.html) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Cherry pick a commit]**

Questo modulo di azione seleziona un commit per un determinato ramo.

Per informazioni sui campi, vedere [Scegliere un commit](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a new label]**

Questo modulo di azione crea una nuova etichetta per l’archivio specificato.

Per informazioni sui campi, vedere [Creare una nuova etichetta](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a new pipeline]**

Questo modulo di azione crea una nuova pipeline per il progetto specificato.

Per informazioni sui campi, consulta [Creare una nuova pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a new release]**

Questo modulo di azione aggiunge note sulla versione al tag Git esistente.

Per informazioni sui campi, consulta [Creare una versione](https://docs.gitlab.com/ee/api/releases/#create-a-release) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a new tag]**

Questo modulo di azione crea un nuovo tag nell’archivio che punta al riferimento fornito.

Per informazioni sui campi, vedere [Creare un nuovo tag](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo]**

Questo modulo di azione crea una attività per l’utente corrente sul problema selezionato. L’utente corrente è l’utente identificato dalle credenziali sulla connessione utilizzata per questo modulo.

Per informazioni sui campi, consulta [Creare una attività](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo on a merge request]**

Questo modulo di azione crea un token per l’utente corrente nella richiesta di unione selezionata. L’utente corrente è l’utente identificato dalle credenziali sulla connessione utilizzata per questo modulo.

Per informazioni sui campi, consulta [Creare una cosa da fare](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create merge request]**

Questo modulo di azione crea una nuova richiesta di unione su un progetto.

Per informazioni sui campi, vedere [Creare una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create new file in repository]**

Questo modulo di azione crea un nuovo file nell’archivio selezionato.

Per informazioni sui campi, vedere [Creare un nuovo file nel repository](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create new issue note]**

Questo modulo di azione crea una nota di problema per un singolo problema di progetto.

Per informazioni sui campi, vedi [Crea nuova nota problema](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create new merge request note]**

Questo modulo di azione crea una nota per una singola richiesta di unione.

Per informazioni sui campi, consulta [Creare una nuova nota sulla richiesta di unione](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create a new milestone]**

Questo modulo di azione crea una nuova milestone per un progetto.

Per informazioni sui campi, consulta [Creare una nuova milestone](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create new snippet note]**

Questo modulo di azione crea una nuova nota per un singolo frammento. Le note dello snippet sono commenti che gli utenti possono pubblicare su uno snippet.

Per informazioni sui campi, consulta [Creare una nuova nota frammento](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create repository branch]**

Questo modulo di azione crea un singolo ramo dell’archivio.

Per informazioni sui campi, vedere [Creare un ramo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Create build variable]**

Questo modulo di azione crea una nuova variabile di build.

Per informazioni sui campi, vedere [Creare la variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Delete a merge request]**

Questo modulo di azione è destinato solo agli amministratori e ai proprietari dei progetti. Elimina la richiesta di unione in questione

Per informazioni sui campi, vedere [Eliminare una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Delete existing file in repository]**

Questo modulo di azione elimina un file esistente dal repository.

Per informazioni sui campi, vedere [Eliminare il file esistente nel repository](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Delete repository branch]**

Questo modulo di azione elimina un ramo dall’archivio.

Per informazioni sui campi, vedere [Elimina ramo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Edit issue]**

Questo modulo di azione aggiorna un problema di progetto esistente. Questa chiamata viene utilizzata anche per contrassegnare un problema come chiuso.

Per informazioni sui campi, consulta [Modifica problema](https://docs.gitlab.com/ee/api/issues.html#edit-issue) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Edit Milestone]**
Questo modulo di azione aggiorna una milestone di progetto esistente.

Per informazioni sui campi, consulta [Modifica milestone](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Erase a build]**

Questo modulo di azione cancella la build di un progetto (rimuove gli artefatti del processo e il registro di processo).

Per informazioni sui campi, vedere [Cancellare un processo](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a list of todos]**

Questo modulo di ricerca recupera un elenco di cose da fare.

Per informazioni sui campi, vedere [Ottenere un elenco di cose da fare](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a single build]**

Questo modulo di azione recupera un singolo processo di un progetto.

Per informazioni sui campi, vedere [Ottenere un singolo processo](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a single repository tag]**

Questo modulo di azione recupera un tag specifico dell’archivio determinato dal suo nome.

Per informazioni sui campi, vedere [Ottenere un singolo tag repository](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a specific deployment]**

Questo modulo di azione recupera una distribuzione specifica.

Per informazioni sui campi, vedere [Ottenere una distribuzione specifica](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get all issues assigned to a single milestone]**

Questo modulo di ricerca recupera tutti i problemi assegnati a un singolo progetto milestone.

Per informazioni sui campi, vedi [Ottieni tutti i problemi assegnati a un&#39;unica attività cardine](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get file from repository]**

Questo modulo di azione recupera informazioni su un file nell’archivio come nome, dimensione o contenuto.

Per informazioni sui campi, vedere [Ottenere il file dal repository](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get project users]**

Questo modulo di ricerca recupera gli utenti del progetto.

Per informazioni sui campi, vedere [Ottenere gli utenti del progetto](https://docs.gitlab.com/ee/api/projects.html#get-project-users) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a single issue]**

Questo modulo recupera i dettagli del problema.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] a Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>Seleziona il progetto contenente il problema di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>Inserisci o mappa il nome del problema di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Get single issue note]**

Questo modulo di azione recupera una singola nota per un problema di progetto specifico.

Per informazioni sui campi, consulta [Ottenere una singola nota del problema](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request]**

Questo modulo di azione recupera informazioni su una singola richiesta di unione.

Per informazioni sui campi, vedere [Ottenere una singola richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request changes]**

Questo modulo di ricerca recupera informazioni sulla richiesta di unione, inclusi i relativi file e le modifiche.

Per informazioni sui campi, vedere [Ottenere modifiche a una richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request commits]**

Questo modulo di azione recupera un elenco di commit di richieste di unione.

Per informazioni sui campi, vedere [Ottenere commit di richieste di unione singole](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request note]**

Questo modulo di azione restituisce una singola nota per una determinata richiesta di unione.

Per informazioni sui campi, vedere [Ottenere una richiesta di unione singola](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a Milestone]**

Questo modulo di azione recupera i dettagli delle milestone.

Per informazioni sui campi, vedi [Ottenere una singola milestone](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single project]**

Questo modulo recupera i dettagli del progetto.

Per informazioni sui campi, vedere [Ottenere un singolo progetto](https://docs.gitlab.com/ee/api/projects.html#get-single-project) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get single repository branch]**

Questo modulo di azione recupera i dettagli del ramo dell’archivio.

Per informazioni sui campi, vedere [Ottieni ramo singolo dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get snippet note]**

Questo modulo recupera una singola nota per uno snippet specifico.

Per informazioni sui campi, vedere [Ottenere una singola nota frammento](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get the comments of a commit]**

Questo modulo di ricerca recupera i commenti di un commit in un progetto.

Per informazioni sui campi, vedere [Ottenere i commenti di un commit](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get the diff of a commit]**

Questo modulo di azione ottiene la differenza di un commit in un progetto.

Per informazioni sui campi, vedere [Ottenere le differenze di un commit](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Keep artifacts]**

Impedisce l&#39;eliminazione degli artefatti quando è impostata la scadenza.

Per informazioni sui campi, vedere [Mantieni artifact](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List all merge request notes]**

Questo modulo di ricerca recupera un elenco di tutte le note per una singola richiesta di unione.

Per informazioni sui campi, vedere [Elencare tutte le note sulla richiesta di unione](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List all snippet notes]**

Questo modulo ottiene un elenco di tutte le note per un singolo snippet. Le note dello snippet sono commenti che gli utenti possono pubblicare su uno snippet.

Per informazioni sui campi, vedere [??](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List commit builds]**

Questo modulo di ricerca restituisce un elenco di build per un commit specifico in un progetto.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] a Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Selezionare il progetto contenente il commit per il quale si desidera elencare le build.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> Per limitare la ricerca alla generazione con uno stato specifico, seleziona lo stato. Se si lascia vuoto questo campo, vengono restituite tutte le build del commit.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL List issues]**

Questo modulo di ricerca restituisce tutti i problemi in base alle impostazioni del filtro specificate.

Per informazioni sui campi, consulta [Elencare i problemi](https://docs.gitlab.com/ee/api/issues.html#list-issues) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List Issues That Close on Merge]**

Questo modulo di ricerca recupera tutti i problemi che verrebbero chiusi unendo la richiesta di unione fornita.

Per informazioni sui campi, consulta [Elencare i problemi che si chiuderanno al momento dell&#39;unione](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List Labels]**

Questo modulo di ricerca recupera tutte le etichette nel progetto.

Per informazioni sui campi, vedere [Etichette elenco](https://docs.gitlab.com/ee/api/labels.html#list-labels) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List merge requests]**

Questo modulo di ricerca recupera tutte le richieste di unione in base alle impostazioni del filtro.

Per informazioni sui campi, consulta [Elencare richieste di unione](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List Owned Projects]**

Questo modulo di ricerca recupera i progetti in cui l’utente autenticato è impostato come proprietario.

Per informazioni sui campi, consulta [Elencare i progetti utente](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project builds]**

Questo modulo di ricerca recupera un elenco di build in un progetto.

Per informazioni sui campi, consulta [Elencare i processi di progetto](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project deployments]**

Questo modulo di ricerca recupera un elenco di distribuzioni in un progetto.

Per informazioni sui campi, consulta [Elencare le distribuzioni dei progetti](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project issue notes]**

Questo modulo di ricerca recupera un elenco di tutte le note per un singolo problema.

Per informazioni sui campi, consulta [Elencare le note sui problemi del progetto](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project issues]**

Questo modulo di ricerca restituisce tutti i problemi di un progetto specificato.

Per informazioni sui campi, consulta [Elencare i problemi del progetto](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project milestones]**

Questo modulo di ricerca recupera tutte le milestone nel progetto.

Per informazioni sui campi, consulta [Elencare le milestone del progetto](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project pipelines]**

Questo modulo di ricerca recupera tutte le pipeline per il progetto.

Per informazioni sui campi, consulta [Elencare le pipeline del progetto](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project repository tags]**

Questo modulo di ricerca recupera un elenco di tag del repository da un progetto, ordinati per nome in ordine alfabetico inverso.

Per informazioni sui campi, vedere [Elencare i tag del repository dei progetti](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List project variables]**

Questo modulo di ricerca recupera un elenco delle variabili di un progetto.

Per informazioni sui campi, vedere [Elencare le variabili di progetto](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List projects]**

Questo modulo di ricerca recupera tutti i progetti di cui l’utente autenticato è membro.

Per informazioni sui campi, vedere [Elencare tutti i progetti](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List repository branches]**

Questo modulo cerca i rami dell’archivio in base al termine di ricerca.

Per informazioni sui campi, consulta [Elenca rami dell&#39;archivio](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List repository commits]**

Questo modulo di ricerca recupera un elenco di commit dell’archivio in un progetto.

Per informazioni sui campi, vedere [Elenca commit repository](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List repository contributors]**

Questo modulo di ricerca recupera un elenco di collaboratori dell’archivio.

Per informazioni sui campi, vedi [Collaboratori](https://docs.gitlab.com/ee/api/repositories.html#contributors) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL List repository tree]**

Questo modulo di ricerca recupera un elenco di file e directory del repository in un progetto.

Per informazioni sui campi, vedere [Elenco struttura repository](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Mark a todo as done]**

Questo modulo di azione contrassegna come completato un singolo elemento da fare in sospeso fornito dal relativo ID per l’utente corrente.

Per informazioni sui campi, vedere [Contrassegnare un elemento attività come completato](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing issue note]**

Modifica una nota esistente di un problema.

Per informazioni sui campi, consulta [Modificare la nota di problema esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing merge request note]**

Modifica la nota esistente di una richiesta di unione.

Per informazioni sui campi, vedere [Modificare la nota di richiesta di unione esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing snippet note]**

Questo modulo modifica una nota esistente di uno snippet.

Per informazioni sui campi, vedere [Modificare la nota frammento esistente](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL New issue]**

Questo modulo di azione crea un nuovo problema di progetto.

Per informazioni sui campi, vedi [Nuovo problema](https://www.integromat.com/en/help/app/gitlab) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Play a build]**

Questo modulo di azione attiva un’azione manuale per avviare un processo.

Per informazioni sui campi, consulta [Riprodurre un processo](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Post comment to commit]**

Questo modulo di azione aggiunge un commento a un commit.

Per informazioni sui campi, vedere [Pubblica commento per eseguire il commit](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Remove variable]**

Questo modulo di azione rimuove la variabile di un progetto.

Per informazioni sui campi, vedere [Rimuovi variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Retry a build]**

Questo modulo di azione tenta nuovamente una singola build in un commit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per creare una nuova connessione, vedere <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] a Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Seleziona il progetto contenente la build da riprovare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> Seleziona la build da riprovare. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Retry Failed Jobs in a Pipeline]**

Questo modulo di azione tenta nuovamente le build non riuscite in una pipeline.

Per informazioni sui campi, vedere [Riprovare i processi in una pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Get a Variable]**

Questo modulo recupera i dettagli della variabile specifica di un progetto.

Per informazioni sui campi, vedere [Mostra dettagli variabili](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Update a release]**

Questo modulo di azione aggiorna una versione.

Per informazioni sui campi, consulta [Aggiornare una versione](https://docs.gitlab.com/ee/api/releases/#update-a-release) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Update merge request]**

Questo modulo di azione aggiorna una richiesta di unione esistente. È possibile modificare il ramo di destinazione, il titolo o anche chiudere MR.

Per informazioni sui campi, vedere [Aggiorna richiesta di unione](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) nella documentazione di [!DNL GitLab].

+++

+++**[!UICONTROL Update a Variable]**

Questo modulo di azione aggiorna la variabile di un progetto.

Per informazioni sui campi, vedere [Aggiorna variabile](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) nella documentazione di [!DNL GitLab].

+++
