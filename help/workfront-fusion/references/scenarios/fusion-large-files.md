---
title: Utilizzo di file di grandi dimensioni
description: Il supporto per file di grandi dimensioni è attualmente disponibile per i connettori Workfront e HTTP.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: 80cb3736d96d4b7c3226d78149842a80077e3551
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 2%

---

# Utilizzo di file di grandi dimensioni

>[!IMPORTANT]
>
>La funzionalità per file di grandi dimensioni è disponibile solo per le organizzazioni che utilizzano il pacchetto Workfront Ultimate.

In Workfront Fusion sono ora disponibili funzionalità di trasferimento dati migliorate che consentono di elaborare file di dimensioni notevolmente maggiori.

Per gestire file di grandi dimensioni, è necessario aggiornare gli scenari.

## Connettori che supportano file di grandi dimensioni

Attualmente, i seguenti connettori supportano file di grandi dimensioni.

>[!NOTE]
>
>* Se un file viene scaricato utilizzando un modulo che supporta file di grandi dimensioni e quindi trasmesso a un modulo che non supporta file di grandi dimensioni, tale modulo non elabora correttamente il file. I file di grandi dimensioni devono essere gestiti esclusivamente con i moduli supportati in tutto il flusso di lavoro.
>* I moduli che non supportano file di grandi dimensioni possono elaborare file fino a 200 MB.

* Workfront
   * Carica documento
   * Scarica Documento
* Adobe Experience Manager Assets
   * Carica documento
* Workfront Proof
   * Carica file
   * Scarica bozza
* Adobe Authenticator
   * Effettuare una chiamata API personalizzata
* SharePoint
   * Creare un file
   * Ottieni un file
* Forza vendita
   * Carica file
* AWS S3
   * Carica file
   * Ottieni file
* HTTP

Altri connettori saranno supportati nelle versioni future.

## Aggiornare gli scenari per gestire file di grandi dimensioni

Il modulo Workfront > Carica documento è stato modificato per gestire file di dimensioni maggiori. Nella versione precedente di questo modulo ora vengono visualizzati `(Legacy)` aggiunti al nome del modulo. Nella maggior parte dei casi il modulo legacy continuerà a funzionare.

Se prevedi di lavorare con file di dimensioni maggiori, ti consigliamo di sostituire il modulo legacy con il nuovo modulo Carica documento. Il nuovo modulo Carica documento evita timeout e altri errori.

![Carica documento](assets/new-upload-document.png)

## Domande frequenti

### Qual è il nuovo limite di dimensione file?

Gli utenti possono ora elaborare file che superano il precedente limite di 1 GB, migliorando l&#39;efficienza e la produttività.  Anche se non esiste un limite di dimensione definito per la piattaforma Workfront Fusion, l’utilizzo di file di grandi dimensioni può essere influenzato da altri fattori:

* **Limitazioni relative alle dimensioni dei file del servizio a cui Fusion si connette**: se il servizio limita le dimensioni dei file, Workfront Fusion non supera tali limitazioni. I limiti di dimensione dei file dipendono in ultima analisi dal servizio Web a cui Fusion si connette.

* **Tempo di esecuzione scenario**: Fusion elabora i file di qualsiasi dimensione fino al raggiungimento del limite di esecuzione di 40 minuti. Il caricamento, il download o l&#39;elaborazione di file di grandi dimensioni nello scenario Fusion potrebbe richiedere del tempo. Se i file di grandi dimensioni fanno durare l’esecuzione più di 40 minuti, lo scenario non riesce. Il tempo di esecuzione di uno scenario può essere influenzato anche dalle dimensioni dello scenario, dalla complessità del modulo e dalla velocità di rete. Pertanto, si consiglia di considerare questi aspetti degli scenari quando si utilizzano file di grandi dimensioni.

>[!NOTE]
>
>Come best practice, consigliamo di limitare le dimensioni del file a 15 GB.

### Come funziona il nuovo trasferimento di file di Fusion?

Quando Fusion elabora i file, i file più grandi vengono aggiunti all’archiviazione persistente (Bucket S3 o Archiviazione BLOB di Azure). Quando un modulo Fusion esegue un’azione sul file, come il caricamento o il download, Fusion utilizza il file nell’archiviazione persistente come origine invece che come memoria attiva.

### È possibile utilizzare file di grandi dimensioni con esecuzioni incomplete?

Sì, Fusion supporta esecuzioni incomplete con file di dimensioni maggiori. Tieni presente che le esecuzioni incomplete hanno dimensioni limitate per un’organizzazione e devono essere gestite attivamente.

### Posso usare file più grandi con qualsiasi connettore?

Ogni connettore Fusion deve essere aggiornato per supportare file di grandi dimensioni. I connettori supportati sono Workfront, HTTP e AEM Assets. I connettori Fusion sono ancora limitati dalle dimensioni del file supportate dal servizio web. I limiti di dimensione dei file sono generalmente inclusi nella documentazione API per gli endpoint del servizio web che scaricano e caricano i file.

### Questo influisce sulle operazioni?

No, il numero di operazioni eseguite da un modulo è lo stesso.

### Quando verrà aggiornata l’interfaccia utente di Fusion per visualizzare i dati di trasferimento dei file?

Questa funzione è già stata completata e implementata in produzione.

### Quali sono alcuni modi per pensare ai nuovi limiti di elaborazione dei file che mi aiuteranno a progettare scenari?

Progettare uno scenario che funzioni entro il limite di esecuzione di 40 minuti può sembrare complicato. Durante la progettazione di uno scenario, è consigliabile tenere presente quanto segue:

* **Comprendere i requisiti aziendali per il tempo di esecuzione**: il limite della piattaforma Fusion per il tempo di esecuzione è di 40 minuti, ma si prevede che la maggior parte delle automazioni dei processi aziendali venga eseguita molto più rapidamente. Ad esempio, le automazioni avviate dall’utente con continuazione dipendente dai risultati dovrebbero essere completate ben al di sotto del limite di 40 minuti.
* **Considera il tempo di esecuzione durante la progettazione**: durante la progettazione dello scenario, è essenziale comprendere il tempo di esecuzione del modulo per le singole azioni sui file, ad esempio caricamenti e download. Questa conoscenza consente di pianificare scenari che richiedono più azioni sui file.  Per garantire la precisione del progetto, si consiglia di arrotondare il tempo di esecuzione del modulo per includere un buffer.
Ad esempio, se Fusion scarica un documento in 144 secondi (2,4 minuti), è possibile prevedere che una singola esecuzione possa eseguire più volte azioni simili. In questo esempio, l’esecuzione del modulo richiede 144 secondi ed è necessario pianificare un tempo di esecuzione di 3 minuti per il download. Se i tuoi requisiti includono sia un caricamento che un download, il tempo di esecuzione previsto sarebbe di circa 6 minuti. I tempi di esecuzione di Fusion sono limitati a 40 minuti.

* **Consolidare le azioni file**: l&#39;esempio più comune di azioni file in uno scenario Fusion è un download e un caricamento. La maggior parte degli scenari con solo queste due azioni verrà eseguita in pochi minuti. Se possibile, i progettisti di Fusion devono vincolare i loro scenari a un unico download e a un unico caricamento.

* **Calcola le dimensioni utilizzando il pannello di mappatura**: Workfront e altri servizi Web includono le dimensioni del file nell&#39;output del modulo di download. Puoi utilizzare questi dati per filtrare i file troppo grandi per il caricamento di un modulo o troppo grandi per il tempo di esecuzione dello scenario.

* **Isolare le azioni file nel proprio scenario quando si lavora con più file**: i progettisti di Fusion devono prendere in considerazione l&#39;isolamento delle azioni file in scenari separati. Ad esempio, uno scenario Fusion attivato da una nuova richiesta Workfront con più file allegati potrebbe dover contenere fino a 30 file. Dato che il caricamento e il download di ciascun file potrebbero richiedere fino a 3 minuti, l’elaborazione di tutti i file in una singola esecuzione supererebbe il limite di esecuzione di Fusion di 40 minuti. La soluzione consiste nel creare uno scenario di azioni file dedicato alla gestione del caricamento e del download di singoli file. Lo scenario attivato dalla richiesta viene iterato attraverso i file allegati, richiamando lo scenario di azioni file per ogni file utilizzando il modulo HTTP. Questo approccio garantisce che ogni file venga elaborato entro i limiti di tempo di esecuzione.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
