---
title: Approfondimenti modello
description: Scopri come ottenere dettagli sul modello, come panoramica storica, informazioni sul modello e qualità del modello in Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: e5fa52cee1725ddfe4d75c50857a1e5ef4daf5b2
workflow-type: tm+mt
source-wordcount: '2255'
ht-degree: 0%

---

# Approfondimenti modello

Ogni visualizzazione nelle informazioni sul modello è progettata per aiutarti a:

* Visualizza e quantifica l’impatto delle attività di marketing della tua organizzazione.
* Identifica i canali con prestazioni elevate.
* Identifica i canali che potrebbero necessitare di ottimizzazione.

Queste informazioni aiutano a supportare la definizione delle priorità e l’allocazione delle risorse.

Per visualizzare le informazioni sul modello, nell&#39;interfaccia ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** in Mix Modeler:

1. Dalla tabella **[!UICONTROL Models]**, selezionare il nome di un modello con **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]**.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**.



Sono disponibili le seguenti schede:

* [Approfondimenti modello](#model-insights)
* [Fattori](#factors-beta) [!BADGE beta]
* [Attribuzione](#attribution) (solo per modelli abilitati per MTA)
* [Diagnostica](#diagnostics)
* [Panoramica cronologica](#historical-overview).

Puoi modificare il periodo di data su cui si basano le visualizzazioni in ciascuna scheda. Immettere un periodo di data o selezionare ![Calendario](/help/assets/icons/Calendar.svg) per selezionare un periodo di data.

## Deriva modello

{{release-limited-testing-section}}

Se nel modello viene rilevata una deriva del modello, viene visualizzata una finestra di dialogo **[!UICONTROL Model drift detected]** con opzioni da ricordare in seguito o per [**[!UICONTROL Retrain]**](overview.md#retrain) immediatamente il modello. Se selezioni **[!UICONTROL Remind me later]**, riceverai un promemoria il giorno successivo o all&#39;accesso successivo.

![Finestra di dialogo rilevata deviazione modello](/help/assets/model-drift-dialog.png)

## [!UICONTROL Model insights]

La scheda Approfondimenti modello mostra le visualizzazioni per [Contributo per data e supporto di base](#contribution-by-date-and-base-media), [Contributo per canale](#contribution-by-channel), [Riepilogo prestazioni marketing](#marketing-performance-summary) e [Curve di risposta marginali](#marginal-response-curves). La scheda fornisce anche una tabella con [raggruppamento punto di contatto](#touchppint-breakdown).

![Modello - Approfondimenti modello](/help/assets/model-insights-insights.png)

* Puoi passare il cursore sopra i singoli elementi del grafico in ogni visualizzazione per visualizzare un elemento a comparsa con ulteriori dettagli.

* Per scaricare un file CSV contenente i dati per la visualizzazione, seleziona ![Scarica](/help/assets/icons/Download.svg).

* Per scaricare i dati completi di Approfondimenti modello in formato Microsoft® Excel, seleziona ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contributo per data e media di base.

Questa visualizzazione con grafico in pila è ordinata come segue:

* La base viene visualizzata nella parte inferiore.
* I canali non spesi vengono visualizzati al centro.
* I canali di spesa sono visualizzati in alto.

Questa visualizzazione rappresenta la proporzione di contributo ottenuta per base, per canali di spesa e per canali non di spesa in un intervallo di date. Questa visualizzazione è utile per mostrare l’incrementalità. La base rappresenta ciò che sarebbe successo senza alcun marketing e i canali non spesi più i canali spesi (oltre alla base) attribuiscono all’impatto del marketing. In breve, il valore non speso più spesa equivale all’impatto incrementale delle attività di marketing e la visualizzazione fornisce ad insight informazioni semplici sul valore generato dal marketing.

### Contributo per canale

Una visualizzazione ad anello che mostra una distribuzione del contributo tra vari canali. Questa visualizzazione mostra l’incrementalità attraverso l’obiettivo dei primi tre canali con prestazioni (escluse le categorie base e *Tutte le altre*). La visualizzazione consente di supportare la definizione delle priorità e l’allocazione del budget.

### Riepilogo prestazioni marketing.

Visualizzazione con grafico a barre orizzontale che visualizza le prestazioni del ROI o CPA per ciascun canale. Questa visualizzazione evidenzia il ROI/CPA dei tuoi investimenti di marketing. I canali sono ordinati in ordine decrescente in base al ROI/CPA. La visualizzazione consente di identificare quali canali sono più efficaci e quali potrebbero necessitare di ottimizzazione.

### Curve di risposta marginale.

Il grafico a linee visualizza e confronta i rendimenti marginali generati dall’investimento nei canali di marketing.  Identifica inoltre il punto di pareggio in cui il ritorno incrementale è inferiore alla spesa incrementale. Di conseguenza, questa visualizzazione ti aiuta a capire quando l’investimento marketing inizia a diventare meno incisivo.

La curva, il punto di pareggio e i valori corrispondenti vengono calcolati in base all’intervallo di dati selezionato e al canale selezionato.

Per cambiare il canale:

* Selezionare un canale dal menu a discesa **[!UICONTROL Channel]** per aggiornare la visualizzazione per un canale specifico.


### Suddivisione punto di contatto

La tabella di suddivisione dei punti di contatto mostra i raggruppamenti settimanali dei punti di contatto per tutti i canali o per alcuni di essi, su base settimanale, visualizzando le metriche chiave associate a ciascuno di essi. La tabella consente un confronto semplice, l’identificazione delle tendenze e il tracciamento delle prestazioni a un livello di canale più granulare. Questa tabella integra esplicitamente la visualizzazione [Contributo per data e supporto di base](#contribution-by-date-and-base-media) e la visualizzazione [Contributo per canale](#contribution-by-channel).

![Suddivisione punto di contatto](../assets/touchpoint-breakdown.png)

Sono disponibili le seguenti colonne:

| Colonna | Descrizione |
|---|---|
| **[!UICONTROL Date range]** | La settimana in cui generare il rapporto. |
| **[!UICONTROL Touchpoint]** | Canale del punto di contatto specifico. |
| **[!UICONTROL ROI]** | Percentuale di (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | I ricavi per l’intervallo di date. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | Le conversioni per l’intervallo di date. |
| **[!UICONTROL Spend]** | Spesa per l’intervallo di dati. |

Per selezionare un canale specifico o tutti i canali, selezionare dal menu a discesa **[!UICONTROL View]**.

Per scaricare il contenuto della tabella dei raggruppamenti dei punti di contatto, seleziona ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.

## **[!UICONTROL Factors]** [!BADGE beta]

La scheda Fattori [!BADGE beta] mostra informazioni relative ai fattori esterni.

![Fattori](/help/assets/factors.png)

Questa visualizzazione ti aiuta a comprendere l’effetto incrementale che vari fattori interni ed esterni hanno sulla linea di base delle conversioni. Ad esempio, condizioni economiche o attività promozionali.

Utilizza il menu a discesa **[!UICONTROL Factors]** per selezionare i fattori da visualizzare.

<!-- need to update the image when we do have a proper example -->

Per scaricare un file CSV contenente i dati per la tabella, seleziona ![Scarica](/help/assets/icons/Download.svg).

Se non sono disponibili dati, viene visualizzato un messaggio ![TabellaEGrafico](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
>La scheda Attribuzione è disponibile solo per i modelli abilitati per MTA.


Utilizzando la scheda [!UICONTROL Attribution], puoi comprendere l’efficacia dei punti di contatto e delle campagne di marketing con dati a livello di evento.  Vedi [Genera modello](build.md).

Sono supportati i seguenti modelli di attribuzione:

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

Selezionare uno o più modelli di attribuzione dal menu a discesa **[!UICONTROL Attribution Model]**. I modelli di attribuzione selezionati si applicano a tutte le visualizzazioni nella scheda Attribuzione.

![Attribuzione](/help/assets/model-insights-attribution.png)

I punteggi dell’evento granulare di attribuzione multi-touch di Mix Modeler sono allineati ai punteggi e al ROI complessivi di Mix Modeler. Questi punteggi sono resi disponibili anche come set di dati in Experience Platform.

La scheda Attribuzione è costituita dalle seguenti visualizzazioni:

### [!UICONTROL Overview]

La visualizzazione [!UICONTROL Overview] mostra, per i modelli di attribuzione selezionati, i totali e le percentuali di conversione. Selezionando più modelli si aggiungono ulteriori cerchi alla visualizzazione, ciascuno con il proprio colore corrispondente alla legenda.

Per visualizzare un pop-up con i dettagli di un modello di attribuzione, passa il cursore del mouse su uno dei cerchi nella visualizzazione.

### [!UICONTROL Trends]

La visualizzazione [!UICONTROL Daily trends], [!UICONTROL Weekly trends] o [!UICONTROL Monthly trends] mostra le tendenze di conversione giornaliere, settimanali o mensili per i modelli di attribuzione selezionati.

Per scegliere il periodo, selezionare **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** o **[!UICONTROL Monthly trends]** da ![Altro](/help/assets/icons/More.svg).

Per visualizzare i dettagli, passa il cursore del mouse sulla riga di dati di un modello di attribuzione specifico per visualizzare un elemento a comparsa che mostra il numero totale di conversioni per tali dati.

### [!UICONTROL Breakdown]

La visualizzazione [!UICONTROL Breakdown] è una suddivisione per canale o punto di contatto delle conversioni per ciascuno dei modelli di attribuzione selezionati. Questa visualizzazione può essere utile per prendere decisioni sull’efficacia di ciascun canale o punto di contatto.

Per scegliere il tipo di suddivisione, selezionare **[!UICONTROL Breakdown by channel]** o **[!UICONTROL Breakdown by touchpoint]** da ![Altro](/help/assets/icons/More.svg).

Per visualizzare i dettagli, passa il cursore sopra uno degli elementi del grafico.

### [!UICONTROL Top campaigns]

La visualizzazione Campagne principali mostra una tabella delle campagne principali con colonne per Nome campagna, Canale, Tipo di media e Conversioni incrementali. Questa visualizzazione può aiutare a informare il team dell’efficacia di una campagna specifica per un dato canale e fornire informazioni sulle campagne in cui investire ulteriormente.

↑ Per ordinare la tabella in ordine crescente o decrescente ↓ per le conversioni Canale, Tipo di file multimediale o Incrementale, seleziona l’intestazione della colonna e attiva/disattiva l’ordinamento.

Per espandere la tabella in una finestra di dialogo separata, selezionare **[!UICONTROL Expand]** da ![Altro](/help/assets/icons/More.svg).

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

La scheda Diagnostica mostra le visualizzazioni per:

* **[!UICONTROL Model Assessment]** visualizzazioni, costituite da:

  ![Valutazione modello](../assets/model-assessment.png)

   * Un grafico che puoi scomporre per conversioni effettive rispetto a quelle previste o residue.
Per suddividere la visualizzazione, selezionare una delle opzioni seguenti dall&#39;elenco **[!UICONTROL Breakdown]**.

      * **[!UICONTROL Actual vs Predicted]**: questa opzione confronta i valori reali con le previsioni del modello. Idealmente, i valori previsti dovrebbero allinearsi strettamente con i valori effettivi, anche se ci si aspetta una certa deviazione. Deviazioni o pattern ampi o sistematici possono indicare relazioni e dati mancanti o potenziali distorsioni.

      * **[!UICONTROL Residuals]**: questa opzione mostra la differenza tra i valori effettivi e quelli previsti. Un modello dalle prestazioni soddisfacenti presenta residui distribuiti in modo casuale, senza pattern chiari o diffusione crescente. Le tendenze strutturate o l&#39;ampliamento dei residui possono segnalare l&#39;assenza di relazioni e dati o problemi di varianza.

   * Una tabella che mostra le seguenti colonne per ogni metrica di conversione:

      * **[!UICONTROL Actual Conversion]**
      * **[!UICONTROL Predicted Conversion]**
      * **[!UICONTROL Residual Conversion]**
      * **[!UICONTROL R<sup>2</sup>]**, un punteggio che indica se i dati si adattano al modello di regressione (bontà di adattamento).
      * **[!UICONTROL MAPE]** (errore percentuale assoluto medio), uno dei KPI più comunemente utilizzati per misurare la precisione della previsione ed esprime l&#39;errore di previsione come percentuale del valore effettivo.
      * **[!UICONTROL RMSE]** (errore quadrato medio radice): indica l&#39;errore medio, ponderato in base al quadrato dell&#39;errore.

  Per scaricare un file CSV contenente i dati per la tabella, seleziona ![Scarica](/help/assets/icons/Download.svg).

* Tabella **[!UICONTROL Model training fit metrics]**, che visualizza per ogni metrica di conversione:

  ![Tabella delle metriche Adattamento al modello](../assets/model-training-fit-metrics.png)

   * **[!UICONTROL Training R<sup>2</sup>]**: indica la proporzione di varianza nei valori effettivi spiegata dalle previsioni del modello, compresa tra 0 e 1.
   * **[!UICONTROL Training sMAPE]** (errore percentuale assoluto medio simmetrico): misura l’errore percentuale medio nei dati di apprendimento. Valori più bassi indicano una maggiore precisione.
   * **[!UICONTROL Training RMSE]** (errore radice quadrata media): misura l’errore percentuale medio nei dati di apprendimento. Penalizza gli errori più grandi rispetto a MAPE. Una RMSE più bassa suggerisce una maggiore precisione predittiva, ma è sensibile ai valori anomali.
   * **[!UICONTROL Out-of-sample sMAPE]**: valuta la percentuale di errore sui dati non visualizzati, bilanciando le previsioni eccessive e insufficienti. Aiuta a valutare la generalizzazione. Attualmente, Mix Modeler valuta la percentuale di errore utilizzando l’ultimo trimestre dei dati di formazione come set di dati di sospensione.
   * **[!UICONTROL Out-of-sample RMSE]**: valuta la percentuale di errore sui dati non visualizzati, bilanciando le previsioni eccessive e insufficienti. Aiuta a valutare la generalizzazione. Attualmente, Mix Modeler valuta la percentuale di errore utilizzando l’ultimo trimestre dei dati di formazione come set di dati di sospensione. RMSE penalizza gli errori più grandi rispetto a MAPE.


* Tabella **[!UICONTROL Touchpoint effectiveness]**, che rappresenta il risultato del modello algoritmico di IA per l’attribuzione.

  ![Tabella dell&#39;efficacia dei punti di contatto](../assets/touchpoint-effectiveness.png)

  I dati per questa tabella vengono generati solo per periodi di tempo specifici. Seleziona **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) per ulteriori dettagli.

  La visualizzazione mostra, in ordine decrescente di [!UICONTROL Efficiency measure] ![Ordine decrescente](/help/assets/icons/SortOrderDown.svg), per ogni punto di contatto:

   * **[!UICONTROL Paths touched]**: visualizza la percentuale di percorsi che raggiungono la conversione e la percentuale di percorsi che non raggiungono la conversione. Per un punto di contatto, puoi vedere più conversioni attribuite quando il rapporto di conversione dell’attribuzione è elevato. Questo rapporto confronta la percentuale di percorsi che portano alla conversione rispetto alla percentuale di percorsi che portano alla conversione *not*.
   * **[!UICONTROL Efficiency measure]**: generato dal modello di attribuzione algoritmica, la misura di efficienza indica l&#39;importanza relativa di un punto di contatto verso la conversione, indipendentemente dal volume del punto di contatto. L&#39;efficienza è misurata su una scala da 1 a 5. Tieni presente che un volume di punti di contatto più elevato non garantisce una misura di efficienza più elevata.
   * **[!UICONTROL Total volume]**: numero aggregato di volte in cui un utente tocca un punto di contatto. Il numero include i punti di contatto visualizzati in un percorso che raggiunge la conversione e i percorsi *non* che determinano la conversione.


### Rilevamento della deriva del modello

>[!AVAILABILITY]
>
>La funzionalità descritta in questa sezione si trova nella fase di test limitato del rilascio e potrebbe non essere ancora disponibile nell’ambiente. Questa nota verrà rimossa quando la funzionalità sarà generalmente disponibile. Per informazioni sulla procedura di rilascio di Mix Modeler, vedere [Versioni delle funzionalità di Mix Modeler](/help/releases/latest.md).
>

Se viene rilevata una deriva del modello, viene visualizzata una notifica **[!UICONTROL Model drift detected]** nella parte superiore.

![Notifica di deviazione modello](/help/assets/model-drift-notification.png)

Selezionare **[!UICONTROL Hide]** per nascondere la notifica. La notifica riapparirà il giorno successivo o al successivo accesso.


## [!UICONTROL Historical overview]

La scheda Cronologia mostra le visualizzazioni per:

![Modello - Panoramica cronologica](/help/assets/model-insights-historical-overview.png)


### Conversione e spesa per trimestre fiscale e prodotto

Questa visualizzazione rappresenta la conversione e la distribuzione della spesa tra vari trimestri all’interno dell’intervallo di date specificato. La visualizzazione consente di identificare i trimestri con prestazioni elevate in cui la spesa sta guidando le conversioni.


### Spesa per canale

Questa visualizzazione rappresenta la distribuzione della spesa tra vari canali all’interno dell’intervallo di date specificato. La visualizzazione consente di identificare rapidamente quali canali ricevono più spese.


### Spesa punto di contatto

Questa visualizzazione rappresenta la distribuzione della spesa tra punti di contatto pagati per ogni trimestre all’interno dell’intervallo di date specificato. La visualizzazione consente di comprendere quali punti di contatto sono prioritari all’interno di canali e trimestri specifici. La visualizzazione consente di identificare i modelli e le tendenze di spesa dei canali, in particolare quelli con spesa bassa e non frequente nel tempo.

Per selezionare un canale alternativo basato sulla spesa da visualizzare per questa visualizzazione:

* Selezionare un canale da **[!UICONTROL Channels]**.


### Volume punto di contatto

Questa visualizzazione rappresenta la distribuzione del volume in tutti i punti di contatto per ogni trimestre all’interno dell’intervallo di date specificato.

Per selezionare un canale alternativo basato sul volume da visualizzare per questa visualizzazione:

* Selezionare un canale da **[!UICONTROL Channels]**.


## **[!UICONTROL Edit]**

Puoi modificare il nome, la descrizione e la pianificazione dell’apprendimento e del punteggio del modello.

1. Seleziona ![Modifica](/help/assets/icons/Edit.svg) Modifica

1. Nella finestra di dialogo **[!UICONTROL Edit model]**:

   * Immettere un nuovo **[!UICONTROL Name]** e **[!UICONTROL Description]**.

   * Per abilitare la pianificazione, abilitare **[!UICONTROL Status]**. Puoi abilitare la pianificazione solo per i modelli che sono stati addestrati e valutati.

      1. Seleziona **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: selezionare un giorno della settimana e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: selezionare un giorno del mese dal menu a discesa Esegui su ogni e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).

      1. Selezionare **[!UICONTROL Training frequency]** dal menu a discesa: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

     ![Modifica modello](../assets/model-edit.png)

1. Seleziona **[!UICONTROL Save]**.
