---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere un webhook a uno scenario di base
description: I webhook, noti anche come trigger istantanei, sono un tipo specifico di modulo di trigger che può avviare uno scenario ogni volta che viene apportata una modifica, anziché in base a una determinata pianificazione.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# Aggiungere un webhook a uno scenario di base

I webhook, noti anche come trigger istantanei, sono un tipo specifico di modulo di trigger che può avviare uno scenario ogni volta che viene apportata una modifica, anziché in base a una determinata pianificazione.

In questo esempio, aggiungi un webhook per avviare uno scenario non appena una richiesta viene inviata a una coda di richieste specifica. Lo scenario quindi converte tali richieste in un progetto.

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

## Aggiungere e configurare il webhook


### Aggiungere il modulo webhook

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

## Aggiornare il secondo modulo

1. Apri lo scenario.
1. Fare clic sul modulo **Converti oggetto** per aprirlo.
1. Nel campo ID problema, elimina il blocco ID nero. Il blocco è nero perché il modulo da cui è stato mappato non è più disponibile.
1. Seleziona il blocco ID sotto il primo modulo (Osserva eventi) per mapparlo al secondo modulo.
1. Fare clic su **OK**.



### Test e attivazione

1. Fare clic su **[!UICONTROL Run once]** nell&#39;angolo inferiore sinistro dell&#39;editor di scenari.

   Lo scenario deve essere in esecuzione per controllare la nuova richiesta.
1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema.

   Lo scenario deve essere eseguito.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario.
1. In [!DNL Workfront Fusion], fai clic su **[!UICONTROL Save]** nell&#39;angolo in basso a sinistra per salvare l&#39;avanzamento dello scenario.
