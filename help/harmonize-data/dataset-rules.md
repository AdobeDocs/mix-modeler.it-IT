---
title: Regole del set di dati
description: Scopri come definire le regole del set di dati da utilizzare come parte dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 33883626d8e7aca2eecc3571593be53ef41ac458
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Regole del set di dati

Le regole del set di dati ti aiutano a mappare i campi armonizzati con i campi dei dati acquisiti in Mix Modeler.

* Per i dati aggregati acquisiti in Adobe Experience Platform, mappi uno o più campi del set di dati disponibili ai campi armonizzati appropriati.
* Per i dati evento, puoi mappare singolarmente uno o più campi armonizzati ai campi del set di dati, direttamente o utilizzando le condizioni.


## Gestire regole e mappature dei set di dati

Per visualizzare una tabella dei mapping dei set di dati disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Dataset rules]** dalla barra superiore. Viene visualizzata una tabella delle mappature dei set di dati.

Le colonne della tabella specificano i dettagli sulle mappature dei set di dati:

| Nome colonna | Dettagli |
| ---------------------- | ----------|
| Set di dati | Nome del set di dati. |
| Origine | L’origine del set di dati, che può essere Adobe Analytics, Experience Events, Summary (aggregato) o Consumer Experience Events. |
| Schema | Schema a cui è conforme il set di dati. Puoi selezionare rapidamente il nome dello schema per aprire lo schema in una nuova scheda nell’editor schema in Mix Modeler - Schemi. |
| Granularità | Granularità dei dati nel set di dati. I valori possibili sono Giornaliero, Settimanale, Mensile o Annuale. |
| Inizio della settimana | Specifica quale giorno della settimana viene considerato come inizio di una nuova settimana per il set di dati specifico. |
| Ultima modifica | Dati e ora dell’ultima modifica della mappatura del set di dati. |

{style="table-layout:auto"}

### Creare una mappatura del set di dati

Per creare una mappatura di set di dati, nella ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler, seleziona **[!UICONTROL Create Dataset Mapping]**.

In **[!UICONTROL Create]** schermo,

1. In entrata **[!UICONTROL Dataset Details]**, seleziona un set di dati da **[!UICONTROL Select dataset]** per iniziare la configurazione.

1. Seleziona un giorno per **[!UICONTROL Start of the week]**.

1. Seleziona **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** per **[!UICONTROL Granularity]**.

1. Dopo aver selezionato un **[!UICONTROL Summary]** tipo di set di dati:

   1. Mappa ciascuno dei **[!UICONTROL Available dataset fields]** corrispondente a **[!UICONTROL Standard harmonized fields]**. Se non desideri mappare un campo set di dati su un campo armonizzato, seleziona esplicitamente **[!UICONTROL -- None --]**.

   1. Se hai bisogno di un nuovo campo armonizzato, non disponibile dall’elenco, seleziona **[!UICONTROL Create New]** creare un nuovo campo armonizzato. La finestra di dialogo viene visualizzata come descritto in [Aggiungi un nuovo campo armonizzato](fields.md#add-a-harmonized-field) per poter aggiungere rapidamente un nuovo campo armonizzato.

   1. Una volta completata la mappatura per tutti i campi, seleziona **[!UICONTROL Save]**. Seleziona **[!UICONTROL Cancel]** per annullare la mappatura.

      ![Creare le regole del set di dati](../assets/dataset-create-summary.png)

1. Dopo aver selezionato un tipo di evento di set di dati (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), nella casella ombreggiata sottostante **[!UICONTROL Map to harmonized fields]**:

   1. Seleziona un campo armonizzato da **[!UICONTROL Standard harmonized field]**.

   1. Quando il campo armonizzato selezionato è di tipo metrica:

      1. Seleziona **[!UICONTROL Count]** o **[!UICONTROL Sum]** da **[!UICONTROL Mapping type]**.

      1. Seleziona un **[!UICONTROL *Campo set di dati AEP *]**che desideri venga mappato al campo armonizzato per impostazione predefinita.

   1. Quando il campo selezionato è di tipo dimensione:

      1. Seleziona **[!UICONTROL Map Into]** o **[!UICONTROL Case]** da **[!UICONTROL Mapping type]**.

      1. Dopo aver selezionato **[!UICONTROL Map Into]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**o **[!UICONTROL Value]**e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo del set di dati o al valore immesso.

      1. Dopo aver selezionato **[!UICONTROL Case]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**o **[!UICONTROL Value]**e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo del set di dati o al valore immesso.

         1. Inoltre, puoi definire uno o più casi, costituiti da una o più condizioni per impostare esplicitamente i valori. Ogni condizione può verificare la presenza di un **[!UICONTROL *Campo set di dati AEP *]**se **[!UICONTROL Exists]**o **[!UICONTROL Not Exists]**o se **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**, o **[!UICONTROL Ends With]**un valore immesso in corrispondenza di**[!UICONTROL * Immetti il valore di input *]**.

         1. Per aggiungere un altro caso, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, per aggiungere un&#39;altra condizione, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Per eliminare un caso o una condizione, seleziona ![Chiudi](../assets/icons/Close.svg) nel contenitore corrispondente.

         1. Per selezionare se una o tutte le condizioni devono essere applicate a un caso, seleziona **[!UICONTROL Any of]** o **[!UICONTROL All of]**.

         1. Per impostare il valore di risultato per un caso, immettere il valore in corrispondenza di **[!UICONTROL Then]**.

      L’esempio seguente

      * utilizza un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** per mappare **[!UICONTROL Channel Type At Source]** campo armonizzato al **[!UICONTROL channel_type]** campo da **[!DNL Luma Transactions]** set di dati.

      * utilizza un **[!UICONTROL Case]** **[!UICONTROL Mapping]** digita per mappare in modo condizionale il valore del **[!UICONTROL marketing.campaignName]** campo in **[!DNL Luma Transactions]** set di dati per **[!UICONTROL Campaign]** campo armonizzato. Il campo armonizzato di Campaign è impostato su:

         * `Black Friday` quando **[!UICONTROL marketing.campaignName]** è `_black_friday` o `BlackFriday`.
         * al valore del **[!UICONTROL marketing.campaignName]** in tutti gli altri casi

        ![Evento regola set di dati](../assets/dataset-create-event.png)

1. Seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** per definire campi aggiuntivi.

Al termine, seleziona **[!UICONTROL Save]** per salvare la mappatura, oppure seleziona **[!UICONTROL Cancel]** per annullare la mappatura.


### Modificare una mappatura di set di dati

Per modificare la mappatura di un set di dati, in ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** interfaccia in Mix Modeler:

1. Seleziona ![Altro](../assets/icons/More.svg) nel **[!UICONTROL Dataset]** per la mappatura del set di dati che desideri modificare.
1. Dal menu di scelta rapida, selezionare ![Modifica](../assets/icons/Edit.svg) **[!UICONTROL Edit]** per iniziare a modificare la mappatura del set di dati. Fai riferimento a [Creare una mappatura del set di dati](#create-a-dataset-mapping) per ulteriori dettagli.


### Eliminare una mappatura di set di dati

Per eliminare una mappatura di set di dati, nella ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** interfaccia in Mix Modeler:

1. Seleziona ![Altro](../assets/icons/More.svg) nel **[!UICONTROL Dataset]** per il mapping di set di dati che desideri eliminare.
1. Dal menu di scelta rapida, selezionare ![Elimina](../assets/icons/Delete.svg) **[!UICONTROL Delete]** per eliminare la mappatura del set di dati.


## Sincronizza dati

Per sincronizzare i dati tra i dati armonizzati e i set di dati di riepilogo e/o evento, segui tutte le logiche delle regole dei set di dati:

1. Seleziona **[!UICONTROL Sync data]**.

1. Dalla sezione **[!UICONTROL Sync data for dataset rules]** , seleziona una delle seguenti opzioni: **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]**, o **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Seleziona **[!UICONTROL Sync]** per avviare la sincronizzazione in base alle regole definite per i set di dati tra dati armonizzati e dati nei set di dati. Per annullare la sincronizzazione, selezionare **[!UICONTROL Cancel]**.

   ![Sincronizza dati](../assets/sync-data.png)
