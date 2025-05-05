---
title: Moduli Google Docs
description: I moduli di Adobe Workfront Fusion [!DNL Google Docs] ti consentono di monitorare, creare, modificare e recuperare documenti nei tuoi [!DNL Google Docs] e [!DNL Google Docs] (per [!DNL Google Workspace] utenti).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: 2af808aaf8136253c623ee65641d0e57d4f6cf10
workflow-type: tm+mt
source-wordcount: '4045'
ht-degree: 0%

---

# [!DNL Google Docs] moduli

I moduli [!DNL Adobe Workfront Fusion] [!DNL Google Docs] consentono di monitorare, creare, modificare e recuperare i documenti in [!DNL Google Docs] e [!DNL Google Docs] (per [!DNL Google Workspace] utenti).

Per utilizzare [!DNL Google Docs] con [!DNL Adobe Workfront Fusion], è necessario disporre di un account [!DNL Google]. Se non si dispone ancora di un account [!DNL Google], è possibile crearne uno nella pagina della guida dell&#39;account [!DNL Google].

Per istruzioni sulla creazione di uno scenario, vedere gli articoli in [Creare scenari: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

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

* [[!UICONTROL Crea un documento]](#create-a-document)
* [[!UICONTROL Crea documento da modello]](#create-a-document-from-a-template)
* [[!UICONTROL Elimina documento]](#delete-a-document)
* [[!UICONTROL Scarica un documento]](#download-a-document)
* [[!UICONTROL Ottieni contenuto di un documento]](#get-content-of-a-document)
* [[!UICONTROL Inserire un paragrafo in un documento]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL Inserire un&#39;immagine in un documento]](#insert-an-image-to-a-document)
* [[!UICONTROL Elenca documenti]](#list-documents)
* [[!UICONTROL Sostituisci testo in un documento]](#replace-text-in-a-document)
* [[!UICONTROL Sostituisci un&#39;immagine con una nuova immagine]](#replace-an-image-with-a-new-image)
* [[!UICONTROL Guarda i documenti]](#watch-documents)

#### [!UICONTROL Crea un documento]

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
   <td> <p>Immettere un nome per il documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td> <p>Immettere il contenuto del documento. È possibile includere HTML per formattare il documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si desidera creare un documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Nel campo Posizione nuovo documento selezionare la cartella in cui si desidera creare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Nel campo Posizione nuovo documento selezionare la cartella in cui si desidera creare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si desidera creare un documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci intestazione]</td> 
   <td> <p> Abilitare questa opzione per inserire l'intestazione nel documento, quindi immettere o mappare il testo dell'intestazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Inserisci piè di pagina] </td> 
   <td> <p>Abilitare questa opzione per inserire il piè di pagina nel documento, quindi immettere o mappare il testo dell'intestazione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Crea documento da modello]

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
   <td role="rowheader"> <p>[!UICONTROL Crea un documento da un modello]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL Per Elenco a discesa]</strong> <br>Selezionare questa opzione per scegliere il modello di documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il modello. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p>  </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il modello.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Mappa l’ID del modello se hai selezionato In base a mappatura oppure seleziona il percorso del modello e del modello.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Per ogni tag per cui si desidera immettere un valore, fare clic su <b>Aggiungi elemento</b>, immettere il tag e immettere il valore che verrà immesso al posto del tag nel nuovo documento.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tags]</strong> <br>Immettere i tag contenuti nel modello di documento. Non utilizzare <code>&#123;&#123;&#125;&#125;</code>. Esempio: utilizzare <code>name</code> invece di <code>&#123;&#123;name&#125;&#125;</code>.</li> 
     <li><strong>[!UICONTROL Replaced Value]</strong><br>Immettere il valore del tag.</li> 
    </ul> <p>Ad esempio, la variabile <code> &#123;&#123;name&#125;&#125;</code> nel documento di origine verrà visualizzata come campo del nome in cui è possibile inserire il valore, ad esempio <code>John</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Immagini Sostituzione]</p> </td> 
   <td> <p>&gt;Per ogni tag per cui si desidera immettere un valore, fare clic su <b>Aggiungi elemento</b>, quindi immettere il collegamento all'[!UICONTROL ID oggetto immagine] e all'[!UICONTROL URL immagine] che sostituiranno l'immagine corrente.</p> <p>Nota: è possibile recuperare gli ID immagine utilizzando il modulo [!UICONTROL Get a Document], in cui gli ID sono contenuti nell'array [!UICONTROL Inline Object Array].</p> <p>È consigliabile aggiungere testo ALT alle immagini del documento [!DNL Google]. </p> <p>Per aggiungere un testo ALT all'immagine [!DNL Google Docs]:</p> 
    <ol> 
     <li value="1">Fai clic con il pulsante destro del mouse sull’immagine.</li> 
     <li value="2">Selezionare l'opzione [!UICONTROL ALT text].</li> 
     <li value="3">Immettere il testo ALT  nel campo Titolo  e fare clic su [!UICONTROL OK].</li> 
    </ol> <p>Dopo aver aggiunto il testo ALT all'immagine, il testo ALT viene visualizzato tra parentesi nel nome del campo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Immettere il nome del nuovo documento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il modello. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui creare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui creare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui creare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina documento]

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
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento che si desidera eliminare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera eliminare, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Unità condivisa]</td> 
   <td> <p>Selezionare l'unità contenente il documento che si desidera scaricare, quindi selezionare un documento. Questa opzione è disponibile se hai selezionato [!DNL My Drive] nel campo [!UICONTROL Scegli un'unità].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p> Selezionare o mappare il documento che si desidera eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Scarica un documento]

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
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento da scaricare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Nel campo ID documento selezionare la cartella in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Nel campo ID documento selezionare la cartella in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera scaricare, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Selezionare il formato di file di destinazione del documento scaricato.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni contenuto di un documento]

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
   <td role="rowheader">[!UICONTROL Ottieni contenuto di un documento]</td> 
   <td> <p>Specificare se si desidera mappare l'ID documento del documento oppure selezionare manualmente il documento dal menu a discesa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità contenente il documento che si desidera recuperare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella contenente il documento che si desidera recuperare.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella contenente il documento che si desidera recuperare.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa contenente il documento che si desidera recuperare.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Immettere o selezionare il documento che si desidera recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filtro]</p> </td> 
   <td> <p>Selezionare l'oggetto da restituire nell'output del modulo.</p> 
    <ul> 
     <li>[!UICONTROL Image] (impostazione predefinita)</li> 
     <li>[!UICONTROL Drawing]</li> 
     <li>Grafico </li> 
    </ul> <p>Nota:  <p>Per eseguire ulteriori mapping di questi oggetti, utilizzare il valore [!UICONTROL Inline Objects Array] nell'output di questo modulo (anziché [!UICONTROL inlineObjects]).</p> <p>Gli oggetti [!UICONTROL Inline Objects Array] vengono ordinati nello stesso ordine in cui vengono visualizzati nel documento. Semplificherà l’ulteriore elaborazione.</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Inserire un paragrafo in un documento]

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
   <td role="rowheader"> <p>[!UICONTROL Seleziona documento]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per eseguire il mapping del documento.</li> 
     <li><strong>[!UICONTROL Per elenco a discesa]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere un paragrafo. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un paragrafo.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un paragrafo.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere un paragrafo, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Mappare o selezionare il documento in cui si desidera inserire il testo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Inserisci paragrafo]</p> </td> 
   <td> <p>Selezionare la modalità di inserimento del nuovo testo nel documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL In base alla specifica della posizione]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Per indice]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Indice]</strong> </p> <p>Immettere il numero di indice in cui si desidera inserire il testo. È possibile utilizzare il modulo [!UICONTROL Get a Document] per recuperare il numero di indice.</p> </li> 
         <li> <p><strong>[!UICONTROL Inserito testo]</strong> </p> <p>Immettere il testo da inserire nel documento.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL Per ID segmento]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire il contenuto di testo e immettere il testo da inserire nei campi corrispondenti.</p> <p>Se l'intestazione o il piè di pagina contiene già del testo, il nuovo testo verrà aggiunto prima del testo esistente.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Aggiungendo al corpo del documento]</strong> </p> <p>Aggiunge il testo immesso alla fine del contenuto del corpo del documento.</p> <p>Lo stile del nuovo paragrafo verrà copiato dal paragrafo nell'indice di inserimento corrente, inclusi elenchi e punti elenco.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Aggiungendo alla fine del segmento (intestazione e piè di pagina)]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire il contenuto di testo e immettere il testo da inserire nei campi corrispondenti.</p> <p>Se l'intestazione o il piè di pagina contiene già del testo, il nuovo testo verrà aggiunto dopo il testo esistente.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo Aggiunto]</td> 
   <td>Immettere o mappare il testo da aggiungere al documento</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Inserire un&#39;immagine in un documento]

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
   <td role="rowheader"> <p>[!UICONTROL Seleziona documento]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL Per elenco a discesa]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere un'immagine. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un'immagine.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere un'immagine.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere un'immagine, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Mappare o selezionare il documento in cui si desidera inserire un'immagine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL - Inserisci immagine]</p> </td> 
   <td> <p>Selezionare la modalità di inserimento della nuova immagine nel documento.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL In base alla specifica della posizione]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Per indice]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Indice]</strong> </p> <p>Immettere il numero di indice in cui si desidera inserire l'immagine. È possibile utilizzare il modulo [!UICONTROL Get a Document] per recuperare il numero di indice .</p>  </li> 
         <li> <p><strong>[!UICONTROL URL immagine]</strong> </p> <p>Immettere l'URL dell'immagine da inserire nel documento.</p> <p>La dimensione massima dell'immagine è di 50 MB. Non deve superare i 25 megapixel. È supportato solo il formato PNG, JPEG o GIF.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL Per ID segmento]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire l'immagine e immettere l'URL dell'immagine nei campi corrispondenti.</p> <p>La dimensione massima dell'immagine è di 50 MB. L’immagine non deve superare i 25 megapixel. È supportato solo il formato PNG, JPEG o GIF.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Aggiungendo al corpo del documento]</strong> </p> <p>Aggiunge un'immagine specifica alla fine del contenuto del corpo del documento.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Aggiungendo alla fine del segmento (intestazione e piè di pagina)]</strong> </p> <p>Selezionare l'intestazione e il piè di pagina a cui si desidera inserire un'immagine e immettere l'URL dell'immagine da inserire nei campi corrispondenti.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Altezza in punti/Larghezza Grandezza in punti]</p> </td> 
   <td> <p>Definite l'altezza o la larghezza dell'immagine inserita. Le proporzioni vengono mantenute.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca documenti]

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
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità da cui elencare i documenti.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella da cui si desidera elencare i documenti.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella da cui si desidera elencare i documenti.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa da cui elencare i documenti.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di documenti [!DNL Workfront Fusion] restituiti in un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Sostituisci testo in un documento]

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
   <td role="rowheader"> <p>[!UICONTROL Seleziona documento]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL Per elenco a discesa]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento a cui si desidera aggiungere il testo. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento a cui si desidera aggiungere il testo, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Mappare o selezionare il documento in cui si desidera sostituire il testo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sostituisci testo]</p> </td> 
   <td> <p>Per ogni parte di testo che si desidera sostituire, fare clic su <b>Aggiungi elemento</b> e immettere quanto segue:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Vecchio testo da sostituire]</strong> </p> <p>Immettere il testo che si desidera sostituire.</p> </li> 
     <li> <p><strong>[!UICONTROL Nuovo testo da inserire]</strong> </p> <p>Immettere il nuovo testo.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Sostituisci un&#39;immagine con una nuova immagine]

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
   <td role="rowheader"> <p>[!UICONTROL Seleziona documento]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL Per elenco a discesa]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento che si desidera sostituire. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento che si desidera sostituire, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p>Mappare o selezionare il documento in cui si desidera sostituire un'immagine.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Immagini sostituzione]</p> </td> 
   <td> Per ogni immagine da sostituire, fare clic su <b>Aggiungi elemento</b> e immettere l'ID immagine esistente, quindi immettere o mappare l'URL della nuova immagine che sostituirà l'immagine esistente. <p>Le immagini sono elencate nell'ordine in cui compaiono nel documento. <code>Body: Image No. 1</code> è ad esempio la prima immagine del documento.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Guarda i documenti]

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
   <td role="rowheader">[!UICONTROL - Osserva documenti]</td> 
   <td> <p style="color: #000000;">Seleziona se desideri guardare i documenti creati ([!UICONTROL By Created Date]) o modificati ([!UICONTROL By Modified Date]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità che si desidera monitorare.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella da controllare per i documenti creati o modificati.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella da controllare per i documenti creati o modificati.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa che si desidera controllare.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Shared Drive] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Impostare il numero massimo di documenti restituiti da Workfront Fusion in un ciclo di esecuzione.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

* [[!UICONTROL Rendere selezionabili tutti i collegamenti in un documento]](#make-all-links-in-a-document-clickable)
* [[!UICONTROL Effettuare una chiamata API]](#make-an-api-call)

#### [!UICONTROL Rendere selezionabili tutti i collegamenti in un documento]

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
   <td role="rowheader"> <p>[!UICONTROL Crea tutti i collegamenti in un documento]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Selezionare questa opzione per mappare il modello di documento.</li> 
     <li><strong>[!UICONTROL Per elenco a discesa]</strong> <br> Selezionare questa opzione per scegliere il documento dal menu a discesa.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scegli unità]</td> 
   <td> <p>Selezionare il tipo di unità in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti. Questa opzione è disponibile se nel campo precedente è stato selezionato [!UICONTROL Per elenco a discesa].</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Unità]</strong> </p> <p>Selezionare la cartella in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti.</p> </li> 
     <li> <p><strong>[!UICONTROL Condiviso Con Me]</strong> </p> <p>Selezionare la cartella in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Unità condivisa]</strong> (disponibile solo per [!DNL Google Workspace] utenti)</p> <p>Selezionare se si desidera [!UICONTROL Utilizzare Domain Admin Access]. Se si seleziona [!UICONTROL Sì], la richiesta viene inviata come amministratore di dominio e vengono restituite tutte le unità condivise in cui il richiedente è un amministratore.</p> <p>Selezionare l'unità condivisa in cui si trova il documento in cui si desidera rendere cliccabili i collegamenti, quindi selezionare il documento.</p> <p>Nota: se hai selezionato l'opzione [!DNL Google Docs] in questo campo e non sei un utente [!DNL Google Workspace], viene restituito l'errore <code>[400] Invalid Value</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Unità condivisa]</td> 
   <td> <p>Selezionare l'unità contenente il documento in cui si desidera aggiornare i collegamenti, quindi selezionare un documento. Questa opzione è disponibile se è stato selezionato [!DNL My Drive] nel campo [!UICONTROL Scegli un'unità].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID documento]</td> 
   <td> <p> Selezionare o mappare il documento in cui si desidera aggiornare i collegamenti.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effettuare una chiamata API]

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

**Esempio:** La chiamata API seguente recupera i dettagli del documento specificato nel Google Docs:

**URL:**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**Metodo:**

[!UICONTROL GET]

![Esempio di chiamata API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

I dettagli del documento recuperato si trovano nell&#39;output del modulo in [!UICONTROL Bundle] > [!UICONTROL Corpo].

![Output chiamata API](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

>[!ENDSHADEBOX]
