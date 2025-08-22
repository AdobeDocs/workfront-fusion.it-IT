---
title: Moduli calendario di Google
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Google Calendar, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2723'
ht-degree: 0%

---

# [!DNL Google Calendar] moduli

In uno scenario di Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL Google Calendar], nonché collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Piano Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] o versione successiva</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito di licenza corrente: nessun requisito di licenza per Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno corrente del prodotto: se disponi del piano Adobe Workfront [!UICONTROL Select] o [!UICONTROL Prime], per utilizzare le funzionalità descritte in questo articolo la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront. Workfront Fusion è incluso nel piano Workfront di [!UICONTROL Ultimate].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: per utilizzare le funzionalità descritte in questo articolo, la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore Workfront.

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

Quando si configurano [!DNL Google Calendar] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Calendar], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
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
   <td> <p>Selezionare il mailhook che si desidera utilizzare per questo modulo. Per creare un nuovo mailhook, fare clic su <b>Aggiungi</b> e immettere la connessione da utilizzare per il mailhook.</p><p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Numero massimo di eventi]</td> 
   <td> <p> Impostare il numero massimo di eventi con cui Workfront Fusion lavora durante un ciclo (il numero di ripetizioni per esecuzione dello scenario). Se il valore è impostato su un valore troppo alto, la connessione potrebbe essere interrotta sul lato del servizio di terze parti specificato (timeout). Workfront Fusion non ha alcuna influenza su questo aspetto. È consigliabile impostare un valore più basso e definire un valore più alto per il numero massimo di cicli oppure eseguire lo scenario più frequentemente.</p> </td> 
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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Selezionare il colore da associare al calendario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nome calendario] </td> 
   <td> <p>Immettere o mappare un nome per il nuovo calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea un evento]

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
   <td>[!UICONTROL Nome evento]</td> 
   <td> <p> Inserisci o mappa un nome per l’evento. </p> <p>Nota: se è stato selezionato [!UICONTROL Aggiunta rapida] nel campo [!UICONTROL Crea un evento], è possibile includere la data e l'ora dell'evento e Workfront Fusion crea l'evento per tale data e ora. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se si seleziona [!UICONTROL Aggiunta rapida] ma non si include una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
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
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Chiunque condivida il calendario può visualizzare questo evento.</p> </li> 
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

#### [!UICONTROL Elimina un evento]

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
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selezionare il calendario contenente l'evento che si desidera eliminare.</p> </td> 
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
   <td>[!UICONTROL Data di inizio]</td> 
   <td> <p> Immetti o mappa la data di inizio dell’evento. Questo modulo recupera anche gli eventi che hanno inizio prima di questa data e che si verificano ancora nella data di inizio inserita. </p> <p>Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data di fine]</td> 
   <td> <p> Immetti o mappa la data di fine dell’evento. </p> <p> Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</p> </td> 
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

Il modulo restituisce l’ID dell’evento ed eventuali campi associati, insieme a eventuali campi e valori personalizzati a cui la connessione accede. Puoi mappare queste informazioni nei moduli successivi nello scenario.

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Calendar] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selezionare il calendario che si desidera utilizzare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID evento] </td> 
   <td> <p>Immettere l'ID evento dall'evento [!DNL Google Calendar] creato in precedenza che si desidera aggiornare.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Nome evento]</td> 
   <td> <p> Inserisci o mappa un nome per l’evento. </p> <p>Nota: se è stato selezionato [!UICONTROL Aggiunta rapida] nel campo [!UICONTROL Crea un evento], è possibile includere la data e l'ora dell'evento e Workfront Fusion crea l'evento per tale data e ora. Esempio: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Se si seleziona [!UICONTROL Aggiunta rapida] ma non si include una data e un'ora nel nome dell'evento, l'evento viene creato dall'ora corrente e dura un'ora.</p> </td> 
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
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Chiunque condivida il calendario può visualizzare questo evento.</p> </li> 
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

1. Crea un nuovo scenario che inizia con il modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato].

   1. Copia l’indirizzo e-mail del mailhook.
   1. Salva lo scenario ed eseguilo.

1. In [!DNL Gmail], reindirizzare i promemoria e-mail di [!DNL Google Calendar] all&#39;indirizzo e-mail del mailhook:

   1. Apri le impostazioni di **[!UICONTROL [!DNL Gmail]]**.
   1. Apri la scheda **[!UICONTROL Inoltro e POP/IMAP]**.
   1. Fai clic su **[!UICONTROL Aggiungi un indirizzo di inoltro].**
   1. Incolla l&#39;indirizzo e-mail dei mailhook copiati, fai clic su&#x200B;**[!UICONTROL Avanti]**, conferma premendo **[!UICONTROL Procedi]** nella finestra popup, quindi fai clic su **[!UICONTROL OK]**.

   1. In Workfront Fusion, passa al nuovo scenario che deve terminare la sua esecuzione ricevendo l’e-mail di conferma.
   1. Fai clic sulla bolla sopra il modulo per controllare l’output del modulo.
   1. Espandere l&#39;elemento `Text` e copiare il codice di conferma:

      ![Codice di conferma](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. In Gmail, incolla il codice di conferma nella casella di modifica e fai clic su&#x200B;**[!UICONTROL Verifica]**:

      ![Incolla codice](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Apri la scheda **[!UICONTROL Filtri e indirizzi bloccati]**.
   1. Fare clic su **[!UICONTROL Crea nuovo filtro]**.
   1. Imposta un filtro per tutte le e-mail provenienti da `     calendar-notification@google.com` e fai clic su&#x200B;**[!UICONTROL Crea un filtro]**:
   1. Seleziona **[!UICONTROL Inoltra a]** e scegli l&#39;indirizzo e-mail dei collegamenti nell&#39;elenco.
   1. Fare clic su **[!UICONTROL Crea filtro]** per creare il filtro.

1. (Facoltativo) In Workfront Fusion, aggiungi il modulo [!UICONTROL Parser di testo] > [!UICONTROL Corrispondenza pattern] dopo il modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato] per analizzare il codice HTML dell&#39;e-mail e ottenere le informazioni necessarie.

   Ad esempio, puoi configurare il modulo come segue per ottenere l’ID dell’evento:

   *Pattern*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Testo*: l&#39;elemento `HTML content` è stato restituito dal modulo [!UICONTROL Webhook] >[!UICONTROL mailhook personalizzato].
