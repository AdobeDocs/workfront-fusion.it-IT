---
title: Moduli Adobe Experience Manager Forms
description: Con il connettore  [!DNL Adobe Experience Manager Forms]  per Adobe Workfront Fusion, puoi avviare uno scenario basato sugli eventi nel tuo account  [!DNL Adobe Experience Manager Forms] , creare, caricare e aggiornare le risorse e copiare o spostare cartelle e risorse.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
TQID: https://experienceleague.adobe.com/LTNDa0pulA4RE5tG59Fui-5bPlKxqHoQHEsKOp485No
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 600
ht-degree: 50%

---

# Moduli [!DNL Adobe Experience Manager Forms]

Con il connettore [!DNL Adobe Experience Manager Forms] per Adobe Workfront Fusion, puoi avviare uno scenario basato sugli eventi nell&#39;account [!DNL Adobe Experience Manager Forms] creando un webhook.

È possibile configurare un modulo all&#39;interno di [!DNL Adobe Experience Manager Forms] per inviare invii di moduli a questo webhook.

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

* Per utilizzare questo modulo è necessario disporre di un account [!DNL Adobe Experience Manager Forms].

## Informazioni sulle API di Adobe Experience Manager Assets

Il connettore Adobe Experience Manager Assets utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Creare una connessione ad Adobe Experience Manager Forms

Per creare una connessione per i moduli [!DNL Adobe Experience Manager Forms]:

1. In qualsiasi modulo, fai clic su **[!UICONTROL Aggiungi]** accanto alla casella Connessione.

1. Compila i seguenti campi:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name] (Nome della connessione)</td>
        <td>
          <p>Specifica un nome per questa connessione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiente]</td>
        <td>
          <p>Seleziona se questa connessione si connette a un ambiente di produzione o non di produzione.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tipo]</td>
        <td>
          <p>Specificare se l'account è un account di servizio o un account personale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL URL istanza senza una barra finale]</td>
        <td>
          <p>Immetti l’URL da utilizzare per accedere all’account, senza la barra finale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS endpoint]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID client]</td>
        <td>Immetti l'ID client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret] (Segreto client)</td>
        <td>Immetti il segreto client [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID organizzazione]</td>
        <td>Immetti l'ID organizzazione [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL ID account tecnico]</td>
        <td>Immetti l'ID account tecnico [!DNL Adobe]. È disponibile nella sezione [!UICONTROL Credentials details] (Dettagli delle credenziali) di [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Ambiti Meta]</td>
        <td>Inserisci i meta-ambiti appropriati       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Chiave privata]</td>
        <td>
          <p>Immettere la chiave privata generata al momento della creazione delle credenziali in [!DNL Adobe Developer Console]. </p>
          <p>Per estrarre la chiave privata o il certificato:</p>
          <ol>
            <li value="1">
              <p>Fai clic su <b>[!UICONTROL Estrai]</b>.</p>
            </li>
            <li value="2">
              <p>Seleziona il tipo di file da estrarre.</p>
            </li>
            <li value="3">
              <p>Seleziona il file che contiene la chiave privata o il certificato.</p>
            </li>
            <li value="4">
              <p>Inserisci la password per il file.</p>
            </li>
            <li value="5">
              <p>Fai clic su <b>[!UICONTROL Salva]</b> per estrarre il file e tornare alla configurazione della connessione.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Fai clic su **[!UICONTROL Continue]** (Continua) per salvare la connessione e tornare al modulo.

## Modulo Adobe Experience Manager Forms e relativi campi

Attualmente, nel connettore Adobe Experience Manager Forms è presente un solo modulo.

### Osserva eventi modulo

Questo trigger immediato (webhook) consente di avviare uno scenario quando si verifica un&#39;azione Invia in un Adobe Experience Manager Form.

>[!IMPORTANT]
>
>Questo modulo richiede anche la configurazione in Adobe Experience Manager. Dopo aver configurato il webhook, è necessario aprire Adobe Experience Manager e configurare il modulo per inviare gli invii al webhook.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nome webhook]</td> 
   <td> <p>Specifica un nome per il webhook.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connessione]</td> 
   <td> <p>Per istruzioni sulla connessione dell'account [!DNL Adobe Experience Manager] a Workfront Fusion, vedere <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">Creare una connessione a [!DNL Adobe Experience Manager Forms]</a></p> </td> 
  </tr>

Il modulo crea un webhook e fornisce l&#39;indirizzo del webhook, che è possibile immettere nella finestra di dialogo di invio del modulo in [!DNL Adobe Experience Manager Forms].
