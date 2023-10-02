---
title: Conversioni
description: Scopri come creare conversioni da utilizzare come parte dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Conversions
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 3%

---


# Conversioni

Gli eventi di conversione sono obiettivi aziendali che identificano l’impatto delle attività di marketing. Esempi: ordini di e-commerce, acquisti in-store, visite al sito web e così via.

Puoi definire le conversioni marketing per l’analisi di attribuzione.

## Gestire le conversioni

Per visualizzare una tabella delle conversioni disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Conversions]** dalla barra superiore. Vedi una tabella delle conversioni.

Le colonne della tabella specificano i dettagli sulla conversione:

| Nome colonna | Dettagli |
| --- | ---|
| Nome | Nome della conversione. |
| Ricavi | La metrica di dati armonizzata da utilizzare per calcolare i ricavi da una conversione. |
| Metrica di conversione | La metrica di dati armonizzata da utilizzare come metrica di conversione per l’analisi. |
| Creato | Data e ora della creazione della conversione. |
| Ultima modifica | Data e ora dell’ultima modifica della conversione. |

{style="table-layout:auto"}

## Aggiungere una conversione

Per aggiungere una conversione, in ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** interfaccia in Mix Modeler:

1. Seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. In **[!UICONTROL Create Conversion]** finestra di dialogo:

   1. Inserisci un nome per **[!UICONTROL Conversion]**, ad esempio `Store Conversions`.

   1. Definisci il **[!UICONTROL Conversion category]**.

      1. Seleziona un valore da **[!UICONTROL *Seleziona armonizza...*]**, ad esempio `Conversion Type`.

      1. Seleziona un valore per l’operatore ![Freccia](../assets/icons/ChevronDown.svg), ad esempio **[!UICONTROL is]**.

      1. Seleziona un valore da **[!UICONTROL *Seleziona valore *]**oppure inserisci un valore, ad esempio **[!UICONTROL Store]**.

   1. Seleziona un campo armonizzato da **[!UICONTROL Conversion metric for analysis]**, ad esempio **[!UICONTROL Orders]**.

   1. Seleziona un campo armonizzato da **[!UICONTROL Revenue field]**, ad esempio **[!UICONTROL Gross Demand]**.

   1. Per creare la conversione, seleziona **[!UICONTROL Create]**. Per annullare la creazione di una conversione, seleziona **[!UICONTROL Cancel]**.

      ![Testo alternativo](../assets/create-conversion.png)

1. Una volta creata, la conversione viene aggiunta alla tabella delle conversioni.
