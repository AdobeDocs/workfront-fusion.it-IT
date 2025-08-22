---
title: Crittografia
description: I moduli di Adobe Workfront Fusion Encryptor consentono di crittografare qualsiasi dato di testo. Attualmente supportano la crittografia dei messaggi tramite AES256 e PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 1%

---

# Crittografia

I moduli [!UICONTROL Encryptor] di Adobe Workfront Fusion ti consentono di crittografare qualsiasi dato di testo. Attualmente supportano la crittografia dei messaggi tramite AES256 e PGP ([!UICONTROL OpenPGP]).

Questi moduli richiedono una certa familiarità con i processi di crittografia.

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
   <p>Nessun requisito di licenza per Workfront Fusion</p>
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

## Crittografia e decrittografia dei messaggi tramite PGP

Durante la crittografia e la decrittografia tramite PGP, è necessario utilizzare un portachiavi e creare una chiave privata o pubblica (o entrambe).

Per ulteriori informazioni sulle chiavi pubbliche e private, vedere [Glossario di Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

Per ulteriori informazioni sulle chiavi, vedere [Chiavi](/help/workfront-fusion/references/modules/keys.md).

## [!UICONTROL Moduli Encryptor] e relativi campi

Durante la configurazione di [!UICONTROL moduli Encryptor] vengono visualizzati i campi seguenti. Un titolo in grassetto in un modulo indica un campo obbligatorio.

### Decrittografia AES (avanzata)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Seleziona la chiave da utilizzare per il modulo. Per creare una chiave, fare clic su <b>Aggiungi</b> e immettere il nome, la chiave e il tipo di codifica della chiave.</td>
    </tr>
    <tr>
        <td>Bit</td>
        <td>Specificare se si desidera che il modulo utilizzi la crittografia a 128 bit o a 256 bit.</td>
    </tr>
    <tr>
        <td>Codifica di input</td>
        <td>Selezionare il tipo di codifica di input che si desidera utilizzare:
        <ul>
        <li>Binario</li>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dati</td>
        <td>Immettere o mappare i dati da decrittografare.</td>
    </tr>
    <tr>
        <td>Codifica di output</td>
        <td>Seleziona il tipo di codifica di output da utilizzare:
        <ul>
        <li>ASCII</li>
        <li>Binario</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algoritmo di crittografia</td>
        <td>Selezionare l'algoritmo di crittografia da utilizzare:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codifica vettoriale di inizializzazione</td>
        <td>Selezionare la codifica del vettore di inizializzazione da utilizzare:
        <ul>
        <li>UTF-8</li>
        <li>Binario</li>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codifica tag di autenticazione</td>
        <td>Seleziona la codifica del tag di autenticazione da utilizzare:
        <ul>
        <li>UTF-8</li>
        <li>Binario</li>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
</table>

### Decrittografia AES (semplice)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Seleziona la chiave da utilizzare per il modulo. Per creare una chiave, fare clic su <b>Aggiungi</b> e immettere il nome, la chiave e il tipo di codifica della chiave.</td>
    </tr>
   <tr>
        <td>Codifica di input</td>
        <td>Selezionare il tipo di codifica di input che si desidera utilizzare:
        <ul>
        <li>Binario</li>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dati</td>
        <td>Immettere o mappare i dati da decrittografare.</td>
    </tr>
    <tr>
        <td>Codifica di output</td>
        <td>Seleziona il tipo di codifica di output da utilizzare:
        <ul>
        <li>ASCII</li>
        <li>Binario</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>Chiave segreta</td>
        <td>Immetti o mappa la chiave segreta che desideri utilizzare.</td>
    </tr>
</table>

### Crittografia AES (avanzata)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Seleziona la chiave da utilizzare per il modulo. Per creare una chiave, fare clic su <b>Aggiungi</b> e immettere il nome, la chiave e il tipo di codifica della chiave.</td>
    </tr>
    <tr>
        <td>Bit</td>
        <td>Specificare se si desidera che il modulo utilizzi la crittografia a 128 bit o a 256 bit.</td>
    </tr>
    <tr>
        <td>Codifica di input</td>
        <td>Selezionare il tipo di codifica di input che si desidera utilizzare:
        <ul>
        <li>Binario</li>
        <li>ASCII</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dati</td>
        <td>Immettere o mappare i dati da crittografare.</td>
    </tr>
    <tr>
        <td>Codifica di output</td>
        <td>Seleziona il tipo di codifica di output da utilizzare:
        <ul>
        <li>ASCII</li>
        <li>Binario</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algoritmo di crittografia</td>
        <td>Selezionare l'algoritmo di crittografia da utilizzare:
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codifica vettoriale di inizializzazione</td>
        <td>Seleziona la codifica del tag di autenticazione da utilizzare:
        <ul>
        <li>UTF-8</li>
        <li>Binario</li>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
</table>

### Crittografia AES (semplice)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Seleziona la chiave da utilizzare per il modulo. Per creare una chiave, fare clic su <b>Aggiungi</b> e immettere il nome, la chiave e il tipo di codifica della chiave.</td>
    </tr>
   <tr>
        <td>Codifica di input</td>
        <td>Selezionare il tipo di codifica di input che si desidera utilizzare:
        <ul>
        <li>Binario</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dati</td>
        <td>Immettere o mappare i dati da crittografare.</td>
    </tr>
    <tr>
        <td>Codifica di output</td>
        <td>Seleziona il tipo di codifica di output da utilizzare:
        <ul>
        <li>Base 64</li>
        <li>Binario</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Chiave segreta</td>
        <td>Immetti o mappa la chiave segreta che desideri utilizzare.</td>
    </tr>
</table>


### Crea firma digitale

Questo modulo consente di decrittografare un messaggio utilizzando chiavi pubbliche e private.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chiave privata]</td>
        <td>Selezionare la chiave privata da utilizzare per la firma. Per aggiungere una chiave privata, fare clic su <b>Aggiungi</b> e immettere il nome, il testo e la passphrase della chiave.</td>
    </tr>
    <tr>
        <td>Algoritmo </td>
        <td>Specificare se si desidera utilizzare RSA-SHA1 o RSA-SHA256. </td>
    </tr>
   <tr>
        <td>Codifica di input</td>
        <td>Selezionare il tipo di codifica di input che si desidera utilizzare:
        <ul>
        <li>ASCII</li>
        <li>Binario</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Codifica di output</td>
        <td>Seleziona il tipo di codifica di output da utilizzare:
        <ul>
        <li>Base 64</li>
        <li>Esadecimale</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Dati</td>
        <td>Immettere o mappare i dati da cui si desidera creare la firma.</td>
    </tr>
</table>

### Decrittare un messaggio PGP

Questo modulo consente di decrittografare un messaggio utilizzando chiavi pubbliche e private.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chiave privata]</td>
        <td>Seleziona la chiave privata del destinatario da utilizzare per questo messaggio. Per aggiungere una chiave privata, fare clic su <b>Aggiungi</b> e immettere il nome, il testo e la passphrase della chiave.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public Key]</td>
        <td>Immetti la chiave pubblica del mittente. Questa operazione può autenticare l’identità del mittente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Messaggio]</td>
        <td>Mappa il messaggio da decrittografare.</td>
    </tr>
</table>

### Crittografare un messaggio PGP

Questo modulo consente di crittografare un messaggio utilizzando chiavi pubbliche e private.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Chiave privata]</td>
        <td>Immetti la chiave privata del mittente. Questa operazione può autenticare l’identità del mittente.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public Key]</td>
        <td>Immetti la chiave pubblica del destinatario.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Messaggio]</td>
        <td>Immetti il messaggio da crittografare.</td>
    </tr>
    </table>
