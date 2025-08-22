---
title: Generare un segmento di scenario utilizzando IA
description: Puoi utilizzare l’intelligenza artificiale per immettere un prompt di testo che descriva ciò che occorre fare per un segmento dello scenario. Fusion genera quindi uno o più moduli che eseguono tali azioni, che è possibile utilizzare nello scenario.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# Generare un segmento di scenario utilizzando IA

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

Puoi utilizzare l’intelligenza artificiale per immettere un prompt di testo che descriva ciò che occorre fare per un segmento dello scenario. Fusion genera quindi uno o più moduli che eseguono tali azioni, che è possibile utilizzare nello scenario.

I segmenti di scenario generati contengono moduli per un singolo connettore. Per generare moduli per un connettore diverso, crea un prompt separato, quindi unisci i segmenti dello scenario nello scenario.

Come per tutto ciò che viene generato dall’intelligenza artificiale, ti consigliamo di controllare e testare i moduli generati per verificare che funzionino come previsto.

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
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: [!UICONTROL Work] o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion.</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Piano Workfront di [!UICONTROL Select] o [!UICONTROL Prime]: l'organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Piano Workfront di [!UICONTROL Ultimate]: è incluso Workfront Fusion.</li></ul>
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

Per utilizzare questa funzionalità, la tua organizzazione deve soddisfare i seguenti prerequisiti:

* L&#39;organizzazione deve aver partecipato al programma Workfront AI Assistant Beta.
* Adobe deve disporre di un contratto Adobe Gen AI firmato per la tua organizzazione.

  Per ulteriori informazioni sulla firma del contratto, consulta [Firmare il contratto di Adobe Gen AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) nell&#39;articolo Panoramica dell&#39;Assistente IA nella documentazione di Workfront.

## Applicazioni del modulo di IA attualmente supportate

Fusion AI può attualmente generare moduli che si connettono alle seguenti applicazioni:

* Adobe Firefly
* Azure OpenAI
* Grafico Microsoft
* Adobe Workfront Planning
* Adobe Analytics
* Servizi Adobe PDF
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Calendario Google
* Jira Atlassian
* GitLab
* Spotify
* Bitbucket
* OpenAI
* Slack

## Genera moduli

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un modulo.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic sull&#39;icona **Assistente AI** ![Icona Assistente AI](assets/ai-assistant-icon.png) nell&#39;angolo superiore destro dello schermo.
1. Immettete un prompt di testo nel pannello Assistente AI.

   Per suggerimenti sui prompt, vedere [Suggerimenti per la creazione di prompt per i segmenti di scenario](#tips-for-creating-prompts-for-scenario-segments) in questo articolo.

   L’Assistente AI genera il modulo o il set di moduli.
1. (Condizionale) Se necessario, aggiungi il token API per l’applicazione ai moduli.
1. Controlla i moduli per assicurarti che siano configurati per l’applicazione e l’azione appropriate.
1. (Condizionale) Se la sezione dello scenario generato non è associata allo scenario, trascinala nella posizione desiderata.

È consigliabile testare i moduli per verificare che funzionino come previsto.

## Suggerimenti per la creazione di prompt per i segmenti di scenario

I prompt di testo devono includere almeno le seguenti informazioni:

* Applicazione a cui ci si connette
* Azione o azioni da eseguire

>[!IMPORTANT]
>
>È possibile generare più di un modulo alla volta, ma è possibile generare moduli solo per un&#39;applicazione alla volta.

>[!BEGINSHADEBOX]

**Esempi**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
Ciò include l&#39;applicazione `Workfront Planning` e l&#39;azione `delete records`. Questo prompt crea tre moduli, uno per ogni record che verrà eliminato.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
Ciò include l&#39;applicazione `Workfront Planning` e l&#39;azione `change campaign summary`.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
Ciò include l&#39;applicazione `Workfront Planning` e l&#39;azione `get field details`.

L’esempio seguente NON è corretto:

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Questo esempio non è corretto perché include più di un&#39;applicazione

>[!ENDSHADEBOX]

Durante la creazione di prompt di testo, tenete presente quanto segue:

* Utilizza un linguaggio semplice e diretto.
* Controlla e verifica il segmento dello scenario. Se non funziona come previsto, perfeziona la richiesta e riprova.
