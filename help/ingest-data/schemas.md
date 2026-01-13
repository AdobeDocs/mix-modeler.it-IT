---
title: Schemi
description: Scopri come gestire gli schemi necessari per acquisire i dati in Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 7524c2ffc0408b04e6bef5bd5deedc1feea0b682
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 4%

---

# Schemi

Per gestire gli schemi, supportare i dati che desideri acquisire in Experience Platform e utilizzare in Mix Modeler:

1. Passa all’interfaccia di Mix Modeler.

1. Seleziona ![Schemi](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, sotto **[!UICONTROL SETUP]**.

Per ulteriori informazioni, consulta la [Panoramica dell&#39;interfaccia utente degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=it).

## Dati aggregati o di riepilogo

Si consiglia vivamente di utilizzare la classe Metriche di riepilogo XDM come base dello schema sottostante qualsiasi dato aggregato o di riepilogo che si desidera acquisire in Experience Platform e utilizzare in Mix Modeler.

Utilizza la classe Metriche di riepilogo XDM per:

- dati sui giardini murati, ad esempio dati provenienti da Facebook o YouTube.

- dati relativi a fattori esterni, come i dati di SPX (indici azionari S&amp;P 500), dati meteorologici,

- dati sui fattori interni, ad esempio le variazioni di prezzo, un calendario festivo.

>[!IMPORTANT]
>
>La definizione dello schema deve contenere almeno un campo numerico (utilizzando un valore Integer, Double, Boolean o un altro tipo numerico) per supportare le metriche richieste per i dati acquisiti.

Uno schema che utilizza la classe base **[!DNL XDM Summary Metrics]** può essere semplice, come mostrato nella **[!DNL ExternalFactorSummarySchema]** seguente.

![Schema Fattori Esterni](/help/assets/external-factors-schema.png)

Questo semplice schema può essere utilizzato per acquisire set di dati contenenti dati per, ad esempio:

- Dati di indice della concorrenza

  | timestamp | date_type | fattore | valore |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | settimana | competitor_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | settimana | competitor_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | settimana | competitor_index | 280,07 |
  | ... | ... | ... | ... |

- Dati festività pubbliche

  | timestamp | date_type | fattore | valore |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 12-12-2020:00:00.000Z | settimana | all_Holiday_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | settimana | all_Holiday_flag | 1,0 |
  | ... | ... | ... | ... |


Di seguito è riportato un esempio più completo di **[!DNL LumaPaidMarketingSchema]** che utilizza **[!DNL XDM Summary Metrics]** come classe base. Lo schema utilizza gruppi di campi dedicati (con annotazioni di colori) per metriche (**[!DNL AMMMetrics]**), dimensioni (**[!DNL AMMDimensions]**) e altre informazioni specifiche del cliente (**[!DNL CustomerSpecific]**).

![Schema di riepilogo](/help/assets/summary-schema.png)

Data la natura asincrona dell’acquisizione del profilo, durante la raccolta di dati aggregati o di riepilogo da origini esterne si consiglia di utilizzare il gruppo di campi Dettagli audit del sistema Source esterno come parte di uno schema. Questo gruppo di campi definisce un set di proprietà di controllo per le origini esterne.

## Gruppo di campi Campi Fattore standard

Per comodità, Experience Platform supporta un gruppo di campi Factor Standard dedicato per i dati dei fattori interni ed esterni, che spesso fanno parte dei dati di riepilogo, dei fattori interni o dei fattori esterni. Questo gruppo di campi definisce i campi seguenti:

| Nome visualizzato campo | Nome campo | Tipo di campo | Tipo di dati | Obbligatorio | Descrizione |
|---|---|---|---|:-:|---|
| Nome fattore | nomeFattore | Dimensione | Stringa | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | Nome del fattore |
| Valore fattore | factorValue | Metrica | Doppio | ![Segno di spunta](/help/assets/icons/Checkmark.svg) | Valore del fattore |
| Tipo di fattore | factorType | Dimensione | Stringa (enum) | | Tipo del fattore.<br/>I valori possibili sono: <ul><li>Interno (fattore interno)</li><li>Esterno (fattore esterno)</li></ul> |
| Tipo di valore | valueType | Dimensione | Stringa (enum) | | I valori possibili sono:<ul><li>Effettivo (valore effettivo)</li><li>Previsto (valore previsto)</li></ul>Se non è specificato alcun valore, il valore predefinito è Effettivo. |
| Granularità | granularità | Dimensione | Stringa (enum) | | I valori possibili sono:<ul><li>Giornaliero</li><li>Ogni settimana</li><li>Mensile</li></ul> |

Un set di dati di riepilogo, fattore interno o fattore esterno può essere basato su:

- Uno schema che **utilizza** il gruppo Campi Factor Standard. Questo set di dati viene visualizzato come **[!UICONTROL Factors]** quando si configurano le regole del set di dati. I campi armonizzati definiti dall’utente, come parte delle regole del set di dati per il set di dati, sono disponibili come fattori quando si crea un modello.
- Uno schema che **non utilizza** il gruppo Campi Factor Standard. Questo set di dati viene visualizzato come **[!UICONTROL Summary]** quando si configurano le regole del set di dati. Il set di dati è configurato come dati di riepilogo e non influenza i dati armonizzati.

## Tipi di dati supportati

Attualmente, Mix Modeler supporta un sottoinsieme di tipi di dati di Experience Platform. Sono supportati i seguenti tipi di dati di base (campi), menzionati in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it#data-type):

- Stringa
- Intero
- Doppio
- Booleano
- Lungo
- Breve
- Byte
- Data
- Data-ora


>[!MORELIKETHIS]
>
>- [Schemi](schemas.md)
