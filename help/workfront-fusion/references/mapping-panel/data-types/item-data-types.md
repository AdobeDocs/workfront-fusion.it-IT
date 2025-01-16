---
title: Tipi di dati degli elementi
description: I tuoi  [!DNL Adobe Workfront Fusion]  scenari possono contenere i tipi di elementi elencati di seguito in un bundle.
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Tipi di dati degli elementi

Puoi contenere in un bundle i tipi di elementi elencati di seguito.

Per informazioni sui tipi di elementi [!DNL Workfront Fusion] che consentono la conversione tra di loro, vedere [Tipo di coercizione](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Testo</p> </td> 
   <td> <p>Il tipo di elemento più comune. Per alcuni elementi di testo, [!DNL Adobe Workfront Fusion] controlla se la lunghezza massima o minima consentita è soddisfatta o se l'elemento esegue la convalida del formato (e-mail, URL o nome file).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Numero</p> </td> 
   <td> <p>Per alcuni elementi numerici, [!DNL Workfront Fusion] può convalidare l'input per un intervallo specificato (il valore minimo o massimo consentito).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Booleano (sì/no)</p> </td> 
   <td> <p>Questo tipo viene utilizzato per gli elementi con solo due valori possibili: true o false. </p> <p>Quando si impostano i moduli, il tipo booleano può apparire in due forme diverse:</p> 
    <ul> 
     <li> <p>La casella di controllo obbligatoria viene visualizzata se il campo è obbligatorio e deve essere compilato.</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>I campi facoltativi che possono essere lasciati vuoti vengono visualizzati come una casella di selezione che consente la selezione tra tre valori: <code>Yes</code>, <code>No</code> e <code>Not defined</code> (impostazione predefinita).</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>Puoi fare clic su <strong>[!UICONTROL Map]</strong> se devi mappare il valore su un elemento da un altro modulo.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Data</p> </td> 
   <td> <p>Le date vengono immesse nel formato data ISO 8601, ad esempio <code>2015-09-18T11:58Z</code>. È possibile modificare il fuso orario nelle impostazioni del profilo. </p> <p>Se fai clic su un campo che richiede una data, nelle impostazioni del modulo viene visualizzato un calendario a comparsa. L'ora non è richiesta per alcuni elementi.</p> <p>I valori degli elementi Data vengono formattati utilizzando il fuso orario locale e Web selezionato nel profilo. Puoi visualizzare la versione ISO 8601 del valore di un elemento data passando il cursore sopra l’elemento.</p> <p>Nota: se il valore ISO non viene visualizzato, l’elemento è probabilmente un testo, non una data.</p> <p>L'ora viene immessa nel formato <code>hours:minutes:seconds</code>, ad esempio <code>14:03:52</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Buffer (dati binari)</p> </td> 
   <td> <p>Il contenuto del file viene in genere inviato come contenuto di tipo buffer (contenuto immagine, file video e altri). In alcuni casi, i dati di testo sono inclusi in questo tipo (ad esempio, un file di testo). [!DNL Workfront Fusion] è in grado di convertire automaticamente dati di testo nel codice binario in testo e testo in dati di testo nel codice binario. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref">File di mapping</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Raccolta</p> </td> 
   <td> <p>Una raccolta è un elemento costituito da più elementi secondari. L'elemento Sender in un messaggio e-mail è un esempio di raccolta: contiene il nome del mittente (tipo di testo) e l'indirizzo e-mail del mittente (tipo di testo).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Seleziona (menu)</p> </td> 
   <td> <p>Quando configuri le impostazioni del modulo, puoi selezionare tra più elementi dello stesso tipo. Un esempio è il menu di selezione delle cartelle nelle impostazioni per i moduli [!DNL Dropbox]. </p> <p>Quando si impostano i moduli, il menu di selezione può essere visualizzato in due forme:</p> <p> <p>Se è possibile selezionare più elementi, vengono visualizzati diversi elementi con caselle di controllo.</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>Se è disponibile una sola opzione, viene visualizzato un menu a discesa.</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>Se devi mappare un elemento da un altro modulo, usa il pulsante <strong>Mappa</strong>. Questo pulsante consente di aprire un campo di testo anziché il menu di selezione. Per ulteriori informazioni sulla mappatura, vedere <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref">Panoramica sulla mappatura</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Array</p> </td> 
   <td> <p>Puoi utilizzare il tipo di array per lavorare con diversi valori dello stesso tipo, incluse le raccolte. Un esempio sono i moduli [!UICONTROL Email]: restituiscono un array di allegati e ogni allegato contiene nome, contenuto, dimensione e così via. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref">Mappare un array o un elemento di array</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Convalida</p> </td> 
   <td> <p>[!DNL Workfront Fusion] potrebbe eseguire la convalida per ogni tipo di elemento. Se un elemento non supera la convalida, l’elaborazione del modulo verrà interrotta a causa di un errore di dati. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref">Tipi di errore </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
