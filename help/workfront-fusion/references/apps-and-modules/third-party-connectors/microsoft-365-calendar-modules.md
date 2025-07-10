---
title: Calendario di Microsoft Office 365
description: In uno scenario  [!DNL Adobe Workfront Fusion]  è possibile automatizzare i flussi di lavoro che utilizzano Calendario di Microsoft Office 365 e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Calendar]

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Microsoft Office 365 Calendar] e collegarlo a più applicazioni e servizi di terze parti.

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

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Microsoft Office 365 Calendar], è necessario disporre di un account [!DNL Microsoft Office 365 Calendar].

## Informazioni sull&#39;API del calendario di Microsoft Office 365

Il connettore Calendario di Microsoft Office 365 utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Connessione del servizio [!DNL Office 365 Calendar] a [!DNL Workfront Fusion]

Per istruzioni sulla connessione dell&#39;account [!DNL Office 365 Calendar] a [!UICONTROL Workfront Fusion], vedere [Creare una connessione a [!UICONTROL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Alcune app Microsoft utilizzano la stessa connessione, che è associata alle autorizzazioni dei singoli utenti. Pertanto, durante la creazione di una connessione, nella schermata di consenso delle autorizzazioni vengono visualizzate tutte le autorizzazioni concesse in precedenza alla connessione dell’utente, oltre alle nuove autorizzazioni necessarie per l’applicazione corrente.
>
>Ad esempio, se un utente dispone delle autorizzazioni &quot;Leggi tabella&quot; concesse tramite il connettore Excel e quindi crea una connessione nel connettore Outlook per leggere le e-mail, nella schermata di consenso delle autorizzazioni verranno visualizzate sia l’autorizzazione &quot;Leggi tabella&quot; già concessa che l’autorizzazione &quot;Scrivi e-mail&quot; appena richiesta.

## [!DNL Microsoft Office 365 Calendar] moduli e relativi campi

Quando configuri [!DNL Microsoft Office 365 Calendar] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Microsoft Office 365 Calendar], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Evento](#event)
* [Calendario](#calendar)
* [Altro](#other)

### Evento

* [[!UICONTROL Crea un evento]](#create-an-event)
* [[!UICONTROL Eliminare un evento]](#delete-an-event)
* [[!UICONTROL Ottieni un evento]](#get-an-event)
* [[!UICONTROL Cerca eventi]](#search-events)
* [[!UICONTROL Aggiorna un evento]](#update-an-event)
* [[!UICONTROL Guarda gli eventi]](#watch-events)

#### [!UICONTROL Crea un evento]

Questo modulo di azione crea un nuovo evento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Inserisci o mappa un titolo per l’evento creato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di inizio]</td> 
   <td> Immettere un singolo punto di inizio dell'evento in una rappresentazione combinata data e ora. Utilizza il formato <code>{date}T{time}</code>, ad esempio <code>2017-08-29T04:00:00.0000000</code>. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
   <td> Immettere un singolo punto di ora in cui l'evento termina con una rappresentazione combinata data e ora. Utilizza il formato <code>{date}T{time}</code>, ad esempio <code>2017-08-29T04:00:00.0000000</code>. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Promemoria attivato]</td> 
   <td>Seleziona se desideri attivare un promemoria per questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Immetti o mappa il numero di minuti prima dell’inizio dell’evento in cui deve attivarsi il promemoria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza di questo evento.</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Seleziona la riservatezza dell’evento.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normale]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personale]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL Please treat this as Personal]" (Considera questo come personale).</p> </li> 
     <li> <p><strong>[!UICONTROL Privato]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL Please treat this as Private]" (Considera privato questo elemento). Questo evento non viene inoltrato o reindirizzato dalle regole della casella in entrata del destinatario.</p> </li> 
     <li> <p><strong>[!UICONTROL Riservato]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL È da considerarsi riservato]". </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di contenuto corpo]</td> 
   <td>Seleziona se il corpo del testo è testo normale o HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td>Inserisci o mappa il corpo del messaggio associato all’evento. Può essere in formato HTML o testo (come specificato nel campo [!UICONTROL Body Content Type] qui sopra).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Immetti o mappa i dettagli della posizione dell’evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Risposta [!UICONTROL richiesta]</td> 
   <td>Selezionare <strong>[!UICONTROL Sì]</strong> per richiedere all'invitato di inviare una risposta all'invito all'evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra come]</td> 
   <td> <p>Selezionare la modalità di visualizzazione dell'evento per gli utenti che visualizzano il calendario.</p> 
    <ul> 
     <li>[!UICONTROL libero]</li> 
     <li>[!UICONTROL Provvisorio]</li> 
     <li>[!UICONTROL Occupato]</li> 
     <li>[!UICONTROL Fuori sede]</li> 
     <li>[!UICONTROL Lavora altrove]</li> 
     <li>[!UICONTROL Sconosciuto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partecipanti]</p> </td> 
   <td> <p>Per ogni partecipante che si desidera invitare, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere o mappare il nome del partecipante.</p> </li> 
     <li> <p><strong>[!UICONTROL E-Mail]</strong> </p> <p>Immettere o mappare l'indirizzo e-mail del partecipante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categories]</td> 
   <td>Per ogni categoria che si desidera visualizzare come nel calendario, fare clic su <b>Aggiungi elemento</b> e immettere o mappare la categoria.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Eliminare un evento]

Questo modulo di azione elimina un evento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td> <p>Inserisci o mappa l’ID dell’evento da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un evento]

Questo modulo di azione recupera i dettagli dell’evento specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td> <p>Immetti o mappa l’ID dell’evento di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cerca eventi]

Questo modulo di ricerca recupera i dettagli di un evento quando viene creato, aggiornato, eliminato, avviato o terminato nel calendario selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Selezionare il gruppo di calendari [!UICONTROL] che contiene il calendario in cui si desidera visualizzare gli eventi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Selezionare il calendario specifico che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Imposta le condizioni del filtro per filtrare i risultati. Puoi filtrare in base alle seguenti proprietà:</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL ID evento]</li> 
     <li>Data e ora di creazione di [!UICONTROL]</li> 
     <li>[!UICONTROL Data e ora ultima modifica]</li> 
     <li>[!UICONTROL Anteprima corpo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ordina per]</td> 
   <td> <p>Seleziona la modalità desiderata per ordinare i risultati.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, crescente o decrescente</li> 
     <li><strong>[!UICONTROL Data e ora creazione]</strong>, crescente o decrescente</li> 
     <li><strong>[!UICONTROL Data e ora ultima modifica]</strong>, crescente o decrescente</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere il numero massimo di eventi [!DNL Workfront Fusion] che devono essere restituiti durante un ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un evento]

Questo modulo di azione aggiorna un evento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td>Inserisci, mappa o seleziona l’ID dell’evento da aggiornare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Inserisci o mappa un nuovo titolo per l’evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di inizio]</td> 
   <td> Immettere un singolo punto di inizio dell'evento in una rappresentazione combinata data e ora. Utilizza il formato <code>{date}T{time}</code>, ad esempio <code>2017-08-29T04:00:00.0000000</code>. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data di fine]</td> 
   <td> Immettere un singolo punto di ora in cui l'evento termina con una rappresentazione combinata data e ora. Utilizza il formato <code>({date}T{time}</code>, ad esempio <code>2017-08-29T04:00:00.0000000</code>. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Promemoria attivato]</td> 
   <td>Seleziona se desideri attivare un promemoria per questo evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Immetti o mappa il numero di minuti prima dell’inizio dell’evento in cui deve attivarsi il promemoria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Seleziona l’importanza di questo evento.</p> 
    <ul> 
     <li>[!UICONTROL Minimo]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL alto]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Seleziona la riservatezza dell’evento.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normale]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personale]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL Please treat this as Personal]" (Considera questo come personale).</p> </li> 
     <li> <p><strong>[!UICONTROL Privato]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL Please treat this as Private]" (Considera privato questo elemento). Questo evento non viene inoltrato o reindirizzato dalle regole della casella in entrata del destinatario.</p> </li> 
     <li> <p><strong>[!UICONTROL Riservato]</strong> </p> <p>Il destinatario visualizza un messaggio "[!UICONTROL È da considerarsi riservato]". </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di contenuto corpo]</td> 
   <td>Seleziona se il contenuto del corpo del messaggio associato all’evento è testo normale o HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contenuto corpo]</td> 
   <td>Inserisci o mappa il corpo del messaggio associato all’evento. Può essere in formato HTML o testo (come specificato nel campo [!UICONTROL Body Content Type] qui sopra).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Immettere i dettagli della posizione dell'evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Risposta [!UICONTROL richiesta]</td> 
   <td>Selezionare <strong>[!UICONTROL Sì]</strong> per richiedere all'invitato di inviare una risposta all'invito all'evento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra come]</td> 
   <td> <p>Selezionare la modalità di visualizzazione dell'evento per gli utenti che visualizzano il calendario.</p> 
    <ul> 
     <li>[!UICONTROL libero]</li> 
     <li>[!UICONTROL Provvisorio]</li> 
     <li>[!UICONTROL Occupato]</li> 
     <li>[!UICONTROL Fuori sede]</li> 
     <li>[!UICONTROL Lavora altrove]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partecipanti]</p> </td> 
   <td> <p>Aggiungi i partecipanti all'evento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome]</strong> </p> <p>Immettere il nome del partecipante.</p> </li> 
     <li> <p><strong>[!UICONTROL E-Mail]</strong> </p> <p>Immettere l'indirizzo di posta elettronica del partecipante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categoria]</td> 
   <td>Immetti o mappa le categorie che desideri che l’evento venga visualizzato nel calendario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Guarda gli eventi]

Questo modulo trigger recupera i dettagli di un evento quando viene creato, aggiornato, eliminato, avviato o terminato nel calendario selezionato.

>[!NOTE]
>
>Per controllare le occorrenze eliminate di una serie di eventi, selezionare [!UICONTROL Per ora di aggiornamento] nel campo [!UICONTROL Osserva eventi]. Questo modulo non verifica la presenza di singoli eventi o serie di eventi eliminati.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Osserva eventi]</td> 
   <td> <p>Seleziona la modalità di visualizzazione degli eventi.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Per Ora Di Creazione]</strong> </p> <p>Guarda i nuovi eventi.</p> </li> 
     <li> <p><strong>[!UICONTROL Per Ora Di Aggiornamento]</strong> </p> <p>Controlla gli eventi aggiornati.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Selezionare il gruppo di calendari [!UICONTROL] che contiene il calendario in cui si desidera visualizzare gli eventi.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Selezionare il calendario specifico che si desidera controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td>Imposta le condizioni del filtro per filtrare i risultati per oggetto, ID evento o corpo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere il numero massimo di messaggi che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Calendario

* [[!UICONTROL Crea un calendario]](#create-a-calendar)
* [[!UICONTROL Elimina calendario]](#delete-a-calendar)
* [[!UICONTROL Ottieni un calendario]](#get-a-calendar)
* [[!UICONTROL Elenca calendari]](#list-calendars)
* [[!UICONTROL Aggiorna calendario]](#update-a-calendar)



#### [!UICONTROL Crea un calendario]

Questo modulo di azione crea un nuovo calendario nell’account di Office 365.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome calendario]</td> 
   <td> <p>Immettere un nome per il nuovo calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina calendario]

Questo modulo elimina un calendario esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID calendario]</td> 
   <td>Immettere l'ID [!UICONTROL Calendar] per il calendario che si desidera eliminare.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni un calendario]

Questo modulo di azione recupera i dettagli di un singolo calendario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID calendario]</td> 
   <td> <p>Immetti o mappa l’ID del calendario di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca calendari]

Questo modulo di ricerca recupera un elenco di tutti i calendari dell’utente autenticato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Selezionare il gruppo di calendari [!UICONTROL] contenente i calendari da elencare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Immettere il numero massimo di calendari che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna calendario]

Questo modulo di azione modifica un calendario esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID calendario]</td> 
   <td>Immettere l'ID del calendario [!UICONTROL] per il calendario che si desidera aggiornare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome nuovo calendario]</td> 
   <td> <p>Immettere un nuovo nome per il calendario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

#### [!UICONTROL Effettuare una chiamata API]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Office 365] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code>https://graph.microsoft.com</code>. Esempio:<code> /v1.0/me/events</code></p> </td> 
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
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
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
