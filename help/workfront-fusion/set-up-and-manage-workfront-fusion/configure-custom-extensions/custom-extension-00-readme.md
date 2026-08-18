---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 'Estensioni UI personalizzate: indice dell''articolo'
description: Estensioni personalizzate in Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 3%

---


# Estensioni UI personalizzate: indice dell&#39;articolo

Fusion può visualizzare la tua interfaccia web all’interno della stessa. Puoi creare una piccola app web, denominata estensione, pubblicarla in Adobe e visualizzarla come pulsante nella navigazione di Fusion. Quando un utente fa clic su di essa, l’interfaccia utente si carica nell’area principale di Fusion e riceve automaticamente informazioni su chi ha effettuato l’accesso, in quale organizzazione e team lavora e altro ancora.

Questa sezione della documentazione di fusion illustra l’intero processo senza presupporre un’esperienza precedente con Adobe App Builder o con i framework front-end. Comprende anche il codice necessario, insieme alle relative spiegazioni.

## Quando utilizzare questa guida

Utilizzate questa guida per aggiungere una schermata o uno strumento personalizzato a Fusion. Non è necessario essere uno sviluppatore esperto. È necessario avere familiarità con la copia dei comandi in un terminale e la modifica di alcuni file di testo.

Per creare un’estensione dell’interfaccia utente personalizzata, è necessario disporre di un Adobe ID e di un accesso a un’organizzazione Adobe (lo stesso tipo di accesso che si utilizza per accedere a Fusion).

## Cosa verrà creato

Al termine di questa guida avrai:

1. Un progetto Adobe **App Builder** gratuito. Qui è dove vive la tua estensione.
1. Una piccola app web che esegue il rendering dell’interfaccia utente personalizzata.
1. L’app web si è connessa a uno dei punti di estensione di Fusion in modo che venga visualizzata nella navigazione di Fusion.
1. L’interfaccia utente legge il contesto live da Fusion, ad esempio l’utente corrente, l’organizzazione e il team, e reagisce quando l’utente cambia organizzazione o team.
1. L’estensione pubblicata in modo che possa essere visualizzata da altri utenti dell’organizzazione.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## Sommario

Leggi le pagine in ordine la prima volta. Successivamente puoi passare direttamente a quello di cui hai bisogno.

| # | Pagina | Cosa copre |
| --- | ------ | ---------------- |
| 1 | [Panoramica e concetti chiave](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | Il vocabolario, l&#39;architettura e lo scopo di ciascun punto di estensione di Fusion. |
| 2 | [Configura i tuoi strumenti e l&#39;account Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, Adobe I/O CLI, accesso e creazione del progetto in Adobe Developer Console. |
| 3 | [Crea il progetto e configuralo per Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | Genera un progetto App Builder generico con la riga di comando `aio` (non un modello specifico per il prodotto). Quindi, puntare il progetto a un punto di estensione Fusion e registrare il widget. |
| 5 | [Generare l&#39;interfaccia utente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | Esegui il rendering della schermata personalizzata e completa la connessione (&quot;handshake&quot;) con Fusion. |
| 6 | [Riferimento al contesto di Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | Ogni campo che Fusion invia, cosa significa e come reagire ai cambiamenti. |
| 7 | [Pubblica la tua estensione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Genera, distribuisci e rendi visibile l’estensione in Fusion. |
| 8 | [Risoluzione dei problemi](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | Correzioni per gli errori più comuni. |
| 9 | [Procedura dettagliata per la demo](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | Uno script lineare di copia e incolla: scaffold dal modello generico di Experience Cloud Shell → il retargeting a Fusion → la distribuzione nell’ambiente di staging → l’esecuzione in Fusion. Ideale per una demo dal vivo. |
| 10 | [Chiamata delle API Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | Chiama le API back-end dall’estensione senza premere CORS del browser, utilizzando un proxy runtime-action. Include `require-adobe-auth`, intestazioni Fusion v3 e un esempio elaborato. |

## Nota sulla disponibilità

Fusion attualmente espone i seguenti punti di estensione:

* `fusion/nav-organization/1` — viene visualizzato nella sezione **Organizzazione**.
* `fusion/nav-team/1` — viene visualizzato nella sezione **Team**.

Prima di poter pubblicare su uno di questi, è necessario eseguire l’onboarding del punto di estensione per la tua organizzazione Adobe. Se il passaggio di pubblicazione non riesce e il punto di estensione &quot;non esiste&quot;, vedi [Risoluzione dei problemi](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Documentazione ufficiale di Adobe

Questa guida è specifica per Fusion. Per la piattaforma sottostante, i riferimenti canonici sono:

* [Panoramica sull’estensibilità dell’interfaccia utente](https://developer.adobe.com/uix/docs/)
* [Flusso di sviluppo delle estensioni dell&#39;interfaccia utente](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gestione delle estensioni dell’interfaccia utente (pubblicazione/approvazione/revoca)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Guida introduttiva di Adobe App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
