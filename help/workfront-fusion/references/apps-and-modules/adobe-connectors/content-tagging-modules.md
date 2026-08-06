---
title: Moduli di Adobe Content Tagger
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Content Tagger, nonché collegarlo a più applicazioni e servizi di terze parti.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 801e8cb1a4c807aaa4275382c2d6211cf3cd6d1f
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 20%

---

# Moduli di Adobe Content Tagger

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano Adobe Content Tagger, nonché collegarlo a più applicazioni e servizi di terze parti.

Se hai bisogno di istruzioni per la creazione di uno scenario, consulta gli articoli in [Creare uno scenario: indice articolo](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <p>Basato su operazioni: disponibile per le organizzazioni con licenze basate su operazioni</p>
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

## Creare una connessione ad Adobe Content Tagger

Per creare una connessione per i moduli Adobe Content Tagger:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nome connessione</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Ambiente</td>
        <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">Tipo</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
        <tr>
        <td role="rowheader">ID client</td>
        <td>Immetti l'ID client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Segreto client</td>
        <td>Immetti il segreto client di Adobe. È disponibile nella sezione Dettagli credenziali di Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.


## Moduli di Adobe Content Tagger e relativi campi

Quando configuri i moduli di Adobe Content Tagger, Workfront Fusion visualizza i campi elencati di seguito. Insieme a questi, possono essere visualizzati campi Adobe Content Tagger aggiuntivi, a seconda di fattori quali il livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Azioni

* [Colori tag](#tag-colors)
* [Parole chiave tag](#tag-keywords)
* [Assegnare tag al testo di un&#39;immagine](#tag-text-in-an-image)

#### Colori tag

Questo modulo restituisce la percentuale di un’immagine coperta da diversi colori di pixel, ordinata in 40 categorie di colori.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione a Adobe Content Tagger, vedere <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Creare una connessione a Adobe Content Tagger</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome file immagine</td> 
   <td>Immettete o mappate il nome file dell'immagine per la quale desiderate assegnare i colori.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dati immagine</td> 
   <td>Immettete o mappate i dati del file dell'immagine per la quale desiderate assegnare i tag ai colori.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato immagine</td> 
    <td>Selezionare il tipo di immagine per cui si desidera assegnare i tag ai colori.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero di colori</td> 
    <td>Immettere o mappare il numero di colori da restituire. Per restituire tutti i risultati, immettere 0.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">Copertura minima</td> 
   <td>Immetti o mappa la copertura minima per la quale desideri assegnare i tag ai colori. Verranno restituiti solo i colori che coprono almeno questa quantità di immagine. Il valore 1 corrisponde al 100% dell'immagine e il valore 0,5 rappresenta il 50% dell'immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ridimensiona l’immagine prima dell’estrazione.</td> 
   <td>Selezionate Sì (Yes) per ridimensionare l'immagine a 320x320 prima di estrarre i colori. Selezionate No per estrarre i colori dall'immagine a dimensione intera.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Abilita maschera di primo piano/sfondo</td> 
   <td>Selezionare Sì se si desidera visualizzare separatamente i colori per l'immagine complessiva, il primo piano e lo sfondo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recupera toni</td> 
   <td>Selezionare Sì se si desidera recuperare i dati sui toni caldi, neutri e freddi oltre ai colori.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di colori restituiti</td> 
   <td>Immettere o mappare il numero massimo di colori restituiti dal modulo per un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>



#### Parole chiave tag

Questo modulo estrae parole chiave o frasi chiave che descrivono meglio l’oggetto del documento.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione a Adobe Content Tagger, vedere <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Creare una connessione a Adobe Content Tagger</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome file documento</td> 
   <td>Immettere o mappare il nome file del documento da cui si desidera estrarre le parole chiave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dati immagine</td> 
   <td>Immettere o mappare i dati del file del documento da cui si desidera estrarre le parole chiave.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato immagine</td> 
    <td>Selezionare il formato del documento da cui estrarre le parole chiave.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID applicazione</td> 
   <td>Immettere o mappare l'ID applicazione per il documento.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero di frasi chiave</td> 
   <td>Immettere o mappare il numero di frasi chiave che si desidera vengano restituite dal modulo. Per restituire tutti i risultati, immettere 0.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rilevanza minima</td> 
   <td>Inserisci o mappa la soglia di punteggio al di sotto della quale i risultati non verranno restituiti.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lunghezza minima frase chiave (parole)</td> 
   <td>Immettere o mappare il numero minimo di parole richieste nelle frasi chiave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lunghezza massima frase chiave (parole)</td> 
   <td>Immettere o mappare il numero massimo di parole richieste nelle frasi chiave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profondità dell’unità semantica</td> 
   <td>Selezionare il livello di profondità desiderato per le risposte gerarchiche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tipi di entità</td> 
   <td>Per ogni tipo di entità a cui si desidera limitare le frasi chiave, fare clic su <b>Aggiungi elemento</b> e immettere le informazioni per il tipo di entità.</td> 
  </tr> 
 </tbody> 
</table>

#### Assegnare tag al testo di un&#39;immagine

Questo modulo indica se il testo è presente in un’immagine e restituisce il testo se presente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connessione</td> 
   <td>Per istruzioni sulla creazione di una connessione a Adobe Content Tagger, vedere <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Creare una connessione a Adobe Content Tagger</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nome file immagine</td> 
   <td>Immettere o mappare il nome file del documento da cui si desidera estrarre il testo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dati immagine</td> 
   <td>Immettere o mappare i dati del file del documento da cui si desidera estrarre il testo.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Formato immagine</td> 
    <td>Selezionare il formato del documento da cui si desidera estrarre il testo.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtra con dizionario</td> 
   <td>Seleziona se restituire solo le parole presenti nel dizionario inglese.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Probabilità minima</td> 
   <td>Immettere o mappare la probabilità minima, in cui il modulo restituirà solo le parole riconosciute con una probabilità almeno equivalente. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rilevanza minima</td> 
   <td>Immetti la percentuale minima dell'immagine che deve essere coperta dal testo restituito. La rilevanza viene calcolata come frazione dell'area del riquadro del testo estratto rispetto all'immagine completa. 0,01 si tradurrebbe in un testo che occupi almeno l’1% dell’immagine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Numero massimo di risultati restituiti</td> 
   <td>Immettere o mappare il numero massimo di risultati restituiti dal modulo per un ciclo di esecuzione.</td> 
  </tr> 
 </tbody> 
</table>
