---
title: Aggiungere filtri e nidificazione alle route di gestione degli errori
description: Puoi aggiungere tecniche avanzate di gestione degli errori al percorso di gestione degli errori includendo filtri e nidificazione.
author: Becky
feature: Workfront Fusion
exl-id: 745bfdc4-1327-4a28-a863-c217f15a7fc5
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 0%

---

# Aggiungere filtri e nidificazione alle route di gestione degli errori

Puoi aggiungere tecniche avanzate di gestione degli errori al percorso di gestione degli errori includendo filtri e nidificazione.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Selezionare o Prime Workfront Plan: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Ultimate Workfront: Workfront Fusion è incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Filtro

Esistono due tipi di filtro che possono essere eseguiti su un percorso di gestore degli errori.

* [Aggiungere un filtro alla route del gestore degli errori](#add-a-filter-to-the-error-handler-route)
* [Aggiungi un router seguito da filtri alla route del gestore errori](#add-a-router-followed-by-filters-to-the-error-handler)

### Aggiungere un filtro alla route del gestore degli errori

È possibile utilizzare un filtro per controllare gli errori gestiti dalla route del gestore degli errori. Questo consente di elaborare solo tipi specifici di errori. Se un errore non passa attraverso il filtro, verrà trattato come se non fosse stato definito alcun percorso del gestore degli errori per il modulo specificato.

Questi filtri sono configurati come qualsiasi altro filtro in Fusion. Per istruzioni, vedere [Aggiungere un filtro a uno scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

### Aggiungi un router seguito da filtri al gestore degli errori

L&#39;aggiunta di un router a una route di gestione degli errori consente di configurare route diverse per tipi diversi di errori.

Ad esempio, per configurare una route da eseguire quando l&#39;errore è un DataError, è possibile impostare un filtro che consenta la trasmissione dei dati se il tipo di errore mappato è uguale a DataError.

![Filtro DataError](assets/filter-dataerror.png)

Per informazioni su come Fusion valuta ed elabora vari tipi di dati, vedere [Tipi di errore](/help/workfront-fusion/references/errors/error-processing.md).

### Esempio: gestione degli errori con i filtri

>[!BEGINSHADEBOX]

Questo scenario di esempio mostra il funzionamento di questi filtri per la gestione degli errori.

Se si utilizza Dropbox > Crea modulo cartella e esiste già una cartella con lo stesso nome, il modulo genera un errore dati:

![Errore nel Dropbox](assets/dropbox.png)

Lo scenario completo funziona come segue:

![Scenario Dropbox](assets/dropbox-scenario.png)

1. Il modulo Strumenti > Imposta variabile contiene il nome della cartella
1. Il modulo HTTP > Ottieni file recupera il file che deve essere caricato nella cartella
1. Il modulo Dropbox > Crea cartella genera un errore se esiste già una cartella con lo stesso nome di quella mappata nel modulo
1. La route del gestore degli errori (bolle trasparenti) contiene un router per filtrare gli errori
La prima route è per un tipo di errore specificato denominato `DataError`.

   1. Se si verifica un `DataError` e i dettagli dell&#39;errore passano attraverso il filtro, il Dropbox >Elenca tutti i file/sottocartelle in un modulo cartella elenca tutte le cartelle nel Dropbox.
   1. Il filtro successivo corrisponde ai nomi delle cartelle.
   1. La direttiva **Riprendi** specifica l&#39;ID cartella e il percorso della cartella esistente e l&#39;esecuzione dello scenario riprende dal Dropbox > Crea modulo cartella. Tuttavia, invece di creare una nuova cartella, Fusion utilizza i valori della direttiva Riprendi per passare al modulo successivo e caricare il file nella cartella esistente.

1. La seconda route è per tutti gli altri errori e termina con la direttiva Rollback, che determina l&#39;interruzione immediata dello scenario

Di seguito è riportata una spiegazione dettagliata della route DataError.

Per utilizzare la cartella esistente nei moduli successivi, ad esempio Caricare un file, è necessario aggiungere al modulo un percorso del gestore degli errori e recuperare il percorso della cartella da mappare nel modulo della direttiva di ripresa che segue:

![Aggiungi route gestore errori](assets/add-error-handler-route.png)

Il filtro della prima route è impostato per gestire solo l&#39;errore specifico (DataError) che viene visualizzato quando esiste già una cartella con lo stesso nome:

![Condizione](assets/condition.png)

Il Dropbox > Elenca tutti i file in un modulo di cartelle è configurato per restituire tutte le cartelle nella cartella di destinazione. Il seguente filtro passa solo a quello che stavamo originariamente tentando di creare. (Il nome della cartella viene memorizzato in 33. Elemento Nome cartella.)

![Condizione](assets/condition2.png)

La direttiva Riprendi fornisce quindi il percorso della cartella come output per il modulo non riuscito. L’ID cartella è stato lasciato vuoto perché non è necessario dal modulo Carica file.

![Controllo flusso](assets/flow-control.png)

>[!ENDSHADEBOX]

## Nidificazione

È possibile creare e configurare route del gestore errori in tutti i moduli, ad eccezione dei router. È pertanto possibile creare una route di gestore degli errori per un modulo che fa già parte di una route di gestore degli errori esistente.

>[!BEGINSHADEBOX]

Esempio:

Route del gestore degli errori nidificata con filtri:

![Errore nidificato durante la gestione della route](assets/nested-error-handling-route.png)

In questo scenario, la seconda route del gestore errori è nidificata sotto la prima route del gestore errori.

Se il modulo Dropbox > Crea cartella riscontra un errore, l’esecuzione si sposta sulla prima route. Se viene passato il filtro `DataError Takes Place`, viene eseguito il modulo successivo, seguito dal modulo Riprendi direttiva se non si verifica un errore in Dropbox > Elenca tutti i file/sottocartelle in un modulo cartella.

Tuttavia, se si verifica un errore in Dropbox > Elenca tutti i file/sottocartelle in un modulo cartelle, l&#39;esecuzione si sposta su Gestione errori Route 2 e termina con la direttiva [!UICONTROL Ignore]. Il modulo [!UICONTROL Resume directive] non viene eseguito in questo caso.

>[!ENDSHADEBOX]
