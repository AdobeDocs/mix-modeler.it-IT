---
title: Panoramica dell’acquisizione dei dati
description: Scopri come acquisire dati in Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: bb05cee1d4e2245cf665e5dcea17a30c5c0cf203
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 7%

---

# Panoramica dell’acquisizione dei dati

Mix Modeler utilizza dati a livello di evento, aggrega o riassume i dati delle attività di marketing provenienti da vari giardini murati, e aggrega o riassume i dati provenienti da qualsiasi altra origine, ad esempio pubblicità offline, fattori interni o esterni.

I clienti possono utilizzare qualsiasi tipo di dati acquisito in Experience Platform come set di dati e basato su schemi che utilizzano ExperienceEvent XDM o Metriche di riepilogo XDM come classe base.

Ad esempio:

* dati raccolti utilizzando il connettore di origine di Adobe Analytics e trasformati in set di dati conformi all’impostazione predefinita o a una versione personalizzata dello schema di Adobe Analytics, oppure in alternativa,
* dati raccolti utilizzando Experience Platform Web SDK, Mobile SDK o Edge Network Server API per raccogliere le interazioni dei clienti su web, dispositivi mobili o qualsiasi altro tipo di dispositivo,
* dati aggregati o riassuntivi provenienti da giardini murati (come Facebook, YouTube), da fonti di traffico o da dati pubblicitari offline,
* dati aggregati o di riepilogo non di marketing contenenti fattori interni o esterni utili per la creazione di modelli.

Puoi utilizzare qualsiasi tipo di meccanismo supportato da Experience Platform per acquisire a livello di evento l’esperienza, aggregare i dati relativi alle attività di marketing e i dati provenienti da altre origini. I meccanismi di acquisizione includono gli SDK di Experience Platform, le API, i connettori di origine, lo streaming e l’acquisizione batch. Per ulteriori informazioni sull&#39;acquisizione dei dati in Experience Platform per l&#39;utilizzo in Adobe Mix Modeler, consulta [Panoramica sull&#39;acquisizione dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/home).

## Linee guida

Per acquisire i dati in Experience Platform per l’utilizzo con Mix Modeler, segui queste linee guida:

* Non dovrebbero esserci sovrapposizioni nei dati incrementali aggiunti ai set di dati.
* Tutti i dati provenienti da una singola origine devono avere la stessa granularità.
* Data e granularità sono campi obbligatori nello schema sottostante per tutti i dati aggregati acquisiti come set di dati
* Canale è un campo obbligatorio nello schema sottostante per tutte le attività di marketing e i dati di spesa acquisiti come set di dati.


## Esempi

Di seguito trovi alcuni esempi di dati utilizzati in genere in Mix Modeler oltre ai dati dell’evento di esperienza più standard.

+++ Aggregazione dei dati relativi allo sforzo di marketing

| Geo | Data | Tipo di data | Channel | Campaign | Clic | Guadagnato | Coinvolgimento | Impression | Open | Di proprietà | Inviato | Spesa |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 31/10/2021 | giorno | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 31/10/2021 | giorno | FB | | 148844 | | | | | | | 42111 |
| AMER | 31/10/2021 | giorno | YT | | | | 2314452 | | | | | 10540 |
| JPN | 21/10/2021 | giorno | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 21/10/2021 | giorno | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Aggregare i dati di conversione

| Geo | Data | Tipo di data | Prodotto | Unità vendute | Ricavi |
|---|:---|:---:|---|--:|--:|
| EMEA | 13/09/2021 | giorno | Economia creatrice | 603 | 36537,68 |
| EMEA | 13/09/2021 | giorno | Metaverse | 55 | 21704,37 |
| JPN | 30/05/2022 | giorno | Pro Imaging | 487 | 64469,60 |
| JPN | 30/05/2022 | giorno | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Dati fattori esterni

| Dati | Tipo di data | Fattore | Valore |
|---|:---:|:---:|:---|
| 02/08/2020 | settimana | SPX | 3325,866 |
| 09/08/2020 | settimana | SPX | 3364,158 |
| 16/08/2020 | settimana | SPX | 3385,858 |
| 23/08/2020 | settimana | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Per lavorare con i dati in Mix Modeler, è necessario che siano raccolti in set di dati e modellati secondo gli schemi in Experience Platform. L’interfaccia di Mix Modeler consente di accedere facilmente sia agli schemi di Experience Platform che all’interfaccia utente dei set di dati.


## Convalida

Per verificare se i dati sono disponibili correttamente in Mix Modeler, puoi effettuare le seguenti operazioni:

* Utilizza le visualizzazioni in [Panoramica](/help/overview.md).
* Scarica e controlla i dati da [Dati armonizzati](/help/harmonize-data/overview.md) nei set di dati armonizzati.

Per verificare se i dati vengono acquisiti correttamente in Experience Platform, è possibile [scrivere ed eseguire query SQL utilizzando Experience Platform Query Service](https://experienceleague.adobe.com/it/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Per ulteriori dettagli su come gestire schemi e set di dati, consulta:
>
>* [Schemi](schemas.md)
>* [Set di dati](datasets.md)
