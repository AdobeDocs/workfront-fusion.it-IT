---
title: Moduli evento
description: In uno scenario  [!DNL Adobe Workfront Fusion] , puoi automatizzare i flussi di lavoro che utilizzano Cvent, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# [!DNL Cvent] moduli

In uno scenario [!DNL Adobe Workfront Fusion], è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Cvent] e collegarlo a più applicazioni e servizi di terze parti.

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

## Connetti [!DNL Cvent] a [!DNL Adobe Workfront Fusion] {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>I moduli [!DNL Cvent] funzionano tramite un&#39;API [!UICONTROL SOAP]. Per creare una connessione a [!DNL Cvent], è necessario verificare quanto segue:
>
>* Hai accesso [!UICONTROL SOAP] all&#39;API [!DNL Cvent].
>* Gli indirizzi IP [!DNL Workfront Fusion] sono stati aggiunti al inserisco nell&#39;elenco Consentiti di della tua organizzazione.
>
>  Per un elenco di [!DNL Workfront Fusion] indirizzi IP, consulta [Configurare gli indirizzi IP per Fusion nel inserisco nell&#39;elenco Consentiti di della tua organizzazione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


Puoi creare una connessione al tuo account [!DNL Cvent] direttamente da un modulo [!DNL Cvent].

1. In qualsiasi modulo [!DNL Cvent], fare clic su **[!UICONTROL Add]** accanto al campo [!UICONTROL Connection].
1. Selezionare l&#39;area a cui si desidera connettersi.

   * [!UICONTROL North America]
   * [!UICONTROL Europe]
   * [!UICONTROL Sandbox]

1. Fare clic su **[!UICONTROL Continue]** per creare la connessione e tornare al modulo.

## [!DNL Cvent] moduli e relativi campi

Quando configuri [!DNL Cvent] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Cvent], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Azioni](#actions)
* [Ricerche](#searches)

### Azioni

* [[!UICONTROL Custom API Call]](#create-meeting-request)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Register Invitee]](#register-invitee)
* [[!UICONTROL Add Invitee]](#add-invitee)
* [[!UICONTROL Delete Contact]](#delete-contact)
* [[!UICONTROL Update Contact]](#update-contact)
* [[!UICONTROL Create meeting request]](#create-meeting-request)

#### [!UICONTROL Custom API Call]

Questo modulo di azione consente di effettuare una chiamata autenticata personalizzata all&#39;API [!DNL Cvent]. In questo modo è possibile creare un&#39;automazione del flusso di dati che non può essere eseguita dagli altri moduli [!DNL Cvent].

Durante la configurazione di questo modulo, vengono visualizzati i campi seguenti.

Il modulo restituisce il codice di stato a, insieme alle intestazioni e al corpo della chiamata API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Operazione</td> 
   td&gt; <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corpo (XML)</td> 
   <td> <p>Inserisci o mappa il corpo della chiamata API. Deve includere solo il codice XML. Il modulo includerà automaticamente le intestazioni di autenticazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Questo modulo di azione legge le informazioni su un record specifico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td>Selezionare il tipo di elemento del record che si desidera leggere.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL Invitee ID]</td> 
   <td> <p>Immetti o mappa l’ID dell’elemento da leggere.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selezionare i campi da includere nell'output del modulo. I campi sono disponibili in base al tipo di elemento selezionato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Register Invitee]

Questo modulo di azione registra un invitato per un evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
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

#### [!UICONTROL Add Invitee]

Questo modulo di azione invita un contatto a un evento.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Inserisci o mappa l’ID del contatto da aggiungere a un evento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Inserisci o mappa l’ID dell’evento a cui desideri aggiungere il contatto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Contact]

Questo modulo di azione elimina un singolo contatto in Cvent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID]</td> 
   <td> <p>Immetti o mappa l’ID del contatto da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Contact]

Questo modulo di azione aggiorna un contatto esistente utilizzando il suo ID.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Immetti o mappa l’ID del contatto da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Selezionare i campi per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> <p>Selezionare i campi per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create meeting request]

Questo modulo di azione aggiunge una convocazione di riunione al tuo account.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Form ID]</p> </td> 
   <td> <p>Immettere o mappare l'ID del modulo che si desidera utilizzare per creare la nuova convocazione di riunione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Meeting Request Fields]</td> 
   <td> <p>Selezionare i campi della convocazione di riunione per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Request Fields]</td> 
   <td> <p>Seleziona i campi della richiesta di evento per i quali vuoi inserire le informazioni, quindi inserisci i valori desiderati per tali campi.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP Request Fields]</td> 
   <td> <p>Selezionare i campi della richiesta di proposta per i quali si desidera inserire le informazioni, quindi immettere i valori desiderati per tali campi.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ricerche

#### [!UICONTROL List records]

Questo modulo di ricerca recupera informazioni su tutti i record di un tipo specifico.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Cvent] a [!DNL Workfront Fusion], vedere <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connessione di [!DNL Cvent] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td> <p>Selezionare il tipo di record da elencare.</p> 
    <ul> 
     <li> <p>Tutti gli eventi dal tuo account [!DNL Cvent]</p> </li> 
     <li> <p>Tutte le sessioni di un evento</p> </li> 
     <li> <p>Tutti gli invitati a un evento</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Se vengono elencati gli invitati o le sessioni, immettere o mappare l'ID dell'evento a cui sono associati tali invitati o sessioni.</p> </td> 
  </tr> 
 </tbody> 
</table>
