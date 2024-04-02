---
title: Armonizzare i dati
description: Scopri come armonizzare i dati in Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 7%

---

# Armonizzare i dati

I dati in Mix Modeler sono di natura diversa a seconda della fonte dei dati. I dati possono essere:

* dati aggregati o riassuntivi, ad esempio raccolti da fonti di dati provenienti da giardini murati o dati pubblicitari offline raccolti (come spendere) dall’esecuzione di una campagna su cartelloni pubblicitari, un evento o una campagna pubblicitaria fisica,
* dati evento, ad esempio da origini dati di prime parti. Questi dati dell’evento possono essere raccolti tramite il connettore di origine di Adobe Analytics da Adobe Analytics, oppure tramite l’SDK per web o mobile di Experienci Platform o l’API della rete Edge, oppure possono essere acquisiti tramite i connettori di origine.

Il servizio di armonizzazione di Mix Modeler assimila i dati aggregati e i dati evento in una visualizzazione dati coerente. Questa visualizzazione dati, combinata con dati di fattori interni ed esterni, è la sorgente dei modelli in Mix Modeler. Il servizio utilizza la granularità più elevata tra i diversi set di dati. Ad esempio, se un set di dati ha una granularità mensile e i set di dati rimanenti hanno granularità settimanale e giornaliera, il servizio di armonizzazione crea una visualizzazione dati con granularità mensile.

## Un esempio di dati armonizzati

Immagina di disporre dei seguenti set di dati per Mix Modeler.

**Set di dati 1**

Contiene il set di dati dell’attività di marketing di YouTube, con una granularità dei dati aggregati impostata su giornaliero.

| Data | Tipo di data | Channel | Campaign | Marchio | Geo | Clic | Spesa |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | giorno | YouTube | Y_Autunno_02 | BrandX | STATI UNITI | 10000 | 100 |
| 01-01-2022 | giorno | YouTube | Y_Autunno_02 | BrandX | STATI UNITI | 1000 | 10 |
| 01-03-2022 | giorno | YouTube | Y_Autunno_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | giorno | YouTube | Y_Summer_01 | Nullo | CA | 9000 | 80 |

{style="table-layout:auto"}


**Set di dati 2**

Contiene il set di dati dell’attività di marketing di Facebook, con una granularità del set di dati aggregati impostata su Settimanale.

| Data | Tipo di data | Channel | Campaign | Geo | Clic | Spesa |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | settimana | Facebook | FB_Autunno_01 | STATI UNITI | 8000 | 100 |
| 01-08-2022 | settimana | Facebook | FB_Autunno_02 | STATI UNITI | 1000 | 10 |
| 01-08-2022 | settimana | Facebook | FB_Autunno_01 | STATI UNITI | 7000 | 100 |
| 01-16-2022 | settimana | Facebook | FB_Estate_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Set di dati 3**

Un set di dati di conversione con granularità dell’insieme di dati aggregati impostata su Daily.

| Data | Tipo di data | Geo | Obiettivo | Ricavi |
|--- |:---: |---|---|---:|
| 01-01-2022 | giorno | STATI UNITI | Moda | 200 |
| 01-08-2022 | giorno | STATI UNITI | Moda | 10 |
| 01-08-2022 | giorno | STATI UNITI | Gioielli | 1100 |
| 01-16-2022 | giorno | CA | Gioielli | 80 |

{style="table-layout:auto"}


**Set di dati 4**

Un set di dati di esempio per l’evento esperienza (eventi Web SDK) dal cliente.

| Timestamp | Spazio dei nomi delle identità | ID identità | Channel | Clic |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Desideri creare un set di dati armonizzato con granularità impostata su Settimanale. I dati dell’evento vengono aggregati con granularità settimanale e aggiunti al set di dati armonizzato. Il risultato è:

**Set di dati armonizzato**

| Data | Tipo di data | Channel | Campaign | Marchio | Geo | Obiettivo | Clic | Spesa | Ricavi |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | settimana | YouTube | Y_Autunno_02 | BrandX | STATI UNITI | Nullo | 11000 | 110 | Nullo |
| 01-03-2022 | settimana | YouTube | Y_Autunno_01 | BrandY | CA | Nullo | 10000 | 100 | Nullo |
| 01-03-2022 | settimana | YouTube | Y_Summer_01 | Nullo | CA | Nullo | 9000 | 80 | Nullo |
| 01-01-2022 | settimana | Facebook | FB_Autunno_01 | Nullo | STATI UNITI | Nullo | 8000 | 100 | Nullo |
| 01-08-2022 | settimana | Facebook | FB_Autunno_02 | Nullo | STATI UNITI | Nullo | 1000 | 10 | Nullo |
| 01-08-2022 | settimana | Facebook | FB_Autunno_01 | Nullo | STATI UNITI | Nullo | 7000 | 100 | Nullo |
| 01-16-2022 | settimana | Facebook | FB_Estate_01 | Nullo | CA | Nullo | 10000 | 80 | Nullo |
| 12-27-2021 | settimana | Nullo | Nullo | Nullo | STATI UNITI | Moda | Nullo | Nullo | 200 |
| 01-03-2022 | settimana | Nullo | Nullo | Nullo | STATI UNITI | Moda | Nullo | Nullo | 10 |
| 01-03-2022 | settimana | Nullo | Nullo | Nullo | STATI UNITI | Gioielli | Nullo | Nullo | 1100 |
| 01-10-2022 | settimana | Nullo | Nullo | Nullo | CA | Gioielli | Nullo | Nullo | 80 |
| 01-01-2022 | settimana | CSE | Nullo | Nullo | Nullo | Nullo | 2 | Nullo | Nullo |
| 01-08-2022 | settimana | CSE | Nullo | Nullo | Nullo | Nullo | 2 | Nullo | Nullo |

{style="table-layout:auto"}


## Imposta dati armonizzati

Per creare un set di dati armonizzato, come nella sezione [esempio](#an-example-of-harmonized-data), è necessario seguire questi passaggi:

1. Definisci ulteriori [campi armonizzati](fields.md) che desideri utilizzare oltre i campi armonizzati globali già disponibili.
1. Configurazione [regole del set di dati](dataset-rules.md) per mappare i campi dai set di dati aggregati o evento esperienza ai campi armonizzati.
1. Definisci [punti di contatto di marketing](marketing-touchpoints.md) utilizzando i campi standard e armonizzati aggiuntivi definiti dall&#39;utente.
1. Definisci [conversioni](conversions.md) utilizzando i campi standard e armonizzati aggiuntivi definiti dall&#39;utente.


## Visualizza dati armonizzati

Per visualizzare i dati armonizzati, nell’interfaccia Mix Modeler:

1. Seleziona ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Harmonized Data]** dalla barra superiore. Viene mostrato un riassunto dei dati armonizzati in base ai campi, alle regole del set di dati, ai punti di contatto di marketing e alle conversioni definite.

   1. Per ridefinire il periodo su cui si basa la ricapitolazione dei dati armonizzati, immettere un intervallo di date per **[!UICONTROL Date range]** o utilizzare ![Calendario](../assets/icons/Calendar.svg) per selezionare un intervallo di dati.

   1. Per modificare le colonne dei campi armonizzati visualizzate per la tabella dati armonizzata, utilizzare ![Impostazioni](../assets/icons/Setting.svg) per aprire **[!UICONTROL Column settings]** .

      1. Seleziona ![SelectBox](../assets/icons/SelectBox.svg) una o più colonne da **[!UICONTROL AVAILABLE COLUMNS]** e utilizzare ![Freccia destra](../assets/icons/ChevronRight.svg) per aggiungere queste colonne a **[!UICONTROL SELECTED COLUMNS]**.

      1. Seleziona ![SelectBox](../assets/icons/SelectBox.svg) una o più colonne da **[!UICONTROL SELECTED COLUMNS]** e utilizzare ![Freccia sinistra](../assets/icons/ChevronLeft.svg) per rimuovere le colonne selezionate e restituirle a **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Seleziona una colonna da **[!UICONTROL DEFAULT SORT]** e passa da **[!UICONTROL Ascending]** o **[!UICONTROL Descending]**.

      1. Per modificare l’ordine delle colonne visualizzate, puoi spostare una colonna in **[!UICONTROL SELECTED COLUMNS]** su e giù tramite trascinamento.

   1. Seleziona **[!UICONTROL Submit]** per inviare le modifiche alle impostazioni di colonna. Seleziona **[!UICONTROL Close]** per annullare le modifiche apportate.

1. Se sono disponibili più pagine, utilizza ![Freccia sinistra](../assets/icons/ChevronLeft.svg) o ![Freccia a destra](../assets/icons/ChevronRight.svg) a **[!UICONTROL Page _x _di_x_]** per spostarsi tra le pagine.
