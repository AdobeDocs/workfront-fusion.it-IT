---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere un modulo trigger a uno scenario di base
description: Scopri come aggiungere un modulo trigger per consentire allo scenario di cercare periodicamente nuove richieste e convertirle in progetti.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
TQID: https://experienceleague.adobe.com/xepLecibr9U6FpQM0neDy15DbFGF55rR6gVYvo644H4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 347280547bea92c0ee498da519495569a3cac661
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 11%
---
# Aggiungere un modulo trigger a uno scenario di base

I moduli di attivazione vengono posizionati all’inizio di uno scenario. Questi moduli iniziano l’esecuzione di uno scenario quando si è verificata una modifica in un determinato servizio. La modifica può consistere nella creazione di nuovi record, nell&#39;eliminazione di record, nell&#39;aggiornamento di record e così via. È possibile specificare i criteri per le modifiche che avviano lo scenario.

I moduli di polling controllano il servizio a un intervallo di tempo impostato e restituiscono informazioni sulle modifiche apportate durante tale intervallo. Se non ci sono state modifiche, il trigger non esegue lo scenario.

In questo esempio, aggiungi un modulo trigger che viene eseguito ogni 15 minuti e avvia uno scenario se sono state inviate richieste a una coda specifica. Lo scenario quindi converte tali richieste in un progetto.

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

## Aggiungi e configura il modulo trigger nella nuova esperienza (scelta consigliata)

* [Aggiungere il modulo trigger](#add-the-trigger-module)
* [Pianificare il modulo trigger](#schedule-the-trigger-module)
* [Aggiornare il secondo modulo](#update-the-second-module)
* [Test e attivazione](#test-and-activate)

### Aggiungere il modulo trigger

1. Apri lo scenario nell’editor dello scenario.
1. Fare clic con il pulsante destro del mouse sul primo modulo (Ricerca) e selezionare **[!UICONTROL Elimina modulo]**.

   Il modulo viene eliminato, lasciando un segnaposto vuoto.

1. Fai clic sul modulo vuoto per aprire l’elenco delle app e dei servizi.

   ![Selettore app e servizi](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Seleziona **Adobe Workfront**.
1. Seleziona **Record di controllo**.
1. Assicurati che il modulo utilizzi la stessa connessione degli altri moduli dello scenario.
1. Nel campo Tipo di record selezionare **Problema**.
1. Nel campo Filtro, selezionare **Solo nuovi record**.
1. Nella casella Output selezionare `ID`, `Name` e `Project ID`.
1. Fare clic su **OK** per salvare le impostazioni del modulo.

   Viene visualizzata la finestra Scegli da dove iniziare.

1. Seleziona **Da ora in data**.

### Pianificare il modulo trigger

1. Fare clic sull&#39;icona dell&#39;orologio nel modulo Record di controllo.

   ![Icona orologio nel modulo Record di controllo](assets/clock-icon-on-watch-record.png)

   Viene visualizzata la finestra di impostazione Schedule.

1. Nel campo Esegui scenario selezionare **A intervalli regolari**.

1. Fai clic su **OK**.

### Aggiornare il secondo modulo

Poiché il primo modulo è stato sostituito, il secondo modulo deve essere mappato al nuovo primo modulo.

1. Aprire il modulo Converti oggetto.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Record di controllo) per mapparlo al secondo modulo.
1. Fai clic su **OK**.

### Test e attivazione

1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.
1. Fai clic sull&#39;icona **[!UICONTROL Esegui una volta]**.

   Esegui una volta è solo un’icona nella nuova esperienza. Passa il puntatore sull&#39;icona per visualizzare la descrizione comando **[!UICONTROL Esegui una volta]**.

   ![pulsante esegui scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;opzione **Pianificazione** per passare a **Il**.

   Questo attiva lo scenario.

   ![Interruttore pianificazione](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Fai clic sull&#39;icona **Salva** ![Salva icona](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) nell&#39;area Controlli per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Aggiungere e configurare il modulo trigger nell’esperienza classica

* [Aggiungi il modulo del trigger (Classic)](#add-the-trigger-module-classic)
* [Pianifica il modulo del trigger (Classic)](#schedule-the-trigger-module-classic)
* [Aggiornare il secondo modulo (Classic)](#update-the-second-module-classic)
* [Test e attivazione (Classic)](#test-and-activate-classic)

### Aggiungi il modulo del trigger (Classic)

1. Apri lo scenario nell’editor dello scenario.
1. Fare clic con il pulsante destro del mouse sul primo modulo (Ricerca) e selezionare **Elimina modulo**.

   Il modulo viene eliminato, lasciando un segnaposto vuoto.

1. Fai clic sul modulo vuoto e seleziona **Adobe Workfront** dall&#39;elenco delle app.
1. Seleziona **Record di controllo**.
1. Assicurati che il modulo utilizzi la stessa connessione degli altri moduli dello scenario.
1. Nel campo Tipo di record selezionare **Problema**.
1. Nel campo Filtro, selezionare **Solo nuovi record**.
1. Nella casella Output selezionare `ID`, `Name` e `Project ID`.
1. Fare clic su **OK** per salvare le impostazioni del modulo.

   Viene visualizzata la finestra Scegli da dove iniziare.

1. Seleziona **Da ora in data**.

### Pianifica il modulo del trigger (Classic)

1. Fare clic sull&#39;orologio nel modulo Registrazione di controllo.

   Viene visualizzata la finestra di impostazione Schedule.

1. Nel campo Esegui scenario selezionare **A intervalli regolari**.

1. Fai clic su **OK**.

### Aggiornare il secondo modulo (Classic)

Poiché il primo modulo è stato sostituito, il secondo modulo deve essere mappato al nuovo primo modulo.

1. Aprire il modulo Converti oggetto.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Record di controllo) per mapparlo al secondo modulo.
1. Fai clic su **OK**.

### Test e attivazione (Classic)

1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.
1. Fai clic su **[!UICONTROL Esegui una volta]** nell&#39;angolo inferiore sinistro dell&#39;editor scenari.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario.
1. In Workfront Fusion, fai clic su **[!UICONTROL Salva]** nell&#39;angolo inferiore sinistro per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Risorse

* Per ulteriori informazioni sui moduli trigger, vedere [Moduli trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) nell&#39;articolo Panoramica dei moduli.
