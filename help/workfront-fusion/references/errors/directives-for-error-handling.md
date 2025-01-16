---
content-type: reference
title: Direttive per la gestione degli errori
description: Questo articolo descrive le direttive che puoi utilizzare per la gestione degli errori nei tuoi  [!DNL Adobe Workfront Fusion]  scenari.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 16%

---

# Direttive per la gestione degli errori

Le direttive di gestione degli errori consentono di scegliere cosa accade quando uno scenario rileva un errore.

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] pacchetto</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza</td> 
   <td> Nuovo: Standard<p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licenza</td> 
   <td>
   <p>Corrente: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Legacy: qualsiasi </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>[!UICONTROL Select] o [!UICONTROL Prime] [!DNL Workfront] piano: l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] piano: [!DNL Workfront Fusion] incluso.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>


Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni su [!DNL Adobe Workfront Fusion] per informazioni sulle licenze di Adobe Workfront Fusion, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Direttive per la gestione degli errori

In Workfront Fusion sono disponibili le seguenti direttive per la gestione degli errori.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Rollback</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>L’esecuzione dello scenario viene interrotta immediatamente.</li><li>Viene avviata una fase di rollback su tutti i moduli, nel tentativo di ripristinarne lo stato iniziale. </li><li>I moduli successivi non vengono elaborati.</p></li><li> <p>Nella maggior parte dei casi, lo scenario viene disattivato dopo il numero di errori consecutivi specificati in Impostazioni scenario. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">Numero di errori consecutivi</a>.</p> </li><li><p>Lo stato di esecuzione dello scenario è contrassegnato come "Errore".</p></li></ul> <p><b>Nota</b>: questo è il comportamento predefinito se al modulo non è allegata alcuna route del gestore degli errori e se non è selezionata l'impostazione <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">Consenti archiviazione esecuzioni incomplete</a>Consenti archiviazione esecuzioni incomplete in [!UICONTROL Scenario settings].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Conferma</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>L’esecuzione dello scenario viene interrotta immediatamente.</li><li>Viene avviata una fase Commit su tutti i moduli. </li><li>I moduli successivi non vengono elaborati.</p></li><li> <p>Tutti i bundle non elaborati vengono ignorati.</p> </li><li><p>Lo stato di esecuzione dello scenario viene contrassegnato come “Success” (Completato). </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Resume (Riprendi)</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>Un output sostitutivo viene specificato e fornito al modulo che rileva un errore.</p> </li><li><p>Vengono elaborati i moduli successivi.</p></li><li> <p>Lo stato di esecuzione dello scenario viene contrassegnato come “Success” (Completato).</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ignora</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>L’errore viene ignorato.</li><li> I moduli successivi non vengono elaborati.</p> </li><li><p>Se sono presenti bundle non elaborati, l’esecuzione dello scenario continua normalmente.</p> </li><li><p>Lo stato di esecuzione dello scenario viene contrassegnato come “Success” (Completato).</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Break (Interrompi)</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>Lo stato di esecuzione dello scenario viene memorizzato nella coda delle esecuzioni incomplete dove l’errore può essere risolto manualmente. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">Visualizzare e risolvere le esecuzioni incomplete</a>.</p> <p>Vi sono tuttavia alcune eccezioni. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">Consentire l'archiviazione di esecuzioni incomplete</a> nell'articolo Configurare le impostazioni dello scenario</a>.</p></li><li> <p>I moduli successivi non vengono elaborati.</p></li><li> <p>Se sono presenti bundle non elaborati, l’esecuzione dello scenario continua normalmente.</p> </li><li><p>Lo stato di esecuzione dello scenario è contrassegnato come "avvertenza" quando l'opzione [!UICONTROL Automatically complete execution] è disabilitata.</p></li></ul> <p>Per ulteriori informazioni, vedere la sezione <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> in questo articolo</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Riprova</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>In alcuni casi può essere utile rieseguire un modulo non riuscito quando è possibile che il motivo dell’errore passi nel tempo.</p> <p>Workfront Fusion attualmente non offre la direttiva sui nuovi tentativi, anche se è possibile utilizzare diverse soluzioni alternative per imitarne la funzionalità. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">Gestione degli errori dei tentativi</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Le direttive di gestione degli errori non possono essere utilizzate al di fuori di un percorso di gestione degli errori.
>* [!DNL Workfront Fusion] al momento non offre un modulo Throw che consentirebbe di generare errori in modo semplice e condizionale, anche se è possibile utilizzare una soluzione alternativa per imitare la funzionalità.
>
>  Per ulteriori informazioni, vedere [Configurazione della soluzione alternativa per l&#39;errore `throw`](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md).

## Risorse

* Per informazioni sul rollback e sulla fase di rollback, vedere [Rollback](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) nell&#39;articolo Esecuzione di uno scenario, cicli e fasi.
* Per informazioni sulla fase di esecuzione, vedere [Esecuzione](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) nell&#39;articolo Esecuzione scenario, cicli e fasi.
