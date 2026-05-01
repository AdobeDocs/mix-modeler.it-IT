---
title: Campi armonizzati
description: Scopri come definire i campi da utilizzare nell’ambito dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
TQID: https://experienceleague.adobe.com/NlB6aA4AO-0Tpbb9SibgUz0eVUgs8roO9Mju2M8tl7s
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:13:17.577Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 688
ht-degree: 11%

---

# Campi armonizzati

I campi armonizzati ti consentono di definire i campi per gli stessi dati concettualmente, provenienti da origini diverse, ciascuno con la propria definizione di tali dati. Ad esempio, una metrica di clic può essere definita e denominata in modo diverso a seconda dell’origine dei dati. Un campo armonizzato dei clic ti consente di definire una nomenclatura comune per una metrica di clic in base a tali diverse origini di dati di clic.

I campi armonizzati ti consentono di definire i campi che desideri utilizzare come parte del flusso di lavoro armonizza dati. I campi definiti possono essere utilizzati per definire regole per set di dati, punti di contatto di marketing e conversioni.

## Settori di armonizzazione globale

I campi di armonizzazione globali predefiniti disponibili in Mix Modeler sono:


| Nome campo | Nome visualizzato | Categoria | Tipo di dati | Commento |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| brand | Brand | Dimensione | Stringa |           |
| campagna | Campaign | Dimensione | Stringa |           |
| canale | Canale | Dimensione | Stringa |           |
| channel_id | ID canale | Dimensione | Stringa |           |
| channel_type_at_source | Tipo Di Canale In Source | Dimensione | Stringa |           |
| canale | Canale | Dimensione | Stringa |           |
| clic | Clic | Metrica | Numero |           |
| conversiontype | Tipo di conversione | Dimensione | Stringa |           |
| costo | Costo | Metrica | Valuta |           |
| set di dati | Set di dati | Dimensione | Stringa |           |
| date_type | Tipo di data | Dimensione | Stringa | giorno, settimana |
| inviato via e-mail | E-mail inviate | Metrica | Numero |           |
| event_date | Data | Dimensione | Data e ora |           |
| domanda_lorda | Domanda lorda | Metrica | Valuta |           |
| impressioni | Impatti | Metrica | Numero |           |
| data_ultimo_aggiornamento | Data ultimo aggiornamento | Dimensione | Data e ora |           |
| linkvisit | Visite collegamenti | Metrica | Numero |           |
| mediatype | Tipo di file multimediale | Dimensione | Stringa |           |
| net_sales | Vendite nette | Metrica | Valuta |           |
| ordini | Ordini | Metrica | Numero |           |
| sourcetype | Tipo Source | Dimensione | Stringa |           |
| spendere | Spesa | Metrica | Valuta |           |
| trafficsource | Traffic Source | Dimensione | Stringa |           |

{style="table-layout:auto"}

Puoi aggiungere, modificare o eliminare i tuoi campi armonizzati sopra questi campi armonizzati globali.

## Gestisci campi armonizzati

Per visualizzare una tabella dei campi armonizzati disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Fields]** dalla barra superiore. Viene visualizzata una tabella dei campi armonizzati. Se sono disponibili altre pagine, usa ![Freccia a sinistra](/help/assets/icons/ChevronLeft.svg) o ![Freccia a destra](/help/assets/icons/ChevronRight.svg) alle **[!UICONTROL Page _x _di_x_]** per spostarti tra le pagine della tabella.

   Le colonne della tabella specificano i dettagli relativi ai campi armonizzati

   | Nome colonna | Dettagli |
   | ---------------------- | ----------|
   | Nome campo | Nome del campo armonizzato. |
   | Nome visualizzato | Nome visualizzato del campo armonizzato. Questo nome visualizzato viene utilizzato quando si definiscono le regole del set di dati, il punto di contatto di marketing e le definizioni di conversione. |
   | Categoria | Specifica se un campo dati armonizzato è [!UICONTROL Dimension], [!UICONTROL Metric] o [!UICONTROL Derived]. Una categoria derivata è un campo armonizzato che utilizza una definizione di formula basata su metriche. |
   | Tipo di dati | Specifica il tipo di dati ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Data di creazione | Data e ora di creazione del campo armonizzato. |
   | Proprietario | Indica se un campo armonizzato è predefinito ([!UICONTROL Global]) o è definito dall&#39;utente ([!UICONTROL Client]). |
   | Data ultima modifica | Data e ora dell’ultima modifica del campo armonizzato. |
   | Formula | Specifica la formula per un campo armonizzato basato su una categoria derivata. |

   {style="table-layout:auto"}

1. Per cercare un campo armonizzato specifico, utilizzare ![Cerca](/help/assets/icons/Search.svg) **[!UICONTROL *Cerca campo armonizzato *]**.


### Aggiungi un campo armonizzato

Per aggiungere un campo armonizzato, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** in Mix Modeler:

1. Selezionare ![Aggiungi](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. Nella finestra di dialogo **[!UICONTROL Create]**:

   1. Immettere un **[!UICONTROL Field name]**, ad esempio `region`.
   1. Immettere un **[!UICONTROL Display name]**, ad esempio `Region`.
   1. Selezionare un **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** o **[!UICONTROL Derived]**.

      Quando selezioni **[!UICONTROL Derived]**, specifica **[!UICONTROL Formula]**. Per creare un&#39;espressione aritmetica valida, combinare una o più metriche di **[!UICONTROL Insert Metric]** con uno o più operatori **[!UICONTROL + - * / ( )]**. Ad esempio: `[orders]/[impressions]`

   1. Seleziona **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** o **[!UICONTROL Date time]**, quando la categoria selezionata è Dimension.
      - **[!UICONTROL Number]** o **[!UICONTROL Currency]** se la categoria selezionata è metrica o derivata.

   1. Selezionare **[!UICONTROL Submit]** per aggiungere il campo armonizzato. Seleziona **[!UICONTROL Close]** per chiudere la finestra di dialogo senza aggiungere il campo armonizzato.

      ![Crea un campo](/help/assets/create-field.png)


### Modificare un campo armonizzato

Puoi modificare solo i campi armonizzati creati in precedenza (il proprietario è il client). Non è possibile modificare un campo armonizzato globale.

Per modificare un campo armonizzato, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** in Mix Modeler:

1. Seleziona il campo armonizzato da modificare. Ad esempio, **[!UICONTROL Region]**.

1. Nel riquadro **[!UICONTROL Edit harmonization values]** modificare i valori per **[!UICONTROL Display name]**, **[!UICONTROL Category]** e **[!UICONTROL Data type]**. Per ulteriori informazioni, vedere [Aggiungere un campo armonizzato](#add-a-harmonized-field).

1. Selezionare **[!UICONTROL Submit]** per applicare le modifiche al campo armonizzato.

   ![Modifica un campo](/help/assets/edit-field.png)

### Cancellare un campo armonizzato

Puoi eliminare solo i campi armonizzati creati in precedenza (il proprietario è il client). Non puoi eliminare un campo armonizzato globale.

Per eliminare un campo armonizzato, nell&#39;interfaccia ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** in Mix Modeler:

1. Selezionare il campo armonizzato da eliminare, ad esempio **[!UICONTROL Region]**.

1. Selezionare ![Elimina](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** dal riquadro sinistro **[!UICONTROL Edit harmonization values]**.

   >[!WARNING]
   >
   >   Il campo verrà eliminato immediatamente.

