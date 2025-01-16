---
title: Aggiungere un modulo a uno scenario
description: Questo articolo descrive il processo di base per l’aggiunta di un modulo a uno scenario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# Aggiungere un modulo a uno scenario

Uno scenario è costituito da una serie di moduli che indicano come i dati devono essere trasformati all’interno di un’app o trasferiti tra app e servizi web. Puoi creare un modulo aggiungendo e configurando i moduli.

Questo articolo descrive il processo di base per l’aggiunta di un modulo a uno scenario. Per istruzioni più specifiche su come aggiungere uno scenario, vedere gli altri articoli in [Aggiungi moduli: indice articolo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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

## Aggiungere il primo modulo a uno scenario

Il primo modulo di uno scenario è in genere un modulo trigger.

Per ulteriori informazioni sui moduli trigger, vedere [Moduli trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) nell&#39;articolo Panoramica dei moduli.

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Inizia a creare uno scenario facendo clic su **Crea un nuovo scenario** nell&#39;angolo superiore destro della schermata.

   Viene aperto l’editor dello scenario, con un modulo segnaposto (punto interrogativo) e l’elenco dei connettori disponibili.

   ![Modulo segnaposto](assets/placeholder-module.png)

1. Seleziona il connettore o il webhook che avvierà questo scenario. È possibile digitare il nome del connettore nella barra di ricerca dell&#39;elenco per filtrare l&#39;elenco.
1. Configura il modulo.

   Per istruzioni sulla configurazione di moduli specifici, vedere l&#39;articolo relativo alle applicazioni selezionate, elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Se hai rimosso il primo modulo da uno scenario e desideri sostituirlo, fai clic sul modulo segnaposto (punto interrogativo) per aprire l’elenco dei connettori.

## Aggiungere un altro modulo a uno scenario

1. Se non ti trovi nell&#39;editor dello scenario in cui desideri aggiungere un modulo, fai clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri esportare una blueprint.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Per aggiungere un modulo a un altro modulo, passa il cursore sull&#39;handle destro del modulo dopo il quale vuoi aggiungere un modulo, quindi fai clic su **Aggiungi un altro modulo** quando viene visualizzato.

   Viene visualizzato l’elenco dei connettori, con tutti i connettori già utilizzati nello scenario.

1. (Facoltativo) Per selezionare un altro connettore, fare clic su **Aggiungi un altro modulo** nell&#39;elenco, quindi selezionare il connettore. È possibile digitare il nome del connettore nella barra di ricerca dell&#39;elenco per filtrare l&#39;elenco.
1. Configura il modulo.

   Per istruzioni sulla configurazione di moduli specifici, vedere l&#39;articolo relativo alle applicazioni selezionate, elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Inserire un modulo tra moduli esistenti in uno scenario

1. Se non ti trovi nell&#39;editor dello scenario in cui desideri aggiungere un modulo, fai clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri esportare una blueprint.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic sul percorso punteggiato tra i moduli in cui si desidera inserire un modulo.
1. Nel menu visualizzato, selezionare **Aggiungi modulo**.

Viene visualizzato l’elenco dei connettori, con tutti i connettori già utilizzati nello scenario.

1. (Facoltativo) Per selezionare un altro connettore, fare clic su **Aggiungi un altro modulo** nell&#39;elenco, quindi selezionare il connettore. È possibile digitare il nome del connettore nella barra di ricerca dell&#39;elenco per filtrare l&#39;elenco.
1. Configura il modulo.

   Per istruzioni sulla configurazione di moduli specifici, vedere l&#39;articolo relativo alle applicazioni selezionate, elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
