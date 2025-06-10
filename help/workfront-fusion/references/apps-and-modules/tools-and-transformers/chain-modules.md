---
title: Moduli catena
description: Utilizzando questi moduli, puoi concatenare gli scenari effettuando una chiamata all’altra.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: 454e06527fe1a624f36be3b7f3682ff49a61d42d
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# Moduli catena

Utilizzando i moduli Catena, potete collegare uno scenario a un altro.

<!--This article will be about the specific module configuration-->

Per istruzioni sulla pianificazione di scenari concatenati, vedere [Creare concatenamenti di più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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
   <p>Nessun requisito di licenza per Workfront Fusion</p>
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

## Moduli catena e relativi campi

### Trigger

#### Ricevi dati dal genitore

Questo modulo è il modulo trigger nello scenario figlio e viene attivato dal modulo Call a child scenario nello scenario padre. Riceve i dati dallo scenario padre, che possono essere elaborati nello scenario figlio.

Per configurare Ricevi dati dal modulo padre:

1. Per utilizzare una struttura dati esistente, nel campo Struttura dati selezionare la struttura dati che verrà utilizzata per i dati di input dello scenario.

   Oppure

   Per creare una nuova struttura dati da utilizzare come dati di input dello scenario, fare clic su **Aggiungi** accanto al campo Struttura dati e creare la struttura dati.

   Per istruzioni sulla creazione di una struttura dati, vedere [Strutture dati](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Fare clic su **OK** per salvare il modulo.

### Azioni

#### Scenario di chiamata figlio

Questo modulo si trova nello scenario principale. I campi riflettono la struttura dati impostata nello scenario figlio Ricevi dati dal modulo padre.

>[!NOTE]
>
>* Puoi selezionare uno scenario figlio esistente o crearne uno nuovo tramite questo modulo.
>* Puoi creare la struttura dati durante la creazione di uno scenario figlio.

Per configurare il modulo di scenario Call a child

1. Aggiungi il modulo di scenario Call a child allo scenario.
1. Per utilizzare uno scenario figlio esistente, nel campo Catena selezionare lo scenario figlio che si desidera chiamare.

   Oppure

   Per creare un nuovo scenario figlio, fai clic su Aggiungi accanto al campo Catena. Lo scenario figlio viene visualizzato in una finestra separata, con la risposta Ricevi dati da padre e Restituisci da moduli padre attive.

   I campi configurati nel modulo trigger dello scenario figlio vengono visualizzati nel modulo dello scenario Call a child.

1. Immetti o mappa le informazioni da passare allo scenario figlio nel modulo di scenario Call a child.
1. Fare clic su **OK** per salvare il modulo.

>[!NOTE]
>
>Se crei un nuovo scenario figlio per questo modulo, lo scenario figlio viene aperto in una finestra del browser separata, che consente di visualizzare e configurare sia gli scenari padre che figlio contemporaneamente.

#### Restituisce la risposta all’elemento padre

Si trova nello scenario figlio e invia i dati nella struttura selezionata allo scenario padre. Puoi mappare questi dati in moduli successivi nello scenario principale.

Se lo scenario figlio dispone di più route, si consiglia di aggiungere questo modulo a una route che viene sempre eseguita ed eseguita dopo qualsiasi altra route.

Per configurare il modulo Aggiungi risponditore:

1. Per utilizzare una struttura dati esistente, nel campo Struttura dati selezionare la struttura dati che verrà utilizzata per i dati restituiti dallo scenario figlio allo scenario padre.

   Oppure

   Per creare una nuova struttura dati per i dati, fare clic su **Aggiungi** accanto al campo Struttura dati e creare la struttura dati.

   Per istruzioni sulla creazione di una struttura dati, vedere [Strutture dati](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Fare clic su **OK** per salvare il modulo.

