---
title: Moduli calendario di Google
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Google Calendar e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 160e503adeca5404e18fd0cba9f475fee8510a48
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# [!DNL Google Calendar] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL Google Calendar] e collegarlo a più applicazioni e servizi di terze parti.

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

## Prerequisiti

Per utilizzare i moduli [!DNL Google Calendar], è necessario disporre di un account [!DNL Google].

## Informazioni API calendario Google

Il connettore Google Calendar utilizza quanto segue:

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

## [!DNL Google Calendar] moduli e relativi campi

Quando configuri [!DNL Google Calendar] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Calendar], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Trigger](#triggers)
* [Azioni](#actions)
* [Iteratori](#iterators)

### Trigger

* [Guarda gli eventi](#watch-events)
* [Guarda gli eventi (istantanei)](#watch-events-instant)

#### Guarda gli eventi

Questo modulo trigger esegue uno scenario quando un nuovo evento viene aggiunto, aggiornato, eliminato, avviato o terminato nel calendario specificato. Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Seleziona il calendario con cui vuoi usare il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Scegli se desideri guardare solo i nuovi eventi o i nuovi eventi e tutte le modifiche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Abilita questa opzione per includere gli eventi eliminati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Immettere il testo per il quale si desidera restituire i risultati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Impostare il numero massimo di eventi con cui [!DNL Workfront Fusion] funziona durante un ciclo (il numero di ripetizioni per esecuzione dello scenario). Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). [!DNL Workfront Fusion] non ha alcuna influenza su questo elemento. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
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
   <td> <p>Selezionare il mailhook che si desidera utilizzare per questo modulo. Per creare un nuovo mailhook, fare clic su <b>Aggiungi</b> e immettere la connessione da utilizzare per il mailhook.</p><p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Impostare il numero massimo di eventi con cui [!DNL Workfront Fusion] funziona durante un ciclo (il numero di ripetizioni per esecuzione dello scenario). Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). [!DNL Workfront Fusion] non ha alcuna influenza su questo elemento. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
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
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Selezionare il colore da associare al calendario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Immettere o mappare un nome per il nuovo calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

Questo modulo di azione crea un evento.

Puoi specificare il calendario e i parametri per l’evento.

Il modulo restituisce l’ID dell’evento ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Seleziona il calendario in cui desideri visualizzare l’evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Selezionare il colore visualizzato dall'evento nel calendario.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Inserisci o mappa un nome per l’evento. </p> <p>Nota: se hai selezionato [!UICONTROL Quick add] nel campo [!UICONTROL Create an event], puoi includere la data e l'ora dell'evento e [!DNL Workfront Fusion] crea l'evento per tale data e ora. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se hai selezionato [!UICONTROL Quick add] ma non includi una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Abilita questa opzione se l’evento è un evento di una giornata intera (non richiede orari di inizio e fine).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Immettere o mappare la data e l'ora di inizio dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Immettere o mappare la data e l'ora di fine dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione per l'evento. Questo campo supporta HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Immetti una posizione per l’evento in formato testo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Abilita questa opzione per utilizzare le impostazioni predefinite del promemoria. Se si imposta un promemoria personalizzato nel campo [!UICONTROL Reminder], questo valore viene impostato su No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Aggiungi promemoria per l’evento. Per ogni promemoria da aggiungere, fai clic su <b>Aggiungi elemento</b>, quindi seleziona il metodo con cui vuoi ricevere il promemoria e definisci per quanto tempo (in minuti) prima dell'evento a cui vuoi inviare il promemoria.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Aggiungi i partecipanti all’evento. Per ogni partecipante, fare clic su <b>Aggiungi un partecipante</b>, quindi immettere o mappare il nome e l'indirizzo di posta elettronica.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Specificare se si desidera che gli utenti che visualizzano il calendario visualizzino l'utente come Occupato o Disponibile durante l'evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Seleziona la visibilità di questo evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>L'evento ha la visibilità impostata nelle impostazioni del calendario.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Chiunque condivida il calendario può visualizzare questo evento.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Solo i partecipanti possono visualizzare questo evento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Seleziona se inviare notifiche sulla creazione di un nuovo evento a tutti gli ospiti, a non [!DNL Google Calendar] ospiti o a nessuno.</p> <p>Suggerimento: si consiglia di utilizzare l'opzione [!UICONTROL None] solo per i casi di utilizzo relativi alla migrazione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Abilita questa opzione se desideri che gli ospiti possano modificare questo evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Aggiungi eventuali regole di ricorrenza da applicare a questo evento. Ogni regola richiede un elenco di [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] righe per un evento ricorrente. Si noti che [!UICONTROL DTSTART] e [!UICONTROL DTEND] righe non sono consentite in questo campo; gli orari di inizio e fine dell'evento sono specificati nei campi di inizio e fine. Questo campo viene omesso per singoli eventi o istanze di eventi ricorrenti. Per ulteriori informazioni, vedere <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

Questo modulo di azione elimina un evento.

Puoi specificare il calendario e l’ID evento.

Il modulo restituisce l’ID dell’evento ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selezionare il calendario contenente l'evento che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Immettere l'ID evento da un evento [!DNL Google Calendar] creato in precedenza che si desidera eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

Questo modulo recupera informazioni sugli eventi nel calendario selezionato in base ai criteri specificati.

Specificare il calendario e i parametri della ricerca.

Il modulo restituisce l’ID degli eventi e dei campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selezionare il calendario per il quale si desidera recuperare gli eventi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Immetti o mappa la data di inizio dell’evento. Questo modulo recupera anche gli eventi che hanno inizio prima di questa data e che si verificano ancora nella data di inizio inserita. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Immetti o mappa la data di fine dell’evento. </p> <p> Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Abilita questa opzione per trattare gli eventi ricorrenti come singole istanze. Ad esempio, se hai una riunione settimanale e questa opzione è abilitata, il modulo restituisce ogni riunione della settimana come evento separato.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Immettere o mappare il termine di ricerca in base al quale si desidera eseguire la ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Seleziona l’ordine degli eventi restituiti nel risultato.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: ordina per data e ora di inizio (crescente). Questa funzione è disponibile solo quando si eseguono query su singoli eventi.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: ordina per ora dell’ultima modifica (crescente).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>Impostare il numero massimo di eventi [!DNL Workfront Fusion] restituiti durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

Questo modulo di azione modifica un evento esistente.

Puoi specificare il calendario e l’ID evento.

Il modulo restituisce l’ID dell’evento ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selezionare il calendario che si desidera utilizzare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Immettere l'ID evento dall'evento [!DNL Google Calendar] creato in precedenza che si desidera aggiornare.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Inserisci o mappa un nome per l’evento. </p> <p>Nota: se hai selezionato [!UICONTROL Quick add] nel campo [!UICONTROL Create an event], puoi includere la data e l'ora dell'evento e [!DNL Workfront Fusion] crea l'evento per tale data e ora. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se hai selezionato [!UICONTROL Quick add] ma non includi una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Abilita questa opzione se l’evento è un evento di una giornata intera (non richiede orari di inizio e fine).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Immettere o mappare la data e l'ora di inizio dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Immettere o mappare la data e l'ora di fine dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Immettere o mappare una descrizione per l'evento. Questo campo supporta HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Immetti una posizione per l’evento in formato testo.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Abilita questa opzione per utilizzare le impostazioni predefinite del promemoria. Se si imposta un promemoria personalizzato nel campo [!UICONTROL Reminder], questo valore viene impostato su No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Aggiungi promemoria per l’evento. Per ogni promemoria da aggiungere, fai clic su <b>Aggiungi elemento</b>, quindi seleziona il metodo con cui vuoi ricevere il promemoria e definisci per quanto tempo (in minuti) prima dell'evento a cui vuoi inviare il promemoria.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Aggiungi i partecipanti all’evento. Per ogni partecipante, fare clic su <b>Aggiungi un partecipante</b>, quindi immettere o mappare il nome e l'indirizzo di posta elettronica.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Specificare se si desidera che gli utenti che visualizzano il calendario visualizzino l'utente come Occupato o Disponibile durante l'evento.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Seleziona la visibilità di questo evento. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>L'evento ha la visibilità impostata nelle impostazioni del calendario.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Chiunque condivida il calendario può visualizzare questo evento.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Solo i partecipanti possono visualizzare questo evento.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Seleziona se inviare notifiche sulla creazione di un nuovo evento a tutti gli ospiti, a non [!DNL Google Calendar] ospiti o a nessuno.</p> <p>Suggerimento: si consiglia di utilizzare l'opzione [!UICONTROL None] solo per i casi di utilizzo relativi alla migrazione.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Abilita questa opzione se desideri che gli ospiti possano modificare questo evento.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Aggiungi eventuali regole di ricorrenza da applicare a questo evento. Ogni regola richiede un elenco di [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] e [!UICONTROL EXDATE] righe per un evento ricorrente. Si noti che [!UICONTROL DTSTART] e [!UICONTROL DTEND] righe non sono consentite in questo campo; gli orari di inizio e fine dell'evento sono specificati nei campi di inizio e fine. Questo campo viene omesso per singoli eventi o istanze di eventi ricorrenti. Per ulteriori informazioni, vedere <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
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
   <td>[!UICONTROL Source module] </td> 
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
   <td>[!UICONTROL Source module] </td> 
   <td> Selezionare il modulo in questo scenario che restituisce l'evento contenente i partecipanti da iterare. </td> 
  </tr> 
 </tbody> 
</table>





## Attivare uno scenario prima di un evento

È possibile attivare uno scenario un tempo specificato prima di un evento con l&#39;aiuto di [!DNL Google Calendar] promemoria e-mail standard e del modulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].

1. Utilizza il modulo [!UICONTROL Google Calendar] >[!UICONTROL Update an event] per aggiungere un promemoria e-mail all&#39;evento:

   ![Scenario di attivazione prima dell&#39;evento](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Crea un nuovo scenario che inizia con il modulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].

   1. Copia l’indirizzo e-mail del mailhook.
   1. Salva lo scenario ed eseguilo.

1. In [!DNL Gmail], reindirizzare i promemoria e-mail di [!DNL Google Calendar] all&#39;indirizzo e-mail del mailhook:

   1. Apri **[!UICONTROL [!DNL Gmail] settings]**.
   1. Apri la scheda **[!UICONTROL Forwarding and POP/IMAP]**.
   1. Fare clic su **[!UICONTROL Add a forwarding address].**
   1. Incolla l&#39;indirizzo e-mail dei mailhook copiati, fai clic su&#x200B;**[!UICONTROL Next]**, conferma premendo **[!UICONTROL Proceed]** nella finestra popup, quindi fai clic su **[!UICONTROL OK]**.

   1. In [!DNL Workfront Fusion], passa al nuovo scenario che deve terminare l&#39;esecuzione ricevendo l&#39;e-mail di conferma.
   1. Fai clic sulla bolla sopra il modulo per controllare l’output del modulo.
   1. Espandere l&#39;elemento `Text` e copiare il codice di conferma:

      ![Codice di conferma](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. In Gmail, incolla il codice di conferma nella casella di modifica e fai clic su&#x200B;**[!UICONTROL Verify]**:

      ![Incolla codice](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Apri la scheda **[!UICONTROL Filters and Blocked Addresses]**.
   1. Fare clic su **[!UICONTROL Create a new filter]**.
   1. Imposta un filtro per tutte le e-mail provenienti da `     calendar-notification@google.com` e fai clic su&#x200B;**[!UICONTROL Create a filter]**:
   1. Selezionare **[!UICONTROL Forward it to]** e scegliere l&#39;indirizzo di posta elettronica dei collegamenti dall&#39;elenco.
   1. Fare clic su **[!UICONTROL Create filter]** per creare il filtro.

1. (Facoltativo) In [!DNL Workfront Fusion], aggiungere il modulo [!UICONTROL Text parser] > [!UICONTROL Match pattern] dopo il modulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] per analizzare il codice HTML dell&#39;e-mail e ottenere le informazioni necessarie.

   Ad esempio, puoi configurare il modulo come segue per ottenere l’ID dell’evento:

   *Pattern*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Testo*: elemento `HTML content` restituito dal modulo [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].
