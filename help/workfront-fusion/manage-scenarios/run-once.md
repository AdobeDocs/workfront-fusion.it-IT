---
title: Utilizza Esegui una volta per testare uno scenario
description: Puoi testare uno scenario senza un trigger esterno utilizzando il pulsante Esegui una volta.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 9c05aa1111fd571ea6f0ff86943b2849a39e4973
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 0%

---

# Utilizza Esegui una volta per testare uno scenario

Durante la creazione, l’aggiornamento o il perfezionamento di uno scenario, puoi utilizzare il pulsante &quot;Esegui una volta&quot; per attivarlo su richiesta. In questo modo, puoi testare lo scenario senza attenderne la logica di attivazione, ad esempio eventi specifici o intervalli di polling.

Puoi anche eseguire uno scenario una volta per configurare le strutture di dati

>[!TIP]
>
>È consigliabile eseguire test frequenti durante la creazione e l’ottimizzazione degli scenari.

## Utilizzare la funzionalità Esegui una volta

La funzione Esegui una volta si trova nell’editor di scenari.

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Selezionare lo scenario in cui si desidera eseguire l&#39;esperto punteggio scenario.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic su **Esegui una volta** nell&#39;angolo inferiore sinistro dell&#39;editor scenari.
1. (Condizionale) Se lo scenario viene attivato da un webhook o è uno scenario figlio, seleziona l’input per l’esecuzione dei test.

   * **Attesa di una chiamata del webhook esterno**: lo scenario inizierà ad essere in ascolto di una chiamata del webhook in ingresso. Per fornire il webhook, devi attivarlo dal sistema esterno.

     Ad esempio, se il webhook è in ascolto di una nuova richiesta in Workfront, devi creare una nuova richiesta in Workfront per attivarla e completare la funzionalità &quot;Esegui una volta&quot;.

     >[!NOTE]
     >
     >Questa opzione è disponibile solo per gli scenari webhook.

   * **Utilizza un input di esecuzione precedente**: è necessario selezionare un&#39;esecuzione precedente. L’esecuzione &quot;Esegui una volta&quot; utilizza i dati di input che hanno attivato l’esecuzione selezionata.

     Per selezionare un&#39;esecuzione precedente, selezionarla e fare clic su **Esegui**.

     Per esaminare i dati di input dell&#39;esecuzione prima di selezionarla, fare clic su **Anteprima input** per l&#39;esecuzione.

     >[!NOTE]
     >
     >Prima che questa opzione sia disponibile, è necessario che lo scenario abbia completato le esecuzioni precedenti.

   * **Fornire l&#39;input manualmente**: è necessario fornire il payload del webhook per l&#39;input dello scenario. Deve essere in formato JSON.

     Per specificare l&#39;input, immettere il testo nella casella **Payload webhook** e fare clic su **Esegui**.
