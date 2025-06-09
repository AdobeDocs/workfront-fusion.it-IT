---
title: Moduli MCP (Model Context Protocol)
description: Il modulo MCP (Model Context Protocol) consente di elaborare un prompt utente utilizzando MCP.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# Moduli MCP (Model Context Protocol)

Model Context Protocol (MCP) è un modo per collegare in modo sicuro i modelli di linguaggio AI con altre applicazioni. Puoi configurare i server MCP, che consentono al modello di intelligenza artificiale di accedere all’applicazione. È quindi possibile inviare un messaggio di richiesta al modello di IA, che può restituire informazioni dall&#39;applicazione.

Ad esempio, puoi configurare un server MCP per collegare un modello di IA con Gmail. Quando invii il messaggio &quot;Dammi le mie ultime 5 e-mail da Gmail&quot;, l’utente può accedere a Gmail e restituire le e-mail.

Il modulo MCP (Model Context Protocol) consente di elaborare un prompt utente utilizzando un modello del linguaggio e server MCP.

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
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

## Modulo Model Context Protocol e relativi campi

Quando configuri il modulo MCP, [!DNL Adobe Workfront Fusion] visualizza i campi elencati di seguito. Un titolo in grassetto in un modulo indica un campo obbligatorio.

### Prompt utente processo

Questo modulo di azione elabora un prompt utilizzando il modello di linguaggio e i server MCP specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Chiave [!UICONTROL Large Language Model (LLM)]</td> 
   <td> <p>Immetti o mappa la chiave API per il modello di lingua di grandi dimensioni che desideri utilizzare per questo prompt. </p> <p>Attualmente, è supportata solo la chiave API antropica.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Server MCP]</td> 
   <td> <p>Per ogni server MCP che si desidera rendere disponibile per questo prompt, fare clic su <b>Aggiungi elemento</b> e immettere il nome e l'host del server. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Immettere il prompt]</td> 
   <td> <p>Immettete o mappate la richiesta per il modello di lingua di grandi dimensioni. </p> </td> 
  </tr> 
 </tbody> 
</table>
