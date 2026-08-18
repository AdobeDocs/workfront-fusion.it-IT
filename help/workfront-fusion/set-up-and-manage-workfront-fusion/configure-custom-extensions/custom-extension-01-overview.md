---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Panoramica sull’estensibilità dell’interfaccia utente
description: Estensioni personalizzate in Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 835
ht-degree: 0%

---

# Panoramica sull’estensibilità dell’interfaccia utente

L’estensibilità dell’interfaccia utente consente di inserire in Adobe Workfront Fusion la logica e l’interfaccia utente personalizzate (interfaccia utente). Utilizzando Adobe App Builder, puoi modificare l’esperienza di Workfront Fusion della tua organizzazione per soddisfare al meglio le sue esigenze, pur affidandoti sempre alle funzionalità di base di Fusion.

Questo articolo offre una panoramica dell’estensibilità dell’interfaccia utente e del modo in cui l’estensione personalizzata comunica con Workfront Fusion.

## Struttura delle estensioni

* [Host e ospiti](#hosts-and-guests)
* [La tecnologia sottostante](#the-technology-underneath)

### Host e ospiti

Fusion può visualizzare un’interfaccia utente che non è stata creata dal team di Workfront Fusion. Per garantire che queste modifiche non influiscano sulla funzionalità di base di Fusion, l&#39;interfaccia utente viene eseguita nel proprio frame del browser isolato (un `<iframe>`), completamente separato dal codice di Fusion.

* **Host**: applicazione che *contiene* l&#39;estensione. In questo caso è **Fusion**. L&#39;host decide dove possono apparire le estensioni e quali dati condividere con loro.
* **Guest**: *La tua estensione*. Si tratta di una piccola applicazione web che l’host carica in un iframe.

Quando crei un’estensione dell’interfaccia utente, non modifichi Fusion. Puoi creare e pubblicare un guest, che Fusion può utilizzare dopo la pubblicazione del guest.

### La tecnologia sottostante

Il tuo ospite è stato creato con due tecnologie Adobe:

* **Adobe App Builder**: piattaforma di hosting e strumenti gratuita per piccole app Web e azioni senza server. L&#39;estensione è un&#39;app App Builder. App Builder consente di ospitare l&#39;interfaccia utente (nella rete di distribuzione dei contenuti `*.adobeio-static.net` di Adobe) e uno strumento da riga di comando denominato `aio` per crearlo, generarlo e pubblicarlo.
* **Adobe UI Extensibility SDK (UIX)**: librerie che consentono all&#39;host e al guest di comunicare. Verrà utilizzato un pacchetto, `@adobe/uix-guest`, al tuo fianco. Fusion utilizza il pacchetto `@adobe/uix-host` corrispondente sul suo lato.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## Punti di estensione

Un punto di estensione è uno &quot;slot&quot; denominato nell&#39;host in cui è consentito visualizzare un ospite. Fusion ne definisce gli slot e scegli quale usare per il guest.

Il nome di un punto di estensione è composto da tre parti: `service/name/version`.

Fusion offre i seguenti punti di estensione:

| Punto di estensione | Dove viene visualizzata l’interfaccia utente in Fusion | Quando utilizzarlo |
| --- | --- | ---- |
| `fusion/nav-organization/1` | Nella sezione **Organizzazione** della navigazione a sinistra. | Il tuo strumento riguarda l&#39;intera organizzazione. |
| `fusion/nav-team/1` | Nella sezione **Team** della barra di navigazione a sinistra (visualizzata quando è selezionato un team). | Il tuo strumento riguarda un team specifico. |

* `fusion` è il **servizio** (il prodotto, Fusion).
* `nav-organization` / `nav-team` è il **nome** (lo slot specifico).
* `1` è la **versione**.

Un’estensione può implementare uno o entrambi i punti di estensione. La maggior parte delle estensioni utilizza un punto.

In base al punto di estensione selezionato, Fusion aggiunge un pulsante con il titolo dell&#39;estensione alla sezione di navigazione corrispondente. Facendo clic su di essa si apre una pagina dedicata nell’area del contenuto principale di Fusion, dove viene caricata l’interfaccia utente.

## Frame inclusi in un&#39;estensione dell&#39;interfaccia utente

>[!IMPORTANT]
>
>Questa sezione descrive un aspetto delle estensioni dell’interfaccia utente che può causare confusione. Consigliamo di leggerlo attentamente.

Quando Fusion carica il guest, l&#39;estensione viene eseguita in **due** frame:

1. **Frame di registrazione (invisibile).** Viene eseguito per primo, in background. Il frame di registrazione indica a Fusion cosa offre la tua estensione. Ad esempio, potrebbe indicare che dispone di un widget del dashboard e inviare il titolo del widget e l’URL della relativa interfaccia utente. Il frame di registrazione esegue questa operazione chiamando `register(...)`. Non viene visualizzata alcuna interfaccia utente.
1. **Frame dell&#39;interfaccia utente (visibile).** Questa è la pagina che Fusion mostra all’utente. Deve annunciarsi all&#39;host chiamando `attach(...)`. Se non chiama mai `attach`, Fusion attende e alla fine scade con un errore.

>[!BEGINSHADEBOX]

Questo esempio mostra il flusso quando un utente fa clic sul pulsante di estensione.

1. Fai clic sul pulsante.
1. Fusion carica il riquadro REGISTRATION (nascosto).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()` restituisce l&#39;URL dell&#39;interfaccia utente visibile
1. Fusion carica il frame dell’interfaccia utente (visibile) in corrispondenza di tale URL.

   ```
   attach({ id }) 
   ```

   Questa operazione è obbligatoria oppure Fusion va in timeout
1. Fusion invia il contesto e i rendering dell’interfaccia utente.

>[!ENDSHADEBOX]

Entrambi i fotogrammi vengono scritti quando si crea l’interfaccia utente. È importante ricordare che la pagina visibile **deve** chiamare `attach`.

Per ulteriori informazioni sulla creazione dell&#39;interfaccia utente, vedere [Creare l&#39;interfaccia utente dell&#39;estensione personalizzata](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

## Contesto da Fusion

Dopo aver collegato l&#39;estensione, Fusion condivide un oggetto `context` con il tuo ospite. Contiene:

* **Utente**: il profilo Fusion dell&#39;utente connesso e l&#39;ID utente Adobe IMS.
* **Organizzazione**: il record completo dell&#39;organizzazione attiva Fusion e l&#39;ID organizzazione Adobe IMS.
* **Team**: il team attivo, se applicabile.
* **Token di accesso Adobe IMS**: chiama le API Adobe o Fusion per conto dell&#39;utente, se necessario.

Anche Fusion invia gli aggiornamenti. Ad esempio, se l’utente cambia organizzazione o team mentre l’interfaccia utente è aperta, Fusion invia il nuovo contesto in modo che l’interfaccia utente possa reagire immediatamente.

Per l&#39;elenco completo dei campi di contesto, vedere [Riferimento al contesto di Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Creazione di un’estensione dell’interfaccia utente

Per creare un’estensione dell’interfaccia utente, effettua le seguenti operazioni:

1. [Installare gli strumenti e creare un progetto Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [Generare un progetto App Builder vuoto, posizionarlo in un punto di estensione Fusion e registrare il widget](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [Creare l&#39;interfaccia utente e connettersi a Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Utilizza il contesto inviato da Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
1. [Pubblica in modo che Fusion possa trovarla](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (Facoltativo) [Chiama le API Workfront/Fusion per dati reali senza CORS](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

Per iniziare il processo, vai a [Configura i tuoi strumenti e l&#39;account Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


