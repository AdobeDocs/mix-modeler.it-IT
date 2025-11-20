---
title: Prestazioni da pianificare
description: Scopri come utilizzare le Prestazioni per pianificare una panoramica in Mix Modeler.
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
source-git-commit: 89def3d6f5a1415d8f7a91b05d68d70ca881bdf4
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Prestazioni da pianificare

>[!NOTE]
>
>La scheda **[!UICONTROL Performance to plan]** [!BADGE Beta]{type=Informative} in Mix Modeler ![Home](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** è una funzionalità beta e la relativa funzionalità è soggetta a modifiche. Questa funzione è disponibile per un numero limitato di clienti.

La scheda **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} in Mix Modeler ![Home](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** fornisce un dashboard di tracciamento per monitorare le prestazioni di marketing rispetto al piano. Puoi monitorare le prestazioni effettive rispetto a quelle pianificate tramite schede di stato e visualizzazioni.

La dashboard consente di identificare lacune, individuare rischi o opportunità e apportare modifiche tempestive ai piani e ai budget.

Per selezionare i dati visualizzati per le schede di stato e le visualizzazioni dei KPI:

* Selezionare un piano dal menu a discesa **[!UICONTROL Plan name]** utilizzando **[!UICONTROL _Selezionare un&#39;opzione..._]**.

* Specifica un periodo di data. Per modificare il periodo di data, immettere manualmente una data di inizio e una data di fine oppure selezionare un periodo di data, utilizzando ![Calendario](/help/assets/icons/Calendar.svg).

La scheda **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} mostra:

* [Schede di stato KPI](#kpi-status-cards):

   * [Budget](#budget)
   * [Ricavi](#revenue)
   * [ROI](#roi)
   * [KPI](#kpi)

* [Visualizzazione](#visualizations):
   * [*Metrica*](#metric-actual-vs-planned)
   * [*Metrica*](#metric-actual-vs-planned-by-granularity)
   * [Canale ](#channel-metric-by-granularity)
   * [*Metrica*](#metric-vs-metric-by-channel)
   * [*Metrica*](#metric-by-granularity)
   * [*Metrica*](#metric-by-channel)

## Schede di stato KPI

![Schede di stato KPI](../assets/performance-to-plan-kpi-cards.png)


### Budget

Visualizzazione circolare dell’avanzamento che mostra il confronto tra le spese di marketing e il budget del piano per il periodo di data.

### Ricavi

Una visualizzazione circolare dell’avanzamento che mostra il confronto tra i ricavi effettivi e i ricavi target pianificati per il periodo di data.


### ROI

Visualizzazione a linee che visualizza il ROI per il periodo di data.


### KPI

Visualizzazione a linee che visualizza l’indicatore KPI per il periodo della data.

Per selezionare un altro indicatore KPI:

1. Seleziona ![Modifica](/help/assets/icons/Edit.svg).
1. Nella finestra di dialogo **[!UICONTROL KPI status card]**, selezionare un indicatore KPI dal menu a discesa **[!UICONTROL KPI]**. Opzioni disponibili: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI] e [!UICONTROL Spend].


## Visualizzare

Sono disponibili sei visualizzazioni e puoi modificare ciascuna delle sei.

Per ridimensionare una visualizzazione, utilizzare l&#39;handle ┛ nell&#39;angolo inferiore destro. Per spostare una visualizzazione, trascinala e rilasciala nella posizione desiderata.

Puoi passare il cursore del mouse su qualsiasi linea, barra o elemento a dispersione in una visualizzazione per visualizzare una finestra a comparsa con informazioni aggiuntive.

![Visualizzazione](../assets/performance-to-plan-visualizations.png)

### *Metrica*: Effettivo rispetto a pianificato

Visualizzazione a barre in pila che confronta i valori della metrica selezionata per progressivo, progressivo pianificato e totale.


### *Metrica*: Effettivo rispetto a pianificato da *granularità*

Visualizzazione a linee che mostra i valori effettivi e pianificati per la metrica selezionata e la granularità selezionata.


### Canale *metrica* per *granularità*

Visualizzazione a barre sovrapposte che mostra le barre sovrapposte che visualizzano i canali per la metrica selezionata e la granularità selezionata.


### *Metrica* rispetto a *Metrica* per canale

Visualizzazione a dispersione che mostra un grafico a dispersione per i canali nelle metriche selezionate.


### *Metrica* per *granularità*

Visualizzazione a barre che mostra i valori effettivi e pianificati per la metrica selezionata.


### *Metrica* per canale

Visualizzazione su più righe che mostra la metrica selezionata sulla granularità selezionata.


### Modificare una visualizzazione

Per modificare una visualizzazione:

1. Seleziona ![Modifica](/help/assets/icons/Edit.svg) per aprire la finestra di dialogo **[!UICONTROL Edit data]**.
1. A seconda della visualizzazione, puoi modificare:

   * Una o due metriche: selezionare una metrica dal menu a discesa **[!UICONTROL Select metric]**.

      * Per i piani basati sul ROI, le opzioni sono: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI], [!UICONTROL Spend] e [!UICONTROL Volume].
      * Per i piani basati su CPA, le opzioni sono: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Spend] e [!UICONTROL Volume].
   * **[!UICONTROL Granularity]**: selezionare **[!UICONTROL date ranges]** o **[!UICONTROL week]** dal menu a discesa **[!UICONTROL Granularity]**.

   In **[!UICONTROL Preview]** vengono visualizzate le differenze tra le modifiche e la visualizzazione **[!UICONTROL Current]**.

1. Selezionare **[!UICONTROL Apply]** per applicare le modifiche. Seleziona **[!UICONTROL Cancel]** per annullare eventuali modifiche alla visualizzazione.
