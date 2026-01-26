---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Utilizzare i modelli per collegare Adobe Workfront Fusion e Jira
description: Utilizza questi modelli per automatizzare i flussi di lavoro tra Adobe Workfront Fusion e Jira.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ede5c7a75725a6540d6a8ff9cd056e6147d5c55
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 3%

---

# Utilizzare i modelli per collegare Adobe Workfront Fusion e Jira

Adobe Workfront Fusion offre modelli in grado di automatizzare flussi di lavoro comuni tra Fusion e Jira.

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Workfront: se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</p><p>Jira: devi disporre di una licenza per Jira Cloud</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurazioni del livello di accesso</td> 
   <td> <p>Workfront: autorizzazione per creare utenti, moduli personalizzati e campi personalizzati.</p> <p>Jira: autorizzazioni per creare utenti e campi personalizzati e per modificare schermate e webhook.</td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisiti

### Workfront

* È necessario disporre di un account tecnico in Adobe Developer Console.

  Per informazioni e istruzioni, consulta [Configurazione account tecnico](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) nella documentazione di Adobe.
* È necessario applicare le autorizzazioni di amministratore di sistema all&#39;account tecnico nell&#39;area Profili di prodotto di Adobe Admin Console.

  Per informazioni e istruzioni, vedere [Creazione di amministratori di sistema in Workfront con Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira

Se utilizzi l&#39;autorizzazione OAuth2 per Jira (scelta consigliata), devi configurare un&#39;applicazione OAuth2 all&#39;indirizzo [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Per informazioni e istruzioni, consulta [Creare una connessione OAuth2 a Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira) nell&#39;articolo Moduli Jira.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## Presupposti

Questi moduli presuppongono quanto segue:

* Workfront è la fonte di verità del progetto complessivo della campagna di marketing
* Jira è utilizzato da team tecnici, che realizzano parte di un progetto avviato in Workfront.
* Non tutti gli utenti Jira hanno accesso a Workfront o viceversa.
* Workfront e Jira sono ospitati nel cloud.

## Modello dati (mappature campi)


| Workfront | Jira | Direzione | Note |
|---|---|---|---|
| ObjId | ID WF* | WF → Jira | Alla Creazione Del Problema Jira |
| Chiave Jira* | Chiave problema | Jira → WF | Alla Creazione Del Problema Jira |
| URL Jira* | - | Jira → WF | Collegamento cliccabile da WF a Jira |
| - | Collegamento WF* | WF → Jira | Collegamento cliccabile in Jira a WF |
| Nome | Riepilogo | WF → Jira |  |
| Descrizione | Descrizione | WF → Jira |  |
| Stato | Stato WF | WF → Jira | Stato WF |
| Stato Jira* | Stato | Jira → WF | Stato Jira |
| Data di completamento Pianificata | Data di scadenza | WF → Jira | Data di completamento Pianificata |
| Note | Commenti | WF ↔ Jira | Copia bidirezionale |
| Documento | Allegato | WF → Jira | Come allegati sulla creazione del problema e commenti sui nuovi documenti dopo la creazione. |

\* Questi campi sono configurati come parte di questa configurazione dell’integrazione. Per istruzioni, vedere [Configurare i prerequisiti in Workfront, Jira e Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion).

## Configurare i prerequisiti in Workfront, Jira e Workfront Fusion

Per utilizzare i modelli di integrazione Jira, è necessario eseguire le seguenti configurazioni:

* [Configurare Jira](#configure-jira)
* [Configurare Workfront](#configure-workfront)
* [Configurare le connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion)

### Configurare Jira

Per utilizzare questi moduli, è necessario creare quanto segue in Jira:

* Un utente dell’integrazione del sistema
* Tre campi personalizzati specifici

#### Creare un utente di integrazione del sistema in Jira

1. In Jira, crea un utente specifico denominato Utente di integrazione del sistema. Questo utente deve essere utilizzato solo da Workfront Fusion e non deve rappresentare un utente umano. Le credenziali di questo utente verranno utilizzate dalle connessioni di Workfront Fusion.

#### Creare i campi personalizzati necessari in Jira

Questa integrazione prevede tre campi specifici nell’account Jira a cui si connette. Senza questi campi, l’integrazione non avrà successo

1. In Jira, vai a **Impostazioni** (icona ingranaggio) e seleziona **Elementi di lavoro**.
1. Nel menu di navigazione a sinistra, seleziona **Campi personalizzati**.
1. Nell&#39;angolo superiore destro dello schermo fare clic su **Crea campo personalizzato.**
1. Crea i campi seguenti:

   | Nome campo | Tipo di campo |
   |---|---|
   | ID WF | Campo di testo (riga singola) |
   | Stato WF | Campo di testo (riga singola) |
   | Collegamento WF | Campo URL |

   Per informazioni sulla creazione di collegamenti in Jira, consulta la documentazione di Jira sulla creazione di campi.
1. Aggiungi i nuovi campi creati alla schermata associata al progetto Jira.

   Per informazioni sulle schermate in Jira, consulta la documentazione di Jira sulla configurazione delle schermate degli elementi di lavoro.


### Configurare Workfront

Per utilizzare questi moduli, è necessario creare quanto segue in Workfront:

* Un utente dell’integrazione del sistema
* Un modulo personalizzato specifico

#### Creazione di un utente di integrazione del sistema in Workfront

1. In Workfront, crea un utente di System Integration. Questo utente viene utilizzato solo da Workfront Fusion e non rappresenta un utente umano. Le attività assegnate a questo utente attiveranno lo scenario che sincronizza Workfront con Jira.

   Per istruzioni, consulta [Aggiungere utenti](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) nella documentazione di Workfront.

#### Creare un modulo personalizzato in Workfront

1. In Workfront, inizia a creare un modulo personalizzato.

   Per istruzioni, consulta [Creare un modulo personalizzato](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) nella documentazione di Workfront.
1. Denomina il modulo &quot;**Campi JIRA**&quot;.
1. Includi i campi seguenti nel modulo personalizzato:

| Nome campo | Tipo di campo |
|---|---|
| Chiave Jira | Campo di testo a riga singola |
| URL Jira | Campo di testo a riga singola |
| Stato Jira | Campo di testo a riga singola |

1. Aggiungi eventuali campi aggiuntivi da mappare tra Jira e Workfront.
1. Salva il modulo personalizzato.

>[!NOTE]
>
>È consigliabile limitare questo modulo alle modifiche apportate da altri utenti. A tale scopo, è necessario assicurarsi che tutti gli utenti aggiunti al modulo personalizzato dispongano del solo accesso in visualizzazione.
>
>Per istruzioni, consulta [Condividere un modulo personalizzato](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) nella documentazione di Workfront.

### Configurare le connessioni in Workfront Fusion

Prima di poter creare le connessioni, è necessario aver creato gli utenti di System Integration in Jira e Workfront.

Quando crei queste connessioni, assicurati di utilizzare le credenziali degli utenti di Integrazione di sistema creati.

Se lo desideri, puoi creare queste connessioni come parte della configurazione dei modelli.

* Per istruzioni sulla creazione di una connessione a Workfront, vedere [Connettere Workfront a Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) nell&#39;articolo Moduli Workfront.
* Per istruzioni sulla creazione di una connessione a Jira, vedere [Connettere Jira a Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) nell&#39;articolo Moduli software Jira.


## Scenari

Otto modelli pronti per l’utilizzo per Jira hanno lo scopo di aiutare a replicare i flussi di lavoro comuni e accelerare l’implementazione. I modelli sono completamente personalizzabili per soddisfare specifiche esigenze aziendali e possono essere estesi in base all&#39;evoluzione dei requisiti.

Non è necessario implementare tutti gli scenari. L’implementazione minima richiederebbe lo Scenario 1, che creerebbe un’integrazione unidirezionale a un problema JIRA da un’assegnazione in Workfront.  È possibile aggiungere altri scenari per aumentare la robustezza e l&#39;interconnettività bidirezionale tra Workfront e JIRA.  Puoi anche creare scenari aggiuntivi per gestire casi come un’integrazione da progetto a epico o un problema JIRA per problemi o attività di Workfront.

Qualsiasi utilizzo di questi modelli o estensioni è considerato una configurazione personalizzata e per supporto e implementazione consigliamo di utilizzare Adobe Professional Services o un partner Adobe.

* **[Da Workfront a Jira: crea un problema JIRA dall&#39;attività o dall&#39;assegnazione di un problema Workfront](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA a Workfront: JIRA a Workfront: Inviare aggiornamenti su problemi e commenti da Jira a Workfront](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront a Jira: cambia l’attività di Workfront in problema JIRA](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront a Jira: modifiche al problema Workfront a problema JIRA](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront a Jira: crea un commento in JIRA quando una nuova nota sull’attività o sul problema di Workfront](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront a Jira: Creare un commento in JIRA sulla nota eliminata su attività o problema Workfront](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [Workfront a Jira: crea un commento in JIRA quando un nuovo documento su un’attività o un problema Workfront](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [Workfront a Jira: Creare un commento in JIRA su un documento eliminato su un’attività o un problema di Workfront](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### Parametri generali

Durante la configurazione di questi modelli, utilizza i seguenti parametri generali:

* **JiraBaseURL**: URL di base per l&#39;istanza Jira. Esempio: `https://myjira.atlassian.net/`
* **wfBaseURL**: URL di base per l&#39;istanza di Workfront.  In genere: `https://<domain>.my.workfront.com` dove `<domain>` è il nome di dominio di Workfront specifico.
* **defaultJIRAReporterID**: ID dell&#39;utente in JIRA che crea problemi. (Esempio: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
Per ottenere questo ID, effettua una delle seguenti operazioni:
   * Fai clic sul profilo dell’utente in JIRA e controlla l’URL nel browser.
(Esempio`https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * Esegui la seguente chiamata API sull’istanza JIRA per ottenere l’ID per l’account specifico in JIRA:
     `GET /rest/api/3/user/search?query=email@example.com`


### Scenario 1: da Workfront a Jira: creare un problema JIRA dall’assegnazione di un’attività o di un problema Workfront

Questo scenario crea un problema Jira quando un’attività o un problema Workfront viene assegnato all’utente di integrazione del sistema. Lo scenario viene compilato nei campi Riepilogo, Descrizione, Data scadenza, Stato WF e ID WF. Dopo la creazione del problema, questo scenario carica anche l’elenco degli allegati e la cronologia delle note relative all’attività o al problema originale in Workfront.

Se viene assegnata un’attività Workfront, il problema in Jira è un’attività. Se viene assegnato un problema Workfront, il problema Jira è un bug.

+++**Espandi per visualizzare le istruzioni per configurare lo scenario 1:Workfront in Jira: crea un problema JIRA dall&#39;attività di Workfront o dall&#39;assegnazione del problema**

#### Configurare il modulo trigger

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fai clic sul modello **Workfront to Jira: Create JIRA issue from Workfront task or issue assignment** (Da a Jira: crea problema JIRA dall&#39;attività o dall&#39;assegnazione di un problema di).

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Selezionare la connessione Workfront creata in [Configurare le connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion).
1. Nel campo **Tipo di record**, selezionare `Assignment`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le operazioni seguenti, utilizzando l&#39;opzione **And**:

   | Campo | Operatore | Valore |
   |---|---|---|
   | assignedToID | Uguale a | (Immetti l&#39;ID Workfront dell&#39;utente di System Integration). |
   | TaskID | Esiste |  |
   | projectID | Uguale a | (Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli) |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare Solo nuovo record.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. Continua a [Connettere i moduli modello a Workfront e Jira](#connect-template-modules-to-workfront-and-jira)

#### Collegare i moduli modello a Workfront e Jira

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront creata in [Configura connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion), quindi fare clic su **OK** per salvare la connessione a tale modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Workfront creata in [Configura connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion), quindi fare clic su **OK** per salvare la connessione a tale modulo.
1. Continuare ad [Aggiornare il modulo Parametri generali](#update-the-general-parameters-module).

#### Aggiornare il modulo Parametri generali

1. Nel secondo modulo del modello (Imposta dettagli ambiente), per ciascuna delle seguenti variabili, fare clic su **Aggiungi elemento** e immettere il nome e il valore della variabile

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Immetti l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Inserisci l’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | Immetti l’URL di base dell’account Workfront a cui ti stai connettendo. |

1. Continua con [Mappa campi personalizzati in Jira](#map-custom-fields-in-jira)

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### Scenario 2: da JIRA a Workfront: invia aggiornamenti sui problemi e commenti a Workfront da Jira

Questo scenario crea un’attività o un problema Workfront quando si crea un problema in Jira.

>[!NOTE]
>
>Questo scenario richiede una connessione OAuth2 per Jira.
>Per utilizzare l&#39;autorizzazione OAuth2 per Jira, è necessario configurare un&#39;applicazione OAuth2 in [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Per informazioni e istruzioni, consulta la documentazione di Jira.

+++**Espandi per visualizzare le istruzioni per la configurazione dello Scenario 2: JIRA in Workfront: invia aggiornamenti sui problemi e commenti a Workfront da Jira**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fai clic sul modello **Part 2: JIRA to Workfront: Send updates on issues and comments back to Workfront from Jira** (Invia aggiornamenti sui problemi e i commenti a da Jira).

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Seleziona una connessione che utilizza le credenziali per l’utente di Integrazione di sistema oppure crea una connessione a Jira con le credenziali di Integrazione di sistema.

* Per istruzioni sulla creazione di una connessione a Jira, vedere [Connettere Jira a Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) nell&#39;articolo Moduli software Jira.

1. Configurare il filtro webhook

1. Continua a [Configurare un webhook in Jira](#configure-a-webhook-in-jira)

#### Configurare un webhook in Jira

1. In Jira, crea un webhook.

   Per istruzioni, consulta [Webhook](https://developer.atlassian.com/server/jira/platform/webhooks/) nella documentazione di Jira.

1. Durante la configurazione del webhook, utilizza i seguenti valori:

   * **JQL**: progetto = &quot;yourProjectName&quot; (dove yourProjectName = nome del progetto JIRA)
   * **Problema**: creato, aggiornato
   * **Commento**: creato, eliminato


1. Continua con [Connetti moduli modello a Workfront e Jira (Modulo 2)](#connect-template-modules-to-workfront-and-jira-module-2)

#### Collegare i moduli modello a Workfront e Jira (Modulo 2)

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront creata in [Configura connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion), quindi fare clic su **OK** per salvare la connessione a tale modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Workfront creata in [Configura connessioni in Workfront Fusion](#configure-connections-in-workfront-fusion), quindi fare clic su **OK** per salvare la connessione a tale modulo.
   <!--#### Map custom fields-->

+++

### Scenario 3: da Workfront a Jira: cambia l’attività di Workfront in problema JIRA

+++**Espandi per visualizzare le istruzioni per la configurazione dello scenario 3: modifiche da WF a Jira (attività)**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fare clic sul modello **Part 3: Workfront to Jira: Changes to Workfront task to JIRA issue**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.

1. Fai clic sul modello per accedere all’editor.
1. Seleziona l’organizzazione e il team a cui appartiene questo scenario.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Task`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le operazioni seguenti, utilizzando l&#39;opzione **And**:

   | Campo | Operatore | Valore |
   |---|---|---|
   | assignedToID | Uguale a | Immetti l&#39;ID Workfront dell&#39;utente di System Integration. |
   | projectID | Uguale a | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |
   | DE: Chiave Jira | Esiste |  |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `Updated record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. Nel modulo **Imposta variabili JIRA**, imposta le seguenti variabili, quindi fai clic su **OK** per salvare il modulo.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.

+++

### Scenario 4: da Workfront a Jira: modifiche al problema Workfront al problema JIRA

Questo scenario invia aggiornamenti dai problemi di Workfront ai problemi JIRA precedentemente connessi.

+++**Espandi per visualizzare le istruzioni per la configurazione dello Scenario 4: da Workfront a Jira: modifiche al problema Workfront al problema JIRA**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fai clic sul modello **Scenario 4: WF-to-Jira Changes (Issues)**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.

1. Fai clic sul modello per accedere all’editor.
1. Seleziona l’organizzazione e il team a cui appartiene questo scenario.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Issues`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le operazioni seguenti, utilizzando l&#39;opzione **And**:

   | Campo | Operatore | Valore |
   |---|---|---|
   | assignedToID | Uguale a | Immetti l&#39;ID Workfront dell&#39;utente di System Integration. |
   | projectID | Uguale a | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |
   | DE: Chiave Jira | Esiste |  |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `Updated record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. Nel modulo **Imposta variabili JIRA**, imposta le seguenti variabili, quindi fai clic su **OK** per salvare il modulo.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.

+++

### Scenario 5: da Workfront a Jira: creare un commento in JIRA quando viene aggiunta una nota sull’attività o sul problema di Workfront

+++**Espandi per visualizzare le istruzioni per la configurazione dello Scenario 5: da Workfront a Jira: crea un commento in JIRA quando viene aggiunta una nota sull&#39;attività o sul problema di Workfront**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fai clic sul modello **Scenario 5: WF-to-Jira New Notes (Tasks and Issues)**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Note`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le seguenti operazioni:

   | Campo | Operatore | Valore |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |
   | O |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `New record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. Nel modulo **Imposta variabili**, imposta le seguenti variabili, quindi fai clic su **OK** per salvare il modulo.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.

+++

### Scenario 6: da Workfront a Jira: creare un commento in JIRA su una nota eliminata su un’attività o un problema di Workfront

+++**Espandi per visualizzare le istruzioni per la configurazione dello scenario 6: da Workfront a Jira: crea un commento in JIRA sulla nota eliminata sull&#39;attività o sul problema di Workfront**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fare clic sul modello **Scenario 6: WF-to-Jira Remove notes (Tasks and Issues)**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Note`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le seguenti operazioni:

   | Campo | Operatore | Valore |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |
   | O |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `Deleted record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. Nel secondo modulo, imposta le seguenti variabili, quindi fai clic su **OK** per salvare il modulo.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.

+++

### Scenario 7: da Workfront a Jira: creare un commento in JIRA quando si crea un nuovo documento su un’attività o un problema di Workfront

+++**Espandi per visualizzare le istruzioni per la configurazione dello Scenario 7: da Workfront a Jira: crea un commento in JIRA quando si crea un nuovo documento su attività o problema di Workfront**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fare clic sul modello **Scenario 7: WF-to-Jira New Attachments (Tasks and Issues)**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Document`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le operazioni seguenti, utilizzando l&#39;opzione **And**:

   | Campo | Operatore | Valore |
   |---|---|---|
   | assignedToID | Uguale a | Immetti l&#39;ID Workfront dell&#39;utente di System Integration. |
   | projectID | Uguale a | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |

1. Nel secondo modulo, imposta le seguenti variabili.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `New record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.

+++

### Scenario 8: da Workfront a Jira: creare un commento in JIRA su un documento eliminato per un’attività o un problema di Workfront

+++**Espandi per visualizzare le istruzioni per la configurazione dello Scenario 8: da Workfront a Jira: crea un commento in JIRA sul documento eliminato per l&#39;attività o il problema di Workfront**

1. Fai clic sulla scheda **Modelli** ![icona Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Cercare il modello utilizzando la barra di ricerca nell&#39;angolo superiore sinistro dello schermo. Puoi eseguire ricerche per nome del modello o per applicazioni incluse.
1. Fare clic sul modello **Scenario 8: WF-to-Jira Remove Attachments (Tasks and Issues)**.

   Viene visualizzata una vista del modello che mostra informazioni e un&#39;animazione del flusso di dati.
1. Nel primo modulo, inizia ad aggiungere un webhook.
1. Nel campo Connessione selezionare la connessione Workfront che utilizza le credenziali di integrazione di sistema.
1. Nel campo **Tipo di record**, selezionare `Document`.
1. Nel campo **Stato**, selezionare `New state`.
1. Configura il filtro con le seguenti operazioni:

   | Campo | Operatore | Valore |
   |---|---|---|
   | projectID<br>AND<br>TaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |
   | O |  |  |
   | projectID<br>AND<br>OpTaskID | Equals<br><br>Esiste | Immetti l’ID del progetto o dei progetti che desideri che il webhook controlli. |

1. Nel modulo **Imposta variabili**, imposta le seguenti variabili.

   | Nome variabile | Valore variabile |
   |---|---|
   | defaultJiraReporterID | Questo è l’ID dell’utente predefinito quando l’Utente Creatore non esiste in Jira. Per trovare questo ID utente fai clic sul profilo dell’utente e controlla l’URL del browser. Esempio: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | L’URL di base dell’account Jira a cui ti stai connettendo. |
   | wfBaseURL | L’URL di base dell’account Workfront a cui ti stai connettendo. |

1. Abilita l&#39;opzione **Escludi aggiornamenti effettuati da questa connessione**.
1. Nel campo **Origine record**, selezionare `Deleted record only`.
1. Fai clic su **Salva** per salvare il webhook, quindi fai clic su **OK** per salvare il modulo trigger.
1. In **ogni** modulo Workfront, nel campo Connessione, selezionare la connessione Workfront che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.
1. In **ogni** modulo Jira, nel campo Connessione, selezionare la connessione Jira che utilizza le credenziali di integrazione del sistema, quindi fare clic su **OK** per salvare il modulo.


+++

