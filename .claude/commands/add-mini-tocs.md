---
name: add-mini-tocs
description: ""
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Aggiungi mini sommari

Esegue la scansione di un file Markdown e inserisce un mini sommario sotto ogni titolo qualificato con sottotitoli diretti.

## Flusso di lavoro

1. Leggi il file di destinazione.
2. Identifica ogni intestazione al livello `##` o più profonda con almeno un&#39;intestazione figlio diretta (un livello `#` più profondo).
3. Per ogni intestazione padre di questo tipo, crea un elenco puntato di collegamenti solo ai relativi elementi figlio diretti.
4. Inserisci l’elenco immediatamente prima del primo titolo figlio, dopo qualsiasi testo introduttivo che segue il titolo padre.
5. Se in tale posizione esiste già un mini sommario, confrontalo con le intestazioni figlio correnti in tale sezione. Se l&#39;elenco non è aggiornato (voci mancanti, voci aggiuntive o collegamenti non corretti), sostituirlo con l&#39;elenco aggiornato. Se corrisponde già, salta.
6. Scrivi il file aggiornato.

## Ambito

- **Mai** creare un mini sommario con il titolo dell&#39;articolo `#`. I sommari mini vengono aggiunti solo sotto le intestazioni `##` e più dettagliatamente.
- Un&#39;intestazione `##` ottiene un elenco dei relativi `###` elementi figlio diretti.
- Un&#39;intestazione `###` ottiene un elenco dei relativi `####` elementi figlio diretti.
- E così via per livelli più profondi.

## Formato collegamento

Ogni voce dell&#39;elenco utilizza questo formato esatto:

```
* [Heading text](#anchor)
```

### Regole di generazione ancoraggio

Converte il testo dell’intestazione in un ancoraggio come segue:

1. Tutto il testo in minuscolo
2. Rimuovere i caratteri che non sono lettere, numeri, spazi o trattini.
3. Sostituire gli spazi con i trattini.
4. Rimuovi la formattazione del codice racchiuso tra apici inversi (mantieni il testo all’interno).

Esempio: `### Create or edit a function` → `#create-or-edit-a-function`

## Regole di nidificazione

- Collega solo **figli diretti** (un livello più profondo del padre) in ogni elenco.
- Non includere nipoti o intestazioni più profonde nello stesso elenco.
- Se le intestazioni figlio hanno figli, vengono inseriti sotto di essi i mini sommari separati.

**Struttura di esempio:**

```
## Manage a package          ← parent: gets a list of ### headings
### Functions                ← child of ##, parent of ####: gets a list of #### headings
#### Create a function       ← child of ###
#### Delete a function       ← child of ###
### Variables                ← child of ##
### History                  ← child of ##
```

Risultati in:

In `## Manage a package`:

```
* [Functions](#functions)
* [Variables](#variables)
* [History](#history)
```

In `### Functions`:

```
* [Create a function](#create-a-function)
* [Delete a function](#delete-a-function)
```

## Posizionamento

Inserisci il mini elenco sommario immediatamente prima del primo titolo figlio. Se tra l&#39;intestazione padre e la prima intestazione figlio è presente un testo introduttivo, l&#39;elenco viene posizionato dopo tale testo, direttamente sopra la prima intestazione figlio. Includi sempre una riga vuota prima e dopo l’elenco del sommario mini.

## Cosa saltare

- `#` intestazioni (titolo articolo): non aggiungere mai un mini sommario qui.
- Intestazioni padre con un solo figlio diretto: ignora — un elenco a voce singola non aggiunge alcun valore di navigazione.
- Sezioni senza intestazioni figlio: ignora.
