---
title: Moduli MIME
description: È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME text/html viene elaborato in un browser in modo diverso rispetto a un file con tipo MIME image/jpeg. I tipi MIME funzionano indipendentemente dal sistema operativo e dall'hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
TQID: https://experienceleague.adobe.com/65lJuH7aL35rZCYDowjJuxuQAh88LHNyL3XRQVDJoOY
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 25%

---

# [!UICONTROL Moduli MIME]

È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME `text/html` verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME `image/jpeg`. I tipi MIME funzionano indipendentemente dal sistema operativo e dall&#39;hardware.

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



## [!UICONTROL Moduli MIME] e relativi campi

* [Ottieni estensione file](#get-a-file-extension)
* [Ottieni un tipo MIME](#get-a-mime-type)

### [!UICONTROL Ottieni estensione file]

Questo modulo di trasformazione restituisce l’estensione di file originale per un determinato tipo MIME.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL tipo MIME]</td> 
   <td> <p>Immetti o mappa il tipo MIME per il quale desideri determinare l’estensione del file. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Ottieni un tipo MIME]

Questo modulo di trasformazione restituisce il tipo MIME associato a un nome di file, un percorso o un’estensione specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>Immetti o mappa il file per il quale desideri determinare il tipo MIME. </p> <p>È possibile immettere il file utilizzando:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Percorso file]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Nome file]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL Estensione File]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
