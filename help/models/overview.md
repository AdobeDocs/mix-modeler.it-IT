---
title: Modelli
description: Scopri come configurare e utilizzare i modelli in Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Modelli

La funzionalità dei modelli in Mix Modeler consente di configurare, addestrare e valutare modelli AI/ML specifici per gli obiettivi aziendali e supportati dall’apprendimento del trasferimento basato sull’intelligenza artificiale tra l’attribuzione multitouch e la modellazione marketing mix.

I modelli si basano sui dati armonizzati creati come parte del flusso di lavoro dell’applicazione Mix Modeler.

Un modello in Mix Modeler è un modello di apprendimento automatico utilizzato per misurare e/o prevedere un risultato specifico basato sugli investimenti di un addetto marketing. I punti di contatto di marketing e i dati di riepilogo possono essere utilizzati come input. Mix Modeler consente di creare varianti di modelli basati su diversi set di variabili, dimensioni e risultati, come ricavi, unità vendute, lead.

Un modello richiede:

* una conversione,
* uno o più punti di contatto di marketing (canali) costituiti da dati a livello riassuntivo, dati di punto di contatto di marketing (dati evento) o entrambi,
* un intervallo di lookback configurabile per
* una finestra di formazione configurabile.

Un modello può facoltativamente includere:

* fattori esterni,
* fattori interni,
* i cosiddetti &quot;priori&quot; (distribuzione di probabilità che rappresenta la conoscenza o l’incertezza dei dati prima o prima di osservarli), che indicizza le conversioni precedenti per canale,
* condivisione di spesa, che utilizza come proxy la condivisione di spesa relativa quando i dati di marketing sono sparsi.


## Creare un modello

Per creare un modello, utilizzare il flusso di configurazione guidato del modello Mix Modeler passo dopo passo disponibile quando si seleziona **[!UICONTROL Open model canvas]**. Per ulteriori dettagli, vedere [Creare un modello](create.md).

## Gestisci modelli

Per visualizzare una tabella dei modelli correnti, nell’interfaccia Mix Modeler:

1. Seleziona ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Viene visualizzata una tabella dei modelli correnti.

   Le colonne della tabella specificano i dettagli relativi al modello.

   | Nome colonna | Dettagli |
   |---|---|
   | Nome | Nome del modello |
   | Descrizione | Descrizione del modello |
   | Evento di conversione | Conversione selezionata per il modello. |
   | Frequenza di esecuzione | Frequenza di esecuzione dell&#39;addestramento del modello. |
   | Ultima esecuzione | La data e l’ora dell’ultimo addestramento del modello. |
   | Stato | Lo stato dell’ultima esecuzione dell’addestramento del modello. <br/><span style="color:green">●</span> riuscito<br/><span style="color:orange">●</span> problema di formazione<br/> <span style="color:orange">●</span> In attesa del corso di formazione <br/><span style="color:red">●</span> Non riuscito <br/><span style="color:gray">●</span> _ (quando è in corso l&#39;ultima esecuzione) |

   {style="table-layout:auto"}

1. Per modificare le colonne visualizzate per l&#39;elenco, selezionare ![Impostazioni colonna](/help/assets//icons/ColumnSetting.svg) e attivare o disattivare le colonne in ![Controlla](/help/assets//icons/Checkmark.svg).


### Visualizzare i dettagli di un modello

Per visualizzare ulteriori dettagli su un modello:

1. Seleziona ![Info](/help/assets//icons/Info.svg) per un modello per visualizzare un popup con i dettagli.



### Approfondimenti modello

Per visualizzare le informazioni di un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dalla tabella **[!UICONTROL Models]**. Le informazioni sul modello sono disponibili solo sui modelli addestrati correttamente.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**. Sei stato reindirizzato a [Model Insights](insights.md).


### Punteggio di nuovo


Per assegnare nuovamente un punteggio a un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dalla tabella **[!UICONTROL Models]**. Il nuovo punteggio è disponibile solo sui modelli addestrati correttamente.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Re-score]**. La visualizzazione di uno stato aggiornato per il modello potrebbe richiedere alcuni minuti.


### Eliminare un modello

Per eliminare un modello:

1. Selezionate il nome del modello da eliminare.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Delete]** per eliminare il modello.

   >[!WARNING]
   >
   >Il modello viene eliminato immediatamente.


