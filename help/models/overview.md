---
title: Modelli
description: Scopri come configurare e utilizzare i modelli in Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 935b179e31d1b677a8c83b1566c02b7aaa617e8d
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Modelli

La funzionalità dei modelli in Mix Modeler consente di configurare, addestrare e valutare modelli specifici per gli obiettivi aziendali. La formazione e il punteggio supportano l’apprendimento del trasferimento basato sull’intelligenza artificiale tra attribuzione multitouch e modellazione marketing mix.

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


## Creare un modello

Per creare un modello, utilizzare il flusso di configurazione guidato del modello Mix Modeler passo dopo passo disponibile quando si seleziona **[!UICONTROL Open model canvas]**. Per ulteriori dettagli, vedere [Creare un modello](create.md).

## Gestisci modelli

Per visualizzare una tabella dei modelli correnti, nell’interfaccia Mix Modeler:

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
   | Stato | Lo stato dell’ultima esecuzione dell’addestramento del modello. <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) riuscito<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) problema di formazione<br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) In attesa del corso di formazione <br/>![StatusRed](/help/assets/icons/StatusRed.svg) Non riuscito <br/>![StatusGreen](/help/assets/icons/StatusGray.svg) _ (quando è in corso l&#39;ultima esecuzione) |

   {style="table-layout:auto"}

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



### Riaddestramento


La riformazione di un modello è disponibile solo su modelli con formazione corretta.

Considera di riaddestrare un modello quando desideri:

* Includi nuovi dati di marketing e fattori incrementali. Ad esempio, nell’ultimo trimestre, le dinamiche di mercato sono cambiate o la distribuzione dei dati di marketing è cambiata in modo significativo.

Per riaddestrare un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Train]**. In alternativa, selezionare ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** dalla barra delle azioni blu.

   Nella finestra di dialogo **[!UICONTROL Train model]**, seleziona l&#39;opzione per:

   * **[!UICONTROL Train model with last 2 years of marketing data]**, oppure
   * **[!UICONTROL Train model using specific date range of data]**.
Specifica l’intervallo di date. È possibile utilizzare il ![Calendario](/help/assets/icons/Calendar.svg) per selezionare un intervallo di date. Devi selezionare un intervallo di dati con un minimo di un anno.

   ![Riaddestramento di un modello](../assets/re-train-model.png)

1. Selezionare **[!UICONTROL Train]** per riaddestrare il modello.


### Punteggio o nuovo punteggio


Puoi assegnare un punteggio incrementale a un modello in base a nuovi dati di marketing o assegnare un nuovo punteggio a un modello per un intervallo di date specifico.

Valuta di valutare nuovamente un modello quando desideri:

* Correggere i dati di marketing errati. Ad esempio, i dati recenti relativi alla ricerca a pagamento inclusi nell’addestramento e nel punteggio del modello non hanno riportato una settimana di dati.
* Utilizza i nuovi dati di marketing incrementali resi disponibili tramite aggiornamenti nei set di dati configurati come parte dei dati armonizzati.

Per assegnare un punteggio o un nuovo punteggio a un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Score]**. In alternativa, selezionare ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** dalla barra delle azioni blu.

   Nella finestra di dialogo **[!UICONTROL Score marketing data]**, seleziona l&#39;opzione per:

   * **[!UICONTROL Score new marketing data from *mm/gg/aaaa *]**, per valutare il modello in modo incrementale utilizzando nuovi dati di marketing, oppure
   * **[!UICONTROL Score specific date range of marketing data]** per ripetere il punteggio per un intervallo di date specifico.
Specifica l’intervallo di date. È possibile utilizzare il ![Calendario](/help/assets/icons/Calendar.svg) per selezionare un intervallo di date.

   ![Riaddestramento di un modello](../assets/re-score-model.png)

1. Selezionare **[!UICONTROL Score]**. Quando si assegna un nuovo punteggio a un modello utilizzando un intervallo di dati specifico, viene visualizzata una finestra di dialogo **[!UICONTROL Existing model is replaced]** in cui viene richiesto di confermare la sostituzione del modello con nuovi punteggi per l’intervallo di date selezionato. Selezionare **[!UICONTROL Replace model]** per confermare.


### Elimina modelli

Per eliminare un modello:

1. Seleziona ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.
1. Seleziona ![Altro](/help/assets/icons/More.svg) per un modello e dal menu di scelta rapida seleziona **[!UICONTROL Delete]**. In alternativa, selezionare ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dalla barra delle azioni blu.
1. Selezionare **[!UICONTROL Delete]** nella finestra di dialogo di conferma **[!UICONTROL Delete model]** per eliminare il modello. Selezionare **[!UICONTROL Cancel]** per annullare.

Per eliminare più modelli:

1. Seleziona più modelli.
1. Dalla barra blu delle azioni, seleziona ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** per eliminare i modelli.
1. Selezionare **[!UICONTROL Delete]** nella finestra di dialogo di conferma **[!UICONTROL Delete *x *modelli]**per eliminare i modelli. Selezionare **[!UICONTROL Cancel]**per annullare.

