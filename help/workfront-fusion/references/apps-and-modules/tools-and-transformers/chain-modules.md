---
title: Moduli catena
description: Utilizzando questi moduli, puoi concatenare gli scenari effettuando una chiamata all’altra.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
TQID: https://experienceleague.adobe.com/AlHUrliXikCc3OVHiBTjLNQFndCf5qLzOLuBvnDTUfA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 81d1dfcdb5c15f6a93e2793f9a0e41821b65c7e3
workflow-type: tm+mt
source-wordcount: 883
ht-degree: 10%

---

# Moduli di concatenamento

>[!IMPORTANT]
>
>Questa funzione è disponibile in Beta e non è consigliata per flussi di lavoro di produzione mission-critical. In quanto funzione di Beta, il comportamento può cambiare e i casi limite potrebbero non essere gestiti completamente.
>
>Per integrazioni stabili, puoi attivare un secondo scenario tramite webhook utilizzando un modulo di richiesta HTTP: questo modello utilizza primitive completamente supportate e fornisce a ogni scenario un controllo di esecuzione indipendente.
>
>Se scegli di utilizzare scenari concatenati, consulta [Creare più scenari insieme](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md) per indicazioni sulla progettazione.

Utilizzando i moduli Catena, potete collegare uno scenario a un altro.

<!--This article will be about the specific module configuration-->

Per istruzioni sulla pianificazione di scenari concatenati, vedere [Creare concatenamenti di più scenari](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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

>[!IMPORTANT]
>
> Prima di configurare questo modulo in uno scenario di produzione, verifica quanto segue:
>
> * **Non abilitare Commit Trigger Last (CTL)** in questo scenario quando Fire and Forget è disabilitato. CTL ritenterà lo scenario quando sospende l&#39;attesa di una risposta figlio, creando un ciclo di nuovi tentativi non limitato.
> * **Prestare attenzione quando si inserisce questo modulo all&#39;interno di un iteratore.** L’invio di uno scenario figlio per ogni elemento in un iteratore di grandi dimensioni crea un carico di piattaforma significativo. Valuta di allineare la logica dello scenario secondario o di pre-calcolare le ricerche condivise al di fuori dell’iteratore.
> * **Attivato e dimenticato** significa che l&#39;elemento padre non ha alcuna visibilità sull&#39;esecuzione o sul completamento dell&#39;elemento figlio. Da utilizzare solo quando gli errori figlio vengono monitorati in modo indipendente.
>
> Per istruzioni complete sulla progettazione, consulta [Incatenare più scenari](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios).

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
1. (Condizionale) Se desideri che lo scenario principale continui la sua esecuzione senza attendere una risposta dallo scenario secondario, abilita l&#39;opzione **Attiva e dimentica**.
1. Fare clic su **OK** per salvare il modulo.

>[!NOTE]
>
>Se crei un nuovo scenario figlio per questo modulo, lo scenario figlio viene aperto in una finestra del browser separata, che consente di visualizzare e configurare sia gli scenari padre che figlio contemporaneamente.

#### Restituisce la risposta all’elemento padre

Si trova nello scenario figlio e invia i dati nella struttura selezionata allo scenario padre. Puoi mappare questi dati in moduli successivi nello scenario principale.

>[!IMPORTANT]
>
> Se lo scenario figlio ha più route, **devi** garantire che la risposta Return to parent module sia raggiungibile da ogni percorso di esecuzione. Se il modulo di risposta Return si trova su una route ignorata o non eseguita, lo scenario padre attenderà indefinitamente una risposta che non arriva mai.
>
> Aggiungere la risposta Return al modulo padre dopo il router, su una route che viene sempre eseguita indipendentemente dal risultato del router, oppure aggiungere la gestione degli errori per garantire che venga sempre restituita una risposta anche quando si verifica un errore.

Per configurare il modulo Aggiungi risponditore:

1. Per utilizzare una struttura dati esistente, nel campo Struttura dati selezionare la struttura dati che verrà utilizzata per i dati restituiti dallo scenario figlio allo scenario padre.

   Oppure

   Per creare una nuova struttura dati per i dati, fare clic su **Aggiungi** accanto al campo Struttura dati e creare la struttura dati.

   Per istruzioni sulla creazione di una struttura dati, vedere [Strutture dati](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Fare clic su **OK** per salvare il modulo.
