---
title: Moduli Microsoft Teams
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano i team e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 2%

---

# Moduli Microsoft Teams

<!-- ADD REDIRECTS -->

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Microsoft Teams e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli Microsoft Teams, è necessario disporre di un account Microsoft Teams in grado di eseguire l&#39;azione nel modulo.

## Collegamento del servizio Microsoft Teams a Workfront Fusion

Per istruzioni sulla connessione dell&#39;account Microsoft Teams a Workfront Fusion, vedere [Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## Moduli Microsoft Teams e relativi campi

Quando configuri i moduli di Microsoft Teams, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi Microsoft Teams aggiuntivi, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Team](#team)
* [Canale](#channel)
* [Messaggio](#message)
* [Membro](#member)
* [Riunione online](#online-meeting)
* [Altro](#other)

### Team

* [Creare un team da un gruppo](#create-a-team-from-a-group)
* [Creare un gruppo di Office 365](#create-an-office-365-group)
* [Eliminare un team o un gruppo](#delete-a-team-or-group)
* [Ottieni un team](#get-a-team)
* [Elenca tutti i team e i gruppi](#list-all-teams-and-groups)
* [Elencare i team uniti](#list-joined-teams)
* [Aggiornare un team](#update-a-team)
* [Guarda i team](#watch-teams)

#### Creare un team da un gruppo

Questo modulo di azione crea un team da un gruppo esistente di Microsoft Office 365 e configura le impostazioni per il nuovo team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID Gruppo</td> 
   <td> <p>Selezionare il gruppo da cui si desidera creare un team.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Consenti ai membri di creare e aggiornare i canali</td> 
   <td>Specificare se si desidera consentire ai membri di creare e aggiornare i canali.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti ai membri di eliminare i canali</td> 
   <td>Specificare se si desidera consentire ai membri di eliminare i canali.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti ai membri di aggiungere e rimuovere app</td> 
   <td>Specificare se si desidera consentire ai membri di aggiungere e rimuovere app.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti ai membri di creare, aggiornare e rimuovere schede</td> 
   <td>Specificare se si desidera consentire ai membri di creare, aggiornare e rimuovere schede.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti ai membri di creare e rimuovere i connettori</td> 
   <td>Specificare se si desidera consentire ai membri di creare e rimuovere i connettori.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti agli utenti di modificare i messaggi</td> 
   <td>Seleziona se desideri consentire agli utenti di modificare i loro messaggi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti agli utenti di eliminare i messaggi</td> 
   <td>Seleziona se desideri consentire agli utenti di eliminare i loro messaggi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti ai proprietari di eliminare i messaggi</td> 
   <td>Seleziona se desideri consentire ai proprietari di eliminare qualsiasi messaggio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti menzioni @team</td> 
   <td>Seleziona se desideri consentire le menzioni @team.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti menzioni @channel</td> 
   <td>Seleziona se desideri consentire le menzioni @channel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti Giphy</td> 
   <td>Seleziona se vuoi consentire l’uso di Giphy per questo team.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti adesivi e meme</td> 
   <td>Specificare se si desidera consentire agli utenti di includere adesivi e meme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti memi personalizzati</td> 
   <td>Seleziona se consentire agli utenti di includere memi personalizzati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti agli ospiti di creare e aggiornare i canali</td> 
   <td>Seleziona se desideri consentire agli ospiti di creare e aggiornare i canali.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Consenti agli ospiti di eliminare i canali</td> 
   <td>Seleziona se desideri consentire agli ospiti di eliminare i canali.</td> 
  </tr> 
 </tbody> 
</table>

#### Creare un gruppo di Office 365

Questo modulo di azione crea un gruppo in Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome visualizzato</td> 
   <td> <p>Immettere o mappare il nome visualizzato dal gruppo nella rubrica.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias per gruppo</td> 
   <td>Immetti o mappa l’alias e-mail per questo gruppo. È possibile includere lettere minuscole, numeri e trattini bassi. Per il tipo di gruppo di Office 365, questo sarà l'alias di posta elettronica del gruppo ([Alias]@[Dominio].onmicrosoft.com). Per il tipo Gruppo di sicurezza, l'alias funziona come nome alternativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di gruppo</td> 
   <td>Specificare se si sta creando un gruppo di Office 365 o un gruppo di sicurezza.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrizione</td> 
   <td>Immettere o mappare una descrizione per questo gruppo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sicurezza abilitata</td> 
   <td>Abilitare questa opzione se si desidera che il gruppo sia protetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Proprietari</td> 
   <td>Selezionare i proprietari per questo gruppo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Membri</td> 
   <td>Selezionare i membri del gruppo.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un team o un gruppo

Questo modulo di azione elimina il team o il gruppo specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID Gruppo</td> 
   <td> <p>Inserisci o mappa l’ID del gruppo da eliminare.</p> 
   </tr> 
 </tbody> 
</table>

#### Ottieni un team

Questo modulo recupera le proprietà e le relazioni per il team Microsoft o il gruppo Office 365 specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID Gruppo</td> 
   <td> <p>Immetti o mappa l’ID del gruppo per il quale desideri recuperare i dettagli.</p> 
   </tr> 
 </tbody> 
</table>

#### Elenca tutti i team e i gruppi

Questo modulo elenca tutti i team dei gruppi Microsoft Teams e Office 365 associati all’organizzazione. Puoi filtrare per restituire solo i risultati che soddisfano i criteri specificati.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>È possibile impostare un filtro per restituire solo i team e i gruppi che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND o OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Impostare il numero massimo di team o gruppi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>


#### Elenca team aggiunti

In questo modulo di azione sono elencati i team a cui l&#39;utente ha unito i membri associati alla connessione utilizzata in questo modulo.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Impostare il numero massimo di team o gruppi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare un team

Questo modulo di azione aggiorna le proprietà dei team specificati nel gruppo Microsoft Teams o Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome visualizzato</td> 
   <td> <p>Immettere o mappare il nome visualizzato dal gruppo nella rubrica.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias per gruppo</td> 
   <td>Immetti o mappa l’alias e-mail per questo gruppo. È possibile includere lettere minuscole, numeri e trattini bassi. Per il tipo di gruppo di Office 365, questo sarà l'alias di posta elettronica del gruppo ([Alias]@[Dominio].onmicrosoft.com). Per il tipo di gruppo Sicurezza, l'alias funziona come nome alternativo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Descrizione</td> 
   <td>Immettere o mappare una descrizione per questo gruppo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sicurezza abilitata</td> 
   <td>Abilitare questa opzione se si desidera che il gruppo sia protetto.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Visibilità</td> 
   <td>Specificare la visibilità del gruppo Office 365.</td> 
  </tr> 
 </tbody> 
</table>

#### Guarda i team

Questo modulo di attivazione avvia uno scenario quando viene creato un team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>È possibile impostare un filtro per controllare solo i team e i gruppi che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND o OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Impostare il numero massimo di team o gruppi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

### Canale

* [Creare un canale](#create-a-channel)
* [Eliminare un canale](#delete-a-channel)
* [Ottieni un canale](#get-a-channel)
* [Elenca canali](#list-channels)
* [Aggiornare un canale](#update-a-channel)

#### Creare un canale

Questo modulo di azione crea un nuovo canale per il team specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Seleziona il team in Microsoft Teams per il quale desideri creare un canale.</p> </td> 
   </tr> 
  <tr> 
   <td>Nome canale</td> 
   <td>Inserisci o mappa un nome per il nuovo canale.</td> 
  </tr> 
  <tr> 
   <td>Descrizione</td> 
   <td>Inserisci o mappa una descrizione per il nuovo canale.</td> 
  </tr> 
 </tbody> 
</table>

#### Eliminare un canale

Questo modulo di azione elimina il canale specificato da un team Microsoft.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Immetti o mappa l’ID del team in Microsoft Teams da cui desideri eliminare un canale.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Inserisci o mappa l’ID del canale da eliminare.</td> 
  </tr> 
  </tbody> 
</table>

#### Ottieni un canale

Questo modulo recupera le proprietà e le relazioni di un canale.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Immetti o mappa l’ID del team in Microsoft Teams a cui appartiene il canale per il quale desideri recuperare i dettagli.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Inserisci o mappa l’ID del canale per cui desideri recuperare i dettagli.</td> 
  </tr> 
  </tbody> 
</table>

#### Elenca canali

In questo modulo sono elencati i canali di proprietà del team specificato in Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Seleziona in Microsoft Teams il team per il quale desideri elencare i canali.</p> </td> 
   </tr> 
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Imposta il numero massimo di canali restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
  </tbody> 
</table>

#### Aggiornare un canale

Questo modulo di azione aggiorna la descrizione del canale specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>In Microsoft Teams, seleziona il team a cui appartiene il canale da aggiornare.</p> </td> 
   </tr> 
  <tr> 
   <td>Nome canale</td> 
   <td>Inserisci o mappa il nome del canale che desideri aggiornare.</td> 
  </tr> 
  <tr> 
   <td>Descrizione</td> 
   <td>Inserisci o mappa la nuova descrizione del canale.</td> 
  </tr> 
 </tbody> 
</table>

### Messaggio

* [Rispondi a un messaggio del canale](#reply-to-a-channel-message)
* [Inviare un messaggio](#send-a-message)
* [Osservare i messaggi](#watch-messages)
* [Guarda le nuove risposte](#watch-new-replies)

#### Rispondi a un messaggio del canale

Questo modulo di azione crea una risposta a un messaggio nel canale specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>In Microsoft Teams, seleziona il team a cui appartiene il canale contenente il messaggio a cui desideri rispondere.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Seleziona il canale contenente il messaggio a cui desideri rispondere.</td> 
  </tr> 
  <tr> 
   <td>ID messaggio</td> 
   <td>Inserisci o mappa l’ID del messaggio a cui desideri rispondere.</td> 
  </tr> 
  <tr> 
   <td>Tipo di contenuto</td> 
   <td>Seleziona se desideri inviare il messaggio in formato testo normale o HTML.</td> 
  </tr> 
  <tr> 
   <td>Messaggio di risposta</td> 
   <td>Inserisci o mappa il corpo del messaggio di risposta che desideri inviare.</td> 
  </tr> 
 </tbody> 
</table>

#### Inviare un messaggio

Questo modulo di azione invia un messaggio al canale di un team o a una chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di messaggio/td&gt; 
   <td> <p>Seleziona se stai inviando un messaggio di canale o un messaggio di chat.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Se invii un messaggio a un canale, immetti o mappa l’ID del team di Microsoft Teams proprietario del canale a cui desideri inviare un messaggio.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Se stai inviando un messaggio a un canale, immetti o mappa l’ID del canale a cui desideri inviare un messaggio.</td> 
  </tr> 
  <tr> 
   <td>Crea una nuova chat</td> 
   <td>Se si invia un messaggio di chat, selezionare se si desidera creare una nuova chat.
   <ul><li><b>Sì</b><p>Seleziona se desideri una chat individuale o di gruppo e seleziona il membro da includere nella chat. È necessario selezionare l'utente associato alla connessione utilizzata da questo modulo e una chat individuale deve contenere solo l'utente e un altro utente.</p><p>Se stai creando una chat di gruppo, puoi impostare un argomento nel campo Argomento.</p>
   <li><b>No</b><p>Inserisci o mappa l’ID del team a cui appartiene il canale a cui desideri inviare un messaggio, quindi immetti o mappa l’ID del canale.</td> 
  </tr> 
  <tr> 
   <td>Messaggio</td> 
   <td>Inserisci o mappa il corpo del messaggio che desideri inviare.</td> 
  </tr> 
  <tr> 
   <td>Tipo di contenuto</td> 
   <td>Seleziona se desideri inviare il messaggio in formato testo normale o HTML.</td> 
  </tr> 
 </tbody> 
</table>

#### Osservare i messaggi

Questo modulo di attivazione avvia uno scenario quando un messaggio viene inviato al canale di un team o a una chat.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipo di messaggi da controllare</td> 
   <td> <p>Seleziona se desideri guardare i messaggi del canale o i messaggi della chat.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>Se stai guardando i messaggi del canale, seleziona il team in Microsoft Teams a cui appartiene il canale che guardi per i messaggi.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Se stai guardando messaggi del canale, seleziona il canale che desideri guardare per i messaggi.</td> 
  </tr> 
  <tr> 
   <td>ID chat</td> 
   <td>Se stai guardando messaggi di chat, seleziona la chat che desideri guardare per i messaggi.</td> 
  </tr> 
  <tr> 
   <td>Numero massimo di messaggi restituiti</td> 
   <td>Impostare il numero massimo di messaggi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

#### Guarda le nuove risposte

Questo modulo di attivazione avvia uno scenario quando viene ricevuta una nuova risposta dal messaggio specificato.

Questo modulo non è disponibile per gli account personali.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID team</td> 
   <td> <p>In Microsoft Teams, seleziona il team a cui appartiene il canale che stai guardando per le risposte.</p> </td> 
   </tr> 
  <tr> 
   <td>ID canale</td> 
   <td>Seleziona il canale da controllare per le risposte.</td> 
  </tr> 
  <tr> 
   <td>ID messaggio</td> 
   <td>Selezionare la chat che si desidera controllare per le risposte.</td> 
  </tr> 
  <tr> 
   <td>Numero massimo di risposte restituito</td> 
   <td>Imposta il numero massimo di risposte che Workfront Fusion restituirà durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

### Membro

* [Aggiungi un membro](#add-a-member)
* [Aggiungere un membro a un gruppo](#add-a-member-to-a-group)

#### Aggiungi un membro

Questo modulo di azione aggiunge un membro a Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome membro</td> 
   <td> <p>Immettere o mappare il nome del membro da aggiungere a Microsoft Teams.</p> </td> 
   </tr> 
  <tr> 
   <td>Password</td> 
   <td>Immettere o mappare la password per il membro.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiungere un membro a un gruppo

Questo modulo di azione aggiunge un membro a un gruppo di Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID Gruppo</td> 
   <td> <p>Selezionare il gruppo al quale si desidera aggiungere un membro.</p> </td> 
   </tr> 
  <tr> 
   <td>ID membro</td> 
   <td>Selezionare il membro da aggiungere al gruppo.</td> 
  </tr> 
 </tbody> 
</table>

### Riunione online

* [Creare una riunione in linea](#create-an-online-meeting)
* [Eliminare una riunione in linea](#delete-an-online-meeting)
* [Ottenere una riunione online](#get-an-online-meeting)
* [Aggiornare una riunione online](#update-an-online-meeting)

#### Creare una riunione in linea

Questo modulo di azione crea una riunione autonoma non associata a un evento nel calendario dell&#39;utente. La riunione non verrà visualizzata nel calendario dell&#39;utente.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Oggetto</td> 
   <td>Immettere o mappare un oggetto per la riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e ora di inizio</td> 
   <td>Immettere o mappare la data e l'ora di inizio della riunione. Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e ora di fine</td> 
   <td>Immettere o mappare la data e l'ora di fine della riunione. Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Presentatori consentiti</td> 
   <td>Selezionare il gruppo che può essere presente alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Partecipanti</td> 
   <td>Per ogni partecipante che si desidera aggiungere alla riunione, fare clic su <b>Aggiungi elemento</b> e selezionare il nome e la mansione del partecipante.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti ai partecipanti di attivare le proprie videocamere</td> 
   <td>Selezionare se si desidera consentire ai partecipanti di attivare le proprie fotocamere.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti ai partecipanti di attivare i microfoni</td> 
   <td>Selezionare se si desidera consentire ai partecipanti di attivare i propri microfoni.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti chat riunione</td> 
   <td>Selezionare se si desidera che la chat di riunione sia abilitata, disabilitata o limitata alla durata della convocazione di riunione</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti reazioni dei team</td> 
   <td>Selezionare se si desidera abilitare le reazioni dei team per questa riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID Thread</td> 
   <td>Immettere o mappare l'ID di un thread associato alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID messaggio</td> 
   <td>Immettere o mappare l'ID di un messaggio associato alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID messaggio catena di risposta</td> 
   <td>Immettere o mappare l'ID della catena di risposte associata alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Annuncio di entrata e uscita</td> 
   <td>Specificare se si desidera che la riunione venga annunciata quando i partecipanti entrano o escono.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Limite</td> 
   <td>Selezionare il gruppo di partecipanti che possono evitare di attendere nella sala d'attesa. Questi partecipanti parteciperanno direttamente alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti agli utenti con accesso remoto di ignorare la sala d'attesa</td> 
   <td>Selezionare se consentire agli utenti di accesso remoto di ignorare la sala d'attesa.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Registra automaticamente</td> 
   <td>Selezionare se si desidera registrare automaticamente la riunione.</td> 
   </tr> 
   </tbody> 
</table>

#### Eliminare una riunione in linea

Questo modulo di azione elimina la riunione online con l&#39;ID specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID riunione</td> 
   <td> <p>Immettere o mappare l'ID della riunione che si desidera eliminare.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Ottenere una riunione online

Questo modulo di azione recupera i dettagli della riunione online con l&#39;ID specificato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID riunione</td> 
   <td> <p>Immettere o mappare l'ID della riunione per la quale si desidera recuperare i dettagli.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Aggiornare una riunione online

Questo modulo di azione aggiorna la riunione online con l&#39;ID specificato.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID riunione</td> 
   <td>Immettere o mappare l'ID della riunione che si desidera aggiornare.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Oggetto</td> 
   <td>Immettere o mappare un oggetto per la riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e ora di inizio</td> 
   <td>Immettere o mappare la data e l'ora di inizio della riunione. Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Data e ora di fine</td> 
   <td>Immettere o mappare la data e l'ora di fine della riunione. Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Presentatori consentiti</td> 
   <td>Selezionare il gruppo che può essere presente alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Partecipanti</td> 
   <td>Per ogni partecipante che si desidera aggiungere alla riunione, fare clic su <b>Aggiungi elemento</b> e selezionare il nome e la mansione del partecipante.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti ai partecipanti di attivare le proprie videocamere</td> 
   <td>Selezionare se si desidera consentire ai partecipanti di attivare le proprie fotocamere.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti ai partecipanti di attivare i microfoni</td> 
   <td>Selezionare se si desidera consentire ai partecipanti di attivare i propri microfoni.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti chat riunione</td> 
   <td>Selezionare se si desidera che la chat di riunione sia abilitata, disabilitata o limitata alla durata della convocazione di riunione</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti reazioni dei team</td> 
   <td>Selezionare se si desidera abilitare le reazioni dei team per questa riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID Thread</td> 
   <td>Immettere o mappare l'ID di un thread associato alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID messaggio</td> 
   <td>Immettere o mappare l'ID di un messaggio associato alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID messaggio catena di risposta</td> 
   <td>Immettere o mappare l'ID della catena di risposte associata alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Annuncio di entrata e uscita</td> 
   <td>Specificare se si desidera che la riunione venga annunciata quando i partecipanti entrano o escono.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Limite</td> 
   <td>Selezionare il gruppo di partecipanti che possono evitare di attendere nella sala d'attesa. Questi partecipanti parteciperanno direttamente alla riunione.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Consenti agli utenti con accesso remoto di ignorare la sala d'attesa</td> 
   <td>Selezionare se consentire agli utenti di accesso remoto di ignorare la sala d'attesa.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Registra automaticamente</td> 
   <td>Selezionare se si desidera registrare automaticamente la riunione.</td> 
   </tr> 
   </tbody> 
</table>

### Altro

* [Verificare la presenza di utenti](#check-presence-of-users)
* [Effettuare una chiamata API personalizzata](#make-a-custom-api-call)
* [Cerca utenti](#search-users)

#### Verificare la presenza di utenti

Questo modulo di azione controlla se gli utenti selezionati sono presenti su Microsoft Teams.

Questo modulo non supporta gli account personali.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID utente</td> 
   <td> <p>Selezionare gli utenti per i quali si desidera verificare la presenza.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una richiesta personalizzata all’API Microsoft Teams.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
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

#### Cerca utenti

Questo modulo cerca gli utenti utilizzando i criteri specificati.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione </td> 
   <td> <p>Per istruzioni sulla connessione dell'account Microsoft Teams a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtro</td> 
   <td> <p>Puoi impostare un filtro per restituire solo gli utenti che soddisfano i criteri selezionati.</p> <p>Per ogni filtro, immetti il campo che desideri che il filtro valuti, l’operatore e il valore che desideri che il filtro consenta. Puoi utilizzare più di un filtro aggiungendo regole AND o OR.</p> </td> 
   </tr> 
  <tr> 
   <td>Numero massimo di risultati restituiti</td> 
   <td>Impostare il numero massimo di team o gruppi restituiti da Workfront Fusion durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>



