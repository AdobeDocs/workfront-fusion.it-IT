---
title: Moduli SFTP
description: I moduli  [!DNL Adobe Workfront Fusion SFTP]  consentono di monitorare le modifiche apportate ai file in una cartella o sottocartella selezionata, caricare nuovi file nella cartella desiderata, modificare o eliminare i file esistenti già presenti in una cartella o modificare le autorizzazioni per i file.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Moduli SFTP

I moduli SFTP di [!DNL Adobe Workfront Fusion] consentono di monitorare le modifiche dei file in una cartella o sottocartella selezionata, caricare nuovi file nella cartella desiderata, modificare o eliminare i file esistenti già presenti in una cartella o modificare le autorizzazioni dei file.

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisiti

Per utilizzare SFTP con [!DNL Workfront Fusion], è necessario disporre di un account SFTP (ad esempio [!DNL GoDaddy] hosting Web).

## Connetti SFTP a [!DNL Workfront Fusion] {#connect-sftp-to-workfront-fusion}

Per collegare il tuo account SFTP a [!DNL Workfront Fusion] devi immettere l&#39;host di destinazione e le credenziali SFTP (nome utente e password o nome utente e chiave) nella finestra di dialogo [!UICONTROL Create a connection] del modulo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Immetti il nome della connessione SFTP.</p> </td> 
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
 </tbody> 
</table>

Dopo aver immesso le informazioni di connessione, fare clic su **[!UICONTROL Continue]** per stabilire una connessione.

## [!UICONTROL SFTP] moduli e relativi campi

Quando configuri [!UICONTROL SFTP] moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!UICONTROL SFTP], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Triggers

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
   <td> <p>Immetti o mappa la cartella da controllare. È possibile specificare un percorso assoluto come <code>/home/user/</code>. Oppure puoi specificare un percorso relativo che punti a una cartella specifica dell’utente connesso, ad esempio <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Dimensioni buffer [B]</td> 
   <td> <p> Immettere la dimensione del buffer in byte. Il valore definisce la dimensione dei blocchi trasferiti dal server. Alcuni server possono causare problemi o file danneggiati quando il valore è troppo alto.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Imposta il numero massimo di file con cui [!DNL Workfront Fusion] lavorerà durante un ciclo</p> </td> 
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
   <td> <p> Impostare il numero massimo di cartelle che [!DNL Workfront Fusion] restituirà durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

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
   <td> <p> Impostare il numero massimo di risultati restituiti da [!DNL Workfront Fusion] durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Files]

Questo modulo elenca i file di una cartella specificata.

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
   <td> <p> Impostare il numero massimo di file che [!DNL Workfront Fusion] restituirà durante un ciclo.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

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
   <td> <p> Mappare il file di origine da un modulo precedente, ad esempio [!UICONTROL Dropbox] &gt; [!UICONTROL Get File]. È inoltre possibile immettere o mappare il nome e i dati del file.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Impostare le autorizzazioni desiderate per il file o la cartella. Utilizzare i parametri chmod. Ad esempio: <code>777 </code> o <code>-rwxrwxrwx</code>.</p> <p>Per ulteriori dettagli su chmod, consulta la <a href="https://ss64.com/bash/chmod.html">documentazione chmod</a>.</p> </td> 
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

#### [!UICONTROL Delete a File]

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
   <td> <p>Imposta le autorizzazioni file desiderate. Utilizzare i parametri chmod. Ad esempio, <code>777 </code> o <code>-rwxrwxrwx</code>.</p> <p>Deve corrispondere al pattern <code> /(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Per ulteriori dettagli su chmod, consulta la <a href="https://ss64.com/bash/chmod.html">documentazione chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Folder]

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
   <td> <p>Imposta le autorizzazioni della cartella desiderate. Utilizzare i parametri chmod. Ad esempio, <code>777 </code> o <code>-rwxrwxrwx</code>.</p> <p>Deve corrispondere al pattern <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Per ulteriori dettagli su chmod, fare riferimento alla <a href="https://ss64.com/bash/chmod.html">pagina man chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

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
