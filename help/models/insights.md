---
title: Approfondimenti modello
description: Scopri come ottenere dettagli sul modello, ad esempio panoramica storica, informazioni sul modello e qualità del modello in Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Approfondimenti modello

Per visualizzare le informazioni sul modello, nell&#39;interfaccia ![Models](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** in Mix Modeler:

1. Dalla tabella **[!UICONTROL Models]**, selezionare il nome di un modello con **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]**.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**.

![Barra della scheda Informazioni modello](/help/assets//model-insights-tabbar.png)

Puoi vedere quando il modello specificato viene aggiornato l&#39;ultima volta e i widget vengono visualizzati utilizzando quattro schede: [Informazioni sul modello](#model-insights), [Attribuzione](#attribution), [Diagnostica](#diagnostics) e [Panoramica cronologica](#historical-overview).

È possibile modificare il periodo di data su cui si basano i widget di ciascuna scheda. Immettere un periodo di data o selezionare ![Calendario](/help/assets//icons/Calendar.svg) per selezionare un periodo di data.

## [!UICONTROL Model insights]

La scheda Approfondimenti modello mostra i widget per:

* Contributo per data e media di base. Il grafico ad aree o barre sovrapposte è ordinato: Base in basso, Canali non spesi in mezzo e Canali spesi in alto.

* Contributo per canale.

* Riepilogo prestazioni marketing.

* Curve di risposta marginale.
  <br/>Selezionare un canale dall&#39;elenco a discesa **[!UICONTROL Channel]** per aggiornare il widget per un canale specifico.

![Modello - Approfondimenti modello](/help/assets//model-insights-insights.png)

Puoi passare il cursore sopra i singoli elementi del grafico in ciascun widget per visualizzare un elemento a comparsa con ulteriori dettagli.

Per scaricare un file CSV contenente i dati per il widget, seleziona ![Scarica](/help/assets//icons/Download.svg).

Per scaricare i dati completi di Approfondimenti modello in formato Microsoft® Excel, seleziona ![Scarica](/help/assets//icons/Download.svg) **[!UICONTROL Download data]**.

## [!UICONTROL Attribution]

Utilizzando la scheda [!UICONTROL Attribution], puoi comprendere l’efficacia dei punti di contatto e delle campagne di marketing con dati a livello di evento. Sono supportati i seguenti modelli di attribuzione:

* In base al modello selezionato in Mix Modeler:
   * Algoritmica - Influenzato
   * Algoritmica - Incrementale
* Basato su regole:
   * Unità di decadimento
   * Primo contatto
   * Ultimo contatto
   * Lineare
   * Ushape

Consulta [Attribuzione multi-touch](../get-started/about.md#multi-touch-attribution) per un&#39;introduzione alla funzionalità di attribuzione multi-touch in Mix Modeler.

Selezionare uno o più modelli di attribuzione dall&#39;elenco a discesa **[!UICONTROL Attribution Model]**. I modelli di attribuzione selezionati si applicano a tutti i widget nella scheda Attribuzione.

![Attribuzione](/help/assets//model-insights-attribution.png)

I punteggi dell’evento granulare di attribuzione multi-touch di Mix Modeler sono allineati ai punteggi e ai ROI complessivi di Mix Modeler. Questi punteggi sono resi disponibili anche come set di dati in Experience Platform.

La scheda Attribuzione è costituita dai widget seguenti:

### [!UICONTROL Overview]

Il widget [!UICONTROL Overview] mostra, per i modelli di attribuzione selezionati, i totali e le percentuali di conversione. Selezionando più modelli si aggiungono ulteriori cerchi alla visualizzazione, ciascuno con il proprio colore corrispondente alla legenda.

Per visualizzare un pop-up con i dettagli di un modello di attribuzione, passa il cursore del mouse su uno dei cerchi nella visualizzazione.

### [!UICONTROL Trends]

Il widget [!UICONTROL Daily trends], [!UICONTROL Weekly trends] o [!UICONTROL Monthly trends] mostra le tendenze di conversione giornaliere, settimanali o mensili per i modelli di attribuzione selezionati.

Per scegliere il periodo, selezionare **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** o **[!UICONTROL Monthly trends]** da ![Altro](/help/assets//icons/More.svg).

Per visualizzare i dettagli, passa il cursore del mouse sulla riga di dati di un modello di attribuzione specifico per visualizzare un elemento a comparsa che mostra il numero totale di conversioni per tali dati.

### [!UICONTROL Breakdown]

Il widget [!UICONTROL Breakdown] è una suddivisione per canale o punto di contatto delle conversioni per ciascuno dei modelli di attribuzione selezionati. Questo widget può essere utile per prendere decisioni sull’efficacia di ciascun canale o punto di contatto.

Per scegliere il tipo di suddivisione, selezionare **[!UICONTROL Breakdown by channel]** o **[!UICONTROL Breakdown by touchpoint]** da ![Altro](/help/assets//icons/More.svg).

Per visualizzare i dettagli, passa il cursore sopra uno degli elementi del grafico.

### [!UICONTROL Top campaigns]

Il widget Campagne principali mostra una tabella delle campagne principali con colonne per Nome campagna, Canale, Tipo di media e Conversioni incrementali. Questo widget può aiutare a informare il team dell’efficacia di una campagna specifica per un dato canale e fornire informazioni sulle campagne in cui investire ulteriormente.

↑ Per ordinare la tabella in ordine crescente o decrescente ↓ per le conversioni Canale, Tipo di file multimediale o Incrementale, seleziona l’intestazione della colonna e attiva/disattiva l’ordinamento.

Per espandere la tabella in una finestra di dialogo separata, selezionare **[!UICONTROL Expand]** da ![Altro](/help/assets//icons/More.svg).

La finestra di dialogo espansa Prime campagne mostra la stessa tabella con colonne aggiuntive per

* Conversioni incrementali
* Conversioni influenzate
* Conversioni al primo contatto
* Conversioni ultimo contatto

  Puoi selezionare ciascuna delle intestazioni di colonna aggiuntive per ordinare la tabella in ordine crescente o decrescente.

Per chiudere la finestra di dialogo Inizio campagne espansa, selezionare **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

La visualizzazione [!UICONTROL Breakdown by touchpoint position] è una suddivisione delle conversioni attribuite per posizione del punto di contatto e punto di contatto in tutti i percorsi di conversione. Questo grafico consente di confrontare se un punto di contatto contribuisce meglio in una posizione rispetto alle posizioni rimanenti e ad altri punti di contatto in qualsiasi posizione.

>[!NOTE]
>
>La somma del contributo in percentuale per un modello di attribuzione in tutti i punti di contatto e le posizioni deve essere pari a 100.


Le posizioni [!UICONTROL Starter], [!UICONTROL Player] e [!UICONTROL Closer] sono definite come segue:

| Posizione | Descrizione |
|---|---|
| [!UICONTROL Starter] | Questa posizione indica se il punto di contatto è il primo contatto in un percorso di conversione. |
| [!UICONTROL Player] | Questa posizione indica se il punto di contatto non è il primo o l’ultimo contatto che porta alla conversione. |
| [!UICONTROL Closer] | Questa posizione indica se il punto di contatto è l’ultimo contatto prima della conversione. |


### [!UICONTROL Top conversion paths]

La visualizzazione [!UICONTROL Top conversion paths] mostra i primi 5 percorsi di conversione in base ai modelli di attribuzione selezionati.

Per ogni percorso di conversione, vedi:

* il numero di canali che hanno un impatto,
* il totale dei percorsi attribuiti,
* la percentuale di percorsi attribuiti per questo percorso di conversione rispetto al totale dei percorsi attribuiti,
* per ogni canale, la percentuale di contributo del modello di attribuzione e
* la somma di queste percentuali di contributo del modello di attribuzione del canale.


## [!UICONTROL Diagnostics]

La scheda Diagnostica mostra i widget per:

* Visualizzazione [!UICONTROL Model Assessment], che è possibile suddividere in Conversioni effettive rispetto a quelle previste o residue.

  Per suddividere la visualizzazione, selezionare **[!UICONTROL Actual vs. Predicted]** o **[!UICONTROL Residuals]** dall&#39;elenco **[!UICONTROL Breakdown]**.

* Tabella [!UICONTROL Model fitting metrics], che mostra le seguenti colonne per ogni metrica di conversione:

   * Conversione effettiva

   * Conversione modellata

   * Conversione residua (differenza tra conversione effettiva e modellata)

   * Valori punteggio qualità modello:

      * R2 (R al quadrato), che indica se i dati si adattano al modello di regressione (bontà di adattamento).

      * MAPE (errore percentuale assoluto medio), uno dei KPI più comunemente utilizzati per misurare la precisione della previsione ed esprime l&#39;errore di previsione come percentuale del valore effettivo.

      * RMSE (Root Mean Square Error): indica l’errore medio, ponderato in base al quadrato dell’errore.

  Per scaricare un file CSV contenente i dati per la tabella, seleziona ![Scarica](/help/assets//icons/Download.svg).

* Tabella [!UICONTROL Touchpoint effectiveness], che rappresenta il risultato del modello algoritmico Attribution AI. I dati per questa tabella vengono generati solo per periodi di tempo specifici. Seleziona **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets//icons/InfoOutline.svg) per ulteriori dettagli.

  La visualizzazione mostra, in ordine decrescente di [!UICONTROL Efficiency measure] ![Ordine decrescente](/help/assets//icons/SortOrderDown.svg), per ogni punto di contatto:

   * [!UICONTROL Paths touched]: visualizza la percentuale di percorsi che raggiungono la conversione e la percentuale di percorsi che non raggiungono la conversione. Per un punto di contatto, puoi vedere più conversioni attribuite quando il rapporto di conversione dell’attribuzione è elevato. Questo rapporto confronta la percentuale di percorsi che portano alla conversione rispetto alla percentuale di percorsi che portano alla conversione *not*.
   * [!UICONTROL Efficiency measure]: generato dal modello di attribuzione algoritmica, la misura di efficienza indica l&#39;importanza relativa di un punto di contatto verso la conversione, indipendentemente dal volume del punto di contatto. L&#39;efficienza è misurata su una scala da 1 a 5. Tieni presente che un volume di punti di contatto più elevato non garantisce una misura di efficienza più elevata.
   * [!UICONTROL Total volume]: numero aggregato di volte in cui un utente tocca un punto di contatto. Il numero include i punti di contatto visualizzati in un percorso che raggiunge la conversione e i percorsi *non* che determinano la conversione.

![Diagnostica](/help/assets//model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

La scheda Cronologia mostra i widget per:

* Conversione e spesa per trimestre fiscale e prodotto.

* Spesa per canale.

* Spesa punto di contatto.

  Puoi selezionare un canale alternativo basato sulla spesa da visualizzare per questo widget. Selezionare un canale da **[!UICONTROL Channels]**.

* Volume del punto di contatto.

  Puoi selezionare un canale alternativo basato su volume da visualizzare per questo widget. Selezionare un canale da **[!UICONTROL Channels]**.

![Modello - Panoramica cronologica](/help/assets//model-insights-historical-overview.png)
