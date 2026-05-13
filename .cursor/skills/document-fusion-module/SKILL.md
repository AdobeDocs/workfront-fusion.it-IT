---
name: document-fusion-module
description: Documenta un nuovo modulo del connettore Adobe Workfront Fusion aggiungendolo all’articolo del connettore appropriato in help/workfront-fusion/references/apps-and-module/. Da utilizzare quando l’utente chiede di aggiungere, documentare o descrivere un nuovo modulo Fusion oppure quando fornisce schermate del pannello di configurazione di un modulo Fusion e desidera aggiornare l’articolo corrispondente.
source-git-commit: 976db79104d226a16a35dc04e8c8cb111eb745db
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---


# Documentare un modulo connettore Fusion

Utilizzare questa abilità per aggiungere uno o più nuovi moduli a un articolo del connettore Workfront Fusion (ad esempio, `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Input richiesti (per modulo)

Prima di popolare i campi di qualsiasi modulo, l&#39;utente **deve** fornire tutti i seguenti elementi. Se manca qualcosa, fermati e chiedi prima di procedere.

1. **Nome del modulo**, esattamente come appare nell&#39;interfaccia utente di Fusion (ad esempio, `Generate adaptive composite`).
2. **Percorso dell&#39;articolo del connettore**. L&#39;agente individua l&#39;elemento e conferma l&#39;operazione con l&#39;utente (vedere Fase 1).
3. **URL API** per l&#39;operazione API sottostante. Questa opzione è necessaria in modo che lo scopo di ogni campo possa essere oggetto di riferimento incrociato rispetto alle specifiche API.
4. **Schermata del pannello di configurazione del modulo nella visualizzazione standard** (`Show advanced settings` **deselezionata**).
5. **Schermata del pannello di configurazione del modulo nella visualizzazione avanzata** (`Show advanced settings` **selezionata**) o dichiarazione esplicita che il modulo non contiene campi avanzati.

## Flusso di lavoro

Si tratta di un processo multifase. La velocità è importante. Lavora *con* l&#39;utente, non davanti a loro. Conferma l’avanzamento a ogni limite di fase e resta aperto alle correzioni in qualsiasi momento.

### Fase 1 — Portare avanti i lavori

1. **Chiedere se si tratta di uno o più moduli**: *&quot;Si sta aggiungendo uno o più moduli a un articolo del connettore?&quot;*

2. **Raccogli prima il nome di ogni modulo**, in base alla risposta:
   - **Modulo singolo**: richiederne il nome esatto così come viene visualizzato nell&#39;interfaccia utente di Fusion.
   - **Moduli multipli**: chiedere tutti i nomi contemporaneamente OPPURE chiedere una schermata del connettore che li elenca (ad esempio, la schermata di panoramica del connettore in Fusion che mostra le etichette delle sezioni per ciascun modulo). In entrambi i casi, termina questo passaggio con un elenco confermato di ogni nuovo modulo da aggiungere.

3. **Individua l&#39;articolo del connettore** ricercando `help/workfront-fusion/references/apps-and-modules/` in base al nome del connettore implicito nei moduli. Utilizzare gli strumenti `Glob` o `Grep`.

4. **Conferma il percorso dell&#39;articolo con l&#39;utente**: *&quot;In base ai nomi dei moduli, dovrebbe andare in `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`. È corretto?&quot;*

5. **Leggi l&#39;articolo sul connettore** per scoprire la struttura e le convenzioni esistenti. Presta attenzione a:
   - Stile titolo (in genere `### Module name` in lettere maiuscole/minuscole)
   - Ordinamento dei moduli esistenti (in genere alfabetico)
   - Come sono formulate `Connection` righe
   - Modalità di scrittura dei campi nidificati (ad esempio, `Image > Source`)
   - Eventuali convenzioni di annotazioni o note a piè di pagina esistenti

### Fase 2 - Posizionare i segnaposto per ogni modulo nella parte anteriore

Anche se esiste un solo nuovo modulo, questo offre all’utente una chiara roadmap visiva. Se sono presenti più moduli nuovi, inseriscili tutti ora.

Per ogni nuovo modulo, inserisci una sezione segnaposto in posizione alfabetica:

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

Mostra all’utente l’elenco dei segnaposto aggiunti (ad esempio, &quot;Segnaposto aggiunti per: Genera composito adattivo, Genera immagini con Immagine5, Genera composito preciso, Genera video&quot;). Chiedi quindi con quale iniziare: *&quot;Con quale iniziare?&quot;*

### Fase 3 — Ciclo di documentazione per modulo

Per ogni modulo, completare completamente questo ciclo prima di passare al successivo:

#### 3 bis. Ottieni l’URL API

Chiedere all&#39;utente l&#39;URL API: *&quot;Condividere l&#39;URL API per l&#39;operazione API sottostante di `<module name>`.&quot;*

Quando disponibile:
- Prova `WebFetch` sull&#39;URL.
- Se la pagina è vuota/con rendering JS (comune ai documenti di Adobe Developer), cerca una pagina della guida delle funzioni correlata, in genere l’URL `.../guides/how-tos/...`, e recuperala.
- In caso di esito negativo, tornare a `WebSearch` per il nome dell&#39;operazione.

In un secondo momento, utilizza tutto ciò che apprendi come contesto di sfondo per le descrizioni dei campi. Non scaricarlo sull&#39;utente. È sufficiente riconoscerlo brevemente: *&quot;Ottenuto il contesto API, pronto per lo screenshot della visualizzazione standard.&quot;*

#### 3 ter. Ottieni la schermata della visualizzazione standard

Chiedi: *&quot;Condividi uno screenshot del pannello di configurazione del modulo con `Show advanced settings`**deselezionato**. Dopo aver elaborato i campi standard, chiederò la visualizzazione avanzata, ma non inviarla ancora.&quot;*

#### 3 quater. Documenta i campi standard

Utilizzando la schermata con visualizzazione standard, è possibile acquisire ogni campo visibile dall&#39;alto verso il basso. Per ogni campo:

1. Utilizza l’etichetta dell’interfaccia utente esatta del campo come intestazione di riga. Per i campi raggruppati, unisciti con ` > `:

   ```
   [!UICONTROL Background > Image > Source]
   ```
2. Leggi il testo di supporto sotto il campo nella schermata (la didascalia grigia/gialla). Utilizzala come base per la descrizione.
3. Fare riferimento incrociato al contesto API dal passaggio 3a per identificare ciò che il campo rappresenta (ad esempio, `background.fillAreaMask` è &quot;l&#39;area dello sfondo in cui verrà inserito l&#39;oggetto&quot;).
4. Scrivere la descrizione combinando **il valore del campo** (dall&#39;API) con **come fornirlo** (dal testo helper dell&#39;interfaccia utente e dal tipo di campo).

Ignora qualsiasi campo non visibile nella schermata, anche se l’API lo supporta. Non inventare campi.

Dopo aver inserito i campi standard, riepilogarli brevemente per l&#39;utente (ad esempio, &quot;Campi standard aggiunti: Connessione, Prompt, Proporzioni, ...&quot;), quindi passare al passaggio 3d.

#### 3d Ottieni la schermata della vista avanzata

Chiedi: *&quot;Ora condividi uno screenshot del pannello di configurazione del modulo con `Show advanced settings`**selezionato**. Se il modulo non ha campi avanzati, comunicalo e salteremo l&#39;operazione.&quot;*

#### 3 sexies. Documenta i campi avanzati

Utilizzo della schermata di visualizzazione avanzata:

1. Identifica i campi che *non sono* già presenti nella visualizzazione standard. Si tratta dei campi avanzati.
2. Per ciascun campo avanzato, seguire la stessa procedura di descrizione del passaggio 3c.
3. Aggiungi `*` al nome del campo in `<td role="rowheader">`:

   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```
4. Dopo la chiusura di `</table>`, aggiungere questa nota a piè di pagina sulla propria riga:

   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

Se l’utente ha detto che il modulo non ha campi avanzati, salta completamente i passaggi 3d e 3e.

#### 3 septies. Creare una bozza della descrizione del modulo

Ora (non prima), sostituisci il segnaposto di descrizione nella parte superiore della sezione con una bozza di una frase basata sul contesto API e sulle implicazioni dei campi. Offrilo sempre come bozza per la revisione dell’utente:

> *&quot;Ho scritto questa descrizione: &#39;...&#39;. Vuoi usarlo, modificarlo o sostituirlo?&quot;*

#### 3g Riepilogo per modulo

Fornisci all’utente un riepilogo finale dei campi documentati del modulo (standard + avanzato) e lascia emergere eventuali domande aperte:

- Alcuni campi erano tagliati nelle schermate?
- La descrizione del modulo è accettabile?
- Indicare se qualcosa deve essere contrassegnato come obsoleto o da annotare.

Attendi la conferma prima di dire che il modulo è pronto. Chiedi quindi: *&quot;Passare al modulo successivo?&quot;* (o &quot;Questo articolo del connettore è stato completato.&quot;)

### Fase 4 — Verifica finale

Dopo aver documentato tutti i moduli, esegui questo elenco di controllo per ciascuno di essi:

- [ L&#39;intestazione del modulo ] è `### ` (H3) e utilizza la distinzione tra maiuscole e minuscole.
- [ Il modulo ] viene visualizzato in ordine alfabetico rispetto ai moduli di pari livello.
- [ ] La prima riga è `Connection` e utilizza il testo standard del collegamento di connessione.
- [ ] Ogni campo documentato è visibile nelle schermate dell&#39;utente.
- [ ] I campi avanzati sono contrassegnati con `*` ed esiste una singola nota a piè di pagina sotto la tabella.
- [ ] Nessun campo inventato dalla sola API.
- [ Le descrizioni a discesa di ] Source utilizzano esattamente le etichette delle opzioni dell&#39;interfaccia utente (vedi &quot;Convenzione dei campi di Source&quot; di seguito).
- [ La descrizione del modulo ] è un riepilogo di una frase che descrive le funzioni del modulo.

## Convenzione campo Source

I campi sorgente delle immagini nei connettori di Fusion presentano in genere un menu a discesa con due opzioni. **Usare le etichette esatte mostrate nella schermata dell&#39;utente**. Diverse generazioni di moduli usano termini diversi:

| Se il menu a discesa mostra... | Usa questo formato |
|---|---|
| **Carica immagine** e **URL immagine** (moduli più recenti) | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **File** e **URL preceduto** (moduli precedenti) | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

Se nella schermata non sono visualizzate le opzioni del menu a discesa aperte, chiedi all’utente di condividerle.

## Stile descrizione campo

- Abbina la voce e la struttura delle voci del modulo esistenti nello stesso articolo.
- Breve descrizione: in genere sono sufficienti una o due frasi per campo.
- Utilizza il markup `[!UICONTROL ...]` per qualsiasi nome di campo dell&#39;interfaccia utente a cui si fa riferimento da un altro campo.
- Utilizzare `<code>...</code>` per i valori letterali (`<code>en-US</code>`, `<code>0.0</code>`).
- Per i campi di intervallo numerico, indicare esplicitamente l&#39;intervallo consentito: *&quot;Immettere un numero compreso tra 0 e 1...&quot;*.
- Per gli elenchi a discesa con opzioni discrete, enumerali come `<ul>` con `<b>Option</b>` seguito da `<p>` descrizione.

## Campi comuni e descrizioni consigliate

Riutilizza questi per coerenza tra i moduli:

**Seeds** (quando il campo consente più valori di seeding tramite Aggiungi elemento):
> Fare clic su **Aggiungi elemento** per aggiungere un valore di inizializzazione, quindi immettere o mappare un numero intero. Utilizza un valore di inizializzazione per variante. Il conteggio dei valori iniziali deve corrispondere al valore **Number of Variations**, se vengono forniti entrambi.

**Numero di varianti** (sostituisci l&#39;intervallo con l&#39;intervallo effettivo della schermata):
> Immettere un numero compreso tra [min] e [max]. Il modulo genera questo numero di varianti di tipo [output].

**Limite** (il limite standard del ciclo di esecuzione di Fusion; includi solo se visibile nella schermata):
> Immettere o mappare il numero massimo di risultati che si desidera utilizzare per il modulo durante un ciclo di esecuzione.

**Impostazioni locali**:
> Immetti o mappa un codice di lingua e area geografica per adattare il contenuto generato a un paese e una lingua specifici. Le impostazioni internazionali devono essere specificate nel codice della lingua ISO 639-1 e nell&#39;area geografica ISO 3166-1. Esempio: `en-US`

## Essere aperti alle correzioni in qualsiasi momento

L’utente può correggere il flusso intermedio del lavoro precedente: testo dei seed, etichette a discesa, posizionamento del campo, suddivisione avanzata/standard, ecc. Considera qualsiasi correzione come autorevole e aggiorna senza push back. Dopo la correzione, riepiloga brevemente ciò che è stato modificato.

Se l&#39;utente introduce un nuovo mid-flow della convenzione (ad esempio, &quot;contrassegniamo i campi avanzati con `*` e aggiungiamo una nota a piè di pagina&quot;), adottarlo per il resto della sessione e applicarlo retroattivamente ai moduli già documentati.

## Cosa fare se le informazioni sono in conflitto

Quando le specifiche API e l’interfaccia utente non sono d’accordo (questo accade spesso):

1. **Considera attendibile l&#39;interfaccia utente**, in quanto è ciò che l&#39;utente vede effettivamente in Fusion.
2. **Nota la discrepanza** nella tua risposta all&#39;utente in modo che possa decidere se approfondire l&#39;analisi.
3. **Non inventare una spiegazione** nel corpo dell&#39;articolo, attenendola ai dati dell&#39;interfaccia utente.

Se due schermate dell&#39;utente si contraddicono (ad esempio, una mostra `Blend`, un&#39;altra mostra `Harmonization` per lo stesso modulo), arrestarsi e chiedere quale sia corretta prima di scrivere. Identifica lo screenshot che probabilmente appartiene a un modulo diverso facendo riferimento incrociato alle specifiche API.
