---
title: Acquisire dati
description: Scopri come acquisire dati in Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 1dbdee00f518d98241fc042e2aabc0e40d5a9153
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 14%

---

# Acquisire dati

Mix Modeler funziona con i dati a livello di evento, aggrega i dati di riepilogo delle attività di marketing provenienti da vari giardini murati e aggrega o riassume i dati provenienti da qualsiasi altra origine, come pubblicità offline, fattori interni o esterni.

I clienti possono utilizzare qualsiasi tipo di dati acquisito in Experienci Platform come set di dati e basato su schemi che utilizzano ExperienceEvent XDM o Metriche di riepilogo XDM come classe base.

Ad esempio:

* dati raccolti utilizzando il connettore di origine di Adobe Analytics e trasformati in set di dati conformi all’impostazione predefinita o a una versione personalizzata dello schema di Adobe Analytics, oppure in alternativa,
* dati raccolti utilizzando l’SDK per web di Experienci Platform, l’SDK per dispositivi mobili o l’API del server di rete Edge per raccogliere le interazioni dei clienti su web, dispositivi mobili o qualsiasi altro tipo di dispositivo,
* dati aggregati o riassuntivi provenienti da giardini murati (come Facebook, YouTube), da fonti di traffico o da dati pubblicitari offline,
* dati aggregati o di riepilogo non di marketing contenenti fattori interni o esterni utili per la creazione di modelli.

Puoi utilizzare qualsiasi tipo di meccanismo, supportato da Experienci Platform, per acquisire a livello di evento l’esperienza, aggregare i dati relativi alle attività di marketing e i dati provenienti da altre origini. Ad esempio gli SDK di Experience Platform, le API, i connettori di origine e l’acquisizione in streaming e batch.


## Linee guida

Per acquisire i dati in Experienci Platform per l’utilizzo con Mix Modeler, segui queste linee guida:

* Non dovrebbero esserci sovrapposizioni nei dati incrementali aggiunti ai set di dati.
* Tutti i dati provenienti da una singola origine devono avere la stessa granularità.
* Data e granularità sono campi obbligatori nello schema sottostante per tutti i dati aggregati acquisiti come set di dati
* Canale è un campo obbligatorio nello schema sottostante per tutte le attività di marketing e i dati di spesa acquisiti come set di dati.


## Esempi

Di seguito trovi alcuni esempi di dati utilizzati in genere in Mix Modeler oltre ai dati dell’evento di esperienza più standard.

+++ Aggregazione dei dati relativi allo sforzo di marketing

| Geo | Data | Tipo di data | Channel | Campaign | Clic | Guadagnato | Coinvolgimento | Impression | Open | Di proprietà | Inviate |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|
| AMER | 2021-10-31 | giorno | EMAIL | | 12752 | | | | | | 1132945 |
| AMER | 2021-10-31 | giorno | FB | | 148844 | | | | | | |
| AMER | 2021-10-31 | giorno | YT | | | | 2314452 | | | | |
| JPN | 2021-10-21 | giorno | EMAIL | | 21089 | | | | | | 3283626 |
| JPN | 2021-10-21 | giorno | SOCIAL | | | | 621 | | | | |

{style="table-layout:auto"}

+++

+++ Aggregare i dati di conversione

| Geo | Data | Tipo di data | Prodotto | Unità vendute | Ricavi |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | giorno | Economia creatrice | 603 | 36537.68 |
| EMEA | 2021-09-13 | giorno | Metaverse | 55 | 21704.37 |
| JPN | 2022-05-30 | giorno | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | giorno | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Dati fattori esterni

| Dati | Tipo di data | Fattore | Valore |
|---|:---:|:---:|:---|
| 2020-08-02 | settimana | SPX | 3325.866 |
| 2020-08-09 | settimana | SPX | 3364.158 |
| 2020-08-16 | settimana | SPX | 3385.858 |
| 2020-08-23 | settimana | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Per lavorare con i dati in Mix Modeler, è necessario che i dati vengano raccolti in set di dati e modellati secondo gli schemi di Experienci Platform. L’interfaccia Mix Modeler consente di accedere facilmente sia all’interfaccia utente Schemi che a quella Set di dati.


>[!MORELIKETHIS]
>
>Per ulteriori dettagli su come gestire schemi e set di dati, consulta:
>
>* [Schemi](schemas.md)
>* [Set di dati](datasets.md)
