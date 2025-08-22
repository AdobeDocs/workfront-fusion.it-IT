---
content-type: reference
title: Modifica modelli
description: Questo articolo descrive come modificare i modelli di Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Modifica modelli

I modelli di Adobe Workfront Fusion sono scenari predefiniti progettati per automatizzare e semplificare vari flussi di lavoro. Questi modelli possono aiutarti a configurare rapidamente integrazioni e automazioni senza dover creare nulla.

Gli amministratori dispongono delle autorizzazioni necessarie per visualizzare, modificare, rinominare, pubblicare, approvare ed eliminare i modelli creati da altri utenti.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">piano Adobe Workfront</td>
      <td><p>Qualsiasi</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Licenza Adobe Workfront</td>
      <td><p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p></td>
    </tr>
    <tr>
      <td role="rowheader">Licenza Adobe Workfront Fusion**</td>
      <td>
        <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
        <p>Oppure</p>
        <p>Legacy: qualsiasi</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Prodotto</td>
      <td>
        <p>Novità:</p>
        <ul>
          <li>[!UICONTROL Select] o piano Workfront [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li>
          <li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li>
        </ul>
        <p>Oppure</p>
        <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Modificare i modelli di Workfront Fusion come amministratore

1. Fai clic su **[!UICONTROL Amministrazione]** nel pannello di navigazione a sinistra per aprire l&#39;area [!UICONTROL Amministrazione].
1. Fai clic su **[!UICONTROL Tutti i modelli]** nel pannello di navigazione a sinistra.
1. Fare clic su **[!UICONTROL Dettagli]** a destra del modello che si desidera modificare.
1. (Facoltativo) Rinomina il modello facendo clic su **Opzioni** nell&#39;angolo superiore destro e selezionando **Rinomina**.
1. (Facoltativo) Per modificare la lingua del modello, fare clic su **[!UICONTROL Crea un nuovo modello]** ![icona Impostazioni scenario](assets/fusion-scenario-settings-icon.png) e selezionare la lingua dal menu a discesa Lingua.

   >[!IMPORTANT]
   >
   >La selezione Lingue corrisponde alle lingue disponibili nelle impostazioni di sistema e riguarda solo il nome del modello pubblico e la relativa descrizione. Una volta salvato il modello, non è possibile modificare il linguaggio del modello.

1. (Facoltativo) Per modificare la descrizione del modello, fare clic su **[!UICONTROL Configura modello]** ![Icona impostazioni scenario](assets/fusion-scenario-settings-icon.png) e immettere la descrizione.
1. Aggiungi o modifica app, moduli e strumenti nello stesso modo in cui utilizzi quando crei uno scenario standard.

   Per aggiungere informazioni contestuali ai moduli, vedere [Configurare la funzionalità [!UICONTROL Wizard]](#set-up-wizard-functionality) in questo articolo.

   <!--For more information on building a scenario, see [Create a scenario in Adobe Workfront Fusion](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Se il modello include moduli che richiedono l’aggiunta di connessione, credenziali o altre informazioni riservate, queste informazioni non vengono condivise con gli utenti del modello.

1. (Facoltativo) Fai clic su **[!UICONTROL Esegui una volta]** per verificare il modello.
1. Fai clic sull&#39;icona **[!UICONTROL Salva]** ![Salva](assets/save-icon.png).


## Configura funzionalità [!UICONTROL Wizard]

La [!DNL Workfront Fusion template] [!UICONTROL procedura guidata] consente di fornire agli utenti futuri del modello istruzioni o informazioni relative ai campi specifici utilizzati nei moduli.

1. Fai clic sul modulo aggiunto al modello per visualizzare i campi del modulo.
1. Individuare il campo in cui si desidera aggiungere le informazioni della [!UICONTROL Procedura guidata] e abilitare **[!UICONTROL Utilizza nella procedura guidata]** sotto tale campo.
1. Immettere le informazioni da rendere visibili agli utenti nel campo [!UICONTROL Guida].
1. (Facoltativo) Per consentire agli utenti di visualizzare questo testo quando utilizzano il modello, abilitare **[!UICONTROL Usa come valore predefinito]**.
1. Ripetere i passaggi da 2 a 4 per ogni campo per il quale si desidera fornire informazioni.
1. Fare clic su **[!UICONTROL OK]** per salvare le modifiche e chiudere il modulo.

Il processo di pubblicazione è lo stesso utilizzato per gli utenti standard. Per informazioni, vedere la sezione [Pubblicare e condividere modelli](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) per ulteriori dettagli.

## Stati dei modelli

Puoi controllare lo stato nella pagina del modello sotto il nome del modello.

Sono disponibili i seguenti stati:

* **[!UICONTROL Privato]**: questo modello è visibile solo per l&#39;autore del modello e il relativo team.
* **[!UICONTROL Pubblicato]**: questo modello è visibile solo per l&#39;autore del modello e per il suo team. Dopo la pubblicazione, se necessario, puoi inviare il modello per l’approvazione. È inoltre possibile copiare un collegamento condivisibile.
* **[!UICONTROL Approvato]**: questo modello è visibile a tutti gli utenti di Workfront Fusion nella scheda [!UICONTROL Modelli pubblici]. Puoi anche copiare un collegamento condivisibile facendo clic su [!UICONTROL Opzioni] nell&#39;angolo superiore destro dello schermo.

Puoi anche controllare lo stato dalla scheda [!UICONTROL Modelli team]. Se un modello viene pubblicato, a destra del nome del modello è presente un&#39;icona.

* **Icona occhi**: il modello è pubblicato ed è visibile per il team.
* **Icona segno di spunta giallo**: il modello è pubblicato, è visibile solo per il team ed è in attesa di approvazione per essere aggiunto alla scheda Modelli pubblici.
* **Icona segno di spunta verde**: il modello è disponibile nella scheda Modelli pubblici ed è visibile per qualsiasi utente di Workfront Fusion. È ancora visibile nella scheda [!UICONTROL Modelli team]. L’autore del modello o il suo membro del team può comunque modificarlo.

I modelli senza icone hanno lo stato [!UICONTROL Privato]. Non vengono pubblicati e sono visibili solo al team.

## Individuare le informazioni SVG di un modello

1. Fai clic su **[!UICONTROL Amministrazione]** nel pannello di navigazione a sinistra per aprire l&#39;area [!UICONTROL Amministrazione].
1. Fai clic su **[!UICONTROL Modelli]** nel pannello di navigazione a sinistra.
1. Fare clic sul modello per il quale si desidera individuare le informazioni.
1. Fai clic su **Opzioni** nell&#39;angolo superiore destro.
1. Selezionare *Diagramma SVG*.

Qui puoi visualizzare il diagramma di SVG e il codice SVG.
