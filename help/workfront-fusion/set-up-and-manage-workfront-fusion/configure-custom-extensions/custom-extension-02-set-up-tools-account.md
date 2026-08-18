---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Configurare gli strumenti e l’account dell’estensione dell’interfaccia utente
description: Configurare gli strumenti e l’account dell’estensione dell’interfaccia utente
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---


# Configurare gli strumenti e l’account dell’estensione dell’interfaccia utente

Prima di poter creare un’estensione dell’interfaccia utente per Workfront Fusion, è necessario configurare gli strumenti e l’account. Questo deve essere fatto solo una volta.

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

<!--Access requirements-->

## Prerequisiti

Per configurare gli strumenti e l’account di estensibilità dell’interfaccia utente, è necessario disporre dei seguenti elementi:

* **Adobe ID** con accesso a un&#39;organizzazione Adobe. Questo è l’account che utilizzi per accedere a Fusion.
* **Accesso sviluppatore ad App Builder.** L&#39;amministratore dell&#39;organizzazione potrebbe dover concedere il ruolo **Sviluppatore** e aggiungerti a un **profilo di prodotto** che include App Builder. Se in seguito i comandi non riescono e viene visualizzato il messaggio &quot;non sei uno sviluppatore&quot; o se non riesci a visualizzare la tua organizzazione, chiedi all’amministratore dell’organizzazione Adobe di aggiungerti.
* **Amministratore di sistema** <!--Adobe? Fusion?--> (probabilmente un altro membro del team) per il passaggio finale della versione. La creazione e la distribuzione richiedono solo il ruolo Sviluppatore, ma **l&#39;invio di un&#39;estensione per l&#39;approvazione/pubblicazione richiede il ruolo Amministratore di sistema**.

  Per ulteriori informazioni sui livelli di accesso ad Adobe, consulta
  [Come ottenere l&#39;accesso](https://developer.adobe.com/uix/docs/guides/get-access/) nella documentazione Adobe.

* **Computer in cui è possibile installare software** ed eseguire comandi terminali (macOS, Windows o Linux).

## Installare Node.js

Gli strumenti di Adobe vengono eseguiti su **Node.js**. È necessario installare la versione **LTS** (18 o 20).

1. Vai a <https://nodejs.org> e scarica il programma di installazione di **LTS**.
1. Eseguire il programma di installazione e accettare le impostazioni predefinite.
1. Confermare il funzionamento aprendo un terminale ed eseguendo:

   ```sh
   node --version
   npm --version
   ```

   Dovresti visualizzare i numeri di versione (ad esempio `v20.17.0` e `10.x`).

1. (Condizionale) Se `node` non viene trovato, chiudere e riaprire il terminale o riavviare il computer.

1. Continuare con [Installare Adobe I/O CLI (`aio`)](#install-the-adobe-io-cli-aio).

>[!TIP]
>
>* Se si utilizzano più versioni di Nodo, un gestore delle versioni come `nvm` è comodo, ma è facoltativo.
>* Adobe CLI richiede Node 18 o versione successiva. Versioni molto nuove, non-LTS possono occasionalmente causare problemi, quindi si consiglia di utilizzare LTS.

## Installa Adobe I/O CLI (`aio`)

Lo strumento da riga di comando utilizzato per creare, generare e pubblicare l&#39;estensione è denominato `aio`.

Per installarlo a livello globale:

1. Utilizza il seguente comando `npm` nella riga di comando.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. Conferma l’installazione utilizzando il seguente comando:

   ```sh
   aio --version
   ```

   Dovresti trovare qualcosa come `@adobe/aio-cli/11.x.x`.

1. Continua con [Accedi ad Adobe](#sign-in-to-adobe).

>[!NOTE]
>
> Se viene visualizzato un errore di autorizzazione in macOS/Linux, **non** utilizzare `sudo`. Correggi invece le autorizzazioni della cartella globale di npm oppure utilizza un gestore della versione del nodo che viene installato nella home directory.

## Accedere ad Adobe

1. Connetti CLI al tuo account Adobe con il seguente comando:

   ```sh
   aio login
   ```

1. Nella finestra del browser visualizzata, accedi con il tuo Adobe ID e approva l&#39;accesso.

1. Dopo aver effettuato l’accesso, chiudi la scheda del browser e torna al terminale.

1. (Facoltativo) Per disconnettersi in un secondo momento, ad esempio per cambiare account, utilizzare il comando: `aio logout`.
1. Continua con [Conferma l&#39;organizzazione attiva](#confirm-your-active-organization).

## Conferma l’organizzazione attiva

Verificare a quale organizzazione si rivolge l&#39;interfaccia CLI:

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

Se appartieni a più organizzazioni, seleziona quella corretta:

```sh
aio console org select
```

Ora puoi creare il progetto.
