---
title: Moduli diapositive di Google
description: I moduli delle diapositive di Adobe Workfront Fusion Google consentono di creare, aggiornare, elencare e/o eliminare presentazioni e caricare immagini nelle presentazioni nel proprio account Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 0%

---

# [!DNL Google Slides] moduli

I moduli di Adobe Workfront Fusion [!DNL Google Slides] ti consentono di creare, aggiornare, elencare e/o eliminare presentazioni e caricare immagini nelle presentazioni nel tuo account [!DNL Google Slides].

Per utilizzare [!DNL Google Slides] con Workfront Fusion, è necessario disporre di un account [!DNL Google]. Se non si dispone ancora di un account [!DNL Google], è possibile crearne uno nella pagina della guida dell&#39;account [!DNL Google].

È inoltre necessario [!DNL Google Slides] in [!DNL Google Drive].

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
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Google Slides], è necessario disporre di un account [!DNL Google].

## Informazioni API per diapositive Google

Il connettore Diapositive Google utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides] moduli e relativi campi

Quando si configurano [!DNL Google Slides] moduli, in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Slides], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Presentazione](#presentation)
* [Altro](#other)

### Presentazione

* [[!UICONTROL Aggiungi/Elimina diapositiva]](#adddelete-a-slide)
* [[!UICONTROL Crea una presentazione da un modello]](#create-a-presentation-from-a-template)
* [[!UICONTROL Ottieni pagina/miniatura]](#get-a-pagethumbnail)
* [[!UICONTROL Ottieni una presentazione]](#get-a-presentation)
* [[!UICONTROL Elenca presentazioni]](#list-presentations)
* [[!UICONTROL Aggiorna grafico]](#refresh-a-chart)
* [[!UICONTROL Carica un&#39;immagine in una presentazione]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Guarda le presentazioni]](#watch-presentations)

#### [!UICONTROL Aggiungi/Elimina diapositiva]

Questo modulo di azione crea una diapositiva o elimina una diapositiva esistente nella presentazione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Selezionare il metodo]</td> 
   <td> <p>Scegliere se si desidera aggiungere una nuova diapositiva o eliminarla.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>Se si sta eliminando una diapositiva, selezionare se si desidera immettere manualmente l'ID diapositiva oppure selezionare la diapositiva da un elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Selezionare la presentazione o mappare l'ID presentazione della presentazione per la quale si desidera aggiungere o eliminare una diapositiva.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>Se si sta eliminando una diapositiva e si è scelto di inserire la diapositiva manualmente, immettere o mappare l'ID diapositiva. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di layout predefinito]</td> 
   <td> <p> Selezionare il layout di diapositiva predefinito che si desidera utilizzare per la diapositiva aggiunta. Specificare i valori per eventuali campi aggiuntivi, ad esempio [!UICONTROL Title].</p> 
    <ul> 
     <li>[!UICONTROL Layout vuoto, senza segnaposto]</li> 
     <li>[!UICONTROL Layout con una didascalia in basso]</li> 
     <li>[!UICONTROL Layout con titolo e sottotitolo]</li> 
     <li>[!UICONTROL Layout con titolo e corpo]</li> 
     <li>[!UICONTROL Layout con titolo e due colonne]</li> 
     <li>[!UICONTROL Layout con solo un titolo]</li> 
     <li>[!UICONTROL Layout con titolo sezione]</li> 
     <li>[!UICONTROL Layout con titolo e sottotitolo su un lato e descrizione sull'altro]</li> 
     <li>[!UICONTROL Layout con un titolo e un corpo, disposti in una singola colonna]</li> 
     <li>[!UICONTROL Layout con un punto principale]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Questo campo è disponibile se si è selezionato di aggiungere una diapositiva.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Immettere o mappare il contenuto di testo per la diapositiva. I campi sono disponibili in base al modello selezionato.</p> <p>Questo campo è disponibile se si è selezionato di aggiungere una diapositiva.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea una presentazione da un modello]

Questo modulo di azione crea una nuova presentazione copiando una presentazione e sostituendo tutti i tag come `{{Name}}`, `{{Email}}` in con i dati forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Immettere un nome per la nuova presentazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia presentazione]</td> 
   <td> <p> Selezionare l'opzione se si sta copiando una presentazione esistente:</p> 
    <ul> 
     <li>[!UICONTROL Per Mappatura]</li> 
     <li>[!UICONTROL Per Elenco A Discesa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copia dell'ID presentazione esistente]</td> 
   <td> <p> Immettere il Percorso o l'ID presentazione di una presentazione esistente che si desidera copiare. Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL By Mapping].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un'unità]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> <p>Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL Per elenco a discesa].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p> Selezionare la presentazione oppure immettere o mappare l'ID presentazione della presentazione che si desidera utilizzare come modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Aggiungi i valori:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: immettere il tag che si desidera sostituire nella presentazione. Ad esempio: <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: immetti il valore con cui sostituire il tag esistente. Ad esempio, se una stringa <code>&#123;&#123;Name&#125;&#125;</code> nella presentazione e il valore sostituito è Sample, <code>&#123;&#123;Name&#125;&#125;</code> verrà sostituito da <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nuovo Percorso Unità]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si desidera archiviare o aggiungere la nuova presentazione:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Posizione nuovo documento]</p> </td> 
   <td> <p>Selezionare la cartella in cui archiviare o aggiungere la presentazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL condiviso] </td> 
   <td> <p>Selezionare se si desidera condividere la presentazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Immettere l'indirizzo di posta elettronica con cui si desidera condividere la presentazione. Se abiliti l’opzione Condiviso senza inserire un messaggio e-mail in questo campo, la presentazione sarà condivisibile con chiunque.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni pagina/miniatura]

Questo modulo di azione ottiene la versione più recente della pagina specificata o della miniatura di una pagina nella presentazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci una presentazione e un ID pagina]</td> 
   <td> <p> Scegli se inserire manualmente una presentazione e un ID pagina o selezionali da un elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p> Seleziona l’ID presentazione da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID oggetto pagina]</td> 
   <td> <p> Selezionare la diapositiva per la quale si desidera visualizzare i dettagli dell'oggetto pagina.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mostra miniatura pagina]</td> 
   <td> <p> Selezionare la casella di controllo se si desidera visualizzare le informazioni sulle miniature della pagina.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni una presentazione]

Questo modulo di azione ottiene la versione più recente di una presentazione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un'unità]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p> Selezionare la presentazione che si desidera recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca presentazioni]

Questo modulo recupera un elenco di tutte le presentazioni nella posizione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un percorso unità]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID cartella]</td> 
   <td> <p>Scegliere il percorso della cartella delle presentazioni da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di presentazioni che il modulo deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna grafico]

Questo modulo di azione aggiorna i dati del grafico memorizzati in una presentazione specificata da ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci un ID presentazione]</td> 
   <td> <p> Scegli se inserire manualmente un ID presentazione o selezionarlo da un elenco.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un'unità]</td> 
   <td> <p>Se si seleziona la presentazione da un elenco, selezionare [!DNL Google Drive] in cui si trovano le presentazioni che si desidera elencare:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p>Selezionare la presentazione oppure immettere o mappare l'ID presentazione della presentazione che include il grafico che si desidera aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID oggetto grafico]</td> 
   <td> <p> Se immetti i dati manualmente, immetti o mappa l’ID del grafico che desideri aggiornare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Carica un&#39;immagine in una presentazione]

Carica un’immagine con i dati forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli presentazione]</td> 
   <td> <p>Scegliere come selezionare la presentazione in cui si sta caricando un'immagine.</p> 
    <ul> 
     <li>[!UICONTROL Per Mappatura]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un'unità]</td> 
   <td> <p>Se si sceglie da un elenco a discesa, selezionare [!DNL Google Drive] dove si trova la presentazione a cui si desidera aggiungere un'immagine:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p> Seleziona l’ID presentazione della presentazione in cui stai caricando un’immagine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona il metodo]</td> 
   <td> <p> Selezionare la modalità di sostituzione dell'immagine.</p>
   <ul>
   <li><p><b>Caricare un’immagine sostituendo un tag di testo</b></p><p>Nel campo Valori, per ogni immagine da caricare, fare clic su <b>Aggiungi elemento</b> e immettere il tag dell'immagine e l'URL della nuova immagine.</p></li>
   <li><p><b>Carica un’immagine sostituendola</b></p><p>Nel campo Valori, per ogni immagine da caricare, fare clic su <b>Aggiungi elemento</b> e immettere l'ID oggetto, il metodo replace e l'URL della nuova immagine.</p></li>
   </ul>
  <p>Nota: le dimensioni delle immagini devono essere inferiori a 50 MB, a 25 megapixel e in formato PNG, JPEG o GIF.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Guarda le presentazioni]

Questo modulo di attivazione avvia uno scenario quando viene creata o aggiornata una nuova presentazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Seleziona l’opzione per guardare le presentazioni:</p> 
    <ul> 
     <li> <p>[!UICONTROL Data di creazione]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Immettere o mappare il numero massimo di presentazioni che Workfront Fusion deve restituire durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Inserire collegamenti in una presentazione]](#insert-links-in-a-presentation)
* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)

#### [!UICONTROL Inserire collegamenti in una presentazione]

Questo modulo rende selezionabili tutti i collegamenti di una presentazione o inserisce un collegamento in tutti i testi di input corrispondenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli presentazione]</td> 
   <td> <p>Scegliere come selezionare la presentazione in cui si sta caricando un'immagine.</p> 
    <ul> 
     <li>[!UICONTROL Per Mappatura]</li> 
     <li>[!UICONTROL Per Elenco A Discesa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli un'unità]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL Unità]</li> 
     <li>[!UICONTROL condiviso con me]</li> 
     <li>[!UICONTROL [!DNL Google] unità condivisa]</li> 
    </ul> <p>Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL Per elenco a discesa].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID presentazione]</td> 
   <td> <p>Scegliere il percorso della cartella delle presentazioni da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Selezionare se si desidera rendere selezionabili tutti i collegamenti di una presentazione o se si desidera inserire un collegamento in tutti i testi di input corrispondenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Testo]</td> 
   <td>Se si inserisce un collegamento, per ogni elemento di testo per cui si desidera aggiungere un collegamento fare clic su <b>Aggiungi elemento</b> e immettere il testo e il collegamento associato. Ogni volta che l'elemento viene visualizzato nella presentazione, viene automaticamente collegato al sito specificato.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

Esegue una chiamata API autorizzata arbitraria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Immettere un percorso relativo a <code>https://developers.google.com/slides/</code>. Ad es. Presentazione.</p> <p>Per l'elenco degli endpoint disponibili, fare riferimento alla documentazione API <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Inserisci le intestazioni di richiesta desiderate. Non è necessario aggiungere intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa Di Query]</td> 
   <td> <p> Immettere la stringa di query richiesta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Aggiungi il contenuto body per la chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando si utilizzano istruzioni condizionali come <code>if</code> nel JSON, inserire le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Esempio:** utilizzando una chiamata API è possibile ottenere i dettagli della presentazione per l&#39;ID presentazione immesso. È possibile trovare l&#39;ID presentazione nell&#39;URL quando si apre la presentazione in [!DNL Google Slides].

![Esempio di chiamata API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

La seguente chiamata API restituisce i dettagli della presentazione:

![Dettagli presentazione](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Le corrispondenze della ricerca si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].

Nel nostro esempio, sono stati restituiti i dettagli della presentazione richiesti:

![Dettagli presentazione](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
