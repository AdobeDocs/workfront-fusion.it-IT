---
title: Moduli Qualtrics
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Qualtrics e collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# Moduli Qualtrics

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Qualtrics] e collegarlo a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Piano Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] o versione successiva</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Requisito di licenza corrente: nessun requisito di licenza per Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno corrente del prodotto: se disponi del piano Adobe Workfront [!UICONTROL Select] o [!UICONTROL Prime], per utilizzare le funzionalità descritte in questo articolo la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront. Workfront Fusion è incluso nel piano Workfront di [!UICONTROL Ultimate].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: per utilizzare le funzionalità descritte in questo articolo, la tua organizzazione deve acquistare Adobe Workfront Fusion e Adobe Workfront.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso di cui si dispone, contattare l&#39;amministratore Workfront.

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare i moduli [!DNL Qualtrics], è necessario disporre di un account [!UICONTROL Qualtrics].

## Informazioni API Qualtrics

Il connettore Qualtrics utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## Connessione di [!DNL Qualtrics] a Workfront Fusion

Puoi creare una connessione al tuo account [!DNL Qualtrics] direttamente da un modulo [!UICONTROL Qualtrics].

1. In qualsiasi modulo [!UICONTROL Qualtrics], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Immettere le seguenti informazioni:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Nome connessione]</p> </td> 
      <td> <p>Immettere un nome per la nuova connessione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID datacenter] </td> 
      <td>Utilizza il formato <code>&lt;Data Center ID>.qualtrics.com</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>Per individuare la tua chiave API, consulta la documentazione di [!DNL Qualtrics].</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## [!DNL Qualtrics] moduli e relativi campi

Per il connettore [!DNL Qualtrics] sono disponibili i seguenti moduli:

* [!UICONTROL Guarda la risposta al nuovo sondaggio]
* [!UICONTROL Crea un contatto directory]
* [!UICONTROL Eliminare un contatto directory]
* [!UICONTROL Ottieni un contatto directory]
* [!UICONTROL Aggiorna un contatto directory]
* [!UICONTROL Crea una nuova distribuzione sondaggio tramite SMS]
* [!UICONTROL Distribuire un sondaggio tramite e-mail]
* [!UICONTROL Effettuare una chiamata API]
* [!UICONTROL Elenca contatti directory]
