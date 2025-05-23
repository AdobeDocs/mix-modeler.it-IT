---
title: Regole del set di dati
description: Scopri come definire le regole del set di dati da utilizzare come parte dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a8590d604f79268bc8d1f012f2c19271a3b38668
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 0%

---

# Regole del set di dati

Le regole del set di dati ti aiutano a mappare i campi armonizzati con i campi dei dati acquisiti in Mix Modeler.

* Per i dati aggregati acquisiti in Adobe Experience Platform, mappi uno o più campi del set di dati disponibili ai campi armonizzati appropriati.
* Per i dati evento, puoi mappare singolarmente uno o più campi armonizzati ai campi del set di dati, direttamente o utilizzando le condizioni.


## Gestire le regole dei set di dati

Per visualizzare una tabella delle regole dei set di dati disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Dataset rules]** dalla barra superiore. Viene visualizzata una tabella delle regole del set di dati.

Le colonne della tabella specificano i dettagli sulle regole del set di dati:

| Nome colonna | Dettagli |
| ---------------------- | ----------|
| Set di dati | Nome del set di dati. |
| Origine | L’origine del set di dati: Adobe Analytics, Eventi esperienza, Riepilogo (aggregato) o Eventi esperienza del consumatore. |
| Schema | Schema a cui è conforme il set di dati. È possibile selezionare rapidamente il nome dello schema per aprire lo schema in una nuova scheda nell&#39;editor schema in ![Schema](/help/assets/icons/Schemas.svg) [Schemi](../ingest-data/schemas.md). |
| Granularità | Granularità dei dati nel set di dati. I valori possibili sono Giornaliero, Settimanale, Mensile o Annuale. |
| Inizio della settimana | Specifica quale giorno della settimana viene considerato come inizio di una nuova settimana per il set di dati specifico. |
| Stato | Stato del campo: <p><span style="color:gray">●</span> bozza o <p><span style="color:green">●</span> attivo |
| Ultima modifica | Dati e ora dell’ultima modifica della regola del set di dati. |

{style="table-layout:auto"}

### Creare una regola del set di dati

Per creare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler, selezionare **[!UICONTROL Create a dataset rule]** nella procedura guidata **[!UICONTROL Dataset rules configuration]**.

Nella schermata **[!UICONTROL Create]**,

1. In **[!UICONTROL Dataset details]**, selezionare un set di dati da **[!UICONTROL Select dataset]** per iniziare la configurazione. Nell&#39;elenco, i set di dati sono classificati in **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** e **[!UICONTROL Summary]**.

1. Selezionare un giorno per **[!UICONTROL Start of the week]**.

1. Selezionare **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** per **[!UICONTROL Granularity]**.

1. Dopo aver selezionato un set di dati della categoria **[!UICONTROL Summary]**:

   1. Per definire se i dati per il set di dati aggregano o sostituiscono i dati esistenti, selezionare **[!UICONTROL Aggregation]** o **[!UICONTROL Replacement]** per **[!UICONTROL Data restatement is by]**.

   1. Mappare ciascuno dei **[!UICONTROL Available dataset fields]** ai **[!UICONTROL Standard harmonized fields]** corrispondenti in **[!UICONTROL Map to harmonized fields]**. Se non desideri mappare un campo set di dati a un campo armonizzato, seleziona esplicitamente **[!UICONTROL -- None --]**.

   1. Se è necessario un nuovo campo armonizzato, non disponibile nell&#39;elenco, selezionare **[!UICONTROL Create New]** per creare un nuovo campo armonizzato. La finestra di dialogo viene visualizzata come descritto in [Aggiungi un nuovo campo armonizzato](fields.md#add-a-harmonized-field).

   1. Una volta completata la mappatura per tutti i campi della regola, selezionare **[!UICONTROL Save as draft]** per salvare una bozza della regola o **[!UICONTROL Save]** per salvare e attivare la regola. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione della regola.

      ![Crea regole set di dati](/help/assets/dataset-create-summary.png)

1. Dopo aver selezionato un set di dati categoria eventi (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), nella casella sottostante **[!UICONTROL Map to harmonized fields]**:

   1. Selezionare un campo armonizzato da **[!UICONTROL Standard harmonized field]**.

   1. Quando il campo armonizzato selezionato è di tipo metrica:

      1. Selezionare **[!UICONTROL Count]** o **[!UICONTROL Sum]** da **[!UICONTROL Mapping type]**.

      1. Selezionare un **[!UICONTROL *campo set di dati AEP *]**&#x200B;a cui si desidera mappare il campo armonizzato per impostazione predefinita.

   1. Quando il campo selezionato è di tipo dimensione:

      1. Selezionare **[!UICONTROL Map Into]** o **[!UICONTROL Case]** da **[!UICONTROL Mapping type]**.

      1. Dopo aver selezionato **[!UICONTROL Map Into]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**&#x200B;o **[!UICONTROL Value]**&#x200B;e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo set di dati o al valore immesso.

      1. Quando selezioni **[!UICONTROL Case]**, seleziona **[!UICONTROL Field]** e **[!UICONTROL *Campo set di dati AEP *]**&#x200B;o **[!UICONTROL Value]**&#x200B;e un valore predefinito per mappare il campo armonizzato per impostazione predefinita al campo set di dati o al valore immesso.

         1. Per impostare i valori in modo esplicito, definite uno o più casi, costituiti da una o più condizioni. Ogni condizione può verificare la presenza di un campo del set di dati **[!UICONTROL *AEP *]**&#x200B;specifico, che si tratti di **[!UICONTROL Exists]**&#x200B;o **[!UICONTROL Not Exists]**&#x200B;oppure di **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;o **[!UICONTROL Ends With]**, un valore immesso in&#x200B;**[!UICONTROL * Immettere il valore di input *]**.

         1. Per aggiungere un altro caso, selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, per aggiungere un&#39;altra condizione, selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Per eliminare un caso o una condizione, selezionare ![Chiudi](/help/assets/icons/Close.svg) nel contenitore corrispondente.

         1. Per specificare se devono essere applicate le condizioni di un caso o tutte, selezionare **[!UICONTROL Any of]** o **[!UICONTROL All of]**.

         1. Per impostare il valore del risultato per un caso, immettere il valore in **[!UICONTROL Then]**.

      L’esempio seguente

      * utilizza un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** per mappare il campo armonizzato **[!UICONTROL Channel Type At Source]** al campo **[!UICONTROL channel_type]** dal set di dati **[!DNL Luma Transactions]**.

      * utilizza un **[!UICONTROL Case]** **[!UICONTROL Mapping type]** per mappare in modo condizionale il valore del campo **[!UICONTROL marketing.campaignName]** nel set di dati **[!DNL Luma Transactions]** al campo armonizzato **[!UICONTROL Campaign]**. Il campo armonizzato di Campaign è impostato su:

         * `Black Friday` quando **[!UICONTROL marketing.campaignName]** è `_black_friday` o `BlackFriday`.
         * al valore di **[!UICONTROL marketing.campaignName]** in tutti gli altri casi.

        ![Evento regola set di dati](/help/assets/dataset-create-event.png)

1. Seleziona ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** per definire campi aggiuntivi.

Al termine, selezionare **[!UICONTROL Save as draft]** per salvare una bozza della regola o **[!UICONTROL Save]** per salvare e attivare la regola. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione della regola.


### Modificare una regola del set di dati

Per modificare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler:

1. Seleziona ![Altro](/help/assets/icons/More.svg) nella colonna **[!UICONTROL Dataset]** per la regola del set di dati da modificare.
1. Dal menu di scelta rapida, seleziona ![Modifica](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** per iniziare a modificare la regola del set di dati. Per ulteriori dettagli, consulta [Creare una regola del set di dati](#create-a-dataset-rule).


### Eliminare una regola di set di dati

Per eliminare una regola del set di dati, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** in Mix Modeler:

1. Seleziona ![Altro](/help/assets/icons/More.svg) nella colonna **[!UICONTROL Dataset]** per la regola del set di dati da eliminare.
1. Dal menu di scelta rapida, selezionare ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** per eliminare la regola del set di dati. Viene richiesta una conferma. Selezionare **[!UICONTROL Delete]** per eliminare definitivamente la regola del set di dati selezionato.


## Sincronizza dati

Per sincronizzare i dati tra i dati armonizzati e i set di dati di riepilogo e/o evento durante l’applicazione della logica nelle regole dei set di dati:

1. Seleziona **[!UICONTROL Sync data]**.

1. Dalla finestra di dialogo **[!UICONTROL Sync data for dataset rules]**, seleziona
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, oppure
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Per avviare la sincronizzazione in base alle regole definite per il set di dati tra dati armonizzati e dati nei set di dati, selezionare **[!UICONTROL Sync]**. Per annullare la sincronizzazione, selezionare **[!UICONTROL Cancel]**.

   ![Sincronizza dati](/help/assets/sync-data.png)


## Preferenze di unione dati

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

Per garantire previsioni accurate dei modelli, puoi definire le preferenze di unione dei dati. Questa funzionalità consente agli utenti di risolvere eventuali conflitti dopo l’unione di dati a livello di riepilogo e di evento.

Puoi configurare una preferenza metrica predefinita da applicare in caso di aggiornamenti in conflitto. Questa metrica predefinita può essere una delle tre opzioni seguenti:

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Quando, durante l’armonizzazione, più origini di dati tentano di aggiornare un campo metrico per un dato canale, viene applicata la preferenza predefinita configurata dall’utente. Questa preferenza viene applicata a livello di sandbox, a meno che non venga bypassata per alcune preferenze basate su metriche configurate in aggiunta.

In **[!UICONTROL Metric based preferences]**, l&#39;utente può configurare l&#39;origine specifica (**[!UICONTROL Summary]** o **[!UICONTROL Event]**) per una metrica specifica e il tipo di conversione corrispondente per tale metrica.

I casi d’uso tipici sono:

* la stessa metrica pubblicitaria è misurata e segnalata in più set di dati, oppure
* la misurazione delle metriche può essere incompleta in alcuni set di dati, mentre un altro set di dati può essere un superset di una particolare metrica, con conseguente doppio conteggio.

### Configura

Per configurare le preferenze di unione dati:


1. Seleziona ![Preferenze unione dati](/help/assets/icons/Merge.svg) [!BADGE beta].

1. In **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}

   ![Preferenze di unione dati](/help/assets/data-merge-preferences.png)

   * Seleziona **[!UICONTROL Default metric preference]**. La preferenza metrica predefinita selezionata viene applicata quando, durante l’armonizzazione, più origini di dati aggiornano un campo metrico per un determinato canale. La preferenza viene applicata a livello di sandbox, a meno che non venga bypassata per specifiche preferenze basate su metriche. È possibile selezionare tra **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** e **[!UICONTROL Sum of summary and event data]**.

   * Per aggiungere preferenze specifiche basate su metriche:

      1. Seleziona ![Più](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Selezionare una metrica dall&#39;elenco **[!UICONTROL *Selezione metrica *]**.
         1. Selezionare **[!UICONTROL CHANNELS]** o **[!UICONTROL CONVERSION TYPES]**. Dall&#39;elenco, selezionare **[!UICONTROL All]** o un canale o un tipo di conversione specifico.
         1. Selezionare **[!UICONTROL Summary]** o **[!UICONTROL Event]** per specificare se i dati di riepilogo o i dati evento sono preferiti per la metrica (e per tutti o per il canale selezionato) durante l&#39;unione dei dati.

         Per aggiungere uno o più tipi di canale o conversione aggiuntivi:

         1. Seleziona ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** o ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Seleziona **[!UICONTROL Summary]** (Mostra origine dati) o **[!UICONTROL Event]** (Blocca selezione).

         Per eliminare un tipo di canale o conversione, selezionare ![Cross](/help/assets/icons/Close.svg).

      1. Per aggiungere preferenze più specifiche basate su metriche, ripeti il passaggio precedente.

   * Per eliminare una specifica preferenza basata su metriche esistente, selezionare ![Elimina](/help/assets/icons/Delete.svg).

1. Selezionare **[!UICONTROL Save]** per salvare le preferenze di unione dati. È stata avviata una risincronizzazione dei dati. <br/>Selezionare **[!UICONTROL Cancel]** per annullare.

## Eliminare un set di dati di origine

Quando si elimina un set di dati di origine utilizzato nei dati armonizzati, le voci sottostanti in tale set di dati di origine vengono rimosse da [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). Tuttavia, la regola del set di dati con il set di dati di origine eliminato rimane nell&#39;elenco di configurazione delle regole del set di dati con un&#39;icona ![DataRemove](/help/assets/icons/DataRemove.svg) che indica che il set di dati di origine è stato eliminato. Per maggiori dettagli:

* Selezionare ![Altro](/help/assets/icons/More.svg) e ![Anteprima](/help/assets/icons/Preview.svg) **[!UICONTROL View]** dal menu di scelta rapida.
La finestra di dialogo **[!UICONTROL Dataset rule mapping - Fields]** visualizza informazioni sul set di dati di origine eliminato e sui campi utilizzati nella configurazione della regola del set di dati.

Quando si torna alla configurazione **[!UICONTROL Dataset rules]**, viene visualizzata una finestra di dialogo in cui viene spiegato che uno o più set di dati di origine sono stati eliminati. I dati armonizzati sono interessati da una prossima sincronizzazione ad hoc o pianificata. Verifica la configurazione delle regole del set di dati.

I dati armonizzati vengono aggiornati senza i dati di origine eliminati alla successiva sincronizzazione ad hoc o pianificata. Tuttavia, continuerai a visualizzare le finestre di dialogo degli avvisi che ti richiedono di eliminare la regola del set di dati in base al set di dati di origine eliminato. Questo avviso consente agli utenti di visualizzare e valutare i campi interessati nel set di dati eliminato. E per determinare l’impatto sui punti di contatto di marketing o sulle conversioni che possono essere utilizzati in qualsiasi modello. Dopo aver valutato e attenuato questo impatto, devi eliminare la regola del set di dati dall’elenco di configurazione delle regole del set di dati.
