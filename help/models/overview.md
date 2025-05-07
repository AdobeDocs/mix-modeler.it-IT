---
title: Panoramica dei modelli
description: Scopri come generare e utilizzare i modelli in Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Panoramica dei modelli

La funzionalità dei modelli di Mix Modeler consente di configurare, addestrare e valutare modelli specifici per gli obiettivi aziendali. La formazione e il punteggio supportano l’apprendimento del trasferimento basato sull’intelligenza artificiale tra attribuzione multitouch e modellazione marketing mix.

I modelli si basano sui dati armonizzati creati come parte del flusso di lavoro dell’applicazione Mix Modeler.

Un modello in Mix Modeler è un modello di apprendimento automatico utilizzato per misurare e prevedere un risultato specifico basato sugli investimenti di un addetto marketing. I punti di contatto di marketing e i dati di riepilogo possono essere utilizzati come input. Mix Modeler consente di creare varianti di modelli basati su diversi set di variabili, dimensioni e risultati, come ricavi, unità vendute, lead.

Un modello richiede:

* Una conversione.
* Uno o più punti di contatto di marketing (canali) costituiti da dati a livello di riepilogo, dati dei punti di contatto di marketing (dati evento) o entrambi.
* Un intervallo di lookback configurabile.
* Una finestra di formazione configurabile.

Un modello può facoltativamente includere:

* Fattori esterni.
* Fattori interni.
* Conoscenza preventiva dei contributi di marketing da altre fonti, come la precedente esperienza delle parti interessate, test incrementali, altri modelli.
* La condivisione di spesa, che utilizza come proxy la condivisione di spesa relativa quando i dati di marketing sono sparsi.

La prima volta che viene creato un modello, la creazione avvia immediatamente il processo di formazione e punteggio. Dopo il completamento dell’esecuzione iniziale dell’addestramento e del punteggio, gli approfondimenti del modello sono disponibili per la revisione. Un modello può essere successivamente riaddestrato. Inoltre, i dati possono essere aggiunti al modello che richiede il ripristino manuale del modello. Il training e il re-scoring sono un processo iterativo, in quanto emergono nuovi risultati e informazioni e sono necessari adeguamenti per ottenere un adattamento del modello più appropriato per gli obiettivi aziendali.


## Creare modelli

Per creare un modello, utilizzare il flusso di configurazione guidato passo passo del modello di Mix Modeler disponibile quando si seleziona **[!UICONTROL Open model canvas]**. Per ulteriori dettagli, vedi [Modelli di compilazione](build.md).

## Gestisci modelli

Per visualizzare una tabella dei modelli correnti, nell’interfaccia di Mix Modeler:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Viene visualizzata una tabella dei modelli correnti.

   Le colonne della tabella specificano i dettagli relativi al modello.

   | Nome colonna | Dettagli |
   |---|---|
   | Nome | Nome del modello |
   | Descrizione | Descrizione del modello |
   | Evento di conversione | Conversione selezionata per il modello. |
   | Frequenza di esecuzione | Frequenza di esecuzione dell&#39;addestramento del modello. |
   | Ultima esecuzione | La data e l’ora dell’ultimo addestramento del modello. |
   | Stato | Stato del modello. |

   {style="table-layout:auto"}

   Lo stato segnalato del modello dipende dalla posizione in cui si trova un modello all&#39;interno del suo ciclo di vita. Ad esempio, se un modello viene creato, o riaddestrato con successo o meno, o ha ottenuto o ottenuto nuovamente un punteggio.

   Nella tabella seguente:

   * ![Segno di spunta](/help/assets/icons/Checkmark.svg): indica la corretta esecuzione di un passaggio del ciclo di vita del modello.
   * ![Orologio](/help/assets/icons/Clock.svg): indica un&#39;esecuzione corrente continua di un passaggio del ciclo di vita del modello.
   * ![Chiudi](/help/assets/icons/Close.svg) - indica una mancata esecuzione di un passaggio nel ciclo di vita del modello.

   | Stato | [Build](/help/models/build.md) | [Addestra](/help/models/train-score.md#train) | [Punteggio](/help/models/train-score.md#score) | [Riprova](/help/models/train-score.md#train) | [Riscore](/help/models/train-score.md#score) |
   |---|:---:|:---:|:---:|:---:|:---:|
   | In corso | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | | | | |
   | In corso | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Orologio](/help/assets/icons/Clock.svg) | | | |
   | In corso | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Orologio](/help/assets/icons/Clock.svg) | | |
   | In corso | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Orologio](/help/assets/icons/Clock.svg) | |
   | In corso | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Orologio](/help/assets/icons/Clock.svg) |
   | Addestramento non riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Chiudi](/help/assets/icons/Close.svg) | | | |
   | Addestramento non riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Chiudi](/help/assets/icons/Close.svg) | |
   | Formazione completata | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | | | |
   | Formazione completata | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | |
   | Punteggio non riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Chiudi](/help/assets/icons/Close.svg) | | |
   | Punteggio non riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Chiudi](/help/assets/icons/Close.svg) |
   | Punteggio riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | | |
   | Punteggio riuscito | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | ![Segno di spunta](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. Per modificare le colonne visualizzate per l&#39;elenco, selezionare ![Impostazioni colonna](/help/assets/icons/ColumnSetting.svg) e attivare o disattivare le colonne in ![Controlla](/help/assets/icons/Checkmark.svg).

È possibile eseguire le azioni seguenti su un modello specifico.

### Approfondimenti modello

La funzionalità Approfondimenti modello è disponibile solo su modelli con formazione e punteggi completati.

Per visualizzare le informazioni di un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Selezionate il nome del modello.

Sei stato reindirizzato a [Model Insights](insights.md).


### Visualizza dettagli

Per visualizzare ulteriori dettagli su un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona ![Info](/help/assets/icons/Info.svg) per un modello per visualizzare un popup con i dettagli.


### Duplica

Potete duplicare rapidamente un modello.

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Duplicate]**.

Sei stato reindirizzato ai passaggi per creare un nuovo modello, con un nome proposto composto dal nome del modello originale seguito da **[!UICONTROL (Copy)] (_n_)**.

### Modifica

Puoi modificare il nome, la descrizione e la pianificazione dell’apprendimento e del punteggio di un modello.

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Edit]**.

   Nella finestra di dialogo **[!UICONTROL Edit model]**:

   * Immettere un nuovo **[!UICONTROL Name]** e **[!UICONTROL Description]**.

   * Per abilitare la pianificazione, abilitare **[!UICONTROL Status]**. Puoi abilitare la pianificazione solo per i modelli che sono stati addestrati e valutati.

      1. Seleziona **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: selezionare un giorno della settimana e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: selezionare un giorno del mese dal menu a discesa Esegui su ogni e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).

      1. Selezionare **[!UICONTROL Training frequency]** dal menu a discesa: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

     ![Modifica modello](../assets/model-edit.png)

1. Seleziona **[!UICONTROL Save]**.



### Addestra

È consigliabile riqualificare un modello quando si desidera includere nuovi dati di marketing e di fattore incrementali. Per ulteriori informazioni, vedere [Modelli di addestramento e valutazione](train-score.md#train).


### Punteggio

Puoi assegnare un punteggio incrementale a un modello in base a nuovi dati di marketing o ripristinare un modello per un intervallo di date specifico. Per ulteriori informazioni, vedere [Modelli di addestramento e valutazione](train-score.md#score).


### Elimina modelli

Per eliminare un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.
1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Delete]**. In alternativa, selezionare ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dalla barra delle azioni blu.
1. Selezionare **[!UICONTROL Delete]** nella finestra di dialogo di conferma **[!UICONTROL Delete model]** per eliminare il modello. Selezionare **[!UICONTROL Cancel]** per annullare.

Per eliminare più modelli:

1. Seleziona più modelli.
1. Dalla barra blu delle azioni, seleziona ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** per eliminare i modelli.
1. Selezionare **[!UICONTROL Delete]** nella finestra di dialogo di conferma **[!UICONTROL Delete *x *modelli]**&#x200B;per eliminare i modelli. Selezionare **[!UICONTROL Cancel]**&#x200B;per annullare.

