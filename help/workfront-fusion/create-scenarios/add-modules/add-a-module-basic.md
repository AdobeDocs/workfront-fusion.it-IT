---
title: Aggiungere un modulo a uno scenario
description: Questo articolo descrive il processo di base per l’aggiunta di un modulo a uno scenario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Aggiungere un modulo a uno scenario

Uno scenario è costituito da una serie di moduli che indicano come i dati devono essere trasformati all’interno di un’app o trasferiti tra app e servizi web. Puoi creare un modulo aggiungendo e configurando i moduli.

Questo articolo descrive il processo di base per l’aggiunta di un modulo a uno scenario. Per istruzioni più specifiche su come aggiungere uno scenario, vedere gli altri articoli in [Aggiungi moduli: indice articolo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Aggiungere il primo modulo a uno scenario

Il primo modulo di uno scenario è in genere un modulo trigger.

Per ulteriori informazioni sui moduli trigger, vedere [Moduli trigger](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) nell&#39;articolo Panoramica dei moduli.

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
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

1. Se non ti trovi nell&#39;editor scenari dello scenario in cui desideri aggiungere un modulo, fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Per aggiungere un modulo a un altro modulo, passa il cursore sull&#39;handle destro del modulo dopo il quale vuoi aggiungere un modulo, quindi fai clic su **Aggiungi un altro modulo** quando viene visualizzato.

   Viene visualizzato l’elenco dei connettori, con tutti i connettori già utilizzati nello scenario.

1. (Facoltativo) Per selezionare un altro connettore, fare clic su **Aggiungi un altro modulo** nell&#39;elenco, quindi selezionare il connettore. È possibile digitare il nome del connettore nella barra di ricerca dell&#39;elenco per filtrare l&#39;elenco.
1. Configura il modulo.

   Per istruzioni sulla configurazione di moduli specifici, vedere l&#39;articolo relativo alle applicazioni selezionate, elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Inserire un modulo tra moduli esistenti in uno scenario

1. Se non ti trovi nell&#39;editor scenari dello scenario in cui desideri aggiungere un modulo, fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic sul percorso punteggiato tra i moduli in cui si desidera inserire un modulo.
1. Nel menu visualizzato, selezionare **Aggiungi modulo**.

Viene visualizzato l’elenco dei connettori, con tutti i connettori già utilizzati nello scenario.

1. (Facoltativo) Per selezionare un altro connettore, fare clic su **Aggiungi un altro modulo** nell&#39;elenco, quindi selezionare il connettore. È possibile digitare il nome del connettore nella barra di ricerca dell&#39;elenco per filtrare l&#39;elenco.
1. Configura il modulo.

   Per istruzioni sulla configurazione di moduli specifici, vedere l&#39;articolo relativo alle applicazioni selezionate, elencate in [Riferimenti alle applicazioni Fusion e ai relativi moduli: indice articolo](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Per creare un collegamento a un modulo specifico, aggiungere `?moduleId=<module-id>` all&#39;URL durante la visualizzazione delle pagine seguenti:
>
>* Pagina di modifica scenario (l&#39;URL termina in `/edit`)
>* Esecuzione di uno scenario specifico (l&#39;URL termina in `/logs/<log-id>`)
>
>`<module-id>` fa riferimento al numero accanto all&#39;etichetta del modulo durante la visualizzazione dello scenario.
>
>Questo può essere utile quando si eseguono scenari di debug o si copia la configurazione del modulo.
