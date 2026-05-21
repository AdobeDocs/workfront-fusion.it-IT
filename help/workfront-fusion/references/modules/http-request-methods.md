---
title: Metodi di richiesta HTTP
description: Quando configuri una chiamata API in un modulo, devi selezionare il metodo di richiesta HTTP. In questo articolo vengono descritti i metodi disponibili e i motivi per cui è consigliabile selezionarli.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
TQID: https://experienceleague.adobe.com/Z11y3dk6PtoN11Gja8S2ZyJlTJZNZfXfcPPrNJWvbRk
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 303
ht-degree: 1%

---

# Metodi di richiesta HTTP

Quando configuri una chiamata API in un modulo, devi selezionare il metodo di richiesta HTTP. In questo articolo vengono descritti i metodi disponibili e i motivi per cui è consigliabile selezionarli.

## Metodi HTTP

Utilizza uno dei seguenti metodi HTTP.

* **[!UICONTROL GET]**: recupera i dati da un server Web in base ai parametri. [!UICONTROL GET] richiede una rappresentazione della risorsa specificata e, in caso di esito positivo, riceve un messaggio di risposta [!UICONTROL 200 OK] con il contenuto richiesto.
* **[!UICONTROL POST]**: invia dati a un server Web in base ai parametri. Le richieste [!UICONTROL POST] includono azioni come il caricamento di un file. Più [!UICONTROL POST]s possono produrre un risultato diverso rispetto a un singolo [!UICONTROL POST]. Prestare quindi attenzione all&#39;invio involontario di più [!UICONTROL POST]. Se un [!UICONTROL POST] ha esito positivo, si riceve un messaggio di risposta [!UICONTROL 200 OK].
* **[!UICONTROL PUT]**: invia dati a una posizione nel server Web in base ai parametri. Le richieste [!UICONTROL PUT] includono azioni come il caricamento di un file. La differenza tra [!UICONTROL PUT] e [!UICONTROL POST] è che PUT è idempotente, il che significa che il risultato di un singolo [!UICONTROL PUT] riuscito è lo stesso di molti [!UICONTROL PUT] identici. Se un metodo PUT ha esito positivo, si riceve un messaggio di risposta 200 (in genere 201 o 204).
* **[!UICONTROL PATCH]**: (non disponibile per alcuni moduli di chiamata API) Applica modifiche parziali a una risorsa su un server Web in base ai parametri. [!UICONTROL PATCH] non è idempotente, il che significa che il risultato di più [!UICONTROL PATCH] potrebbe avere conseguenze indesiderate. Se un [!UICONTROL PATCH] ha esito positivo, riceverai un messaggio di risposta di 200 (in genere 204).
* **[!UICONTROL DELETE]**: elimina la risorsa specificata dal server Web in base ai parametri (se la risorsa esiste). Se un [!UICONTROL DELETE] ha esito positivo, verrà visualizzato un messaggio di risposta di 200 OK.
