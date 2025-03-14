---
title: Configura soluzione alternativa per la gestione degli errori dei tentativi
description: A volte è utile rieseguire un modulo non riuscito se è possibile che il motivo dell’errore si risolva rapidamente.
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Configura soluzione alternativa per la gestione degli errori `retry`

A volte è utile rieseguire un modulo non riuscito se è possibile che il motivo dell’errore si risolva rapidamente.

Adobe Workfront Fusion attualmente non offre la direttiva per la gestione degli errori `retry`, ma sono disponibili due soluzioni alternative per simulare la funzionalità `retry`.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Selezionare o Prime Workfront Plan: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Ultimate Workfront: Workfront Fusion è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Soluzioni per la direttiva di gestione degli errori [!UICONTROL Riprova]

Workfront Fusion attualmente non offre la direttiva di gestione degli errori `retry`. Utilizza una delle seguenti soluzioni per simulare la funzionalità dei nuovi tentativi.

Per istruzioni, vedere [Direttive per la gestione degli errori](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

* [Utilizzare la direttiva Break](#use-the-break-directive)
* [Utilizzare il modulo Repeater (Ripetitore)](#use-the-repeater-module)

### Utilizzare la direttiva Break

Quando viene eseguita la direttiva Break, lo stato di esecuzione dello scenario viene memorizzato nella coda di esecuzioni incomplete. In questo caso, puoi risolvere manualmente l’esecuzione incompleta.

Per istruzioni, vedere [Risolvere gli errori gestiti dalla direttiva Interrompi](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)

Per istruzioni sulla risoluzione delle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

#### Svantaggi

* L&#39;intervallo minimo tra i tentativi è di un minuto.
* Se il modulo elabora più bundle e l&#39;elaborazione di un bundle non riesce, l&#39;esecuzione parziale (solo il bundle che ha causato l&#39;errore) viene spostata nella cartella esecuzioni incomplete e pianificata per i nuovi tentativi in base alle impostazioni della direttiva [!UICONTROL Break]. Tuttavia, l’esecuzione corrente continua e il modulo continua a elaborare i bundle successivi.

  Per impedire che lo scenario venga eseguito nuovamente finché l&#39;esecuzione archiviata nella cartella Esecuzioni incomplete non è stata risolta correttamente, abilitare l&#39;opzione &quot;[!UICONTROL Elaborazione sequenziale]&quot; nelle [!UICONTROL Impostazioni scenario].

Per ulteriori informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Utilizzare il modulo Repeater (Ripetitore)

La soluzione alternativa del modulo Repeater è più complessa, ma più personalizzabile.

#### Configurare la route del gestore degli errori

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera aggiungere la soluzione alternativa.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fare clic sull&#39;icona **Controllo flusso** ![Controllo flusso](assets/flow-control-icon.png) e selezionare **Ripetitore**.
1. Nel modulo Repeater (Ripetitore), impostare il campo **[!UICONTROL Repeats]** sul numero massimo di tentativi che si desidera vengano ripetuti dallo scenario.
1. Allega il modulo che potrebbe generare errori dopo il modulo **[!UICONTROL Repeater]**.
1. Collegare una route del gestore degli errori al modulo che potrebbe non riuscire.

   Per istruzioni, vedere [Gestione degli errori](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).
1. Aggiungi il modulo **[!UICONTROL Strumenti] > [!UICONTROL Sospendi]** alla route del gestore errori e imposta il campo **[!UICONTROL Ritarda]** sul numero di secondi tra un tentativo e l&#39;altro.

1. Aggiungi la direttiva **[!UICONTROL Ignora]** dopo il modulo **[!UICONTROL Strumenti] > [!UICONTROL Sospendi]**.
1. Continua con [Configurare la route predefinita](#configure-the-default-route).

#### Configurare la route predefinita

1. Aggiungere il modulo **[!UICONTROL Strumenti] > [!UICONTROL Imposta variabile]** in una route separata (gestore non di errore) dopo il modulo che potrebbe generare un errore e configurarlo per memorizzare il risultato del modulo in una variabile denominata, ad esempio `Result`.

1. Aggiungere il modulo **[!UICONTROL Array aggregator]** dopo **[!UICONTROL Tools] > [!UICONTROL Set variable]** e selezionare il modulo **[!DNL Repeater]** nel relativo campo Source Module.

1. Aggiungere il modulo **[!UICONTROL Strumenti] > [!UICONTROL Ottieni variabile]** dopo il modulo **[!UICONTROL Array aggregator]** e mappare il valore della variabile `Result` su di esso.

1. Inserire il modulo **[!UICONTROL Tools] > [!UICONTROL Get variable]** tra il modulo **[!UICONTROL Repeater]** e il modulo che potrebbe non riuscire e mappare il valore della variabile `Result` su di esso.

1. Inserire un filtro tra il modulo **[!UICONTROL Tools] > [!UICONTROL Get variable]** e il modulo che potrebbe non riuscire per continuare solo se la variabile `Result` non esiste.

>[!BEGINSHADEBOX]

**Esempio:**

In questo scenario di esempio, il modulo [!UICONTROL HTTP] > [!UICONTROL Effettua una richiesta] rappresenta il modulo che potrebbe non riuscire:

![HTTP Fai una richiesta](assets/http-make-request.png)

>[!ENDSHADEBOX]

Se il risultato del modulo con potenziale errore è troppo complesso per essere memorizzato in una variabile semplice, puoi utilizzare un archivio dati per memorizzare e recuperare il risultato. L’archivio dati conterrebbe un solo record. La chiave del record può essere ad esempio `Result`.

Per ulteriori informazioni sugli archivi dati, vedere [Archivi dati](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

#### Svantaggi

* Questa soluzione alternativa è più complessa.
* Questa soluzione alternativa utilizza più operazioni.

## Risorse

* Per ulteriori informazioni sui moduli Repeater e sulle direttive di interruzione, vedere [Controllo di flusso](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md).
* Per ulteriori informazioni sui moduli Get Variable, vedere [Strumenti](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md).
