---
title: Creare piani
description: Scopri come creare piani in Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 3650135ee3ed5c435593aeed94bee8952bbe6df4
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---


# Creare piani

In Mix Modeler è possibile creare un piano utilizzando l&#39;area di lavoro del piano. Nell&#39;area di lavoro del piano è possibile impostare i dettagli e i budget del piano e del modello sottostante da utilizzare per il piano. Una volta specificati i dettagli, il budget e il modello, puoi procedere con un piano consigliato dall’intelligenza artificiale o modificare la spesa per canale.

Per creare un piano, nell&#39;interfaccia ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** in Mix Modeler, selezionare **[!UICONTROL Create plan]**.


1. Nella schermata **[!UICONTROL Plan creation]**:

   1. Nella sezione **[!UICONTROL Setup]**:

      1. Immettere un **[!UICONTROL Plan name]**, ad esempio `Demo plan`. Immettere un **[!UICONTROL Description]**, ad esempio `Demo plan for Luma company`.
      1. Selezionare un **[!UICONTROL Model]** da **[!UICONTROL _Selezionare un&#39;opzione._.]**
      1. È possibile selezionare ![LinkOut](/help/assets/icons/LinkOut.svg) **[!UICONTROL Create model]** per creare un modello direttamente dalla creazione del piano. Verrà aperta una nuova scheda nel browser e verrà visualizzata l&#39;interfaccia [Models](../models/overview.md).

         ![Configurazione del piano](/help/assets/plan-setup.png)

   1. Nella sezione **[!UICONTROL Budget]**:

      1. Specificare un intervallo di date digitando le date o selezionando un intervallo di date utilizzando ![Calendario](/help/assets/icons/Calendar.svg).
      1. Inserire un budget.

      Per aggiungere altri intervalli di date, ciascuno con il proprio budget, selezionare ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Per eliminare un intervallo di date e il budget associato, selezionare ![Chiudi](/help/assets/icons/Close.svg).

      Per definire un budget massimo specificato:

      1. Attiva **[!UICONTROL Maximize budget]**.
      1. Specifica l&#39;importo del budget massimo. L’importo deve essere uguale o superiore all’importo totale dei budget specificato per gli intervalli di date.

         ![Budget del piano](/help/assets/plan-budget.png)

   1. Seleziona **[!UICONTROL Next]**.

1. Nella finestra di dialogo **[!UICONTROL Done with all required fields]**:

   ![Piano completato](/help/assets/plan-done-required-fields.png)

   * Selezionare ![NuovoPiano](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** se si desidera generare un piano consigliato di IA con ROI previsto.


     Selezionare **[!UICONTROL OK]**. Il piano è stato creato.


   * Selezionare ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se si desidera modificare il budget dei canali e definire configurazioni avanzate prima della creazione di un piano con ROI previsto.

     Seleziona **[!UICONTROL OK]** per definire la spesa del tuo canale in **[!UICONTROL Spend selection]** nel passaggio successivo.



1. Nella sezione **[!UICONTROL Spend selection]**, per ogni intervallo di date del budget, utilizzare la ![freccia](/help/assets/icons/ChevronRight.svg) per aprire la visualizzazione di distribuzione del canale per tale intervallo di dati.

   Puoi utilizzare i dati di riferimento storici se desideri utilizzare dati e informazioni sulle spese di marketing passate. Considera i dati storici di riferimento per:

   * Migliorare l&#39;allocazione del budget evidenziando i canali con prestazioni elevate e quelli con prestazioni insoddisfacenti.
   * Supporta l’analisi delle tendenze.
   * Identificare strategie efficaci ed evitare errori durante la configurazione dei piani.

   Se si seleziona un periodo di riferimento storico, si allinea alle preferenze del modello di spesa precedente e la funzionalità di pianificazione di Mix Modeler può generare piani che rientrano nelle aspettative. Questi piani dovrebbero in ultima analisi aumentare la fiducia delle parti interessate, garantire che i piani di marketing siano strategici ed efficienti e che siano basati su dati sulle prestazioni e sulle esigenze aziendali comprovate.

   ![Selezione spese](/help/assets/plan-spend-selection.png)

   1. Seleziona **[!UICONTROL Spend pattern]**.

      * Per impostazione predefinita è **[!UICONTROL Automatic]**.
      * Selezionare **[!UICONTROL Historical reference]** e immettere **[!UICONTROL Start date]** per fare riferimento ai dati relativi alle spese di marketing precedenti già disponibili per Mix Modeler. **[!UICONTROL End date]** viene determinato automaticamente in base all&#39;intervallo di dati per il quale si definisce il modello di spesa. La data di inizio proposta è il primo dato disponibile sulla spesa di marketing passata. Per indicare che hai selezionato un periodo di riferimento storico non esistente o non valido, viene visualizzato un ![AlertRed](/help/assets/icons/AlertRed.svg).

   1. Per definire i budget per ciascun canale, immettere un valore per **[!UICONTROL Min]** e **[!UICONTROL Max]** oppure utilizzare i cursori.

   1. Per passare dalla valuta all&#39;input percentuale, selezionare **[!UICONTROL $]** o **[!UICONTROL %]** per **[!UICONTROL View spend by]**.

   1. Al termine, selezionare **[!UICONTROL Create]**.
      ![Selezione spese](/help/assets/plan-spend-selection.png)

   1. Seleziona **[!UICONTROL Next]**.



1. Nella sezione **[!UICONTROL Advanced configurations]** è possibile immettere configurazioni avanzate facoltative.

   ![Riepilogo piano](../assets/plan-advanced-configurations.png)

   * Vengono riepilogati il nome del piano, il modello, l&#39;intervallo di date e il budget totale.

   * Per impostazione predefinita, Mix Modeler calcola automaticamente i ricavi medi per conversione utilizzando i dati stagionali storici più recenti. In **[!UICONTROL Average Revenue per conversion]** puoi definire ricavi medi specifici per conversione.

      1. Per ogni intervallo di date nel budget:

         1. Selezionare un intervallo di date dal menu a discesa **[!UICONTROL Date range]**.
         1. Immettere un valore **[!UICONTROL Average revenue]**.

      1. Seleziona ![AggiungiCerchio](/help/assets/icons/AddCircle.svg) Aggiungi ricavi medi personalizzati per unità di conversione per aggiungere un intervallo di date.
      1. Selezionare ![RimuoviCerchio](/help/assets/icons/RemoveCircle.svg) per rimuovere un intervallo di date.

     >[!NOTE]
     >
     >Se il modello non include dati storici sui ricavi, è necessario definire un ricavo medio per conversione per ogni intervallo di date specificato per il budget.
     >

   * Per impostazione predefinita, Mix Modeler calcola automaticamente i costi del canale utilizzando i dati stagionali più recenti. In **[!UICONTROL Channel costs]** è possibile definire i costi del canale personalizzati.

      1. Per ogni canale nel modello, definisci il costo del canale personalizzato.

         1. Selezionare un canale dal menu a discesa **[!UICONTROL Channel]**.
         1. Per ogni intervallo di date nel budget:
            1. Selezionare un intervallo di date dal menu a discesa **[!UICONTROL Date range]**.
            1. Immettere un valore **[!UICONTROL Average revenue]**.
         1. Seleziona ![AggiungiCerchio](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** per aggiungere un intervallo di date.
         1. Selezionare ![RimuoviCerchio](/help/assets/icons/RemoveCircle.svg) per rimuovere un intervallo di date.

      1. Selezionare ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** per aggiungere un canale.
      1. Selezionare ![CrossSize400](/help/assets/icons/CrossSize400.svg) per rimuovere un canale personalizzato.


   1. Al termine, selezionare **[!UICONTROL Create]**.

   1. Nella finestra di dialogo **[!UICONTROL Create plan]**, seleziona **[!UICONTROL Create plan]** per creare il piano. Selezionare **[!UICONTROL Cancel]** per annullare la creazione del piano. Viene visualizzata una finestra di dialogo **[!UICONTROL No work is saved]** per confermare.

