---
title: Pianificare gli approfondimenti
description: Scopri come visualizzare informazioni approfondite sul piano e modificarlo in Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: 1d017960409e5433ac6b4950a5cf7a5b3174840a
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Pianificare gli approfondimenti


In [!UICONTROL Plan insights], vengono create le informazioni del piano, mostrando [!UICONTROL Model], [!UICONTROL Data range] e [!UICONTROL Total budget] su cui è basato il piano.

Al termine del recupero, viene visualizzata una panoramica del piano, costituita da:

- Visualizzazione [!UICONTROL Forecasted paid channel ROI]
- Visualizzazione [!UICONTROL Forecasted revenue]
- Visualizzazione [!UICONTROL Forecasted conversion]
- Visualizzazione [!UICONTROL Marginal channel return]
- [!UICONTROL Data range breakdown] tabella del piano, con colonne per

   - Channel
   - ROI
   - CPA
   - Ricavi
   - Obiettivo di conversione
   - Spesa

Per chiudere l&#39;interfaccia, selezionare **[!UICONTROL Close]**.

Per modificare la modalità di visualizzazione del ROI del piano, selezionare **[!UICONTROL X]** o **[!UICONTROL  %]** in **[!UICONTROL View ROI]**.

## Spesa canale a pagamento e ROI previsti

Questa visualizzazione mostra un grafico a dispersione per la spesa prevista e il ritorno sull’investimento sui canali a pagamento, in base al modello, all’intervallo di date e al budget.

![Spesa canale a pagamento prevista e visualizzazione del ROI](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## Ricavi previsti

Questa visualizzazione con grafico a barre mostra i ricavi previsti per i canali in base al modello, all’intervallo di date e al budget.

![Visualizzazione ricavi previsti](../assets/overview-plan-forecasted-revenue.png)


## Conversioni previste

Questa visualizzazione con grafico a barre mostra le conversioni previste per i canali in base al modello, all’intervallo di date e al budget.

![Visualizzazione delle conversioni previste](../assets/overview-plan-forecasted-conversions.png)


## Ritorno canale marginale

Questa visualizzazione del grafico a linee mostra una curva di ritorno marginale per il canale selezionato con indicatori per **[!UICONTROL Marginal break-even]** e **[!UICONTROL Return point]**. Questa visualizzazione ti aiuta a capire come la spesa per un canale viene dal raggiungimento di un punto di pareggio marginale e se hai spazio per aumentare la spesa in un canale o se dovresti spendere meno su un canale per migliorare l’efficienza della spesa del canale.

![Visualizzazione ritorno canale marginale](../assets/overview-plan-marginal-channel-return.png)

Per selezionare un canale specifico per la visualizzazione, seleziona un canale dal menu a discesa **[!UICONTROL View]**.


## Raggruppamento per intervallo di date

La tabella [!UICONTROL Date range breakdown] mostra dati granulari dettagliati per canale per [!UICONTROL ROI], [!UICONTROL Revenue], [!UICONTROL CPA], [!UICONTROL Conversions] e [!UICONTROL Spend].

![Tabella di suddivisione intervallo di date](../assets/overview-plan-date-range-breakdown.png)

1. Per scaricare un file CSV contenente i dati del raggruppamento per intervallo di date, seleziona ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**. Dal menu di scelta rapida:

   - Seleziona ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** per i dati dettagliati in formato CSV.
   - Seleziona ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Summary CSV]** per i dati di riepilogo in formato CSV.

   I dati dettagliati sono dati granulari divisi per settimana. I dati di riepilogo sono dati chiave dell’intervallo di date fornito dal modello.

1. Per visualizzare la suddivisione dell&#39;intervallo di date per categoria di canali, selezionare **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]** o **[!UICONTROL Non-paid channels]** dalla selezione **[!UICONTROL View]**.


## Modifica piano

1. Per modificare il piano, seleziona ![Modifica](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**:

   Nella sezione **[!UICONTROL Spend selection]**, per ogni intervallo di date del budget, utilizzare la ![freccia](/help/assets/icons/ChevronRight.svg) per aprire la visualizzazione di distribuzione del canale per tale intervallo di dati.

   Puoi utilizzare i dati di riferimento storici se desideri utilizzare dati e informazioni sulle spese di marketing passate. Considera i dati storici di riferimento per:

   - Migliorare l&#39;allocazione del budget evidenziando i canali con prestazioni elevate e quelli con prestazioni insoddisfacenti.
   - Supporta l’analisi delle tendenze.
   - Identificare strategie efficaci ed evitare errori durante la configurazione dei piani.

   Se si seleziona un periodo di riferimento storico, si allinea alle preferenze del modello di spesa precedente e la funzionalità di pianificazione di Mix Modeler può generare piani che rientrano nelle aspettative. Questi piani dovrebbero in ultima analisi aumentare la fiducia delle parti interessate, garantire che i piani di marketing siano strategici ed efficienti e che siano basati su dati sulle prestazioni e sulle esigenze aziendali comprovate.

   ![Selezione spese](/help/assets/plan-spend-selection.png)

   1. Seleziona **[!UICONTROL Spend pattern]**.

      - Per impostazione predefinita è **[!UICONTROL Automatic]**.
      - Selezionare **[!UICONTROL Historical reference]** e immettere **[!UICONTROL Start date]** per fare riferimento ai dati relativi alle spese di marketing precedenti già disponibili per Mix Modeler. **[!UICONTROL End date]** viene determinato automaticamente in base all&#39;intervallo di dati selezionato. La data di inizio proposta è il primo dato disponibile sulla spesa di marketing passata. Per indicare che hai selezionato un periodo di riferimento storico non esistente, viene visualizzato un ![AlertRed](/help/assets/icons/AlertRed.svg).


   1. Per modificare i budget per ciascun canale, modificare i valori per **[!UICONTROL Min]** e **[!UICONTROL Max]** o utilizzare i cursori.

   1. Per passare dalla valuta all&#39;input percentuale, selezionare **[!UICONTROL $]** o **[!UICONTROL %]** per **[!UICONTROL View spend by]**.

   1. Per modificare i dettagli del piano, selezionare **[!UICONTROL Edit details]**:

      1. Nella sezione **[!UICONTROL Setup]**, se applicabile, modificare **[!UICONTROL Plan name]** e **[!UICONTROL Description]**.

      1. Nella sezione **[!UICONTROL Budget]**:

         1. Modificare **[!UICONTROL Date range]** per uno o più intervalli di date del piano digitando le date o selezionando un intervallo di date utilizzando ![Calendario](/help/assets/icons/Calendar.svg).

         1. Modifica **[!UICONTROL Budget]** per uno o più intervalli di date del piano.

         Per aggiungere altri intervalli di date, ciascuno con il proprio budget, selezionare ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

         Per eliminare un intervallo di date e il budget associato, selezionare ![Chiudi](/help/assets/icons/Close.svg).

         Per definire un budget massimo:

         1. Attiva **[!UICONTROL Maximize budget]**.
         1. Specifica l&#39;importo del budget massimo. L’importo deve essere uguale o superiore all’importo totale dei budget specificato per gli intervalli di date.

      1. Selezionare **[!UICONTROL Next]** per tornare alla sezione **[!UICONTROL Spend]**. Seleziona **[!UICONTROL Cancel]** per tornare alla panoramica dei tuoi piani.

         ![Dettagli piano](/help/assets/plan-details.png)

   1. Se sono state definite configurazioni avanzate per il piano, selezionare **[!UICONTROL Next]**.

      ![Modifica configurazione avanzata](../assets/edit-plan-advanced-configuration.png)

      - Vengono riepilogati il nome del piano, il modello, l&#39;intervallo di date e il budget totale.

      - Per impostazione predefinita, Mix Modeler calcola automaticamente i ricavi medi per conversione utilizzando i dati stagionali storici più recenti. In **[!UICONTROL Average Revenue per conversion]** puoi definire ricavi medi specifici per conversione.

         1. Per ogni intervallo di date nel budget:
            1. Selezionare un intervallo di date dal menu a discesa **[!UICONTROL Date range]**.
            1. Immettere un valore **[!UICONTROL Average revenue]**.

         1. Seleziona ![AggiungiCerchio](/help/assets/icons/AddCircle.svg) Aggiungi ricavi medi personalizzati per unità di conversione per aggiungere un intervallo di date.
         1. Selezionare ![RimuoviCerchio](/help/assets/icons/RemoveCircle.svg) per rimuovere un intervallo di date.

        >[!NOTE]
        >
        >Se il modello non include dati storici sui ricavi, è necessario definire un ricavo medio per conversione per ogni intervallo di date specificato per il budget.
        >

      - Per impostazione predefinita, Mix Modeler calcola automaticamente i costi del canale utilizzando i dati stagionali più recenti. In **[!UICONTROL Channel costs]** è possibile definire i costi del canale personalizzati.

         1. Per ogni canale nel modello, definisci il costo del canale personalizzato.
            1. Selezionare un canale dal menu a discesa **[!UICONTROL Channel]**.
            1. Per ogni intervallo di date nel budget:
               1. Selezionare un intervallo di date dal menu a discesa **[!UICONTROL Date range]**.
               1. Immettere un valore **[!UICONTROL Average revenue]**.
            1. Seleziona ![AggiungiCerchio](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** per aggiungere un intervallo di date.
            1. Selezionare ![RimuoviCerchio](/help/assets/icons/RemoveCircle.svg) per rimuovere un intervallo di date.

         1. Selezionare ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** per aggiungere un canale.
         1. Selezionare ![CrossSize400](/help/assets/icons/CrossSize400.svg) per rimuovere un canale personalizzato.


1. Al termine della modifica del piano, selezionare **[!UICONTROL Edit]**.

   Nella finestra di dialogo **[!UICONTROL All changes are final]**, selezionare **[!UICONTROL OK]** per aggiornare l&#39;allocazione di spesa corrente del piano e le previsioni di ROI e ricavi. Selezionare **[!UICONTROL Cancel]** per annullare l&#39;aggiornamento del piano.

1. Per annullare gli aggiornamenti del piano, selezionare **[!UICONTROL Cancel]**.

   Nella finestra di dialogo **[!UICONTROL No work will be saved]**, seleziona **[!UICONTROL Cancel]** per continuare a lavorare sul tuo piano oppure seleziona **[!UICONTROL OK]** per tornare all&#39;interfaccia Piani.
