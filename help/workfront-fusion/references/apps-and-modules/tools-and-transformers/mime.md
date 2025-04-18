---
title: Moduli MIME
description: È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME text/html viene elaborato in un browser in modo diverso rispetto a un file con tipo MIME image/jpeg. I tipi MIME funzionano indipendentemente dal sistema operativo e dall'hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 7edfe4a7b19597ea6e56bb2ca3969d742dbaf999
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# [!UICONTROL Moduli MIME]

È possibile utilizzare i tipi MIME in Adobe Workfront Fusion. I tipi MIME (Multipurpose Internet Mail Extension) sono etichette che consentono al software di identificare diversi tipi di dati condivisi su Internet. I server web e i browser utilizzano il tipo MIME per determinare cosa si deve fare con un file. Ad esempio, un file con tipo MIME `text/html` verrà elaborato in un browser in modo diverso rispetto a un file con tipo MIME `image/jpeg`. I tipi MIME funzionano indipendentemente dal sistema operativo e dall&#39;hardware.

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
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Nessun requisito di licenza per Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
