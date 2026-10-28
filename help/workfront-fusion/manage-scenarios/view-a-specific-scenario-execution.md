---
title: Visualizzare una specifica esecuzione di uno scenario
description: Puoi visualizzare i dettagli di una specifica esecuzione dello scenario, inclusi il filtro e la ricerca di eventi dello scenario.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
TQID: 'https://experienceleague.adobe.com/Msh3ArxBUIu6YDZjL7eXpxlEBiYABHN-Q7xUlJ-qU0g'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 15%
---
# Visualizzare una specifica esecuzione di uno scenario

Puoi visualizzare i dettagli di una specifica esecuzione dello scenario, inclusi il filtro e la ricerca di eventi dello scenario.

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

## Visualizzare un’esecuzione specifica

Puoi visualizzare un’esecuzione dalla cronologia dello scenario.


1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra, quindi fai clic sullo scenario.

   Oppure

   Se si sta lavorando sullo scenario nell&#39;editor scenario, fare clic sulla freccia sinistra ![Esci dalla modifica](assets/exit-editing-arrow.png) nell&#39;angolo superiore sinistro della finestra.

1. Fare clic su **Cronologia** accanto al nome dello scenario.
   ![scheda cronologia](assets/history-tab.png)


1. Individua l&#39;esecuzione che desideri visualizzare e fai clic su **Dettagli** all&#39;estrema destra della riga dell&#39;esecuzione. Il collegamento [!UICONTROL details] è visibile solo se sono disponibili dettagli sull&#39;esecuzione.

   Viene visualizzato il diagramma di scenario con il pannello dei dettagli di esecuzione aperto a destra.

   I moduli che hanno prodotto l’output per questa esecuzione sono contrassegnati con titoli verdi.

   I moduli non eseguiti vengono oscurati.

1. Per visualizzare l’output di un modulo, fai clic sulla bolla dei dettagli di output accanto al modulo. Il numero nella bolla rappresenta il numero di bundle generati dal modulo.

   ![Bolla di output vicino a un modulo](assets/new-output-bubble.png)

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

## Rivedere un’esecuzione nel nuovo editor di scenari

Nella nuova esperienza, quando apri un’esecuzione dalla cronologia di esecuzione, i controlli accanto al lato destro dell’area di lavoro consentono di individuare l’errore senza modificare lo scenario:

![Rivedere un&#39;esecuzione](assets/review-an-execution.png)

| Controllo | Dettagli |
| ---------- | ---------- |
| Passa all&#39;errore o all&#39;avviso successivo | Mostra quanti moduli hanno avuto un problema nel ciclo corrente. Ogni clic passa al successivo, prima gli errori e poi gli avvisi, da sinistra a destra. Il modulo viene centrato e viene aperta la prima operazione non riuscita. Il pulsante è nascosto quando l’esecuzione non presentava errori o avvisi. |
| Moduli di ricerca | Trova un modulo per nome e centralo sull’area di lavoro. Premere Ctrl+K (Windows) o Comando+K (Mac). |
| Note | Mostrare o nascondere le note dello scenario. Questo controllo viene visualizzato solo quando lo scenario include note e le note sono di sola lettura. |
| Spiega flusso | Animare l&#39;ordine di esecuzione dei moduli dello scenario. Fare di nuovo clic su di esso oppure premere ESC per interrompere. |
| Zoom in, Zoom out, Focus e minimap | Funziona come in modalità di modifica. |

Nell&#39;angolo superiore destro è disponibile anche l&#39;opzione **Visualizzazione compatta**. Quando si esamina un’esecuzione, questo cambia il layout solo mentre si osserva tale esecuzione. Non modifica l’impostazione della vista Compatta per la modifica e non viene salvato nulla nello scenario.

Seleziona un evento nell’esecuzione per centrare ed evidenziare il modulo corrispondente. Quando sono disponibili i dettagli dell’operazione, viene visualizzato il pannello Richiesta e risposta. Se il pannello non dispone di dati, i dettagli delle richieste e delle risposte non vengono conservati per tale esecuzione. Per raccoglierli per le esecuzioni future, vedere [Log di debug temporanei](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs).
