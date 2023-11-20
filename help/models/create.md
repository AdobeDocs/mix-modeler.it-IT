---
title: Creare un modello
description: Scopri come creare un modello in Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 73534d1aecb6d1513f6f3b5f1801b497ad73278f
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Creare un modello

Per creare un modello, in ![Modelli](../assets/icons/FileData.svg) **[!UICONTROL Models]** in Mix Modeler, seleziona **[!UICONTROL Open model canvas]**.

Per creare modelli personalizzati basati sull’intelligenza artificiale, l’interfaccia fornisce un flusso guidato e dettagliato di configurazione del modello.

1. In **[!UICONTROL Setup]** passaggio:

   1. Inserisci il modello **[!UICONTROL Name]**, ad esempio `Demo model`. Immetti un **[!UICONTROL Description]**, ad esempio `Demo model to explore AI featues of Mix Modeler`.

      ![Nome e descrizione del modello](../assets/model-name-description.png)

   1. Seleziona **[!UICONTROL Next]** per procedere al passaggio successivo. Seleziona **[!UICONTROL Cancel]** per annullare la configurazione del modello.

1. In **[!UICONTROL Configured]** passaggio:

   1. In **[!UICONTROL Conversion goal]** all’interno del contenitore:

      1. Immetti un **[!UICONTROL Conversion name]** per la conversione, ad esempio `Conversion`

      1. Seleziona una conversione da **[!UICONTROL *Seleziona campo armonizzato *]**, contenente le conversioni disponibili definite come [Conversioni](../harmonize-data/conversions.md) in [!UICONTROL Harmonized datasets]. Ad esempio,**[!UICONTROL Online Conversion]**.

      1. Puoi selezionare ![Rispondi](../assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** per creare una conversione direttamente dalla configurazione del modello.

         ![Modello - Passaggio di conversione](../assets/model-conversion-step.png)

   1. In **[!UICONTROL Marketing touchpoints]** sezione, puoi visualizzare una serie di contenitori di punti di contatto di marketing, corrispondenti ai punti di contatto di marketing definiti come parte [Punti di contatto di marketing](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets].

      * Per ciascun contenitore:

         1. È possibile modificare **[!UICONTROL Marketing touchpoint name]**.

         1. Seleziona un punto di contatto di marketing da **[!UICONTROL _Seleziona punto di contatto di marketing_]**.

         1. Puoi selezionare ![Rispondi](../assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** per creare un punto di contatto di marketing direttamente dalla configurazione del modello.

      * Per aggiungere un contenitore per punti di contatto di marketing, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Per rimuovere un contenitore punto di contatto marketing, all’interno del contenitore, seleziona ![Altro](../assets/icons/More.svg), e seleziona **[!UICONTROL Remove container]** dal menu di scelta rapida.

        ![Modello - punti di contatto di marketing-passaggio](../assets/model-marketing-touchpoint-step.png)

   1. Per impostazione predefinita, viene generato un punteggio per tutti i dati nella vista armonizzata. Per valutare solo un sottoinsieme della popolazione, definisci uno o più filtri utilizzando i contenitori in **[!UICONTROL Eligible data population]** sezione.

      * Per ogni contenitore, definisci uno o più eventi.

         1. Per ogni evento:

            1. Seleziona una metrica o dimensione da **[!UICONTROL _Seleziona campo armonizzato_]**.

            1. Seleziona l’operatore appropriato: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]**, o **[!UICONTROL is not in]**.

            1. Inserisci o seleziona un valore in **[!UICONTROL _Inserisci o seleziona il valore_]**.

         1. Per aggiungere un evento aggiuntivo al contenitore, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Per rimuovere un evento dal contenitore, seleziona ![Chiudi](../assets/icons/Close.svg).

         1. Per filtrare utilizzando tutti o uno qualsiasi dei più eventi definiti nel contenitore, seleziona **[!UICONTROL Any of]** o **[!UICONTROL All of]**. L’etichetta cambia di conseguenza da **[!UICONTROL Include ... Or ...]** a **[!UICONTROL Include ... And ...]**.

      * Per aggiungere un contenitore per la popolazione di dati idonea, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Per rimuovere un contenitore di popolazione dati idoneo, all’interno del contenitore, seleziona ![Altro](../assets/icons/More.svg), e seleziona **[!UICONTROL Remove container]** dal menu di scelta rapida.

        ![Modello - Popolazione dei dati idonea](../assets/model-eligible-data-population-step.png)

   1. Per aggiungere al modello set di dati contenenti fattori esterni, utilizza uno o più contenitori in **[!UICONTROL External factors dataset]** sezione.

      * Per ciascun contenitore:

         1. Immetti un **[!UICONTROL Factor name]** a **[!UICONTROL _Immetti il fattore_]**.

         1. Seleziona un set di dati da **[!UICONTROL _Seleziona un set di dati_]**. Puoi selezionare ![Dati](../assets/icons/Data.svg) per gestire i set di dati. Consulta [Set di dati](../ingest-data/datasets.md) per ulteriori informazioni.

      * Per aggiungere un contenitore di set di dati di fattori esterni aggiuntivi, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Per rimuovere un contenitore di set di dati di fattori esterni, all’interno del contenitore, seleziona ![Altro](../assets/icons/More.svg), e seleziona **[!UICONTROL Remove container]** dal menu di scelta rapida.

        ![Modello: set di dati di fattori esterni](../assets/model-external-factors-dataset-step.png)


   1. Per aggiungere al modello set di dati contenenti fattori interni, utilizza uno o più contenitori in **[!UICONTROL Internal factors dataset]** sezione.

      * Per ciascun contenitore:

         1. Immetti un **[!UICONTROL Factor name]** a **[!UICONTROL _Immetti il fattore_]**.

         1. Seleziona un set di dati da **[!UICONTROL _Seleziona un set di dati_]**. Puoi selezionare ![Dati](../assets/icons/Data.svg) per gestire i set di dati. Consulta [Set di dati](../ingest-data/datasets.md) per ulteriori informazioni.

      * Per aggiungere un contenitore di set di dati di fattori interni aggiuntivo, seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Per rimuovere un contenitore di set di dati di fattori interni aggiuntivi, all’interno del contenitore, seleziona ![Altro](../assets/icons/More.svg), e **[!UICONTROL Remove container]** dal menu di scelta rapida.

        ![Modello: set di dati di fattori interni](../assets/model-internal-factors-dataset-step.png)

   1. Per definire l’intervallo di lookback per il modello, inserisci un valore compreso tra `1` e `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

   1. Seleziona **[!UICONTROL Next]** per procedere al passaggio successivo. Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria. <br/>Seleziona **[!UICONTROL Back]** per tornare al passaggio precedente. <br/>Seleziona **[!UICONTROL Cancel]** per annullare la configurazione del modello.

1. In **[!UICONTROL Advanced]** passaggio:

   1. In **[!UICONTROL Define training window]** sezione, seleziona tra

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** e

      * **[!UICONTROL Manually input a training window]**. Se selezionata, definisci il numero di anni in **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modello: definire la finestra di formazione](../assets/model-define-training-window.png)

   1. In **[!UICONTROL Spend share]** sezione:

      * Per utilizzare i rapporti di investimento di marketing storici per informare il modello quando i dati di marketing sono sparsi, attiva **[!UICONTROL Allow spend share]**.

   1. In **[!UICONTROL Prior knowledge]** sezione:

      1. Seleziona **[!UICONTROL Rule type]**.

      1. Specifica le percentuali di contributo per uno dei canali elencati in **[!UICONTROL Name]**, utilizzando **[!UICONTROL Contribution proportion]** colonna.

      1. Se necessario, puoi aggiungere per ogni canale una **[!UICONTROL Level of confidence]** percentuale.

      1. Quando necessario, utilizza **[!UICONTROL Clear all]** per cancellare tutti i valori di input per **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]** colonne.

         ![Modello - Conoscenze precedenti](../assets/model-prior-knowledge-step.png)

1. Seleziona **[!UICONTROL Finish]** per completare la configurazione del modello.

   * In **[!UICONTROL Create instance?]** finestra di dialogo, seleziona **[!UICONTROL Ok]** per attivare immediatamente il primo set di addestramento e punteggio. Il modello è elencato con lo stato <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**.

     Seleziona **[!UICONTROL Cancel]** per annullare.

   * Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria.

   Seleziona **[!UICONTROL Back]** per tornare al passaggio precedente.

   Seleziona **[!UICONTROL Cancel]** per annullare la configurazione del modello.
