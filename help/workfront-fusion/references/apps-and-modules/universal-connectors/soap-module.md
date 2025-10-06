---
title: Modulo SOAP
description: Puoi utilizzare il modulo SOAP per connettersi alle API SOAP in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: 29f9595d063e89e9cd393fecba07194d2e9008aa
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%

---

# Modulo [!UICONTROL SOAP]

È possibile utilizzare il modulo [!UICONTROL SOAP] per connettersi alle [!UICONTROL API SOAP] in [!UICONTROL Adobe Workfront Fusion].

## Modulo SOAP e relativi campi

Il connettore SOAP include un solo modulo, azione Esegui SOAP

### Esegui azione SOAP

Questo modulo di azione esegue l’azione SOAP specificata.



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
   <td role="rowheader">Licenza Adobe Workfront</td> 
   <td> <p>Nuovo: Standard</p><p>Oppure</p><p>Corrente: Lavoro o versione successiva</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licenza Adobe Workfront Fusion**</td> 
   <td>
   <p>Corrente: nessun requisito di licenza Workfront Fusion</p>
   <p>Oppure</p>
   <p>Legacy: Workfront Fusion per l'automazione e l'integrazione del lavoro </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Novità:</p> <ul><li>Seleziona o crea un pacchetto Prime Workfront: la tua organizzazione deve acquistare Adobe Workfront Fusion.</li><li>Pacchetto Ultimate Workfront: è incluso Workfront Fusion.</li></ul>
   <p>Oppure</p>
   <p>Corrente: la tua organizzazione deve acquistare Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, vedere [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Per informazioni sulle licenze di Adobe Workfront Fusion, vedere [Licenze di Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Modulo SOAP e relativi campi

Quando configuri i moduli di SOAP, Workfront Fusion visualizza i campi elencati di seguito.  Un titolo in grassetto in un modulo indica un campo obbligatorio.

Se viene visualizzato il pulsante Mappa sopra un campo o una funzione, è possibile utilizzarlo per impostare variabili e funzioni per tale campo. Per ulteriori informazioni, vedere [Mappare le informazioni da un modulo a un altro](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Attiva/Disattiva mappa](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Esegui azione SOAP

Questo modulo di azione esegue un&#39;azione SOAP, in base al file WSDL specificato.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Selezionare il file WSDL che si desidera venga utilizzato dal modulo. Per creare un file WSDL, fare clic su <b>Aggiungi</b> accanto al campo e compilare i campi. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP headers]</td> 
   <td> Per ogni intestazione HTTP da aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere il nome e il valore dell'intestazione.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Intestazioni SOAP]</td> 
   <td> Per ogni intestazione SOAP che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere il nome, il valore, lo spazio dei nomi e l'XMLNS dell'intestazione.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Forza intestazioni SOAP]</td> 
   <td> Abilita questa opzione per configurare le intestazioni per SOAP 1.2. </td> 
  </tr> 
  </tbody> 
</table>

## Limitazioni del modulo [!UICONTROL SOAP]

>[!NOTE]
>
>I reindirizzamenti sono disattivati durante il caricamento WDSL. Si tratta di una funzione di sicurezza, ma potrebbe significare che i reindirizzamenti non verificati vengono bloccati durante l’esecuzione del modulo.

Il modulo [!UICONTROL SOAP] è attualmente in versione beta e non supporta:

* Ridefinire gli elementi
* Limitazioni per cifre frazionarie
* Limitazioni per le cifre totali
* Limitazioni dello spazio vuoto
* Più parti nei messaggi di input e di output. Sono supportati solo i messaggi in una sola parte
* Elementi schema XML personalizzati definiti con l&#39;aiuto di schemi ed elementi di codifica SOAP.

>[!BEGINSHADEBOX]

**Esempio:**

I seguenti elementi non verrebbero riconosciuti correttamente da [!UICONTROL Workfront Fusion]:

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

Questo esempio include i riferimenti `soapenc:Array`, `soapenc:arrayType` e `wsdl:arrayType`, non ancora supportati in [!UICONTROL Workfront Fusion].

>[!ENDSHADEBOX]

## Soluzione alternativa

Se il modulo [!UICONTROL SOAP] rifiuta di elaborare il file WSDL o genera vari errori nella configurazione del modulo, è possibile provare a utilizzare il modulo universale **[!UICONTROL HTTP] > [!UICONTROL Richiedi]**:

1. In Workfront Fusion, crea un nuovo scenario.
1. Inserisci il modulo **[!UICONTROL HTTP] > [!UICONTROL Invia una richiesta]** nello scenario.
1. Apri la configurazione del modulo e compila i campi seguenti:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Tipo di corpo]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Tipo di contenuto]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Analizza risposta]</td> 
      <td>[!UICONTROL abilitato]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Aprire una nuova finestra o scheda del browser Web.
1. Incollare l&#39;URL WSDL nella barra degli indirizzi del browser Web e recuperare il file XML.

   L&#39;URL WSDL termina in genere con `?wsdl`, ma non necessariamente, ad esempio `http://voip.ms/api/v1/server.wsdl`.

1. Se il file WSDL non viene visualizzato direttamente nel browser Web, aprire il file scaricato in un editor di testo.
1. Cerca il tag `<service>` o `<wsdl:service>`:

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Una volta individuato, copiare l&#39;URL dall&#39;attributo `location`.
1. In Workfront Fusion, incolla l&#39;URL nel campo **Request content** del modulo HTTP.
1. Fornire i valori per i parametri selezionati sostituendo i punti interrogativi con i valori effettivi.

   >[!NOTE]
   >
   > Per ottenere valori specifici dal file WSDL, utilizzare un visualizzatore WSDL online.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Chiudere la configurazione del modulo facendo clic su **[!UICONTROL OK]**.
1. Esegui lo scenario o il modulo.
