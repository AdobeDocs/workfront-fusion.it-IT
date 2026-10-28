---
title: Moduli Adobe CX Enterprise Coworker
description: Utilizza il connettore Adobe CX Enterprise Coworker in Adobe Workfront Fusion per inviare un prompt in linguaggio naturale a Collaboratore e utilizzarne la risposta in uno scenario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 6%
---
# Moduli Adobe CX Enterprise Coworker

Utilizza il connettore Adobe CX Enterprise Coworker in Adobe Workfront Fusion per inviare un prompt in linguaggio naturale a Collaboratore e utilizzarne la risposta in uno scenario. Il collaboratore interpreta la richiesta e può utilizzare gli strumenti disponibili nel tuo account per eseguire il lavoro.

Il connettore fornisce due moduli:

* **[!UICONTROL Esegui una richiesta]** avvia una nuova richiesta e, per impostazione predefinita, attende il risultato.
* **[!UICONTROL Ottieni stato esecuzione]** controlla una richiesta avviata in precedenza.

## Requisiti di accesso

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisiti

Devi disporre di un account Adobe con accesso ad Adobe CX Enterprise Coworker.

## Collegare Adobe CX Enterprise Coworker a Workfront Fusion

Accedi con un account Adobe che abbia accesso a Coworker e a tutti i servizi necessari per la richiesta.

Per creare una connessione:

1. Nel modulo MCP di Adobe Fusion, fai clic su **[!UICONTROL Aggiungi]** accanto al campo **Connessione**.
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
        <td>
          <p>Immettere o mappare un override facoltativo per questa connessione. In caso contrario, utilizza l’ID client gestito dalla piattaforma di questo tipo di account. Registra l’URL di callback di Fusion visualizzato per l’account Collaboratore dedicato.</p>
        </td>
      <tr>
        <td role="rowheader">Segreto client</td>
        <td>
          <p>Immettere o mappare un override facoltativo per questa connessione. In caso contrario, utilizza il clientSecret gestito dalla piattaforma di questo tipo di account. Utilizza le credenziali rilasciate per l’ambiente IMS configurato.</p>
        </td>
    </tbody>
   </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua).

Se non riesci ad accedere o utilizzare un servizio richiesto, contatta l’amministratore.

## Moduli Adobe CX Enterprise Coworker e relativi campi

>[!WARNING]
>
>Non includere mai password o altre credenziali in un prompt.

### Ottieni stato esecuzione

Questo modulo di azione controlla lo stato corrente di un&#39;attività avviata da **[!UICONTROL Esegui un prompt]**.

Questo modulo controlla l’operazione una sola volta. Non avvia una nuova attività o continua a controllarla fino al completamento dell’attività. Se il risultato è ancora in sospeso, controlla di nuovo più tardi.

>[!NOTE]
>
>Non convertire l&#39;ID attività in un numero, arrotondarlo o riformattarlo. Se Collaboratore ha risposto immediatamente al prompt originale senza un ID attività, non è necessario controllare lo stato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Facoltativo, avanzato)</i></td> 
   <td> <p>Questa opzione è disattivata per impostazione predefinita. Includi nell’output la risposta completa del Collaboratore. La risposta potrebbe contenere informazioni riservate.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Selezionare la stessa connessione utilizzata nell'esecuzione <b>[!UICONTROL Run a Prompt]</b> originale.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID attività]</td> 
   <td> <p>Mappa l'ID attività restituito da <b>[!UICONTROL Esegui un prompt]</b>. Mantenerlo come testo esattamente come restituito.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Esegui una richiesta

Questo modulo di azione invia un’istruzione a Collaboratore, ad esempio per riepilogare il testo o raccogliere informazioni utilizzando gli strumenti disponibili sul tuo account.

Ogni esecuzione invia il prompt una volta e avvia una nuova conversazione. Non è necessario selezionare un modello di IA o fornire una chiave del provider di IA separata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione]</td> 
   <td> <p>Seleziona la tua connessione a Collaboratore. Per istruzioni, vedere <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Connettere Adobe CX Enterprise Coworker a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL User Prompt]</td> 
   <td> <p>Immetti l’istruzione. È possibile utilizzare più linee e mappare le informazioni dei moduli precedenti.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendi completamento] <i>(Facoltativo, avanzato)</i></td> 
   <td> <p>Questa opzione è attivata per impostazione predefinita. Abilita questa opzione se desideri che il modulo attenda il completamento dell’attività o richieda attenzione. Disattivarla per restituire immediatamente il risultato iniziale.</p><p>Per ulteriori informazioni, vedere <a href="#wait-for-completion">Attendere il completamento</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Facoltativo, avanzato)</i></td> 
   <td> <p>Questa opzione è disattivata per impostazione predefinita. Abilita questa opzione se desideri che il modulo includa nell’output la risposta completa del Collaboratore. La risposta potrebbe contenere informazioni riservate.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> Ti consigliamo di lasciare inattivo **[!UICONTROL Includi risultato non elaborato]** a meno che tu non abbia bisogno della risposta completa per uno scopo specifico. I risultati non elaborati potrebbero contenere informazioni sensibili e non rappresentano un record completo garantito di ogni azione. Esaminare il contenuto di un risultato non elaborato prima di salvarlo, condividerlo o passarlo a un altro servizio.

#### Attendere il completamento

Quando **[!UICONTROL Attendi completamento]** è attivo, il modulo controlla l&#39;attività dopo un&#39;attesa di cinque secondi. Se l&#39;operazione è ancora in sospeso, il modulo attende altri cinque secondi prima di eseguire di nuovo il controllo. Ogni controllo richiede anche del tempo per ricevere una risposta. La verifica dello stato non invia nuovamente la richiesta.

L&#39;attesa si interrompe quando l&#39;attività viene completata, non riesce, viene annullata o rifiutata oppure è necessario l&#39;input o l&#39;autorizzazione dell&#39;utente. Se Collaboratore fornisce una risposta immediata, il modulo la restituisce senza ulteriori controlli.

Quando **[!UICONTROL Attendi completamento]** è disattivato, il modulo restituisce il primo risultato senza attendere il completamento dell&#39;attività. Ispeziona **[!UICONTROL Stato]**, **[!UICONTROL Completato]** e **[!UICONTROL Richiede attenzione]** per decidere cosa fare dopo. Un&#39;attività può essere già completata quando arriva il primo risultato.

L’attesa è soggetta al timeout del modulo di Fusion. Se il modulo si interrompe o si interrompe, è possibile che Collaborator continui a lavorare. In tal caso, potrebbe non essere possibile ricevere un output o un ID attività.

Per un lavoro più lungo, disattiva l&#39;attesa e salva l&#39;**[!UICONTROL ID attività]** iniziale in modo da poter controllare l&#39;attività in un secondo momento. Non eseguire di nuovo automaticamente il prompt dopo un timeout. La prima richiesta potrebbe essere già in corso e la sua ripetizione potrebbe duplicare le modifiche.


## Uscita modulo

Entrambi i moduli restituiscono le seguenti informazioni quando vengono completati senza errori.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID attività]</td> 
   <td> <p>Identifica l’attività. Questo campo è vuoto se Collaboratore fornisce una risposta immediata senza creare un'attività. Utilizzare questo valore con <b>[!UICONTROL Get Execution Status]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID contesto]</td> 
   <td> <p>Identifica la conversazione. Non è un input per continuare la conversazione.</p><p>Per ulteriori informazioni, vedere <a href="#use-previous-answers">Utilizzare le risposte precedenti</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stato]</td> 
   <td> <p>Stato corrente dell'attività. Vedi <a href="#task-states" class="MCXref xref">Stati attività</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL completato]</td> 
   <td> <p>True quando l'attività viene completata o Collaboratore fornisce una risposta immediata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL richiede attenzione]</td> 
   <td> <p>True quando il collega ha bisogno di input o autorizzazione.</p><p>Per ulteriori informazioni, vedere <a href="#requests-that-need-attention">Richieste che richiedono attenzione</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo finale dell'assistente]</td> 
   <td> <p>Risposta finale al completamento dell'attività. Questo campo è vuoto quando l'attività è in sospeso o richiede attenzione. Una risposta completata può anche non avere un testo di risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artefatti di testo (può includere testo intermedio)]</td> 
   <td> <p>Testo restituito durante il lavoro. Ogni elemento può includere un ID artefatto, un nome e un testo. Questi elementi non sono necessariamente risposte finali.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Raw result (opt-in)]</td> 
   <td> <p>La risposta completa. Questo è incluso solo quando <b>[!UICONTROL Include raw result]</b> è attivo.</p> </td> 
  </tr> 
 </tbody> 
</table>

Utilizza **[!UICONTROL il testo finale dell&#39;assistente]** per la risposta invece di combinare tutti gli artefatti di testo. Gli artefatti possono includere descrizioni dell’avanzamento o altro testo intermedio.

### Richieste che richiedono attenzione

Il collaboratore potrebbe aver bisogno di ulteriori informazioni o autorizzazioni prima di continuare. In questo caso, **[!UICONTROL Richiede attenzione]** è true e **[!UICONTROL Completed]** è false. Instrada il risultato a una persona invece di trattarlo come lavoro completato.

Questi moduli non possono rispondere a una domanda di follow-up né approvare un’azione per tuo conto. **[!UICONTROL Ottieni stato esecuzione]** può verificare se lo stato dell&#39;attività è cambiato, ma non risolve la richiesta di input o autorizzazione.

### Usa le risposte precedenti

Ogni **[!UICONTROL Esegui una richiesta]** avvia una nuova conversazione. Per fare riferimento a una risposta precedente, includere la domanda e la risposta pertinenti come testo nel nuovo prompt. In questo modo viene fornito il contesto di Collaboratore, ma non viene ripresa la conversazione precedente.

**[!UICONTROL ID contesto]** identifica la conversazione associata al risultato. Non è possibile fornirlo a questi moduli per continuare una conversazione.

>[!IMPORTANT]
>
>**[!UICONTROL Completato]** non garantisce la riuscita dell&#39;azione aziendale richiesta. Ad esempio, Collaboratore potrebbe terminare spiegando che uno strumento richiesto non era disponibile. Rivedi la risposta e verifica eventuali risultati richiesti prima di intraprendere l’azione successiva.

### Stati attività

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>L'attività è in sospeso. <b>[!UICONTROL Completed]</b> è false. <b>[!UICONTROL Esegui un prompt]</b> continua ad attendere quando è in attesa. In caso contrario, salva l’ID attività e controlla più tardi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Completed]</b> è true. Rivedi <b>[!UICONTROL Testo finale assistente]</b> e il risultato previsto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>L'attività richiede attenzione. <b>[!UICONTROL Completato]</b> è falso e <b>[!UICONTROL Richiede attenzione]</b> è vero. L'attesa si interrompe. Instradare il risultato per la revisione umana.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>Il modulo riporta un errore invece di un risultato normale.</p> </td> 
  </tr> 
 </tbody> 
</table>

Un risultato in sospeso, o un risultato che richiede attenzione, non è un completamento riuscito, anche se il modulo restituisce senza errore.

## Esempi

### Riepilogare un aggiornamento

1. Aggiungi **[!UICONTROL Esegui una richiesta]** e seleziona la connessione.
1. Immetti quanto segue nel campo **[!UICONTROL Prompt utente]**:

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. Lascia **[!UICONTROL Attendere il completamento]** e **[!UICONTROL Includi risultato non elaborato]** disattivato.
1. Se **[!UICONTROL Richiede attenzione]** è true, instradare il risultato per la revisione umana. Se **[!UICONTROL Completed]** è true, mappa **[!UICONTROL Testo assistente finale]** nel passaggio successivo.

Il testo generato dall’intelligenza artificiale può variare. Esaminare i risultati quando la precisione è importante.

### Controlla un&#39;attività più lunga in un secondo momento

1. Aggiungi **[!UICONTROL Esegui una richiesta]**, seleziona la connessione e immetti le istruzioni.
1. Disattiva **[!UICONTROL Attesa completamento]**.
1. Esaminare il risultato iniziale.

   * Se l&#39;attività è completata, elaborare il risultato.
   * Se l&#39;attività richiede attenzione, instradare il risultato per la revisione.
   * Se l&#39;attività è in sospeso, salvare l&#39;**[!UICONTROL ID attività]** come testo e annotare la connessione utilizzata.

1. In seguito, usa **[!UICONTROL Ottieni stato esecuzione]** con la connessione e l&#39;ID attività.
1. Se l&#39;attività è ancora in sospeso, organizzare un altro controllo entro i limiti dello scenario. Elabora il risultato una volta al termine e gestisci separatamente l’attenzione o gli errori.

Non rieseguire il prompt originale solo per verificarne l&#39;avanzamento.

## Considerazioni sull’utilizzo

* Il collaboratore può utilizzare gli strumenti ed eseguire le azioni consentite dal tuo account, incluse le modifiche ai record. Utilizza i prompt attendibili e un account con accesso appropriato.
* Questi moduli non consentono di limitare i singoli strumenti. Istruzioni come &quot;non modificare nulla&quot; descrivono l’intento, ma non sono una modalità di sola lettura imposta.
* Gli strumenti e le competenze disponibili variano a seconda dell’account. Il connettore non fornisce un selettore di abilità né garantisce una particolare azione, ad esempio la creazione di un percorso o l’aggiornamento di un progetto. Non presumere che le richieste che richiedono l’approvazione vengano completate in modo automatico.
* Il connettore si avvia e controlla le richieste di Collaboratore. Non monitora le modifiche al progetto o salva automaticamente le risposte a un’altra applicazione. Aggiungi i moduli trigger, di archiviazione e di follow-on appropriati allo scenario in base alle esigenze.
* Le risposte generate dall’intelligenza artificiale possono essere incomplete o imprecise. Convalida i risultati importanti prima di utilizzarli per apportare modifiche o prendere decisioni.
* Il connettore non ritenta automaticamente una richiesta non riuscita. Assicurati che la gestione degli errori dello scenario non ripeta un prompt il cui risultato è incerto.

## Risoluzione dei problemi

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Manca un campo richiesto</td> 
   <td> <p>Selezionare una connessione e immettere il prompt o l'ID task richiesto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Accesso non riuscito o accesso negato</td> 
   <td> <p>Accedi di nuovo e verifica che il tuo account Adobe abbia accesso a Collaboratore e ai servizi richiesti. Se necessario, contatta l’amministratore.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Attività non trovata</td> 
   <td> <p>Verificare che l'ID attività sia invariato e che si stia utilizzando la connessione originale. Una nuova attività potrebbe non essere visibile immediatamente. Controlla lo stato in un secondo momento, invece di inviare nuovamente la richiesta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Un controllo dello stato non riesce</td> 
   <td> <p>Se l'errore include l'ID attività accettato, utilizzare <b>[!UICONTROL Get Execution Status]</b> per analizzare l'attività. Non riavviare automaticamente il prompt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Esecuzione di un prompt in timeout o perdita della risposta</td> 
   <td> <p>L'attività potrebbe essere stata avviata anche se non ne hai ricevuto l'ID. Esamina prima di ripetere la richiesta, per evitare di duplicare il lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Timeout di Fusion durante l'attesa</td> 
   <td> <p>Il collega potrebbe continuare a lavorare. Se disponi del relativo ID, controlla l’attività. Per le attività lunghe future, disattiva l’attesa e salva prima l’ID iniziale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Collaboratore o servizio richiesto non disponibile</td> 
   <td> <p>Condividi l’errore visualizzato con l’amministratore, senza credenziali o contenuto sensibile dei risultati.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
