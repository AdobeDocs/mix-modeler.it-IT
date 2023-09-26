---
title: Acquisire dati
description: Scopri come acquisire i dati in Adobe Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
source-git-commit: ae1c74ed2edf1e69e7ab77d16aba797921c14ad9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 14%

---


# Acquisire dati

Adobe Mix Modeler funziona sia con i dati a livello di evento che con i dati aggregati delle attività di marketing provenienti da vari giardini murati. I clienti possono utilizzare tutti i tipi di dati acquisiti in Adobe Experience Platform come set di dati e basati su schemi basati su XDM Experience Event.

Ad esempio:

* dati raccolti utilizzando il connettore di origine di Adobe Analytics e trasformati in set di dati conformi all’impostazione predefinita o a una versione personalizzata dello schema di Adobe Analytics, oppure in alternativa,
* dati raccolti utilizzando Adobe Experience Platform Web SDK, Mobile SDK o l’API del server di rete Edge per raccogliere le interazioni dei clienti su web, dispositivi mobili o qualsiasi altro tipo di dispositivo,
* dati di riepilogo da diverse origini del traffico o del giardino protetto, basati su uno schema che include la classe XDM Summary Metrics con il gruppo di campi Riepilogo traffico e conversione,
* dati non commerciali (ad esempio indicatori macroeconomici) utili per la creazione di modelli,

Puoi utilizzare qualsiasi tipo di meccanismo supportato da Adobe Experience Platform per acquisire il livello dell’evento esperienza e aggregare i dati delle attività di marketing. Ad esempio gli SDK di Adobe Experience Platform, le API, i connettori di origine e l’acquisizione in streaming e batch.


## Linee guida

Per acquisire in Adobe Experience Platform i dati da utilizzare con Adobe Mix Modeler, attieniti alle seguenti linee guida:

* Non dovrebbero esserci sovrapposizioni nei dati incrementali aggiunti ai set di dati.
* Tutti i dati provenienti da una singola origine devono avere la stessa granularità.
* Data e granularità sono campi obbligatori nello schema sottostante per tutti i dati aggregati acquisiti come set di dati
* Canale è un campo obbligatorio nello schema sottostante per tutte le attività di marketing e i dati di spesa acquisiti come set di dati.


## Esempi

Di seguito sono riportati alcuni esempi di dati utilizzati in genere in Adobe Mix Modeler oltre i dati degli eventi di esperienza standard.

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

Per lavorare con i dati in Adobe Mix Modeler, è necessario che i dati vengano raccolti in set di dati e modellati secondo gli schemi in Adobe Experience Platform. L’interfaccia di Adobe Mix Modeler consente di accedere facilmente sia all’interfaccia utente Schemi che a quella Set di dati.

>[!MORELIKETHIS]
>
>Per ulteriori dettagli su come gestire schemi e set di dati, consulta:
>
>* [Schemi](schemas.md)
>* [Set di dati](datasets.md)
