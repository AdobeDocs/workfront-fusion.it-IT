---
title: Moduli delle schede madri Adobe Workfront
description: Puoi utilizzare il connettore per schede madri Adobe Workfront per automatizzare i processi all’interno delle schede Workfront e collegarlo ad app e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '2440'
ht-degree: 1%

---

# [!DNL Adobe Workfront] moduli Schede

>[!NOTE]
>
>Il connettore Boards Fusion è in stato beta. Di conseguenza, il supporto per questo connettore è limitato e potrebbe cambiare a causa del futuro sviluppo di schede madri. Inoltre, potrebbero esserci modifiche all’API di GraphQL senza preavviso che potrebbero influire sul processo del connettore Fusion.

Le bacheche Adobe Workfront sono strumenti flessibili che consentono la collaborazione in team fornendo l’accesso a una bacheca condivisa contenente colonne e schede.

Puoi utilizzare i moduli Schede Adobe Workfront per leggere o aggiornare i record, effettuare una chiamata API all’API delle schede Workfront o attivare uno scenario quando si verifica un’azione su una scheda.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td>
  <td> <p>Qualsiasi</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza</td>
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisito licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione lavoro, [!UICONTROL [!DNL Workfront Fusion] per automazione lavoro</p>
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

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).


## Prerequisiti

È necessario aver configurato una bacheca in Adobe Workfront prima di potersi connettere ad essa.

## Informazioni API per le schede madri Adobe Workfront

Il connettore delle schede madri Adobe Workfront utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione alle schede madri Workfront

>[!NOTE]
>
>È possibile utilizzare una connessione Workfront per connettersi alle schede madri Workfront oppure creare una connessione separata alle schede madri Workfront.

Per creare una connessione alle schede madri Workfront:

1. In qualsiasi modulo [!DNL Adobe Workfront Boards], fare clic su **[!UICONTROL Add]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Immettere un nome per la connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Seleziona se ti interessa la connessione a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Facoltativo)</p></td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client ID]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Facoltativo)</p></td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Facoltativo)</p></td>
          <td>Immetti l’URL che verrà utilizzato dall’istanza di Workfront per autenticare questa connessione. <p>Il valore predefinito è <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Immetti il prefisso host.<p>Il valore predefinito è <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Fare clic su **[!UICONTROL Continue]** per salvare la connessione e tornare al modulo.

## Moduli delle schede madri Adobe Workfront e relativi campi

Quando si configurano i moduli delle schede madri Workfront, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati campi aggiuntivi per le Schede Workfront, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Schede](#cards)
* [Bacheche](#boards)
* [Colonne](#columns)
* [Tag](#tags)
* [Commenti](#comments)
* [Altro](#other)

<!--

### Watch

#### Watch events

This trigger module starts a scenario when an event occurs on a board.

1. Click **[!UICONTROL Add]** to the right of the **Webhook** box.

1. Configure the webhook in the **[!UICONTROL Add a hook]** box that displays.

   When you are configuring this module, the following fields display.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>(Optional) Type a new name for the webhook</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Object type]</td> 
      <td>Select the type of [!DNL Workfront] object that you want the module to watch.</td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Objects to watch]</p> </td> 
      <td> Select whether you want to trigger a scenario when there is a new object, an updated object, a new or updated object, or a deleted object. </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Exclude events made by this connection</td> 
      <td>Enable this option to exclude events created or updated using the same connector that this trigger module uses. This can prevent situations where a scenario might trigger itself, causing it to repeat in an endless loop.</td> 
     </tr> 
    </tbody> 
   </table>

After the webhook is created, you can view the address of the endpoint that events are sent to.

-->

### Schede

* [Aggiungi voce elenco di controllo](#add-checklist-item)
* [Aggiungi sottoattività](#add-subtask)
* [Creare una scheda](#create-a-card)
* [Spostare una scheda](#move-a-card)
* [Leggi una scheda](#read-a-card)
* [Aggiornare una scheda](#update-a-card)

#### Aggiungi voce elenco di controllo

Questo modulo di azione aggiunge una voce dell’elenco di controllo alla scheda specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della carta a cui desideri aggiungere una voce all’elenco di controllo.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklist items]</td> 
   <td>Per ogni voce dell'elenco di controllo che si desidera aggiungere, fare clic su Aggiungi voce, immettere il nome della voce dell'elenco di controllo e selezionare se la voce è stata completata.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Aggiungi sottoattività

Questo modulo di azione aggiunge una sottoattività a una scheda in Bacheche. La scheda deve essere collegata. L’attività secondaria viene aggiunta anche all’attività Workfront rappresentata dalla scheda.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Parent card ID]</td> 
   <td>Inserisci o mappa l’ID della scheda a cui desideri aggiungere una sottoattività.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca contenente la scheda a cui desideri aggiungere un’attività secondaria.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Immettere o associare un nome per la nuova sottoattività.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Creare una scheda

Questo modulo di azione crea una nuova scheda su una scheda Workfront.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca a cui desideri aggiungere una scheda.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Immettere o mappare l'ID della colonna a cui si desidera aggiungere una sottoattività.<p>Puoi trovare l’ID di colonna nelle informazioni restituite dal modulo Read a board.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Immettere o mappare un nome per la nuova scheda.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Spostare una scheda

Questo modulo di azione sposta una scheda in una colonna diversa sulla stessa bacheca.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della carta da spostare.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca che contiene la scheda da spostare.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination column ID]</td> 
   <td>Inserisci o mappa l’ID della colonna in cui desideri spostare la scheda.<p>Puoi trovare l’ID di colonna nelle informazioni restituite dal modulo Read a board.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To index]</td> 
   <td>Immetti o mappa la posizione della scheda nella nuova colonna.<p>La posizione superiore nella colonna nell'indice 0.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Leggi una scheda

Questo modulo di azione recupera informazioni su una scheda specifica.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della carta da leggere.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare una scheda

Questo modulo di azione aggiorna le informazioni relative a una scheda specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Immetti o mappa l’ID della carta da aggiornare.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca che contiene la scheda da aggiornare.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Immetti o mappa un nuovo nome per la scheda.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Immettere o mappare una nuova descrizione per la scheda.</p></td> 
  </tr> 
 </tbody> 
</table>

### Bacheche

* [Creare una bacheca](#create-a-board)
* [Leggi una bacheca](#read-a-board)

#### Creare una bacheca

Questo modulo di azione crea una scheda in Workfront. Puoi specificare il tipo di bacheca da creare.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>Inserisci o mappa un nome per la nuova bacheca.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type]</td> 
   <td>Seleziona il tipo di bacheca da creare.</td> 
  </tr> 
 </tbody> 
</table>

#### Leggi una bacheca

Questo modulo di azione restituisce informazioni su una singola bacheca, ad esempio schede, colonne, tag e membri della bacheca.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Immetti o mappa l’ID della bacheca per la quale desideri recuperare informazioni.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

### Colonne

* [Creare una colonna](#create-a-column)
* [Cercare una colonna](#search-for-a-column)
* [Aggiornare una colonna](#update-a-column)

#### Creare una colonna

Questo modulo di azione crea una nuova colonna sulla bacheca specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca a cui desideri aggiungere una colonna.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Immetti o mappa l’ID della colonna da aggiornare.<p>Puoi trovare l’ID di colonna nelle informazioni restituite dal modulo Read a board.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column name]</td> 
   <td>Immettere o mappare un nuovo nome per la colonna.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP Limit]</td> 
   <td>Immettere o mappare un nuovo limite WIP per la colonna.</td> 
  </tr> 
 </tbody> 
</table>

#### Cercare una colonna

Questo modulo di ricerca restituisce informazioni sulla colonna con il nome specificato.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Immetti o mappa l’ID della bacheca che contiene la colonna da recuperare.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Immettere o mappare il nome della colonna che si desidera recuperare.</td> 
  </tr> 
 </tbody> 
</table>

#### Aggiornare una colonna

Questo modulo di azione aggiorna il nome o il limite WIP della colonna specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Immetti o mappa l’ID della bacheca che contiene la colonna da recuperare.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>Immettere o mappare il nome della colonna che si desidera recuperare.</td> 
  </tr> 
 </tbody> 
</table>

### Tag

* [Aggiungere un tag a una scheda](#add-card-tag)
* [Creare un tag](#create-a-tag)

#### Aggiungere un tag a una scheda

Questo modulo di azione aggiunge un tag a una scheda.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della scheda a cui desideri aggiungere un tag.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca contenente la scheda a cui desideri aggiungere un tag.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag ID]</td> 
   <td>Inserisci o mappa l’ID del tag da aggiungere.<p>Puoi trovare l’ID tag nelle informazioni restituite dal modulo Read a board.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Creare un tag

Questo modulo di azione crea un nuovo tag e gli assegna un colore.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Inserisci o mappa l’ID della bacheca per cui desideri creare un tag.<p>Puoi trovare l’ID della bacheca nell’URL quando visualizzi la bacheca in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag name]</td> 
   <td>Immetti o mappa il nome del nuovo tag.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag Color]</td> 
   <td>Seleziona il colore per questo tag.</td> 
  </tr> 
 </tbody> 
</table>

### Commenti

* [Creare un commento](#create-a-comment)
* [Leggi i commenti sulle schede](#read-card-comments)

#### Creare un commento

Questo modulo di azione ha creato un commento sulla scheda specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della scheda a cui desideri aggiungere un commento.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Immettere o mappare il testo del commento che si desidera aggiungere.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Leggi i commenti sulle schede

Questo modulo di azione recupera i commenti dalla scheda specificata.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Inserisci o mappa l’ID della carta per la quale desideri recuperare i commenti.<p>Puoi trovare l’ID della scheda nell’URL quando la visualizzi in Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Immettere il numero massimo di commenti che il modulo deve restituire in un ciclo di esecuzione.</p></td> 
  </tr> 
 </tbody> 
</table>

### Altro

#### Effettuare una chiamata API personalizzata

Questo modulo di azione effettua una chiamata personalizzata all’API delle schede madri Workfront.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>È possibile utilizzare una connessione Workfront esistente per connettersi alle schede madri Workfront oppure una connessione specifica alle schede madri Workfront. </p><p>Per istruzioni sulla connessione dell'app [!DNL Workfront] a [!DNL Workfront Fusion], vedere <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Creare una connessione alle schede madri Workfront</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Immettere un percorso relativo a <code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP in [!DNL Adobe Workfront Fusion]</a>.</p><p>Per la maggior parte delle chiamate alle bacheche il metodo è POST. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Determina il tipo di contenuto della richiesta.</p> <p>Ad esempio:<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Aggiungi la query per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Per le bacheche Workfront, in genere questa sezione viene lasciata vuota.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto del corpo per la chiamata API sotto forma di Graphql incorporato JSON </p> <p>Esempio:</p><p>In questo esempio viene aggiornato il nome di una colonna. È possibile includere <code>boardId</code> e <code>columnId</code> come GUID codificati o mappati da un modulo precedente.<p><pre>{<br> "query": "mutation { updateColumn(boardId: \"\", columnId: \"\", updateColumnInput: { name: \"\" }) { id name }}"<br>}</pre><p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
