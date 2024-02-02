---
title: Modelli
description: Scopri come configurare e utilizzare i modelli in Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
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

Per creare un modello, utilizzate il flusso di configurazione guidato del modello Mix Modeler, disponibile quando selezionate **[!UICONTROL Open model canvas]**. Consulta [Creare un modello](create.md) per ulteriori dettagli.

## Gestisci modelli

Per visualizzare una tabella dei modelli correnti, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Viene visualizzata una tabella dei modelli correnti.

   Le colonne della tabella specificano i dettagli relativi al modello.

   | Nome colonna | Dettagli |
   |---|---|
   | Nome | Nome del modello |
   | Descrizione | Descrizione del modello |
   | Evento di conversione | Conversione selezionata per il modello. |
   | Frequenza di esecuzione | Frequenza di esecuzione dell&#39;addestramento del modello. |
   | Ultima esecuzione | La data e l’ora dell’ultimo addestramento del modello. |
   | Stato | Lo stato dell’ultima esecuzione dell’addestramento del modello. <br/><span style="color:green">●</span> Completato<br/><span style="color:orange">●</span> Problema di formazione<br/> <span style="color:orange">●</span> In attesa di formazione <br/><span style="color:red">●</span> Non riuscito <br/><span style="color:gray">●</span> _ (quando è in corso un&#39;ultima esecuzione) |

   {style="table-layout:auto"}

1. Per modificare le colonne visualizzate per l&#39;elenco, selezionare ![Impostazioni colonna](../assets/icons/ColumnSetting.svg) e attiva/disattiva colonne ![Verifica](../assets/icons/Checkmark.svg) o disattivato.


### Visualizzare i dettagli di un modello

Per visualizzare ulteriori dettagli su un modello:

1. Seleziona ![Info](../assets/icons/Info.svg) affinché un modello possa mostrare un pop-up con i relativi dettagli.



### Approfondimenti modello

Per visualizzare le informazioni di un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con un **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dal **[!UICONTROL Models]** tabella. Le informazioni sul modello sono disponibili solo sui modelli addestrati correttamente.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**. Sei stato reindirizzato a [Approfondimenti modello](insights.md).


### Punteggio di nuovo


Per assegnare nuovamente un punteggio a un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con un **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dal **[!UICONTROL Models]** tabella. Il nuovo punteggio è disponibile solo sui modelli addestrati correttamente.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Re-score]**. La visualizzazione di uno stato aggiornato per il modello potrebbe richiedere alcuni minuti.


### Eliminare un modello

Per eliminare un modello:

1. Selezionate il nome del modello da eliminare.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Delete]** per eliminare il modello.

   >[!WARNING]
   >
   >Il modello viene eliminato immediatamente.


