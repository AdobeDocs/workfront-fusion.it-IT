---
title: Moduli di Adobe Substance
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL Adobe Substance], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 25%

---

# [!DNL Adobe Substance] moduli

In uno scenario Adobe Workfront Fusion, è possibile automatizzare i flussi di lavoro che utilizzano [!DNL Adobe Substance] e collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Per informazioni sui moduli, vedere gli articoli in [Moduli: indice articolo](/help/workfront-fusion/references/modules/modules-toc.md).

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità descritta in questo articolo.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi pacchetto Workflow di Adobe Workfront, e qualsiasi pacchetto Automation and Integration di Adobe Workfront</p><p>Workfront Ultimate</p><p>Pacchetti Workfront Prime e Select con un ulteriore acquisto di Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenze di Adobe Workfront</td> 
   <td> <p>Standard</p><p>Work o successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza di Adobe Workfront Fusion</td> 
   <td>
   <p>Basata sulle operazioni: nessun requisito di licenza di Workfront Fusion</p>
   <p>Basata sul connettore (precedente): Workfront Fusion for Work Automation and Integration </p>
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

Prima di poter utilizzare il connettore [!DNL Adobe Substance], è necessario verificare che siano soddisfatti i seguenti prerequisiti:

* Devi avere un account [!DNL Adobe Substance] attivo.



## Moduli [!DNL Adobe Substance] e relativi campi

Quando configuri i moduli [!DNL Adobe Substance], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL Adobe Substance], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un asterisco accanto al nome del campo in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione mappatura](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Compositi](#composites)
* [Scene](#scenes)
* [Spaces](#spaces)

### Compositi

#### Genera oggetto 3D composito

Questo modulo di azione genera contenuti per un composito 3D che include la risorsa principale selezionata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td>Configura altri campi come desiderato. Per informazioni dettagliate sui campi, consulta la <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">documentazione API Adobe Substance</a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Scene

* [Conversione di file 3D](#convert-3d-files)
* [Crea scena 3D](#create-3d-scene)
* [Descrivi scena 3D](#describe-3d-scene)
* [Rendering oggetto 3D](#render-3d-object)
* [Rendering oggetto 3D (versione di base)](#render-3d-object-basic-version)

#### Conversione di file 3D

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Formato</td> 
   <td>Selezionare il formato in cui si desidera convertire il file.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Punto di ingresso modello</td> 
   <td>In genere la conversione richiede il primo file considerato un modello 3D valido. Definisci questo punto di ingresso per evitare ambiguità in presenza di più opzioni.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Origini</td> 
   <td>Per ogni file che si desidera convertire, fare clic su <b> Aggiungi elemento</b> e immettere le informazioni sul file.</td> 
  </tr> 
 </tbody> 
</table>

#### Crea scena 3D

Questo modulo di azione crea una scena utilizzando le risorse specificate.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Codifica</td> 
   <td>Selezionate il tipo di file per la scena.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome base file</td> 
   <td>Immettere o mappare un nome per il file di output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Altri campi</td> 
   <td>Configura altri campi come desiderato. Per informazioni dettagliate sui campi, consulta la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">documentazione API Adobe Substance</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origini</td> 
   <td>Per ogni file che si desidera utilizzare, fare clic su <b> Aggiungi elemento</b> e immettere le informazioni sul file.</td> 
  </tr> 
 </tbody> 
</table>

#### Descrivi scena 3D

Questo modulo di azione recupera informazioni sul contenuto di scene 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">File di scena</td> 
   <td>Immettete o mappate il percorso del file di scena che desiderate descrivere.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origini</td> 
   <td>Per ogni file che si desidera descrivere, fare clic su <b> Aggiungi elemento</b> e immettere le informazioni sul file.</td> 
  </tr> 
 </tbody> 
</table>

#### Rendering oggetto 3D

Questo modulo di azione esegue il rendering di un&#39;immagine di una scena.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
   <td role="rowheader">Altri campi</td> 
   <td>Configura altri campi come desiderato. Per informazioni dettagliate sui campi, consulta la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">documentazione API Adobe Substance</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origini</td> 
   <td>Per ogni file che si desidera utilizzare, fare clic su <b> Aggiungi elemento</b> e immettere le informazioni sul file.</td> 
  </tr> 
 </tbody> 
</table>

#### Rendering oggetto 3D (versione di base)

Questo modulo di azione esegue il rendering di un&#39;immagine di una scena, ma dispone di un numero inferiore di opzioni rispetto al modulo Rendering oggetto 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
   <td role="rowheader">Altri campi</td> 
   <td>Configura altri campi come desiderato. Per informazioni dettagliate sui campi, consulta la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">documentazione API Adobe Substance</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Origini</td> 
   <td>Per ogni file che si desidera utilizzare, fare clic su <b> Aggiungi elemento</b> e immettere le informazioni sul file.</td> 
  </tr> 
 </tbody> 
</table>

### Spaces

#### Crea spazio

Questo modulo di azione ti consente di caricare e archiviare temporaneamente i file.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Substance] a Workfront Fusion, vedere <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Creare una connessione ad Adobe Workfront Fusion - Istruzioni di base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Nome file</td> 
   <td>Inserisci o mappa il nome del file che viene caricato.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Dati dei file</td> 
   <td>Immettere o mappare i dati binari del file.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome</td> 
   <td>Immettere o mappare un nome per il valore del modulo multipart.</td> 
  </tr> 
 </tbody> 
</table>
