---
title: Moduli e-mail
description: In uno scenario Adobe Workfront Fusion, puoi collegare il tuo account e-mail a più applicazioni e servizi di terze parti. Questo ti consente di scaricare e-mail tramite IMAP, inviare e-mail tramite SMTP, creare nuove bozze, spostare e copiare e-mail da una cartella a un’altra, contrassegnare le e-mail come lette o non lette ed eliminare le e-mail.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---

# Moduli e-mail

In uno scenario Adobe Workfront Fusion, puoi collegare il tuo account e-mail a più applicazioni e servizi di terze parti. Questo ti consente di scaricare e-mail tramite IMAP, inviare e-mail tramite SMTP, creare nuove bozze, spostare e copiare e-mail da una cartella a un’altra, contrassegnare le e-mail come lette o non lette ed eliminare le e-mail.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto di flusso di lavoro Adobe Workfront e qualsiasi pacchetto di automazione e integrazione Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select, con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze Adobe Workfront</td> 
   <td> <p>Standard</p><p>Lavoro o superiore</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion</td> 
   <td>
   <p>Basato su operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basato su connettore (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Collegare l&#39;e-mail a Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Connetti a Google](#connect-to-google)
* [Connetti ad altri servizi di posta elettronica (IMAP)](#connect-to-other-email-services-smap)

### Connetti a [!DNL Google]

Utilizzare questa opzione per creare scenari con moduli e-mail che richiedono una connessione all&#39;account [!DNL Google]. Questo è un account con ambiti limitati.

Puoi creare una connessione al tuo account [!DNL Google] direttamente dall&#39;interno di un modulo e-mail.

1. In qualsiasi modulo e-mail, fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Selezionare **[!DNL Google]** come tipo di connessione.
1. Immettere un nome per la connessione.
1. (Facoltativo) Immetti l&#39;ID client [!UICONTROL [!DNL Google]] e il [!UICONTROL segreto client].
1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

### Connetti ad altri servizi di posta elettronica (IMAP)

La connessione IMAP consente di accedere alla cassetta postale in modalità remota e di leggere o manipolare i messaggi nella cassetta postale. La connessione IMAP viene utilizzata dalla maggior parte dei moduli E-mail.

1. In qualsiasi modulo e-mail, fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Selezionare **[!UICONTROL Altri (SMTP)]** come tipo di connessione.
1. Immetti un **[!UICONTROL Nome]** per la connessione.
1. Seleziona il tuo **[!UICONTROL provider di posta elettronica]** dall&#39;elenco. Se il tuo provider di posta elettronica non è presente nell’elenco, seleziona Altro.
1. Immetti **[!UICONTROL Nome utente]** e la **[!UICONTROL Password]** per l&#39;account di posta elettronica.
1. (Condizionale) Se il provider non è incluso nell&#39;elenco, immettere il **[!UICONTROL server SMTP]** e la **[!UICONTROL porta]** e specificare se si desidera **[!UICONTROL utilizzare una connessione sicura (TLS)]**. Per trovare queste informazioni, controllare la sezione [!UICONTROL Guida] della cassetta postale. Se non disponi di queste informazioni, contatta il provider di servizi e-mail.
1. Per utilizzare un certificato autofirmato, abilita l&#39;opzione **Rifiuta certificati non autorizzati** e carica il certificato autofirmato. Per istruzioni, vedere [Caricare un certificato autofirmato](#upload-a-self-signed-certificate)
1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

#### Carica un certificato autofirmato

Per aggiungere un certificato autofirmato:

1. Fai clic su **Estrai**.
1. Selezionare il tipo di file da estrarre.
1. Seleziona il file che contiene il certificato o.
1. Immettere la password per il file.
1. Fai clic su **Salva** per estrarre il file e tornare alla configurazione del modulo.

## [!UICONTROL E-mail] moduli e relativi campi

Quando configuri i moduli [!UICONTROL E-mail], Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati campi aggiuntivi, a seconda di fattori come il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Alcuni campi e-mail potrebbero contenere già dati, perché sono stati utilizzati in un altro modulo dello scenario. Se hai bisogno di informazioni su di loro, consulta la documentazione dell’e-mail.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>L&#39;ID e-mail univoco noto come &#39;[!UICONTROL ID e-mail (UID)]&#39; è l&#39;identificatore dell&#39;e-mail. L’ID e-mail è specifico per ciascuna cartella dell’e-mail.

* [Trigger](#triggers)
* [Azioni](#actions)
* [Iteratori](#iterators)

### Trigger

#### [!UICONTROL Controlla le e-mail]

Questo modulo di attivazione avvia uno scenario in cui viene ricevuta una nuova e-mail da elaborare in base a criteri specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Seleziona la cartella contenente le e-mail che desideri controllare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Seleziona i criteri in base ai quali desideri guardare le e-mail:</p> 
    <ul> 
     <li>[!UICONTROL Tutte Le E-Mail]</li> 
     <li>[!UICONTROL Solo Lettura E-Mail]</li> 
     <li>[!UICONTROL Solo E-Mail Non Lette]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indirizzo E-Mail Mittente] </td> 
   <td> <p>Immetti l’indirizzo e-mail del mittente di cui desideri guardare le e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Immetti l’oggetto dell’e-mail che desideri guardare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Inserisci eventuali parole chiave per guardare solo le e-mail contenenti le parole chiave.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contrassegna i messaggi come letti al recupero]</td> 
   <td> <p>Abilita questa opzione per contrassegnare l’e-mail non letta come letta dopo aver recuperato i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di risultati]</td> 
   <td> <p> Immetti o mappa il numero massimo di e-mail che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Azioni

* [[!UICONTROL Copia un&#39;e-mail]](#copy-an-email)
* [[!UICONTROL Crea bozza]](#create-a-draft)
* [[!UICONTROL Eliminare un&#39;e-mail]](#delete-an-email)
* [[!UICONTROL Ricevi e-mail]](#get-emails)
* [[!UICONTROL Contrassegna un&#39;e-mail come già letta]](#mark-an-email-as-read)
* [[!UICONTROL Contrassegna un&#39;e-mail come non letta]](#mark-an-email-as-unread)
* [[!UICONTROL Sposta un&#39;e-mail]](#move-an-email)
* [[!UICONTROL Invia un&#39;e-mail]](#send-an-email)

#### [!UICONTROL Copia un&#39;e-mail]

Questo modulo di azione copia un messaggio e-mail o una bozza in una cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Seleziona la cartella da cui desideri copiare l’e-mail. Esempio: primario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartella di destinazione]</td> 
   <td> <p> Seleziona la cartella in cui desideri copiare l’e-mail. Esempio: lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID e-mail (UID)]</p> </td> 
   <td> <p>Immetti l’UID e-mail dell’e-mail da copiare nella cartella di destinazione.</p> <p>È possibile ottenere l'UID dell'e-mail utilizzando il modulo [!UICONTROL E-mail] &gt; [!UICONTROL E-mail di controllo] o il modulo [!UICONTROL E-mail di ricerca].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea bozza]

Questo modulo di azione crea e aggiunge una nuova bozza a una cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Seleziona la cartella in cui desideri creare la bozza di e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL A] </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail a cui desideri inviare l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Inserisci o mappa l’oggetto dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Inserisci o mappa il contenuto dell’e-mail in formato HTML utilizzando i tag HTML o nel testo normale.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome file]</strong> </p> <p>Immetti il nome del file, inclusa l’estensione. </p> </li> 
     <li> <p><strong>[!UICONTROL Dati]</strong> </p> <p>Immettere il percorso della cartella in cui si desidera caricare l'allegato.</p> </li> 
     <li> <p><strong>[!UICONTROL ID contenuto]</strong> </p> <p>Immetti l’ID contenuto per inserire l’allegato (immagine) nel contenuto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia Destinatario] </td> 
   <td> <p>Per ogni indirizzo e-mail a cui desideri inviare una copia di questo messaggio, fai clic su <b>Aggiungi elemento</b> e immetti l'indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destinatario [!UICONTROL Blind Copy]</td> 
   <td> <p> Per ogni indirizzo di posta elettronica a cui si desidera inviare una copia di questa e-mail senza che l'indirizzo venga visualizzato nell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere l'indirizzo di posta elettronica.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, Workfront Fusion uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL Eliminare un&#39;e-mail]

Questo modulo di azione rimuove un messaggio e-mail o una bozza dalla cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Seleziona la cartella che contiene l’e-mail da eliminare.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID e-mail (UID)]</p> </td> 
   <td> <p>Immetti l’UID e-mail dell’e-mail da eliminare.</p> <p>Puoi ottenere l’UID dell’e-mail utilizzando il modulo E-mail &gt; E-mail di controllo o il modulo Ricerca .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Abilita questa opzione per rimuovere definitivamente tutti i messaggi contrassegnati come [!UICONTROL Deleted] nella cassetta postale attualmente aperta.</p> <p>Nota: in [!DNL Gmail], questo comportamento è guidato dall'impostazione nella sezione [!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ricevi e-mail]

Questo modulo restituisce le e-mail che corrispondono ai criteri specificati.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Seleziona la cartella contenente le e-mail da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contrassegna i messaggi come letti al recupero] </td> 
   <td> <p>Abilita questa opzione se desideri contrassegnare l’e-mail non letta come letta dopo aver recuperato i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Seleziona i criteri delle e-mail che desideri recuperare:</p> 
    <ul> 
     <li>[!UICONTROL Tutte Le E-Mail]</li> 
     <li>[!UICONTROL Solo Lettura E-Mail]</li> 
     <li>[!UICONTROL Solo E-Mail Non Lette]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indirizzo E-Mail Mittente] </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail del mittente di cui desideri recuperare le e-mail.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL E-Mail Destinatario]</td> 
   <td> <p> Inserisci o mappa l’indirizzo e-mail del destinatario di cui desideri recuperare le e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Da data] </td> 
   <td> <p>Inserisci o mappa la data in cui recuperare le e-mail elaborate nella data specificata o in una data successiva.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prima della data]</td> 
   <td> <p> Inserisci o mappa la data in cui recuperare le e-mail elaborate entro la data specificata.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Inserisci o mappa l’oggetto dell’e-mail che desideri recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Inserisci o mappa le parole chiave per recuperare solo le e-mail contenenti tali parole chiave.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID e-mail (UID)]</td> 
   <td> <p> Immetti l’ID e-mail (UID) dell’e-mail di cui desideri recuperare i dettagli.</p> <p>Puoi ottenere l’UID dell’e-mail utilizzando il modulo [!UICONTROL Watch Email] di Workfront Fusion o il modulo [!UICONTROL Search Email].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di risultati]</td> 
   <td> <p> Il numero massimo di e-mail che Workfront Fusion deve restituire durante un ciclo di esecuzione di uno scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continua l'esecuzione della route anche se il modulo non restituisce alcun risultato]</td> 
   <td> <p> Seleziona questa opzione se desideri continuare a eseguire il modulo anche se non vengono restituiti risultati.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Contrassegna un&#39;e-mail come già letta]

Questo modulo di azione contrassegna un messaggio e-mail o una bozza in una cartella selezionata come già letti impostando il flag [!UICONTROL Leggi].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Seleziona la cartella contenente l’e-mail da contrassegnare come letta.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID e-mail (UID)]</p> </td> 
   <td> <p>Inserisci l’UID e-mail dell’e-mail che desideri contrassegnare come letta.</p> <p>Puoi ottenere l’UID dell’e-mail utilizzando il modulo E-mail &gt; E-mail di controllo o il modulo Ricerca .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Contrassegna un&#39;e-mail come non letta]

Contrassegna un messaggio e-mail o una bozza in una cartella selezionata come non letti impostando il flag Unread.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Seleziona la cartella contenente l’e-mail da contrassegnare come non letta. Esempio: primario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID e-mail (UID)]</p> </td> 
   <td> <p>Inserisci l’UID e-mail dell’e-mail che desideri contrassegnare come non letta.</p> <p>Puoi ottenere l’UID dell’e-mail utilizzando il modulo E-mail &gt; E-mail di controllo o il modulo Ricerca .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Sposta un&#39;e-mail]

Sposta un messaggio e-mail o una bozza selezionati in una cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a [!UICONTROL Workfront Fusion], vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Seleziona la cartella contenente l’e-mail che desideri spostare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cartella di destinazione]</td> 
   <td> <p> Seleziona la cartella a cui desideri aggiungere l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL ID e-mail (UID)]</p> </td> 
   <td> <p>Immetti l’UID e-mail dell’e-mail che desideri spostare nella cartella di destinazione.</p> <p>Puoi ottenere l’UID dell’e-mail utilizzando il modulo E-mail &gt; E-mail di controllo o il modulo Ricerca .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Invia un&#39;e-mail]

Invia una nuova e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account di posta elettronica a Workfront Fusion, vedere <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connettere l'indirizzo di posta elettronica a [!UICONTROL Workfront Fusion]</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Salva messaggio dopo l'invio]</td> 
   <td>Una volta inviato, il messaggio e-mail verrà salvato nella cassetta postale. Abilitare questa opzione se si desidera salvare le e-mail inviate tramite Workfront Fusion nella cartella <i>[!UICONTROL Sent mail]</i> o in un'altra cartella della cassetta postale. Alcuni servizi di posta elettronica, ad esempio [!DNL Gmail], salvano automaticamente i messaggi inviati.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL A] </td> 
   <td> <p>Aggiungi gli indirizzi e-mail a cui desideri inviare l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Inserisci o mappa l’oggetto dell’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tipo di contenuto]</p> </td> 
   <td> <p>Seleziona il tipo di contenuto  per l'e-mail:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Testo normale]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Inserisci o mappa il contenuto dell’e-mail in formato HTML utilizzando i tag HTML oppure nel testo normale, a seconda di ciò che hai scelto nel campo [!UICONTROL Content Type] (Tipo di contenuto).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Allegati]</p> </td> 
   <td> <p>Per ogni allegato che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Nome file]</strong> </p> <p>Immetti il nome del file, inclusa l’estensione. </p> </li> 
     <li> <p><strong>[!UICONTROL Dati]</strong> </p> <p>Immettere il percorso della cartella in cui si desidera caricare l'allegato.</p> </li> 
     <li> <p><strong>[!UICONTROL ID contenuto]</strong> </p> <p>Immetti l’ID contenuto per inserire l’allegato (immagine) nel contenuto.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia Destinatario] </td> 
   <td> <p>Per ogni indirizzo e-mail a cui desideri inviare una copia di questo messaggio, fai clic su <b>Aggiungi elemento</b> e immetti l'indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destinatario [!UICONTROL Blind Copy]</td> 
   <td> <p> Per ogni indirizzo di posta elettronica a cui si desidera inviare una copia di questa e-mail senza che l'indirizzo venga visualizzato nell'e-mail, fare clic su <b>Aggiungi elemento</b> e immettere l'indirizzo di posta elettronica.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Inserisci o mappa l’indirizzo e-mail visualizzato nel campo [!UICONTROL Sender] dell’e-mail.</p> <p>Suggerimento: se non si è sicuri di utilizzare questo campo o il campo Da, è consigliabile scegliere il campo Da.</p> <p>Importante: utilizzare la sintassi corretta: <code>name@email.com</code> o <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL - Risposta]</td> 
   <td> <p> Se si desidera che le risposte a questa e-mail vengano inviate a un indirizzo diverso da quello del mittente, immettere l'indirizzo e-mail a cui si desidera inviare le risposte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Se rispondi a un’e-mail specifica, inserisci o mappa l’ID dell’e-mail a cui stai rispondendo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Riferimenti] </td> 
   <td> <p>Immetti gli ID messaggio di tutte le risposte nel thread.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Priorità </p> </td> 
   <td> <p>Seleziona la priorità dell’e-mail:</p> 
    <ul> 
     <li>[!UICONTROL alto]</li> 
     <li>[!UICONTROL Normale]</li> 
     <li>[!UICONTROL Minimo]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Aggiungi le intestazioni:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Aggiungi la chiave. [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To] e così via.</p> </li> 
     <li> <p><strong>[!UICONTROL Valore]</strong> </p> <p>Immetti il valore per la chiave.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Da] </td> 
   <td> <p>Immetti o mappa l'indirizzo e-mail (e il nome, se necessario) che viene visualizzato nel campo [!UICONTROL Da] dell'e-mail. </p> <p>Importante: utilizzare la sintassi corretta: <code>name@email.com</code> o <code>"Name" name@email.com</code>.</p> <p>Nota: in genere, Workfront Fusion utilizza come indirizzo del mittente l’indirizzo e-mail inserito durante la creazione della connessione. Se inserisci un altro indirizzo e-mail, potrebbe verificarsi un errore durante l’invio di un messaggio, perché il tuo account potrebbe non disporre dell’autorizzazione per inviare e-mail da un indirizzo diverso dal tuo. Esempio: <code>test@mail.com</code> o "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iteratori

#### [!UICONTROL Itera Allegati]

Gli iterati hanno ricevuto gli allegati uno per uno.

Il modulo dell’iteratore e-mail consente di gestire separatamente gli allegati e-mail. Ad esempio, puoi impostare per controllare le e-mail in modo da iterare le e-mail con allegati e ricevere avvisi.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Modulo Source]</td> 
   <td> <p>Seleziona il modulo che restituisce l’e-mail con gli allegati che desideri iterare.</p> </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori informazioni sugli iteratori, vedere [Modulo iteratore](/help/workfront-fusion/references/modules/iterator-module.md).
