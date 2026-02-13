---
content-type: reference
title: Tipi di errore
description: A volte può verificarsi un errore durante l’esecuzione di uno scenario. Ciò si verifica in genere se un servizio non è disponibile a causa di un errore di connessione a un servizio o se una convalida non riesce. In questo articolo vengono descritti gli errori comuni che possono verificarsi.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 8%

---

# Tipi di errore

A volte può verificarsi un errore durante l’esecuzione di uno scenario. Ciò si verifica in genere se un servizio non è disponibile a causa di un errore di connessione al servizio o se una convalida non riesce.

Adobe Workfront Fusion distingue tra diversi tipi di errore di base. Il tipo di errore determina le azioni successive dello scenario Fusion.

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Errore di connessione

`ConnectionError`

Gli errori di connessione sono uno degli errori più comuni. Di solito sono causate dall’indisponibilità del servizio di terze parti per vari motivi, come sovraccarico, manutenzione o interruzione. La gestione predefinita di questo errore dipende dal modulo che ha riscontrato l’errore.

* Se l’errore si verifica sul primo modulo, l’esecuzione dello scenario viene terminata con un messaggio di avviso. Workfront Fusion quindi tenta ripetutamente di eseguire nuovamente lo scenario a intervalli di tempo crescenti. Se tutti i tentativi hanno esito negativo, Workfront Fusion disattiva lo scenario.
* Se l’errore di connessione si verifica in un modulo diverso dal primo, i passaggi successivi dipendono dall’opzione Consenti archiviazione di esecuzioni incomplete nelle impostazioni avanzate dello scenario:

   * Se questa opzione è abilitata, l&#39;esecuzione dello scenario viene spostata nella cartella [!UICONTROL Esecuzioni incomplete] in cui Workfront Fusion tenta ripetutamente di eseguire nuovamente lo scenario a intervalli di tempo crescenti. Se tutti i tentativi non vanno a buon fine, l’esecuzione rimarrà nella cartella Esecuzioni incomplete in attesa della risoluzione manuale da parte dell’utente.

     Per ulteriori informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).
   * Se questa opzione è disabilitata, l’esecuzione dello scenario termina con un errore seguito da una fase di rollback. Workfront Fusion quindi tenta ripetutamente di eseguire nuovamente lo scenario a intervalli di tempo crescenti. Se tutti i tentativi hanno esito negativo, Workfront Fusion disattiva lo scenario.

  Per ulteriori informazioni sull&#39;impostazione Consenti l&#39;archiviazione di esecuzioni incomplete, vedere [Consenti l&#39;archiviazione di esecuzioni incomplete](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) nell&#39;articolo Configurare le impostazioni dello scenario.

### Aumento degli intervalli di tempo

L’algoritmo per aumentare gli intervalli di tempo tra i tentativi quando si verifica un errore è noto come backoff esponenziale. Gli intervalli di tempo crescenti vengono impostati come segue:

1. 10 minuti
1. 1 ora
1. 3 ore
1. 12 ore
1. 24 ore

L’aumento degli intervalli di tempo consente di evitare che gli scenari eseguiti di frequente utilizzino operazioni su tentativi ripetutamente non riusciti.

>[!BEGINSHADEBOX]

**Esempio:**

Uno scenario contiene il trigger [!DNL Google Sheets] [!UICONTROL Righe controllo]. [!DNL Google Sheets] non è disponibile per 30 minuti a causa di manutenzione all&#39;avvio dello scenario da parte di Workfront Fusion, pertanto non è possibile recuperare nuove righe. Lo scenario si interrompe e riprova tra 10 minuti. Poiché [!DNL Google Sheets] non è ancora disponibile, Workfront Fusion non è ancora in grado di ottenere informazioni sulle nuove righe. La prossima esecuzione dello scenario è pianificata in 1 ora. [!DNL Google Sheets] è nuovamente disponibile in questo momento e lo scenario viene eseguito correttamente.

>[!ENDSHADEBOX]

## Errore di dati

`DataError`

Quando un elemento viene mappato in modo errato, viene generato un errore di dati che non passa la convalida eseguita sul lato Workfront Fusion o sul lato del servizio di terze parti.

Se si verifica questo errore, lo scenario, fino al punto in cui il modulo non è riuscito, viene spostato nella cartella esecuzioni incomplete, dove è possibile risolvere il problema. Tuttavia, lo scenario non si arresta e continua a essere eseguito in base alla pianificazione. Per interrompere l’esecuzione dello scenario quando viene visualizzato l’errore Dati, abilita l’opzione Elaborazione sequenziale nel pannello Impostazioni scenario.

Se non hai abilitato l&#39;opzione [!UICONTROL Consenti la memorizzazione di esecuzioni incomplete] nelle impostazioni dello scenario, l&#39;esecuzione dello scenario termina con l&#39;errore e viene eseguito un rollback.

## Errore di dati duplicati

`DuplicateDataError`

Se Workfront Fusion tenta di inserire lo stesso bundle due volte in un servizio che non consente la duplicazione dei dati, viene generato un errore di dati duplicati. Se si verifica questo errore, Workfront Fusion procede come per l’errore relativo ai dati.

Per ulteriori informazioni, vedere [Errore dati](#data-error) in questo articolo.


## Errore token di accesso non valido

`InvalidAccessTokenError`

Si verifica un errore di token di accesso non valido quando Workfront Fusion non può accedere all’account registrato con un servizio di terze parti. Ciò si verifica in genere quando si revocano i diritti di accesso per Workfront Fusion nell’amministrazione di un determinato servizio, ma gli scenari che utilizzano tale servizio continuano a essere eseguiti in base alla pianificazione.

Se si verifica questo errore, l’esecuzione dello scenario viene interrotta immediatamente. Il resto dello scenario che inizia dal modulo in cui si è verificato l’errore si sposta nella cartella delle esecuzioni incomplete.

## Errore limite di frequenza

`RateLimitError`

Se viene superato un limite impostato da un determinato servizio, viene generato un errore di limite della frequenza. Se si verifica questo errore, Workfront Fusion procede come per l’errore di connessione.

Per ulteriori informazioni, vedere [Errore di connessione](#connection-error) in questo articolo.

## Errore di dati incompleti

`IncompleteDataError`

Un errore di dati incompleto si verifica solo con i trigger. Questo errore viene generato se un trigger non riesce a scaricare i dati richiesti da un determinato servizio.

Se uno scenario termina con `IncompleteDataError`, il suo ulteriore comportamento dipenderà dall&#39;impostazione di [!UICONTROL Numero massimo di errori consecutivi].

Per ulteriori informazioni, vedere [Numero di errori consecutivi](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) nell&#39;articolo Configurare le impostazioni dello scenario.

>[!BEGINSHADEBOX]

**Esempio:**

In uno scenario il trigger di Workfront [!UICONTROL Record di controllo] è impostato per la verifica dei documenti. Lo scenario viene eseguito durante il caricamento di un documento di grandi dimensioni, ad esempio un video lungo. Poiché [!UICONTROL Workfront Fusion] tenta di scaricare il video mentre è ancora in fase di caricamento in Workfront, lo scenario termina con `IncompleteDataError`.

>[!ENDSHADEBOX]

## Errore di runtime

`RuntimeError`

Qualsiasi errore che viene visualizzato durante l&#39;esecuzione dello scenario e che non rientra in uno di questi tipi di errore viene segnalato come `RunTimeError`.

Se uno scenario termina con `RuntimeError`, il suo ulteriore comportamento dipende dall&#39;impostazione [!UICONTROL Numero massimo di errori consecutivi].

Per ulteriori informazioni, vedere [Numero di errori consecutivi](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) nell&#39;articolo Configurare le impostazioni dello scenario.


>[!NOTE]
>
>Se uno scenario inizia con un trigger immediato e riscontra questo errore, l&#39;impostazione di [!UICONTROL Numero massimo di errori consecutivi] viene ignorata e lo scenario viene disattivato immediatamente.
>Per ulteriori informazioni, vedi [Trigger istantanei](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) nell&#39;articolo Panoramica dei moduli.

## Errore di incoerenza

`InconsistencyError`

Se uno di questi errori si verifica durante la fase di commit o rollback, lo scenario termina con un errore di incoerenza.

Se questo errore viene visualizzato in uno scenario, l’esecuzione dello scenario viene interrotta immediatamente.

## Avvertenza

Durante l’esecuzione di uno scenario, è possibile che venga visualizzato un avviso che ti informa su un problema. Un avviso non impedisce il completamento corretto dello scenario.

Ad esempio, può comparire un avviso quando viene superata la dimensione massima consentita per il file e l&#39;opzione [!UICONTROL Abilita perdita di dati] è disabilitata.

## Risorse

Per ulteriori informazioni sulla mappatura, vedere [Panoramica sulla mappatura](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

Per informazioni sulle esecuzioni incomplete, vedere [Visualizzare e risolvere le esecuzioni incomplete](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Per informazioni sul pannello delle impostazioni dello scenario, vedere [Configurare le impostazioni dello scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

Per informazioni sulle pianificazioni, vedere [Pianificare uno scenario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Per informazioni sulle fasi dello scenario, vedere [Esecuzione dello scenario, cicli e fasi](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Per informazioni sull&#39;opzione Abilita perdita dati, vedere [Abilita perdita dati](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) nell&#39;articolo Configurare le impostazioni dello scenario.
