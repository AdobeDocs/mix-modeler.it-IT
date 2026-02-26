---
title: Consulta le note sulla versione corrente di Mix Modeler
description: Note sulla versione più recente di Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 0a5fdbe90c4a32de45f4f2756f080dc265f5fbb7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 8%

---

# Note sulla versione corrente di Mix Modeler

**Ultimo aggiornamento**: 26 febbraio 2026.

Queste note sulla versione descrivono l’ultima versione di Mix Modeler. I rilasci di Mix Modeler funzionano su un modello di consegna continua, che consente una cadenza di rilascio mensile approssimativa. Di conseguenza, queste note sulla versione vengono aggiornate e quindi controllate regolarmente.


## Febbraio 2026

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **Flusso di lavoro dei fattori armonizzati** | I fattori sono ora gestiti come parte di un [flusso di lavoro dei fattori armonizzati](/help/harmonize-data/overview.md#factors). In questo modo è più semplice [definire i dati dei fattori](/help/ingest-data/schemas.md#factor-standard-fields-field-group), [gestire i fattori interni ed esterni come parte delle regole del set di dati](/help/harmonize-data/dataset-rules.md#factor-datasets) e utilizzare i dati dei fattori in [modelli](/help/models/build.md#configure). | giovedì 25 febbraio 2026 | giovedì 25 febbraio 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Definisci i campi armonizzati in modo da poter analizzare in profondità il reporting del modello utilizzando [campi di reporting di approfondimenti granulari](/help/models/build.md#granular-insights-reporting-fields), invece di dover creare modelli separati. | giovedì 18 febbraio 2026 | giovedì 18 febbraio 2026 |

## Gennaio 2026

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Tabella regole set di dati aggiornata](/help/harmonize-data/dataset-rules.md). È possibile cercare una o più regole del set di dati e visualizzarle, modificarle o eliminarle direttamente dalla tabella. | mercoledì 13 gennaio 2026 | mercoledì 13 gennaio 2026 |
| **[!UICONTROL Current spend]** | Aggiungi un punto di spesa corrente nella [visualizzazione della curva di risposta marginale](/help/models/insights.md#marginal-response-curves) in Approfondimenti modello. | mercoledì 13 gennaio 2026 | mercoledì 13 gennaio 2026 |
| **[!UICONTROL Sort and resize columns]** | È stato aggiunto l&#39;ordinamento e il ridimensionamento delle colonne nella tabella [Modelli](/help/models/overview.md) e [Piani](/help/plans/overview.md). | mercoledì 13 gennaio 2026 | mercoledì 13 gennaio 2026 |
| **Correzioni** | Correzioni per i seguenti biglietti: <ul><li>AMM-3328: Input sul campo disattivato per i nuovi operatori per i fattori</li><li>AMM-3359: Selezione data e blocco casella combinata.</li><li>AMM-3441: la duplicazione di un piano non viene compilata automaticamente nell&#39;intervallo di date e nel budget.</li></ul> | mercoledì 13 gennaio 2026 | mercoledì 13 gennaio 2026 |


## Strategia di rilascio

[!UICONTROL Mix Modeler] utilizza i flag di funzionalità (noti anche come &quot;interruttori&quot;) per controllare la visibilità delle nuove funzionalità, consentendo test su scala controllati prima del rilascio completo. Questa strategia di rilascio include le seguenti fasi:

* **Test limitati**: un rilascio graduale inizia con il test da parte degli utenti interni di Adobe. Viene quindi reso disponibile a un piccolo gruppo di clienti per garantire che la funzione soddisfi le esigenze e le aspettative dei clienti.

* **Inizio rollout**: il rollout di una versione graduale inizia con la fase Test limitato. La versione viene quindi scalata dallo 0% al 100% di disponibilità ai clienti nel corso di un paio di mesi. Il rollout graduale avviene a livello di organizzazione Experience Cloud, in modo che tutti gli utenti autorizzati in un’organizzazione ricevano la stessa esperienza.
