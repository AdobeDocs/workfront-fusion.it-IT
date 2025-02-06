---
title: Flusso di lavoro per la creazione di uno scenario
description: Segui questo flusso di lavoro generale per creare uno scenario
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: 394f80a2d7c124bbd00e1a5b51ad3dc6e73a996b
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Flusso di lavoro per la creazione di uno scenario

Gli scenari sono progettati per soddisfare le esigenze della tua organizzazione, con applicazioni e moduli che soddisfano i tuoi casi d’uso. Tuttavia, la creazione di uno scenario segue lo stesso flusso di lavoro di base indipendentemente dal caso d’uso. Questo articolo descrive il processo di base per la creazione di uno scenario.


* [Creare e denominare lo scenario](#create-and-name-the-scenario)
* [Aggiungere e configurare il primo modulo](#configure-the-first-module)
* [Creare connessioni](#create-connections)
* [Aggiungere e configurare moduli aggiuntivi](#add-and-configure-additional-modules)
* [Mappare i dati tra i moduli](#map-data-between-modules)
* [Configurare l’indirizzamento](#configure-routing)
* [Configurare la gestione degli errori](#configure-error-handling)
* [Configurare le impostazioni dello scenario](#onfigure-scenario-settings)
* [Test e revisione](#test-and-revise)
* [Attiva lo scenario](#activate-the-scenario)
* [Scelte rapide da tastiera per lo scenario Workfront Fusion](#workfront-fusion-scenario-keyboard-shortcuts)

Scelte rapide da tastiera



## Creare e denominare lo scenario

1. Accedi al tuo account [!DNL Workfront Fusion].
1. Fai clic su **[!UICONTROL Scenarios]** ![Icona Scenari](assets/scenarios-icon.png) nel pannello a sinistra.

   >[!NOTE]
   >
   >Se il pannello di navigazione a sinistra o le relative icone non sono visibili, fare clic sull&#39;icona Menu ![Menu](assets/main-menu-icon-left-nav.png).

1. (Facoltativo)Nel pannello [!UICONTROL **Cartelle**], fai clic sull&#39;icona **[!UICONTROL Add folder]** ![Icona Aggiungi cartella](assets/add-folder-icon.png), quindi digita un nome come &quot;Scenari di esercitazione&quot; per la prima cartella.

1. (Facoltativo) Aprire la cartella, quindi fare clic su **[!UICONTROL Create a new scenario]** nell&#39;angolo superiore destro della pagina.

1. Selezionare il nome del segnaposto **[!UICONTROL New scenario]** nell&#39;angolo superiore sinistro, quindi digitare un nome come &quot;Esercitazione scenario 1&quot;.

   ![Assegna un nome allo scenario](assets/name-the-scenario.png)

1. Continua con [Connetti il primo modulo](#2-connect-the-first-module) di seguito.

## Aggiungere e configurare il primo modulo

Il primo modulo per lo scenario è un modulo trigger, che avvierà lo scenario quando vengono soddisfatte determinate condizioni.

Per istruzioni sull&#39;aggiunta del primo modulo a uno scenario, vedere [Aggiungere il primo modulo a uno scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) nell&#39;articolo Aggiungere un modulo a uno scenario.

Per istruzioni sulla configurazione di un modulo, vedere [Configurare un modulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

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

## Configurare le impostazioni dello scenario

Puoi configurare le impostazioni per lo scenario nel suo complesso, ad esempio pianificare uno scenario, creare note o determinare come vengono memorizzati i dati.

Per istruzioni, vedere gli articoli in [Configurare le impostazioni dello scenario: indice articolo](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Test e revisione

Il test dello scenario consente di determinare se funziona come previsto. È quindi possibile rivedere lo scenario in base ai risultati, quindi ripetere il test.

1. Fare clic su **[!UICONTROL Run once]** nell&#39;angolo inferiore sinistro dell&#39;editor di scenari.
1. Al termine dell’esecuzione dello scenario, fai clic sulla bolla del controllo di esecuzione sopra ogni modulo per visualizzare l’input delle informazioni e l’output di quel modulo.

   * Per informazioni generali sulla lettura delle informazioni di esecuzione dello scenario, vedere [Flusso di esecuzione dello scenario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Per informazioni sui bundle elaborati, vedere [Esecuzione scenario, cicli e fasi in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In [!DNL Workfront Fusion], fai clic sull&#39;icona **[!UICONTROL Save]** ![Salva](assets/save-icon.png) nell&#39;angolo inferiore sinistro per salvare l&#39;avanzamento dello scenario.

   >[!IMPORTANT]
   >
   >Risparmia spesso quando affili e testa uno scenario.

## Attiva lo scenario

Questo scenario di esempio non ha un modulo trigger. Se si trattasse di uno scenario da utilizzare per dati reali, inizierebbe con un modulo trigger e l’ultima cosa da fare è attivarlo. Dopo aver attivato uno scenario, per impostazione predefinita viene eseguito ogni 15 minuti. Puoi modificare questa impostazione definendo quando e con quale frequenza desideri che venga eseguita.

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
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Ctrl+Maiusc+S</td> 
   <td>Cmd+Maiusc+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>CTRL+MAIUSC+INVIO</td> 
   <td>Cmd+Maiusc+Invio</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Open the DevTool]</td> 
   <td>F12</td> 
   <td>CTRL+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select multiple modules]</td> 
   <td>Maiusc+Trascina</td> 
   <td>Maiusc+Trascina</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>CTRL+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paste]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Incolla cURL nello scenario per creare il modulo HTTP</td> 
   <td colspan="2">Copia cURL, quindi incolla ovunque nell’editor scenario.<p>Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md">Utilizzare cURL per aggiungere un modulo HTTP</a>.</td> 
  </tr> 
 </tbody> 
</table>





