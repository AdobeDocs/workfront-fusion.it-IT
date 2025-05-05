---
title: Moduli Frame.io (Beta)
description: Account  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: d81785ec60dfd74583a54a75ab1bfc1a253d8faf
workflow-type: tm+mt
source-wordcount: '2168'
ht-degree: 1%

---

# [!DNL Frame.io] moduli Beta (V4)

>[!IMPORTANT]
>
>Questo articolo descrive la nuova versione (beta) del connettore Frame.io. Questo connettore viene utilizzato per connettersi alla versione 4 di Frame.io.
>
>Per istruzioni sulla versione legacy del connettore Frame.io, vedere [Frame.io connettore](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md) legacy.

I [!DNL Adobe Workfront Fusion] [!DNL Frame.io] moduli consentono di monitorare, creare, aggiornare, recuperare o eliminare risorse e commenti nel account [!DNL Frame.io] .

Workfront offre due connettori Frame.io, in base alla versione di Frame.io a cui ci si connette.

| Connettore | Versione Frame.io |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io (legacy) | V3 |

Per istruzioni sulla versione legacy del connettore Frame.io, vedere [Connettore legacy Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Per un video introduttivo sul connettore Frame.io, vedi:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Pacchetto Adobe Workfront</td> 
   <td> <p>Qualsiasi</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licenza Adobe Systems Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Current: Nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Nuovo:</p> <ul><li>Pacchetto Select o Prime Workfront: l'organizzazione deve acquistare Adobe Systems Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Current: L'organizzazione deve acquistare Adobe Systems Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori informazioni sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisiti

Per utilizzare i moduli [!DNL Frame.io], è necessario disporre di un account [!DNL Frame.io]

## Informazioni API Frame.io

Il connettore Frame.io utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL di base</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Versione API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Connetti [!DNL Frame.io] a [!UICONTROL Adobe Workfront Fusion]

Il processo di connessione varia a seconda che si utilizzi il connettore Frame.io legacy o il connettore Frame.io Beta.

1. In qualsiasi modulo di Beta Frame.io, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i campi seguenti:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Tipo di connessione]</td>
          <td>
            <p>Specificare se si desidera creare una connessione di autenticazione utente IMD o una connessione server-server IMS.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Nome connessione]</td>
          <td>
            <p>Immettere un nome per la connessione.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL ID client]</td>
          <td>Inserisci il tuo [!DNL Adobe] [!UICONTROL ID client]. Questo può essere trovato nel [!UICONTROL Dettagli credenziali] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Segreto client]</td>
          <td>Immetti [!DNL Adobe] [!UICONTROL Client Secret]. È disponibile nella sezione [!UICONTROL Credentials details] di [!DNL Adobe Developer Console].<p>Per istruzioni su come individuare le credenziali, consulta <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Credenziali</a> nella documentazione per gli sviluppatori di Adobe.</p>
        </tr>
       </tbody>
    </table>
1. Fai clic su **[!UICONTROL Continua]** per salvare la connessione e tornare al modulo.

## [!DNL Frame.io] Moduli e relativi campi

Quando si configurano [!DNL Frame.io] i moduli, [!DNL Workfront Fusion] visualizza i campi elencati di seguito. Oltre a questi, potrebbero essere visualizzati campi aggiuntivi [!DNL Frame.io] , a seconda di fattori quali il livello di accesso nell&#39;app o nel servizio. Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se vedi la mappa pulsante sopra un campo o una funzione, puoi usarla per impostare variabili e funzioni per quel campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Risorse](#assets)
* [Commenti](#comments)
* [Cartelle](#folders)
* [Progetti](#projects)
* [Condivisioni](#shares)
* [Aree di lavoro](#workspaces)
* [Altro](#other)

### Risorse

* [[!UICONTROL Crea una risorsa]](#create-an-asset)
* [[!UICONTROL Eliminare una risorsa]](#delete-an-asset)
* [[!UICONTROL Ottieni una risorsa]](#get-an-asset)
* [[!UICONTROL Elenco risorse]](#list-assets)
* [[!UICONTROL Aggiornare un risorsa]](#update-an-asset)

#### [!UICONTROL Crea una risorsa] <!--different for v4-->

Questo modulo crea una nuova risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Selezionare il account o mappare l'ID del account contenente il progetto per il quale si desidera creare un risorsa.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL ID Area di lavoro] </td> 
   <td> <p>Selezionare l'area di lavoro o mappare l'ID dell'area di lavoro contenente il progetto per il quale si desidera creare un risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Progetto] </td> 
   <td> <p>Seleziona il progetto o mappa l’ID del progetto per il quale desideri creare una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso in cui desideri creare un risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome File] </td> 
   <td> <p>Immettere il nome del file che si desidera utilizzare per il risorsa.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Dimensione file </td> 
    <td> <p>Immettere o mappare la dimensione del file in byte.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL URL Source] </td> 
   <td> <p>Durante la creazione di un file, immettete il URL del file da caricare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tipo di supporto] </td> 
   <td> <p>Seleziona il tipo di media per questo risorsa.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Eliminare una risorsa]

Questo modulo di azione elimina una risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account o esegui il mapping dell’ID dell’account che contiene la risorsa da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Seleziona o mappa la risorsa da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ottieni una risorsa]

Questo modulo di azione recupera i dettagli della risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona il account o mappa l'ID del account che contiene il risorsa che desideri recuperare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Seleziona o mappa la risorsa da recuperare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elencare risorse]

Questo modulo di ricerca recupera tutte le risorse nella cartella del progetto specificato.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account o esegui il mapping dell’ID dell’account che contiene le risorse da elencare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di risorse] restituiti </td> 
   <td> <p>Immettere o mappare il numero massimo di risorse che si desidera che il modulo restituisca durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Commenti

* [[!UICONTROL Crea un commento]](#create-a-comment)
* [[!UICONTROL Eliminare un commento]](#delete-a-comment)
* [[!UICONTROL Leggi un commento]](#get-a-comment)
* [[!UICONTROL Elenca commenti]](#list-comments)
* [[!UICONTROL Aggiorna un commento]](#update-a-comment)

#### [!UICONTROL Crea un commento]

Questo modulo di azione aggiunge un nuovo commento o una nuova risposta alla risorsa.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account o esegui il mapping dell’ID dell’account contenente la risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Seleziona l’account o mappa l’ID dell’area di lavoro che contiene la risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Progetto] </td> 
   <td> <p>Seleziona il progetto o mappa l'ID del progetto che contiene il risorsa a cui vuoi aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Seleziona il percorso della risorsa a cui desideri aggiungere un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Immettere il contenuto del testo del commento o della risposta.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Immetti il numero del fotogramma nel video a cui deve essere collegato il commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Se la risorsa è un PDF, immetti o mappa la pagina a cui deve essere allegato il commento.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elimina commento]

Questo modulo elimina un commento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account o esegui il mapping dell’ID dell’account che contiene il commento da eliminare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID commento] </td> 
   <td> <p>Inserisci o mappa l’ID del commento da eliminare.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Visualizza un commento]

Questo modulo di azione recupera i dettagli del commento specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connessione [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona l’account o esegui il mapping dell’ID dell’account che contiene il commento di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID commento] </td> 
   <td> <p>Seleziona il commento di cui desideri recuperare i dettagli.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenca commenti]

Questo modulo di ricerca recupera tutti i commenti della risorsa specificata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account contenente la risorsa da cui desideri recuperare i commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selezionare o mappare l'area di lavoro contenente il risorsa da cui si desidera recuperare commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Progetto] </td> 
   <td> <p>Seleziona il progetto contenente il risorsa da cui desideri recuperare commenti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Percorso] </td> 
   <td> <p>Seleziona il percorso da cui si trova la risorsa da cui desideri elencare i commenti.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di commenti restituiti] </td> 
   <td> <p>Immettere o mappare il numero massimo di commenti che il modulo deve restituire durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Aggiorna un commento]

Questo modulo modifica un commento esistente.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o associa il account contenente il progetto contenente il risorsa su cui desideri aggiornare un commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID Commento] </td> 
   <td> <p>Selezionate il commento da aggiornare.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Immetti il contenuto del testo del commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Immetti il numero del fotogramma nel video a cui è collegato il commento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Se la risorsa è un PDF, immetti o mappa la pagina a cui è associato il commento.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Cartelle

#### Creare una cartella

Questo modulo di azione crea una nuova cartella in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account in cui desideri creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Seleziona o mappa l’area di lavoro in cui desideri creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona la posizione in cui desideri creare una cartella.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Seleziona il percorso in cui desideri creare una cartella.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Immettere o mappare un nome per la nuova cartella.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Progetti

* [Crea un Progetto](#create-a-project)
* [Elencare progetti](#list-projects)

#### Crea un Progetto

Questo modulo crea un nuovo progetto in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o esegui il mapping dell’account nel punto in cui desideri creare un progetto.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Seleziona o mappa l’area di lavoro in cui desideri creare un progetto.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Immetti o mappa un nome per il nuovo progetto.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Elenco progetti]

Questo modulo di ricerca recupera tutti i progetti per il team specificato.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account contenente la risorsa da cui desideri recuperare i progetti.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Seleziona o mappa l’area di lavoro contenente la risorsa da cui desideri recuperare i progetti.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di progetti restituiti] </td> 
   <td> <p>Inserisci o mappa il numero massimo di progetti
   desideri che il modulo venga restituito durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Condivisioni

* [Aggiungere una risorsa a un collegamento di condivisione](#add-an-asset-to-a-share-link)
* [Crea un collegare azionario](#create-a-share-link)

#### Aggiungere un risorsa a un collegare di condivisione

Questo modulo di azione aggiunge un risorsa a un collegare di condivisione in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account contenente il collegamento di condivisione a cui desideri aggiungere una risorsa.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID collegamento condivisione] </td> 
   <td> <p>Seleziona o mappa il collegamento di condivisione a cui desideri aggiungere una risorsa.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL ID risorsa] </td> 
   <td> <p>Inserisci o mappa l’ID della risorsa da aggiungere al collegamento di condivisione.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Crea un collegare azionario

Questo modulo di azione crea un nuovo collegare di condivisione in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Selezionare o mappare l'account in cui si desidera creare un collegamento di condivisione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Seleziona o mappa l’area di lavoro in cui desideri creare un collegamento di condivisione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID progetto] </td> 
   <td> <p>Seleziona o mappa il progetto in cui desideri creare un collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Accesso </td> 
   <td> <p>Seleziona se il collegamento ha accesso pubblico o limitato.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Risorse </td> 
   <td> <p>Per ogni risorsa che desideri aggiungere al collegamento di condivisione, fai clic su <b>Aggiungi elemento</b> e immetti l'ID della risorsa.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Descrizione </td> 
   <td> <p>Immettere o mappare una descrizione per il collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Immettere o mappare la data di scadenza del collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Immettere o mappare un nome per il nuovo collegamento di condivisione.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nome </td> 
   <td> <p>Immettere o mappare una passphrase per il collegamento di condivisione.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aree di lavoro

#### Crea un’area di lavoro

Questo modulo di azione crea un nuovo workspace in Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account in cui desideri creare un’area di lavoro.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Immettere o mappare un nuovo nome per l'area di lavoro.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Elencare aree di lavoro

Questo modulo elenca tutte le aree di lavoro di un account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID account] </td> 
   <td> <p>Seleziona o mappa l’account contenente la risorsa da cui desideri recuperare le aree di lavoro.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Numero massimo di aree di lavoro restituite] </td> 
   <td> <p>Inserisci o mappa il numero massimo di aree di lavoro
   desideri che il modulo venga restituito durante ogni ciclo di esecuzione dello scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Altro

#### [!UICONTROL Effettuare una chiamata API personalizzata]

Questo modulo ti consente di eseguire una chiamata API personalizzata.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Per istruzioni sulla creazione di una connessione a [!DNL Frame.io], vedere <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connettere [!DNL Frame.io] a [!DNL Adobe Workfront Fusion]</a> in questo articolo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Immettere un percorso relativo a <code>https://api.frame.io</code>. Esempio: <code> /v4/me</code></p> <p>Nota: per l'elenco degli endpoint disponibili, fare riferimento al riferimento API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Seleziona il metodo di richiesta HTTP necessario per configurare la chiamata API. Per ulteriori informazioni, vedere <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">richiesta HTTP metodi</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Intestazioni]</td> 
   <td> <p>Aggiungi le intestazioni del richiesta sotto forma di un oggetto JSON standard.</p> <p>Ad esempio: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Aggiunge automaticamente le intestazioni di autorizzazione.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringa di query] </td> 
   <td> <p>Immettere la richiesta stringa di query. Per ogni parametro che si desidera includere nella stringa di query, fare clic su <b>[!UICONTROL Aggiungi elemento]</b> e immettere il nome del campo e il valore desiderato.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Corpo]</td> 
   <td> <p>Aggiungi il corpo contenuto per la chiamata API sotto forma di un oggetto JSON standard.</p> <p>Nota:  <p>Quando utilizzi istruzioni condizionali come <code>if</code> nel tuo JSON, inserisci le virgolette al di fuori dell'istruzione condizionale.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
