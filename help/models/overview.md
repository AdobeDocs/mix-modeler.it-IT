---
title: Modelli
description: Scopri come configurare e utilizzare i modelli in Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: f445cb2b1ec04ffe9247e858c048587802bffe9c
workflow-type: tm+mt
source-wordcount: '485'
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

Per creare un modello, utilizzate il flusso di configurazione guidato del modello Mix Modeler, disponibile quando selezionate **[!UICONTROL Guide me]**. Consulta [Creare un modello](create.md) per ulteriori dettagli.

## Gestisci modelli

Per visualizzare una tabella dei modelli correnti, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Viene visualizzata una tabella dei modelli correnti.

   Le colonne della tabella specificano i dettagli relativi al modello.

   | Nome colonna | Dettagli |
   |---|---|
   | Nome | Nome del modello |
   | Descrizione | Descrizione del modello |
   | Eventi di conversione | Conversione selezionata per il modello. |
   | Set di dati | Set di dati utilizzato dal modello per addestrare e valutare. Per impostazione predefinita, questo è il set di dati armonizzato. |
   | Frequenza di esecuzione | Frequenza di esecuzione dell&#39;addestramento del modello. |
   | Ultima esecuzione | La data e l’ora dell’ultimo addestramento del modello. |
   | Stato ultima esecuzione | Lo stato dell’ultima esecuzione dell’addestramento del modello. <br/><span style="color:green">●</span> Completato<br/><span style="color:orange">●</span> Problema di formazione<br/> <span style="color:orange">●</span> In attesa di formazione <br/><span style="color:red">●</span> Non riuscito |

   {style="table-layout:auto"}

1. Per modificare le colonne visualizzate per l&#39;elenco, selezionare ![Impostazioni colonna](../assets/icons/ColumnSetting.svg) e attiva/disattiva colonne ![Verifica](../assets/icons/Checkmark.svg) o disattivato.

### Eliminare un modello

Per eliminare un modello:

1. Selezionate il nome del modello da eliminare.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Delete]** per eliminare il modello.

### Visualizzare i dettagli di un modello

Per visualizzare ulteriori dettagli su un modello:

1. Selezionare il nome del modello di cui si desidera visualizzare ulteriori dettagli.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL More]**. I dettagli del modello selezionato vengono visualizzati nel riquadro di destra.



### Approfondimenti modello

>[!NOTE]
>
>Questa selezione è disponibile solo su modelli addestrati correttamente.
>

Per visualizzare le informazioni di un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con un **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dal **[!UICONTROL Models]** tabella.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**. Sei stato reindirizzato a [Approfondimenti modello](insights.md).
