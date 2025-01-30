---
title: Mappare un file tra moduli
description: Alcuni moduli sono in grado di elaborare i file. Questi moduli possono restituire un file di output da inviare per l'ulteriore elaborazione o richiedere che venga trasmesso un file per l'elaborazione. Prima che questi moduli possano lavorare insieme per elaborare i file, devono essere mappati l’uno sull’altro.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Mappare un file tra moduli

Alcuni moduli possono elaborare i file. Questi moduli possono restituire un file di output da inviare per l&#39;ulteriore elaborazione o richiedere che venga passato un file per l&#39;elaborazione. È possibile mappare i file in modo che un output di file di un modulo possa essere elaborato da un altro modulo.

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

## Mappare i file dai moduli di origine ai moduli di destinazione

I moduli possono elaborare file che richiedono due informazioni:

* Nome file
* Contenuto file (dati)

Se uno dei moduli precedenti genera un file, è possibile selezionare il modulo di origine e il nome e i dati dell&#39;output di file di tale modulo vengono mappati al modulo di destinazione.

Puoi anche immettere manualmente questo nome e questi dati o mapparli dai moduli precedenti. Ciò può risultare utile, ad esempio, quando si rinomina un file.

>[!NOTE]
>
>Se devi elaborare un file da un URL, ti consigliamo di utilizzare il modulo `HTTP > Get a File` per scaricare il file dall&#39;URL e quindi di mappare il file dal modulo `HTTP > Get a File` al campo del modulo desiderato nel tuo scenario.
>
>![File mappa](assets/map-source-file.png)

Per mappare un file:

1. Fare clic sulla scheda **[!UICONTROL Scenarios]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera mappare un file.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Nel modulo di destinazione, che è la destinazione a cui si sta eseguendo il mapping, individuare l&#39;area **file Source**.
1. Per mappare l&#39;output di un file di un modulo precedente, selezionare il modulo che restituisce il file.

   ![Documento di download Workfront](assets/wf-download-document.png)

1. Per mappare il nome e i dati manualmente, selezionare Mappa, quindi immettere o mappare il nome e i dati del file.

   ![Utilizza l&#39;opzione mappa](assets/use-the-map-option.png)

1. Continuare la configurazione del modulo oppure fare clic su **OK**.
