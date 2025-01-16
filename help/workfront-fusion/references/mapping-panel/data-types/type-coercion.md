---
title: Tipo coercizione
description: In questo documento viene descritto il comportamento di  [!DNL Adobe Workfront Fusion]  nelle situazioni in cui riceve valori in formati di dati previsti e imprevisti.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 3%

---

# Tipo coercizione

## Requisiti di accesso

+++ Espandi per visualizzare i requisiti di accesso per la funzionalità in questo articolo.

Per utilizzare le funzionalità di questo articolo, è necessario disporre dei seguenti diritti di accesso:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] piano*</td> 
   <td> <p>[!DNL Pro] o superiore</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licenza*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licenza**</td> 
   <td>
   <p>Requisiti di licenza correnti: nessun requisito di licenza [!DNL Workfront Fusion].</p>
   <p>Oppure</p>
   <p>Requisiti di licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione del lavoro] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prodotto</td> 
   <td>
   <p>Fabbisogno prodotto corrente: se si dispone del piano [!UICONTROL Select] o [!UICONTROL Prime] [!DNL Adobe Workfront], l'organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo. [!DNL Workfront Fusion] è incluso nel piano [!UICONTROL Ultimate] [!DNL Workfront].</p>
   <p>Oppure</p>
   <p>Requisiti del prodotto legacy: la tua organizzazione deve acquistare [!DNL Adobe Workfront Fusion] e [!DNL Adobe Workfront] per utilizzare le funzionalità descritte in questo articolo.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per conoscere il piano, il tipo di licenza o l&#39;accesso disponibili, contattare l&#39;amministratore [!DNL Workfront].

Per informazioni sulle licenze di Adobe Workfront Fusion, vedi [[!DNL Adobe Workfront Fusion] licenze](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Tipo coercizione

Questo documento descrive il comportamento di [!DNL Adobe Workfront Fusion] nelle situazioni in cui riceve valori in formati di dati previsti e imprevisti.

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Previsto</th> 
   <th>Ricevuto</th> 
   <th> <p>Descrizione</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>array </td> 
   <td>array </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>array </td> 
   <td>altro </td> 
   <td> <p>Se il valore ricevuto non è di tipo array, [!DNL Workfront Fusion] creerà un array e il primo (e unico) elemento sarà il valore ricevuto.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>booleano </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>numero </td> 
   <td> <p>Il valore viene convertito in logico Sì, anche se il valore è 0.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>text </td> 
   <td> <p>Se il valore è uguale a false o è vuoto, viene convertito in No logico. In caso contrario, viene convertito in logico Sì.</p> </td> 
  </tr> 
  <tr> 
   <td>booleano </td> 
   <td>altro </td> 
   <td> <p>Il valore viene convertito in Sì logico ogni volta che esiste il valore ricevuto (non è nullo).</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>buffer </td> 
   <td> <p>Il valore viene trasmesso invariato solo se la tabella codici è come previsto. Se la tabella codici è diversa, [!DNL Workfront Fusion] tenterà di convertire il valore ricevuto nella tabella codici richiesta. Se questa conversione non è supportata, [!DNL Workfront Fusion] restituirà un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>booleano </td> 
   <td> <p>Il valore viene convertito in testo (vero/falso) e quindi in dati binari seguendo i passaggi indicati sopra per la conversione in testo.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>data </td> 
   <td> <p>Il valore viene convertito in testo ISO 8601 e quindi in dati binari seguendo i passaggi indicati per la conversione in testo.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>numero </td> 
   <td> <p>Il valore viene convertito in testo e quindi in dati binari seguendo i passaggi indicati sopra per la conversione in testo.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>text </td> 
   <td> <p>Il valore viene convertito in dati binari e codificato come previsto. Se non viene specificata la codifica prevista, verrà utilizzata la codifica utf8.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>raccolta </td> 
   <td>raccolta </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>raccolta </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>data </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] tenterà di convertire il testo in una data. Se la conversione non riesce, verrà restituito un errore di convalida. La data deve contenere giorno, mese e anno. La data può contenere fuso orario e orario. Il fuso orario predefinito è basato sulle impostazioni. Esempi:</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>data </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>numero </td> 
   <td>numero </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>numero </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] tenterà di convertire il testo in un numero. Se la conversione non riesce, verrà restituito un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>numero </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>text </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>array </td> 
   <td> <p>Se l’array specificato supporta la conversione in testo, il valore verrà convertito. In caso contrario, [!DNL Workfront Fusion] restituirà un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>booleano </td> 
   <td> <p>Il valore viene convertito in testo (true/false).</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>buffer </td> 
   <td> <p>Se per i dati binari è specificata la codifica del testo, il valore verrà convertito in testo. In caso contrario, [!DNL Workfront Fusion] restituirà un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>data </td> 
   <td> <p>Il valore viene convertito in testo ISO 8601.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>numero </td> 
   <td> <p>Il valore viene convertito in testo.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>tempo </td> 
   <td>tempo </td> 
   <td> <p>Il valore viene consegnato invariato.</p> </td> 
  </tr> 
  <tr> 
   <td>tempo </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] tenterà di convertire l'ora nel formato <code>hours:minutes:seconds</code>. Se la conversione non riesce, verrà restituito un errore di convalida.</p> </td> 
  </tr> 
  <tr> 
   <td>tempo </td> 
   <td>altro </td> 
   <td> <p>[!DNL Workfront Fusion] restituisce un errore di convalida.</p> </td> 
  </tr> 
 </tbody> 
</table>
