---
title: Moduli Google Docs
description: I moduli di Adobe Workfront Fusion [!DNL Google Docs] ti consentono di monitorare, creare, modificare e recuperare documenti nei tuoi [!DNL Google Docs] e [!DNL Google Docs] (per [!DNL Google Workspace] utenti).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '3215'
ht-degree: 0%

---

# [!DNL Google Docs] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL Google Docs] consentono di monitorare, creare, modificare e recuperare i documenti in [!DNL Google Docs] e [!DNL Google Docs] (per [!DNL Google Workspace] utenti).

Per utilizzare [!DNL Google Docs] con [!DNL Adobe Workfront Fusion], è necessario disporre di un account [!DNL Google]. Se non si dispone ancora di un account [!DNL Google], è possibile crearne uno nella pagina della guida dell&#39;account [!DNL Google].

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

Per utilizzare i moduli [!DNL Google Docs], è necessario disporre di un account Google.

## Informazioni API di Google Docs

Il connettore Google Docs utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://docs.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.4.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Docs] moduli e relativi campi

Quando configuri [!DNL Google Docs] moduli, [!UICONTROL Workfront Fusion] visualizza i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati ulteriori campi di [!DNL Google Docs], a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Documento

* [[!UICONTROL Watch Documents]](#watch-documents)
* [[!UICONTROL List Documents]](#list-documents)
* [[!UICONTROL Get Content of a Document]](#get-content-of-a-document)
* [[!UICONTROL Create a Document]](#create-a-document)
* [[!UICONTROL Create a Document From a Template]](#create-a-document-from-a-template)
* [[!UICONTROL Insert a Paragraph to a Document]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL Insert an Image to a Document]](#insert-an-image-to-a-document)
* [[!UICONTROL Replace an Image with a New Image]](#replace-an-image-with-a-new-image)
* [[!UICONTROL Replace Text in a Document]](#replace-text-in-a-document)
* [[!UICONTROL Download a Document]](#download-a-document)
* [[!UICONTROL Delete a Document]](#delete-a-document)

#### [!UICONTROL Watch Documents]

Questo modulo di attivazione restituisce i dettagli del documento quando viene creato o modificato un nuovo documento nella cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Documents]</td> 
   <td> <p style="color: #000000;">Specificare se si desidera controllare i documenti creati ([!UICONTROL By Created Date]) o modificati ([!UICONTROL By Modified Date]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità che si desidera monitorare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella da controllare per i documenti creati o modificati.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella da controllare per i documenti creati o modificati.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa che si desidera controllare.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Shared Drive] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di documenti restituiti da Workfront Fusion in un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Documents]

Questo modulo di azione recupera un elenco di documenti dalla cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità da cui elencare i documenti.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella da cui si desidera elencare i documenti.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella da cui si desidera elencare i documenti.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa da cui elencare i documenti.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di documenti [!DNL Workfront Fusion] restituiti in un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Content of a Document]

Questo modulo di azione recupera un documento specificato.

Potrebbe essere necessario estendere le autorizzazioni.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get Content of a Document]</td> 
   <td> <p>Specificare se si desidera mappare l'ID documento del documento oppure selezionare manualmente il documento dal menu a discesa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità contenente il documento che si desidera recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella contenente il documento che si desidera recuperare.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella contenente il documento che si desidera recuperare.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa contenente il documento che si desidera recuperare.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Selezionare l'oggetto da restituire nell'output del modulo.</p> 
    <ul> 
     <li>[!UICONTROL Image] (impostazione predefinita)</li> 
     <li>[!UICONTROL Drawing]</li> 
     <li>[!UICONTROL Chart]</li> 
    </ul> <p>Nota:  <p>Per ulteriori mappature di questi oggetti, utilizzare il valore [!UICONTROL Inline Objects Array] nell'output di questo modulo (anziché [!UICONTROL inlineObjects]).</p> <p>Gli oggetti [!UICONTROL Inline Objects Array] vengono ordinati nello stesso ordine in cui vengono visualizzati nel documento. Semplificherà l’ulteriore elaborazione.</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Document]

Questo modulo consente di creare un nuovo documento nella cartella selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere il nome del documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td> <p>Immettere il contenuto del documento. HTML è supportato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si desidera creare un documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si desidera creare un documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si desidera creare un documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si desidera creare un documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Insert a Header]</td> 
   <td> <p> Abilitare questa opzione per inserire l'intestazione nel documento, quindi immettere o mappare il testo dell'intestazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Insert a Footer] </td> 
   <td> <p>Abilitare questa opzione per inserire il piè di pagina nel documento, quindi immettere o mappare il testo dell'intestazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Document From a Template]

Questo modulo di azione crea una copia di un documento modello esistente e sostituisce eventuali tag. Questo modulo consente inoltre agli utenti di sostituire le immagini con nuove immagini tramite URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Create a Document from a Template]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>Selezionare questa opzione per scegliere il modello di documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il modello. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Seleziona la cartella in cui si trova il modello.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Seleziona la cartella in cui si trova il modello.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il modello.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Immettere i valori che verranno immessi al posto delle variabili nel nuovo documento.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tags]</strong> <br>Immettere i tag contenuti nel modello di documento. Non utilizzare <code>&#123;&#123;&#125;&#125;</code>. Esempio: utilizzare <code>name</code> invece di <code>&#123;&#123;name&#125;&#125;</code>.</li> 
     <li><strong>[!UICONTROL Replaced Value]</strong><br>Immetti il valore del tag.</li> 
    </ul> <p>Ad esempio, la variabile <code> &#123;&#123;name&#125;&#125;</code> nel documento di origine verrà visualizzata come campo del nome in cui è possibile inserire il valore, ad esempio <code>John</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Images Replacement]</p> </td> 
   <td> <p>Immettere il collegamento a [!UICONTROL Image Object ID] e [!UICONTROL Image URL] che sostituiranno l'immagine corrente.</p> <p>Nota: è possibile recuperare gli ID immagine utilizzando il modulo [!UICONTROL Get a Document], in cui gli ID sono contenuti nell'array [!UICONTROL Inline Object Array].</p> <p>È consigliabile aggiungere testo ALT alle immagini del documento [!DNL Google]. </p> <p>Per aggiungere un testo ALT all'immagine [!DNL Google Docs]:</p> 
    <ol> 
     <li value="1">Fai clic con il pulsante destro del mouse sull’immagine.</li> 
     <li value="2">Selezionare l'opzione [!UICONTROL ALT text].</li> 
     <li value="3">Immettere [!UICONTROL ALT text] nel campo [!UICONTROL Title] e fare clic su [!UICONTROL OK].</li> 
    </ol> <p>Dopo aver aggiunto il testo ALT all'immagine, il testo ALT viene visualizzato tra parentesi nel nome del campo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Immettere il nome del nuovo documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il modello. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui creare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui creare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui creare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Insert a Paragraph to a Document]

Questo modulo di azione aggiunge o inserisce un nuovo paragrafo in un documento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere un paragrafo. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un paragrafo, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un paragrafo, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere un paragrafo, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Insert a Paragraph]</p> </td> 
   <td> <p>Selezionare la modalità di inserimento del nuovo testo nel documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By specification of location]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Immettere il numero di indice in cui si desidera inserire il testo. È possibile utilizzare il modulo [!UICONTROL Get a Document] per recuperare il numero di indice.</p> <p>Per visualizzare tutti i caratteri (inclusi quelli nascosti) nel documento, è possibile utilizzare il componente aggiuntivo [!UICONTROL Show]. È possibile trovare il componente aggiuntivo in [!UICONTROL Add-ons] &gt; [!UICONTROL Get add-ons]. Cercare [!UICONTROL Show] e installare il componente aggiuntivo [!UICONTROL Show].</p> </li> 
         <li> <p><strong>[!UICONTROL Inserted text]</strong> </p> <p>Immettere il testo da inserire nel documento.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL By segment ID]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire il contenuto di testo e immettere il testo da inserire nei campi corrispondenti.</p> <p>Se l'intestazione o il piè di pagina contiene già del testo, il nuovo testo verrà aggiunto prima del testo esistente.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL By appending to the body of the document]</strong> </p> <p>Aggiunge il testo immesso alla fine del contenuto del corpo del documento.</p> <p>Lo stile del nuovo paragrafo verrà copiato dal paragrafo nell'indice di inserimento corrente, inclusi elenchi e punti elenco.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to the end of segment (Header and Footer)]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire il contenuto di testo e immettere il testo da inserire nei campi corrispondenti.</p> <p>Se l'intestazione o il piè di pagina contiene già del testo, il nuovo testo verrà aggiunto dopo il testo esistente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Appended Text]</td> 
   <td>Immettere o mappare il testo da aggiungere al documento</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Insert an Image to a Document]

Questo modulo di azione inserisce un’immagine dall’URL al documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere un'immagine. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un'immagine, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un'immagine, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere un'immagine, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Insert an Image]</p> </td> 
   <td> <p>Selezionare la modalità di inserimento della nuova immagine nel documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By specification of location]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Immettere il numero di indice in cui si desidera inserire l'immagine. È possibile utilizzare il modulo [!UICONTROL Get a Document] per recuperare [!UICONTROL Index number].</p> <p>Per visualizzare tutti i caratteri (inclusi quelli nascosti) nel documento, è possibile utilizzare il componente aggiuntivo [!UICONTROL Show]. È possibile trovare il componente aggiuntivo in [!UICONTROL Add-ons] &gt; [!UICONTROL Get add-ons]. Cercare [!UICONTROL Show] e installare il componente aggiuntivo [!UICONTROL Show].</p> </li> 
         <li> <p><strong>[!UICONTROL Image URL]</strong> </p> <p>Immettere l'URL dell'immagine da inserire nel documento.</p> <p>La dimensione massima dell'immagine è di 50 MB. Non deve superare i 25 megapixel. È supportato solo il formato PNG, JPEG o GIF.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL By segment ID]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire l'immagine e immettere l'URL dell'immagine nei campi corrispondenti.</p> <p>La dimensione massima dell'immagine è di 50 MB. L’immagine non deve superare i 25 megapixel. È supportato solo il formato PNG, JPEG o GIF.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL By appending to the body of the document]</strong> </p> <p>Aggiunge un'immagine specifica alla fine del contenuto del corpo del documento.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to the end of segment (Header and Footer)]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire un'immagine e immettere l'URL dell'immagine da inserire nei campi corrispondenti.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Height Magnitude in Points/Width Magnitude in Points]</p> </td> 
   <td> <p>Definire le dimensioni dell'immagine inserita. Le proporzioni vengono mantenute.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace an Image with a New Image]

Questo modulo sostituisce un’immagine esistente. Vengono mantenute le proporzioni dell&#39;immagine originale.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento che si desidera sostituire. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Image URL]</p> </td> 
   <td> <p>Inserisci o mappa l’URL della nuova immagine che sostituirà l’immagine esistente.</p> <p>Le immagini sono elencate nell'ordine in cui compaiono nel documento. <code>Body: Image No. 1</code> è ad esempio la prima immagine del documento.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace Text in a Document]

Questo modulo di azione sostituisce il testo di un documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere il testo. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace a Text]</p> </td> 
   <td> <p>Aggiungere ogni testo da sostituire.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Old text to be replaced]</strong> </p> <p>Immettere il testo che si desidera sostituire.</p> </li> 
     <li> <p><strong>[!UICONTROL New text to be inserted]</strong> </p> <p>Immettere il nuovo testo.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a Document]

Questo modulo consente di convertire e scaricare il documento selezionato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento da scaricare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Selezionare il formato di file di destinazione del documento scaricato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Document]

Questo modulo di azione elimina un documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento che si desidera eliminare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Selezionare l'unità contenente il documento che si desidera scaricare, quindi selezionare un documento. Questa opzione è disponibile se hai selezionato [!DNL Google Docs] nel campo [!UICONTROL Choose a Drive].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p> Selezionare o mappare il documento in cui si desidera sostituire una o più immagini.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Make All Links in a Document Clickable]](#make-all-links-in-a-document-clickable)

#### [!UICONTROL Make an API Call]

Questo modulo di azione ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Immettere un percorso relativo a <code>https://docs.googleapis.com/</code>. Esempio: <code>/v1/documents/{presentationID}</code>. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Metodi di richiesta HTTP</a>.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard. Ad esempio, <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] aggiunge le intestazioni di autorizzazione.</p> </td> 
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

**Esempio:** La chiamata API seguente recupera i dettagli del documento specificato nel Google Docs:

**URL:**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**Metodo:**

[!UICONTROL GET]

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

I dettagli del documento recuperato si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Body].

![](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

#### [!UICONTROL Make All Links in a Document Clickable]

Questo modulo di azione trova tutti i collegamenti nel documento e li rende cliccabili.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Google] a [!DNL Workfront Fusion], vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Make All Links in a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti. Questa opzione è disponibile se hai selezionato [!UICONTROL By Dropdown] nel campo precedente.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Selezionare la cartella in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti, quindi selezionare il documento.</p> </li> 
     <li> <p>Unità condivisa <strong>[!UICONTROL [!DNL Google]]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Use Domain Admin Access]. Se si seleziona [!UICONTROL Yes], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Selezionare l'unità contenente il documento in cui si desidera aggiornare i collegamenti, quindi selezionare un documento. Questa opzione è disponibile se hai selezionato [!DNL Google Docs] in [!UICONTROL Choose a Drive field].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p> Selezionare o mappare il documento in cui si desidera aggiornare i collegamenti.</p> </td> 
  </tr> 
 </tbody> 
</table>
