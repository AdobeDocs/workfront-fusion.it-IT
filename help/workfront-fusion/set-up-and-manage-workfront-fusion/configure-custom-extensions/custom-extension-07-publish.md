---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Pubblicare l’estensione personalizzata
description: Pubblicare l’estensione personalizzata
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 1%

---

# Pubblicare l’estensione personalizzata

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

L&#39;estensione viene eseguita in Fusion solo dopo che è stata **generata**, **distribuita** in Adobe e **approvata** per la tua organizzazione. Le procedure in questa pagina mostrano come pubblicare l’estensione e come verificare il risultato.

Queste informazioni sono tratte dalla documentazione ufficiale di Adobe e si applicano in modo specifico a Workfront Fusion. Per informazioni generali su Adobe, consulta [Flusso di sviluppo delle estensioni dell&#39;interfaccia utente](https://developer.adobe.com/uix/docs/guides/development-flow/) e [Gestione estensioni dell&#39;interfaccia utente](https://developer.adobe.com/uix/docs/guides/publication/) nella documentazione di Adobe.

## Aree di lavoro

Ogni progetto App Builder ha un&#39;area di lavoro **Stage** e un&#39;area di lavoro **Produzione**. Considerali come ambienti:

* **Stage** è per sviluppo e test. Distribuisci qui durante l’iterazione. Non è richiesta alcuna approvazione e il risultato è visibile solo attraverso l’interruttore di prova dello staging descritto di seguito (o l’anteprima locale).
* **Produzione** è per il rilascio a tutti. Dopo la distribuzione in produzione, invii una **richiesta di approvazione** e, una volta approvata, l&#39;estensione viene registrata nel Registro di sistema dell&#39;app Adobe e mostrata all&#39;intera organizzazione.

>[!NOTE]
>
> **Per la creazione e la distribuzione di** è necessario il ruolo **Sviluppatore**. Per inviare la richiesta di approvazione per la pubblicazione è necessario il ruolo **Amministratore di sistema**.
>Per ulteriori informazioni, consulta:
>
> * [Configurare gli strumenti e l&#39;account dell&#39;estensione dell&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * [Come ottenere l&#39;accesso](https://developer.adobe.com/uix/docs/guides/get-access/) nella documentazione Adobe.

Per impostazione predefinita, Fusion mostra solo **estensioni pubblicate**. Si tratta di estensioni distribuite nell&#39;area di lavoro **Produzione** e quindi inviate per l&#39;approvazione ****. Questa è l’impostazione predefinita sicura, pertanto una distribuzione work-in-progress non viene mai visualizzata per errore nell’intera organizzazione.

Una distribuzione nell&#39;area di lavoro **Stage** non è pubblicata, pertanto non viene visualizzata in Fusion. Puoi provare un’estensione in due modi prima di pubblicarla:

* **Anteprima locale** con `aio app run` (vedi [Anteprima locale delle estensioni dell&#39;interfaccia utente](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) nella documentazione di Adobe). Non viene distribuito nulla e solo tu lo vedi.
* **Caricalo dallo stage all&#39;interno di Fusion** attivando un&#39;opzione di test per utente nel tuo profilo di Fusion. Questo è descritto in [Testare una build della fase in Fusion](#test-a-stage-build-in-fusion) in questo articolo.

## Testare una build di staging in Fusion

Utilizzare questo flusso per visualizzare una distribuzione di staging in Fusion prima di pubblicarla.

### Passaggio 1: selezionare l&#39;area di lavoro dello stage

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Passaggio 2: generare

```sh
aio app build
```

In questo modo viene compilato il front-end e viene eseguito l&#39;hook dei metadati (che genera `app-metadata.json`). Correggi eventuali errori segnalati prima di continuare.

### Passaggio 3: distribuire

```sh
aio app deploy
```

`deploy` esegue due operazioni:

* **Ospita la tua interfaccia utente** nella rete di distribuzione dei contenuti di Adobe, in un URL come `https://<project>-stage.adobeio-static.net`. Al termine, CLI stampa l&#39;**URL dell&#39;endpoint dell&#39;estensione**. Questo è l’URL che Fusion carica nel suo iframe.
* **Registra gli endpoint dell&#39;estensione** per il punto di estensione (`fusion/nav-organization/1`) nell&#39;area di lavoro di staging.

>[!TIP]
>
> **Se la distribuzione non riesce con &quot;Il punto di estensione &#39;fusion/nav-organization/1&#39; non esiste&quot; (errore 1060):** il punto di estensione Fusion non è ancora abilitato per la tua organizzazione. Questo è un passaggio di onboarding, non un errore nel codice.
>Per ulteriori informazioni, vedere [Il punto di estensione non esiste](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist) nell&#39;articolo sulla risoluzione dei problemi.

### Passaggio 4: attivare il test dello staging nel profilo di Fusion

Fusion carica le estensioni Stage solo quando si dà il consenso, per utente:

1. Accedi a Fusion con un account nella **stessa organizzazione** a cui hai eseguito la distribuzione.
1. Apri il menu dell&#39;avatar utente nell&#39;angolo superiore e vai a **Impostazioni prodotto** > **Profilo di Fusion** > **Preferenze**.
1. Attiva l&#39;opzione **Estensioni stage**.

   Fusion richiede di ricaricare.
1. Conferma il ricaricamento.

Dopo il ricaricamento, Fusion carica le estensioni dall&#39;area di lavoro dello stage anziché dal set pubblicato e assegna a ciascuna un&#39;etichetta **(Stage)** nell&#39;area di navigazione per distinguerle.

Si tratta di un&#39;impostazione di test personali memorizzata nel browser, non di un&#39;impostazione dell&#39;organizzazione. Disattivala (e ricaricala) per tornare alle estensioni pubblicate. Poiché è memorizzato localmente, non vi segue in un altro browser o computer.

### Passaggio 5: verifica in Fusion

1. Apri la sezione che corrisponde al punto di estensione:
   * `fusion/nav-organization/1` → l&#39;area **Organizzazione** della navigazione a sinistra.
   * `fusion/nav-team/1` →&#39;area **Team** (selezionare prima un team).

   Viene visualizzato un pulsante con il titolo impostato in `getWidget()`, contrassegnato **(Stage)**.
1. Fai clic sul pulsante visualizzato.

L&#39;interfaccia utente carica e riceve il [contesto Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Se il pulsante non viene visualizzato o se nel pannello viene visualizzato un errore, vedere [Risoluzione dei problemi](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Rilascio in produzione

Quando l’estensione funziona su Stage e sei pronto per tutti gli utenti:

### Passaggio 1: passare all’area di lavoro di produzione

```sh
aio console workspace select       # choose Production
```

Quando la CLI richiede informazioni sul file `.env`, seleziona **Unisci** per mantenere le variabili di ambiente.

### Passaggio 2: generare e distribuire in produzione

```sh
aio app build
aio app deploy
```

### Passaggio 3: sottomettere la richiesta di approvazione

La pubblicazione è una **richiesta di approvazione inviata dall&#39;area di lavoro di produzione**:

1. Apri [Adobe Developer Console](https://developer.adobe.com/console), seleziona la tua **organizzazione**, apri il tuo **progetto** e passa all&#39;area di lavoro **Produzione**.
1. Invia l&#39;app per **approvazione/pubblicazione** (richiede il ruolo di **amministratore di sistema**).
1. Dopo l&#39;approvazione, l&#39;estensione viene aggiunta al **Registro app Adobe** e diventa disponibile in [Adobe Experience Cloud](https://experience.adobe.com), incluso Fusion, per la tua organizzazione.

Per istruzioni dettagliate, consulta [Gestione estensioni interfaccia utente](https://developer.adobe.com/uix/docs/guides/publication/) nella documentazione di Adobe Developer.

## Stato e aggiornamenti

Vale la pena conoscere alcuni comportamenti, in modo da poter distinguere &quot;ci stai ancora lavorando&quot; da &quot;qualcosa non va&quot;:

* **Distribuito in produzione non è lo stesso di visibile.** `aio app deploy` in Produzione carica l&#39;app, ma l&#39;estensione non viene visualizzata. Viene visualizzato solo dopo l’invio e l’approvazione della richiesta di approvazione. Se è stato implementato in Produzione e non viene ancora visualizzato in Fusion, il motivo comune è che non è ancora stato approvato.
* **Non è necessaria una nuova approvazione per gli aggiornamenti solo codice.** Se l’estensione è già pubblicata e ne modifichi solo il codice (l’interfaccia utente o le azioni di runtime), ridistribuisci allo stesso URL con:

  ```sh
  aio app deploy --force-deploy
  ```

  Gli utenti ricevono la nuova versione alla successiva apertura dell’estensione. Nessun elemento da installare. È sufficiente inviare una nuova richiesta di approvazione quando si modifica la **registrazione** stessa, ad esempio aggiungendo un nuovo punto di estensione o modificando gli annunci di `getWidget()`.
* **Un&#39;estensione revocata o ritirata scompare.** Se un’estensione viene revocata o ritirata dall’utente, non viene più visualizzata in Fusion senza alcun messaggio di errore. Se un&#39;estensione funzionante in precedenza scompare per tutti, verifica se è stata revocata prima di cercare un problema di codice.

## Rimuovere (revocare) un’estensione

La rimozione di un&#39;estensione pubblicata viene eseguita **revocandola** in Adobe Exchange:

1. Accedi a **Adobe Exchange**.
1. Vai a **Gestisci** > **App App Builder**.
1. Seleziona **Revoca** accanto all&#39;estensione da rimuovere e conferma.

Dopo la revoca, l&#39;estensione mostra uno stato *revoked* in Extension Manager e non viene più visualizzata in Fusion. Per rimuoverlo completamente, elimina il progetto in Developer Console. Un progetto non può essere eliminato finché la sua estensione non viene revocata.

Per una distribuzione di test solo stage, è possibile rimuovere la distribuzione con:

```sh
aio app undeploy
```

## Risorse aggiuntive

Le seguenti risorse sono disponibili nella documentazione di Adobe:

* [Flusso di sviluppo delle estensioni dell&#39;interfaccia utente](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gestione delle estensioni dell’interfaccia utente (pubblicazione/approvazione/revoca)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Creazione di un progetto in Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [Come ottenere l’accesso (ruoli)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [Anteprima locale delle estensioni dell’interfaccia utente](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
