---
title: Mappare le informazioni da un modulo all'altro
description: La mappatura è il processo di assegnazione degli output di un modulo, strutturati in elementi, ai campi di input di un altro modulo.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Mappare le informazioni da un modulo all&#39;altro

La mappatura è il processo di assegnazione degli output di un modulo ai campi di input di un altro modulo.

Il pannello di mappatura viene visualizzato quando fai clic su un campo in cui puoi inserire un valore generato da un modulo precedente in uno scenario.

È inoltre possibile creare una formula utilizzando qualsiasi combinazione di funzioni ed elementi mappati dal pannello di mappatura con testo statico digitato. Questi elementi possono essere nidificati l’uno nell’altro.

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

## Mappare un elemento

Dopo aver creato una sequenza di moduli collegandone due o più, ogni modulo può elaborare i valori degli elementi generati dai moduli che lo precedono.

Per assegnare elementi di output ai campi di input di un modulo:

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri mappare i dati.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic sul modulo che deve elaborare l’output del modulo o dei moduli precedenti.
1. Nel pannello Impostazioni modulo visualizzato, fai clic su un campo in cui desideri utilizzare il valore di un elemento prodotto da un modulo precedente.

   Viene visualizzato il pannello di mappatura.

1. (Facoltativo) Per cercare un campo specifico nel pannello di mappatura, fate clic sulla barra di ricerca del pannello di mappatura e digitate il termine da cercare. Fare clic sul campo quando viene visualizzato nell&#39;elenco.

   I risultati della ricerca contengono il termine di ricerca e non fanno distinzione tra maiuscole e minuscole.
1. Per selezionare un valore che sia un elemento di una raccolta, fai clic sulla freccia accanto alla raccolta, quindi seleziona l’elemento quando viene visualizzato.

   ![Elemento raccolta](assets/collection-dropdown.png)

1. Fai clic su un elemento dal pannello di mappatura per inserirlo nel campo.

Per ulteriori informazioni, vedere [Configurare un modulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Risoluzione dei problemi

### Problema: elementi mancanti nel pannello di mappatura

Il pannello di mappatura visualizza gli elementi di output dei moduli precedenti. A volte, alcuni elementi potrebbero non essere presenti in questo pannello. Puoi eseguire il modulo a cui manca l’output nell’editor di scenari e il pannello di mappatura può quindi includere tali elementi nei moduli successivi. La procedura esatta varia a seconda del tipo di modulo

* [Trigger istantaneo](#instant-trigger)
* [Trigger di polling](#polling-trigger)
* [Altri moduli](#other-modules)

#### Trigger istantaneo

1. Fare clic con il pulsante destro del mouse sul modulo, quindi scegliere **[!UICONTROL Run this module only]** dal menu visualizzato.

   Poiché questo è un trigger istantaneo, inizia a guardare gli eventi.

1. Crea l’evento che il modulo sta guardando.

   Ad esempio, se il modulo è un modulo Workfront > Osserva eventi che controlla le assegnazioni delle attività, accedi a Workfront (come utente che non è quello utilizzato dalla connessione Fusion) e assegna un’attività.

1. Al termine dell’esecuzione del modulo, fai clic sulla bolla sopra il modulo per esplorarne l’output completo.

   Il pannello di mappatura per i moduli successivi ora contiene tutti gli elementi nell’output del modulo.

#### Trigger di polling

1. Fare clic con il pulsante destro del mouse sul modulo, quindi scegliere **[!UICONTROL Run this module only]** dal menu visualizzato.
1. Se non è presente alcun output, fare clic su **[!UICONTROL Choose where to start]** e modificare le impostazioni.
1. (Condizionale) Se non è presente alcun evento da elaborare, crea l’evento per il quale il modulo controlla e ripeti il passaggio 2.

   Ad esempio, se il modulo è un modulo Workfront > Osserva record che sta controllando le assegnazioni delle attività, accedi a Workfront (come utente che non è quello utilizzato dalla connessione Fusion) e assegna un’attività, quindi esegui di nuovo il modulo.

1. Al termine dell’esecuzione del modulo, fai clic sulla bolla sopra il modulo per esplorarne l’output completo.

   Il pannello di mappatura per i moduli successivi ora contiene tutti gli elementi nell’output del modulo.

#### Altri moduli

Puoi scegliere di eseguire:

* L&#39;intero scenario (o solo la parte contenente il modulo)
* Il modulo singolo

Per eseguire il modulo singolo:

1. Fare clic con il pulsante destro del mouse sul modulo, quindi scegliere **[!UICONTROL Run this module only]** dal menu visualizzato.
1. Fornire valori di esempio per gli elementi di input, quindi fare clic su **[!UICONTROL OK]**.
1. Al termine dell’esecuzione del modulo, fai clic sulla bolla sopra il modulo per esplorarne l’output completo.

   Il pannello di mappatura per i moduli successivi ora contiene tutti gli elementi nell’output del modulo.
