---
title: Copiare moduli o scenari
description: In Adobe Workfront Fusion è possibile copiare moduli, gruppi di moduli o interi scenari. Questa funzionalità consente di riutilizzare scenari o parti di scenari senza doverli ricreare.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# Copiare moduli o scenari

In Adobe Workfront Fusion è possibile copiare moduli, gruppi di moduli o interi scenari. Questa funzionalità consente di riutilizzare scenari o parti di scenari senza doverli ricreare.

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

## Prerequisiti

I moduli devono esistere in uno scenario prima di poterli copiare.

## Copiare un modulo o un gruppo di moduli

Quando si copia un modulo, la copia mantiene tutti i valori e le impostazioni dei campi del modulo originale.

Puoi incollare il modulo o i moduli in un’altra area dello stesso scenario o in uno scenario diverso.

Quando si incollano moduli in uno scenario diverso, considera quanto segue:

* Qualsiasi valore di campo che richiami informazioni da un altro modulo non copiato non può più accedere a tali informazioni. Devi impostare questi campi per estrarre informazioni dal nuovo scenario.
* Se si incollano i moduli in uno scenario di proprietà di un altro team o organizzazione, tutte le connessioni devono essere aggiornate alle connessioni di proprietà del team o dell&#39;organizzazione proprietaria del nuovo scenario.

### Copia moduli

La copia di un gruppo di moduli è simile alla copia di un singolo modulo.

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri copiare un modulo.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic con il pulsante destro del mouse sul modulo che desideri copiare.

   >[!NOTE]
   >
   >È possibile selezionare più moduli tenendo premuto [!UICONTROL shift] e facendo clic sui moduli da copiare. Copiando un gruppo di moduli vengono copiate anche le linee di connessione, i filtri o la logica di routing tra di essi.

1. Selezionare **[!UICONTROL Copy module]**.
1. Spostare il cursore nell&#39;area dello scenario in cui si desidera copiare lo scenario.
1. Fare clic con il pulsante destro del mouse e selezionare **[!UICONTROL Paste]**.
1. Connetti i moduli incollati allo scenario trascinandoli nella posizione appropriata nello scenario.

   È inoltre possibile utilizzare i tasti di scelta rapida per copiare e incollare.

## Copiare uno scenario tramite clonazione

La clonazione di uno scenario ne crea una copia, che potrai quindi modificare.

1. Apri la pagina dei dettagli dello scenario:

   1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic su uno scenario su cui desideri visualizzare i dettagli.

      Oppure

      Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic con il pulsante destro del mouse su **[!UICONTROL Options]** in alto a destra della pagina.
1. Selezionare **[!UICONTROL Clone]**.
1. (Facoltativo) Immetti un nome per il nuovo scenario.
1. (Facoltativo) Abilitare **[!UICONTROL Keep the states of any new modules the same as those being duplicated]** per assicurarsi che lo scenario copiato includa anche informazioni sui record più recenti elaborati dallo scenario originale.
1. Fare clic su **[!UICONTROL Save]** per creare lo scenario.

## Copiare uno scenario utilizzando blueprint

I blueprint dello scenario rappresentano i valori di disposizione, mappatura e campi di uno scenario specifico in un determinato momento. Puoi esportare una blueprint di scenario in un file JSON sul computer, quindi importarla durante la creazione di un nuovo scenario. È possibile modificare gli scenari importati da una blueprint di scenario.

Una blueprint di scenario rappresenta l’intero scenario. Se desideri copiare solo determinati moduli da uno scenario, consulta [Copiare un modulo o un gruppo di moduli](#copy-a-module-or-a-group-of-modules) in questo articolo.

### Esportare una blueprint di scenario

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri esportare una blueprint.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Nello scenario, fare clic sul menu **[!UICONTROL More]** nell&#39;area delle impostazioni dello scenario.
1. Fare clic su **[!UICONTROL Export Blueprint]**.

   Viene creato un file JSON che viene scaricato sul computer. È possibile individuare questo file nella cartella [!DNL Downloads].

### Importare una blueprint

>[!IMPORTANT]
>
>Se importi una blueprint in uno scenario esistente, la blueprint dello scenario sostituisce quello esistente. Non puoi aggiungere una blueprint a uno scenario esistente.

1. Inizia a creare un nuovo scenario.
1. Nello scenario, fare clic sul menu **[!UICONTROL More]** nell&#39;area delle impostazioni dello scenario.
1. Fare clic su **[!UICONTROL Import Blueprint]**.
1. Nella finestra di dialogo visualizzata, fare clic su **[!UICONTROL Browse]**
1. Passare alla blueprint da importare e fare clic su **[!UICONTROL Open]**.
1. Fare clic su **[!UICONTROL Save]**.

   Viene creato un file JSON che viene scaricato sul computer. È possibile individuare questo file nella cartella [!UICONTROL Downloads].

## Copiare e riutilizzare gli scenari utilizzando i modelli

È possibile creare modelli come punto di partenza per gli scenari [!DNL Workfront Fusion]. Quando crei uno scenario da un modello, puoi modificarlo senza modificarlo. I valori dei campi non vengono salvati nei modelli.

Per ulteriori informazioni sulla creazione di uno scenario utilizzando un modello, vedere [Creare scenari con modelli](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md).

## Risoluzione dei problemi

Se si stanno copiando e incollando moduli come descritto in [Copiare un modulo o un gruppo di moduli](#copy-a-module-or-a-group-of-modules) e non viene visualizzato nulla quando si incolla, controllare le impostazioni del sito del browser per assicurarsi che sia consentito incollare dagli Appunti.