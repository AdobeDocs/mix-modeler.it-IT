---
title: Flusso di lavoro di Mix Modeler
description: Scopri il flusso di lavoro tipico di Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 33883626d8e7aca2eecc3571593be53ef41ac458
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# Flusso di lavoro di Mix Modeler

Un flusso di lavoro tipico in Mix Modeler è simile al seguente:

![Testo alternativo](../assets/ApplicationWorkflow.svg)

|  | Attività | Descrizione |
|---|---|---|
| ![Dati](../assets/icons/Data.svg){width="100"} | [**Acquisire dati**](../ingest-data/overview.md) | Acquisisci dati evento da Experienci Platform (ad esempio Adobe Analytics, Web SDK, altre origini), dati aggregati dai canali di marketing (ad esempio TV, giardini murati, e-mail, attività possedute e gestite), dati di fattori esterni dai clienti (ad esempio le variazioni di prezzo nel servizio di abbonamento) e dati di fattori interni (ad esempio i piani delle vacanze). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Armonizzare i dati**](../harmonize-data/overview.md) | Configura le regole di mappatura e di risoluzione dei conflitti per unire i vari set di dati di marketing necessari per misurare e pianificare le prestazioni della campagna in Mix Modeler. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Configurare i modelli**](../models/create.md) | Configura le istanze del modello con i punti di contatto di marketing (ad esempio i canali) e le definizioni di conversione. |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**Formazione e valutazione dei modelli**](../models/overview.md) | Crea punteggi aggregati e a livello di evento utilizzando l’apprendimento automatico e il punteggio. |
| ![FileChart](../assets/icons/FileChart.svg){width="100"} | [**Creare piani**](../plans/overview.md) | Determinare la migliore allocazione di fondi di marketing per raggiungere un obiettivo aziendale utilizzando l’output dei modelli Mix Modeler. |
| ![Dashboard di](../assets/icons/Dashboard.svg){width="100"} | [**Dashboard panoramica**](../dashboard/overview.md) | Ottieni informazioni su dati, modelli e piani armonizzati utilizzando vari widget configurabili. |

{style="table-layout:auto"}
