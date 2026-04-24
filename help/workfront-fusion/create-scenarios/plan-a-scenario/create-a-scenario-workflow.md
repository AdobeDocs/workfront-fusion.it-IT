---
title: Flusso di lavoro per creare uno scenario
description: Follow this general workflow to create a scenario
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 3%

---

# Flusso di lavoro per creare uno scenario

Scenarios are built to meet the needs of your organization, with applications and modules that address your use cases. However, creating a scenario follows the same basic workflow regardless of use case. This article describes the basic process of creating a scenario.


* [Create and name the scenario](#create-and-name-the-scenario)
* [Add and configure the first module](#configure-the-first-module)
* [Creare connessioni](#create-connections)
* [Add and configure additional modules](#add-and-configure-additional-modules)
* [Map data between modules](#map-data-between-modules)
* [Configure routing](#configure-routing)
* [Configurare la gestione degli errori](#configure-error-handling)
* [Configurare le impostazioni di uno scenario](#onfigure-scenario-settings)
* [Test and revise](#test-and-revise)
* [Activate the scenario](#activate-the-scenario)
* [Workfront Fusion scenario keyboard shortcuts](#workfront-fusion-scenario-keyboard-shortcuts)

Scelte rapide da tastiera



## Create and name the scenario

1. Sign into your Workfront Fusion account.
1. Fai clic su **[!UICONTROL Scenari]** ![Icona Scenari](assets/scenarios-icon.png) nel pannello a sinistra.

   >[!NOTE]
   >
   >If you do not see the left navigation panel or its icons, click the Menu ![Menu](assets/main-menu-icon-left-nav.png) icon.

1. (Optional)In the [!UICONTROL **Folders**] panel, click the **[!UICONTROL Add folder]** icon ![Add folder icon](assets/add-folder-icon.png), then type a name like &quot;Practice scenarios&quot; for your first folder.

1. (Optional) Open the folder, then click **[!UICONTROL Create a new scenario]** in the upper-right corner of the page.

1. Select the **[!UICONTROL New scenario]** placeholder name in the upper-left corner, then type a name such as &quot;Practice scenario 1.&quot;

   ![Name the scenario](assets/name-the-scenario.png)

1. Continue with [Connect the first module](#2-connect-the-first-module) below.

## Add and configure the first module

The first module for your scenario is a trigger module, which will start the scenario when certain conditions are met.

For instructions on adding the first module to a scenario, see [Add the first module to a scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) in the article Add a module to a scenario.

For instructions on configuring a module, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## Creare connessioni

Durante la configurazione di un modulo, devi immettere o creare una connessione. Il modulo utilizza questa connessione e le autorizzazioni in esso contenute per accedere alla data nell’applicazione.

Per istruzioni di base sulla creazione di una connessione, vedere [Creare una connessione - Istruzioni di base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

Per casi d&#39;uso specifici che coinvolgono Google, Microsoft o applicazioni senza connettori dedicati, vedere gli altri articoli in [Connetti alle applicazioni: indice articolo](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## Aggiungere e configurare moduli aggiuntivi

Continua ad aggiungere e configurare moduli aggiuntivi.

Per istruzioni su come aggiungere moduli, vedere gli articoli elencati in [Aggiungi moduli: indice articolo](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Mappare i dati tra i moduli

Puoi utilizzare l’output dei moduli precedenti come input nei moduli successivi. Ad esempio, puoi creare un progetto Workfront in un modulo e caricare un documento in tale modulo.

Per istruzioni, vedere gli articoli in [Dati mappa: indice articolo](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## Configurare l’indirizzamento

L’instradamento consente allo scenario di eseguire azioni diverse in base ai valori dei dati.

Per istruzioni, vedere [Aggiungere un modulo router e configurare le route](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Configurare la gestione degli errori

La gestione degli errori consente il recupero dello scenario dagli errori. È possibile selezionare la modalità di reazione dello scenario in diverse situazioni di errore.

Per istruzioni, vedere [Gestione degli errori](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).

## Configurare le impostazioni di uno scenario

Puoi configurare le impostazioni per lo scenario nel suo complesso, ad esempio pianificare uno scenario, creare note o determinare come vengono memorizzati i dati.

Per istruzioni, vedere gli articoli in [Configurare le impostazioni dello scenario: indice articolo](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Test e revisione

Il test dello scenario consente di determinare se funziona come previsto. È quindi possibile rivedere lo scenario in base ai risultati, quindi ripetere il test.

1. Fai clic su **[!UICONTROL Esegui una volta]** nell&#39;angolo inferiore sinistro dell&#39;editor scenari.
1. Al termine dell’esecuzione dello scenario, fai clic sulla bolla del controllo di esecuzione sopra ogni modulo per visualizzare l’input delle informazioni e l’output di quel modulo.

   * Per informazioni generali sulla lettura delle informazioni di esecuzione dello scenario, vedere [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Per informazioni sui bundle elaborati, vedere [Esecuzione di scenari, cicli e fasi in Adobe Workfront Fusion](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In Workfront Fusion, fai clic su **[!UICONTROL Salva]** ![Icona Salva](assets/save-icon.png) nell&#39;angolo in basso a sinistra per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Attiva lo scenario

Dopo aver attivato uno scenario, per impostazione predefinita viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza desideri che venga eseguita.

Per ulteriori informazioni sull&#39;attivazione degli scenari, vedere [Attivare o disattivare uno scenario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Per informazioni sulle pianificazioni, vedere [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Scelte rapide da tastiera per lo scenario Workfront Fusion

Durante la creazione o la modifica di uno scenario è possibile utilizzare le seguenti scelte rapide da tastiera:

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>Azione</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Salva] </td> 
   <td>Ctrl+Maiusc+S</td> 
   <td>Cmd+Maiusc+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Una Volta]</td> 
   <td>CTRL+MAIUSC+INVIO</td> 
   <td>Cmd+Maiusc+Invio</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Apri DevTool]</td> 
   <td>F12</td> 
   <td>CTRL+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona più moduli]</td> 
   <td>Maiusc+Trascina</td> 
   <td>Maiusc+Trascina</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>CTRL+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Incolla]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cerca moduli]</td> 
   <td>CTRL+K</td> 
   <td>Cmd+K</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Incolla cURL nello scenario per creare il modulo HTTP</td> 
   <td colspan="2">Copia cURL, quindi incolla ovunque nell’editor scenario.<p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md">Utilizzare cURL per aggiungere un modulo HTTP</a>.</td> 
  </tr> 
 </tbody> 
</table>





