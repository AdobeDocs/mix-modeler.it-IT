---
title: Schemi
description: Scopri come gestire gli schemi necessari per acquisire i dati in Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 3%

---

# Schemi

Per gestire gli schemi, supportare i dati che desideri acquisire in Experienci Platform e utilizzare in Mix Modeler:

1. Passa all’interfaccia Mix Modeler.

1. Seleziona ![Schemi](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, sotto **[!UICONTROL SETUP]**.

Consulta la [Panoramica dell’interfaccia utente degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) per ulteriori informazioni.

## Dati aggregati o di riepilogo

Si consiglia vivamente di utilizzare la classe Metriche di riepilogo XDM come base dello schema sottostante qualsiasi dato aggregato o di riepilogo che si desidera acquisire in Experienci Platform e utilizzare in Mix Modeler.

Utilizza la classe Metriche di riepilogo XDM per:

- dati sui giardini murati, ad esempio dati provenienti da Facebook o YouTube.

- dati relativi a fattori esterni, come i dati di SPX (indici azionari S&amp;P 500), dati meteorologici,

- dati sui fattori interni, ad esempio le variazioni di prezzo, un calendario festivo.

>[!IMPORTANT]
>
>La definizione dello schema deve contenere almeno un campo numerico (utilizzando un valore Integer, Double, Boolean o un altro tipo numerico) per supportare le metriche richieste per i dati acquisiti.

Uno schema che utilizza **[!DNL XDM Summary Metrics]** la classe base può essere semplice, come illustrato nella **[!DNL ExternalFactorSummarySchema]** di seguito.

![Schema Fattori Esterni](../assets/external-factors-schema.png)

Questo semplice schema può essere utilizzato per acquisire set di dati contenenti dati per, ad esempio:

- Dati di indice della concorrenza

  | timestamp | date_type | fattore | valore |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | settimana | competitor_index | 289,8 |
  | 05.05.2020:00:00.000Z | settimana | competitor_index | 291,2 |
  | 12-12-2020:00:00.000Z | settimana | competitor_index | 280,07 |
  | ... | ... | ... | ... |

- Dati festività pubbliche

  | timestamp | date_type | fattore | valore |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 05.05.2020:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 12-12-2020:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | settimana | all_Holiday_flag | 1,0 |
  | ... | ... | ... | ... |


Vedi di seguito per un esempio più completo di **[!DNL LumaPaidMarketingSchema]** utilizzando **[!DNL XDM Summary Metrics]** come classe base. Lo schema utilizza gruppi di campi dedicati (con annotazioni di colori) per le metriche (**[!DNL AMMMetrics]**), dimensioni (**[!DNL AMMDimensions]**) e altre informazioni specifiche per il cliente (**[!DNL CustomerSpecific]**).

![Schema di riepilogo](../assets/summary-schema.png)

Data la natura asincrona dell’acquisizione del profilo, durante la raccolta di dati aggregati o di riepilogo da origini esterne si consiglia di utilizzare il gruppo di campi Dettagli audit sistema di origine esterna come parte di uno schema. Questo gruppo di campi definisce un set di proprietà di controllo per le origini esterne.


## Tipi di dati supportati

Attualmente, Mix Modeler supporta un sottoinsieme di tipi di dati Experienci Platform. I seguenti tipi di dati di base (campi), indicati in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type), sono supportati:

- Stringa
- Intero
- Doppio
- Booleano
- Lungo
- Breve
- Byte
- Data
- Data-ora
