---
title: Creare nuovi modelli
description: È possibile creare nuovi modelli di scenario in [!DNL Adobe] Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---

# Creare nuovi modelli

È possibile creare nuovi modelli di scenario in [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Prima di creare un nuovo modello, è possibile controllare la scheda [!UICONTROL Modelli pubblici] per assicurarsi che il modello che si desidera creare non sia già disponibile.

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

## Crea un nuovo modello

È possibile creare un modello in un processo simile alla creazione di uno scenario. Gli amministratori di Fusion possono anche creare modelli da scenari esistenti.

* [Creare un modello](#build-a-template)
* [Creare un modello da uno scenario](#create-a-template-from-a-scenario)

### Creare un modello

1. Fai clic sull&#39;icona **[!UICONTROL Modelli]** ![Modelli](assets/templates-icon.png) nel pannello di navigazione a sinistra.
1. Fai clic su **[!UICONTROL Crea un nuovo modello]** nell&#39;angolo superiore destro.
1. (Facoltativo) Rinominare il modello sostituendo il **[!UICONTROL Nome nuovo modello]** predefinito nell&#39;angolo superiore sinistro.
1. (Facoltativo) Per modificare la lingua del modello, fare clic su **[!UICONTROL Imposta modello]** ![icona Impostazioni scenario](assets/scenario-settings-icon.png) e selezionare la lingua dal menu a discesa Lingua.

   >[!IMPORTANT]
   >
   >La selezione Lingue corrisponde alle lingue disponibili nelle impostazioni di sistema e riguarda solo il nome del modello pubblico e la relativa descrizione. Una volta salvato il modello, non è possibile modificare il linguaggio del modello.

1. (Facoltativo) Per immettere una descrizione del modello, fare clic su **[!UICONTROL Configura modello]** ![Icona impostazioni scenario](assets/scenario-settings-icon.png) e immettere la descrizione.
1. Aggiungi app, moduli e strumenti, utilizzando gli stessi processi utilizzati per aggiungere moduli a uno scenario.

   Per istruzioni, vedere gli articoli in [Aggiungi moduli](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Per aggiungere informazioni contestuali ai moduli, vedere [Configurare la funzionalità della procedura guidata](#set-up-wizard-functionality) in questo articolo.

   Per ulteriori informazioni sulla creazione di uno scenario, vedere [Flusso di lavoro per la creazione di uno scenario](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Se il modello include moduli che richiedono l’aggiunta di connessione, credenziali o altre informazioni riservate, queste informazioni non vengono condivise con gli utenti del modello.

1. (Facoltativo) Fai clic su **[!UICONTROL Esegui una volta]** per verificare il modello.
1. Fai clic sull&#39;icona **[!UICONTROL Salva]** ![Salva icona](assets/save-icon.png) per salvare il modello.

Quando salvi il modello, questo diventa visibile ai membri del gruppo. Se desideri che il modello sia accessibile all’esterno del team, devi inviare una richiesta per far sì che sia approvato e pubblicato. La richiesta viene inviata al team di Adobe Workfront Fusion per l’approvazione. Dopo l’approvazione, il modello è accessibile ad altri utenti esterni al team.

Per informazioni sulla pubblicazione dei modelli, vedere [Pubblicare e condividere modelli di Adobe Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Creare un modello da uno scenario

>[!NOTE]
>
>Per creare un modello da uno scenario, è necessario essere un amministratore di Fusion.

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario da cui desideri creare un modello.
1. Fai clic sul menu a discesa **Amministratore** nell&#39;angolo superiore destro della pagina.
1. Seleziona **Clona come modello**.

   Lo scenario viene copiato in una pagina Nuovo modello.
1. (Facoltativo) Rinominare il modello sostituendo il **[!UICONTROL Nome nuovo modello]** predefinito nell&#39;angolo superiore sinistro.
1. (Facoltativo) Per modificare la lingua del modello, fare clic su **[!UICONTROL Imposta modello]** ![icona Impostazioni scenario](assets/scenario-settings-icon.png) e selezionare la lingua dal menu a discesa Lingua.

   >[!IMPORTANT]
   >
   >La selezione Lingue corrisponde alle lingue disponibili nelle impostazioni di sistema e riguarda solo il nome del modello pubblico e la relativa descrizione. Una volta salvato il modello, non è possibile modificare il linguaggio del modello.

1. (Facoltativo) Per immettere una descrizione del modello, fare clic su **[!UICONTROL Configura modello]** ![Icona impostazioni scenario](assets/scenario-settings-icon.png) e immettere la descrizione.
1. Modifica le app, i moduli e gli strumenti come desideri, utilizzando gli stessi processi utilizzati per aggiungere moduli a uno scenario.

   Per istruzioni, vedere gli articoli in [Aggiungi moduli](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Per aggiungere informazioni contestuali ai moduli, vedere [Configurare la funzionalità [!UICONTROL Wizard]](#set-up-wizard-functionality) in questo articolo.

   >[!NOTE]
   >
   >Se il modello include moduli che richiedono l’aggiunta di connessione, credenziali o altre informazioni riservate, queste informazioni non vengono condivise con gli utenti del modello.

1. (Facoltativo) Fai clic su **[!UICONTROL Esegui una volta]** per verificare il modello.
1. Fai clic sull&#39;icona **[!UICONTROL Salva]** ![Salva](assets/save-icon.png).

## Configura funzionalità [!UICONTROL Wizard] {#set-up-wizard-functionality}

La [!DNL Workfront Fusion template] [!UICONTROL procedura guidata] consente di fornire agli utenti futuri del modello istruzioni o informazioni relative ai campi specifici utilizzati nei moduli.

1. Durante la creazione di un modello, fai clic su un modulo aggiunto al modello per visualizzarne i campi.
1. Individuare il campo in cui si desidera aggiungere le informazioni della [!UICONTROL Procedura guidata] e abilitare **[!UICONTROL Utilizza nella procedura guidata]** per tale campo.
1. Immettere le informazioni da rendere visibili agli utenti nel campo [!UICONTROL Guida].
1. (Facoltativo) Per consentire agli utenti di visualizzare questo testo quando utilizzano il modello, abilitare **[!UICONTROL Usa come valore predefinito]**.
1. Ripetere i passaggi da 2 a 4 per ogni campo per il quale si desidera fornire informazioni.
1. Fare clic su **[!UICONTROL OK]** per salvare le modifiche e chiudere il modulo.
