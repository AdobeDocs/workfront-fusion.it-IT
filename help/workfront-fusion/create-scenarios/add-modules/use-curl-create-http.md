---
title: Utilizzare cURL per aggiungere un modulo HTTP
description: È possibile incollare una richiesta cURL nello scenario e Fusion crea un modulo HTTP configurato dalla richiesta cURL.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# Utilizzare cURL per aggiungere un modulo HTTP

È possibile incollare una richiesta cURL nello scenario e Fusion crea un modulo HTTP configurato dalla richiesta cURL.

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
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Creare un modulo HTTP da una richiesta cURL


Per creare un modulo HTTP utilizzando cURL:

1. Crea il testo della richiesta cURL al di fuori di Fusion, ad esempio in un editor di testo.
1. Copia la richiesta cURL negli Appunti.
1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri creare il modulo.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic con il pulsante destro del mouse su uno spazio vuoto nell&#39;editor di scenari e seleziona **Incolla**.

   Oppure

   Premere Ctrl + V (Windows) o Cmd + V (Mac).


   Viene creato un modulo HTML.
1. Trascina il modulo per collegarlo allo scenario.

## Risoluzione dei problemi

Se il cURL non viene incollato nello scenario, controlla le impostazioni del browser per assicurarti che l’operazione Incolla dagli Appunti sia abilitata.
