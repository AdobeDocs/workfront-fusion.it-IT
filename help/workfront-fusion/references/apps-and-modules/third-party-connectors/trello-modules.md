---
title: Moduli Trello
description: In uno scenario  [!DNL Adobe Workfront Fusion] , è possibile automatizzare i flussi di lavoro che utilizzano Trello, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '5217'
ht-degree: 0%

---

# [!UICONTROL Moduli Trello]

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!UICONTROL Trello], nonché collegarlo a più applicazioni e servizi di terze parti.

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

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Trello], è necessario disporre di un account [!UICONTROL Trello].

## Informazioni API Trello

Il connettore Trello utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!UICONTROL Trello] a [!DNL Workfront Fusion]

Per istruzioni sulla connessione dell&#39;account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere [Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Moduli Trello] e relativi campi

Quando si configurano i moduli [!UICONTROL Trello], [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi [!UICONTROL Trello], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Bacheche](#boards)
* [Elenchi](#lists)
* [Schede](#cards)
* [Membri](#members)
* [Elenchi di controllo](#checklists)
* [Etichette](#labels)
* [Commenti](#comments)

### Bacheche

+++ **[!UICONTROL Archiviare o annullare l&#39;archiviazione di una bacheca]**

Questo modulo di azione chiude (archivia) o riapre (annulla l’archiviazione) una bacheca specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p> Inserisci o mappa l’ID della bacheca da chiudere o riaprire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archivia o annulla archiviazione]</td> 
   <td> <p> Seleziona se desideri chiudere (archiviare) o riaprire (annullare l’archiviazione) la bacheca.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assegna un membro a una bacheca]**

Questo modulo di azione assegna un membro a una bacheca specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p> Selezionare la bacheca in cui si desidera aggiungere un membro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Inserisci o mappa l’indirizzo e-mail del membro che desideri aggiungere alla bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di membro]</p> </td> 
   <td> <p>Selezionare il tipo di membro desiderato per il nuovo membro.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: un amministratore della bacheca può eseguire qualsiasi azione sulla bacheca.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: un membro normale è semplicemente un membro della bacheca.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: un osservatore è un membro con accesso in sola lettura alla bacheca. <br>Gli osservatori sono disponibili solo per i team con [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome completo]</td> 
   <td> <p> Inserisci o mappa il nome completo dell’utente che desideri aggiungere alla bacheca.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea una bacheca]**

Questo modulo di azione crea una nuova bacheca con le impostazioni selezionate.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Inserisci o mappa un nome per la nuova bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione]</td> 
   <td> <p>Inserisci o mappa la descrizione della bacheca, se necessario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID organizzazione]</p> </td> 
   <td> <p>Inserisci o mappa l’ID dell’organizzazione. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Livello di autorizzazione]</p> </td> 
   <td> <p>Le bacheche hanno regole di voto e commento diverse per ogni livello di autorizzazione. Se ad esempio la bacheca è [!UICONTROL Private] e si impostano le regole di voto e commento come [!UICONTROL All], verrà visualizzato un errore. </p> <p>Le votazioni e i commenti sono limitati ai seguenti gruppi per ogni livello di autorizzazione:</p> 
    <ul> 
     <li><strong>[!UICONTROL Privato]</strong>: 
      Membri, membri e osservatori</li> 
     <li><strong>[!UICONTROL Per Organizzazione]</strong>: 
      Membri, membri e osservatori, membri dell’organizzazione</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Membri, membri e osservatori, membri dell'organizzazione, tutti</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Seleziona un’opzione per specificare chi può votare su questa bacheca. Per informazioni sulle limitazioni di voto nei livelli di autorizzazione, vedere il campo [!UICONTROL Livello di autorizzazione].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Commenti]</p> </td> 
   <td> <p>Seleziona un’opzione per specificare chi può commentare le schede per questa bacheca. Per informazioni sulle limitazioni relative ai livelli di autorizzazione, vedere il campo [!UICONTROL Livello di autorizzazione].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL inviti]</p> </td> 
   <td> <p>Seleziona chi può invitare altre persone a questa bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Seleziona se i membri del team possono unirsi alla bacheca autonomamente o se devono essere invitati.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Etichette predefinite]</p> </td> 
   <td> <p>Seleziona se utilizzare il set di etichette predefinito per la nuova bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Elenchi predefiniti]</p> </td> 
   <td> <p>Seleziona se aggiungere il set di elenchi predefinito alla bacheca ([!UICONTROL Da fare], [!UICONTROL Da fare], [!UICONTROL Da fare]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID sorgente bacheca]</p> </td> 
   <td> <p>Seleziona o mappa l’ID della bacheca da copiare nella nuova bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Copertine scheda]</p> </td> 
   <td> <p>Selezionare <strong>[!UICONTROL Sì]</strong> se si desidera abilitare i coperchi per la scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sfondo]</p> </td> 
   <td> <p>Seleziona il colore dello sfondo o dello sfondo personalizzato.</p> <p>Nota: gli sfondi personalizzati sono disponibili solo per gli abbonati a [!UICONTROL Trello Gold and Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID sfondo]</td> 
   <td> <p> Se si è selezionato di utilizzare uno sfondo personalizzato nel campo [!UICONTROL Background], immettere o mappare l'ID dello sfondo che si desidera utilizzare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Scegli tra due modalità di aging della carta. </p> 
    <ul> 
     <li><strong>[!UICONTROL Modalità pirata]</strong>: le carte si lacerano, ingialliscono e si rompono come una vecchia mappa pirata quando invecchiano.</li> 
     <li><strong>[!UICONTROL Modalità regolare &#x200B;]</strong>: le schede diventano progressivamente più trasparenti con l'invecchiamento. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Modifica bacheca]**

Questo modulo di azione modifica le impostazioni di una scheda esistente.

>[!SUCCESS]
>
><table style="table-layout:auto">
><col> 
> <col> 
> <tbody> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Connection] </td> 
>   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL ID bacheca]</p> </td> 
>   <td> <p>Immettere o mappare l'ID [!UICONTROL Trello] univoco della bacheca che si desidera creare con il modulo. Puoi recuperare l’ID della bacheca utilizzando un altro modulo, ad esempio il modulo Bacheche di controllo</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Nuovo nome]</td> 
>   <td> <p> Immetti o mappa un nuovo nome per la bacheca.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Nuova descrizione]</td> 
>   <td> <p> Inserisci o mappa una nuova descrizione della bacheca.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL ID organizzazione]</p> </td> 
>   <td> <p>Immettere o mappare l'ID [!UICONTROL Trello] univoco della bacheca che si desidera modificare con il modulo.  </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Subscribe] </td> 
>   <td> <p>Seleziona un’opzione per specificare se l’utente proprietario della connessione utilizzata da questo modulo è abbonato alla bacheca.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Livello di autorizzazione]</p> </td> 
>   <td> <p>Le bacheche hanno regole di voto e commento diverse per ogni livello di autorizzazione. Ad esempio: se la tua bacheca è [!UICONTROL Private] e imposti le regole di voto e commento come [!UICONTROL All], viene visualizzato un errore. </p> <p>Le votazioni e i commenti sono limitati ai seguenti gruppi per ogni livello di autorizzazione:</p> 
>    <ul> 
>     <li><strong>[!UICONTROL Privato]</strong>: 
>      Membri, membri e osservatori</li> 
>     <li><strong>[!UICONTROL Per Organizzazione]</strong>: 
>      Membri, membri e osservatori, membri dell’organizzazione</li> 
>     <li><strong>[!UICONTROL Public]</strong>: 
>      Membri, membri e osservatori, membri dell'organizzazione, tutti</li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
>   <td> <p>Seleziona un’opzione per specificare chi può votare su questa bacheca. Per informazioni sulle limitazioni di voto nei livelli di autorizzazione, vedere il campo [!UICONTROL Livello di autorizzazione].</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Commenti]</p> </td> 
>   <td> <p>Seleziona un’opzione per specificare chi può commentare le schede per questa bacheca. Per informazioni sulle limitazioni relative ai livelli di autorizzazione, vedere il campo [!UICONTROL Livello di autorizzazione].</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL inviti] </td> 
>   <td> <p>Seleziona chi può invitare le persone su questa bacheca.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Self-join]</td> 
>   <td> <p> Seleziona se i membri del team possono unirsi alla bacheca autonomamente o se devono essere invitati.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Copertine per schede]</td> 
>   <td> <p> Seleziona se i coperchi della scheda devono essere visualizzati su questa bacheca.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Sfondo] </td> 
>   <td> <p>Seleziona il colore dello sfondo o dello sfondo personalizzato.</p> <p>Nota: gli sfondi personalizzati sono disponibili solo per gli abbonati a [!UICONTROL Trello Gold and Business Class].</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL ID sfondo]</td> 
>   <td> <p> Se si è selezionato di utilizzare uno sfondo personalizzato nel campo [!UICONTROL Background], immettere o mappare l'ID dello sfondo che si desidera utilizzare.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
>   <td> <p>Scegli tra due modalità di aging della carta. </p> 
>    <ul> 
>     <li><strong>[!UICONTROL Modalità pirata]</strong>: le carte si lacerano, ingialliscono e si rompono come una vecchia mappa pirata quando invecchiano.</li> 
>     <li><strong>[!UICONTROL Modalità regolare]</strong>: le schede diventano progressivamente più trasparenti con l'invecchiamento. </li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Feed calendario abilitato]</td> 
>   <td> <p> Seleziona se il feed del calendario è abilitato o meno.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL &lt;Colore&gt; nome etichetta]</td> 
>   <td> <p> Assegna un nome all’etichetta colore desiderata.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Archive] </td> 
>   <td> <p>Seleziona un’opzione per indicare se desideri archiviare (chiudere) la bacheca. </p> </td> 
>  </tr> 
> </tbody> 
></table>


+++

+++ **[!UICONTROL Ottieni una bacheca]**

Questo modulo di azione recupera i dettagli di una bacheca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID bacheca]</p> </td> 
   <td> <p>Inserisci o mappa l’ID della bacheca di cui desideri recuperare le informazioni.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Questo modulo di ricerca recupera informazioni su una bacheca specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Inserisci o mappa il nome (o parte del nome) della bacheca di cui desideri ottenere le informazioni.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di schede restituite]</td> 
   <td> <p> Immetti il numero massimo di bacheche che [!DNL Workfront Fusion] restituirà durante un ciclo di esecuzione. Questo valore deve essere minore o uguale a 1000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parziale] </p> </td> 
   <td> <p>Per impostazione predefinita, questo modulo cerca nel contenuto dei membri le corrispondenze esatte di ogni parola nella query. Quando [!UICONTROL Parziale] è abilitato, il modulo cerca il contenuto che inizia con qualsiasi parola nella query.</p> <p> Ad esempio, se utilizzi la parola "sviluppo" per cercare una bacheca denominata "Rapporto sullo stato di sviluppo personale", per impostazione predefinita dovrai cercare l’intera parola. Se è abilitato [!UICONTROL Partial], è possibile cercare "dev" ma non "velopment".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bacheche] </td> 
   <td> <p>Inserisci "mine" o mappa un elenco separato da virgole degli ID della bacheca.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Annulla l&#39;assegnazione di un membro a una bacheca]**

Questo modulo rimuove un membro da una bacheca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p> Immetti (mappa o seleziona) l’ID della bacheca da cui desideri rimuovere l’utente.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Selezionare il membro da rimuovere dalla bacheca.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Bacheche da guardare]**

Questo modulo di attivazione inizia uno scenario quando viene aggiunta una nuova bacheca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immetti o mappa il numero massimo di bacheche che il modulo deve restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Elenchi

+++ **[!UICONTROL Crea un elenco]**

Questo modulo di azione crea un elenco su una bacheca specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p> Inserisci o mappa l’ID della bacheca in cui desideri creare un elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere o mappare un nome per il nuovo elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Seleziona se desideri aggiungere l’elenco in alto o aggiungerlo in basso nella scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia elenco]</td> 
   <td> <p> Se si sta copiando un elenco, selezionare la modalità di immissione dell'ID dell'elenco che si desidera copiare.</p> 
    <ul> 
     <li> <p><strong>Immetti manualmente</strong> </p> <p>Nel campo <strong>[!UICONTROL ID elenco]</strong>, immetti o mappa l'ID dell'elenco da copiare.<br></p> </li> 
     <li> <p><strong>Seleziona</strong> </p> <p>Seleziona la bacheca contenente l’elenco da copiare, quindi seleziona l’elenco.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Modifica elenco]**

Questo modulo di azione modifica un elenco esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco]</td> 
   <td> <p> Inserisci o mappa l’ID dell’elenco da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere o mappare un nuovo nome per l'elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p> Mappa o seleziona la bacheca in cui desideri spostare l’elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Seleziona se desideri aggiungere l’elenco in alto o aggiungerlo in basso nella scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Abbonato]</td> 
   <td> <p>Abilitare questa opzione se si desidera sottoscrivere il membro attivo all'elenco.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni un elenco]**

Questo modulo di azione recupera i dettagli di un elenco specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID elenco]</p> </td> 
   <td> <p>Inserisci o mappa l’ID dell’elenco di cui desideri recuperare le informazioni.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Schede di controllo spostate in un elenco]**

Questo modulo di attivazione si attiva quando una scheda viene spostata in un elenco specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Seleziona la bacheca contenente l’elenco da controllare per le schede.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Seleziona l’elenco da controllare per le schede.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Schede

+++ **[!UICONTROL Aggiungi un allegato]**

Questo modulo di azione aggiunge un allegato alla scheda selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda a cui desideri aggiungere un allegato.</p> 
    <ul> 
     <li> <p><strong>Immetti manualmente</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda a cui desideri aggiungere un allegato.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca contenente la scheda a cui desideri aggiungere un allegato, quindi seleziona l’elenco contenente la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di allegato]</p> </td> 
   <td> <p>Seleziona se desideri caricare il file direttamente o fornire un URL al file.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Immettere l'URL del file e specificare un nome per l'allegato.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archiviare o annullare l&#39;archiviazione di una scheda]**

Questo modulo di azione archivia o invia nuovamente una scheda alla bacheca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID scheda]</td> 
   <td> <p> Inserisci o mappa l’ID della scheda che desideri archiviare o inviare alla bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archivia o annulla archiviazione]</td> 
   <td> <p> Seleziona se desideri chiudere la scheda (archivio) o inviarla nuovamente alla bacheca (annulla archiviazione).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea una scheda]**

Questo modulo di azione crea una scheda in un elenco selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID elenco]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID dell’elenco in cui desideri aggiungere una scheda.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID elenco]</strong>, immetti o mappa l'ID dell'elenco in cui desideri aggiungere una scheda.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca contenente l’elenco in cui desideri aggiungere una scheda, quindi seleziona l’elenco.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette] </td> 
   <td> <p>Per ogni etichetta da aggiungere alla scheda, fare clic su <b>Aggiungi elemento</b> e immettere l'ID dell'etichetta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Membri]</td> 
   <td>Per ogni membro che si desidera aggiungere alla scheda, fare clic su <b>Aggiungi elemento</b> e immettere l'ID del membro. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere un nome per la nuova scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Descrizione]</p> </td> 
   <td> <p>Immettere la descrizione della scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Seleziona se desideri aggiungere la scheda in alto o aggiungerla in basso nell’elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scadenza]</td> 
   <td> <p> Immettere una data di scadenza per la scheda. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Completato]</td> 
   <td> <p> Abilita questa opzione per contrassegnare la scheda come completata alla data di scadenza.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL file]</td> 
   <td> <p>Inserisci o mappa l’URL di un file da aggiungere come allegato alla scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Immettere o mappare le informazioni per un file da aggiungere come allegato alla scheda. Seleziona un file da un modulo precedente o mappane il nome e i dati del file</p> 
     <p>Nota: esiste un limite di caricamento di file di 10 MB per ogni allegato. Tuttavia, i membri [!UICONTROL Business Class] e [!UICONTROL Trello Gold] hanno un limite di caricamento file di 250 MB per allegato.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia scheda]</td> 
   <td> <p> Se stai creando una nuova scheda come copia di una scheda esistente, seleziona la modalità di immissione dell’ID della scheda che desideri copiare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda da copiare.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la scheda che contiene la scheda da copiare, quindi seleziona l’elenco che contiene la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Modifica una scheda]**

Questo modulo di azione modifica una scheda esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda da modificare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda da modificare.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la scheda che contiene la scheda da modificare, quindi seleziona l’elenco che contiene la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nuovo nome]</td> 
   <td> <p>Immetti o mappa un nuovo nome per la scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nuova descrizione]</p> </td> 
   <td> <p>Immettere o mappare una nuova descrizione per la scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sposta una scheda]</p> </td> 
   <td> <p>Seleziona la bacheca o la bacheca e seleziona l’elenco in cui desideri spostare la scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Etichette] </td> 
   <td> <p>Per ogni etichetta da aggiungere alla scheda, fare clic su <b>Aggiungi elemento</b> e immettere l'ID dell'etichetta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Seleziona se desideri aggiungere la scheda in alto o [!UICONTROL append] alla fine dell'elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scadenza]</td> 
   <td> <p> Immettere una data di scadenza per la scheda. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Completato]</td> 
   <td> <p> Abilita questa opzione per contrassegnare la scheda come completata alla data di scadenza.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Membri] </td> 
   <td> <p>Per ogni membro che si desidera aggiungere alla scheda, fare clic su <b>Aggiungi elemento</b> e immettere o mappare l'ID del membro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID copertina allegato]</p> </td> 
   <td> <p>Immetti o mappa l’ID dell’allegato immagine che desideri utilizzare come copertina della scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Seleziona se il membro deve essere iscritto alla scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Seleziona un’opzione per indicare se desideri archiviare (chiudere) la scheda. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Ottieni una carta]**

Questo modulo di azione recupera i dettagli di una scheda selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID bacheca]</td> 
   <td> <p>Immetti l’ID della bacheca che contiene la scheda di cui desideri recuperare i dettagli. Questo consente di visualizzare i nomi dei campi personalizzati della bacheca.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell'ID della scheda su cui desideri recuperare i dettagli.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID carta]</strong>, immetti o mappa l'ID della carta di cui desideri recuperare i dettagli.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca contenente la scheda di cui desideri recuperare i dettagli, quindi seleziona l’elenco che contiene la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Cerca schede]**

Questo modulo di azione restituisce schede che corrispondono alla query di ricerca.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Seleziona le bacheche in cui desideri eseguire la ricerca. Se non è selezionata alcuna bacheca, la ricerca verrà effettuata su tutte le bacheche.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>Immettere la query di ricerca. Puoi perfezionare la ricerca utilizzando i seguenti operatori di ricerca:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>Puoi aggiungere "-" a qualsiasi operatore per effettuare una ricerca negativa, ad esempio <code>[!UICONTROL -has:members]</code> per cercare le schede senza alcun membro assegnato.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Restituisce le schede assegnate a un membro. È inoltre possibile utilizzare <code>member:</code>. Utilizza <code>@me</code> per includere solo le tue schede.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Restituisce le schede con etichetta. È inoltre possibile utilizzare <code>label:</code>. <code>label:"FIX IT"</code>, ad esempio, restituirà schede con l'etichetta "FIX IT".</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Restituisce le schede all’interno di una bacheca specifica. <code>board:Trello</code>, ad esempio, restituirà le schede nelle bacheche il cui nome contiene [!UICONTROL Trello].</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Restituisce le schede all’interno dell’elenco denominato "name".</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Restituisce schede con allegati. L'operatore <code>has</code>: può essere utilizzato anche con altri attributi, ad esempio <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> o <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Restituisce le carte in scadenza entro 24 ore. L'operatore <code>due:</code> può essere utilizzato anche con altri intervalli di tempo, ad esempio <code>due:week</code>, <code>due:month</code> o <code>due:overdue</code>. Puoi anche cercare un intervallo di giorni specifico. Ad esempio, l'aggiunta di <code>due:14</code> alla ricerca include le schede con scadenza nei successivi 14 giorni.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Restituisce le schede create nelle ultime 24 ore. L'operatore <code> created:</code> può essere utilizzato anche con altri intervalli di tempo come <code>created:week</code> o <code>created:month</code>. Puoi anche cercare un intervallo di giorni specifico. Ad esempio, l'aggiunta di <code>created:14</code> alla ricerca include schede create negli ultimi 14 giorni.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Restituisce le schede modificate nelle ultime 24 ore. L'operatore <code>edited:</code> può essere utilizzato anche con altri intervalli di tempo, ad esempio <code>edited:week</code> o <code>edited:month</code>. Puoi anche cercare un intervallo di giorni specifico. Ad esempio, l'aggiunta di <code>edited:21</code> alla ricerca include schede modificate negli ultimi 21 giorni.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Restituisce schede che corrispondono al testo delle descrizioni delle schede, degli elenchi di controllo, dei commenti o dei nomi. Ad esempio, <code>comment:"FIX IT"</code> restituirà le schede con "FIX IT" in un commento.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Restituisce schede aperte o archiviate. Se non viene specificato nessuno dei due, [!UICONTROL Trello] restituisce entrambi i tipi.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Sono incluse solo le schede su bacheche con protagonista.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di schede restituite]</td> 
   <td> <p> Immettere o mappare il numero massimo di schede che [!DNL Workfront Fusion] deve restituire durante un ciclo di esecuzione. Questo valore deve essere minore o uguale a 1000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parziale] </td> 
   <td> <p>Per impostazione predefinita, questo modulo cerca nel contenuto dei membri le corrispondenze esatte di ogni parola nella query. Quando [!UICONTROL Parziale] è abilitato, il modulo cerca il contenuto che inizia con qualsiasi parola nella query.</p> <p> Ad esempio, se utilizzi la parola "sviluppo" per cercare una bacheca denominata "Rapporto sullo stato di sviluppo personale", per impostazione predefinita dovrai cercare l’intera parola. Se è abilitato [!UICONTROL Partial], è possibile cercare "dev" ma non "velopment".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>Per cercare schede specifiche, fai clic su <b>Aggiungi elemento</b> e aggiungi l'ID della scheda.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Guarda le schede]**

Questo modulo di attivazione avvia uno scenario quando viene aggiunta una nuova scheda.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Seleziona la posizione da controllare per le schede.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tutte le schede]</strong> </li> 
     <li> <p><strong>Schede in una bacheca specifica</strong> </p> <p>Seleziona la bacheca da controllare per le schede</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Seleziona la bacheca contenente l’elenco da controllare per le schede, quindi seleziona l’elenco.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Membri

+++ **[!UICONTROL Aggiungere un membro a una scheda]**

Questo modulo di azione aggiunge il membro specificato alla scheda specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Immetti l'ID della scheda e l'ID del membro]</p> </td> 
   <td> <p>Scegli come inserire l'ID carta e l'ID membro.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Immettere o mappare l'ID <strong>[!UICONTROL Card]</strong> e l'ID membro <strong></strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Selezionare la bacheca contenente la scheda a cui si desidera aggiungere un membro, quindi selezionare l'elenco contenente la scheda, la scheda stessa e il membro che si desidera aggiungere alla scheda.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assegna un membro a una bacheca]**

Vedi &quot;[!UICONTROL Assegna un membro a una bacheca]&quot; in [bacheche](#boards).

+++

+++ **[!UICONTROL Cerca membri]**

Questo modulo di azione recupera informazioni sui membri [!UICONTROL Trello].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Immettere il nome o il nome utente dell'utente che si desidera trovare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parziale] </td> 
   <td> <p>Per impostazione predefinita, questo modulo cerca nel contenuto dei membri le corrispondenze esatte di ogni parola nella query. Quando [!UICONTROL Parziale] è abilitato, il modulo cerca il contenuto che inizia con qualsiasi parola nella query.</p> <p> Ad esempio, se utilizzi la parola "sviluppo" per cercare una bacheca denominata "Rapporto sullo stato di sviluppo personale", per impostazione predefinita dovrai cercare l’intera parola. Se è abilitato [!UICONTROL Partial], è possibile cercare "dev" ma non "velopment".</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di membri restituiti]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Annulla l&#39;assegnazione di un membro a una bacheca]**

Consulta &quot;[!UICONTROL Annulla l&#39;assegnazione di un membro da una bacheca]&quot; in [Bacheche](#boards).

+++

### Elenchi di controllo

+++ **[!UICONTROL Creare un elenco di controllo]**

Questo modulo di azione crea un elenco di controllo sulla scheda selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda in cui desideri aggiungere un elenco di controllo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un elenco di controllo.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca che contiene la scheda in cui desideri aggiungere un elenco di controllo, quindi seleziona l’elenco che contiene la scheda, quindi seleziona la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere o mappare un nome per l'elenco di controllo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Seleziona se desideri aggiungere l’elenco di controllo in alto o aggiungerlo in basso nella scheda.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserisci ID checklist]</p> </td> 
   <td> <p>Se si sta creando l'elenco di controllo copiandone uno esistente, immettere o mappare l'ID di un elenco di controllo di origine che si desidera copiare in quello nuovo.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Crea un elemento elenco di controllo]**

Questo modulo di azione aggiunge un elemento a un elenco di controllo specifico.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci ID checklist]</td> 
   <td> <p> Se si sta creando un nuovo elenco di controllo copiandone uno esistente, selezionare la modalità di immissione dell'ID dell'elenco di controllo in cui si desidera aggiungere un elemento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID elenco di controllo]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un elenco di controllo.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca che contiene la scheda in cui desideri aggiungere un elenco di controllo, quindi seleziona l’elenco che contiene la scheda, quindi seleziona la scheda, quindi seleziona l’elenco di controllo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome elemento]</p> </td> 
   <td> <p>Immettere o mappare un nome per il nuovo elemento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Seleziona se desideri aggiungere l'elemento all'inizio o [!UICONTROL append] alla fine dell'elenco di controllo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Selezionato]</p> </td> 
   <td> <p>Abilita questa opzione se desideri aggiungere l’elemento come già selezionato.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Modifica elemento elenco di controllo]**

Questo modulo di azione modifica un elenco di controllo esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID carta e un ID voce elenco di controllo]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda e dell’elenco di controllo in cui desideri modificare un elemento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID elenco di controllo]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un elenco di controllo.</p> <p>Nel campo <strong>[!UICONTROL ID elemento elenco di controllo]</strong>, immettere o mappare l'ID dell'elenco di controllo.</p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca che contiene la scheda in cui desideri aggiungere un elenco di controllo, quindi seleziona l’elenco che contiene la scheda, quindi seleziona la scheda, quindi seleziona l’elenco di controllo.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID elenco di controllo]</td> 
   <td>Selezionare o mappare l'elenco di controllo in cui si desidera spostare la voce dell'elenco.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nome elemento]</p> </td> 
   <td> <p>Immettere o mappare un nome per il nuovo elemento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Seleziona se desideri aggiungere l’elemento in alto o in basso nell’elenco di controllo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Selezionare se la voce dell'elenco di controllo è completa o incompleta.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Etichette

+++ **[!UICONTROL Aggiungere un&#39;etichetta a una scheda]**

Questo modulo di azione aggiunge un’etichetta a una scheda selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda in cui desideri aggiungere un elenco di controllo.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un elenco di controllo. Nel campo <strong>[!UICONTROL ID etichetta]</strong>, immettere o mappare l'ID dell'etichetta che si desidera aggiungere.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca che contiene la scheda in cui desideri aggiungere un elenco di controllo, quindi seleziona l’elenco che contiene la scheda, quindi seleziona la scheda. </p> <p>Seleziona l’etichetta da aggiungere alla scheda.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Commenti

+++ **[!UICONTROL Creare un commento in una scheda]**

Questo modulo di azione aggiunge un commento alla scheda selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda in cui desideri aggiungere un commento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un commento.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca contenente la scheda in cui desideri aggiungere un commento, quindi seleziona l’elenco contenente la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Inserisci o mappa il commento da aggiungere alla scheda selezionata.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Elenca commenti in una scheda]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID scheda]</td> 
   <td> <p> Seleziona la modalità di immissione dell’ID della scheda in cui desideri aggiungere un commento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Immetti manualmente]</strong> </p> <p>Nel campo <strong>[!UICONTROL ID scheda]</strong>, immetti o mappa l'ID della scheda in cui desideri aggiungere un commento.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Seleziona]</strong> </p> <p>Seleziona la bacheca contenente la scheda in cui desideri aggiungere un commento, quindi seleziona l’elenco contenente la scheda, infine la scheda.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di commenti restituiti]</td> 
   <td> <p> Immettere il numero massimo di commenti che [!DNL Workfront Fusion] restituirà durante un ciclo di esecuzione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da] </td> 
   <td> <p>Imposta la data di inizio del periodo in cui è stato creato il commento. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Imposta la data di fine del periodo in cui è stato creato il commento. Per un elenco dei formati di data e ora supportati, vedere <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Tipo di coercizione in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Osserva commenti]**

Questo modulo di attivazione avvia uno scenario quando viene aggiunto un commento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!UICONTROL Trello] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Selezionare la posizione da controllare per i commenti.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tutte le schede] ovunque</strong> </li> 
     <li> <p><strong>[!UICONTROL Bacheca]</strong> </p> <p>Seleziona la bacheca da controllare per i commenti</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Seleziona la bacheca contenente l’elenco da controllare per i commenti, quindi seleziona l’elenco.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Seleziona la bacheca contenente la scheda da controllare per i commenti, quindi seleziona l’elenco che contiene la scheda, quindi seleziona la scheda.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Immettere o mappare il numero massimo di commenti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] ID oggetto

* [Come trovare l&#39;ID o il collegamento rapido di una scheda in [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [Come trovare gli ID di altri oggetti in [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### Come trovare l&#39;ID o il collegamento rapido di una scheda in [!DNL Trello]

Se desideri modificare una scheda o creare un nuovo commento, è necessario conoscere l’ID della scheda o il relativo collegamento rapido. Puoi ottenere queste informazioni dall&#39;output del trigger [!UICONTROL Nuova scheda]. Per ottenere il collegamento rapido per una scheda, aprire la scheda e fare clic sul pulsante [!UICONTROL Condividi]. Il collegamento rapido si trova nella casella [!UICONTROL Collega a questa scheda], alla fine dell&#39;URL dopo `https://trello.com/c/`.

![Condividi e altro](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### Come trovare gli ID di altri oggetti in [!DNL Trello]

È possibile ottenere gli ID di bacheca, elenco e commento solo utilizzando i trigger. Il sito Web [!DNL `trello.com`] non mostra questi ID.
