---
title: Moduli MIME
description: È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME text/html viene elaborato in un browser in modo diverso rispetto a un file con tipo MIME image/jpeg. I tipi MIME funzionano indipendentemente dal sistema operativo e dall'hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# [!UICONTROL MIME] moduli

È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME `text/html` verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME `image/jpeg`. I tipi MIME funzionano indipendentemente dal sistema operativo e dall&#39;hardware.

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisito licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione lavoro, [!UICONTROL [!DNL Workfront Fusion] per automazione lavoro</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL MIME] moduli e relativi campi

### [!UICONTROL Get a MIME type]

Questo modulo di trasformazione restituisce il tipo MIME associato a un nome, percorso o estensione specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>Immetti o mappa il file per il quale desideri determinare il tipo MIME. </p> <p>È possibile immettere il file utilizzando:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File path]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File name]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File extension]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Esempio: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a file extension]

Questo modulo di trasformazione restituisce l’estensione di file originale per un determinato tipo MIME.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>Immetti o mappa il tipo MIME per il quale desideri determinare l’estensione del file. </p> </td> 
  </tr> 
 </tbody> 
</table>
