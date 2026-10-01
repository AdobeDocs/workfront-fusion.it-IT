---
title: Configurare il server Adobe Workfront Fusion MCP
description: Collegare Adobe Workfront Fusion a una piattaforma di intelligenza artificiale compatibile con MCP o a Coworker (standalone o nella barra a destra di Fusion).
source-git-commit: 5f3bd6b7b8837632af245ea2c172205625e4ecba
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 0%
---

# Configurare il server Adobe Workfront Fusion MCP

Il server Adobe Workfront Fusion MCP consente di lavorare con gli scenari, le esecuzioni, le connessioni, i webhook, gli archivi dati della tua organizzazione Fusion e molto altro ancora, attraverso una conversazione in linguaggio naturale in una piattaforma di intelligenza artificiale supportata.

Per un elenco degli strumenti disponibili nel server Adobe Workfront Fusion MCP, vedere [Strumenti server Adobe Workfront Fusion MCP](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

## Piattaforme di IA agente supportate

Il server MCP di Fusion funziona con qualsiasi piattaforma di intelligenza artificiale che supporta i server MCP (Model Context Protocol) e MCP remoti (Streamable HTTP) con OAuth.

>[!NOTE]
>
> Al momento Adobe non pubblica un connettore Workfront Fusion nella directory dei connettori Claude o nella directory dell’app/plug-in ChatGPT. Per utilizzare Fusion con Claude, ChatGPT o Microsoft Copilot, aggiungilo come **server MCP personalizzato** tramite URL, come descritto in questo articolo.

Questo articolo illustra i passaggi di connessione per:

* [Adobe Coworker](#use-fusion-with-coworker): Collaboratore come autonomo e Collaboratore nella barra a destra di Fusion
* [Claude](#connect-fusion-to-claude): connettore personalizzato
* [ChatGPT](#connect-fusion-to-chatgpt): server MCP personalizzato
* [Una soluzione MCP personalizzata](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>Se utilizzi una piattaforma compatibile con MCP diversa, ad esempio Gemini, Cursor o VS Code, segui la documentazione di tale piattaforma per aggiungere un server MCP personalizzato. Quando viene richiesto l&#39;URL del server MCP, immetti:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Prerequisiti

Prima di poter collegare Fusion a una piattaforma di intelligenza artificiale, è necessario:

* Disporre di una licenza Adobe Workfront Fusion attiva e avere accesso ad almeno un’organizzazione Fusion.
* Avere un ruolo utente e ruoli team di Fusion che concedano l’accesso ai dati che desideri utilizzare.
* Accedi con un Adobe ID (Adobe Identity Management System, IMS).
* Avere accesso a una piattaforma agente di intelligenza artificiale compatibile con MCP o a Coworker.

## Utilizzare Fusion con il collaboratore

Collaboratore è l’agente di intelligenza artificiale di Adobe. Fusion è integrato in Coworker, quindi non è necessario immettere un URL MCP o registrare un’app OAuth. È possibile utilizzare Collaboratore con Fusion in due posizioni:

* [Collaboratore (autonomo)](#use-fusion-in-coworker): collabora con Fusion insieme alle altre app Adobe.
* [Collaboratore nella barra a destra di Fusion](#use-coworker-in-the-fusion-right-rail): apri Collaboratore in un pannello all’interno dell’interfaccia utente di Fusion.

Entrambi utilizzano gli stessi strumenti MCP di Fusion, l’Adobe ID e le autorizzazioni di Fusion. Le impostazioni degli strumenti MCP di lettura o scrittura si applicano a entrambi. Le azioni distruttive, come l’eliminazione, la cancellazione della coda o la sovrascrittura, richiedono sempre una conferma.

### Utilizzare Fusion in Collaborator

1. Apri Collaboratore.
2. Apri **Personalizzazione** > **Integrazioni**
3. Trova **fusion-mcp** e fai clic su **Test**.
4. Se hai accesso a più organizzazioni di Fusion, questa verrà selezionata automaticamente. Se necessario, puoi chiedere a Collaboratore di cambiare organizzazione in un secondo momento.

### Utilizzare Collaboratore nella barra a destra di Fusion

In Fusion, Collaboratore si apre nella barra a destra

1. Accedere a Workfront Fusion.
2. Fai clic sull&#39;icona **Collaboratore** nella barra a destra.
3. Poni una domanda nel pannello.

### Esempi di prompt

* *Mostra tutti gli scenari che non sono stati eseguiti nelle ultime 24 ore.*
* *Elenca tutti gli scenari creati o eliminati questa settimana, ordinati in base al più recente.*
* *Funzionamento di questo scenario*
* *Perché l&#39;esecuzione non è riuscita?*

## Connect Fusion a Claude

Aggiungere Fusion come connettore personalizzato.

>[!NOTE]
>
> In Claude Team/Enterprise, per aggiungere un connettore personalizzato è necessario essere un proprietario. Per informazioni, vedere [Introduzione ai connettori personalizzati utilizzando MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) remoto nella documentazione di Claude.

1. Accedi a [Claude](https://claude.ai).
2. Nel menu a sinistra, seleziona **Personalizza**.
3. Seleziona **Connettori**.
4. Seleziona **+**, quindi **Aggiungi connettore personalizzato**.
5. Immetti un nome (ad esempio, &quot;Workfront Fusion&quot;) e l’URL del server MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

6. Fai clic su **Connetti**.
7. Accedi. Selezionare un profilo e un&#39;organizzazione Fusion.

Per Claude Code, puoi aggiungere il server dalla riga di comando:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Connetti Fusion a ChatGPT

Aggiungere Fusion come server MCP personalizzato.

### ChatGPT Desktop o Codex

1. In ChatGPT aprire **Impostazioni**.
2. Fare clic su **Plug-in**.
3. Fare clic su **Aggiungi server**.
4. Immettere un nome per il server.
5. Per il tipo, selezionare **HTTP semplificabile**.
6. Immettere l&#39;URL del server MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

7. Fai clic su **Salva**.
8. Fare clic su **Autentica** per il nuovo server e accedere.
9. Verificare che l&#39;interruttore accanto al server sia attivato.

### ChatGPT sul web

1. Accedi a [ChatGPT](https://chatgpt.com).
2. Vai a [https://chatgpt.com/plugins](https://chatgpt.com/plugins). La modalità Sviluppatore potrebbe dover essere attivata in **Impostazioni**; nei piani aziendali/aziendali, un amministratore deve consentire connettori personalizzati.
3. Fare clic su **+**.
4. Immetti un **Nome**.
5. Per **Connessione**, selezionare **URL server** e immettere l&#39;URL del server MCP.
6. Lascia **Authentication** impostato su **OAuth**.
7. Leggi il messaggio di rischio e seleziona la casella di controllo.
8. Fai clic su **Crea**, quindi accedi con il tuo.

## Connessione di Fusion a una soluzione MCP personalizzata

Se si sta creando un&#39;applicazione o un agente personalizzato, connettersi direttamente al server Fusion MCP.

## Passare a un&#39;organizzazione Fusion diversa

Non è necessario disconnettersi per cambiare le organizzazioni. Il server MCP di Fusion può cambiare l’organizzazione attiva all’interno di una sessione:

* _Di quali organizzazioni di Fusion si dispone?_
* _Passa all&#39;organizzazione 1234._

L&#39;agente utilizza `fusion_orgs_list` e `fusion_orgs_set`. Il parametro si applica solo alla conversazione/sessione corrente. Le organizzazioni in diverse aree del centro dati (ad esempio, Stati Uniti e Unione Europea) sono tutte disponibili attraverso lo stesso URL MCP.

## Risoluzione dei problemi di configurazione e autenticazione

| Problema | Probabile causa | Correggi |
| --- | --- | --- |
| Non è possibile trovare un connettore Fusion nella directory Claude o ChatGPT. | Adobe non pubblica un connettore di directory per Fusion. | Aggiungi Fusion come server MCP personalizzato utilizzando l’URL riportato in questo articolo. |
| Non puoi aggiungere un connettore personalizzato in Claude o ChatGPT. | Il piano limita i connettori personalizzati ai proprietari o agli amministratori. | Chiedi all’amministratore Claude o ChatGPT di aggiungere il connettore o consentire server MCP personalizzati. |
| Ti sei connesso ma non vedi dati o dati errati. | L&#39;organizzazione Fusion errata è attiva. | Chiedi all&#39;agente di elencare le tue organizzazioni e di passare a quella giusta. |
| Autenticazione non riuscita o connessione interrotta. | Sessione scaduta o errore di connessione. | Disconnettere e riconnettere il server. |
| Viene visualizzato un messaggio che informa che l’accesso MCP è disabilitato. | L&#39;accesso MCP è disattivato per l&#39;organizzazione Fusion. | Chiedere all&#39;amministratore di Fusion di attivarla. |
| L&#39;agente può leggere gli scenari ma non può crearli, eseguirli, aggiornarli o eliminarli. | Gli strumenti di scrittura MCP sono disabilitati o il ruolo del team non lo consente. | Chiedi all’amministratore di Fusion di abilitare gli strumenti di scrittura o di assegnarti il ruolo di team richiesto. |
| Autenticazione app personalizzata rifiutata. | L&#39;URL di richiamata non è incluso nell&#39;elenco delle autorizzazioni. | Chiedi all&#39;amministratore di aggiungere l&#39;URL di callback esatto. |
| Fusion non è elencato in Collaborator o Coworker non è presente nella barra a destra di Fusion. | Funzione non abilitata per la tua organizzazione. <!-- BECKY CHECK ME: confirm whether this is the correct admin guidance before publishing. --> | Contattare l&#39;amministratore di Fusion. |

## Domande frequenti

### Esiste un connettore Fusion ufficiale per Claude o ChatGPT?

Al momento non è possibile. Utilizza l’URL del server MCP personalizzato. Per il collaboratore (indipendente e nella barra a destra di Fusion) Fusion è stato integrato.

### È possibile utilizzare più organizzazioni di Fusion?

Sì. È possibile cambiare organizzazione attiva durante una conversazione senza riconnettersi.

### Cosa può fare l&#39;agente per mio conto?

L’agente agisce come te, utilizzando il tuo ruolo Fusion e le autorizzazioni del team. Non può accedere a nulla a cui non puoi accedere in Fusion. Le azioni distruttive richiedono una conferma esplicita.

### L&#39;agente visualizza i segreti di connessione?

No. Gli strumenti di connessione e chiave restituiscono metadati (nome, tipo, ambiti, scadenza), non credenziali o valori segreti.

