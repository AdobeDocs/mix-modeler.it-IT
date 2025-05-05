---
title: Conversioni
description: Scopri come creare conversioni da utilizzare come parte dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 935b179e31d1b677a8c83b1566c02b7aaa617e8d
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---

# Conversioni

Gli eventi di conversione sono obiettivi aziendali che identificano l’impatto delle attività di marketing. Esempi: ordini di e-commerce, acquisti in-store, visite al sito web e così via.

Puoi definire le conversioni marketing per l’analisi di attribuzione.

## Gestire le conversioni

Per visualizzare una tabella delle conversioni disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Conversions]** dalla barra superiore. Vedi una tabella delle conversioni.

Le colonne della tabella specificano i dettagli sulla conversione:

| Nome colonna | Dettagli |
| --- | ---|
| Nome | Nome della conversione. |
| Ricavi | La metrica di dati armonizzata da utilizzare per calcolare i ricavi da una conversione. |
| Metrica di conversione | La metrica di dati armonizzata da utilizzare come metrica di conversione per l’analisi. |
| Categoria | La categoria di conversione della conversione. |
| Creato | Data e ora della creazione della conversione. |
| Ultima modifica | Data e ora dell’ultima modifica della conversione. |


## Aggiungere una conversione

Per aggiungere una conversione, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** in Mix Modeler:

1. Selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. Nella finestra di dialogo **[!UICONTROL Create conversion]**:

   1. Immettere un nome per **[!UICONTROL Conversion]**, ad esempio `Store Conversions`.

   1. Definisci **[!UICONTROL Conversion category]**.

      1. Seleziona un valore da **[!UICONTROL *Seleziona armonizza...*]**, ad esempio `Conversion types`.

      1. Selezionare un valore per l&#39;operatore ![Chevron](/help/assets/icons/ChevronDown.svg), ad esempio **[!UICONTROL is]**.

      1. Selezionare un valore da **[!UICONTROL *Selezionare un valore *]**&#x200B;o immettere un valore, ad esempio **[!UICONTROL Store]**.

   1. Selezionare un campo armonizzato da **[!UICONTROL Conversion metric for analysis]**, ad esempio **[!UICONTROL Orders]**.

   1. Selezionare un campo armonizzato da **[!UICONTROL Revenue field]**, ad esempio **[!UICONTROL Gross Demand]**.

   1. Per creare la conversione, selezionare **[!UICONTROL Create]**. Per annullare la creazione di una conversione, selezionare **[!UICONTROL Cancel]**.

      ![Testo alternativo](/help/assets/create-conversion.png)

1. Una volta creata, la conversione viene aggiunta alla tabella delle conversioni.


## Visualizza dettagli

Per visualizzare i dettagli di una conversione:

1. Selezionare ![Altro](/help/assets/icons/More.svg) quando si passa il mouse su un nome di conversione nella tabella.

1. Selezionare ![Visualizza](/help/assets/icons/ViewDetail.svg) **Visualizza dettagli**. Una finestra di dialogo mostra i dettagli della conversione. Per ulteriori informazioni, vedere [Aggiungere una conversione](#add-a-conversion). Selezionare **[!UICONTROL Cancel]** per chiudere la finestra di dialogo.

## Visualizza rapporto

Per visualizzare un rapporto di una conversione:

1. Selezionare ![Altro](/help/assets/icons/More.svg) quando si passa il mouse su un nome di conversione nella tabella.

1. Selezionare ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Visualizza report**. Una finestra di dialogo mostra un rapporto della conversione.

   ![Rapporto vista conversione](../assets/conversion-view-report.png)

   * Per modificare la granularità su cui generare il rapporto, selezionare un valore dal menu a discesa **[!UICONTROL Weekly]**.
   * Per modificare il periodo su cui generare il rapporto, immettere una data di inizio e una data di fine oppure utilizzare ![Calendario](/help/assets/icons/Calendar.svg) per definire un periodo nel popup del calendario.

1. Selezionare **[!UICONTROL Close]** per chiudere la finestra di dialogo.

## Eliminare una conversione

Per eliminare una conversione:

1. Selezionare ![Elimina](/help/assets/icons/Delete.svg) **Elimina** quando si passa il puntatore del mouse su un nome di conversione nella tabella.
1. Nella finestra di dialogo di conferma **[!UICONTROL Delete conversion]**, seleziona **[!UICONTROL Delete]** per eliminare definitivamente la conversione.
