---
title: Moduli JWT
description: L'app  [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fornisce un modulo che crea token JWT in base all'algoritmo fornito.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Modulo [!UICONTROL JWT]

L&#39;app [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fornisce un modulo che crea token JWT in base all&#39;algoritmo specificato.

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
   <p>Requisito licenza legacy: [!UICONTROL [!DNL Workfront Fusion] per automazione e integrazione lavoro, [!UICONTROL [!DNL Workfront Fusion] per automazione lavoro</p>
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

## Informazioni sull’API JWT

Il connettore JWT utilizza quanto segue:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">Tag API</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## Modulo JWT e relativi campi

### Genera JWT

Questo modulo genera un JWT basato sull’algoritmo selezionato.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>Seleziona l’algoritmo con cui desideri generare il JWT.</p> <ul>
   <li><b>HS256</b>: HMAC con algoritmo hash SHA-256</li>
   <li><b>HS384</b>: HMAC con algoritmo hash SHA-384</li>
   <li><b>HS512</b>: HMAC con algoritmo hash SHA-512</li>
   <li><b>RS256</b>: RSASSA-PKCS1-v1_5 con algoritmo hash SHA-256</li>
   <li><b>RS384</b>: RSASSA-PKCS1-v1_5 con algoritmo hash SHA-384</li>
   <li><b>RS512</b>: RSASSA-PKCS1-v1_5 con algoritmo hash SHA-512</li>
   <li><b>PS256</b>: RSASSA-PSS che utilizza l'algoritmo hash SHA-256 (solo il nodo ^6.12.0 O &gt;=8.0.0)</li>
   <li><b>PS384</b>: RSASSA-PSS tramite algoritmo hash SHA-384 (solo il nodo ^6.12.0 O &gt;=8.0.0)</li>
   <li><b>PS512</b>: RSASSA-PSS che utilizza l'algoritmo hash SHA-512 (solo il nodo ^6.12.0 O &gt;=8.0.0)</li>
   <li><b>ES256</b>: ECDSA che utilizza la curva P-256 e l'algoritmo hash SHA-256</li>
   <li><b>ES384</b>: ECDSA che utilizza la curva P-384 e l'algoritmo hash SHA-384</li>
   <li><b>ES512</b>: ECDSA che utilizza la curva P-521 e l'algoritmo hash SHA-512</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>Per ogni elemento del payload che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore dell'elemento.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>Per ogni elemento di opzione che si desidera aggiungere, fare clic su <b>Aggiungi elemento</b> e immettere la chiave e il valore dell'elemento.</p> <p>Sono disponibili le seguenti chiavi:
   <ul>
   <li><b>algoritmo</b>: (impostazione predefinita: RS256)</li>
   <li><b>expiresIn</b>: espresso in secondi o una stringa che descrive un intervallo di tempo (ad esempio 2 giorni, 10h, 7d). Un valore numerico viene interpretato come un conteggio di secondi. Se utilizzi una stringa, assicurati di fornire le unità di tempo (giorni, ore, ecc.), altrimenti per impostazione predefinita viene utilizzata l’unità in millisecondi (120 è uguale a 120 ms).</li>
   <li><b>notBefore</b>: espresso in secondi o una stringa che descrive un intervallo di tempo (ad esempio, 2 giorni, 10h, 7d). Un valore numerico viene interpretato come un conteggio di secondi. Se utilizzi una stringa, assicurati di fornire le unità di tempo (giorni, ore, ecc.), altrimenti per impostazione predefinita viene utilizzata l’unità in millisecondi (120 è uguale a 120 ms).
</li>
   <li><b>pubblico</b></li>
   <li><b>emittente</b></li>
   <li><b>jwtid</b></li>
   <li><b>oggetto</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>intestazione</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b>: se <code>true</code>, la funzione di firma modificherà direttamente l'oggetto payload. Questo è utile se hai bisogno di un riferimento non elaborato al payload dopo che le attestazioni sono state applicate, ma prima che sia stato codificato in un token.</li>
   <li><b>allowInsecureKeySizes</b>: se <code>true</code>, consente l'utilizzo di chiavi private con un modulo inferiore a 2048 per RSA.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>: se <code>true</code>, consente chiavi asimmetriche che non corrispondono all'algoritmo specificato. Questa opzione è destinata solo alla retrocompatibilità e deve essere evitata.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
