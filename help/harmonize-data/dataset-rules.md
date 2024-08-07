---
title: Regole del set di dati
description: Scopri come definire le regole del set di dati da utilizzare come parte dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# Regole del set di dati

Le regole del set di dati ti aiutano a mappare i campi armonizzati con i campi dei dati acquisiti in Mix Modeler.

* Per i dati aggregati acquisiti in Adobe Experience Platform, mappi uno o più campi del set di dati disponibili ai campi armonizzati appropriati.
* Per i dati evento, puoi mappare singolarmente uno o più campi armonizzati ai campi del set di dati, direttamente o utilizzando le condizioni.


## Gestire le regole dei set di dati

Per visualizzare una tabella delle regole dei set di dati disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Dataset rules]** dalla barra superiore. Viene visualizzata una tabella delle regole del set di dati.

Le colonne della tabella specificano i dettagli sulle regole del set di dati:

| Nome colonna | Dettagli |
| ---------------------- | ----------|
| Set di dati | Nome del set di dati. |
| Origine | L’origine del set di dati: Adobe Analytics, Eventi esperienza, Riepilogo (aggregato) o Eventi esperienza del consumatore. |
| Schema | Schema a cui è conforme il set di dati. È possibile selezionare rapidamente il nome dello schema per aprire lo schema in una nuova scheda nell&#39;editor schema in ![Schema](/help/assets//icons/Schemas.svg) [Schemi](../ingest-data/schemas.md). |
| Granularità | Granularità dei dati nel set di dati. I valori possibili sono Giornaliero, Settimanale, Mensile o Annuale. |
| Inizio della settimana | Specifica quale giorno della settimana viene considerato come inizio di una nuova settimana per il set di dati specifico. |
| Stato | Stato del campo: <p><span style="color:gray">●</span> bozza o <p><span style="color:green">●</span> attivo |
| Ultima modifica | Dati e ora dell’ultima modifica della regola del set di dati. |

{style="table-layout:auto"}

### Creare una regola del set di dati

Per creare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler, selezionare **[!UICONTROL Create a dataset rule]** nella procedura guidata **[!UICONTROL Dataset rules configuration]**.

Nella schermata **[!UICONTROL Create]**,

1. In **[!UICONTROL Dataset details]**, selezionare un set di dati da **[!UICONTROL Select dataset]** per iniziare la configurazione. Nell&#39;elenco, i set di dati sono classificati in **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** e **[!UICONTROL Summary]**.

1. Selezionare un giorno per **[!UICONTROL Start of the week]**.

1. Selezionare **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** per **[!UICONTROL Granularity]**.

1. Dopo aver selezionato un set di dati della categoria **[!UICONTROL Summary]**:

   1. Per definire se i dati per il set di dati aggregano o sostituiscono i dati esistenti, selezionare **[!UICONTROL Aggregation]** o **[!UICONTROL Replacement]** per **[!UICONTROL Data restatement is by]**.

   1. Mappare ciascuno dei **[!UICONTROL Available dataset fields]** ai **[!UICONTROL Standard harmonized fields]** corrispondenti in **[!UICONTROL Map to harmonized fields]**. Se non desideri mappare un campo set di dati a un campo armonizzato, seleziona esplicitamente **[!UICONTROL -- None --]**.

   1. Se è necessario un nuovo campo armonizzato, non disponibile nell&#39;elenco, selezionare **[!UICONTROL Create New]** per creare un nuovo campo armonizzato. La finestra di dialogo viene visualizzata come descritto in [Aggiungi un nuovo campo armonizzato](fields.md#add-a-harmonized-field).

   1. Una volta completata la mappatura per tutti i campi della regola, selezionare **[!UICONTROL Save as draft]** per salvare una bozza della regola o **[!UICONTROL Save]** per salvare e attivare la regola. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione della regola.

      ![Crea regole set di dati](/help/assets//dataset-create-summary.png)

1. Dopo aver selezionato un set di dati categoria eventi (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), nella casella sottostante **[!UICONTROL Map to harmonized fields]**:

   1. Selezionare un campo armonizzato da **[!UICONTROL Standard harmonized field]**.

   1. Quando il campo armonizzato selezionato è di tipo metrica:

      1. Selezionare **[!UICONTROL Count]** o **[!UICONTROL Sum]** da **[!UICONTROL Mapping type]**.

      1. Selezionare un **[!UICONTROL *campo set di dati AEP *]**a cui si desidera mappare il campo armonizzato per impostazione predefinita.

   1. Quando il campo selezionato è di tipo dimensione:

      1. Selezionare **[!UICONTROL Map Into]** o **[!UICONTROL Case]** da **[!UICONTROL Mapping type]**.

      1. Dopo aver selezionato **[!UICONTROL Map Into]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**o **[!UICONTROL Value]**e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo set di dati o al valore immesso.

      1. Quando selezioni **[!UICONTROL Case]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**o **[!UICONTROL Value]**e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo set di dati o al valore immesso.

         1. Per impostare i valori in modo esplicito, definite uno o più casi, costituiti da una o più condizioni. Ogni condizione può verificare la presenza di un campo del set di dati **[!UICONTROL *AEP *]**specifico, che si tratti di **[!UICONTROL Exists]**o **[!UICONTROL Not Exists]**oppure di **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**o **[!UICONTROL Ends With]**, un valore immesso in**[!UICONTROL * Immettere il valore di input *]**.

         1. Per aggiungere un altro caso, selezionare ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add case]**, per aggiungere un&#39;altra condizione, selezionare ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Per eliminare un caso o una condizione, selezionare ![Chiudi](/help/assets//icons/Close.svg) nel contenitore corrispondente.

         1. Per selezionare se una o tutte le condizioni devono essere applicate a un caso, selezionare **[!UICONTROL Any of]** o **[!UICONTROL All of]**.

         1. Per impostare il valore del risultato per un caso, immettere il valore in **[!UICONTROL Then]**.

      L’esempio seguente

      * utilizza un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** per mappare il campo armonizzato **[!UICONTROL Channel Type At Source]** al campo **[!UICONTROL channel_type]** dal set di dati **[!DNL Luma Transactions]**.

      * utilizza un **[!UICONTROL Case]** **[!UICONTROL Mapping type]** per mappare in modo condizionale il valore del campo **[!UICONTROL marketing.campaignName]** nel set di dati **[!DNL Luma Transactions]** al campo armonizzato **[!UICONTROL Campaign]**. Il campo armonizzato di Campaign è impostato su:

         * `Black Friday` quando **[!UICONTROL marketing.campaignName]** è `_black_friday` o `BlackFriday`.
         * al valore di **[!UICONTROL marketing.campaignName]** in tutti gli altri casi.

        ![Evento regola set di dati](/help/assets//dataset-create-event.png)

1. Seleziona ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]** per definire campi aggiuntivi.

Al termine, selezionare **[!UICONTROL Save as draft]** per salvare una bozza della regola o **[!UICONTROL Save]** per salvare e attivare la regola. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione della regola.


### Modificare una regola del set di dati

Per modificare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler:

1. Seleziona ![Altro](/help/assets//icons/More.svg) nella colonna **[!UICONTROL Dataset]** per la regola del set di dati da modificare.
1. Dal menu di scelta rapida, seleziona ![Modifica](/help/assets//icons/Edit.svg) **[!UICONTROL Edit]** per iniziare a modificare la regola del set di dati. Per ulteriori dettagli, consulta [Creare una regola del set di dati](#create-a-dataset-rule).


### Eliminare una regola di set di dati

Per eliminare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler:

1. Seleziona ![Altro](/help/assets//icons/More.svg) nella colonna **[!UICONTROL Dataset]** per la regola del set di dati da eliminare.
1. Dal menu di scelta rapida, selezionare ![Elimina](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** per eliminare la regola del set di dati. Viene richiesta una conferma. Selezionare **[!UICONTROL Delete]** per eliminare definitivamente la regola del set di dati selezionato.


## Sincronizza dati

Per sincronizzare i dati tra i dati armonizzati e i set di dati di riepilogo e/o evento, segui tutte le logiche delle regole dei set di dati:

1. Seleziona **[!UICONTROL Sync data]**.

1. Dalla finestra di dialogo **[!UICONTROL Sync data for dataset rules]**, seleziona
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, oppure
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Per avviare la sincronizzazione in base alle regole definite per il set di dati tra dati armonizzati e dati nei set di dati, selezionare **[!UICONTROL Sync]**. Per annullare la sincronizzazione, selezionare **[!UICONTROL Cancel]**.

   ![Sincronizza dati](/help/assets//sync-data.png)


## Preferenze di unione dati

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

Le preferenze di unione dati consentono di risolvere i conflitti quando si uniscono dati provenienti da origini dati riepilogate ed eventi. I casi di utilizzo sono:

* la stessa metrica pubblicitaria è misurata e segnalata in più set di dati, oppure
* la misurazione delle metriche può essere incompleta in alcuni set di dati, mentre un altro set di dati può essere un superset di una particolare metrica, con conseguente doppio conteggio.

Per garantire previsioni accurate dei modelli, puoi definire le preferenze di unione dei dati:

1. Seleziona ![Preferenze unione dati](/help/assets//icons/Merge.svg) [!BADGE beta].

1. In **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}

   ![Preferenze di unione dati](/help/assets//data-merge-preferences.png)

   * Seleziona **[!UICONTROL Default metric preference]**. La preferenza metrica predefinita selezionata viene applicata quando, durante l’armonizzazione, più origini di dati aggiornano un campo metrico per un determinato canale. La preferenza viene applicata a livello di sandbox, a meno che non venga bypassata per specifiche preferenze basate su metriche. È possibile selezionare tra **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** e **[!UICONTROL Sum of summmary and event data]**.

   * Per aggiungere preferenze specifiche basate su metriche:

      1. Seleziona ![Più](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Selezionare una metrica dall&#39;elenco **[!UICONTROL *Selezione metrica *]**.
         1. Selezionare **[!UICONTROL CHANNELS]** o **[!UICONTROL CONVERSION TYPES]**. Dall&#39;elenco, selezionare **[!UICONTROL All]** o un canale o un tipo di conversione specifico.
         1. Selezionare **[!UICONTROL Summary]** o **[!UICONTROL Event]** per specificare se i dati di riepilogo o i dati evento sono preferiti per la metrica (e per tutti o per il canale selezionato) durante l&#39;unione dei dati.

         Per aggiungere uno o più tipi di canale o conversione aggiuntivi:

         1. Seleziona ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a channel]** o ![Plus](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Seleziona **[!UICONTROL Summary]** (Mostra origine dati) o **[!UICONTROL Event]** (Blocca selezione).

         Per eliminare un tipo di canale o conversione, selezionare ![Cross](/help/assets//icons/Close.svg).

      1. Per aggiungere preferenze più specifiche basate su metriche, ripeti il passaggio precedente.

   * Per eliminare una specifica preferenza basata su metriche esistente, selezionare ![Elimina](/help/assets//icons/Delete.svg).

1. Selezionare **[!UICONTROL Save]** per salvare le preferenze di unione dati. È stata avviata una risincronizzazione dei dati. <br/>Selezionare **[!UICONTROL Cancel]** per annullare.


## Controllo dell’accesso a livello di campo

Durante la configurazione delle regole del set di dati per i set di dati armonizzati, il controllo dell&#39;accesso basato sull&#39;attributo [di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) viene applicato a livello di campo. Un campo è limitato quando un’etichetta viene associata a un campo schema e viene abilitato un criterio attivo che nega l’accesso a tale campo. Di conseguenza:

* quando crei una regola di set di dati, non vengono visualizzati i campi dello schema con restrizioni,
* non puoi visualizzare o modificare la mappatura di uno o più campi dello schema per i quali esistono restrizioni. Quando modifichi o visualizzi una regola del set di dati contenente tali campi con restrizioni, viene visualizzata la schermata seguente.
  ![Azione non consentita](/help/assets//action-not-permitted.png)
