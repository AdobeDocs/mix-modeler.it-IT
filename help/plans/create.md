---
title: Creare un piano
description: Scopri come creare un piano in Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Creare un piano

In Mix Modeler è possibile creare un piano utilizzando l&#39;area di lavoro del piano. Nell&#39;area di lavoro del piano è possibile impostare i dettagli e i budget del piano e del modello sottostante da utilizzare per il piano. Una volta specificati i dettagli, il budget e il modello, puoi procedere con un piano consigliato dall’intelligenza artificiale o modificare la spesa per canale.

Per creare un piano, in ![PLan](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** in Mix Modeler, seleziona **[!UICONTROL Open plan canvas]**.

1. Nella schermata di creazione del piano:

   1. In **[!UICONTROL Setup]** sezione

      1. Immetti un **[!UICONTROL Plan name]**, ad esempio `Demo plan`. Immetti un **[!UICONTROL Description]**, ad esempio `Demo plan for Luma company`.
      1. Seleziona un **[!UICONTROL Model]** da **[!UICONTROL _Seleziona un’opzione._.]**.
      1. Puoi selezionare ![LinkOut](../assets/icons/LinkOut.svg) **[!UICONTROL Create model]** per creare un modello direttamente dalla creazione del piano. Verrà aperta una nuova scheda nel browser e verranno visualizzati i [Modelli](../models/overview.md) di rete.

         ![Impostazione piano](../assets/plan-setup.png)

   1. In **[!UICONTROL Budget]** sezione:

      1. Specificare un intervallo di date digitando le date o selezionando un intervallo di date utilizzando ![Calendario](../assets/icons/Calendar.svg).
      1. Inserire un budget.

      Per aggiungere altri intervalli di date, ciascuno con il relativo budget, seleziona ![CalendarAdd](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Per eliminare un intervallo di date e il budget associato, selezionare ![Chiudi](../assets/icons/Close.svg).

      Per definire un budget massimo specificato:

      1. Switch **[!UICONTROL Maximize budget]** su.
      1. Specifica l&#39;importo del budget massimo. L’importo deve essere uguale o superiore all’importo totale dei budget specificato per gli intervalli di date.

         ![Budget del piano](../assets/plan-budget.png)

   1. Seleziona **[!UICONTROL Next]**.

1. In **[!UICONTROL Done with all required fields]** finestra di dialogo:

   ![Piano completato](../assets/plan-done-required-fields.png)

   * Seleziona <img src="../assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** se desideri generare un piano consigliato ai con ROI previsto.

     Seleziona **[!UICONTROL OK]**. Il piano è stato creato.


   * Seleziona ![ModificaTabella](../assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se si desidera modificare il budget dei canali prima di creare un piano con ROI previsto.

     Seleziona **[!UICONTROL OK]**, in modo da poter definire la spesa del canale in **[!UICONTROL Spend selection]** nel passaggio successivo.



1. In **[!UICONTROL Spend selection]** sezione, per ogni intervallo di date del budget, utilizzare ![Freccia](../assets/icons/ChevronRight.svg) in alto apri la vista distribuzione canale per tale intervallo di dati.

   1. Per definire i budget per ciascun canale, immetti un valore per **[!UICONTROL Min]** e **[!UICONTROL Max]** oppure utilizzare i dispositivi di scorrimento.

   1. Per passare da un input di valuta a un input di percentuale, seleziona **[!UICONTROL $]** o **[!UICONTROL %]** per **[!UICONTROL View spend by]**.

      ![Selezione spesa](../assets/plan-spend-selection.png)

   1. Al termine, seleziona **[!UICONTROL Create]**.

   1. In **[!UICONTROL Create plan]** finestra di dialogo, seleziona **[!UICONTROL Create plan]** per creare il piano. Seleziona **[!UICONTROL Cancel]** per annullare la creazione del piano. A **[!UICONTROL No work is saved]** viene visualizzata una finestra di dialogo di conferma.
