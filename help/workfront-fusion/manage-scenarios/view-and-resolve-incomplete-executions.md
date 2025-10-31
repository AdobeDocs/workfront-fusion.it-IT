---
title: Visualizzare e risolvere le esecuzioni incomplete
description: Nella cartella [!UICONTROL Esecuzioni incomplete] sono memorizzate esecuzioni dello scenario non finalizzate correttamente a causa di un errore. Ogni esecuzione incompleta archiviata può essere risolta manualmente o automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 5%

---

# Visualizzare e risolvere le esecuzioni incomplete

Nella cartella [!UICONTROL Esecuzioni incomplete] sono memorizzate esecuzioni dello scenario non finalizzate correttamente a causa di un errore. Ogni esecuzione incompleta archiviata può essere risolta manualmente o automaticamente.

>[!NOTE]
>
>Per impostazione predefinita, la memorizzazione di esecuzioni incomplete è disabilitata. Per abilitarla, abilita l&#39;opzione [!UICONTROL Consenti l&#39;archiviazione di esecuzioni incomplete] nelle impostazioni avanzate dello scenario.
>
>Per ulteriori informazioni sulle impostazioni dello scenario, vedere [Configurare le impostazioni dello scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Anteprima evidenziata per l&#39;articolo completo {#highlighted-preview-article-level}

<span class="preview">Le informazioni contenute in questa pagina si riferiscono a funzionalità non ancora generalmente disponibili. È disponibile solo nell’ambiente Sandbox di anteprima.</span>## Visualizza esecuzioni incomplete

Se un modulo rileva un errore durante l’operazione, viene aggiunta una nuova esecuzione incompleta alla cartella Esecuzioni incomplete. Ogni esecuzione incompleta contiene il blueprint dello scenario e tutti i bundle che possono essere mappati nel modulo non riuscito. Per aprire l&#39;elenco delle esecuzioni incomplete, fare clic sulla scheda [!UICONTROL Esecuzioni incomplete] nella pagina dei dettagli dello scenario.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

Per ulteriori informazioni, vedere [Errori risultanti in esecuzioni incomplete](#errors-resulting-into-incomplete-executions) in questo articolo.

>[!NOTE]
>
>Il limite di dimensione corrente della cartella esecuzioni incomplete non risolte per ogni scenario è di 10 MB. Se lo scenario supera questo limite, è possibile che venga visualizzato il seguente errore:
>
>`DLQ limit per scenario has been exceeded`
>
>I team sono limitati a un totale di 500 MB per tutte le esecuzioni incomplete non risolte.
>
>Per ulteriori informazioni, vedere [Abilitare la perdita di dati](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) nell&#39;articolo Configurare le impostazioni dello scenario.


## Risolvere le esecuzioni incomplete dalla scheda Esecuzioni incomplete

Quando viene memorizzata una nuova esecuzione incompleta, è possibile risolverla come segue:

1. Apri lo scenario interessato.
1. Fare clic sulla scheda **[!UICONTROL Esecuzioni incomplete]**.
1. Individuare l&#39;esecuzione incompleta da risolvere e fare clic su **[!UICONTROL Dettagli]**.
1. Apri il registro del modulo in cui vengono visualizzate tutte le operazioni del modulo.
1. Individuare l&#39;operazione non riuscita e fare clic su **[!UICONTROL Risolvi]**:

   ![Pulsante Risolvi](assets/resolve-btn-350x188.png)



## Risolvere le esecuzioni incomplete dalla scheda Cronologia

Se si desidera visualizzare il registro di tutte le operazioni del modulo prima di tentare di risolvere l&#39;esecuzione incompleta, è possibile risolverla dalla cartella [!UICONTROL Cronologia]:

1. Apri lo scenario interessato.
1. Fare clic sulla scheda **[!UICONTROL Cronologia]**.
1. Individuare l&#39;esecuzione non riuscita dello scenario e fare clic su **[!UICONTROL Dettagli]**.
1. Apri il registro del modulo in cui vengono visualizzate tutte le operazioni del modulo.
1. Individuare l&#39;operazione non riuscita e fare clic su **[!UICONTROL Risolvi]**:

   ![Pulsante Risolvi](assets/resolve-btn-350x188.png)

## Opzioni relative alle esecuzioni incomplete

Le seguenti opzioni nel pannello [!UICONTROL Impostazioni scenario] determinano se e come vengono archiviate le esecuzioni incomplete:

* Consenti l’archiviazione di esecuzioni incomplete
* Elaborazione sequenziale
* Abilita perdita di dati

Per ulteriori informazioni su queste opzioni, vedere [Configurare le impostazioni dello scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Errori risultanti in esecuzioni incomplete

Esistono diverse categorie di errori che si traducono nella memorizzazione di esecuzioni incomplete. Questi possono includere:

* Errori di convalida derivanti da dati incompleti o errati, principalmente a causa di un elemento mancante previsto per elaborare correttamente tutti i dati che passano attraverso un modulo.
* Errori che si verificano dall’indisponibilità della destinazione finale a causa di un errore di connessione temporaneo o a lungo termine (ad esempio, durante la connessione a un server e-mail o FTP remoto).

Se si verifica un errore nel primo modulo dello scenario, l’esecuzione viene subito interrotta e non viene memorizzata alcuna esecuzione incompleta.

Se si verifica un errore in un altro modulo e non è collegata alcuna route del gestore degli errori, si verifica una delle seguenti situazioni:

* È stato memorizzato un record di esecuzione incompleto con un nuovo tentativo automatico per i seguenti tipi di errore:

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* È stato memorizzato un record di esecuzione incompleto senza tentativi automatici per i seguenti tipi di errore:

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* Se il tipo di errore è diverso da quelli riportati sopra, l’esecuzione non riesce.
