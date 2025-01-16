---
title: Attività del rilascio di Workfront Fusion:&nbsp;Settimana del 30 agosto 2021
description: Attività del rilascio di Workfront Fusion:&nbsp;Settimana del 30 agosto 2021
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Attività di rilascio di Workfront Fusion: settimana del 30 agosto 2021

Questa pagina descrive tutti i miglioramenti apportati ad Adobe Workfront Fusion la settimana del 30 agosto 2021.

Per un elenco di tutte le modifiche recenti, vedere [Attività di Adobe Workfront Fusion release](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Per un elenco delle correzioni di bug recenti in Workfront Fusion, vedere la pagina [Aggiornamenti di manutenzione di Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) e verificare la presenza di eventuali aggiornamenti etichettati Aggiornamento di manutenzione di Workfront Fusion.

## Filtra gli eventi che attivano il modulo Workfront > Osserva eventi

1. Configura un filtro personalizzato per gli eventi che attivano il modulo Workfront > Osserva eventi

   Per ridurre il numero di esecuzioni di scenari non necessari, abbiamo aggiornato il modulo Workfront > Record di controllo per abilitare il filtro degli eventi. Ora è possibile impostare un filtro quando si crea un webhook. Questo consente allo scenario di attivarsi solo quando l’evento soddisfa determinati criteri.

   Il filtro eventi offre attualmente le seguenti operazioni:

   * Equal: attiva uno scenario solo quando un evento corrisponde alle condizioni del filtro. Ad esempio, puoi impostare un filtro che attivi uno scenario solo se l’evento si verifica in un progetto specifico.
   * Not Equal: attiva uno scenario solo se un evento non corrisponde alle condizioni del filtro. Ad esempio, puoi creare un filtro che attiva uno scenario solo se il problema in cui si verifica un evento non ha lo stato Chiuso.

   In precedenza, il modulo Record di controllo recuperava tutti i record. Gli utenti potevano filtrare solo impostando i filtri più avanti nello scenario.

   Per sfruttare il filtro degli eventi, crea un nuovo webhook nel modulo Osserva eventi. Al momento non è possibile modificare i webhook esistenti per includere questa funzionalità. È consigliabile creare nuovi webhook utilizzando i filtri evento per gli scenari esistenti.

1. Escludi gli eventi attivati dalla connessione corrente.

   Per semplificare la configurazione dei webhook per il modulo Workfront > Osserva eventi, abbiamo incluso il filtro eventi più comune. Ora il webhook ha un’opzione per filtrare eventuali modifiche apportate dai moduli utilizzando la connessione specificata per il modulo Osserva eventi. In altre parole, con questo filtro abilitato, eventuali modifiche apportate dall’utente di Workfront associato a tale connessione non possono attivare lo scenario.

   In precedenza, questo filtro non era disponibile. Pertanto, è stato più facile per le modifiche apportate nei moduli Workfront attivare scenari contenenti tali moduli, causando potenzialmente l’attivazione di scenari in un ciclo infinito.
