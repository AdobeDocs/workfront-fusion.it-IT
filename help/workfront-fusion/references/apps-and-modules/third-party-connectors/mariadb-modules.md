---
title: Moduli MariaDB
description: In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano  [!DNL MariaDB], nonché collegarli a più applicazioni e servizi di terze parti.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
TQID: https://experienceleague.adobe.com/Dq7tbOvvEndH-6k3yX8AvH29kZxp748JeT1HW-zcDDQ
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 657
ht-degree: 60%

---

# Moduli [!DNL MariaDB]

In uno scenario Adobe Workfront Fusion, puoi automatizzare i flussi di lavoro che utilizzano [!DNL MariaDB], nonché collegarli a più applicazioni e servizi di terze parti.

Per istruzioni sulla creazione di uno scenario, consulta gli articoli in [Creare scenari: indice degli articoli](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <p>Basata sulle operazioni: nessun requisito di licenza Workfront Fusion</p>
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

## Prerequisiti

Per utilizzare i moduli [!DNL MariaDB], è necessario disporre di un account [!DNL MariaDB].

## Connettere [!DNL MariaDB] a Workfront Fusion

Puoi creare una connessione al tuo account [!DNL MariaDB] direttamente da un modulo [!DNL MariaDB].

1. In qualsiasi modulo [!DNL MariaDB], fai clic su **[!UICONTROL Aggiungi]** accanto al campo [!UICONTROL Connessione].
1. Configura i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name] (Nome della connessione)</p> </td> 
      <td> <p>Inserisci un nome per la nuova connessione.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>Seleziona se la connessione è per un ambiente di produzione o non di produzione.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>Specifica se ti connetti a un account di servizio o a un account personale.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Immettere l'indirizzo IP o il nome host dell'istanza di database. L'host deve essere accessibile dall'esterno della rete.</p> <p>Esempio: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Porta [!UICONTROL]</td> 
      <td>La porta predefinita è 3306. Se si utilizza una porta non standard, impostare questo numero sulla porta. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database ]</td> 
      <td>Immettere il nome del database con cui si desidera interagire.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Utente]</td> 
      <td>Immetti il nome utente.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Immetti la password.</td> 
     </tr> 
    </tbody> 
   </table>

1. Fai clic su **[!UICONTROL Continua]** per creare la connessione e tornare al modulo.

## Moduli di [!DNL MariaDB] e relativi campi

Quando configuri i moduli [!DNL MariaDB], in Workfront Fusion vengono visualizzati i campi elencati di seguito. Insieme a questi, potrebbero essere visualizzati altri campi di [!DNL MariaDB], a seconda di fattori quali il tuo livello di accesso nell’app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se visualizzi il pulsante Map (Mappa) sopra un campo o una funzione, puoi utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, consulta [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Pulsante di attivazione/disattivazione Mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Eseguire una query (avanzata)

Questo modulo di azione recupera le informazioni dal database in base a una query fornita dall&#39;utente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla connessione dell’account [!DNL MariaDB] a Workfront Fusion, consulta <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connettere [!DNL MariaDB] a Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Immettere la query SQL che si desidera venga utilizzata dal modulo per recuperare i dati.</p> <p>Importante: le variabili utilizzate nella query non vengono bonificate. Assicurati di bonificare correttamente le variabili per evitare l’iniezione SQL.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Selezionare righe da una tabella (avanzate)]

Questo modulo legge i record dal database.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td>Per istruzioni sulla connessione dell’account [!DNL MariaDB] a Workfront Fusion, consulta <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connettere [!DNL MariaDB] a Workfront Fusion</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tabella [!UICONTROL]</td> 
   <td> <p>Selezionare la tabella contenente i record che si desidera leggere.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filtro]</td> 
   <td> <p>Imposta il filtro in base al quale desideri selezionare le righe</p> 
    <ul> 
     <li> <p>Selezionare il campo in base al quale si desidera eseguire la ricerca</p> </li> 
     <li> <p>Seleziona l’operatore da utilizzare per la ricerca</p> </li> 
     <li> <p>Immettere o mappare il valore che si desidera cercare.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort] </td> 
   <td> <p>Per ogni livello in base al quale si desidera ordinare i risultati, fare clic su <strong>[!UICONTROL Aggiungi elemento]</strong>, quindi selezionare il campo in base al quale si desidera ordinare i risultati e se si desidera ordinare in ordine crescente o decrescente</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limite]</td> 
   <td> <p>Inserisci oppure mappa il numero massimo di record che il modulo potrà restituire durante ciascun ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>
