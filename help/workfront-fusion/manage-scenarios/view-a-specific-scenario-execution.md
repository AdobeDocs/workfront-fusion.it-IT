---
title: Visualizzare l’esecuzione di uno scenario specifico
description: Puoi visualizzare i dettagli di una specifica esecuzione dello scenario, inclusi il filtro e la ricerca di eventi dello scenario.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 62b09469c1d85fd2bd1f154cde339cc4a10fc34a
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---

# Visualizzare l’esecuzione di uno scenario specifico

Puoi visualizzare i dettagli di una specifica esecuzione dello scenario, inclusi il filtro e la ricerca di eventi dello scenario.

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
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Visualizzare un’esecuzione specifica

Puoi visualizzare un’esecuzione dalla cronologia dello scenario.


1. Fai clic sulla scheda **[!UICONTROL Scenario]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic su **Cronologia** accanto al nome dello scenario.
   ![scheda cronologia](assets/history-tab.png)


1. Individua l&#39;esecuzione che desideri visualizzare e fai clic su **Dettagli** all&#39;estrema destra della riga dell&#39;esecuzione. Il collegamento [!UICONTROL details] è visibile solo se sono disponibili dettagli sull&#39;esecuzione.

   Viene visualizzato il diagramma di scenario con il pannello dei dettagli di esecuzione aperto a destra.

   I moduli che hanno prodotto l’output per questa esecuzione sono contrassegnati con titoli verdi.

   I moduli non eseguiti vengono oscurati.

1. Per visualizzare l’output di un modulo, fai clic sulla bolla dei dettagli di output accanto al modulo. Il numero nella bolla rappresenta il numero di bundle generati dal modulo.

   ![Bolla di output vicino a un modulo](assets/output-bubble.png)

1. Per visualizzare i bundle passati attraverso un filtro, fai clic sul filtro. Il numero accanto al filtro rappresenta il numero di bundle passati attraverso il filtro.
1. Per cercare un modulo o un evento specifico nel pannello di esecuzione, immettere il termine di ricerca nella casella **Cerca eventi di esecuzione**. I risultati vengono visualizzati durante la digitazione.
1. Per limitare i risultati della ricerca nel pannello di esecuzione in base allo stato, ad esempio Completato o Avviso, fare clic sul menu a discesa **Filtro stato** e selezionare lo stato.




>[!NOTE]
>
>Per creare un collegamento a un modulo specifico, aggiungere `?moduleId=<module-id>` all&#39;URL durante la visualizzazione delle pagine seguenti:
>
>* Pagina di modifica scenario (l&#39;URL termina in `/edit`)
>* Esecuzione di uno scenario specifico (l&#39;URL termina in `/logs/<log-id>`)
>
>`<module-id>` fa riferimento al numero accanto all&#39;etichetta del modulo durante la visualizzazione dello scenario.
>
>Questo può essere utile quando si eseguono scenari di debug o si copia la configurazione del modulo.
