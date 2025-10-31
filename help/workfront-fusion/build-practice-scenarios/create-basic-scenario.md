---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Creare uno scenario di base
description: Scopri come creare uno scenario di automazione semplice con Adobe Workfront Fusion. Gli scenari di automazione automatizzano i processi Workfront, inclusa la manipolazione e la trasformazione dei dati. In questo esempio viene illustrato il processo di creazione di uno scenario che cerca un'attività di Workfront in Workfront e la converte in un progetto.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Creare uno scenario di base

Il ruolo di Adobe Workfront Fusion è quello di automatizzare i processi in modo da potersi concentrare su nuove attività anziché ripetere più volte le stesse attività. Funziona tramite il collegamento di azioni all’interno e tra app e servizi per creare uno scenario che trasferisce e trasforma automaticamente i dati. Lo scenario in cui si creano controlli i dati in un’app o in un servizio ed elabora tali dati in modo da fornire il risultato desiderato.

Questo esempio illustra come creare uno scenario che cerca una richiesta in Workfront e la converte in un progetto.

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

## Creare uno scenario di esercitazione

### Inizia a creare lo scenario

1. Nell&#39;area **Scenari**, fare clic su **Crea un nuovo scenario**.

   Per individuare l&#39;area Scenari, vedere [Navigare in Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   Viene visualizzato l’editor scenario, contenente un modulo vuoto al centro.

1. Seleziona il nome del segnaposto **[!UICONTROL Nuovo scenario]** nell&#39;angolo superiore sinistro, quindi immetti un nome.
1. Continua con [Aggiungi e configura il primo modulo](#add-and-configure-the-first-module).

### Aggiungere e configurare il primo modulo

1. Fai clic sul modulo vuoto per scegliere l’app dalla quale selezionare un modulo.

   A destra del modulo viene visualizzato un elenco di app.

1. Seleziona **Adobe Workfront**. Se non è visibile, fare clic sulla barra di ricerca nella parte inferiore dell&#39;elenco, digitare &quot;Workfront&quot; e selezionarla quando viene visualizzata nell&#39;elenco.

   L’elenco viene modificato in modo da visualizzare tutti i moduli Workfront utilizzabili.

1. Fare clic sul modulo **[!UICONTROL Cerca]**.

   Viene visualizzata la finestra di configurazione del modulo.

1. Nella casella [!UICONTROL Connessione], seleziona la tua connessione Workfront.

   Se non disponi di una connessione Workfront, vedi [Creare una connessione](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. Nella casella [!UICONTROL Tipo di record], seleziona **[!UICONTROL Problema]**. Questo imposta il modulo in modo che esegua la ricerca solo dei problemi, che includono le richieste.

   Puoi trovare **[!UICONTROL Problema]** nell&#39;elenco se inizi a digitare la parola &quot;[!UICONTROL Problema].&quot;

1. Nella casella **[!UICONTROL Set di risultati]** selezionare **[!UICONTROL Primo record corrispondente]**.

   In questo modo il modulo restituirà solo il primo record che soddisfa i criteri.
1. Nell&#39;area **[!UICONTROL Criteri di ricerca]** configurare i criteri per restituire l&#39;attività specifica.

   1. Nella prima casella in [!UICONTROL Criteri di ricerca], selezionare il campo che si desidera includere nella ricerca. Per questo esempio, selezionare **[!UICONTROL Nome]**.

      Puoi trovare **[!UICONTROL Name]** nell&#39;elenco se inizi a digitare la parola &quot;[!UICONTROL name].&quot;
   1. Per l&#39;operatore, fare clic sulla freccia a discesa accanto a **Esiste** e modificarla in [!UICONTROL **Contiene (senza distinzione maiuscole/minuscole)**].

      Questo consente al modulo di trovare i progetti il cui nome contiene le parole scelte, anche se non si inserisce il nome completo o si inserisce il nome con lettere maiuscole non corrette.
   1. Nell&#39;ultimo campo in [!UICONTROL Criteri di ricerca], immettere una parola o una frase che si sa essere nel nome dell&#39;attività che si sta cercando.

1. Nell&#39;elenco **[!UICONTROL Output]** selezionare i campi che si desidera vengano generati dal modulo. Per questo esempio, selezionare i campi **[!UICONTROL ID]** e **[!UICONTROL Nome]**.

   >[!TIP]
   >
   >È possibile utilizzare **Cmd+F** ([!DNL Mac] OS) o **Ctrl-F** ([!DNL Windows] OS) per trovare rapidamente un campo.

1. Fare clic su **[!UICONTROL OK]** per salvare la configurazione del modulo.

1. Fare clic con il pulsante destro del mouse sul modulo, scegliere **[!UICONTROL Rinomina]**, quindi digitare un nome che descriva le operazioni che si desidera eseguire (ad esempio &quot;Cerca richieste&quot;), quindi fare clic su **[!UICONTROL OK]**.

   Il nome viene visualizzato appena sotto il modulo. Di seguito è riportata una breve descrizione del tipo di azione eseguita dal modulo in Workfront Fusion.

   ![Modulo rinominato](assets/module-renamed-wf.png)

1. Continua con [Aggiungi e configura il secondo modulo](#add-and-configure-the-second-module).

## Aggiungere e configurare il secondo modulo

1. Passa il puntatore del mouse sul cerchio parziale a destra della sezione del modulo, quindi fai clic su **[!UICONTROL Aggiungi un altro modulo]**.
1. Selezionare Adobe Workfront dall&#39;elenco delle applicazioni, quindi scegliere il modulo **[!UICONTROL Converti oggetto]**.
1. Nel campo [!UICONTROL Connessione], seleziona la stessa connessione Workfront utilizzata nel modulo precedente.
1. Nel campo **[!UICONTROL Tipo di record]**, seleziona **[!UICONTROL problema]**, perché il modulo convertirà un problema.
1. Nel campo **[!UICONTROL Converti in]**, selezionare **Progetto**.
1. Accanto al campo ID attività, fai clic sull’interruttore di mappatura per abilitarlo.

   L’interruttore diventa blu quando è attivato. Questo consente di mappare l’ID attività dal modulo precedente.

   ![Attiva/Disattiva mappa](assets/map-toggle.png)
1. Fare clic sul campo **[!UICONTROL ID attività]**.

   Viene visualizzato un pannello che consente di selezionare l’ID dell’attività da convertire in progetto. Poiché hai abilitato la mappatura, il pannello include l’output di tutti i moduli precedenti. Hai selezionato ID come output del modulo precedente, quindi ora è disponibile nel pannello.

   Questo pannello è denominato pannello di mappatura. Per ulteriori informazioni sul pannello di mappatura, vedi [Panoramica mappatura](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Seleziona **ID** nel pannello di mappatura.

   Nel campo ID viene visualizzato un blocco ID. Mostra il numero del modulo da cui è mappato e il campo mappato.

   ![ID mappa](assets/map-id.png)

1. Fare clic sul campo **ID modello**, iniziare a digitare il nome del modello di Workfront che si desidera utilizzare per il progetto, quindi selezionarlo quando viene visualizzato nell&#39;elenco.
1. Fare clic su **[!UICONTROL OK]** per salvare la configurazione del modulo.

1. Fare clic con il pulsante destro del mouse sul modulo, scegliere **[!UICONTROL Rinomina]**, quindi digitare un nome che descriva le operazioni che si desidera eseguire (ad esempio &quot;Converti in progetto&quot;), quindi fare clic su **[!UICONTROL OK]**.

1. Continua a [Verificare lo scenario](#test-the-scenario).

## Verifica lo scenario

Prima di attivare lo scenario, è importante testarlo eseguendolo almeno una volta e visualizzando i risultati. Questo ti aiuta a capire come i dati scorrono attraverso lo scenario e a trovare eventuali errori.

In questo caso, se il test ha esito positivo, la richiesta viene individuata e convertita in un progetto.

1. Fai clic su **[!UICONTROL Esegui una volta]** nell&#39;angolo inferiore sinistro dell&#39;editor scenari.
1. Al termine dell’esecuzione dello scenario, fai clic sul fumetto sopra il primo modulo per visualizzare informazioni sul bundle di dati elaborato dal modulo, inclusi i dati estratti dalla richiesta restituita dal modulo.

1. Fai clic sul fumetto del controllo dell’esecuzione sopra il secondo modulo per visualizzare l’input (la richiesta) e l’output (il progetto convertito).

   Per ulteriori informazioni sui dati contenuti nelle bolle di ispezione, vedere:

   * Per informazioni generali, vedere [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Per informazioni sui bundle elaborati, vedere [Esecuzione scenario, cicli e fasi](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In Workfront Fusion, fai clic su **[!UICONTROL Salva]** nell&#39;angolo inferiore sinistro per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

>[!TIP]
>
>È consigliabile aggiungere note su ciascun modulo in modo facoltativo ma utile.
>
>1. Fai clic con il pulsante destro del mouse su un modulo, quindi seleziona **[!UICONTROL Aggiungi una nota]**.
>1. Nella nota visualizzata, digita una panoramica del modulo.
>
>    È possibile aggiungere più note per un modulo.
>
>1. Chiudi l&#39;area **[!UICONTROL Note]**.
>
>     Dopo aver aggiunto una nota a uno scenario, un punto viene visualizzato sull&#39;icona **[!UICONTROL Note]** ![Note con punto](assets/notes-icon-w-dot.png) nella parte inferiore dell&#39;editor dello scenario.
>
>1. Fai clic sull&#39;icona **[!UICONTROL Note]** ![Note con punto](assets/notes-icon-w-dot.png) per visualizzare le note. Quando le note sono aperte, viene visualizzato un cerchio attorno all&#39;icona Note.
>

## Attiva lo scenario

L’ultimo passaggio nella creazione di uno scenario è quello di attivarlo.

Poiché questo scenario è alla ricerca di un problema specifico, non è necessario attivarlo. L’attivazione di uno scenario ne determina l’esecuzione secondo una pianificazione o quando si verifica un’azione specifica in un’applicazione. Dopo aver attivato uno scenario, per impostazione predefinita viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza desideri che venga eseguita.

Per ulteriori informazioni sull&#39;attivazione degli scenari, vedere [Attivare o disattivare uno scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Per informazioni sulle pianificazioni, vedere [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Passaggi successivi

* [Aggiungi un modulo trigger](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) per consentire allo scenario di cercare periodicamente nuove richieste e convertirle in progetti.
* [Aggiungi un webhook](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) per consentire l&#39;esecuzione dello scenario ogni volta che viene immessa una richiesta.
* [Aggiungi un filtro](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) per garantire che solo alcune richieste vengano convertite in progetti.
* [Aggiungi una funzione](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) che personalizza il nome del nuovo progetto.
