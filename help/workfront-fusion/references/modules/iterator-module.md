---
title: Modulo iteratore
description: Un modulo Iterator è un tipo speciale di modulo che converte un array in una serie di bundle. Ogni elemento array viene prodotto come bundle separato.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Modulo [!UICONTROL Iterator]

Un [!UICONTROL Iterator] è un tipo di modulo che converte un array in una serie di bundle. Ogni elemento array viene prodotto come bundle separato.

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Se la tua organizzazione dispone di un pacchetto Select o Prime Workfront che non include l’automazione e l’integrazione di Workfront, deve acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## configurazione del modulo [!UICONTROL Iterator]

Il modulo Iterator generale ha un solo campo, il campo [!UICONTROL Array]. Questo campo contiene l’array da convertire o dividere in bundle separati.

![Configura iteratore](assets/set-up-iterator.jpg)

Altri connettori possono includere moduli iteratori specifici per tale iteratore. Questi contengono un campo modulo Source, che consente di selezionare il modulo che restituisce l’array da iterare.

![Iteratori specializzati](assets/specialized-iterators.jpg)

Per ulteriori informazioni, vedere [Configurare un modulo](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

>[!BEGINSHADEBOX]

**Esempi:**

* Lo scenario seguente mostra come recuperare le e-mail con allegati e salvare gli allegati come file singoli in una cartella [!DNL Dropbox] selezionata.

  Le e-mail possono contenere una matrice di allegati. Il modulo [!UICONTROL Iterator] dopo il primo modulo consente allo scenario di gestire ogni allegato separatamente. Il modulo [!UICONTROL Iterator] divide l&#39;array di allegati in singoli bundle. Ogni bundle, con un allegato, viene quindi salvato uno alla volta in una cartella [!DNL Dropbox] selezionata. Il campo [!UICONTROL Array] nel modulo Iterator deve contenere l&#39;array `Attachments`.

  ![Matrice allegati](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## Risoluzione dei problemi

### Problema: il pannello di mappatura non visualizza gli elementi mappabili nel modulo [!UICONTROL Iterator]

Quando un modulo [!UICONTROL Iterator] non dispone di informazioni sulla struttura degli elementi dell&#39;array, il pannello di mappatura nei moduli che seguono il modulo [!UICONTROL Iterator] visualizza solo due elementi nel modulo [!UICONTROL Iterator]: `Total number of bundles` e `Bundle order position`.

![Il pannello di mappatura non viene visualizzato](assets/mapping-panel-doesnt-display.png)

Questo perché ogni modulo è responsabile della fornitura di informazioni sugli elementi prodotti, in modo che possano essere visualizzati correttamente nel pannello di mappatura nei moduli successivi. In alcuni casi, tuttavia, diversi moduli potrebbero non essere in grado di fornire tali informazioni. Ad esempio, [!UICONTROL JSON] > [!UICONTROL Analizza JSON] o [!UICONTROL Webhook] > [!UICONTROL Moduli Webhook] personalizzati con struttura dati mancante non fornirebbero le informazioni.

#### Soluzione

La soluzione consiste nell’eseguire manualmente lo scenario. Questo costringe il modulo a creare output. Fusion può quindi applicare il formato di questo output ai moduli successivi nello scenario.

Ad esempio, uno scenario include un modulo [!UICONTROL JSON] > [!UICONTROL Analizza JSON] senza una struttura dati.

![Analizza JSON](assets/json-parse-json.png)

Un modulo [!UICONTROL Iterator] connesso a questo modulo JSON non può mappare l&#39;output del modulo al campo Array nel pannello di configurazione del modulo [!UICONTROL Iterator].

![Connetti modulo iteratore](assets/connect-iterator-module.png)

Per risolvere il problema:

Avvia manualmente lo scenario nell’editor dello scenario.

>[!NOTE]
>
>Per evitare che l’intero scenario venga eseguito, puoi:
>
>* Scollega i moduli dopo il modulo [!UICONTROL JSON] > [!UICONTROL Analizza JSON] per impedire che il flusso proceda ulteriormente.
>  &#x200B;>   Oppure
>* Fai clic con il pulsante destro del mouse sul modulo [!UICONTROL JSON] > [!UICONTROL Analizza JSON] e scegli **[!UICONTROL Esegui questo modulo solo]** dal menu di scelta rapida per eseguire solo il modulo [!UICONTROL JSON] > [!UICONTROL Analizza JSON].

Dopo l&#39;esecuzione di [!UICONTROL JSON] > [!UICONTROL Parse JSON], è possibile fornire informazioni sugli output a tutti i moduli successivi, incluso il modulo Iterator. Il pannello di mappatura nella configurazione dell’iteratore visualizza quindi gli elementi:

![Il pannello di mappatura visualizza gli elementi](assets/mapping-panel-displays-items.png)

inoltre, il pannello di mappatura nei moduli connessi dopo il modulo [!UICONTROL Iterator] visualizza gli elementi contenuti nell&#39;array:

![Elementi contenuti nella matrice](assets/items-contained-in-array.png)
