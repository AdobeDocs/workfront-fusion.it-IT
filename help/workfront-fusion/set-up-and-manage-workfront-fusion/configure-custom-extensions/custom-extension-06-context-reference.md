---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Riferimento al contesto di Fusion
description: Riferimento al contesto di Fusion
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
source-wordcount: 757
ht-degree: 8%

---

# Riferimento al contesto di Fusion

>[!NOTE]
>
>Questo articolo presuppone una certa familiarità con gli strumenti di sviluppo software.

Quando l&#39;interfaccia utente chiama `attach(...)`, Fusion condivide un oggetto **context** che descrive la sessione corrente. Questa pagina elenca tutti i campi, il loro significato e la correlazione tra gli identificatori Fusion e Adobe IMS.

## Come leggere il contesto

* **Valori iniziali:** `connection.sharedContext.get("<key>")`
* **Aggiornamenti:** Ascolta l&#39;evento `contextchange`. L&#39;oggetto più recente arriva il `event.detail.context`.

Per il modello di codice completo, vedi [Creare l&#39;interfaccia utente dell&#39;estensione personalizzata](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Tasti di primo livello

| Chiave | Tipo | Descrizione |
| ----- | ------ | ------------- |
| `imsToken` | stringa | Il token di accesso Adobe **IMS dell&#39;utente connesso**. Utilizza questo token come `Bearer` per chiamare le API Adobe o Fusion per conto dell&#39;utente. **Poiché è sensibile, non registrarlo né visualizzarlo.** |
| `imsOrgId` | stringa | L&#39;organizzazione Adobe **IMS id**, nel formato `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | stringa | L&#39;ID utente Adobe **IMS** dell&#39;utente connesso. |
| `organization` | oggetto | **organizzazione Fusion attiva completa**. Per ulteriori informazioni, vedere [`organization` campi](#organization-fields) in questo articolo. |
| `team` | oggetto \| non definito | Il **team Fusion attivo completo**, quando uno è attivo (sempre rilevante per `fusion/nav-team/1`). Per ulteriori informazioni, vedere [`team` campi](#team-fields) in questo articolo. |
| `user` | oggetto | **utente Fusion con accesso completo**. Per ulteriori informazioni, vedere [`user` campi](#user-fields) in questo articolo. |

### ID Fusion e ID IMS

Ogni entità ha un **ID Fusion** (utilizzato dalle API di Fusion) e, laddove esiste, un **ID Adobe IMS** (utilizzato dalle API della piattaforma Adobe):

| Entità | ID fusione | ID Adobe IMS |
| -------- | ----------- | -------------- |
| Organizzazione | `organization.id` | `imsOrgId` (esposto anche come `organization.externalOrgId`) |
| Team | `team.id` | *(I team sono solo Fusion; nessun ID IMS)* |
| Utente | `user.id` | `imsUserId` |

## `organization` campi

Questi campi si trovano nel record organizzazione attivo. La maggior parte delle estensioni richiede solo `id`, `name` e gli identificatori.

| Campo | Tipo | Descrizione |
| ------- | ------ | ------------- |
| `id` | stringa | ID organizzazione Fusion. |
| `name` | stringa | Nome visualizzato organizzazione |
| `externalOrgId` | stringa | ID organizzazione Adobe IMS (stesso valore di `imsOrgId`). |
| `externalId` | stringa | Identificatore esterno utilizzato dalle integrazioni Fusion |
| `countryId` | stringa | ID impostazione paese. |
| `timezoneId` | stringa | ID impostazione fuso orario |
| `serviceName` | stringa | Identificatore servizio/piano |
| `teamIds` | stringa[] | ID dei team di questa organizzazione |
| `license` | oggetto | Limiti e autorizzazioni del piano, ad esempio operazioni, trasferimento dati, postazioni utente e flag di funzione |
| `scenariosCount` | numero | Scenari totali nell’organizzazione |
| `activeScenarios` | numero | Scenari attualmente attivi |
| `activeApps` | numero | Numero di app o connessioni attive |
| `operations`, `operationsExt` | numero | Contatori utilizzo operazioni |
| `transfer`, `transferExt` | numero | Contatori di utilizzo per il trasferimento dei dati |
| `isPaused` | booleano | Indica se l’organizzazione è in pausa |
| `isDeleted` | booleano | Indica se l’organizzazione è contrassegnata come eliminata |
| `imsEnabled` | booleano | Se l’organizzazione è collegata ad Adobe IMS |
| `usersCount` | numero | Numero di utenti nell’organizzazione |
| `nextReset` | string (date) | Quando i contatori di utilizzo verranno reimpostati. Visualizza [Date](#dates) |

## `team` campi

Questi campi sono presenti quando un team è attivo. È necessario fornire un fallback nel caso in cui il team sia `undefined` (ad esempio in una schermata a livello di organizzazione senza team selezionato).

| Campo | Tipo | Descrizione |
| ------- | ------ | ------------- |
| `id` | stringa | ID del team Fusion. |
| `name` | stringa | Nome visualizzato team. |
| `organizationId` | stringa | ID Fusion dell’organizzazione a cui appartiene il team. |
| `country` | stringa | Impostazione paese team. |
| `timezone` | stringa | Fuso orario del team. |
| `license` | oggetto | Limiti e adesioni a livello di team. |
| `activeScenarios` | numero | Scenari attivi nel team. |
| `activeApps` | numero | App o connessioni attive nel team. |
| `scenarioDrafts` | booleano | Indica se le bozze degli scenari sono abilitate. |
| `isDeleted` | booleano | Indica se il team è contrassegnato come eliminato. |
| `created` | string (date) | Data di creazione del team. Vedi [Date](#dates). |

## `user` campi

Questi campi si applicano all&#39;utente di Fusion connesso.

| Campo | Tipo | Descrizione |
| ------- | ------ | ------------- |
| `id` | stringa | ID utente di Fusion. |
| `name` | stringa | Nome completo. |
| `email` | stringa | Indirizzo e-mail. |
| `avatar` | stringa | URL immagine avatar. |
| `locale` | stringa | Impostazioni locali utente, ad esempio `en`. |
| `language` | stringa | Lingua preferita, se impostata. |
| `timezone` | stringa | Nome del fuso orario. |
| `timezoneId` | stringa | ID impostazione fuso orario. |
| `countryId` | stringa | ID impostazione paese. |
| `localeId` | stringa | ID impostazione lingua. |
| `features` | oggetto | Flag di funzionalità per utente (ad esempio `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | stringa | L’ID del ruolo di amministratore dell’utente, se applicabile. |

>[!NOTE]
>
> L&#39;oggetto `user` può includere campi interni aggiuntivi. Utilizza solo i campi qui documentati. Altri campi possono cambiare senza preavviso e alcuni campi correlati all’autenticazione non devono mai essere registrati o visualizzati.

## Date

Il contesto viene serializzato prima che raggiunga l&#39;estensione, quindi **i campi data arrivano come stringhe** (ISO 8601, ad esempio `"2026-06-24T00:00:00.000Z"`), non come oggetti JavaScript `Date`. Se necessario, puoi convertire questi elementi:

```js
const resetDate = new Date(context.organization.nextReset);
```

## Aggiornamenti contestuali

Fusion invia nuovamente l&#39;intero contesto (tramite `contextchange`) quando:

* l&#39;utente **cambia organizzazione**,
* l&#39;utente **cambia team**, oppure
* le informazioni dell&#39;utente **connesso** sono state modificate.

Rileggere sempre tutte le chiavi utilizzate all&#39;interno del gestore `contextchange` anziché presupporre che sia stato modificato un solo valore.

## Best practice per la sicurezza

* **Non registrare, visualizzare o mantenere `imsToken`.** Trattala come una password.
* Invia il token solo agli endpoint attendibili di Adobe/Fusion, tramite HTTPS, come token `Bearer`.
* Non memorizzare dati personali dal contesto oltre ciò di cui la funzione ha bisogno.

## Utilizza il token per chiamare le API

Per trasformare `imsToken` (più `organization.id` / `team.id`) in Workfront reale o
Fusion data, non è possibile chiamare tali API direttamente dal browser, perché CORS blocca
... Indirizza invece la chiamata tramite una piccola azione di runtime App Builder. Consulta
[Chiamata delle API Workfront e Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


Per continuare il processo di creazione di un&#39;estensione personalizzata, vedere [Pubblicare l&#39;estensione](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
