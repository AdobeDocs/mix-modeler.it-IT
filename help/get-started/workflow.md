---
title: Flusso di lavoro di Mix Modeler
description: Comprendere il flusso di lavoro tipico di Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
TQID: https://experienceleague.adobe.com/PAKsHAqpIeBVCJGIPS2ZqWw-vVpS9LUpYdJRFKP0ynY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
  - id: d822825b-9821-40d5-9b0d-42a9e3f317c5
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: ba4fd72c-282e-4fb6-abc1-08e6fb87b2ad
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
  - id: c89e26b6-808d-4500-8b01-450a63466999
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
  - id: d7b067e6-4f39-41e9-a081-7650346a84cd
  - id: b2520ae7-8f6c-4952-935e-aacc2c10256f
  - id: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:15:33.908Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 1%

---

# Flusso di lavoro di Mix Modeler

Guarda questo video per un’introduzione al flusso di lavoro degli utenti in Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3440211/?captions=ita&learn=on)


Un flusso di lavoro tipico in Mix Modeler è costituito dalle seguenti attività:

![Testo alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Attività | Descrizione |
|---|---|---|
| ![Dati](/help/assets/icons/Data.svg){width="100"} | [**Acquisire dati**](../ingest-data/overview.md) | Acquisisci dati evento da Experience Platform (ad esempio Adobe Analytics, Web SDK, altre origini), dati aggregati dai canali di marketing (ad esempio TV, giardini murati, e-mail, attività possedute e gestite), dati di fattori esterni dai clienti (ad esempio le variazioni di prezzo nel servizio di abbonamento) e dati di fattori interni (ad esempio i piani delle feste). |
| ![ControlloDati](/help/assets/icons/DataCheck.svg){width="100"} | [**Armonizzare i dati**](../harmonize-data/overview.md) | Configura le regole di mappatura e di risoluzione dei conflitti per unire i vari set di dati di marketing necessari per misurare e pianificare le prestazioni della campagna in Mix Modeler. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Modelli di compilazione**](../models/overview.md) | Crea istanze di modello con punti di contatto di marketing (ad esempio canali), definizioni di conversione e fattori interni ed esterni. |
| ![DatiFile](/help/assets/icons/FileData.svg){width="100"} | [**Formazione e valutazione dei modelli**](../models/overview.md) | Crea punteggi aggregati e a livello di evento utilizzando l’apprendimento automatico e il punteggio. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Piani di compilazione**](../plans/overview.md) | Creare e creare piani. Determinare la migliore allocazione di fondi di marketing per raggiungere un obiettivo aziendale utilizzando i risultati dei modelli di Mix Modeler. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Dashboard panoramica**](../dashboard/overview.md) | Ottieni informazioni su dati, modelli e piani armonizzati utilizzando varie visualizzazioni configurabili. |

{style="table-layout:auto"}

Di seguito è illustrata una panoramica del modo in cui i dati di input possono fluire in Mix Modeler e di come Mix Modeler può produrre dati di output per la propria interfaccia ma anche per altre soluzioni, come Customer Journey Analytics.

![Flusso dati output input Mix Modeler](../assets/mm-input-output.png)

<!--
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)
-->
