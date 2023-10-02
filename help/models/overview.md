---
title: Modelli
description: Scopri come configurare e utilizzare i modelli in Mix Modeler.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---


# Modelli

La funzionalità dei modelli in Mix Modeler consente di configurare, addestrare e valutare modelli AI/ML specifici per gli obiettivi aziendali e supportati dall’apprendimento del trasferimento basato sull’intelligenza artificiale tra l’attribuzione multitouch e la modellazione marketing mix.

I modelli si basano sui dati armonizzati creati come parte del flusso di lavoro dell’applicazione Mix Modeler.

Per creare un modello, utilizzate il flusso di configurazione guidato del modello di Mix Modeler, che potete visualizzare selezionando **[!UICONTROL Guide me]**. Consulta [Creare un modello](create.md) per ulteriori dettagli.

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
>Questa selezione è disponibile solo su modelli addestrati di successo.
>

Per visualizzare le informazioni di un modello, nell’interfaccia Mix Modeler:

1. Seleziona ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** dalla barra a sinistra.

1. Seleziona il nome di un modello con un **[!UICONTROL Last run status]** di <span style="color:green">●</span> **[!UICONTROL Success]** dal **[!UICONTROL Models]** tabella.

1. Dal menu di scelta rapida, selezionare **[!UICONTROL Model Insights]**. Sei stato reindirizzato a [Approfondimenti modello](insights.md).


