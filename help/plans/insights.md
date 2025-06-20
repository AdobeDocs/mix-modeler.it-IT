---
title: Pianificare gli approfondimenti
description: Scopri come visualizzare informazioni approfondite sul piano e modificarlo in Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 0%

---

# Pianificare gli approfondimenti


In [!UICONTROL Plan insights] vengono create le informazioni del piano, con [!UICONTROL Model], [!UICONTROL Data range] e [!UICONTROL Plan target] su cui è basato il piano.


Quando crei gli approfondimenti, visualizzi una panoramica del piano, costituita da:

- Intestazione che visualizza [!UICONTROL Model], [!UICONTROL Data range] e [!UICONTROL Plan target] su cui si basa il piano.
   - Se hai definito un piano basato sull’obiettivo, un badge indica lo stato del target. Le opzioni possibili sono:

      - [!BADGE Destinazione raggiungibile]{type=Positive}
      - [!BADGE Destinazione non raggiungibile]{type=Negative}

   - Selezionare ![ChevronDown](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Show more]** per visualizzare ulteriori dettagli.

- [Visualizzazione [!UICONTROL Forecasted paid channel ROI]](#forecasted-paid-channel-spend-and-roi)
- [Visualizzazione [!UICONTROL Forecasted revenue]](#forecasted-revenue)
- [Visualizzazione [!UICONTROL Forecasted conversion]](#forecasted-conversions)
- [Visualizzazione [!UICONTROL Marginal channel return]](#marginal-channel-return)
- [[!UICONTROL Data range breakdown] tabella del piano](#date-range-breakdown), con colonne per

   - Channel
   - ROI
   - CPA
   - Ricavi
   - Obiettivo di conversione
   - Spesa

Per chiudere l&#39;interfaccia, selezionare **[!UICONTROL Close]**.

Per modificare la modalità di visualizzazione del ROI del piano, selezionare **[!UICONTROL X]** o **[!UICONTROL &#x200B; %]** in **[!UICONTROL View ROI]**.

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

Questa visualizzazione del grafico a linee mostra una curva di ritorno marginale per il canale selezionato con indicatori per **[!UICONTROL Marginal break-even]** e **[!UICONTROL Return point]**. Questa visualizzazione ti aiuta a capire come la spesa per un canale viene dal raggiungimento di un punto di pareggio marginale. E se si dispone di spazio per aumentare la spesa in un canale o se si dovrebbe spendere meno su un canale per migliorare l&#39;efficienza della spesa del canale.

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

Per modificare il piano, selezionare ![Modifica](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**.

1. Nella sezione **[!UICONTROL Spend selection]**, per ogni intervallo di date del budget, utilizzare la ![freccia](/help/assets/icons/ChevronRight.svg) per aprire la visualizzazione di distribuzione del canale per tale intervallo di dati.

   Puoi utilizzare i dati di riferimento storici se desideri utilizzare dati e informazioni sulle spese di marketing passate. Considera i dati di riferimento storici per:

   - Migliorare l&#39;allocazione del budget evidenziando i canali con prestazioni elevate e quelli con prestazioni insoddisfacenti.
   - Supporta l’analisi delle tendenze.
   - Identificare strategie efficaci ed evitare errori durante la configurazione dei piani.

   Se si seleziona un periodo di riferimento storico, si allinea alle preferenze del modello di spesa precedente e la funzionalità di pianificazione di Mix Modeler può generare piani che rientrano nelle aspettative. Questi piani dovrebbero in ultima analisi aumentare la fiducia delle parti interessate, garantire che i piani di marketing siano strategici ed efficienti e che siano basati su dati sulle prestazioni e sulle esigenze aziendali comprovate.

   ![Selezione spese](/help/assets/plan-spend-selection.png)

   1. Seleziona **[!UICONTROL Spend pattern]**.

      - L&#39;opzione predefinita è **[!UICONTROL Automatic]**.
      - Selezionare **[!UICONTROL Historical reference]** e immettere **[!UICONTROL Start date]** per fare riferimento ai dati relativi alle spese di marketing precedenti già disponibili per Mix Modeler. **[!UICONTROL End date]** viene determinato automaticamente in base all&#39;intervallo di dati selezionato. La data di inizio proposta è il primo dato disponibile sulla spesa di marketing passata. Per indicare che hai selezionato un periodo di riferimento storico non esistente, viene visualizzato un ![AlertRed](/help/assets/icons/AlertRed.svg).


   1. Per modificare i budget per ciascun canale, modificare i valori per **[!UICONTROL Min]** e **[!UICONTROL Max]** o utilizzare i cursori.

   1. Per passare dalla valuta all&#39;input percentuale, selezionare **[!UICONTROL $]** o **[!UICONTROL %]** per **[!UICONTROL View spend by]**.

   1. Per modificare i dettagli del piano, selezionare **[!UICONTROL Edit details]**:

      1. Nella sezione **[!UICONTROL Setup]**:

         1. Immettere un **[!UICONTROL Plan name]**, ad esempio `Demo plan`. Immettere un **[!UICONTROL Description]**, ad esempio `Demo plan for Luma company`.
         1. Selezionare un **[!UICONTROL Model]** da **[!UICONTROL _Selezionare un&#39;opzione._.]**

            ![Configurazione del piano](/help/assets/plan-setup.png)

      1. Nella sezione **[!UICONTROL Goal]** selezionare l&#39;obiettivo per il quale si desidera ottimizzare il piano. Puoi scegliere tra
         - **[!UICONTROL I have a budget to spend]**

           ![Budget del piano](../assets/plan-budget.png)

           Questa opzione consente di inserire budget per uno o più intervalli di date.

            1. Nel contenitore **[!UICONTROL Optimize]**:
               1. Selezionare una conversione dal menu a discesa **[!UICONTROL Select conversion]**.
               1. Selezionare un modello dal menu a discesa **[!UICONTROL Select model]**.
            1. Specificare **[!UICONTROL Date range]** digitando le date o selezionando un intervallo di date utilizzando ![Calendario](/help/assets/icons/Calendar.svg).
            1. Immetti **[!UICONTROL Budget]**.
Per aggiungere altri intervalli di date, ciascuno con il proprio budget, selezionare ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Per eliminare un intervallo di date e il budget associato, selezionare ![Chiudi](/help/assets/icons/Close.svg).
            1. Per definire un budget massimo facoltativo entro il quale si desidera vincolare il piano:
               1. Attiva **[!UICONTROL Maximize budget]**.
               1. Specifica l&#39;importo del budget massimo. L’importo deve essere uguale o superiore all’importo totale dei budget specificati per gli intervalli di date.


         - **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

           ![Destinazione piano](../assets/plan-target.png)

            1. Nel contenitore **[!UICONTROL Optimize]**
               1. Selezionare una conversione dal menu a discesa **[!UICONTROL Select conversion]**.
               1. Selezionare una metrica di destinazione dal menu a discesa **[!UICONTROL Select target metric]**. È possibile selezionare tra **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** o **[!UICONTROL ROI]**.
               1. Selezionare un modello dal menu a discesa **[!UICONTROL Select model]**.
            1. Specificare un intervallo di date digitando le date o selezionando un intervallo di date utilizzando ![Calendario](/help/assets/icons/Calendar.svg).
            1. Immetti un valore per la metrica di destinazione selezionata. Ad esempio, un numero per **[!UICONTROL Conversion]**, una percentuale per **[!UICONTROL ROI]** o valori di valuta per **[!UICONTROL CPA]** e **[!UICONTROL Revenue]**.
Per aggiungere altri intervalli di date, ciascuno con la propria metrica di destinazione, selezionare ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Per eliminare un intervallo di date e la metrica di destinazione associata, selezionare ![Chiudi](/help/assets/icons/Close.svg).
            1. Per definire un budget massimo facoltativo entro il quale si desidera vincolare il piano:
               1. Attiva **[!UICONTROL Maximize budget]**.
               1. Specifica l&#39;importo del budget massimo.

         1. Selezionare **[!UICONTROL Next]** per tornare alla sezione **[!UICONTROL Spend selection]**.

1. Nella sezione **[!UICONTROL Advanced configuration]**:

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


- Per annullare gli aggiornamenti del piano in qualsiasi momento, selezionare **[!UICONTROL Cancel]**. Nella finestra di dialogo **[!UICONTROL No work will be saved]**, seleziona **[!UICONTROL Cancel]** per continuare a lavorare sul piano oppure seleziona **[!UICONTROL OK]** per tornare all&#39;interfaccia Piani.
- Per tornare alla procedura guidata, selezionare **[!UICONTROL Back]**.
