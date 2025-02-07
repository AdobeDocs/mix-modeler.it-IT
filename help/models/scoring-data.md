---
title: Dati punteggio USA
description: Scopri come i dati di punteggio di un modello in Mix Modeler vengono mantenuti.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: f073e8f44fc2aa731a69725ebdb99700d1f91a91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 6%

---

# Utilizzare i dati di punteggio

Come parte del punteggio di un modello, i dati di punteggio vengono mantenuti all’interno di un set di dati in Experience Platform. Se hai abilitato l’attribuzione multi-touch durante la creazione del modello, i dati aggiuntivi del punteggio dell’evento vengono mantenuti all’interno di un set di dati in Experience Platform.

Ciascuno di questi set di dati è conforme a uno schema. Questo articolo documenta questi schemi.


## Schema dati di punteggio aggregato

Lo schema per il punteggio dei dati è denominato come `AMM AI Schema - <name of model> <id>`. Esempio: `AMM AI Schema - Model for Online Conversion 10120`.

Il set di dati, che mantiene i dati di punteggio per un modello, è denominato come `AMM AI Aggregrate Scores - <id>`, ad esempio `AMM AI Aggregrate Scores - 10120`.

Lo schema include un gruppo di campi con un oggetto contenente i dettagli dei punteggi. L’oggetto è costituito dai campi seguenti.

| Nome campo | Tipo | Definizione |
|---|---|---|
| `campaignGroup` | Stringa | Nome del gruppo della campagna. |
| `campaignName` | Stringa | Nome della campagna. |
| `contribution` | Doppio | Contributo attribuito a questa conversione per il punto di contatto specificato. |
| `conversionEndDate` | Data | Data di fine della finestra di conversione. |
| `conversionName` | Stringa | Nome della conversione creata durante il passaggio di impostazione della definizione di conversione. |
| `conversionStartDate` | Data | Data di inizio della finestra di conversione. |
| `geo` | Stringa | La posizione geografica in cui si è verificata la conversione. |
| `mediaChannel` | Stringa | Nome del canale utilizzato durante il passaggio di configurazione del punto di contatto. |
| `mediaSubChannel` | Stringa | Nome del sottocanale. |
| `revenue` | Doppio | Ricavi attribuiti a questa conversione per il punto di contatto specificato. |
| `scoreCreatedTime` | DateTime | Timestamp di creazione di questo record di punteggio. |
| `touchpointEndDate` | Data | Data di fine della finestra del punto di contatto. |
| `touchpointName` | Stringa | Nome del punto di contatto creato durante il passaggio di impostazione della definizione del punto di contatto. Attualmente il punto di contatto è definito sul canale multimediale. |
| `touchpointStartDate` | Data | Data di inizio della finestra del punto di contatto. |


## Schema dati per il punteggio evento

Lo schema per il punteggio dei dati è denominato come `Attribution AI Scores - <name of model> <id> - Schema`. Esempio: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

Il set di dati, che mantiene i dati di punteggio per un modello, è denominato come `Attribution AI Scores - <name of model> <id>`, ad esempio `Attribution AI Scores - Model for Online Conversion 10120 `.

Lo schema include un gruppo di campi contenente un oggetto con dettagli sui core. L&#39;oggetto è denominato come `attibution_AI_scores__<name of model> id`.

Il gruppo di campi contiene i campi seguenti.

| Nome campo | Tipo | Descrizione |
|---|---|---|
| `conversion` | Oggetto | Colonne di metadati di conversione. |
|     `passThrough` | Oggetto |  |
|         `eventType` | Stringa | |
|         `channel_typeAtSource` | Stringa | |
|      `dataSource` | Stringa | Identificazione univoca globale di un&#39;origine dati. <br> **Esempio:** `Adobe Analytics` |
|      `eventSource` | Stringa | La sorgente in cui si è verificato l’evento effettivo. <br> **Esempio:** `Adobe.com` |
|      `eventType` | Stringa | Il tipo di evento principale per questo record di serie temporali. <br> **Esempio:** `Order` |
|      `geo` | Stringa | La posizione geografica in cui è stata consegnata la conversione `placeContext.geo.countryCode`. <br> **Esempio:** `US` |
|      `path` | Stringa | |
|      `priceTotal` | Doppio | Ricavi ottenuti tramite la conversione <br> **Esempio:** `99.9` |
|      `product` | Stringa | L’identificatore XDM del prodotto stesso. <br> **Esempio:** `RX 1080 ti` |
|      `productType` | Stringa | Il nome visualizzato del prodotto presentato all’utente per questa visualizzazione prodotto. <br> **Esempio:** `Gpus` |
|      `quantity` | Intero | Quantità acquistata durante la conversione. <br> **Esempio:** `1` |
|      `receivedTimeStamp` | DateTime | Timestamp ricevuto della conversione. <br> **Esempio:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | Stringa | Stock Keeping Unit (SKU), l’identificatore univoco di un prodotto definito dal fornitore. <br> **Esempio:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Timestamp della conversione. <br> **Esempio:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Intero |  |
|      `totalTouchpointCount` | Intero | |
| `customerProfile` | Oggetto | Dettagli di identità dell’utente utilizzato per generare il modello. |
|      `identity` | Oggetto | |
|           `id` | Stringa | |
|           `namespace` | Stringa | Contiene i dettagli dell&#39;utente utilizzato per generare il modello, ad esempio `id` e `namespace`. |
| `touchpointsDetail` | Oggetto[] | L’elenco dei dettagli del punto di contatto che conducono alla conversione, ordinati per occorrenza del punto di contatto o marca temporale. |
|      `scores` | Oggetto | Contributo del punto di contatto a questa conversione come punteggio. |
|           `algorithmicInfluenced` | Doppio | Il punteggio influenzato è la frazione della conversione di cui è responsabile ogni punto di contatto di marketing. |
|           `algorithmicSourced` | Doppio | Il punteggio incrementale è la quantità di impatto marginale causato direttamente da un punto di contatto di marketing. |
|           `decayUnits` | Doppio | Punteggio di attribuzione basato su regole in cui i punti di contatto più vicini alla conversione ricevono più credito rispetto ai punti di contatto più lontani nel tempo dalla conversione. |
|           `firstTouch` | Doppio | Punteggio di attribuzione basato su regole che assegna tutti i crediti al punto di contatto iniziale in un percorso di conversione. |
|           `lastTouch` | Doppio | Punteggio di attribuzione basato su regole che assegna tutto il credito al punto di contatto più vicino alla conversione. |
|           `linear` | Doppio | Punteggio di attribuzione basato su regole che assegna lo stesso credito a ciascun punto di contatto in un percorso di conversione. |
|           `uShape` | Doppio | Punteggio di attribuzione basato su regole che assegna il 40% del credito al primo punto di contatto e il 40% del credito all’ultimo punto di contatto. Gli altri punti di contatto dividono il restante 20% in parti uguali. |
|      `touchPoint` | Oggetto | Metadati dei punti di contatto. |
|           `passThrough` | Oggetto | |
|                `eventType` | Stringa | |
|           `campaignGroup` | Stringa |  |
|           `campaignName` | Stringa | |
|           `campaignTag` | Stringa | |
|           `eventId` | Stringa | |
|           `geo` | Stringa | |
|           `mediaAction` | Stringa | |
|           `mediaChannel` | Stringa | |
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Intero | |
|      `lag` | Intero | |
|      `position` | Stringa | |
|      `touchpointCountToConversion` | Intero | |
|      `touchpointName` | Stringa | Nome del punto di contatto configurato durante la configurazione. <br> **Esempio:** `PAID_SEARCH_CLICK` |
| `conversionName` | Stringa | Nome della conversione configurata durante la configurazione. <br> **Esempio:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | Stringa | Segmento di conversione, ad esempio segmentazione geografica, rispetto al quale viene generato il modello. Quando i segmenti sono assenti, `segmentation` è uguale a `conversionName`. <br> **Esempio:** `ORDER_US` |





Per ulteriori informazioni, vedere [Schemi](../ingest-data/schemas.md).
