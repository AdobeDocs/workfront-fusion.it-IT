---
title: Visualizzare e gestire le versioni degli scenari
description: Puoi visualizzare, ripristinare, rinominare o scaricare i blueprint per le versioni precedenti di uno scenario.
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 14095350b645736fc64160a94204f828fd5f68c8
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 14%

---

# Visualizzare e gestire le versioni degli scenari

Adobe Workfront Fusion salva una versione dello scenario ogni volta che cambia.

Puoi visualizzare, ripristinare, rinominare o scaricare i blueprint per le versioni precedenti di uno scenario.

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

## Visualizzare e gestire la cronologia delle versioni di uno scenario

1. Fai clic su **[!UICONTROL Scenari]** ![Icona Scenari](assets/scenarios-icon.png) nel pannello a sinistra, quindi fai clic sullo scenario per aprirlo.
1. Fai clic sull&#39;icona [!UICONTROL Altro] ![Icona Altro](assets/more-icon.png) nella parte inferiore dello schermo, quindi fai clic su **[!UICONTROL Versioni precedenti]**.

   Viene visualizzato un elenco delle versioni precedenti.
1. (Facoltativo) Per rinominare la versione, fare clic sul menu Altro ![Altro menu](assets/more-icon-vertical.png) nella riga relativa a tale versione, selezionare **Modifica** e immettere un nome nel campo. Fai clic su **Salva** per salvare il nuovo nome.

   È consigliabile assegnare un nome che descriva le modifiche apportate per questa versione.
1. (Facoltativo) Per scaricare il blueprint per una versione precedente, fai clic sul menu Altro ![Altro menu](assets/more-icon-vertical.png) nella riga per quella versione, quindi seleziona **Scarica**.
1. (Facoltativo) Per confrontare le modifiche tra due versioni, fare clic su **Visualizza modifiche** per quella versione.

   Per informazioni dettagliate e istruzioni sul confronto delle versioni, vedere [Confrontare le versioni dello scenario](#compare-scenario-versions) in questo articolo.
1. (Facoltativo) Per ripristinare la versione, fare clic su **Ripristina** nella riga della versione


   >[!NOTE]
   >
   >La versione ripristinata dello scenario non viene salvata automaticamente. Se desideri salvare la versione ripristinata dello scenario, devi salvarla manualmente.



## Confrontare le versioni degli scenari

&#x200B;
La funzionalità di visualizzazione delle modifiche mostra le differenze tra due versioni dello scenario, una accanto all’altra, in modo da poter vedere esattamente ciò che è cambiato prima di decidere di ripristinare una precedente.

1. Fai clic su **[!UICONTROL Scenari]** ![Icona Scenari](assets/scenarios-icon.png) nel pannello a sinistra, quindi fai clic sullo scenario per aprirlo.
1. Fai clic sull&#39;icona [!UICONTROL Altro] ![Icona Altro](assets/more-icon.png) nella parte inferiore dello schermo, quindi fai clic su **[!UICONTROL Versioni precedenti]**.

   Viene visualizzato un elenco delle versioni precedenti.
&#x200B;
1. Fare clic su **Visualizza modifiche** per la versione dello scenario da visualizzare.
1. Viene aperta la visualizzazione **Rivedi modifiche** che confronta la versione con lo scenario corrente.

   Il pannello Revisioni si apre in una vista affiancata di due versioni dello scenario.

   * A sinistra viene visualizzata la versione corrente.
   * A destra è visibile la versione su cui hai fatto clic. Questa è la versione che puoi ripristinare.

   Per informazioni sulle modifiche, vedere [Esaminare le modifiche](#examine-changes) in questo articolo.

1. Per selezionare un&#39;altra versione per entrambi i lati, fai clic sul menu a discesa **Confronta da** o **Confronta con** nella parte superiore del pannello e seleziona un&#39;altra versione dello scenario.
1. Per cambiare lato, fare clic sul pulsante **⇄** tra gli scenari.
1. Per ripristinare lo scenario sul lato destro, fare clic su **Ripristina versione selezionata**

   Le versioni ripristinate vengono salvate come nuove versioni e possono quindi essere ripristinate in futuro.

   Per ripristinare lo scenario attualmente sul lato sinistro, scambiare i lati in modo che si trovi sul lato destro, quindi fare clic su **Ripristina versione selezionata**.


### Esamina le modifiche

&#x200B;
Ogni modifica viene visualizzata sul lato a cui appartiene e colorata in base al tipo di ripristino
eseguire le operazioni seguenti:

* Rosso (a sinistra): questa modifica non è presente nella versione a destra e verrebbe rimossa se la versione fosse stata ripristinata.
* Verde (destra): questa modifica si trova nella versione a destra e verrebbe aggiunta se la versione fosse stata ripristinata.

Se qualcosa è stato modificato, invece di essere rimosso o aggiunto, il valore viene visualizzato in rosso a sinistra e in verde a destra.
&#x200B;
Le modifiche sono raggruppate in sezioni:
&#x200B;

* **Scenario**: nome, descrizione e tipo.
* **Impostazioni scenario**: opzioni di pianificazione ed elaborazione.
* **Moduli**: moduli aggiunti, rimossi, spostati o riconfigurati.
* **Flussi**: banchi aggiunti, rimossi o riordinati.
* **Route router**: route e relativo contenuto.
* **Gestori errori**: rami di gestione degli errori.
* **Gruppi orfani**: moduli disconnessi nell&#39;area di lavoro.
&#x200B;
Se le due versioni sono identiche, viene visualizzato il messaggio/ **Nessuna differenza trovata**.
&#x200B;
