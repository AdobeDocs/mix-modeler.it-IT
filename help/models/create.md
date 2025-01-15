---
title: Creare un modello
description: Scopri come creare un modello in Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 16aec67b3e0562ff766f81b8036c724fa03bba17
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---

# Creare un modello

Per creare un modello, nell&#39;interfaccia ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** in Mix Modeler, selezionare **[!UICONTROL Open model canvas]**.

Per creare modelli personalizzati basati sull’intelligenza artificiale, l’interfaccia fornisce un flusso guidato e dettagliato di configurazione del modello.

## Configurazione

Il nome e la descrizione vengono definiti nel passaggio **[!UICONTROL Setup]**:

1. Immettere il modello **[!UICONTROL Name]**, ad esempio `Demo model`. Immettere un **[!UICONTROL Description]**, ad esempio `Demo model to explore AI featues of Mix Modeler`.

   ![Nome modello e descrizione](/help/assets/model-name-description.png)

1. Selezionare **[!UICONTROL Next]** per continuare con il passaggio successivo. Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.

## Configura

Il modello viene configurato nel passaggio **[!UICONTROL Configure]**. La configurazione comporta la definizione di obiettivi di conversione, punti di contatto di marketing, popolazione di dati idonea, fattori esterni e interni e altro ancora.

1. Nella sezione **[!UICONTROL Conversion goal]**:

   ![Modello - passaggio conversione](/help/assets/model-conversion-step.png)

   1. Selezionare una conversione dal menu a discesa **[!UICONTROL Conversion]**. Le conversioni disponibili sono quelle definite come parte di [Conversioni](../harmonize-data/conversions.md) in [!UICONTROL Harmonized datasets]. Ad esempio, **[!UICONTROL Online Conversion]**.

   1. È possibile selezionare ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]** per creare una conversione direttamente dalla configurazione del modello.



1. Nella sezione **[!UICONTROL Marketing touchpoints]** puoi selezionare uno o più punti di contatto marketing, corrispondenti ai punti di contatto marketing definiti come parte di [punti di contatto marketing](../harmonize-data/marketing-touchpoints.md) in [!UICONTROL Harmonized datasets].


   ![Modello - passaggio punto di contatto marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Selezionare uno o più punti di contatto di marketing dal menu a discesa **[!UICONTROL Touchpoint include]**.

      * È possibile utilizzare ![CrossSize75](/help/assets/icons/CrossSize75.svg) per rimuovere un punto di contatto.
      * È possibile utilizzare **[!UICONTROL Clear all]** per rimuovere tutti i punti di contatto.

   1. Puoi selezionare ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]** per creare un punto di contatto di marketing direttamente dalla configurazione del modello.

   >[!NOTE]
   >
   >Non è possibile impostare il modello con punti di contatto con dati sovrapposti e deve esserci almeno un punto di contatto con la spesa.

1. Per impostazione predefinita, viene generato un punteggio per tutti i dati nella vista armonizzata. Per valutare solo un sottoinsieme della popolazione, definire uno o più filtri utilizzando i contenitori nella sezione **[!UICONTROL Eligible data population]**.

   ![Modello - Popolazione dati idonea](/help/assets/model-eligible-data-population-step.png)

   * Per ogni contenitore, definisci uno o più eventi.

      1. Per ogni evento:

         1. Seleziona una metrica o dimensione da **[!UICONTROL _Seleziona campo armonizzato_]**.

         1. Selezionare l&#39;operatore appropriato: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** o **[!UICONTROL is not in]**.

         1. Immettere o selezionare un valore in **[!UICONTROL _Immettere o selezionare il valore_]**.

      1. Per aggiungere un altro evento nel contenitore, selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Per rimuovere un evento dal contenitore, selezionare ![Chiudi](/help/assets/icons/CrossSize75.svg).

      1. Per filtrare utilizzando tutti o uno qualsiasi dei più eventi definiti nel contenitore, selezionare **[!UICONTROL Any of]** o **[!UICONTROL All of]**. L&#39;etichetta cambia di conseguenza da **[!UICONTROL Include ... Or ...]** a **[!UICONTROL Include ... And ...]**.

   * Per aggiungere un contenitore di popolazione dati idoneo, selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

   * Per rimuovere un contenitore del gruppo di dati idoneo, all&#39;interno del contenitore, selezionare ![Altro](/help/assets/icons/More.svg) e selezionare **[!UICONTROL Remove marketing touchpoint]** dal menu di scelta rapida.

   * Seleziona **And** e **Or** tra contenitori per creare definizioni più complesse per la tua popolazione di dati idonea.


1. Per aggiungere al modello set di dati contenenti fattori esterni, utilizzare uno o più contenitori nella sezione **[!UICONTROL External factors dataset]**. Un esempio di fattori esterni sono gli indici S&amp;P.

   ![Modello - Set di dati fattori esterni](/help/assets/model-external-factors-dataset-step.png)

   * Per ciascun contenitore:

      1. Immettere un **[!UICONTROL External factor name]**, ad esempio `External Factors`.

      1. Selezionare un set di dati dal menu a discesa **[!UICONTROL Dataset]**. Puoi selezionare ![Dati](/help/assets/icons/Data.svg) per gestire i set di dati. Per ulteriori informazioni, vedere [Set di dati](../ingest-data/datasets.md).

      1. Selezionare un&#39;opzione dal menu a discesa **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** o **[!UICONTROL Negative]**.

   * Per aggiungere un contenitore di set di dati di fattori esterni aggiuntivi, seleziona ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Per rimuovere un contenitore di set di dati di fattori esterni, selezionare ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).




1. Per aggiungere set di dati contenenti fattori interni al modello, utilizzare uno o più contenitori nella sezione **[!UICONTROL Internal factors dataset]**. Un esempio di fattori interni sono i dati di e-mail marketing.

   ![Modello - Set di dati fattori interni](/help/assets/model-internal-factors-dataset-step.png)

   * Per ciascun contenitore:

      1. Immettere un **[!UICONTROL Internal factor name]**, ad esempio `Email Marketing Data`.

      1. Seleziona un set di dati da **[!UICONTROL _Seleziona un set di dati_]**. Puoi selezionare ![Dati](/help/assets/icons/Data.svg) per gestire i set di dati. Per ulteriori informazioni, vedere [Set di dati](../ingest-data/datasets.md).

      1. Selezionare un&#39;opzione dal menu a discesa **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** o **[!UICONTROL Negative]**.

   * Per aggiungere un contenitore di set di dati di fattori interni aggiuntivi, seleziona ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Per rimuovere un contenitore di set di dati di fattori interni, selezionare ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).



1. Per definire l&#39;intervallo di lookback per il modello, immettere un valore compreso tra `1` e `52` in **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

1. Selezionare **[!UICONTROL Next]** per continuare con il passaggio successivo. Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria. <br/>Selezionare **[!UICONTROL Back]** per tornare al passaggio precedente. <br/>Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.


## Avanzate

È possibile specificare impostazioni avanzate nel passaggio **[!UICONTROL Advanced]**. In questo passaggio puoi abilitare il modello per l’attribuzione multi-touch (MTA).

1. Nella sezione **[!UICONTROL Spend share]**:

   * Per utilizzare i rapporti di investimento di marketing storici per informare il modello quando i dati di marketing sono sparsi, attivare **[!UICONTROL Allow spend share]**.

1. Nella sezione **[!UICONTROL MTA enabled]**:

   * Per abilitare le funzionalità MTA per il modello, attiva **[!UICONTROL MTA enabled]**. Se hai abilitato l’MTA, gli approfondimenti sull’attribuzione multi-touch sono disponibili dopo aver addestrato e valutato il modello. Consulta la scheda [Attribuzione](insights.md#attribution) in [Informazioni sul modello](insights.md).

1. Nella sezione **[!UICONTROL Prior knowledge]**:

   ![Modello - Conoscenza precedente](/help/assets/model-prior-knowledge-step.png)

   1. Selezionare **[!UICONTROL Rule type]**, che è per impostazione predefinita **[!UICONTROL Absolute values]**.

   1. Specificare le percentuali di contributo per i canali elencati in **[!UICONTROL Name]**, utilizzando la colonna **[!UICONTROL Contribution proportion]**.

   1. Se appropriato, puoi aggiungere per ogni canale una percentuale di **[!UICONTROL Level of confidence]**.

   1. Se necessario, utilizzare **[!UICONTROL Clear all]** per cancellare tutti i valori di input per le colonne **[!UICONTROL Contribution proportion]** e **[!UICONTROL Level of confidence]**.


## Pianificazione

È possibile pianificare l&#39;addestramento e il punteggio per il modello nel passaggio **[!UICONTROL Schedule]**.

1. Nella sezione **[!UICONTROL Schedule]** è possibile pianificare l&#39;apprendimento del modello e il punteggio.

   ![Pianifica modello](../assets/model-schedule.png)

   Per pianificare l’apprendimento e il punteggio del modello:

   1. Attiva **[!UICONTROL Enable scheduled model scoring and training]**.
   1. Seleziona **[!UICONTROL Scoring frequency]**:

      * **[!UICONTROL Daily]**: immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]**: selezionare un giorno della settimana e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]**: selezionare un giorno del mese dal menu a discesa Esegui su ogni e immettere un&#39;ora valida (ad esempio `05:22 pm`) oppure utilizzare ![Orologio](/help/assets/icons/Clock.svg).

   1. Selezionare **[!UICONTROL Training frequency]** dal menu a discesa: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

1. Nella sezione **[!UICONTROL Define training window]**, seleziona tra:

   ![Modello - Definisci la finestra di formazione](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** e

   * **[!UICONTROL Manually input a training window]**. Se selezionata, definire il numero di anni in **[!UICONTROL Include events the following years prior to a conversion]**.


1. Seleziona **[!UICONTROL Finish]** per completare la configurazione del modello.

   * Nella finestra di dialogo **[!UICONTROL Create instance?]**, seleziona **[!UICONTROL Ok]** per attivare immediatamente il primo set di addestramento e punteggio. Il modello è elencato con lo stato ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Selezionare **[!UICONTROL Cancel]** per annullare.

   * Se è necessaria una configurazione maggiore, una struttura e un testo rossi spiegano quale configurazione aggiuntiva è necessaria.

   Selezionare **[!UICONTROL Back]** per tornare al passaggio precedente.

   Selezionare **[!UICONTROL Cancel]** per annullare la configurazione del modello.
