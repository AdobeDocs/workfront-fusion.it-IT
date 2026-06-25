---
name: writing-quality
description: 'Rivedi e migliora la qualità della scrittura tecnica per gli articoli tutorial e la documentazione generale di Workfront. Applica la Guida di stile alla documentazione di Workfront e i principi relativi allo sviluppo di informazioni tecniche di qualità. Utilizza quando modifichi, rivedi o scrivi articoli dimostrativi, articoli di panoramica, articoli di riferimento o documentazione generale. Non utilizzare per le note sulla versione: utilizza piuttosto l’abilità di formattazione delle note sulla versione.'
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---


# Qualità scrittura

Rivede e migliora la documentazione di Workfront utilizzando la Guida di stile alla documentazione di Workfront e i principi DQTI.

## Flusso di lavoro

Durante la revisione o la modifica del contenuto:

1. Leggi il file di destinazione
2. Applica le regole seguenti — correggi i problemi direttamente o segnalali
3. Preservare l&#39;intento dell&#39;autore e l&#39;accuratezza tecnica
4. Per informazioni dettagliate su terminologia, punteggiatura e procedure, vedere .claude/commands/_writing-quality-reference.md

## Voce e punto di vista

- Usa **seconda persona** (&quot;Puoi...&quot;) quando si rivolge al lettore
- Usa le contrazioni per un tono di conversazione (non, non può, è, sono)
- Utilizza &quot;Consigliamo&quot; per le best practice, non &quot;È consigliato&quot; o &quot;Dovresti&quot;
- Quando scrivi per un gruppo di utenti, fai riferimento ad altri ruoli in terze persone (&quot;Puoi visualizzare... Tuttavia, l’amministratore di Workfront può limitare...&quot;)
- Non usare mai pronomi di genere — ristrutturate la frase o usate &quot;loro&quot;
- Nessuna barra per le scelte: usa &quot;o&quot; (&quot;lui o lei&quot; non &quot;lui/lei&quot;)

## Chiarezza (DQTI)

- Un&#39;idea per frase
- Mantieni le frasi sotto ~25 parole dove possibile
- Lead con l’azione o il risultato, non con il contesto di sfondo
- Utilizza la parola più semplice che trasmette il significato (&quot;utilizza&quot; non &quot;utilizza&quot;, &quot;avvia&quot; non &quot;avvia&quot;, &quot;su&quot; non &quot;riguardante&quot;)
- Evita le nominalizzazioni (&quot;crea&quot; non &quot;la creazione di&quot;, &quot;configura&quot; non &quot;la configurazione di&quot;)
- Utilizza un linguaggio specifico e concreto: evita termini vaghi (&quot;diversi&quot;, &quot;vari&quot;, &quot;alcuni&quot;)
- Evitare doppi negativi
- Utilizza pronomi facoltativi (&quot;che&quot;, &quot;chi&quot;) per aggiungere chiarezza alla struttura della frase

## Concretezza (DQTI)

- Utilizza esempi specifici invece di descrizioni astratte
- Includi valori realistici negli esempi
- Denomina esattamente gli elementi, i campi e le aree dell’interfaccia utente

## Orientamento attività (DQTI)

- Concentrati su ciò che l&#39;utente può *fare*, non su ciò che il sistema *è*
- Eseguire procedure con verbi imperativi (&quot;Creare un’attività&quot;, &quot;Configurare le notifiche&quot;)
- Fornire all&#39;utente un contesto sufficiente per agire, ma non più
- Includi un collegamento alla Guida dettagliata (&quot;Per ulteriori informazioni, vedi [articolo].&quot;)

## Uso delle maiuscole

- **Intestazioni**: frase sempre (&quot;Crea un&#39;attività&quot; non &quot;Crea un&#39;attività&quot;)
- **Termini di Workfront**: usare l&#39;iniziale maiuscola solo quando si fa riferimento direttamente a un elemento dell&#39;interfaccia utente
   - Riferimento diretto: &quot;Completare il campo Data di completamento pianificata&quot;.
   - Riferimento indiretto: &quot;Ogni attività deve avere una data di completamento pianificata.&quot;
   - Suggerimento: se è possibile inserire &quot;il&quot; o &quot;a&quot; davanti al termine, di solito dovrebbe essere in minuscolo
- **Pulsanti**: segui le maiuscole nell&#39;interfaccia utente, tranne i pulsanti maiuscoli → le lettere maiuscole
- **Ruoli**: &quot;Amministratore di sistema&quot; per il ruolo nell&#39;interfaccia utente; &quot;Amministratore di Workfront&quot; per la persona

## Intestazioni

- Usa il comando imperativo in caso di frase (&quot;Crea un&#39;attività&quot;, &quot;Configura i livelli di accesso&quot;)
- Le intestazioni devono essere basate sulle attività e descrivono le operazioni che verranno eseguite dall&#39;utente
- Gli articoli Panoramica terminano con &quot;Panoramica&quot; (&quot;Panoramica dei progetti&quot;)
- Suddividere sezioni lunghe in più intestazioni con obiettivi secondari chiari

## Riferimenti incrociati e collegamenti

Utilizza i seguenti pattern esatti:

| Situazione | Formato |
|-----------|--------|
| Collega dopo aver fornito le informazioni | &quot;Per ulteriori informazioni, vedere [Nome articolo].&quot; |
| Collegamento senza informazioni precedenti | &quot;Per informazioni, vedere [Nome articolo].&quot; |
| Collegamento a una sezione in un altro articolo | &quot;Per ulteriori informazioni, vedere [Nome sezione] in [Nome articolo].&quot; |
| Collegamento a una sezione nello stesso articolo | &quot;Per ulteriori informazioni, vedere [Nome sezione] in questo articolo.&quot; |

- In un paragrafo: in linea con il testo
- In un passaggio della procedura: su una nuova riga dopo il passaggio
- Più collegamenti: utilizzare un elenco puntato
- Utilizza &quot;angolo superiore destro&quot; / &quot;angolo superiore sinistro&quot; per le posizioni dello schermo

## Grassetto e corsivo

- **Grassetto** azioni selezionabili ed elementi dell&#39;interfaccia utente solo nei passaggi della procedura
- Non applicare il grassetto agli elementi dell’interfaccia utente al di fuori dei passaggi della procedura
- Non applicare il grassetto ai nomi delle finestre di dialogo, alle pagine, alle icone o ai menu all&#39;esterno dei passaggi
- Utilizza *corsivo* per il testo che l&#39;utente deve digitare (&quot;Digitare *my.workfront.com* nella casella URL&quot;)
- Non usate mai il corsivo per enfasi — ristrutturate la frase invece

## Appunti, suggerimenti e avvisi

Usare con moderazione: un uso eccessivo li rende invisibili ai lettori.

- Massimo una nota/suggerimento/avviso per sezione
- Non impilare mai più note
- Combinare le note correlate in una nota con un elenco puntato
- Non utilizzare le note per annunciare nuove funzionalità. Rielaborare il testo dell&#39;articolo

| Tipo | Scopo |
|------|---------|
| `>[!NOTE]` | Informazioni che non rientrano nel paragrafo; evitare frustrazioni; controllo delle versioni/compatibilità |
| `>[!TIP]` | Suggerimenti utili per semplificare la vita dell&#39;utente |
| `>[!IMPORTANT]` | Informazioni essenziali per la fase o la procedura |
| `>[!WARNING]` | Avvisa l&#39;utente in caso di potenziale perdita di dati |

## Procedure

- Utilizzare le intestazioni di comando imperative (&quot;Crea un&#39;attività&quot;)
- Introduzione solo se necessario — la rubrica dovrebbe essere sufficiente
- Formato introduzione preferito: frase infinita + due punti (&quot;Per creare una password temporanea:&quot;)
- Le procedure in un unico passaggio utilizzano ancora un elenco numerato
- Utilizza &quot;type&quot; o &quot;select&quot; — evita parole vaghe come &quot;set&quot; o &quot;specified&quot;
- Passaggi condizionali: &quot;(Condizionale) Se sei membro di più team, seleziona...&quot;
- Passaggi facoltativi: &quot;(Facoltativo) Per aggiungere un’emoji, fai clic su...&quot;
- Descrivere la risposta del sistema prima che si verifichi o immediatamente dopo
- Metodi multipli: documenta prima il modo più semplice, quindi utilizza &quot;Or&quot;

### Parentesi ad angolo retto nelle procedure

- Utilizza `>` per visualizzare la navigazione del menu/scheda: &quot;Fai clic su **E-mail** > **Notifiche**&quot;
- Grassetto dei nomi dei pulsanti, non delle parentesi
- Includi spazi intorno alle parentesi
- Non utilizzare le parentesi per la navigazione nel menu principale: utilizza lo snippet del menu principale

## Riferimento rapido per la punteggiatura

| Regola | Esempio |
|------|---------|
| Oxford virgola sempre | &quot;movente, mezzi e opportunità&quot; |
| Virgola prima di &quot;then&quot; nelle procedure | &quot;Fare clic su Configurazione, quindi su Interfaccia.&quot; |
| Virgola dopo anno in una data a metà frase | Il 2 gennaio 2016, numero di... |
| Nessuna virgola con solo mese-anno | &quot;Gennaio 2016&quot; |
| Due punti prima di un elenco, lettere minuscole dopo | &quot;Selezionare una delle opzioni seguenti: opzione A&quot; |
| Nessun due punti dopo i titoli della procedura | &quot;Crea un&#39;attività&quot; (non &quot;Crea un&#39;attività:&quot;) |
| Trattini lungo | Ristrutturare la pena se possibile |
| Periodi nelle estensioni file | &quot;Carica un file .pdf&quot; |

Per informazioni complete sulla punteggiatura e la terminologia, consultate .claude/commands/_writing-quality-reference.md.

## Completeness (DQTI) (Completezza)

- Includere tutte le informazioni che l’utente deve comprendere e agire
- Non includere informazioni di cui l&#39;utente non ha bisogno
- Fornisci sempre un collegamento alla documentazione dettagliata &quot;Per ulteriori informazioni&quot;
- Impostazioni predefinite del sistema di documenti: &quot;(Predefinito)&quot; negli elenchi o descrivi nella frase

## Organizzazione (DQTI)

- Struttura logica con divulgazione progressiva (panoramica → dettagli → riferimento)
- Contenuto più recente, prima per le pagine ordinate nel tempo (ad esempio, note sulla versione)
- Un argomento per sezione
- Usa elenchi per più di 3 elementi paralleli
- Utilizzare tabelle per confronti strutturati o descrizioni di campi
- Evitare i paragrafi da muro di testo — suddividerli in blocchi digeribili

## Tipi di articolo

| Tipo | Scopo | Titolo Convenzione |
|------|---------|-----------------|
| Panoramica | Contesto, diagrammi, come funzionano le cose — nessuna procedura | Termina con &quot;panoramica&quot; |
| Procedure | Attività specifica con passaggi chiari | Verbo imperativo |
| Introduzione | Informazioni di configurazione e collegamenti per nuovi utenti | &quot;Inizia a usare...&quot; |
| Riferimenti | Descrizioni dei campi nelle tabelle | Frase sostantivo descrittivo |

## Elenco di controllo convalida

Dopo la modifica, verifica:

- [ ] seconda persona in tutto (&quot;tu&quot;), contrazioni utilizzate
- [ ] tutte le intestazioni con lettere maiuscole/minuscole
- [ ] termini Workfront capitalizzati correttamente (riferimento diretto o indiretto)
- [ ] Grassetto solo per azioni selezionabili nei passaggi della procedura
- [ ] I riferimenti incrociati utilizzano il formato standard (&quot;Per ulteriori informazioni, vedere...&quot;)
- [ ] note/suggerimenti/avvisi non sovrapposti, massimo uno per sezione
- [ ] virgola Oxford utilizzata in modo coerente
- [ ] I passaggi della procedura utilizzano verbi specifici (tipo, selezione, clic — non &quot;set&quot; o &quot;specified&quot;)
- [ ] passaggi condizionali/facoltativi etichettati correttamente
- [ ] Nessun pronome con genere
- [ Le frasi di ] sono chiare, concrete e orientate alle attività
