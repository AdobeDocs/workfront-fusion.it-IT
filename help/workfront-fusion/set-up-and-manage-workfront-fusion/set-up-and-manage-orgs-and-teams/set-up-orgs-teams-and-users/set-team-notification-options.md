---
title: Imposta opzioni di notifica
description: Le opzioni di notifica e-mail sono impostate a livello di team.
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 13%

---

# Impostare le opzioni di notifica

Nell’organizzazione utilizza Adobe Unified Shell, ricevi notifiche tramite l’area Notifiche di Adobe.

Se nell’organizzazione non è stata effettuata la migrazione ad Adobe Unified Shell, puoi scegliere le notifiche che un team riceve. Le notifiche sono impostate a livello di team.

Puoi controllare le situazioni per le quali vengono inviate le notifiche:

* Notify on warning (Notifica in caso di avviso): Fusion invia una notifica quando l’esecuzione di uno scenario registra un avviso.
* Notifica in caso di errore: Fusion invia una notifica quando l’esecuzione di uno scenario non riesce.
* Notifica quando lo scenario è disattivato: Fusion invia una notifica quando uno scenario viene disattivato automaticamente, ad esempio dopo troppi errori consecutivi.

Puoi impostare le notifiche a livello di team o scenario. Le notifiche a livello di scenario sostituiscono le notifiche impostate a livello di team. In altre parole, se l&#39;impostazione di uno scenario contraddice direttamente l&#39;impostazione di un team, viene seguita l&#39;impostazione dello scenario. Le impostazioni di notifica del team mostrano se sono presenti sostituzioni per tale impostazione.

Per impostazione predefinita, in Workfront Fusion sono abilitati tutti i tipi di notifica.

>[!IMPORTANT]
>
>Per ricevere notifiche da Workfront Fusion, è necessario che le impostazioni di notifica di Adobe CX Enterprise siano abilitate. Per accedere a queste impostazioni, fai clic sul campanello di notifica nell’angolo superiore destro dello schermo e sull’icona delle impostazioni.

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
   <p>Se la tua organizzazione dispone di un pacchetto Workfront Select o Prime che non include Workfront Automation and Integration, dovrà acquistare Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Ruolo</td> 
   <td> 
     <p>È necessario essere membri dell'organizzazione e del team di Fusion per cui si stanno modificando le impostazioni di notifica.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Per ulteriori dettagli sulle informazioni contenute in questa tabella, consulta [Requisiti di accesso nella documentazione](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Visualizzare e gestire le impostazioni di notifica a livello di team

1. In Workfront Fusion, fai clic su **Panoramica team** nell&#39;area di navigazione a sinistra.
1. Fare clic sulla scheda **Opzioni di notifica**.

   Viene visualizzato l&#39;elenco delle opzioni di notifica. Se sono presenti sostituzioni, accanto a tale impostazione viene visualizzato il numero di sostituzioni.

1. (Condizionale) Se sono presenti sostituzioni, per visualizzare quali scenari hanno la precedenza sull’impostazione di notifica del team, fai clic sul menu a tre punti relativo a tale impostazione.

   Puoi fare clic su uno scenario in questo menu per passare direttamente a tale scenario.

   ![Ignora menu scenario](assets/view-notification-override.png)

1. Per ripristinare le impostazioni predefinite per un tipo di notifica, vedere [Ripristinare le impostazioni predefinite delle notifiche](#restore-notification-defaults) in questo articolo.

Le modifiche all’elenco delle opzioni delle notifiche vengono salvate automaticamente.

## Imposta le impostazioni di notifica a livello di scenario

Le impostazioni di notifica per i singoli scenari sono impostate nel pannello Impostazioni scenario dello scenario.

1. Fai clic sulla scheda **[!UICONTROL Scenari]** nel pannello a sinistra.
1. Seleziona lo scenario in cui desideri aggiungere un filtro.
1. Fai clic in un punto qualsiasi dello scenario per accedere all’editor scenario.
1. Fai clic sull&#39;icona [!UICONTROL Impostazioni scenario] ![Icona Impostazioni scenario](assets/scenario-settings-icon.png) nella parte inferiore dello scenario.
1. Nel pannello Impostazioni scenario, fai clic su **Mostra impostazioni avanzate** nella parte inferiore del pannello.
1. Regola le impostazioni **Notify on warning**, **Notify on error** e **Notify when scenario is disabled** come desiderato.
1. Fare clic su **OK** per salvare e uscire dalle impostazioni dello scenario.

## Ripristina i valori predefiniti per le notifiche

È possibile ripristinare l&#39;impostazione predefinita di una notifica del team dalla scheda Opzioni di notifica. In questo modo l’opzione di notifica viene impostata su abilitato e vengono rimosse tutte le sostituzioni di notifica degli scenari per quel tipo di notifica.

Se il tipo di notifica è attualmente impostato sul valore predefinito, l&#39;icona **Ripristina sul valore predefinito** non sarà visibile.

1. In Workfront Fusion, fai clic su **Panoramica team** nell&#39;area di navigazione a sinistra.
1. Fare clic sulla scheda **Opzioni di notifica**.

   Viene visualizzato l&#39;elenco delle opzioni di notifica. Se un tipo di notifica non è attualmente impostato sul valore predefinito, per tale tipo di notifica è visibile l’icona Ripristina sul valore predefinito.

   ![Ripristina visualizzazione predefinita](assets/restore-notification-defaults.png)

1. Per ripristinare le impostazioni predefinite per il tipo di notifica, incluse eventuali sostituzioni dello scenario, fare clic sull&#39;icona **Ripristina impostazioni predefinite** ![Ripristina impostazioni predefinite](assets/restore-default-icon.png) per il tipo di notifica.

Le modifiche all’elenco delle opzioni delle notifiche vengono salvate automaticamente.

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
