---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere un modulo trigger a uno scenario di base
description: Scopri come aggiungere un modulo trigger per consentire allo scenario di cercare periodicamente nuove richieste e convertirle in progetti.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 1%

---

# Aggiungere un modulo trigger a uno scenario di base

I moduli di attivazione vengono posizionati all’inizio di uno scenario. Questi moduli iniziano l’esecuzione di uno scenario quando si è verificata una modifica in un determinato servizio. La modifica può consistere nella creazione di nuovi record, nell&#39;eliminazione di record, nell&#39;aggiornamento di record e così via. È possibile specificare i criteri per le modifiche che avviano lo scenario.

I moduli di polling controllano il servizio a un intervallo di tempo impostato e restituiscono informazioni sulle modifiche apportate durante tale intervallo. Se non ci sono state modifiche, il trigger non esegue lo scenario.

In questo esempio, aggiungi un modulo trigger che viene eseguito ogni 15 minuti e avvia uno scenario se sono state inviate richieste a una coda specifica. Lo scenario quindi converte tali richieste in un progetto.

In questo esempio viene modificato lo scenario creato in [Crea uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

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
   <td> <p>Nuovo: [!UICONTROL Standard]</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] piano: [!DNL Workfront Fusion] incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

È necessario creare lo scenario descritto in [Creare uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) prima di seguire questa procedura.

## Aggiungere e configurare il modulo trigger

### Aggiungere il modulo trigger

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

### Pianificare il modulo trigger

1. Fare clic sull&#39;orologio nel modulo Record di controllo.

   Viene visualizzata la finestra di impostazione Schedule.

1. Nel campo Esegui scenario selezionare **A intervalli regolari**.

1. Fare clic su **OK**.

### Aggiornare il secondo modulo

Poiché il primo modulo è stato sostituito, il secondo modulo deve essere mappato al nuovo primo modulo.

1. Aprire il modulo Converti oggetto.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Record di controllo) per mapparlo al secondo modulo.
1. Fare clic su **OK**.

### Test e attivazione

1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.
1. Fare clic su **[!UICONTROL Run once]** nell&#39;angolo inferiore sinistro dell&#39;editor di scenari.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario.
1. In [!DNL Workfront Fusion], fai clic su **[!UICONTROL Save]** nell&#39;angolo in basso a sinistra per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Risorse

* Per ulteriori informazioni sui moduli trigger, vedere [Moduli trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) nell&#39;articolo Panoramica dei moduli.
