---
title: Modifica webhook
description: È possibile modificare i webhook esistenti per i connettori Workfront e Workfront Planning.
author: Becky
feature: Workfront Fusion
source-git-commit: 2561c911b9b542a7b143fae745baf4e1de45be38
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 4%

---

# Modifica webhook

Puoi modificare i webhook esistenti. Gli scenari che utilizzano questi webhook utilizzeranno la nuova configurazione in futuro, eliminando la necessità di creare un nuovo webhook e di assegnarlo manualmente a tutti gli scenari interessati.

I webhook possono essere modificati solo per i seguenti connettori:

* Workfront
* Pianificazione Workfront

>[!IMPORTANT]
>
>Quando si aggiorna un webhook, considera quanto segue:
>
>* Il webhook modificato viene trattato dagli abbonamenti agli eventi di Workfront come un nuovo abbonamento. La cronologia delle sottoscrizioni degli eventi non viene mantenuta per la configurazione del webhook precedente, in quanto viene considerata una sottoscrizione di evento separata.
>* Il passaggio dalla sottoscrizione precedente a quella nuova potrebbe non essere sincronizzato perfettamente. È quindi possibile ricevere un evento due volte (se il nuovo abbonamento inizia a essere eseguito prima che quello vecchio si fermi) o perdere un evento (se il vecchio abbonamento si arresta prima che quello nuovo inizi a essere eseguito).

## Modificare un webhook

Puoi modificare i webhook da uno scenario o dall’elenco Webhook.

### Modificare un webhook in uno scenario

>[!NOTE]
>
>Questa funzionalità è disponibile solo per gli scenari che dispongono di un modulo di attivazione immediata di Workfront o Workfront Planning.

1. Vai allo scenario che include il webhook da modificare.
1. Nel modulo trigger dello scenario, fare clic sul menu a discesa accanto al campo Webhook e selezionare **Modifica elemento**.

   Viene visualizzata la finestra di configurazione del webhook, compilata con la configurazione esistente.

1. Apporta le modifiche desiderate al webhook.
1. Fai clic su **Salva** per salvare il webhook e tornare al modulo.

### Modificare un webhook dall&#39;elenco Webhook

1. Nel menu di navigazione a sinistra, seleziona **Webhook** ![icona Webhook](assets/webhooks-icon.png).
1. Fare clic sulla casella di controllo accanto al webhook che si desidera modificare.
1. Nel banner blu nella parte inferiore della schermata, fai clic su **Modifica**.
1. Apporta le modifiche desiderate al webhook.
1. Fai clic su **Salva** per salvare il webhook e tornare all&#39;elenco dei webhook.

