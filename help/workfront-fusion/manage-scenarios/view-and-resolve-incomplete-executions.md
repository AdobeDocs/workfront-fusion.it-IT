---
title: Visualizzare e risolvere le esecuzioni incomplete
description: Nella cartella [!UICONTROL Esecuzioni incomplete] sono memorizzate esecuzioni dello scenario non finalizzate correttamente a causa di un errore. Ogni esecuzione incompleta archiviata può essere risolta manualmente o automaticamente.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: f2ddf62d660c4709f1e7e59c4302cde5b062725f
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 5%

---

# Visualizzare e risolvere le esecuzioni incomplete

Nella cartella [!UICONTROL Esecuzioni incomplete] sono memorizzate esecuzioni dello scenario non finalizzate correttamente a causa di un errore. Ogni esecuzione incompleta archiviata può essere risolta manualmente o automaticamente.

>[!NOTE]
>
>Per impostazione predefinita, la memorizzazione di esecuzioni incomplete è disabilitata. Per abilitarla, abilita l&#39;opzione [!UICONTROL Consenti l&#39;archiviazione di esecuzioni incomplete] nelle impostazioni avanzate dello scenario.
>
>Per ulteriori informazioni sulle impostazioni dello scenario, vedere [Configurare le impostazioni dello scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

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
   <p>Nuovo:</p> <ul><li>Piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront]: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>Il piano [!UICONTROL Ultimate] [!DNL Workfront]: [!DNL Workfront Fusion] è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per la tua organizzazione.</p>
     <p>Devi essere un amministratore [!DNL Workfront Fusion] per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visualizzare le esecuzioni incomplete

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
