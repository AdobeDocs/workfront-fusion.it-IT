---
content-type: reference
title: Configurare le impostazioni dello scenario
description: Puoi configurare impostazioni specifiche per gli scenari nel pannello delle impostazioni dello scenario.
author: Becky
feature: Workfront Fusion
exl-id: 105e3d39-b0ef-4c22-901d-fb4f29e685a9
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 0%

---

# Configurare le impostazioni dello scenario

Puoi configurare impostazioni specifiche per gli scenari nel pannello delle impostazioni dello scenario.

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

+++

## Apri le impostazioni dello scenario

1. Fai clic su **Scenari** nel pannello a sinistra.
1. Individua lo scenario desiderato, quindi fai clic sul nome.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor dello scenario.
1. Fai clic sull’icona a forma di ingranaggio nell’angolo inferiore sinistro della pagina.

   ![Impostazioni scenario](assets/scenario-settings-350x221.png)

   Nel pannello [!UICONTROL Impostazioni scenario] visualizzato, puoi configurare varie impostazioni avanzate per lo scenario.
1. Attiva o disattiva le impostazioni dello scenario in base alle esigenze. Consulta [Opzioni impostazioni scenario](#scenario-settings-options) di seguito.

## Opzioni impostazioni scenario

### [!UICONTROL Elaborazione sequenziale]

Questa opzione forza l’ordine delle esecuzioni ed è principalmente rilevante per i webhook e per le esecuzioni incomplete.

Quando l’elaborazione sequenziale è abilitata, le esecuzioni parallele dello scenario vengono disabilitate.

**Webhook istantanei**: se un trigger del webhook è configurato come `instant` e &quot;Elaborazione sequenziale&quot; è abilitata, tutti i payload del webhook istantaneo verranno messi in coda ed elaborati nell&#39;ordine in cui arrivano. Questo può essere utile quando si elaborano eventi da sistemi esterni in un ordine esatto.

>[!NOTE]
>
>Si verificheranno ritardi di elaborazione automatici quando ogni payload viene elaborato prima dell’avvio del successivo.

**Esecuzioni incomplete**: se è abilitata anche l&#39;opzione &quot;Esecuzioni incomplete&quot;, se si verifica un errore durante l&#39;esecuzione di uno scenario, lo scenario viene sospeso. Si verifica quindi una delle seguenti situazioni:

* Se l&#39;opzione di elaborazione sequenziale è **enabled**, Workfront Fusion interrompe l&#39;elaborazione della sequenza preesistente fino alla risoluzione di tutte le esecuzioni incomplete.
* Se l&#39;opzione di elaborazione sequenziale è **disabilitata**, lo scenario continua a essere eseguito in base alla pianificazione, accompagnata da ripetuti tentativi di eseguire nuovamente le esecuzioni incomplete.

  Per ulteriori informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

  >[!NOTE]
  >
  >L’elaborazione sequenziale può causare un ritardo nell’esecuzione di uno scenario. Se vi sono ancora esecuzioni incomplete nella coda quando si attiva uno scenario immediato o quando uno scenario pianificato è impostato per l’esecuzione, tale scenario verrà eseguito dopo che tutte le esecuzioni prima di essere nella coda sono state completate.
  >
  >Se il caso di utilizzo per gli scenari non richiede l’elaborazione sequenziale, si consiglia di disabilitare l’opzione di elaborazione sequenziale.

  Per ulteriori informazioni sulla pianificazione, vedere [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

### I dati sono riservati

Una volta eseguito uno scenario, per impostazione predefinita puoi visualizzare informazioni sui dati elaborati dai moduli nello scenario. Se non si desidera archiviare queste informazioni, abilitare l&#39;opzione [!UICONTROL Dati riservati].

>[!IMPORTANT]
>
>Se abiliti questa opzione, potrebbe essere difficile risolvere gli errori che possono verificarsi durante l’esecuzione di uno scenario.

### [!UICONTROL Consenti l&#39;archiviazione di esecuzioni incomplete]

Questa opzione determina il modo in cui Adobe Workfront Fusion procede se si verifica un errore durante l’esecuzione di uno scenario. Se questa opzione è abilitata, lo scenario viene messo in pausa e spostato nella cartella di esecuzione incompleta. Questo consente di risolvere il problema e continuare l’esecuzione dal punto in cui lo scenario è stato interrotto. Se questa opzione è disabilitata, l’esecuzione dello scenario si interrompe e viene avviata una fase di rollback.

Per ulteriori informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Abilita perdita di dati

Questa opzione ha a che fare con l’abilitazione della perdita di dati se Workfront Fusion non riesce a salvare un bundle nella coda di esecuzioni incomplete (ad esempio, a causa di una mancanza di spazio libero). Se questa opzione è abilitata, i dati vengono persi per evitare interruzioni nell’esecuzione complessiva dello scenario. Questo è utile per gli scenari in cui la priorità più alta è l’esecuzione continua e i dati errati in arrivo non sono così importanti.

Inoltre, durante l’esecuzione di uno scenario, a volte un modulo può incontrare un file di dimensioni superiori alla dimensione massima consentita. In questo caso, Workfront Fusion procede in conformità con l&#39;impostazione dell&#39;opzione [!UICONTROL Abilita perdita di dati] e viene visualizzato un messaggio di avviso.

Per ulteriori informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Per ulteriori informazioni sulle dimensioni massime dei file, vedere [Guardrail delle prestazioni di Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#files).

Per ulteriori informazioni sugli avvisi, vedere [Tipi di errore](/help/workfront-fusion/references/errors/error-processing.md).

### [!UICONTROL Commit automatico]

Le impostazioni di [!UICONTROL Auto commit] si applicano alle transazioni e definiscono la modalità di elaborazione di uno scenario. Se l&#39;opzione Auto commit è attiva, la fase di commit su ciascun modulo inizia immediatamente dopo il completamento della fase operativa. Se l&#39;opzione Auto commit è disattivata, non viene eseguito alcun commit finché non vengono eseguite operazioni per tutti i moduli (questa è la modalità predefinita).

### Numero massimo di cicli

>[!NOTE]
>
>Per visualizzare questa opzione è necessario abilitare la casella di controllo **Mostra impostazioni avanzate**.


L&#39;impostazione di più cicli può essere utile quando si desidera evitare l&#39;interruzione della connessione a un servizio di terze parti e assicurarsi che tutti i record vengano elaborati nell&#39;ambito dell&#39;esecuzione dello scenario.

* Se lo scenario inizia con un trigger di polling, l’impostazione definisce il numero massimo di cicli consentiti durante l’esecuzione dello scenario.

  Per ulteriori informazioni sui trigger di polling, vedere [Trigger di polling](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#polling-triggers) nell&#39;articolo Panoramica sui moduli.

* Se lo scenario inizia con un trigger immediato, l’impostazione viene ignorata e tutti gli eventi in sospeso vengono elaborati durante l’esecuzione di un singolo scenario, un evento per ogni ciclo.

  Per ulteriori informazioni sui trigger istantanei, vedere [Trigger istantanei](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) nell&#39;articolo Panoramica sui moduli.

* Se lo scenario non inizia con un trigger (istantaneo/polling), viene sempre eseguito il numero massimo specificato di cicli.

>[!BEGINSHADEBOX]

**Esempi:** Workfront > [!UICONTROL Osserva il record] verifica la presenza di nuovi problemi e Workfront >[!UICONTROL Converti oggetto] converte la nuova richiesta in un progetto e le assegna il modello appropriato.

![Impostazioni scenario](assets/scenario-settings-ex-1-350x157.png)

L&#39;impostazione [!UICONTROL altri cicli] viene applicata solo quando si pianifica l&#39;esecuzione dello scenario. Quando si utilizza il pulsante [!UICONTROL Esegui una volta], vengono prese in considerazione le impostazioni del ciclo.

#### Il numero massimo di cicli è impostato su 1 (impostazione predefinita)

![Numero massimo di cicli](assets/max-number-cycles-1-350x201.png)

Il numero massimo di cicli nel modulo Workfront > Osserva record è impostato su `10`.
Se vengono inviate 100 richieste a Workfront e il campo Numero massimo di cicli è impostato su 10, 90 file vengono lasciati non elaborati dopo l’esecuzione di uno scenario. I successivi 10 file vengono elaborati nella successiva esecuzione pianificata dello scenario.

#### Numero massimo di cicli impostato su 10

Il numero massimo di cicli nel modulo Workfront > Osserva record è impostato su `10`.

Se vengono aggiunti 100 file alla cartella Dropbox e l&#39;opzione Numero massimo di cicli è impostata su 10, vengono elaborati 10 file durante il primo ciclo, i successivi 10 file nel secondo ciclo, i successivi 10 file nel terzo ciclo e così via, fino a quando tutti i file non vengono elaborati.

Tutti i file vengono elaborati entro 1 esecuzione dello scenario.

Puoi visualizzare i cicli già eseguiti nei dettagli dello scenario:

![Dettagli scenario](assets/scenario-detail-350x207.png)

Per ulteriori informazioni su questa pagina, vedere [Dettagli scenario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md).

>[!ENDSHADEBOX]

### Numero di errori consecutivi

Definisce il numero massimo di tentativi di esecuzione consecutivi prima che l&#39;esecuzione di uno scenario venga disattivata (esclusi `DataError`, `DuplicateDataError`, `ModuleTimeoutError` e `ConnectionError`).

Per ulteriori informazioni sugli errori, vedere [Tipi di errore](/help/workfront-fusion/references/errors/error-processing.md).

>[!NOTE]
>
>Se uno scenario inizia con un trigger immediato, l’impostazione viene ignorata e lo scenario viene disattivato immediatamente dopo il primo errore.

### Pool di lavoro

>[!NOTE]
>
>Questa impostazione è visibile solo se sono soddisfatte le due condizioni seguenti:
>
>* Sei un amministratore o un proprietario dell’organizzazione
>* All&#39;organizzazione sono associati più gruppi di lavoro.

Questa impostazione assegna lo scenario a un pool di lavoratori specifico associato all&#39;organizzazione, consentendo di dedicare risorse a scenari ad alta priorità.
