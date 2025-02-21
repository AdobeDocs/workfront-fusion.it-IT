---
title: Moduli diapositive di Google
description: I moduli delle diapositive di Adobe Workfront Fusion Google consentono di creare, aggiornare, elencare e/o eliminare presentazioni e caricare immagini nelle presentazioni nel proprio account Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: 5b88faa7fc3d501e543c1791eac02cbf2a690382
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 0%

---

# [!DNL Google Slides] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL Google Slides] ti consentono di creare, aggiornare, elencare e/o eliminare presentazioni e caricare immagini nelle presentazioni nel tuo account [!DNL Google Slides].

Per utilizzare [!DNL Google Slides] con [!DNL Workfront Fusion], è necessario disporre di un account [!DNL Google]. Se non si dispone ancora di un account [!DNL Google], è possibile crearne uno nella pagina della guida dell&#39;account [!DNL Google].

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

* [[!UICONTROL Watch Presentations]](#watch-presentations)
* [[!UICONTROL List Presentations]](#list-presentations)
* [[!UICONTROL Get a Presentation]](#get-a-presentation)
* [[!UICONTROL Get a Page/Thumbnail]](#get-a-pagethumbnail)
* [[!UICONTROL Create a Presentation From a Template]](#create-a-presentation-from-a-template)
* [[!UICONTROL Upload an Image To a Presentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Refresh a Chart]](#refresh-a-chart)
* [[!UICONTROL Add/Delete a Slide]](#adddelete-a-slide)

#### [!UICONTROL Watch Presentations]

Si attiva quando viene creata o aggiornata una nuova presentazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Seleziona l’opzione per guardare le presentazioni:</p> 
    <ul> 
     <li> <p>[!UICONTROL Created Date]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Il numero massimo di presentazioni che Workfront Fusion deve restituire durante un ciclo di esecuzione di uno scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Presentations]

Recupera un elenco di tutte le presentazioni.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Scegliere il percorso della cartella delle presentazioni da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Il numero massimo di presentazioni [!DNL Workfront Fusion] deve essere restituito durante un ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Presentation]

Ottiene la versione più recente di una presentazione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selezionare la presentazione che si desidera recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Page/Thumbnail]

Ottiene la versione più recente della pagina specificata o della miniatura di una pagina nella presentazione.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Seleziona l’ID presentazione da recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page Object ID]</td> 
   <td> <p> Selezionare la diapositiva per la quale si desidera visualizzare i dettagli dell'oggetto pagina.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Page Thumbnail]</td> 
   <td> <p> Selezionare la casella di controllo se si desidera visualizzare le informazioni sulle miniature della pagina.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Presentation From a Template]

Crea una nuova presentazione sostituendo tutti i tag come `{{Name}}`, `{{Email}}` in un modello con i dati forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Immettere un nome per la nuova presentazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy a Presentation]</td> 
   <td> <p> Selezionare l'opzione se si sta copiando una presentazione esistente:</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy of Existing Presentation ID]</td> 
   <td> <p> Immettere il Percorso o l'ID presentazione di una presentazione esistente che si desidera copiare. Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL By Mapping].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> <p>Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selezionare l'ID presentazione della presentazione che si desidera utilizzare come modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Aggiungi i valori:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: immetti il tag che desideri sostituire nella presentazione. Ad esempio: <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: immetti il valore con cui sostituire il tag esistente. Ad esempio, se una stringa <tr><ul><tr><tr><tr><code>&#123;&#123;Name&#125;&#125;/code> in the presentation and the replaced value is Sample, then the <code>&#123;&#123;Name&#125;&#125;</code> will be replaced by <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Select the [!DNL Google Drive] where you want to store or add the new presentation:</p> 
     
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader"> <p>[!UICONTROL New Document's Location]</p> </td> 
   <td> <p>Select the folder where you want to store or add the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Select if you want to share the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Enter the email address with whom you want to share the presentation. If you are not entering an email address and selecting only shared field, the presentation is shareable to anyone.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an Image To a Presentation]

Carica un’immagine con i dati forniti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Scegliere come selezionare la presentazione in cui si sta caricando un'immagine.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> <p>Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Seleziona l’ID presentazione della presentazione in cui stai caricando un’immagine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Valori Aggiungi i valori:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: immetti il tag al quale desideri aggiungere l’URL.</li> 
     <li><strong>[!UICONTROL Image URL]</strong>: immetti il percorso o l’URL dell’immagine da caricare.</li> 
    </ul> <p>Nota: le dimensioni delle immagini devono essere inferiori a 50 MB, a 25 megapixel e in formato PNG, JPEG o GIF.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Refresh a Chart]

Aggiorna i dati del grafico memorizzati in una presentazione specificata dall&#39;ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Selezionare l'ID presentazione della presentazione che include il grafico da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Selezionare il grafico da aggiornare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add/Delete a Slide]

Crea una diapositiva vuota o elimina una diapositiva esistente nella presentazione specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Scegliere se si desidera aggiungere una nuova diapositiva o eliminarla.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Selezionare l'ID presentazione della presentazione per la quale si desidera aggiungere o eliminare una diapositiva.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Selezionare il layout di diapositiva predefinito che si desidera utilizzare per la diapositiva aggiunta. Specificare i valori per i campi aggiuntivi, ad esempio [!UICONTROL Title].</p> 
    <ul> 
     <li>[!UICONTROL Blank layout, with no placeholders]</li> 
     <li>[!UICONTROL Layout with a caption at the bottom]</li> 
     <li>[!UICONTROL Layout with a title and subtitle]</li> 
     <li>[!UICONTROL Layout with a title and body]</li> 
     <li>[!UICONTROL Layout with a title and two columns]</li> 
     <li>[!UICONTROL Layout with only a title]</li> 
     <li>[!UICONTROL Layout with a section title]</li> 
     <li>[!UICONTROL Layout with a title and subtitle on one side and description on the other]</li> 
     <li>[!UICONTROL Layout with one title and one body, arranged in a single column]</li> 
     <li>[!UICONTROL Layout with a main point]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Questo campo è disponibile se si è selezionato di aggiungere una diapositiva.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Insert Links in a Presentation]](#insert-links-in-a-presentation)

#### [!UICONTROL Make an API Call]

Esegue una chiamata API autorizzata arbitraria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Immetti un percorso relativo a https://developers.google.com/slides/. Ad es. Presentazione.</p> <p>Per l'elenco degli endpoint disponibili, fare riferimento alla documentazione API <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides]</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Query String]</td> 
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

>[!INFO]
>
>**Esempio:** utilizzando una chiamata API è possibile ottenere i dettagli della presentazione per l&#39;ID presentazione immesso. È possibile trovare l&#39;ID presentazione nell&#39;URL quando si apre la presentazione in [!DNL Google Slides].
>
>![Esempio di chiamata API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)
>
>La seguente chiamata API restituisce i dettagli della presentazione:
>
>![Dettagli presentazione](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)
>
>Le corrispondenze della ricerca si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].
>
>Nel nostro esempio, sono stati restituiti i dettagli della presentazione richiesti:
>
>![Dettagli presentazione](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

#### [!UICONTROL Insert Links in a Presentation]

Questo modulo rende selezionabili tutti i collegamenti di una presentazione o inserisce un collegamento in tutti i testi di input corrispondenti.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google Slides] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Creare una connessione a [!DNL Adobe Workfront Fusion] - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Scegliere come selezionare la presentazione in cui si sta caricando un'immagine.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selezionare [!DNL Google Drive] dove si trovano le presentazioni da elencare:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Unità condivisa]</li> 
    </ul> <p>Questo campo viene visualizzato se si sta creando la presentazione [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Scegliere il percorso della cartella delle presentazioni da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Selezionare se si desidera rendere selezionabili tutti i collegamenti di una presentazione o se si desidera inserire un collegamento in tutti i testi di input corrispondenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text Inputs]</td> 
   <td>Per ogni elemento di testo per il quale si desidera aggiungere un collegamento, aggiungere all'elenco l'elemento e il relativo collegamento associato. Ogni volta che l'elemento viene visualizzato nella presentazione, verrà automaticamente collegato al sito specificato.</td> 
  </tr> 
 </tbody> 
</table>
