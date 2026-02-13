---
title: Mappare i dati utilizzando funzioni personalizzate
description: Durante la mappatura degli elementi, puoi utilizzare funzioni per la creazione di formule semplici o complesse.
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 20%

---

# Mappare i dati utilizzando funzioni personalizzate

È possibile creare funzioni personalizzate nell&#39;area Funzioni di Fusion. Puoi quindi aggiungere queste funzioni agli scenari sotto forma di un modulo App Builder di Adobe.

Poiché le funzioni personalizzate funzionano tramite Adobe App Builder, la tua organizzazione deve disporre di una licenza Adobe App Builder per utilizzarle.

Le funzioni personalizzate, come la maggior parte degli elementi dello scenario, sono di proprietà dei team.

Workfront Fusion include inoltre funzioni incorporate che consentono di creare formule semplici o complesse. Queste funzioni coprono un&#39;ampia varietà di casi d&#39;uso, tra cui funzioni per array, stringhe, numeri e dati dei moduli precedenti.

Per informazioni e istruzioni sulle funzioni incorporate, vedere [Mappare un elemento utilizzando le funzioni incorporate](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

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

## Configurare una funzione personalizzata

Le funzioni personalizzate sono configurate nell&#39;area Funzioni di Workfront Fusion. Dopo aver configurato una funzione, puoi aggiungerla a uno scenario utilizzando il connettore App Builder di Adobe.

### Inizializzare l’ambiente di runtime

Prima di poter creare funzioni personalizzate, è necessario inizializzare l&#39;ambiente di runtime. Questa operazione deve essere eseguita solo se il team non dispone di funzioni personalizzate.

>[!IMPORTANT]
>
>L’inizializzazione può essere eseguita solo da un utente con accesso ad Adobe App Builder, che sia uno sviluppatore o un amministratore di sistema all’interno dell’organizzazione IMS.
>
>Una volta completata l&#39;inizializzazione, tutti gli utenti del team in cui è stata eseguita l&#39;inizializzazione saranno in grado di creare e utilizzare le funzioni.

1. Fai clic sulla scheda **Funzioni** ![Icona Funzioni](assets/functions-icon.png) nel pannello a sinistra.

   Se non hai ancora configurato il runtime, viene visualizzato il messaggio &quot;Ambiente di runtime non configurato&quot;.
1. Fare clic su **Inizializza runtime**.

   Dopo un certo periodo di tempo, viene visualizzato un elenco Funzioni, con due funzioni di esempio.

### Creare una funzione personalizzata

Dopo aver configurato l’ambiente di runtime, puoi iniziare a creare funzioni personalizzate.

>[!IMPORTANT]
>
>* La funzione personalizzata **deve** essere una funzione di JavaScript.
>* La funzione personalizzata **must** restituisce un oggetto.
>* Dopo aver creato una funzione personalizzata, non è possibile:
>
>   * Cambia il nome
>   * Visualizza i valori dei parametri predefiniti

1. Fai clic sulla scheda **Funzioni** ![Icona Funzioni](assets/functions-icon.png) nel pannello a sinistra.
1. Fare clic su **Aggiungi funzione**.
1. Immettere un nome per la funzione personalizzata.

   Non sarà possibile modificare questo nome in un secondo momento.
1. Immettere il codice per la funzione.
1. Per ogni valore di parametro predefinito che si desidera aggiungere, fare clic su **Aggiungi parametro** e immettere il nome del parametro e il valore predefinito.

   È possibile ignorare i parametri predefiniti quando si aggiunge la funzione a uno scenario.
1. Fai clic su **Salva**

## Aggiungere una funzione personalizzata a uno scenario

Per aggiungere una funzione personalizzata a uno scenario, utilizza il connettore App Builder di Adobe.

Per istruzioni, vedere [Modulo Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

