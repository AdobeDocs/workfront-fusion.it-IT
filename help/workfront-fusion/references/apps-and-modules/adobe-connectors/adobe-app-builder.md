---
title: Modulo Adobe App Builder
description: Il connettore App Builder di Adobe consente di utilizzare funzioni personalizzate negli scenari.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 02c396f33b6398635462bac8741f446eb82bf5a9
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 16%
---
# Modulo Adobe App Builder

È possibile creare funzioni personalizzate nell&#39;area Funzioni di Fusion. Puoi quindi aggiungere queste funzioni agli scenari sotto forma di un modulo App Builder di Adobe.

Poiché le funzioni personalizzate funzionano tramite Adobe App Builder, la tua organizzazione deve disporre di una licenza Adobe App Builder per utilizzarle.

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
   <td role="rowheader">Prodotto</td> 
   <td>
   <p><ul><li>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li><li>Per utilizzare le funzioni personalizzate è necessario disporre di una licenza Adobe App Builder.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Creare una connessione ad Adobe App Builder

La connessione utilizza le credenziali Adobe I/O Runtime di un’area di lavoro del progetto App Builder. Prima di creare la connessione, ottieni queste credenziali da Adobe Developer Console.

### Ottenere le credenziali runtime

1. Accedi a [Adobe Developer Console](https://developer.adobe.com/console) con l&#39;organizzazione che dispone della tua licenza App Builder.
1. Apri il progetto App Builder che contiene le tue funzioni, quindi seleziona l&#39;area di lavoro a cui vuoi connetterti (ad esempio, **Produzione**).
1. Fai clic su **Scarica tutto** nell&#39;angolo superiore destro per scaricare il file JSON di configurazione dell&#39;area di lavoro.
1. Aprire il file e individuare la sezione `runtime`. Contiene:

   * `namespace`: valore da immettere nel campo **Spazio dei nomi**
   * `auth`: un valore in formato `username:password`. La parte prima dei due punti è **Nome utente** e la parte dopo i due punti è **Password**.

   >[!NOTE]
   >
   >È inoltre possibile trovare i valori dello spazio dei nomi e dell&#39;autenticazione eseguendo `aio runtime namespace get` o `aio app use` nell&#39;interfaccia della riga di comando di Adobe I/O.

### Creare la connessione

1. Nel modulo, fai clic su **Aggiungi** accanto al campo **Connessione**.
1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td> 
      <td>Specifica un nome per questa connessione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Ambiente]</td> 
      <td>Seleziona se ti connetti a un ambiente di produzione o non di produzione.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Tipo]</td> 
      <td>Seleziona <b>Account di servizio</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Username]</td> 
      <td>Immettere il nome utente dal valore <code>auth</code> dell'area di lavoro (la parte prima dei due punti).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Immettere la password dal valore <code>auth</code> dell'area di lavoro (la parte dopo i due punti).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Spazio dei nomi </td> 
      <td>Immetti il valore <code>namespace</code> dalla sezione <code>runtime</code> del file di configurazione dell'area di lavoro.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **Continua** per salvare la connessione.

## Moduli di Adobe App Builder

### Eseguire un blocco di codice personalizzato

Questo modulo consente di eseguire un blocco di codice. Il blocco di codice viene configurato durante la configurazione del modulo e viene eseguito quando il modulo viene eseguito durante l’esecuzione di uno scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Immettere il blocco di codice che si desidera venga eseguito dal modulo.<p>Per formattare il codice per facilitarne la lettura, fare clic sull'icona <b>Formatta codice</b>.</td> 
  </tr> 
   </tbody> 
</table>

### Eseguire una funzione personalizzata dal pacchetto

Questo modulo esegue una funzione da un pacchetto.

Per informazioni sui pacchetti, vedere [Utilizzare pacchetti di funzioni personalizzati](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Selezionare il pacchetto che include la funzione da eseguire nello scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Selezionare la funzione da eseguire nello scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Usa variabile da pacchetto

Questo modulo porta nello scenario una variabile configurata in un pacchetto.

Per informazioni sui pacchetti, vedere [Utilizzare pacchetti di funzioni personalizzati](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Seleziona il pacchetto che include la variabile da inserire nello scenario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Seleziona la variabile da inserire nello scenario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Eseguire una funzione personalizzata o un blocco di codice

Questo modulo consente di utilizzare una funzione JavaScript personalizzata precedentemente configurata e memorizzata nell’area Funzioni.

Per istruzioni sulla configurazione di una funzione personalizzata, vedere [Mappare i dati utilizzando le funzioni personalizzate](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td>
   <td>Selezionare la connessione contenente la funzione personalizzata che si desidera eseguire. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Azione]</td> 
   <td>Selezionare la funzione personalizzata che si desidera eseguire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parameters] </td> 
   <td>Immettere i valori per i parametri della funzione. I parametri disponibili si basano sui parametri configurati al momento della creazione della funzione.<p>Se un parametro ha un valore predefinito, non lo visualizzerai nel campo, ma puoi sovrascriverlo immettendo o mappando un valore nel campo.</p></td> 
  </tr> 
   </tbody> 
</table>


