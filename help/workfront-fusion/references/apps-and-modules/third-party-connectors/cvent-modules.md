---
title: Moduli Cvent
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Cvent, nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
TQID: https://experienceleague.adobe.com/3Zi0MPk58Fvcshiq87skNQ3LlAMwGyRJ54KnktwX8cw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1134
ht-degree: 35%

---

# Moduli [!DNL Cvent]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL Cvent], nonché collegarli a più applicazioni e servizi di terze parti.

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

Per utilizzare i moduli [!DNL Cvent], è necessario disporre di un account [!DNL Cvent].

## Informazioni API evento

Il connettore Cvent utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Cvent] ad Adobe Workfront Fusion {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>I moduli [!DNL Cvent] funzionano tramite un&#39;API [!UICONTROL SOAP]. Per creare una connessione a [!DNL Cvent], è necessario verificare quanto segue:
>
>* Hai accesso [!UICONTROL SOAP] all&#39;API [!DNL Cvent].
>* Gli indirizzi IP di Workfront Fusion sono stati aggiunti al inserisco nell&#39;elenco Consentiti di dell’organizzazione.
>
>  Per un elenco degli indirizzi IP di Workfront Fusion, consulta [Configurare gli indirizzi IP per Fusion nel inserisco nell&#39;elenco Consentiti di dell&#39;organizzazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


Puoi creare una connessione al tuo account [!DNL Cvent] direttamente da un modulo [!DNL Cvent].

1. In qualsiasi modulo [!DNL Cvent], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Selezionare l&#39;area a cui si desidera connettersi.

   * [!UICONTROL America del Nord]
   * [!UICONTROL Europa]
   * [!UICONTROL Sandbox]

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## Moduli [!DNL Cvent] e relativi campi

Quando configuri i moduli [!DNL Cvent], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Cvent], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Ricerche](#searches)

### Azioni

* [[!UICONTROL Chiamata API personalizzata]](#create-meeting-request)
* [[!UICONTROL Leggi un record]](#read-a-record)
* [[!UICONTROL Registra invito]](#register-invitee)
* [[!UICONTROL Aggiungi invito]](#add-invitee)
* [[!UICONTROL Elimina contatto]](#delete-contact)
* [[!UICONTROL Aggiorna contatto]](#update-contact)
* [[!UICONTROL Crea convocazione di riunione]](#create-meeting-request)

#### [!UICONTROL Chiamata API personalizzata]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all’API [!DNL Cvent]. In questo modo puoi creare un’automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Cvent].

Durante la configurazione di questo modulo, vengono visualizzati i seguenti campi.

Il modulo restituisce il codice di stato a, insieme alle intestazioni e al corpo della chiamata API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Operazione</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo (XML)</td> 
   <td> <p>Inserisci o mappa il corpo della chiamata API. Deve includere solo il codice XML. Il modulo includerà automaticamente le intestazioni di autenticazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Leggi un record]

Questo modulo di azione legge le informazioni su un record specifico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di record]</p> </td> 
   <td>Selezionare il tipo di elemento del record che si desidera leggere.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL Invitee ID]</td> 
   <td> <p>Immetti o mappa l’ID dell’elemento da leggere.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Selezionare i campi da includere nell'output del modulo. I campi sono disponibili in base al tipo di elemento selezionato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Registra invito]

Questo modulo di azione registra un invitato per un evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID invito</p> </td> 
   <td> <p>Immettere o mappare l'ID dell'invitato che si desidera registrare per un evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID evento</td> 
   <td> <p>Immettere o mappare l'ID dell'evento per il quale si desidera registrare l'invitato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiungi invito]

Questo modulo di azione invita un contatto a un evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID contatto]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del contatto da aggiungere a un evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td> <p>Inserisci o mappa l’ID dell’evento a cui desideri aggiungere il contatto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina contatto]

Questo modulo di azione elimina un singolo contatto in Cvent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID contatto]</td> 
   <td> <p>Immetti o mappa l’ID del contatto da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna contatto]

Questo modulo di azione aggiorna un contatto esistente utilizzando il suo ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID contatto]</p> </td> 
   <td> <p>Immetti o mappa l’ID del contatto da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi]</td> 
   <td> <p>Selezionare i campi per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi personalizzati]</td> 
   <td> <p>Selezionare i campi per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea convocazione di riunione]

Questo modulo di azione aggiunge una convocazione di riunione al tuo account.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID modulo]</p> </td> 
   <td> <p>Immettere o mappare l'ID del modulo che si desidera utilizzare per creare la nuova convocazione di riunione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi di convocazione riunione]</td> 
   <td> <p>Selezionare i campi della convocazione di riunione per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campi Richiesta Evento]</td> 
   <td> <p>Seleziona i campi della richiesta di evento per i quali vuoi inserire le informazioni, quindi inserisci i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP Request Fields]</td> 
   <td> <p>Selezionare i campi della richiesta di proposta per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL Elenca record]

Questo modulo di ricerca recupera informazioni su tutti i record di un tipo specifico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connessione]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a Workfront Fusion, vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Cvent] ad Adobe Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di record]</p> </td> 
   <td> <p>Seleziona il tipo di record che desideri creare.</p> 
    <ul> 
     <li> <p>Tutti gli eventi dal tuo account [!DNL Cvent]</p> </li> 
     <li> <p>Tutte le sessioni di un evento</p> </li> 
     <li> <p>Tutti gli invitati a un evento</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID evento]</td> 
   <td> <p>Se vengono elencati gli invitati o le sessioni, immettere o mappare l'ID dell'evento a cui sono associati tali invitati o sessioni.</p> </td> 
  </tr> 
 </tbody> 
</table>
