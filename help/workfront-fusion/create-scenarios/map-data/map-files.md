---
title: Mappare un file tra moduli
description: Alcuni moduli sono in grado di elaborare i file. Questi moduli possono restituire un file di output da inviare per l'ulteriore elaborazione o richiedere che venga trasmesso un file per l'elaborazione. Prima che questi moduli possano lavorare insieme per elaborare i file, devono essere mappati l’uno sull’altro.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
TQID: https://experienceleague.adobe.com/DVCy-0qCEuwZJqbGQPd3Pu9erVaX1wosPUWEtTFLkq4
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 24%

---

# Mappare un file tra moduli

Alcuni moduli possono elaborare i file. Questi moduli possono restituire un file di output da inviare per l&#39;ulteriore elaborazione o richiedere che venga passato un file per l&#39;elaborazione. È possibile mappare i file in modo che un output di file di un modulo possa essere elaborato da un altro modulo.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront.</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
