---
title: Modulo SOAP
description: Puoi utilizzare il modulo SOAP per connettersi alle API SOAP in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: bf9af473f08463c00578a1a8b07c800239225f09
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---

# Modulo [!UICONTROL SOAP]

È possibile utilizzare il modulo [!UICONTROL SOAP] per connettersi alle API [!UICONTROL SOAP] in [!UICONTROL Adobe Workfront Fusion].

## Requisiti di accesso

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] piano*</td>
  <td> <p>[!UICONTROL Pro] o superiore</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], è necessario acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle [!DNL Adobe Workfront Fusion] licenze, vedere [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
* Elementi schema XML personalizzati definiti con l&#39;aiuto di [[!UICONTROL SOAP] schemi ed elementi di codifica](https://schemas.xmlsoap.org).

>[!INFO]
>
>**Esempio:**
>  
>I seguenti elementi non verrebbero riconosciuti correttamente da [!UICONTROL Workfront Fusion]:
>
>```
><complexType name="ArrayOfFloat">
>     <complexContent>
>           <restriction base="soapenc:Array">
>                 <attribute ref="soapenc:arrayType"
>                       wsdl:arrayType="xsd:integer[]"/>
>           </restriction>
>     </complexContent>
></complexType>
>```
>
>Questo esempio include i riferimenti `soapenc:Array`, `soapenc:arrayType` e `wsdl:arrayType`, non ancora supportati in [!UICONTROL Workfront Fusion].

## Soluzione alternativa

Se il modulo [!UICONTROL SOAP] rifiuta di elaborare il file WSDL o genera vari errori nella configurazione del modulo, provare a utilizzare il modulo universale **[!UICONTROL HTTP]>[!UICONTROL Make a request]**:

1. In [!DNL Workfront Fusion] creare un nuovo scenario.
1. Inserire il modulo **[!UICONTROL HTTP]>[!UICONTROL Make a request]** nello scenario.
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
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL Enabled]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Aprire una nuova finestra o scheda del browser Web.
1. Incollare l&#39;URL WSDL nella barra degli indirizzi del browser Web e recuperare il file XML.

   L&#39;URL WSDL termina in genere con `?wsdl`, ma non necessariamente, ad esempio `http://voip.ms/api/v1/server.wsdl`.

1. Se il file WSDL non viene visualizzato direttamente nel browser Web, aprire il file scaricato in un editor di testo.
1. Cerca il tag `<service>` o `<wsdl:service>`:

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Una volta individuato, copiare l&#39;URL dall&#39;attributo `location`.
1. In [!DNL Workfront Fusion], incollare l&#39;URL nel campo URL del modulo HTTP.
1. Aprire il client [Online [!UICONTROL SOAP]](https://wsdlbrowser.com/) in una nuova finestra o scheda del browser Web.
1. Incollare l&#39;URL WSDL nel campo URL WSDL.
1. Fare clic su **[!UICONTROL Browse]**.
1. Selezionare dall&#39;elenco di funzioni a sinistra, ad esempio `getLanguages`.
1. Copia il contenuto dell&#39;area di testo [!UICONTROL Request XML].
1. In [!UICONTROL Workfront Fusion], incolla il contenuto copiato nel campo URL del modulo.
1. Fornire i valori per i parametri selezionati sostituendo i punti interrogativi con i valori effettivi:

   <!--![](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Chiudere la configurazione del modulo facendo clic su **[!UICONTROL OK]**.
1. Esegui lo scenario o il modulo.
