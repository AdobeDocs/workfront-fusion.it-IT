---
title: Moduli OpenAI (ChatGPT)
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano OpenAIT(ChatGPT), nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
TQID: https://experienceleague.adobe.com/1k6WyDRiula-WnmQkPxPSeASokz25JpE4dp1eeSo7K8
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1456
ht-degree: 28%

---

# Moduli [!DNL OpenAI (ChatGPT & DALL-E)]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL OpenAI (ChatGPT & DALL-E)], nonché collegarli a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, consulta gli articoli in [Moduli: indice degli articoli](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
   <p>Basata su connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Per informazioni sulle licenze di Adobe Workfront Fusion, consulta [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL OpenAI (ChatGPT & DALL-E)], è necessario disporre di un account [!DNL OpenAI], inclusi una chiave API e un ID organizzazione.

## Informazioni API OpenAI (ChatGPT &amp; DALL-E)

Il connettore OpenAI (ChatGPT &amp; DALL-E) utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion

Puoi creare una connessione al tuo account [!DNL OpenAI (ChatGPT & DALL-E)] direttamente dall&#39;interno di un modulo [!DNL OpenAI (ChatGPT & DALL-E)].

1. In qualsiasi modulo [!DNL OpenAI (ChatGPT & DALL-E)], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Immettere le seguenti informazioni:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name] (Nome della connessione)</p> </td> 
      <td> <p>Inserisci un nome per la nuova connessione.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>Puoi individuare la tua chiave API nelle impostazioni utente di OpenAI.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL ID organizzazione] </td> 
      <td>Puoi individuare il tuo ID organizzazione nella pagina Impostazioni organizzazione in OpenAI.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.


## Moduli [!DNL OpenAI (ChatGPT & DALL-E)] e relativi campi

Quando configuri i moduli [!DNL OpenAI (ChatGPT & DALL-E)], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL OpenAI (ChatGPT & DALL-E)], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Creare un completamento

>[!IMPORTANT]
>
>Questo modulo è stato dichiarato obsoleto.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Crea moderazione

Questo modulo di azione determina se il testo viola il criterio del contenuto di OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Per ogni esempio di testo da includere, fare clic su <b>Aggiungi elemento</b> e immettere o mappare il testo. Includere l'intero testo di esempio.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Inserisci o mappa l’ID del modello da utilizzare. Puoi utilizzare il modulo Ottieni modelli per visualizzare tutti i modelli disponibili. </td> 
  </tr> 
 </tbody> 
</table>

### Creare una modifica

Questo modulo di azione restituisce una versione modificata di un prompt fornito, seguendo le istruzioni.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Inserisci o mappa l’ID del modello da utilizzare. Puoi utilizzare il modulo Ottieni modelli per visualizzare tutti i modelli disponibili. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Immettere o mappare il testo da modificare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Istruzione </td> 
   <td> Immetti o mappa le istruzioni per la modifica. Esempio: "Correggi gli errori di ortografia". </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni avanzate]</td> 
   <td> <p>Per informazioni sulle impostazioni avanzate facoltative in questo modulo, vedi le informazioni sulla creazione di modifiche nella <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">documentazione API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Creare un’incorporazione

Questo modulo di azione crea un vettore di incorporamento che rappresenta il testo di input.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Inserisci o mappa l’ID del modello da utilizzare. Puoi utilizzare il modulo Ottieni modelli per visualizzare tutti i modelli disponibili. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Testo di input da incorporare]</td> 
   <td> Inserisci o mappa il testo da incorporare. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID utente]</td> 
   <td> Inserisci o mappa un identificatore univoco che rappresenta l’utente finale, per consentire a OpenAI di monitorare e rilevare eventuali abusi </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> Immettere o mappare il numero massimo di modifiche con cui si desidera lavorare il modulo durante ogni ciclo di esecuzione dello scenario.</td> 
  </tr> 
 </tbody> 
</table>

### Crea completamento chat

Dato un elenco di messaggi che descrivono una conversazione, questo modulo di azione restituisce una risposta.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Inserisci o mappa l’ID del modello da utilizzare. Puoi utilizzare il modulo Ottieni modelli per visualizzare tutti i modelli disponibili. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>I messaggi descrivono la conversazione fino ad ora. Per ogni messaggio che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e compilare quanto segue:
   <ul>
   <li> <b>Ruolo</b>: selezionare il ruolo dell'autore del messaggio.</li>
   <li> <b>Contenuto</b>: immettere o mappare il contenuto del messaggio.</li>
   <li> <b>Nome</b>: immettere o mappare il nome dell'autore del messaggio. Il nome può contenere lettere maiuscole e minuscole, numeri e trattini bassi. La lunghezza massima per il nome è di 64 caratteri.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni avanzate]</td> 
   <td> <p>Per informazioni sulle impostazioni avanzate facoltative in questo modulo, vedere le informazioni sulla creazione di completamenti chat nella <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">documentazione API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Generare immagini

Questo modulo di azione genera o modifica immagini con modelli Dall-E.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Descrizione testo dell'immagine desiderata]</td> 
   <td> Inserisci o mappa una descrizione dell’immagine desiderata. La lunghezza massima della descrizione è di 1000 caratteri. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Impostazioni avanzate]</td> 
   <td> <p>Per informazioni sulle impostazioni avanzate facoltative in questo modulo, vedere le informazioni sulla creazione di immagini nella <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">documentazione API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Ottieni modelli

Questo modulo elenca e descrive i vari modelli disponibili nell’API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azione]</td> 
   <td> Seleziona se desideri ottenere un elenco di tutti i modelli o recuperare un modello specifico.
    <ul>
    <li><p><b>Modelli di elenco </b></p><p>Questa azione elenca i modelli attualmente disponibili e fornisce informazioni di base su ciascuno di essi, ad esempio il proprietario e la disponibilità.</p></li>
    <li><p><b>Recupera modello </b></p><p>Inserisci o mappa l’ID del modello da recuperare. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### Effettuare una chiamata API personalizzata

Questa azione invia una richiesta HTTP personalizzata all’API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Immettere un percorso relativo a <code>https://api.openai.com/v1/</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metodo]</td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, consulta <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Metodi di richiesta HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni della richiesta sotto forma di oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query]</td> 
   <td> <p>Aggiungi la query per la chiamata API come oggetto JSON standard.</p> <p>Ad esempio: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il contenuto del corpo della chiamata API sotto forma di oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel codice JSON, racchiudi l’istruzione condizionale tra virgolette.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### Gestione file

Questo modulo di azione elenca, elimina o recupera file o contenuto di file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azione]</td> 
   <td> Seleziona l’azione da eseguire. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> Se si elimina un file o si recupera il relativo contenuto, immettere o mappare l'ID del file. 
  </tr> 
</tbody>
</table>

### Gestione ottimizzazioni

Gestisci i processi di ottimizzazione per adattare un modello ai tuoi dati di formazione specifici.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion, vedere <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connessione di [!DNL OpenAI (ChatGPT & DALL-E)] a Workfront Fusion</a> in questo articolo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seleziona l'operazione]</td> 
   <td> Seleziona l’azione da eseguire.
   <ul>
   <li><p>Ottimizzare un modello da un set di dati</p><p>Immettere o mappare una descrizione per l'immagine desiderata.</p>
     <li><p>Ottenere informazioni su un processo di ottimizzazione</p><p>Inserisci o mappa l’ID del processo.</p>
   <li><p>Annullare un processo di ottimizzazione</p><p>Inserisci o mappa l’ID del processo.</p>
   <li><p>Annullare un processo di ottimizzazione</p><p>Inserisci o mappa l’ID del processo.</p>
   <li><p>Ottenere aggiornamenti dello stato per un processo di ottimizzazione</p><p>Inserisci o mappa l’ID del processo e seleziona se desideri inviare questi aggiornamenti in streaming.</p>
   <li><p>Eliminare un modello ottimizzato</p><p>Inserisci o mappa l’ID del modello da eliminare.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID file]</td> 
   <td> Se si elimina un file o si recupera il relativo contenuto, immettere o mappare l'ID del file. 
  </tr> 
</tbody>
