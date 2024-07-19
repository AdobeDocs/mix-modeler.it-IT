---
title: Dati punteggio
description: Scopri come i dati di punteggio di un modello in Mix Modeler vengono mantenuti.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 5%

---

# Dati punteggio

Come parte del punteggio di un modello, i dati di punteggio vengono mantenuti all’interno di un set di dati in Experience Platform. Questo set di dati è conforme a uno schema creato per ogni modello nell’istanza Mix Modeler.

Lo schema per il punteggio dei dati è denominato come `AMM AI Schema - <name of model> <id>`. Esempio: `AMM AI Schema - Model for Online Conversion 10120`.

Il set di dati, che mantiene i dati di punteggio per un modello, è denominato come `AMM AI Aggregrate Scores - <id>`, ad esempio `AMM AI Aggregrate Scores - 10120`.


## Schema

Lo schema include un gruppo di campi con un oggetto contenente i dettagli dei punteggi. L’oggetto è costituito dai campi seguenti.

| Nome campo | Tipo | Definizione |
|---|---|---|
| **gruppoCampagne** | Stringa | Nome del gruppo della campagna. |
| **nomeCampagna** | Stringa | Nome della campagna. |
| **contributo** | Doppio | Contributo attribuito a questa conversione per il punto di contatto specificato. |
| **conversionEndDate** | Data | Data di fine della finestra di conversione. |
| **conversionName** | Stringa | Nome della conversione creata durante il passaggio di impostazione della definizione di conversione. |
| **conversionStartDate** | Data | Data di inizio della finestra di conversione. |
| **geo** | Stringa | La posizione geografica in cui si è verificata la conversione. |
| **mediaChannel** | Stringa | Nome del canale utilizzato durante il passaggio di configurazione del punto di contatto. |
| **mediaSubChannel** | Stringa | Nome del sottocanale. |
| **ricavi** | Doppio | Ricavi attribuiti a questa conversione per il punto di contatto specificato. |
| **scoreCreatedTime** | DateTime | Ora di creazione di questo record di punteggio. |
| **dataFinePuntoDiContatto** | Data | Data di fine della finestra del punto di contatto. |
| **nomePuntoDiContatto** | Stringa | Nome del punto di contatto creato durante il passaggio di impostazione della definizione del punto di contatto. Attualmente il punto di contatto è definito sul canale multimediale. |
| **dataInizioPuntoDiContatto** | Data | Data di inizio della finestra del punto di contatto. |

Per ulteriori informazioni, vedere [Schemi](../ingest-data/schemas.md).
