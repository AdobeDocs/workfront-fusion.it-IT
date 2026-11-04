---
title: Visualizzare e gestire i fusi orari
description: Scopri come visualizzare e gestire le impostazioni del fuso orario in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# Visualizzare e gestire i fusi orari

Adobe Workfront Fusion include controlli per i fusi orari a livello di organizzazione e di utente.

* Fusi orari dell’organizzazione: gli scenari utilizzano i fusi orari dell’organizzazione per determinare quando si verifica un evento programmato.

* Fusi orari utente: i fusi orari utente determinano l’ora che viene visualizzata da un utente.

>[!BEGINSHADEBOX]

Esempio:

Un’organizzazione ha sede a New York e l’orario è impostato su UTC-5 (America/New York). Lo scenario A è di proprietà di questa organizzazione ed è pianificato per l&#39;esecuzione alle 09:00 ogni giorno. Lo scenario va in onda alle 9 nel fuso orario di New York.

Un utente di questa organizzazione vive a Los Angeles e il suo fuso orario è impostato su UTC-8 (America/Los Angeles). Quando questo utente visualizza la cronologia di esecuzione dello scenario A, nota che lo scenario è stato eseguito alle 06:00. Anche se lo scenario è andato in onda in base all&#39;ora a New York, l&#39;utente vede l&#39;ora come convertita nel proprio fuso orario.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">Livello di accesso</td> 
   <td> Per modificare il fuso orario di un'organizzazione è necessario essere proprietari o amministratori. </td>
   </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Visualizzare e gestire il fuso orario dell’utente

1. In Fusion, fai clic sull’icona del tuo profilo Adobe all’estrema parte superiore destra dello schermo.
1. Nel menu visualizzato, selezionare **Profilo Fusion**.
1. Selezionare la scheda **Opzioni fuso orario**. Le schede si trovano direttamente sotto il tuo nome.
Verrà visualizzato l&#39;elenco Opzioni fuso orario.
1. Nell&#39;area Web dell&#39;elenco Opzioni fuso orario individuare il proprio nome.

   L&#39;impostazione attuale del fuso orario dell&#39;utente viene visualizzata a destra del nome.
1. Per modificare il fuso orario, fare clic su Modifica ![Modifica fuso orario](assets/edit-timezone-icon.png) accanto al fuso orario.
1. Nella finestra Modifica dettagli, nel campo **Fuso orario**, selezionare il fuso orario che si desidera impostare autonomamente.
1. Fai clic su **Salva**.


## Visualizza e gestisci il fuso orario della tua organizzazione

>[!NOTE]
>
>Per modificare il fuso orario di un&#39;organizzazione è necessario essere proprietari o amministratori.

1. In Fusion, fai clic sull’icona del tuo profilo Adobe all’estrema parte superiore destra dello schermo.
1. Nel menu visualizzato, selezionare **Profilo Fusion**.
1. Selezionare la scheda **Opzioni fuso orario**. Le schede si trovano direttamente sotto il tuo nome.
Verrà visualizzato l&#39;elenco Opzioni fuso orario.
1. Nell&#39;area Scenari dell&#39;elenco Opzioni fuso orario individuare l&#39;organizzazione per la quale si desidera visualizzare o gestire il fuso orario.

   L’impostazione attuale del fuso orario dell’organizzazione viene visualizzata a destra del nome dell’organizzazione.
1. Per modificare il fuso orario, fare clic su Modifica ![Modifica fuso orario](assets/edit-timezone-icon.png) accanto al fuso orario.
1. Nel campo **Fuso orario** della finestra Modifica dettagli selezionare il fuso orario che si desidera impostare per l&#39;organizzazione.
1. Fai clic su **Salva**.


