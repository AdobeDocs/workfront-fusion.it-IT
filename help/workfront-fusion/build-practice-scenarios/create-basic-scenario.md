---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Creare uno scenario di base
description: Scopri come creare uno scenario di automazione semplice con Adobe Workfront Fusion. Gli scenari di automazione automatizzano i processi Workfront, inclusa la manipolazione e la trasformazione dei dati. In questo esempio viene illustrato il processo di creazione di uno scenario che cerca un'attività  [!DNL Workfront]  in Workfront e la converte in un progetto.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 1%

---

# Creare uno scenario di base

Il ruolo di [!DNL Adobe Workfront Fusion] consiste nell&#39;automatizzare i processi in modo da potersi concentrare su nuove attività anziché ripetere più volte le stesse attività. Funziona tramite il collegamento di azioni all’interno e tra app e servizi per creare uno scenario che trasferisce e trasforma automaticamente i dati. Lo scenario in cui si creano controlli i dati in un’app o in un servizio ed elabora tali dati in modo da fornire il risultato desiderato.

Questo esempio illustra come creare uno scenario che cerca una richiesta in Workfront e la converte in un progetto.

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



## Creare uno scenario di esercitazione

### Inizia a creare lo scenario

1. Nell&#39;area **Scenari**, fare clic su **Crea un nuovo scenario**.

   Per individuare l&#39;area Scenari, vedere [Navigare in Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   Viene visualizzato l’editor scenario, contenente un modulo vuoto al centro.

1. Seleziona il nome del segnaposto **[!UICONTROL New scenario]** nell&#39;angolo superiore sinistro, quindi immetti un nome.
1. Continua con [Aggiungi e configura il primo modulo](#add-and-configure-the-first-module).

### Aggiungere e configurare il primo modulo

1. Fai clic sul modulo vuoto per scegliere l’app dalla quale selezionare un modulo.

   A destra del modulo viene visualizzato un elenco di app.

1. Selezionare **[!DNL Adobe Workfront]**. Se non è visibile, fare clic sulla barra di ricerca nella parte inferiore dell&#39;elenco, digitare &quot;Workfront&quot; e selezionarla quando viene visualizzata nell&#39;elenco.

   L&#39;elenco viene modificato in modo da visualizzare tutti i moduli [!DNL Workfront] utilizzabili.

1. Fare clic sul modulo **[!UICONTROL Search]**.

   Viene visualizzata la finestra di configurazione del modulo.

1. Nella casella [!UICONTROL Connection] selezionare la connessione Workfront.

   Se non disponi di una connessione Workfront, vedi [Creare una connessione](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. Nella casella [!UICONTROL Record Type] selezionare **[!UICONTROL Issue]**. Questo imposta il modulo in modo che esegua la ricerca solo dei problemi, che includono le richieste.

   È possibile trovare **[!UICONTROL Issue]** nell&#39;elenco se si inizia a digitare la parola &quot;[!UICONTROL Issue]&quot;.

1. Nella casella **[!UICONTROL Result Set]** selezionare **[!UICONTROL First Matching Record]**.

   In questo modo il modulo restituirà solo il primo record che soddisfa i criteri.
1. Nell&#39;area **[!UICONTROL Search criteria]** configurare i criteri per restituire l&#39;attività specifica.

   1. Nella prima casella in [!UICONTROL Search Criteria] selezionare il campo che si desidera includere nella ricerca. Per questo esempio, selezionare **[!UICONTROL Name]**.

      È possibile trovare **[!UICONTROL Name]** nell&#39;elenco se si inizia a digitare la parola &quot;[!UICONTROL name]&quot;.
   1. Per l&#39;operatore, fare clic sulla freccia a discesa accanto a **Esiste** e modificarla in [!UICONTROL **Contiene (senza distinzione maiuscole/minuscole)**].

      Questo consente al modulo di trovare i progetti il cui nome contiene le parole scelte, anche se non si inserisce il nome completo o si inserisce il nome con lettere maiuscole non corrette.
   1. Nell&#39;ultimo campo in [!UICONTROL Search Criteria], immettere una parola o una frase che si sa essere nel nome dell&#39;attività che si sta cercando.

1. Nell&#39;elenco **[!UICONTROL Outputs]** selezionare i campi che si desidera vengano generati dal modulo. Per questo esempio, selezionare i campi **[!UICONTROL ID]** e **[!UICONTROL Name]**.

   >[!TIP]
   >
   >È possibile utilizzare **Cmd+F** ([!DNL Mac] OS) o **Ctrl-F** ([!DNL Windows] OS) per trovare rapidamente un campo.

1. Fare clic su **[!UICONTROL OK]** per salvare la configurazione del modulo.

1. Fare clic con il pulsante destro del mouse sul modulo, scegliere **[!UICONTROL Rename]**, quindi digitare un nome che descriva le operazioni che si desidera eseguire (ad esempio &quot;Ricerca richieste&quot;), quindi fare clic su **[!UICONTROL OK]**.

   Il nome viene visualizzato appena sotto il modulo. Di seguito, [!DNL Workfront Fusion] include una breve descrizione del tipo di azione eseguita dal modulo.

   ![Modulo rinominato](assets/module-renamed-wf.png)

1. Continua con [Aggiungi e configura il secondo modulo](#add-and-configure-the-second-module).

## Aggiungere e configurare il secondo modulo

1. Passa il puntatore del mouse sul cerchio parziale a destra della sezione del modulo, quindi fai clic su **[!UICONTROL Add another module]**.
1. Selezionare [!DNL Adobe Workfront] dall&#39;elenco delle applicazioni, quindi scegliere il modulo **[!UICONTROL Convert object]**.
1. Nel campo [!UICONTROL Connection] selezionare la stessa connessione Workfront utilizzata nel modulo precedente.
1. Nel campo **[!UICONTROL Record type]**, seleziona **[!UICONTROL issue]**, perché il modulo convertirà un problema.
1. Nel campo **[!UICONTROL Convert to]** selezionare **Progetto**.
1. Accanto al campo ID attività, fai clic sull’interruttore di mappatura per abilitarlo.

   L’interruttore diventa blu quando è attivato. Questo consente di mappare l’ID attività dal modulo precedente.

   ![Attiva/Disattiva mappa](assets/map-toggle.png)
1. Fare clic sul campo **[!UICONTROL Task ID]**.

   Viene visualizzato un pannello che consente di selezionare l’ID dell’attività da convertire in progetto. Poiché hai abilitato la mappatura, il pannello include l’output di tutti i moduli precedenti. Hai selezionato ID come output del modulo precedente, quindi ora è disponibile nel pannello.

   Questo pannello è denominato pannello di mappatura. Per ulteriori informazioni sul pannello di mappatura, vedi [Panoramica mappatura](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Seleziona **ID** nel pannello di mappatura.

   Nel campo ID viene visualizzato un blocco ID. Mostra il numero del modulo da cui è mappato e il campo mappato.

   ![ID mappa](assets/map-id.png)

1. Fare clic sul campo **ID modello**, iniziare a digitare il nome del modello di Workfront che si desidera utilizzare per il progetto, quindi selezionarlo quando viene visualizzato nell&#39;elenco.
1. Fare clic su **[!UICONTROL OK]** per salvare la configurazione del modulo.

1. Fare clic con il pulsante destro del mouse sul modulo, scegliere **[!UICONTROL Rename]**, quindi digitare un nome che descriva le operazioni che si desidera eseguire (ad esempio &quot;Converti in progetto&quot;), quindi fare clic su **[!UICONTROL OK]**.

1. Continua a [Verificare lo scenario](#test-the-scenario).

## Verifica lo scenario

Prima di attivare lo scenario, è importante testarlo eseguendolo almeno una volta e visualizzando i risultati. Questo ti aiuta a capire come i dati scorrono attraverso lo scenario e a trovare eventuali errori.

In questo caso, se il test ha esito positivo, la richiesta viene individuata e convertita in un progetto.

1. Fare clic su **[!UICONTROL Run once]** nell&#39;angolo inferiore sinistro dell&#39;editor di scenari.
1. Al termine dell’esecuzione dello scenario, fai clic sul fumetto sopra il primo modulo per visualizzare informazioni sul bundle di dati elaborato dal modulo, inclusi i dati estratti dalla richiesta restituita dal modulo.

1. Fai clic sul fumetto del controllo dell’esecuzione sopra il secondo modulo per visualizzare l’input (la richiesta) e l’output (il progetto convertito).

   Per ulteriori informazioni sui dati contenuti nelle bolle di ispezione, vedere:

   * Per informazioni generali, vedere [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Per informazioni sui bundle elaborati, vedere [Esecuzione scenario, cicli e fasi](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In [!DNL Workfront Fusion], fai clic su **[!UICONTROL Save]** nell&#39;angolo in basso a sinistra per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

>[!TIP]
>
>È consigliabile aggiungere note su ciascun modulo in modo facoltativo ma utile.
>
>1. Fare clic con il pulsante destro del mouse su un modulo, quindi selezionare **[!UICONTROL Add a note]**.
>1. Nella nota visualizzata, digita una panoramica del modulo.
>
>    È possibile aggiungere più note per un modulo.
>
>1. Chiudere l&#39;area **[!UICONTROL Notes]**.
>
>     Dopo aver aggiunto una nota a uno scenario, un punto arancione viene visualizzato sull&#39;icona **[!UICONTROL Notes]** ![Note con punto](assets/notes-icon-w-dot.png) nella parte inferiore dell&#39;editor dello scenario.
>
>1. Fai clic sull&#39;icona **[!UICONTROL Notes]** ![Icona Note con punto](assets/notes-icon-w-dot.png) per visualizzare le note.
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
