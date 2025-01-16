---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Aggiungere un filtro a uno scenario di base
description: I filtri ti consentono di garantire che lo scenario avanzi solo se vengono soddisfatte determinate condizioni.
author: Becky
feature: Workfront Fusion
exl-id: 78ab27fe-e2dd-4b52-b986-77b4b7ea3b5e
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 1%

---

# Aggiungere un filtro a uno scenario di base

I filtri ti consentono di garantire che lo scenario avanzi solo se vengono soddisfatte determinate condizioni.

In questo esempio, aggiungi un filtro allo scenario che consente di creare un nuovo progetto a partire da una richiesta solo se la richiesta è stata inviata a una coda di richieste specifica.

In questo esempio viene modificato lo scenario creato in [Crea uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>I moduli di attivazione di Workfront includono filtri che consentono l’avvio di uno scenario solo se vengono soddisfatte determinate condizioni. Tuttavia, poiché i filtri tra moduli vengono utilizzati per ogni caso di utilizzo non-trigger e non-Workfront, è importante imparare a utilizzare i filtri tra i moduli. In questo esempio viene utilizzato un filtro tra moduli per la funzionalità che potrebbe essere soddisfatta con un filtro interno al modulo.

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

## Aggiungi un filtro

### Preparare l’aggiunta del filtro

1. Apri lo scenario.
1. Fai clic sul primo modulo per aprirlo.
1. Nell&#39;area **Output**, selezionare `Project`.
Ora dovresti avere `ID`, `Name` e `Project` selezionati.
1. Scegliere OK per salvare le impostazioni del modulo.
1. Apri Workfront.
1. In Workfront, individua il progetto che rappresenta la coda di richieste con cui lo scenario Fusion lavorerà.

   Il progetto deve trovarsi nello stesso account Workfront per il quale è impostata la connessione Fusion.

1. Prendi nota dell’ID progetto nell’URL.

   Esempio: https://\&lt;Dominio\>.my.workfront.com/project/\&lt;ID progetto\>/attività

### Aggiungere e configurare il filtro

1. Torna allo scenario nell’editor scenario.
1. Fare clic sull&#39;icona chiave inglese ![icona chiave inglese](assets/wrench-icon.png) tra il primo e il secondo modulo e selezionare **Imposta filtro**.
1. Nel campo Etichetta, immettere un&#39;etichetta per il filtro, ad esempio &quot;Filtra per coda richieste&quot;.
1. Nell&#39;area **Condizione**, nel campo superiore, mappare `projectID` dal primo modulo.

   ![Mappa ID progetto](assets/map-proj-id.png)
1. Lascia l&#39;operatore **Condition** uguale a.
1. Nel campo inferiore dell&#39;area **Condizione**, incolla l&#39;ID progetto di cui hai preso nota dall&#39;URL del progetto in [Prepara ad aggiungere il filtro](#prepare-to-add-the-filter).
1. Fare clic su **OK** per salvare le impostazioni del filtro.

### Test e attivazione

1. Vai all’ambiente Workfront a cui si connette Fusion e aggiungi un problema al progetto specificato nel filtro. Aggiungi un altro problema a un altro progetto.
1. Fare clic su **[!UICONTROL Run once]** nell&#39;angolo inferiore sinistro dell&#39;editor di scenari.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.

   Entrambi i problemi dovrebbero comparire nell’output del primo modulo, ma solo il problema nel progetto specificato dovrebbe comparire come input nel secondo modulo.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario.
1. In [!DNL Workfront Fusion], fai clic su **[!UICONTROL Save]** nell&#39;angolo in basso a sinistra per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Risorse

* Per ulteriori informazioni sui filtri, vedere [Aggiungere un filtro a uno scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
