---
title: Criteri
description: Scopri come accedere ai criteri da Mix Modeler.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
TQID: https://experienceleague.adobe.com/fk6qAZS7Uymx2dzptcazBieXIJ3mGF2pjG-EDhm-Kh4
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2: id: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:17:02.907Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 2%

---

# Criteri

Una volta eseguito il flusso di lavoro per creare un modello e inviare la configurazione del modello, [l&#39;applicazione dei criteri](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) verifica se sono presenti violazioni. Se si verifica una violazione dei criteri, viene visualizzato un messaggio a comparsa che indica che uno o più criteri sono stati violati. Questa verifica ha lo scopo di garantire che le operazioni sui dati e le azioni di marketing all’interno di Experience Platform siano conformi ai criteri di utilizzo dei dati.

Per impostazione predefinita, Mix Modeler verifica la presenza di violazioni dei criteri definiti da Adobe associati alle etichette e alle azioni di marketing seguenti:

| Nome criterio | Etichetta associata | Azione di marketing associata |
|---|---|---|
| Limitare l’analisi dell’utilizzo e la misurazione basata sull’utente | C8 | Analytics |
| Limita data science | C9 | Data science |
| Limita l’esportazione dei dati | C12 | Esportazione dati |

Vengono inoltre verificate le violazioni dei criteri definiti personalmente e che contengono le azioni di marketing elencate nella tabella precedente.

Quando si viola un criterio durante la creazione di una regola di set di dati, viene visualizzato un popover che visualizza informazioni sulla violazione del criterio.

Ad esempio:

- hai abilitato il criterio [!UICONTROL Restrict data science] con l&#39;etichetta associata [!UICONTROL C9] e l&#39;azione di marketing associata [!UICONTROL Data Science],
- hai applicato l&#39;etichetta [!UICONTROL C9] - [!UICONTROL No data science] al campo `totalCost` nello schema dei dati di conversione,
- si desidera impostare una regola del set di dati che, tra l&#39;altro, associa il campo `totalCost` dello schema dei dati di conversione al campo armonizzato con nome `spend` (e nome visualizzato `Spend`).

Quando desideri salvare la regola del set di dati, viene visualizzato un popup **[!UICONTROL Data governance policy violation detected]** che mostra un elenco di criteri violati. Quando si seleziona il nome del criterio in [!UICONTROL Violation summary], viene visualizzato un elenco di [!UICONTROL Active data governance labels], contenente [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] e [!UICONTROL Government labels] applicati.

<!-- pending screenshot -->

Quando si applica un’etichetta di utilizzo dati a un campo schema già utilizzato in dati armonizzati, viene visualizzato un messaggio a comparsa con informazioni sulla violazione dei criteri.

Ad esempio:

- hai impostato una regola del set di dati che, tra l&#39;altro, associa il campo `totalCost` dello schema dei dati di conversione al campo armonizzato con nome `spend` (e nome visualizzato `Spend`).
- i dati armonizzati sono stati sincronizzati almeno una volta (vedi [Regole set di dati - Sincronizza dati](/help/harmonize-data/dataset-rules.md#sync-data)).
- si abilita il criterio [!UICONTROL Restrict data science] con l&#39;etichetta associata [!UICONTROL C9] e l&#39;azione di marketing associata [!UICONTROL Data Science],
- desideri applicare l&#39;etichetta [!UICONTROL C9] - [!UICONTROL No data science] al campo `totalCost` nello schema Dati di conversione.

Quando desideri salvare l&#39;aggiornamento dello schema, viene visualizzato un popup **[!UICONTROL Data governance policy violation detected]** che mostra un elenco di criteri violati. Selezionare il nome del criterio in [!UICONTROL Violation summary] per trovare ulteriori dettagli nell&#39;elenco [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Popover rilevati da violazione

La violazione dei criteri di governance dei dati rilevata fornisce informazioni specifiche sulla violazione. Puoi risolvere queste violazioni tramite impostazioni dei criteri e altre misure che non sono direttamente correlate al flusso di lavoro di configurazione. Ad esempio, puoi modificare le etichette in modo che alcuni campi possano essere utilizzati a scopo di scienza dei dati. In alternativa, è possibile modificare la configurazione del modello stessa, in modo che il modello non utilizzi un oggetto con un&#39;etichetta di utilizzo dei dati.

La selezione di ![Privacy](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** nella barra a sinistra consente di accedere all&#39;interfaccia [!UICONTROL Policies] di Experience Platform, consentendo di gestire i criteri, le etichette e le azioni di marketing.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Panoramica sui criteri di utilizzo dei dati](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

