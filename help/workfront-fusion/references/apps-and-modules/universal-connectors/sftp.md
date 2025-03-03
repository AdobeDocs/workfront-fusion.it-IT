---
title: Moduli SFTP
description: I moduli  [!DNL Adobe Workfront Fusion SFTP]  consentono di monitorare le modifiche apportate ai file in una cartella o sottocartella selezionata, caricare nuovi file nella cartella desiderata, modificare o eliminare i file esistenti già presenti in una cartella o modificare le autorizzazioni per i file.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: e1e15985db9683525250d1f9f9276224b2baf0e6
workflow-type: tm+mt
source-wordcount: '1851'
ht-degree: 0%

---

# Moduli SFTP

I moduli SFTP di [!DNL Adobe Workfront Fusion] consentono di monitorare le modifiche dei file in una cartella o sottocartella selezionata, caricare nuovi file nella cartella desiderata, modificare o eliminare i file esistenti già presenti in una cartella o modificare le autorizzazioni dei file.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
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
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare SFTP con [!DNL Workfront Fusion], è necessario disporre di un account SFTP (ad esempio [!DNL GoDaddy] hosting Web).

## Connetti SFTP a [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

Per connettere l&#39;account SFTP a [!DNL Workfront Fusion] è necessario creare una connessione che specifichi l&#39;host di destinazione e le credenziali SFTP (nome utente e password o nome utente e chiave).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Immetti il nome della connessione SFTP.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Environment]</td>
    <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Type]</td>
    <td>Seleziona se ti interessa la connessione a un account di servizio o a un account personale.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Immetti il nome host del server SFTP che desideri connettere.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Immetti la porta del server SFTP. Ad esempio, 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Seleziona il metodo di autorizzazione da utilizzare per la connessione al server SFTP.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong>: immetti le credenziali.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong>: immetti il nome utente e la chiave privata/certificato</p> <p>Carica la chiave privata per utilizzare l’autorizzazione lato client oppure carica il certificato (file P12 o PFX) se desideri utilizzare TLS con il certificato autofirmato. Se utilizzi l’autorizzazione del certificato lato client, puoi immettere qui il certificato CA.</p> <p>[!DNL Workfront Fusion] non conserva né archivia i dati (file, password) forniti in questo documento. File e password vengono utilizzati solo per estrarre una chiave privata o un certificato.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Key exchange algorithms] </td> 
   <td> <p>È possibile immettere un set di algoritmi per lo scambio di chiavi. Il modulo assegna la priorità agli algoritmi in base all’ordine in cui sono stati aggiunti. Per ogni algoritmo che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e selezionare l'algoritmo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ciphers] </td> 
   <td> <p>È possibile immettere un set di crittografie per lo scambio di chiavi. Il modulo assegna la priorità alle crittografie in base all’ordine in cui sono state aggiunte. Per ogni crittografia che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e selezionare la crittografia.</p> </td> 
  </tr> 
 </tbody> 
</table>

Dopo aver immesso le informazioni di connessione, fare clic su **[!UICONTROL Continue]** per stabilire una connessione.

## [!UICONTROL SFTP] moduli e relativi campi

Quando configuri [!UICONTROL SFTP] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!UICONTROL SFTP], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Trigger

* [Controllare i file in una cartella](#watch-files-in-a-folder)
* [Osservare le sottocartelle in una cartella](#watch-subfolders-in-a-folder)

#### [!UICONTROL Watch Files in a Folder]

Restituisce i file con i dettagli quando un file viene creato o modificato in una cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Immetti la cartella da controllare. È possibile specificare un percorso assoluto come <code>/home/user/</code> oppure un percorso relativo che punta a una cartella specifica dell'utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Dimensioni buffer [B]</td> 
   <td> <p> Immettere la dimensione del buffer in byte. Il valore definisce la dimensione dei blocchi trasferiti dal server. Alcuni server possono causare problemi o file danneggiati quando il valore è troppo alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Subfolders in a Folder]

Restituisce le cartelle con i dettagli quando una cartella viene creata o modificata in una cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Immetti o mappa la cartella da controllare. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [Creare una cartella](#create-a-folderr)
* [Eliminare un file](#delete-a-file)
* [Eliminare una cartella](#delete-a-folder)
* [Ottieni un file](#get-a-file)
* [Ottieni file](#get-files)
* [Elencare il contenuto di una cartella](#list-a-folders-content)
* [Spostare un file](#move-a-file)
* [Rinominare un file](#rename-a-file)
* [Autorizzazioni di aggiornamento file](#update-file-permissions)
* [Carica un file](#upload-a-file)

#### [!UICONTROL Create a folder]

Crea una nuova cartella nel percorso specificato.

>[!NOTE]
>
>Se la cartella esiste già, il modulo genera un errore. Per continuare il flusso senza interruzioni, allegare al modulo una route di gestore degli errori per rilevare l&#39;errore e utilizzare la direttiva [!UICONTROL Resume] per continuare il flusso. Per informazioni su come allegare una route del gestore degli errori, vedere [Gestione degli errori in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Per informazioni sulla route del gestore degli errori, vedere [Direttive per la gestione degli errori in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Specificare una cartella esistente come percorso di archiviazione per la nuova cartella. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> Immetti il nome della cartella.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Imposta le autorizzazioni della cartella desiderate. Utilizzare i parametri chmod. Ad esempio, <code>777</code> o <code>-rwxrwxrwx</code>.</p> <p>Queste autorizzazioni devono corrispondere al pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Per ulteriori informazioni su chmod, vedere la <a href="https://ss64.com/bash/chmod.html">documentazione chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Immettere il percorso del file che si desidera eliminare. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Specificare il percorso della cartella da eliminare. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Questo modulo recupera i dettagli del file, inclusi i dati di un file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Immettere la dimensione del buffer in byte. Il valore definisce la dimensione dei blocchi trasferiti dal server. Alcuni server possono causare problemi o file danneggiati quando il valore è troppo alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>Immettere il percorso del file. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get files]

Questo modulo restituisce file da una cartella specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Immettere la dimensione del buffer in byte. Il valore definisce la dimensione dei blocchi trasferiti dal server. Alcuni server possono causare problemi o file danneggiati quando il valore è troppo alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Immettere o mappare la cartella contenente i file o le cartelle da elencare. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Inserisci o mappa il termine di ricerca. Se ad esempio si desidera cercare file con estensione .txt, immettere <code>.txt</code>.È inoltre possibile immettere o mappare il nome del file che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Specificare se si desidera ordinare i risultati in base al nome del file, alla dimensione, alla data dell'ultimo accesso o alla data dell'ultima modifica.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> Seleziona se restituire il risultato in ordine crescente o decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Abilita questa opzione per garantire che questo modulo non interrompa lo scenario se non restituisce alcun risultato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List a folder's content]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Seleziona se desideri recuperare file, cartelle o entrambi.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Immettere o mappare la cartella contenente i file o le cartelle da elencare. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Inserisci o mappa il termine di ricerca. Se ad esempio si desidera cercare file con estensione .txt, immettere <code>.txt</code>.È inoltre possibile immettere o mappare il nome del file che si desidera cercare.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Specificare se si desidera ordinare i risultati in base al nome file, alla dimensione, alla data dell'ultimo accesso o alla data dell'ultima modifica.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>Seleziona se restituire il risultato in ordine crescente o decrescente.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Abilita questa opzione per garantire che questo modulo non interrompa lo scenario se non restituisce alcun risultato.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Immettere o mappare il numero massimo di record che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Immettere il percorso del file che si desidera spostare. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> Immettere il percorso della nuova posizione del file. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File]

Rinomina un file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Immettere il percorso del file da rinominare. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> Immettere il nuovo nome del file, inclusa l'estensione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update file permissions]

Consente di modificare le autorizzazioni del file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Immettere il percorso del file che si desidera spostare. È possibile specificare un percorso assoluto come <code>/home/user/file.txt</code>. Oppure è possibile specificare un percorso relativo che punti a una cartella specifica dell'utente connesso, ad esempio <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Imposta le autorizzazioni file desiderate. Utilizzare i parametri chmod. Ad esempio, <code>777</code> o <code>-rwxrwxrwx</code>.</p> <p>Queste autorizzazioni devono corrispondere al pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Per ulteriori informazioni su chmod, vedere la <a href="https://ss64.com/bash/chmod.html">documentazione chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Questo modulo ti consente di caricare un file sul server SFTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Per istruzioni sulla connessione dell'account SFTP a [!DNL Workfront Fusion], consulta <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connettere SFTP a [!DNL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Specificare una cartella esistente come percorso di archiviazione del file. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> Selezionare un file di origine da un modulo precedente o mappare il nome e i dati del file di origine.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Impostare le autorizzazioni desiderate per il file o la cartella. Utilizzare i parametri chmod. Ad esempio, <code>777</code> o <code>-rwxrwxrwx</code>.</p> <p>Queste autorizzazioni devono corrispondere al pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Per ulteriori informazioni su chmod, vedere la <a href="https://ss64.com/bash/chmod.html">documentazione chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
