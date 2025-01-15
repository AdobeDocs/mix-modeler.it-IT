---
title: Creare un piano
description: Scopri come creare un piano in Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 6331bdfcbc792c03f9cc129daa4e591c2b46a8f1
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Creare un piano

In Mix Modeler è possibile creare un piano utilizzando l&#39;area di lavoro del piano. Nell&#39;area di lavoro del piano è possibile impostare i dettagli e i budget del piano e del modello sottostante da utilizzare per il piano. Una volta specificati i dettagli, il budget e il modello, puoi procedere con un piano consigliato dall’intelligenza artificiale o modificare la spesa per canale.

Per creare un piano, nell&#39;interfaccia ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** in Mix Modeler, selezionare **[!UICONTROL Create plan]**.

1. Nella schermata di creazione del piano:

   1. Nella sezione **[!UICONTROL Setup]**

      1. Immettere un **[!UICONTROL Plan name]**, ad esempio `Demo plan`. Immettere un **[!UICONTROL Description]**, ad esempio `Demo plan for Luma company`.
      1. Selezionare un **[!UICONTROL Model]** da **[!UICONTROL _Selezionare un&#39;opzione._.]**.
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

   * Seleziona <img src="/help/assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** se si desidera generare un piano consigliato di IA con ROI previsto.

     Selezionare **[!UICONTROL OK]**. Il piano è stato creato.


   * Selezionare ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se si desidera modificare il budget dei canali prima di creare un piano con ROI previsto.

     Seleziona **[!UICONTROL OK]** per definire la spesa del tuo canale in **[!UICONTROL Spend selection]** nel passaggio successivo.



1. Nella sezione **[!UICONTROL Spend selection]**, per ogni intervallo di date del budget, utilizza la ![freccia](/help/assets/icons/ChevronRight.svg) superiore per aprire la visualizzazione di distribuzione del canale per tale intervallo di dati.

   1. Per definire i budget per ciascun canale, immettere un valore per **[!UICONTROL Min]** e **[!UICONTROL Max]** oppure utilizzare i cursori.

   1. Per passare dalla valuta all&#39;input percentuale, selezionare **[!UICONTROL $]** o **[!UICONTROL %]** per **[!UICONTROL View spend by]**.

      ![Selezione spese](/help/assets/plan-spend-selection.png)

   1. Al termine, selezionare **[!UICONTROL Create]**.

   1. Nella finestra di dialogo **[!UICONTROL Create plan]**, seleziona **[!UICONTROL Create plan]** per creare il piano. Selezionare **[!UICONTROL Cancel]** per annullare la creazione del piano. Viene visualizzata una finestra di dialogo **[!UICONTROL No work is saved]** per confermare.
