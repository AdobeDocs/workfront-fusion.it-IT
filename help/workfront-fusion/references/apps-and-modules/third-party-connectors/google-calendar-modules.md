---
title: Moduli Google Calendar
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Google Calendar, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 6aad13e81c083754d7aad53dec103715bd6b8807
workflow-type: tm+mt
source-wordcount: '2696'
ht-degree: 16%

---

# Moduli [!DNL Google Calendar]

In uno scenario di Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL Google Calendar], nonché collegarlo a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL Google Calendar], è necessario disporre di un account [!DNL Google].

## Google Calendar API information

The Google Calendar connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## Moduli [!DNL Google Calendar] e relativi campi

Quando configuri i moduli [!DNL Google Calendar], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Google Calendar], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Trigger](#triggers)
* [Azioni](#actions)
* [Iteratori](#iterators)

### Trigger

* [Osserva eventi](#watch-events)
* [Watch events (Instant)](#watch-events-instant)

#### Osserva eventi

Questo modulo trigger esegue uno scenario quando un nuovo evento viene aggiunto, aggiornato, eliminato, avviato o terminato nel calendario specificato. Il modulo restituisce tutti i campi standard associati al record oppure ai record, insieme a tutti i campi e i valori personalizzati a cui accede la connessione. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendario] </td> 
   <td> <p>Seleziona il calendario con cui vuoi usare il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Scegli se desideri guardare solo i nuovi eventi o i nuovi eventi e tutte le modifiche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mostra eventi eliminati]</td> 
   <td> <p>Abilita questa opzione per includere gli eventi eliminati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Immettere il testo per il quale si desidera restituire i risultati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di eventi]</td> 
   <td> <p> Impostare il numero massimo di eventi con cui Workfront Fusion lavora durante un ciclo (il numero di ripetizioni per esecuzione dello scenario). Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). Workfront Fusion non ha alcuna influenza su questo aspetto. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Guarda gli eventi (istantanei)

Questo modulo di attivazione utilizza un mailhook per creare un indirizzo e-mail che puoi utilizzare come invito agli eventi. Il modulo avvia uno scenario basato sugli eventi a cui è invitato l’indirizzo e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Selezionare il mailhook che si desidera utilizzare per questo modulo. To create a new mailhooke, click <b>Add</b> and enter the connection you want to use for the mailhook.</p><p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Set the maximum number of events that Workfront Fusion works with during one cycle (the number of repetitions per scenario run). If the value is set too high, the connection may be interrupted on the side of the given third-party service (timeout). Workfront Fusion has no influence on this. We recommend that you set a lower value and either define a higher value for the maximum number of cycles or run the scenario more frequently.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [Creare un calendario](#create-a-calendar)
* [Creare un evento](#create-an-event)
* [Eliminare un evento](#delete-an-event)
* [Ottieni eventi](#get-events)
* [Aggiornare un evento](#update-an-event)

#### Creare un calendario

Questo modulo di azione crea un calendario associato all’account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Select the color to associate with the calendar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Enter or map a name for the new calendar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

This action module creates an event.

You specify the calendar and the parameters for the event.

The module returns the ID of the  event and any associated fields, along with any custom fields and values that the connection accesses. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendario]</td> 
   <td> <p>Select the calendar where you want the event to appear.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Select the color that the event shows on the calendar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Enter or map a name for the event. </p> <p>Note: If you have selected [!UICONTROL Quick add] in the [!UICONTROL Create an event] field, you can include the date and time of the event, and Workfront Fusion creates the event for that date and time. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se si seleziona [!UICONTROL Aggiunta rapida] ma non si include una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tutto il giorno]</td> 
   <td>Abilita questa opzione se l’evento è un evento di una giornata intera (non richiede orari di inizio e fine).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di inizio]</td> 
   <td> <p>Immettere o mappare la data e l'ora di inizio dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di fine]</td> 
   <td> <p> Immettere o mappare la data e l'ora di fine dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Descrizione]</td> 
   <td>Immettere o mappare una descrizione per l'evento. Questo campo supporta HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Immetti una posizione per l’evento in formato testo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Utilizza le impostazioni predefinite del promemoria per questo evento]</td> 
   <td>Abilita questa opzione per utilizzare le impostazioni predefinite del promemoria. Se si imposta un promemoria personalizzato nel campo [!UICONTROL Reminder], questo valore viene impostato su No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Aggiungi promemoria per l’evento. Per ogni promemoria da aggiungere, fai clic su <b>Aggiungi elemento</b>, quindi seleziona il metodo con cui vuoi ricevere il promemoria e definisci per quanto tempo (in minuti) prima dell'evento a cui vuoi inviare il promemoria.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Partecipanti]</td> 
   <td>Aggiungi i partecipanti all’evento. Per ogni partecipante, fare clic su <b>Aggiungi un partecipante</b>, quindi immettere o mappare il nome e l'indirizzo di posta elettronica.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mostra come]</td> 
   <td>Specificare se si desidera che gli utenti che visualizzano il calendario visualizzino l'utente come Occupato o Disponibile durante l'evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Seleziona la visibilità di questo evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL predefinito]</b></p> <p>L'evento ha la visibilità impostata nelle impostazioni del calendario.</p> </li> 
     <li> <p><b>[!UICONTROL Pubblico]</b></p> <p>Anyone the calendar is shared with can see this event.</p> </li> 
     <li> <p><b>[!UICONTROL Privato]</b></p> <p>Only attendees can see this event.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Seleziona se inviare notifiche sulla creazione di un nuovo evento a tutti gli ospiti, a non [!DNL Google Calendar] ospiti o a nessuno.</p> <p>Suggerimento: è consigliabile utilizzare l'opzione [!UICONTROL None] solo per i casi di utilizzo relativi alla migrazione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Gli ospiti possono modificare l'evento]</td> 
   <td> <p>Abilita questa opzione se desideri che gli ospiti possano modificare questo evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ricorrenza]</td> 
   <td>Aggiungi eventuali regole di ricorrenza da applicare a questo evento. Ogni regola richiede un elenco di righe [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] per un evento ricorrente. Tieni presente che le righe [!UICONTROL DTSTART] e [!UICONTROL DTEND] non sono consentite in questo campo; gli orari di inizio e fine dell'evento sono specificati nei campi di inizio e fine. Questo campo viene omesso per singoli eventi o istanze di eventi ricorrenti. Per ulteriori informazioni, vedere <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina un evento]

Questo modulo di azione elimina un evento.

You specify the calendar and event ID.

The module returns the ID of the  event and any associated fields, along with any custom fields and values that the connection accesses. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendario]</td> 
   <td> <p>Select the calendar that contains the event you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID evento]</td> 
   <td> <p> Immettere l'ID evento da un evento [!DNL Google Calendar] creato in precedenza che si desidera eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni eventi]

Questo modulo recupera informazioni sugli eventi nel calendario selezionato in base ai criteri specificati.

Specificare il calendario e i parametri della ricerca.

Il modulo restituisce l’ID degli eventi e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendario]</td> 
   <td> <p>Selezionare il calendario per il quale si desidera recuperare gli eventi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di inizio]</td> 
   <td> <p> Immetti o mappa la data di inizio dell’evento. Questo modulo recupera anche gli eventi che hanno inizio prima di questa data e che si verificano ancora nella data di inizio inserita. </p> <p>Per un elenco dei formati di data e ora supportati, consulta <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercizione del tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di fine]</td> 
   <td> <p> Immetti o mappa la data di fine dell’evento. </p> <p> Per un elenco dei formati di data e ora supportati, consulta <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercizione del tipo</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singoli eventi]</td> 
   <td> <p> Abilita questa opzione per trattare gli eventi ricorrenti come singole istanze. Ad esempio, se hai una riunione settimanale e questa opzione è abilitata, il modulo restituisce ogni riunione della settimana come evento separato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Immettere o mappare il termine di ricerca in base al quale si desidera eseguire la ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ordina per]</td> 
   <td> <p>Seleziona l’ordine degli eventi restituiti nel risultato.</p> 
    <ul> 
     <li><strong>[!UICONTROL Ora di inizio]</strong>: ordina per data e ora di inizio (crescente). Questa funzione è disponibile solo quando si eseguono query su singoli eventi.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: Ordina per ultima modifica (crescente).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di eventi restituiti]</td> 
   <td> <p>Imposta il numero massimo di eventi restituiti da Workfront Fusion durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un evento]

Questo modulo di azione modifica un evento esistente.

Puoi specificare il calendario e l’ID evento.

Il modulo restituisce l’ID dell’evento ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi dello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connessione] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendario] </td> 
   <td> <p>Select the calendar you want to work with.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID evento] </td> 
   <td> <p>Enter the event ID from the previously created [!DNL Google Calendar] event that you want to update.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Enter or map a name for the event. </p> <p>Nota: se è stato selezionato [!UICONTROL Aggiunta rapida] nel campo [!UICONTROL Crea un evento], è possibile includere la data e l'ora dell'evento e Workfront Fusion crea l'evento per tale data e ora. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se si seleziona [!UICONTROL Aggiunta rapida] ma non si include una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tutto il giorno]</td> 
   <td>Abilita questa opzione se l’evento è un evento di una giornata intera (non richiede orari di inizio e fine).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di inizio]</td> 
   <td> <p>Immettere o mappare la data e l'ora di inizio dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di fine]</td> 
   <td> <p> Immettere o mappare la data e l'ora di fine dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Descrizione]</td> 
   <td>Immettere o mappare una descrizione per l'evento. Questo campo supporta HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Immetti una posizione per l’evento in formato testo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Utilizza le impostazioni predefinite del promemoria per questo evento]</td> 
   <td>Abilita questa opzione per utilizzare le impostazioni predefinite del promemoria. Se si imposta un promemoria personalizzato nel campo [!UICONTROL Reminder], questo valore viene impostato su No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Aggiungi promemoria per l’evento. Per ogni promemoria da aggiungere, fai clic su <b>Aggiungi elemento</b>, quindi seleziona il metodo con cui vuoi ricevere il promemoria e definisci per quanto tempo (in minuti) prima dell'evento a cui vuoi inviare il promemoria.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Partecipanti]</td> 
   <td>Aggiungi i partecipanti all’evento. Per ogni partecipante, fare clic su <b>Aggiungi un partecipante</b>, quindi immettere o mappare il nome e l'indirizzo di posta elettronica.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mostra come]</td> 
   <td>Specificare se si desidera che gli utenti che visualizzano il calendario visualizzino l'utente come Occupato o Disponibile durante l'evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Seleziona la visibilità di questo evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL predefinito]</b></p> <p>L'evento ha la visibilità impostata nelle impostazioni del calendario.</p> </li> 
     <li> <p><b>[!UICONTROL Pubblico]</b></p> <p>Chiunque condivida il calendario può visualizzare questo evento.</p> </li> 
     <li> <p><b>[!UICONTROL Privato]</b></p> <p>Solo i partecipanti possono visualizzare questo evento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Invia notifica sulla creazione dell'evento]</td> 
   <td> <p>Seleziona se inviare notifiche sulla creazione di un nuovo evento a tutti gli ospiti, a non [!DNL Google Calendar] ospiti o a nessuno.</p> <p>Suggerimento: è consigliabile utilizzare l'opzione [!UICONTROL None] solo per i casi di utilizzo relativi alla migrazione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Gli ospiti possono modificare l'evento]</td> 
   <td> <p>Abilita questa opzione se desideri che gli ospiti possano modificare questo evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ricorrenza]</td> 
   <td>Aggiungi eventuali regole di ricorrenza da applicare a questo evento. Ogni regola richiede un elenco di righe [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] per un evento ricorrente. Tieni presente che le righe [!UICONTROL DTSTART] e [!UICONTROL DTEND] non sono consentite in questo campo; gli orari di inizio e fine dell'evento sono specificati nei campi di inizio e fine. Questo campo viene omesso per singoli eventi o istanze di eventi ricorrenti. Per ulteriori informazioni, vedere <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr>

</tbody> 
</table>

### Iteratori

#### Itera allegati

Questo modulo di azione esegue l&#39;iterazione degli allegati a un evento e restituisce ogni allegato in un bundle separato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Modulo Source] </td> 
   <td> Selezionare il modulo in questo scenario che restituisce l'evento contenente gli allegati che si desidera iterare. </td> 
  </tr> 
 </tbody> 
</table>

#### Itera partecipanti

Questo modulo di azione scorre i partecipanti per un evento e restituisce ciascun partecipante in un bundle separato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Modulo Source] </td> 
   <td> Selezionare il modulo in questo scenario che restituisce l'evento contenente i partecipanti da iterare. </td> 
  </tr> 
 </tbody> 
</table>





## Attivare uno scenario prima di un evento

Puoi attivare uno scenario un&#39;ora specificata prima di un evento con l&#39;aiuto di [!DNL Google Calendar] promemoria e-mail standard e del modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato].

1. Utilizza il modulo [!UICONTROL Calendario Google] >[!UICONTROL Aggiorna un evento] per aggiungere un promemoria e-mail all&#39;evento:

   ![Scenario di attivazione prima dell&#39;evento](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Create a new scenario starting with the [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] module.

   1. Copy the mailhook&#39;s email address.
   1. Save the scenario and execute it.

1. In [!DNL Gmail], redirect the [!DNL Google Calendar] email reminders to the mailhook&#39;s email address:

   1. Open your **[!UICONTROL [!DNL Gmail]settings]**.
   1. Open the **[!UICONTROL Forwarding and POP/IMAP]** tab.
   1. Click **[!UICONTROL Add a forwarding address].**
   1. Paste the copied mailhooks&#39;s email address, click **[!UICONTROL Next]**, confirm by pressing **[!UICONTROL Proceed]** in the popup window, then click **[!UICONTROL OK]**.

   1. In Workfront Fusion, switch to the new scenario that should finish its execution by receiving the confirmation email.
   1. Click the bubble above the module to inspect the module&#39;s output.
   1. Expand the `Text` item and copy the Confirmation code:

      ![Confirmation code](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. In Gmail, incolla il codice di conferma nella casella di modifica e fai clic su **[!UICONTROL Verifica]**:

      ![Incolla codice](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Apri la scheda **[!UICONTROL Filtri e indirizzi bloccati]**.
   1. Fare clic su **[!UICONTROL Crea nuovo filtro]**.
   1. Imposta un filtro per tutte le e-mail provenienti da `     calendar-notification@google.com` e fai clic su **[!UICONTROL Crea un filtro]**:
   1. Seleziona **[!UICONTROL Inoltra a]** e scegli l&#39;indirizzo e-mail dei collegamenti nell&#39;elenco.
   1. Fare clic su **[!UICONTROL Crea filtro]** per creare il filtro.

1. (Facoltativo) In Workfront Fusion, aggiungi il modulo [!UICONTROL Parser di testo] > [!UICONTROL Corrispondenza pattern] dopo il modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato] per analizzare il codice HTML dell&#39;e-mail e ottenere le informazioni necessarie.

   Ad esempio, puoi configurare il modulo come segue per ottenere l’ID dell’evento:

   *Pattern*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Testo*: l&#39;elemento `HTML content` è stato restituito dal modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato].
