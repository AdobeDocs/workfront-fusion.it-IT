---
title: Esecuzione scenario, cicli e fasi
description: Questo articolo descrive gli eventi che si verificano durante l’esecuzione di uno scenario Adobe Workfront Fusion, ad esempio inizializzazione, operazioni, commit e rollback.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---

# Esecuzione, cicli e fasi dello scenario

Ogni esecuzione dello scenario inizia con la fase di inizializzazione, continua con almeno un ciclo composto dalle fasi di operazione e commit/rollback e termina con la fase di finalizzazione

* Inizializzazione
* #1 ciclo
   * Funzionamento (lettura o scrittura)
   * Conferma o rollback
* #2 ciclo
   * Funzionamento (lettura o scrittura)
   * Conferma o rollback
* ...
* #n ciclo
   * Funzionamento (lettura o scrittura)
   * Conferma o rollback
* Finalizzazione

Su scala ridotta, ogni modulo segue anche queste fasi. Le informazioni sulle fasi del modulo si trovano nelle informazioni del bundle elaborate, nella bolla numerata in alto a destra di ciascun modulo dopo l’esecuzione dello scenario. Per ulteriori informazioni sull&#39;individuazione delle informazioni sui bundle elaborati, vedere [Informazioni sui bundle elaborati](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) nell&#39;articolo Flusso di esecuzione dello scenario.

Per informazioni sulle fasi di scenario più grandi, consulta i dettagli di esecuzione.

## Fasi di esecuzione dello scenario

### Inizializzazione

Durante la fase di inizializzazione, vengono create e verificate tutte le connessioni necessarie (connessione a un database, a un servizio e-mail e così via) per garantire che il modulo sia in grado di eseguire le operazioni previste.

### Cicli

Ogni ciclo rappresenta un&#39;unità di lavoro indivisibile composta da una serie di operazioni, ciascuna con un commit o un rollback.

Puoi impostare il numero massimo di cicli nel pannello [!UICONTROL impostazioni scenario]. Il numero predefinito è 1.

* [Operazione](#operation)
* [Conferma](#commit)
* [Rollback](#rollback)

#### Operazione

Durante la fase operativa viene eseguita un&#39;operazione di lettura o scrittura:

* Un’operazione di lettura consiste nell’ottenere dati da un servizio che viene quindi elaborato da altri moduli in base a uno scenario predefinito. Ad esempio, il modulo [!UICONTROL Workfront] >[!UICONTROL Osserva record] restituisce nuovi bundle (record) creati dall&#39;ultima esecuzione dello scenario.
* Un’operazione di scrittura consiste nell’inviare dati a un determinato servizio per un’ulteriore elaborazione. Ad esempio, il modulo Workfront >[!UICONTROL Carica documento] carica un file in Workfront.

#### Conferma

Se la fase operativa ha esito positivo, inizia la fase di commit durante la quale vengono eseguite tutte le operazioni eseguite dai moduli. Ciò significa che Workfront Fusion invia informazioni relative al successo a tutti i servizi coinvolti nella fase operativa.

### Rollback

Se si verifica un errore durante la fase di operazione o commit di un modulo, la fase viene interrotta e viene avviata la fase di rollback, rendendo vuote tutte le operazioni durante il ciclo specificato.

>[!IMPORTANT]
>
>Tutti i moduli di Workfront Fusion che supportano il rollback (noto anche come transazionale) sono contrassegnati con il tag ACID.
>
>![Moduli acidi](assets/acid-modules.png)
>
>I moduli non contrassegnati con questo tag non possono essere ripristinati allo stato iniziale quando si verificano errori in altri moduli. Un esempio tipico di modulo non-ACID è l&#39;azione [!UICONTROL E-mail] >[!UICONTROL Invia e-mail]. Una volta inviata l’e-mail, non puoi annullare l’invio.

### Finalizzazione

Durante la fase di finalizzazione, le connessioni aperte (ad esempio le connessioni FTP, le connessioni al database e così via) vengono chiuse e lo scenario viene completato.

## Risorse

Per ulteriori informazioni, vedere [Configurare le impostazioni dello scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).
