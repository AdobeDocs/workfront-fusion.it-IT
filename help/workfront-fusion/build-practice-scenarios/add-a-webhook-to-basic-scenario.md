---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere un webhook a uno scenario di base
description: I webhook, noti anche come trigger istantanei, sono un tipo specifico di modulo di trigger che può avviare uno scenario ogni volta che viene apportata una modifica, anziché in base a una determinata pianificazione.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
TQID: https://experienceleague.adobe.com/V3cpVf8NzJdGjSZvPA0Hy0Uui-zSdd986plS1Us0oNI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 4cd8b43e9ce9a16aca16397ce140cdd2467bf7d4
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 13%
---
# Aggiungere un webhook a uno scenario di base

I webhook, noti anche come trigger istantanei, sono un tipo specifico di modulo di trigger che può avviare uno scenario ogni volta che viene apportata una modifica, anziché in base a una determinata pianificazione.

In questo esempio, aggiungi un webhook per avviare uno scenario non appena una richiesta viene inviata a una coda di richieste specifica. Lo scenario quindi converte tali richieste in un progetto.

In questo esempio viene modificato lo scenario creato in [Crea uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>Workfront Fusion sta passando dall’editor dello scenario a una nuova esperienza. Durante questa transizione, sono disponibili sia le esperienze classiche che quelle nuove, e puoi passare da una all’altra in qualsiasi momento. È consigliabile utilizzare la nuova esperienza. Per ulteriori informazioni, consulta [Esperienze nuove e classiche](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) nell&#39;articolo Editor scenari.

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisiti

È necessario creare lo scenario descritto in [Creare uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) prima di seguire questa procedura.

## Aggiungi e configura il webhook nella nuova esperienza (scelta consigliata)

* [Aggiungere il modulo webhook](#add-the-webhook-module)
* [Aggiornare il secondo modulo](#update-the-second-module)
* [Test e attivazione](#test-and-activate)

### Aggiungere il modulo webhook

1. Apri lo scenario nell’editor dello scenario.
1. Fare clic con il pulsante destro del mouse sul primo modulo e selezionare **[!UICONTROL Elimina modulo]**.

   Il modulo viene eliminato, lasciando un segnaposto vuoto.

1. Fai clic sul modulo vuoto per aprire l’elenco delle app e dei servizi.

   ![Selettore app e servizi](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Seleziona **Adobe Workfront**.
1. Seleziona **Guarda gli eventi**.
1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Nel campo Tipo di record, seleziona **Problema**, in modo che il modulo si attivi per le modifiche nei problemi.
1. Nel campo Stato, selezionare **Nuovo stato**. Questo è un campo obbligatorio utilizzato per il filtro, che questo esempio non copre.
1. Nel campo Origine record selezionare **Solo nuovo record**. Questo consente allo scenario di attivarsi quando viene aggiunto un problema, non quando ne viene aggiornato o eliminato uno.
1. Fai clic su **Salva** per salvare la configurazione del modulo.

### Aggiornare il secondo modulo

1. Apri lo scenario.
1. Fare clic sul modulo **Converti oggetto** per aprirlo.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Osserva eventi) per mapparlo al secondo modulo.
1. Fai clic su **OK**.

### Test e attivazione

1. Fai clic sull&#39;icona **[!UICONTROL Esegui una volta]**.

   Esegui una volta è solo un’icona nella nuova esperienza. Passa il puntatore sull&#39;icona per visualizzare la descrizione comando **[!UICONTROL Esegui una volta]**.

   ![pulsante esegui scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

   Lo scenario deve essere in esecuzione per controllare la nuova richiesta.
1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.

   Lo scenario deve essere eseguito.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;opzione **Pianificazione** per passare a **Il**.

   Questo attiva lo scenario.

   ![Interruttore pianificazione](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Fai clic sull&#39;icona **Salva** ![Salva icona](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) nell&#39;area Controlli per salvare l&#39;avanzamento dello scenario.

## Aggiungere e configurare il webhook nell’esperienza classica

* [Aggiungi il modulo webhook (Classic)](#add-the-webhook-module-classic)
* [Aggiornare il secondo modulo (Classic)](#update-the-second-module-classic)
* [Test e attivazione (Classic)](#test-and-activate-classic)

### Aggiungi il modulo webhook (Classic)

1. Apri lo scenario nell’editor dello scenario.
1. Fare clic con il pulsante destro del mouse sul primo modulo e selezionare **Elimina modulo**.

   Il modulo viene eliminato, lasciando un segnaposto vuoto.

1. Fai clic sul modulo vuoto e seleziona **Adobe Workfront** dall&#39;elenco delle app.
1. Seleziona **Guarda gli eventi**.
1. Fai clic su **Aggiungi** accanto al campo Webhook.
1. Nel campo Tipo di record, seleziona **Problema**, in modo che il modulo si attivi per le modifiche nei problemi.
1. Nel campo Stato, selezionare **Nuovo stato**. Questo è un campo obbligatorio utilizzato per il filtro, che questo esempio non copre.
1. Nel campo Origine record selezionare **Solo nuovo record**. Questo consente allo scenario di attivarsi quando viene aggiunto un problema, non quando ne viene aggiornato o eliminato uno.
1. Fai clic su **Salva** per salvare la configurazione del modulo.

### Aggiornare il secondo modulo (Classic)

1. Apri lo scenario.
1. Fare clic sul modulo **Converti oggetto** per aprirlo.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Osserva eventi) per mapparlo al secondo modulo.
1. Fai clic su **OK**.

### Test e attivazione (Classic)

1. Fai clic su **[!UICONTROL Esegui una volta]** nell&#39;angolo inferiore sinistro dell&#39;editor scenari.

   Lo scenario deve essere in esecuzione per controllare la nuova richiesta.
1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.

   Lo scenario deve essere eseguito.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario.
1. In Workfront Fusion, fai clic su **[!UICONTROL Salva]** nell&#39;angolo inferiore sinistro per salvare l&#39;avanzamento dello scenario.
