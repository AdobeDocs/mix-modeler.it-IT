---
title: Panoramica dei piani
description: Scopri come visualizzare, selezionare e intervenire sui piani in Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Panoramica dei piani

I piani in Mix Modeler consentono di allocare budget per business unit e canale. La funzionalità di pianificazione è integrata con i risultati dei modelli formati in base ai dati armonizzati.

Un piano delinea gli investimenti discrezionali (ad esempio i budget) che un’azienda intende spendere per progetti di marketing in un determinato arco temporale. Questi investimenti servono i KPI comuni (ad esempio ordini, ricavi). I piani possono includere le spese da canali come pubblicità a pagamento, contenuti web sponsorizzati, eventi.

Un piano richiede:

- un modello,
- una serie di dati,
- un budget.

Un piano può facoltativamente includere:

- una finestra di riconoscimento configurata,
- più date di volo, ognuna con un budget prefissato,
- vincoli di budget minimi e massimi per canale e data di volo.

Se un modello utilizzato per il piano viene valutato in base a nuovi dati, è necessario creare un nuovo piano per tenere conto dei dati ricalcolati.


## Creare piani

Per creare un piano, utilizzare la procedura guidata di creazione del piano di Mix Modeler. Per ulteriori dettagli, consulta [Piani di compilazione](build.md).


## Gestisci piani

Per visualizzare una tabella dei piani correnti, nell&#39;interfaccia di Mix Modeler:

1. Seleziona ![](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** dalla barra a sinistra.

1. Viene visualizzata una tabella dei piani correnti e del relativo stato.

   Le colonne della tabella specificano i dettagli relativi ai piani.

   | Nome colonna | Dettagli |
   |---|---|
   | Nome | Nome del piano |
   | Modello | Modello utilizzato come base per il piano. |
   | Intervallo date | Intervallo di date completo per un piano. |
   | Budget | Budget totale per un piano. |
   | Destinazione piano | La metrica di destinazione definita per un piano basato su destinazione. |
   | Rendimento previsto | [rendimento previsto](/help/main-guide/glossary.md) per un piano |
   | ROI previsto | [ROI previsto](/help/main-guide/glossary.md) per un piano. |
   | Conversione prevista | [conversione prevista](/help/main-guide/glossary.md) per un piano |
   | CPA previsto | Il [CPA previsto](/help/main-guide/glossary.md)per un piano |
   | Stato | Stato di un piano: <p><span style="color:red">●</span> non riuscito, <p>Elaborazione di <span style="color:blue">●</span> oppure <p><span style="color:green">●</span> completato. |

   {style="table-layout:auto"}

   È possibile utilizzare ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) per selezionare ![Spunta](/help/assets/icons/Checkmark.svg) le colonne da visualizzare nella tabella.

1. Utilizza ![Ricerca](/help/assets/icons/Search.svg) per cercare e filtrare la tabella per uno o più piani specifici.

### Pianificare gli approfondimenti

Per visualizzare gli approfondimenti di un piano e modificarne uno:

1. Seleziona ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** dalla barra a sinistra.

1. Selezionare il nome del piano.

Sei stato reindirizzato a [Informazioni sul piano](insights.md).


### Duplicare un piano

Per duplicare un piano:

- Seleziona ![Altro](/help/assets/icons/More.svg) per un piano. Dal menu di scelta rapida, selezionare **[!UICONTROL Duplicate]**.
- In alternativa, selezionare un piano nella tabella ![SelectBox](/help/assets/icons/SelectBox.svg) e selezionare ![Copy](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** dalla barra delle azioni blu.

Viene creato un nuovo piano, con un nome composto dal nome del piano originale seguito da **[!UICONTROL (Copy)] (_n_)**. Viene automaticamente reindirizzato a [Creazione piano](build.md) per fornire dettagli aggiornati per il piano copiato.

- I dettagli (come Descrizione, Budget e altro) del piano originale vengono copiati.
- I vincoli di budget del piano originale vengono copiati nel piano appena creato.
- È possibile selezionare un altro modello come base per il piano copiato.
   - Per i punti di contatto o i canali che esistono nel piano copiato ma non nel modello appena selezionato, eventuali vincoli per tali punti di contatto o canali vengono rimossi dal piano.
   - Per i punti di contatto o i canali che non esistono nel piano copiato ma esistono nel modello appena selezionato, i vincoli sono impostati su:
      - un valore minimo di `0`,
      - un valore massimo in linea con il budget intervallo di voli del piano.



### Confronta piani

Per confrontare i piani:

1. Selezionare due piani dalla tabella.
1. Seleziona ![Confronta](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** dalla barra delle azioni blu. Viene visualizzata l&#39;interfaccia utente di **[!UICONTROL Compare plans]**.


### Elimina piani

Per eliminare un piano:

1. Seleziona ![Altro](/help/assets/icons/More.svg) per un piano. Dal menu di scelta rapida, selezionare **[!UICONTROL Delete]**. <br/>In alternativa, selezionare un piano nella tabella ![SelectBox](/help/assets/icons/SelectBox.svg) e selezionare ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dalla barra delle azioni blu.
1. Selezionare **[!UICONTROL Delete]** nella finestra di conferma **[!UICONTROL Delete plan]** per eliminare il piano. Selezionare **[!UICONTROL Cancel]** per annullare.

Per eliminare più piani:

1. Selezionare più piani.
1. Dalla barra delle azioni blu, selezionare ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** per eliminare i piani.
1. Selezionare **[!UICONTROL Delete]** nella finestra di conferma **[!UICONTROL Delete *x *piani]**&#x200B;per eliminare i piani. Selezionare **[!UICONTROL Cancel]**&#x200B;per annullare.


