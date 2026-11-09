---
title: Configurare il server Adobe Workfront Fusion MCP
description: Collegare Adobe Workfront Fusion a una piattaforma di intelligenza artificiale compatibile con MCP o a Coworker (standalone o nella barra a destra di Fusion).
source-git-commit: d5861015b3bb0e9c176fcf4fd71db426671764dd
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 7%
---

# Configurare il server Adobe Workfront Fusion MCP

Il server Adobe Workfront Fusion MCP consente di lavorare con gli scenari, le esecuzioni, le connessioni, i webhook, gli archivi dati della tua organizzazione Fusion e molto altro ancora, attraverso una conversazione in linguaggio naturale in una piattaforma di intelligenza artificiale supportata.

Per un elenco degli strumenti disponibili nel server Adobe Workfront Fusion MCP, vedere [Strumenti server Adobe Workfront Fusion MCP](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisiti

Prima di poter collegare Fusion a una piattaforma di intelligenza artificiale, è necessario:

* Disporre di una licenza Adobe Workfront Fusion attiva e avere accesso ad almeno un’organizzazione Fusion.
* Avere un ruolo utente e ruoli team di Fusion che concedano l’accesso ai dati che desideri utilizzare.
* Accedi con un Adobe ID (Adobe Identity Management System, IMS).
* Avere accesso a una piattaforma agente di intelligenza artificiale compatibile con MCP o a Coworker.

## Applicazioni MCP supportate

Il server Fusion MCP funziona con le seguenti applicazioni.

**Applicazioni chat**

* Claude antropico
* OpenAI ChatGPT
* Copilota Microsoft 365

**Strumenti per sviluppatori**

* Codice Claude antropico
* Cursore
* Copilota GitHub
* Codice VS
* Codice OpenAI
* MCP Inspector, mcp-remote e altri strumenti che utilizzano un callback locale

**Piattaforme di automazione e IA**

* Adobe Workfront Fusion
* Ricerca IA vertice Google
* Glean
* Writer AI Studio
* Postman

### Limitazioni

* Solo le applicazioni elencate in questa sezione possono connettersi al server MCP di Fusion.
* Le app desktop e le interfacce della riga di comando (CLI) funzionano se ricevono il callback di accesso nel computer in uso (`localhost`).
* Non è possibile aggiungere applicazioni personalizzate. Per richiedere il supporto per una nuova applicazione, contattare il team di Fusion all&#39;indirizzo [fusiondev@adobe.com](mailto:fusiondev@adobe.com).

<!-- BECKY CHECK ME: Other parts of this article might conflict with these limitations. See the comments in the important note below, in the section Connect Fusion to a custom MCP solution, and in the troubleshooting table. -->

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
>Se utilizzi una piattaforma compatibile con MCP diversa, segui la relativa documentazione per aggiungere un server MCP personalizzato. Quando viene richiesto l&#39;URL del server MCP, immetti:
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Utilizzare Fusion con il collaboratore

Collaboratore è l’agente di intelligenza artificiale di Adobe. Fusion è integrato in Coworker, quindi non è necessario immettere un URL MCP o registrare un’app OAuth. È possibile utilizzare Collaboratore con Fusion in due posizioni:

* Collaboratore (autonomo): puoi lavorare con Fusion insieme alle altre app Adobe.
* Collaboratore nella barra a destra di Fusion: apri Collaboratore in un pannello all’interno dell’interfaccia utente di Fusion.

Entrambi utilizzano gli stessi strumenti MCP di Fusion, l’Adobe ID e le autorizzazioni di Fusion. Le impostazioni degli strumenti MCP di lettura o scrittura si applicano a entrambi. Le azioni distruttive, come l’eliminazione, la cancellazione della coda o la sovrascrittura, richiedono sempre una conferma.

### Utilizzare Fusion in Collaborator

1. Apri Collaboratore. Puoi trovarlo all’indirizzo https://experience.adobe.com/#/coworker.
1. Apri **personalizzazioni** > **integrazioni**
1. Cercare o individuare **fusion-mcp** e fare clic su di esso.
1. Nella finestra visualizzata, fare clic su **Test**.
1. Se hai accesso a più organizzazioni di Fusion, questa verrà selezionata automaticamente. Se necessario, puoi chiedere a Collaboratore di cambiare organizzazione in un secondo momento.

### Utilizzare Collaboratore nella barra a destra di Fusion

In Fusion, Collaboratore si apre nella barra a destra

1. Accedere a Workfront Fusion.
1. Fai clic sull&#39;icona **Collaboratore** nella barra a destra.
1. Poni una domanda nel pannello.

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
1. Nel menu a sinistra, seleziona **Personalizza**.
1. Seleziona **Connettori**.
1. Seleziona **+**, quindi **Aggiungi connettore personalizzato**.
1. Immetti un nome (ad esempio, &quot;Workfront Fusion&quot;) e l’URL del server MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Fai clic su **Connetti**.
1. Accedi. Selezionare un profilo e un&#39;organizzazione Fusion.

Per Claude Code, puoi aggiungere il server dalla riga di comando:

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Connetti Fusion a ChatGPT

Aggiungere Fusion come server MCP personalizzato.

### ChatGPT Desktop o Codex

1. In ChatGPT aprire **Impostazioni**.
1. Fare clic su **Plug-in**.
1. Fare clic su **Aggiungi server**.
1. Immettere un nome per il server.
1. Per il tipo, selezionare **HTTP semplificabile**.
1. Immettere l&#39;URL del server MCP:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. Fai clic su **Salva**.
1. Fare clic su **Autentica** per il nuovo server e accedere.
1. Verificare che l&#39;interruttore accanto al server sia attivato.

### ChatGPT sul web

1. Accedi a [ChatGPT](https://chatgpt.com).
1. Vai a [https://chatgpt.com/plugins](https://chatgpt.com/plugins). La modalità Sviluppatore potrebbe dover essere attivata in **Impostazioni**; nei piani aziendali/aziendali, un amministratore deve consentire connettori personalizzati.
1. Fare clic su **+**.
1. Immetti un **Nome**.
1. Per **Connessione**, selezionare **URL server** e immettere l&#39;URL del server MCP.
1. Lascia **Authentication** impostato su **OAuth**.
1. Leggi il messaggio di rischio e seleziona la casella di controllo.
1. Fai clic su **Crea**, quindi accedi con il tuo.

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
| Fusion non è elencato in Collaborator o Coworker non è presente nella barra a destra di Fusion. | Funzione non abilitata per la tua organizzazione. | Contattare l&#39;amministratore di Fusion. |

## Domande frequenti

### Esiste un connettore Fusion ufficiale per Claude o ChatGPT?

Al momento non è possibile. Utilizza l’URL del server MCP personalizzato. Per il collaboratore (indipendente e nella barra a destra di Fusion) Fusion è stato integrato.

### È possibile utilizzare più organizzazioni di Fusion?

Sì. È possibile cambiare organizzazione attiva durante una conversazione senza riconnettersi.

### Cosa può fare l&#39;agente per mio conto?

L’agente agisce come te, utilizzando il tuo ruolo Fusion e le autorizzazioni del team. Non può accedere a nulla a cui non puoi accedere in Fusion. Le azioni distruttive richiedono una conferma esplicita.

### L&#39;agente visualizza i segreti di connessione?

No. Gli strumenti di connessione e chiave restituiscono metadati (nome, tipo, ambiti, scadenza), non credenziali o valori segreti.

