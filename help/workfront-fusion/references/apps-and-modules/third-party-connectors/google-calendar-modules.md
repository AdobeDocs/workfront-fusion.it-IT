---
title: Moduli calendario di Google
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Google Calendar e collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '3314'
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

* [Eventi](#events)
* [Calendari](#calendars)
* [Regole di controllo degli accessi](#access-control-rules)
* [Iteratori (obsoleto)](#iterators-deprecated)
* [Altro](#other)

### Eventi

* [[!UICONTROL Watch events]](#watch-events)
* [[!UICONTROL Search events]](#search-events)
* [[!UICONTROL Get an event]](#get-an-event)
* [[!UICONTROL Create an event]](#create-an-event)
* [[!UICONTROL Update an event]](#update-an-event)
* [[!UICONTROL Delete an event]](#delete-an-event)


#### [!UICONTROL Watch events]

Questo modulo trigger esegue uno scenario quando un nuovo evento viene aggiunto, aggiornato, eliminato, avviato o terminato nel calendario specificato. Il modulo restituisce tutti i campi standard associati al record o ai record, insieme a tutti i campi e i valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Seleziona il calendario con cui vuoi usare il modulo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch Events]</td> 
   <td> <p>Scegli se desideri guardare gli eventi per Data di creazione, Data di aggiornamento, Data di inizio o Data di fine.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Abilita questa opzione per includere gli eventi eliminati.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Immettere il testo da cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> Impostare il numero massimo di eventi con cui [!DNL Workfront Fusion] funziona durante un ciclo (il numero di ripetizioni per esecuzione dello scenario). Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). [!DNL Workfront Fusion] non ha alcuna influenza su questo elemento. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search events]

Questo modulo di azione cerca un evento nel calendario selezionato.

Specificare il calendario e i parametri della ricerca.

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
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Immetti o mappa la data di inizio dell’evento. Questo modulo recupera anche gli eventi che hanno inizio prima di questa data e che si verificano ancora nella data di inizio inserita. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Immetti o mappa la data di fine dell’evento. </p> <p> Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Impostare il numero massimo di eventi [!DNL Workfront Fusion] restituiti durante un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an event]

Questo modulo di azione restituisce i metadati per un singolo evento nel calendario specificato.

Specificare il calendario e l&#39;evento.

Il modulo restituisce l’ID dell’evento e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Immetti o mappa l’ID del calendario che contiene l’evento che desideri ottenere.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Immettere l'ID dell'evento [!DNL Google Calendar] esistente che si desidera ottenere.</p> </td> 
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
   <td>[!UICONTROL Create an Event]</td> 
   <td> <p>Seleziona la modalità di creazione dell’evento.</p> 
    <ul> 
     <li><b>[!UICONTROL In Detail]</b><p>Questa opzione consente di inserire maggiori dettagli sull’evento.<br></p></li> 
     <li><b>[!UICONTROL Quickly]</b><p>È sufficiente selezionare il calendario e immettere un nome per l'evento. Puoi includere i dettagli di ora e luogo nel nome. [!DNL Google Calendar] pianificherà l'evento per tale luogo e ora.</p></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
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
   <td> <p>Se si tratta di un evento giornata intera, immettere la data di inizio dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Se si tratta di un evento giornata intera, immettere la data di fine dell'evento. </p> <p>Per un elenco dei formati di data supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
   <td> <p>Aggiungi promemoria per l’evento. Per ogni promemoria, seleziona il metodo con cui vuoi ricevere il promemoria e definisci quanto tempo (in minuti) prima dell’evento a cui vuoi inviare il promemoria.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Aggiungi i partecipanti all’evento. Per ogni partecipante, immettere o mappare il proprio nome e indirizzo di posta elettronica.</td> 
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
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selezionare il calendario che si desidera utilizzare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Immettere l'ID evento dall'evento [!DNL Google Calendar] creato in precedenza che si desidera aggiornare.</p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile aggiornare le informazioni sull’evento immettendo nuovi valori nel campo desiderato. Per informazioni dettagliate sui singoli campi, vedere [[!UICONTROL Create an event]](#create-an-event).

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
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario contenente l'evento che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Immettere l'ID evento da un evento [!DNL Google Calendar] creato in precedenza che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event deletion]</td> 
   <td>Specificare se si desidera inviare notifiche sull'eliminazione dell'evento a tutti gli ospiti, ospiti che non utilizzano [!DNL Google Calendar] o nessuno.</td> 
  </tr> 
 </tbody> 
</table>

### Calendari

* [[!UICONTROL List calendars]](#list-calendars)
* [[!UICONTROL Get a calendar]](#get-a-calendar)
* [[!UICONTROL Create a calendar]](#create-a-calendar)
* [[!UICONTROL Update a calendar]](#update-a-calendar)
* [[!UICONTROL Delete a calendar]](#delete-a-calendar)
* [[!UICONTROL Clear a calendar]](#clear-a-calendar)

#### [!UICONTROL List calendars]

Questo modulo di azione restituisce i calendari nell&#39;elenco dei calendari di un utente.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Minimum access role]</td> 
   <td> <p>Seleziona il ruolo di accesso minimo per l’utente. Il modulo restituisce calendari in base a questo ruolo di accesso minimo.</p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l'utente può leggere le informazioni sulla disponibilità. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utente può leggere e modificare gli eventi e accedere agli elenchi di controllo. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utente può leggere eventi che non sono privati. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utente può leggere e modificare gli eventi.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden calendars]</td> 
   <td>Abilita questa opzione per includere i calendari nascosti nell’elenco restituito dal modulo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Impostare il numero massimo di calendari [!DNL Workfront Fusion] restituiti durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a calendar]

Questo modulo di azione recupera un calendario.

Specifica l’ID del calendario da recuperare.

Il modulo restituisce l’ID del record ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Seleziona il calendario da recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a calendar]

Questo modulo crea un nuovo calendario.

Specificare un nome per il calendario.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> Immettere un nome per il nuovo calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a calendar]

Questo modulo di azione aggiorna un calendario.

Specifica l’ID del calendario da aggiornare.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Seleziona il calendario da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> Immettere un nuovo nome per il calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a calendar]

Questo modulo di azione elimina un calendario.

Specificare l&#39;ID del calendario che si desidera eliminare.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Immetti o mappa l’ID del calendario da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clear a calendar]

Questo modulo di azione rimuove tutti gli eventi dal calendario principale di un account.

Specificare la connessione che si connette all&#39;account contenente il calendario che si desidera cancellare.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
 </tbody> 
</table>

### Regole di controllo degli accessi

* [[!UICONTROL List access control rules]](#list-access-control-rules)
* [[!UICONTROL Get an access control rule]](#get-an-access-control-rule)
* [[!UICONTROL Create an access control rule]](#create-an-access-control-rule)
* [[!UICONTROL Update an access control rule]](#update-an-access-control-rule)
* [[!UICONTROL Delete an access control rule]](#delete-an-access-control-rule)

#### [!UICONTROL List access control rules]

Questo modulo di azione restituisce le regole nell&#39;elenco di controllo di accesso in un calendario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario contenente le regole di controllo di accesso da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Impostare il numero massimo di risultati [!DNL Workfront Fusion] restituiti durante un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an access control rule]

Questo modulo di azione restituisce i metadati di una regola di controllo di accesso.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario contenente la regola di controllo di accesso che si desidera recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access control rule ID]</td> 
   <td>Selezionare la regola di controllo di accesso da recuperare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an access control rule]

Questo modulo di azione crea una nuova regola di controllo di accesso.

Specificare un nome per il calendario.

Il modulo restituisce l’ID della regola di controllo di accesso e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario in cui si desidera creare una regola di controllo degli accessi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>Selezionare il ruolo da assegnare alla regola di accesso. </p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l'utente può leggere le informazioni sulla disponibilità. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utente può leggere e modificare gli eventi e accedere agli elenchi di controllo. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utente può leggere eventi che non sono privati. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utente può leggere e modificare gli eventi.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type]</td> 
   <td> <p>Selezionare il tipo di ambito. </p> 
    <ul> 
     <li><strong>[!UICONTROL Default]</strong>: ambito pubblico. Questo è il valore predefinito. </li> 
     <li><strong>[!UICONTROL User]</strong>: limita l’ambito a un singolo utente. </li> 
     <li><strong>[!UICONTROL Group]</strong>: limita l’ambito a un gruppo. </li> 
     <li><strong>[!UICONTROL Domain]</strong>: limita l’ambito a un dominio. </li> 
    </ul> <p>Nota: le autorizzazioni concesse all'ambito [!UICONTROL Default] o pubblico si applicano a qualsiasi utente autenticato o meno.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td>Immettere l'indirizzo di posta elettronica di un utente o di un gruppo oppure il nome di un dominio, a seconda del tipo di ambito.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>Abilita questa opzione per inviare notifiche sulla modifica dell’accesso. </p> <p>Nota: non sono presenti notifiche sulla rimozione degli accessi. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an access control rule]

Questo modulo di azione aggiorna una regola di controllo di accesso.

Specificare un nome per il calendario.

Il modulo restituisce l’ID della regola di controllo di accesso e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare il calendario contenente la regola di controllo di accesso che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>Selezionare la regola di controllo di accesso da aggiornare.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>Selezionare il ruolo da assegnare alla regola di accesso. </p> 
    <ul> 
     <li><strong>[!UICONTROL None]</strong>: questo ruolo non fornisce accesso.</li> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l'utente può leggere le informazioni sulla disponibilità. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utente può leggere e modificare gli eventi e accedere agli elenchi di controllo. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utente può leggere eventi che non sono privati. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utente può leggere e modificare gli eventi.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>Abilita questa opzione per inviare notifiche sulla modifica dell’accesso. </p> <p>Nota: non sono presenti notifiche sulla rimozione degli accessi. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an access control rule]

Questo modulo di azione elimina una regola di controllo di accesso.

Specificare un nome per il calendario.

Il modulo restituisce l’ID della regola di controllo di accesso e tutti i campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Selezionare o mappare l'ID del calendario contenente la regola di controllo di accesso che si desidera eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>Selezionare o mappare l'ID della regola di controllo di accesso che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

### Iteratori (obsoleto)

I moduli [!UICONTROL iterate attachments] e [!UICONTROL iterate attendees] sono stati dichiarati obsoleti. Per ripetere allegati o partecipanti, utilizzare il modulo [!UICONTROL Flow Control] > [!UICONTROL Iterator]. Per ulteriori informazioni, vedere [Modulo Iterator](/help/workfront-fusion/references/modules/iterator-module.md)

### Altro

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Get Free/Busy Information]](#get-freebusy-information)

#### [!UICONTROL Make an API Call]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Adobe Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Workfront Fusion] - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Immettere un percorso relativo a <code>https://www.googleapis.com/calendar</code>. Esempio: <code>/v3/users/me/calendarList</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:   <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Free/Busy Information]

Questo modulo di azione restituisce informazioni sulla disponibilità per un set di calendari.

Il modulo restituisce l’ID del calendario ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

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
   <td>[!UICONTROL Minimum time]</td> 
   <td> <p> Immettere l'inizio dell'intervallo per il quale si desidera recuperare le informazioni.</p> <p> Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum time]</td> 
   <td> <p> Immettere la fine dell'intervallo per il quale si desidera recuperare le informazioni. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendars]</td> 
   <td> <p>Per ogni calendario da cui si desidera recuperare informazioni, fare clic su <strong>Aggiungi</strong> e immettere o mappare l'ID calendario.</p> </td> 
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
