---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Utilizzare una funzione per aggiornare un progetto in uno scenario di base
description: Scopri come aggiungere una funzione per aggiornare un elemento di lavoro in Workfront.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---

# Utilizzare una funzione per aggiornare un progetto in uno scenario di base

L’aggiornamento di un elemento di lavoro di Workfront è un caso d’uso comune per Workfront Fusion. In questo esempio, utilizzerai una funzione per modificare il nome di un progetto in lettere maiuscole.

Fusion include molti tipi di funzioni che consentono di trasformare ed eseguire logica condizionale sui dati. Per ulteriori informazioni sull&#39;utilizzo delle funzioni, vedere [Panoramica delle funzioni](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

In questo esempio viene modificato lo scenario creato in [Crea uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

È necessario creare lo scenario descritto in [Creare uno scenario di base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) prima di seguire questa procedura.

## Utilizzare una funzione per aggiornare un progetto

### Aggiungi il modulo Aggiorna record allo scenario

1. Apri lo scenario nell’editor dello scenario.
1. Passa il puntatore del mouse sul cerchio parziale a destra del del secondo modulo, quindi fai clic su **[!UICONTROL Aggiungi un altro modulo]**.
1. Seleziona Adobe Workfront dall&#39;elenco delle applicazioni, quindi scegli il modulo **[!UICONTROL Aggiorna record]**.
1. Nel campo ID, seleziona il blocco ID che si trova sotto il modulo Converti oggetto. Questo è l&#39;ID del progetto generato da quel modulo.

   ![ID da Converti oggetto](assets/id-convert-object.png)

1. Nel campo Tipo di record selezionare Progetto, poiché l&#39;oggetto da aggiornare è un progetto.
1. Nell&#39;area Seleziona campi da mappare selezionare Nome.

   Viene aperto un campo Nome.
1. Continua a [Mappare la funzione per l&#39;aggiornamento del nome](#map-the-function-for-the-name-update).

### Mappa la funzione per l’aggiornamento del nome

Quando questo scenario converte una richiesta in un progetto, il nome del progetto è uguale alla richiesta. La funzione in questo caso prende il nome e le lettere in maiuscolo.

1. Fai clic sul campo **Nome**.

   Viene visualizzato il pannello di mappatura.
1. Nel pannello di mappatura, fai clic sull&#39;icona **Funzioni testo e binarie**. ![Icona funzioni testo](assets/toolbar-icon-text&binary-functions.png)
1. Selezionare la funzione **upper**.

   La funzione viene visualizzata nel campo Nome, inclusa la formattazione dell&#39;input previsto.

   L’input per questo esempio è il nome del problema da cui è stato convertito il progetto.

1. Spostare il cursore tra le parentesi, perché è qui che andrà l&#39;input.
1. Nel pannello di mappatura, fai clic sull&#39;icona **Output modulo**. ![Icona output modulo](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. Seleziona il blocco del nome restituito dal primo modulo.

   Il blocco del nome viene visualizzato nella funzione.

   ![Blocco nome nella funzione](assets/map-name.png)

1. Fare clic su **OK** per salvare le impostazioni del modulo.

### Test e attivazione

1. Verificare lo scenario facendo clic su **Esegui una volta** nell&#39;angolo inferiore sinistro della schermata.
1. Esamina l’output per garantire che lo scenario sia stato eseguito come previsto.
1. Quando si è certi che lo scenario funziona come previsto, fare clic sull&#39;interruttore **Pianificazione** in basso a sinistra dello schermo per **Attivato**.

   Questo attiva lo scenario. Gli scenari attivi vengono eseguiti in base alla pianificazione impostata nel modulo trigger.
1. In Workfront Fusion, fai clic su **[!UICONTROL Salva]** nell&#39;angolo inferiore sinistro per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Risorse

* [Mappare gli elementi utilizzando le funzioni](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
