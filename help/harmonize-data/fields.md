---
title: Campi armonizzati
description: Scopri come definire i campi da utilizzare nell’ambito dell’armonizzazione dei dati in Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: fecb122f6e2e8ae532babd0e2964ad200174a032
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 8%

---

# Campi armonizzati

I campi armonizzati ti consentono di definire i campi per gli stessi dati concettualmente, provenienti da origini diverse, ciascuno con la propria definizione di tali dati. Ad esempio, una metrica di clic può essere definita e denominata in modo diverso a seconda dell’origine dei dati. Un campo armonizzato dei clic ti consente di definire una nomenclatura comune per una metrica di clic in base a tali diverse origini di dati di clic.

I campi armonizzati ti consentono di definire i campi che desideri utilizzare come parte del flusso di lavoro armonizza dati. I campi definiti possono essere utilizzati per definire regole per set di dati, punti di contatto di marketing e conversioni.

## Settori di armonizzazione globale

I campi di armonizzazione globali predefiniti disponibili in Mix Modeler sono:


| Nome campo | Nome visualizzato | Categoria | Tipo di dati | Commento |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| brand | Marchio | Dimensione | Stringa |           |
| campaign | Campaign | Dimensione | Stringa |           |
| channel | Channel | Dimensione | Stringa |           |
| channel_id | ID canale | Dimensione | Stringa |           |
| channel_type_at_source | Tipo di canale all’origine | Dimensione | Stringa |           |
| channel | Channel | Dimensione | Stringa |           |
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
| sourcetype | Tipo di origine | Dimensione | Stringa |           |
| spendere | Spesa | Metrica | Valuta |           |
| trafficsource | Traffic Source | Dimensione | Stringa |           |

{style="table-layout:auto"}

Puoi aggiungere, modificare o eliminare i tuoi campi armonizzati sopra questi campi armonizzati globali.

## Gestisci campi armonizzati

Per visualizzare una tabella dei campi armonizzati disponibili, nell’interfaccia Mix Modeler:

1. Seleziona ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** dalla barra a sinistra.

1. Seleziona **[!UICONTROL Fields]** dalla barra superiore. Viene visualizzata una tabella dei campi armonizzati. Se sono disponibili più pagine, utilizza ![Freccia sinistra](../assets/icons/ChevronLeft.svg) o ![Freccia a destra](../assets/icons/ChevronRight.svg) a **[!UICONTROL Page _x _di_x_]** per spostarsi tra le pagine della tabella.

   Le colonne della tabella specificano i dettagli relativi ai campi armonizzati

   | Nome colonna | Dettagli |
   | ---------------------- | ----------|
   | Nome campo | Nome del campo armonizzato. |
   | Nome visualizzato | Nome visualizzato del campo armonizzato. Questo nome visualizzato viene utilizzato quando si definiscono le regole del set di dati, il punto di contatto di marketing e le definizioni di conversione. |
   | Categoria | Specifica se un campo dati armonizzato è un [!UICONTROL Dimension], a [!UICONTROL Metric] o [!UICONTROL Derived]. Una categoria derivata è un campo armonizzato che utilizza una definizione di formula basata su metriche. |
   | Tipo di dati | Specifica il tipo di dati ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Data di creazione | Data e ora di creazione del campo armonizzato. |
   | Proprietario | Indica se un campo armonizzato è un campo predefinito ([!UICONTROL Global]) o è definito da te ([!UICONTROL Client]). |
   | Data ultima modifica | Data e ora dell’ultima modifica del campo armonizzato. |
   | Formula | Specifica la formula per un campo armonizzato basato su una categoria derivata. |

   {style="table-layout:auto"}

1. Per cercare un campo armonizzato specifico, utilizzare ![Ricerca](../assets/icons/Search.svg) **[!UICONTROL *Cerca campo armonizzato *]**.


### Aggiungi un campo armonizzato

Per aggiungere un campo armonizzato, nella ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Interfaccia di Mix Modeler:

1. Seleziona ![Aggiungi](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. In **[!UICONTROL Create]** finestra di dialogo:

   1. Immetti un **[!UICONTROL Field name]**, ad esempio `region`.
   1. Immetti un **[!UICONTROL Display name]**, ad esempio `Region`.
   1. Seleziona un **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** o **[!UICONTROL Derived]**.

      Quando selezioni **[!UICONTROL Derived]**, specifica un **[!UICONTROL Formula]**. Per creare un’espressione aritmetica valida, combina una o più metriche di **[!UICONTROL Insert Metric]** con uno o più operatori **[!UICONTROL + - * / ( )]** . Ad esempio: `[orders]/[impressions]`

   1. Seleziona un **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** o **[!UICONTROL Date time]**, quando Categoria selezionata è Dimension.
      - **[!UICONTROL Number]** o **[!UICONTROL Currency]** quando Categoria selezionata è Metrica o Derivata.

   1. Seleziona **[!UICONTROL Submit]** per aggiungere il campo armonizzato. Seleziona **[!UICONTROL Close]** per chiudere la finestra di dialogo senza aggiungere il campo armonizzato.

      ![Crea un campo](../assets/create-field.png)


### Modificare un campo armonizzato

Puoi modificare solo i campi armonizzati creati in precedenza (il proprietario è il client). Non è possibile modificare un campo armonizzato globale.

Per modificare un campo armonizzato, nella sezione ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Interfaccia di Mix Modeler:

1. Seleziona il campo armonizzato da modificare. Ad esempio, **[!UICONTROL Region]**.

1. In **[!UICONTROL Edit harmonization values]** , modificare i valori per **[!UICONTROL Display name]**, **[!UICONTROL Category]**, e **[!UICONTROL Data type]**. Consulta [Aggiungi un campo armonizzato](#add-a-harmonized-field) per ulteriori informazioni.

1. Seleziona **[!UICONTROL Submit]** applicare le modifiche al campo armonizzato.

   ![Modificare un campo](../assets/edit-field.png)

### Cancellare un campo armonizzato

Puoi eliminare solo i campi armonizzati creati in precedenza (il proprietario è il client). Non puoi eliminare un campo armonizzato globale.

Per eliminare un campo armonizzato, nella sezione ![RicercaDati](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Interfaccia di Mix Modeler:

1. Seleziona il campo armonizzato da eliminare, ad esempio **[!UICONTROL Region]**.

1. Seleziona ![Elimina](../assets/icons/Delete.svg) **[!UICONTROL Delete]** dal **[!UICONTROL Edit harmonization values]** riquadro sinistro.

   >[!WARNING]
   >
   >   Il campo verrà eliminato immediatamente.

