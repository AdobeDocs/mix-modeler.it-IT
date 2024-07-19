---
title: Creare un modello
description: Scopri come creare un modello in Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Creare un modello

Per creare un modello, nell&#39;interfaccia ![Models](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** in Mix Modeler, selezionare **[!UICONTROL Open model canvas]**.

Per creare modelli personalizzati basati sull’intelligenza artificiale, l’interfaccia fornisce un flusso guidato e dettagliato di configurazione del modello.

1. Nel passaggio **[!UICONTROL Setup]**:

   1. Immettere il modello **[!UICONTROL Name]**, ad esempio `Demo model`. Immettere un **[!UICONTROL Description]**, ad esempio `Demo model to explore AI featues of Mix Modeler`.

      ![Nome modello e descrizione](/help/assets//model-name-description.png)

   1. Selezionare **[!UICONTROL Next]** per continuare con il passaggio successivo. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.

1. Nel passaggio **[!UICONTROL Configure]**:

   1. Nella sezione **[!UICONTROL Conversion goal]**, all&#39;interno del contenitore:

      1. Immetti **[!UICONTROL Conversion name]** per la conversione, ad esempio `Conversion`

      1. Seleziona una conversione da **[!UICONTROL *Seleziona campo armonizzato *]**, contenente le conversioni disponibili definite come parte di [Conversioni](../harmonize-data/conversions.md) in [!UICONTROL Harmonized datasets]. Ad esempio,**[!UICONTROL Online Conversion]**.

      1. È possibile selezionare ![Risposta](/help/assets//icons/Reply.svg) **[!UICONTROL Create new conversion]** per creare una conversione direttamente dalla configurazione del modello.

         ![Modello - passaggio conversione](/help/assets//model-conversion-step.png)

   1. Nella sezione **[!UICONTROL Marketing touchpoints]** sono presenti alcuni contenitori di punti di contatto di marketing, corrispondenti ai punti di contatto di marketing definiti come parte di [punti di contatto di marketing](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets].

      * Per ciascun contenitore:

         1. È possibile modificare **[!UICONTROL Marketing touchpoint name]**.

         1. Seleziona un punto di contatto marketing da **[!UICONTROL _Seleziona punto di contatto marketing_]**.

         1. Puoi selezionare ![Rispondi](/help/assets//icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** per creare un punto di contatto di marketing direttamente dalla configurazione del modello.

      * Per aggiungere un contenitore punto di contatto marketing, seleziona ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Per rimuovere un contenitore punto di contatto marketing, all&#39;interno del contenitore, seleziona ![Altro](/help/assets//icons/More.svg) e seleziona **[!UICONTROL Remove container]** dal menu di scelta rapida.

        ![Modello - punti di contatto marketing-passaggio](/help/assets//model-marketing-touchpoint-step.png)

   1. Per impostazione predefinita, viene generato un punteggio per tutti i dati nella vista armonizzata. Per valutare solo un sottoinsieme della popolazione, definire uno o più filtri utilizzando i contenitori nella sezione **[!UICONTROL Eligible data population]**.

      * Per ogni contenitore, definisci uno o più eventi.

         1. Per ogni evento:

            1. Seleziona una metrica o dimensione da **[!UICONTROL _Seleziona campo armonizzato_]**.

            1. Selezionare l&#39;operatore appropriato: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** o **[!UICONTROL is not in]**.

            1. Immettere o selezionare un valore in **[!UICONTROL _Immettere o selezionare il valore_]**.

         1. Per aggiungere un altro evento nel contenitore, selezionare ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Per rimuovere un evento dal contenitore, selezionare ![Chiudi](/help/assets//icons/Close.svg).

         1. Per filtrare utilizzando tutti o uno qualsiasi dei più eventi definiti nel contenitore, selezionare **[!UICONTROL Any of]** o **[!UICONTROL All of]**. L&#39;etichetta cambia di conseguenza da **[!UICONTROL Include ... Or ...]** a **[!UICONTROL Include ... And ...]**.

      * Per aggiungere un contenitore di popolazione dati idoneo, selezionare ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Per rimuovere un contenitore del gruppo di dati idoneo, all&#39;interno del contenitore, selezionare ![Altro](/help/assets//icons/More.svg) e selezionare **[!UICONTROL Remove marketing touchpoint]** dal menu di scelta rapida.

        ![Modello - Popolazione dati idonea](/help/assets//model-eligible-data-population-step.png)

   1. Per aggiungere al modello set di dati contenenti fattori esterni, utilizzare uno o più contenitori nella sezione **[!UICONTROL External factors dataset]**.

      * Per ciascun contenitore:

         1. Immettere **[!UICONTROL Factor name]** in **[!UICONTROL _Immettere il fattore_]**.

         1. Seleziona un set di dati da **[!UICONTROL _Seleziona un set di dati_]**. Puoi selezionare ![Dati](/help/assets//icons/Data.svg) per gestire i set di dati. Per ulteriori informazioni, vedere [Set di dati](../ingest-data/datasets.md).

      * Per aggiungere un contenitore di set di dati di fattori esterni aggiuntivi, seleziona ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Per rimuovere un contenitore di set di dati di fattori esterni, all&#39;interno del contenitore, selezionare ![Altro](/help/assets//icons/More.svg) e selezionare **[!UICONTROL Remove external factor]** dal menu di scelta rapida.

        ![Modello - Set di dati fattori esterni](/help/assets//model-external-factors-dataset-step.png)


   1. Per aggiungere set di dati contenenti fattori interni al modello, utilizzare uno o più contenitori nella sezione **[!UICONTROL Internal factors dataset]**.

      * Per ciascun contenitore:

         1. Immettere **[!UICONTROL Factor name]** in **[!UICONTROL _Immettere il fattore_]**.

         1. Seleziona un set di dati da **[!UICONTROL _Seleziona un set di dati_]**. Puoi selezionare ![Dati](/help/assets//icons/Data.svg) per gestire i set di dati. Per ulteriori informazioni, vedere [Set di dati](../ingest-data/datasets.md).

      * Per aggiungere un contenitore di set di dati di fattori interni aggiuntivi, seleziona ![Aggiungi](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Per rimuovere un contenitore di set di dati di fattori interni aggiuntivi, all&#39;interno del contenitore, selezionare ![Altro](/help/assets//icons/More.svg) e **[!UICONTROL Remove internal factor]** dal menu di scelta rapida.

        ![Modello - Set di dati fattori interni](/help/assets//model-internal-factors-dataset-step.png)

   1. Per definire l&#39;intervallo di lookback per il modello, immettere un valore compreso tra `1` e `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

   1. Selezionare **[!UICONTROL Next]** per continuare con il passaggio successivo. Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria. <br/>Selezionare **[!UICONTROL Back]** per tornare al passaggio precedente. <br/>Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.

1. Nel passaggio **[!UICONTROL Advanced]**:

   1. Nella sezione **[!UICONTROL Define training window]**, seleziona tra

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** e

      * **[!UICONTROL Manually input a training window]**. Se selezionata, definire il numero di anni in **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modello - Definisci la finestra di formazione](/help/assets//model-define-training-window.png)

   1. Nella sezione **[!UICONTROL Spend share]**:

      * Per utilizzare i rapporti di investimento di marketing storici per informare il modello quando i dati di marketing sono sparsi, attivare **[!UICONTROL Allow spend share]**.

   1. Nella sezione **[!UICONTROL Prior knowledge]**:

      1. Seleziona **[!UICONTROL Rule type]**.

      1. Specificare le percentuali di contributo per i canali elencati in **[!UICONTROL Name]**, utilizzando la colonna **[!UICONTROL Contribution proportion]**.

      1. Se appropriato, puoi aggiungere per ogni canale una percentuale di **[!UICONTROL Level of confidence]**.

      1. Se necessario, utilizzare **[!UICONTROL Clear all]** per cancellare tutti i valori di input per le colonne **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]**.

         ![Modello - Conoscenza precedente](/help/assets//model-prior-knowledge-step.png)

1. Seleziona **[!UICONTROL Finish]** per completare la configurazione del modello.

   * Nella finestra di dialogo **[!UICONTROL Create instance?]**, seleziona **[!UICONTROL Ok]** per attivare immediatamente il primo set di addestramento e punteggio. Il modello è elencato con stato <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**.

     Selezionare **[!UICONTROL Cancel]** per annullare.

   * Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria.

   Selezionare **[!UICONTROL Back]** per tornare al passaggio precedente.

   Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.
