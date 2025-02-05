---
title: Controllo del flusso
description: Quando crei o modifichi uno scenario, puoi configurare le impostazioni per controllare il modo in cui i dati scorrono all’interno di esso.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Controllo del flusso

Quando crei o modifichi uno scenario, puoi configurare le impostazioni per controllare il modo in cui i dati scorrono all’interno di esso.

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
   <p>Nessuna licenza Workfront Fusion richiesta.</p>
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

## Ripetitore

È possibile utilizzare un modulo [!UICONTROL Repeater] per ripetere un&#39;attività un determinato numero di volte. Un modulo [!UICONTROL Repeater] genera bundle uno dopo l&#39;altro.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
        <td>Immettere o mappare il valore che si desidera assegnare al modulo nella prima iterazione. Il valore predefinito è 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Immetti o mappa il numero di volte in cui desideri che il modulo si ripeta. Questo numero deve essere maggiore o uguale a 0 e minore o uguale a 10.000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>Questo è il numero di cui il modulo aumenta il valore. Il valore predefinito è 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Ad esempio, è possibile utilizzare un modulo [!UICONTROL Repeater] per inviare cinque messaggi di posta elettronica con gli oggetti &quot;Hello 1&quot;, &quot;Hello 2&quot; e così via, collegando il modulo **[!UICONTROL Email]>[!UICONTROL Send me an email]** al modulo [!UICONTROL Repeater].

1. Fare clic sull&#39;icona [!UICONTROL Flow Control] ![Icona Controllo flusso](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) nella parte inferiore dello schermo, quindi fare clic su **[!UICONTROL Repeater]** nel menu visualizzato.
1. Fare clic sul modulo [!UICONTROL Repeater], quindi fare clic su **[!UICONTROL Connect automatically]** nella casella visualizzata.

   Viene visualizzato il modulo Repeater (Ripetitore).

1. Nel campo **[!UICONTROL Repeats]** immettere il numero di ripetizioni (bundle generati) che si desidera ottenere con il modulo.

   In questo esempio, immetti 5.

   ![Ripetitore](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   Il valore dell&#39;elemento aumenta in ogni ripetizione di questo valore specificato nel campo **[!UICONTROL Step]**, che è possibile visualizzare selezionando **[!UICONTROL Show advanced settings]**. Questo numero è 1 per impostazione predefinita.

1. Fare clic su **[!UICONTROL OK]** per chiudere la casella **[!UICONTROL Flow Control]**.

1. Fare clic sull&#39;app o sul modulo di servizio connesso al modulo [!UICONTROL Repeater].
1. Nella casella visualizzata digitare le informazioni che si desidera ripetere.

   Nel nostro esempio di e-mail, dovresti digitare Hello nella casella [!UICONTROL Subject], quindi mappare `i` dal modulo del ripetitore.

   ![Ripetitore](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Il numero di ripetizioni non è determinato dal valore di `i`, poiché si troverebbe in un ciclo nella programmazione. Il modulo ripeterà il numero di volte indicato nel campo [!UICONTROL Repeats]. Il valore `i` cambia con ogni iterazione del modulo [!DNL repeater] e può essere mappato ai moduli successivi. Nell&#39;esempio precedente il valore di `i` viene mappato nel messaggio Hello, con messaggi che indicano &quot;Hello 1&quot;, Hello 2&quot; e così via.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Un [!UICONTROL Iterator] è un tipo speciale di modulo che converte un array in una serie di bundle. Ogni elemento array sarà un bundle separato nell&#39;output del modulo [!UICONTROL Iterator]. Per ulteriori informazioni, vedere [Modulo Iterator](/help/workfront-fusion/references/modules/iterator-module.md).

## Aggregatore array

Un aggregatore di array è un tipo speciale di modulo che consente di unire più bundle in un singolo bundle. Per ulteriori informazioni, vedere [Modulo aggregatore](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Il modulo [!UICONTROL Router] ti consente di diramare il flusso in più route ed elaborare i dati all&#39;interno di ciascuna route in modo diverso. Quando un modulo [!UICONTROL Router] riceve un bundle, lo inoltra a ogni route connessa nell&#39;ordine in cui le route sono state collegate al modulo [!UICONTROL Router]. Per ulteriori informazioni, vedere [Modulo router in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Direttive

Le direttive per la gestione degli errori consentono di controllare il modo in cui lo scenario reagisce agli errori.

Per informazioni sulle direttive per la gestione degli errori, vedere [Direttive per la gestione degli errori](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

