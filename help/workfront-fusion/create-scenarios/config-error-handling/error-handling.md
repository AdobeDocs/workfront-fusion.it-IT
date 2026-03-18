---
title: Aggiungere la gestione degli errori
description: Quando si verificano errori durante l'esecuzione di uno scenario, in genere ciò è dovuto al fatto che un servizio non è disponibile a causa di un errore, che risponde con dati imprevisti o che la convalida dei dati di input non riesce.
author: Becky
feature: Workfront Fusion
exl-id: 82ddaf73-ecf9-4fd6-8f8e-909351023c77
source-git-commit: d7072a2dca50bf47f20d1f25dba4d3fb819d3ddc
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 9%

---

# Aggiungere la gestione degli errori

Durante l’esecuzione di uno scenario possono verificarsi errori.

Ad esempio, può verificarsi un errore perché:

* Un servizio non è disponibile a causa di un errore
* Un servizio risponde con dati imprevisti
* La convalida dei dati di input non riesce
* Altri motivi

Se un modulo rileva un errore durante l’esecuzione dello scenario e non è presente alcuna route di gestione degli errori associata al modulo o alla relativa route, viene eseguita la logica di gestione degli errori predefinita.

Aggiungendo un gestore degli errori a un modulo o a una route, è possibile sostituire la logica di gestione degli errori predefinita con la propria. Adobe Workfront Fusion offre cinque diverse direttive che possono essere inserite alla fine delle route del gestore degli errori.

Per ulteriori informazioni sulla gestione degli errori predefinita, vedere [Tipi di errore](/help/workfront-fusion/references/errors/error-processing.md).

Per ulteriori informazioni sulle direttive per la gestione degli errori, vedere [Direttive per la gestione degli errori](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

>[!NOTE]
>
>Workfront Fusion supporta la gestione degli errori a livello di route, consentendo di definire una logica di gestione degli errori una volta per route, anziché associare gestori degli errori a ogni singolo modulo.
>Poiché la gestione degli errori a livello di route è un metodo più scalabile, coerente e pulito dal punto di vista dell&#39;architettura per gestire gli errori, soprattutto nelle automazioni avanzate multi-branch, si consiglia di utilizzare la gestione degli errori a livello di route come best practice.

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

## Posizione e gerarchia del gestore degli errori

È possibile aggiungere gestori di errori ai singoli moduli o ai router.

Un gestore di errori associato a un modulo si attiva solo per gli errori rilevati durante l’elaborazione di tale modulo specifico.

Un gestore di errori collegato a un router attiva gli errori rilevati da qualsiasi modulo sulla route del router. Sono inclusi gli errori rilevati in tutte le route secondarie che non dispongono di un gestore degli errori nel router.

Gli errori vengono gestiti dalla seguente gerarchia:

1. Modulo
2. Router
3. Router padre
4. Gestione degli errori predefinita

>[!BEGINSHADEBOX]

### Esempio

Prendi in considerazione lo scenario di esempio seguente:

![Scenario di esempio che mostra route e gestori di errori](assets/error-handling-route-example-with-numbers.png)

1. Questo modulo ha un gestore di errori. Qualsiasi errore in questo modulo viene gestito dalla direttiva Commit.
1. Questo modulo non dispone di un gestore di errori. Se questo modulo rileva un errore, l&#39;errore viene gestito dal gestore sul router che ha creato la route del modulo. Qualsiasi errore in questo modulo viene gestito dalla direttiva di rollback.
1. Questo modulo non dispone di un gestore degli errori, né il router che ha creato la route del modulo, ma è presente un gestore degli errori nel router successivo. Qualsiasi errore in questo modulo viene gestito dalla direttiva Break.

>[!NOTE]
>
>* Se un modulo non dispone di un gestore degli errori sul modulo, sul router o su qualsiasi router padre, tutti gli errori su tale modulo vengono gestiti per impostazione predefinita.
>* Per creare un gestore degli errori globale, creare un router vicino all&#39;inizio dello scenario e allegare la gestione degli errori a tale router.


>[!ENDSHADEBOX]

## Aggiungi un gestore errori

È possibile aggiungere un gestore degli errori a un modulo o a un router.

* [Aggiungere un gestore degli errori a un modulo](#add-an-error-handler-to-a-module)
* [Aggiungere un gestore degli errori a un router](#add-an-error-handler-to-a-router)

### Aggiungere un gestore degli errori a un modulo

Per aggiungere un gestore degli errori a un modulo:

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera aggiungere un ciclo di lavorazione per la gestione degli errori.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic con il pulsante destro del mouse sul modulo dopo il quale si desidera aggiungere una route del gestore degli errori e selezionare **[!UICONTROL Aggiungi gestore errori]**:

   ![Route gestore errori](assets/error-handler-route.png)

   Al modulo viene aggiunta una route di gestore degli errori. Se il modulo è l’ultimo modulo di una route, il gestore degli errori segue direttamente il modulo. Se il modulo contiene più moduli, viene aggiunta una route separata del gestore degli errori.

   Il modulo di gestione degli errori mostra un elenco di direttive e delle app utilizzate nel tuo scenario.

   ![Errore route](assets/error-route.png)

1. Selezionare una delle direttive.

   Oppure

   Aggiungere uno o più moduli alla route del gestore degli errori.

   Se si aggiungono altri moduli alla route, per impostazione predefinita viene applicata la direttiva Ignora. Se si verifica un errore, vengono elaborati i moduli successivi di tale route.

   Per ulteriori informazioni sulle direttive, vedere [Errore nella gestione delle direttive](#error-handling-directives) in questo articolo.

1. (Facoltativo) Aggiungi un filtro al percorso di gestione degli errori. Per istruzioni, vedere [Aggiungere filtri e nidificazioni alle route di gestione degli errori](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md).

>[!NOTE]
>
>Si noti che una route del gestore degli errori è composta da cerchi trasparenti, mentre una route regolare è composta da cerchi solidi.

### Aggiungere un gestore degli errori a un router

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera aggiungere un ciclo di lavorazione per la gestione degli errori.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic con il pulsante destro del mouse sul router in cui si desidera aggiungere una route del gestore degli errori e selezionare **[!UICONTROL Aggiungi gestore errori]**:

   ![Route gestore errori](assets/error-handler-on-router.png)

   Al router viene aggiunta una route di gestore degli errori.

   Il modulo di gestione degli errori mostra un elenco di direttive e delle app utilizzate nel tuo scenario.

   ![Errore route](assets/error-handler-route-from-router.png)

1. Selezionare una delle direttive.

   Oppure

   Aggiungere uno o più moduli alla route del gestore degli errori.

   Se si aggiungono altri moduli alla route, per impostazione predefinita viene applicata la direttiva Ignora. Se si verifica un errore, vengono elaborati i moduli successivi di tale route.

   Per ulteriori informazioni sulle direttive, vedere [Errore nella gestione delle direttive](#error-handling-directives) in questo articolo.

1. (Facoltativo) Aggiungi un filtro al percorso di gestione degli errori. Per istruzioni, vedere [Aggiungere filtri e nidificazioni alle route di gestione degli errori](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md).

## Direttive sulla gestione degli errori

Le direttive sono brevemente illustrate qui di seguito. Per ulteriori informazioni, vedere [Direttive per la gestione degli errori](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

Esistono cinque direttive, che possono essere raggruppate nelle seguenti categorie in base al fatto che l’esecuzione di uno scenario continui dopo l’errore.

Le seguenti direttive garantiscono la prosecuzione dell’esecuzione di uno scenario:

* **[!UICONTROL Riprendi]**: consente di specificare un output sostitutivo per il modulo con l&#39;errore. Lo stato di esecuzione dello scenario è contrassegnato come completato.
* **[!UICONTROL Ignora]**: ignora l&#39;errore. Lo stato di esecuzione dello scenario è contrassegnato come completato.
* **[!UICONTROL Interruzione]**: memorizza l&#39;input nella coda di esecuzioni incomplete. Lo stato di esecuzione dello scenario è contrassegnato come avviso.

  Per ulteriori informazioni, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Se l’esecuzione di uno scenario deve interrompersi quando si verifica un errore, utilizza una delle seguenti direttive:

* **[!UICONTROL Rollback]**: interrompe immediatamente l&#39;esecuzione dello scenario e ne contrassegna lo stato come errore.
* **[!UICONTROL Commit]**: interrompe immediatamente l&#39;esecuzione dello scenario e ne contrassegna lo stato come completato.

## Risorse

Per ulteriori informazioni sulla gestione degli errori, vedere:

* [Direttive per la gestione degli errori in Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md)
* [Aggiungere filtri e nidificazione a percorsi di gestione degli errori](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)
