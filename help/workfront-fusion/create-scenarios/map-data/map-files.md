---
title: Mappare un file tra moduli
description: Alcuni moduli sono in grado di elaborare i file. Questi moduli possono restituire un file di output da inviare per l'ulteriore elaborazione o richiedere che venga trasmesso un file per l'elaborazione. Prima che questi moduli possano lavorare insieme per elaborare i file, devono essere mappati l’uno sull’altro.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '458'
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
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurazioni del livello di accesso*</td> 
   <td> 
     <p>Devi essere un amministratore di Workfront Fusion per la tua organizzazione.</p>
     <p>Devi essere un amministratore di Workfront Fusion per il tuo team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera mappare un file.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Nel modulo di destinazione, che è la destinazione a cui si sta eseguendo il mapping, individuare l&#39;area **file Source**.
1. Per mappare l&#39;output di un file di un modulo precedente, selezionare il modulo che restituisce il file.

   ![Documento di download Workfront](assets/wf-download-document.png)

1. Per mappare il nome e i dati manualmente, selezionare Mappa, quindi immettere o mappare il nome e i dati del file.

   ![Utilizza l&#39;opzione mappa](assets/use-the-map-option.png)

1. Continuare la configurazione del modulo oppure fare clic su **OK**.
