---
title: Consulta le note sulla versione corrente di Mix Modeler
description: Note sulla versione più recente di Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: cfdab6820423f1c5a01ecac52796414cde9a9935
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 6%

---

# Note sulla versione corrente di Mix Modeler

**Ultimo aggiornamento**: 12 novembre 2025.

Queste note sulla versione descrivono l’ultima versione di Mix Modeler. I rilasci di Mix Modeler funzionano su un modello di consegna continua, che consente una cadenza di rilascio mensile approssimativa. Di conseguenza, queste note sulla versione vengono aggiornate e quindi controllate regolarmente.



## Novembre 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Plans tracking]** | Consente agli utenti di comprendere in che modo l’esecuzione dei piani di marketing tiene traccia di ciò che è pianificato. In questo modo puoi avere la certezza delle prestazioni del marketing. Oppure identificare prima opportunità e rischi per correggere il corso e raggiungere gli obiettivi aziendali. Le [Prestazioni per la pianificazione delle visualizzazioni](/help/dashboard/plans.md#performance-to-plan) sono state aggiornate e consentono la configurazione di metriche e granularità. | 12 novembre 2025 | 12 novembre 2025 |
| **[!UICONTROL Channel synergy insights]** | Mostra come i canali di marketing lavorano insieme per creare un impatto maggiore. Sulla base di queste informazioni, potrai spiegare le prestazioni di marketing passate e adeguare di conseguenza le spese di marketing per massimizzare il ritorno complessivo del tuo portfolio di marketing. Una matrice di sinergia dei canali è disponibile in [Approfondimenti modello](/help/models/insights.md#channel-synergy) e [Approfondimenti piano](/help/plans/insights.md#channel-synergies). | 12 novembre 2025 | 12 novembre 2025 |
| **Correzioni** | Correzioni per i seguenti biglietti: <ul><li>AMM-2920: Pianifica il flusso di creazione e la migrazione.</li><li>AMM-3282: Notazione scientifica per numeri piccoli diversi in grandi griglie.</li></ul> | 12 novembre 2025 | 12 novembre 2025 |


## Settembre 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset mapping validations]** | Sono state aggiunte convalide alle mappature dei set di dati di Experience Platform per i campi armonizzati. | mercoledì 9 settembre 2025 | mercoledì 9 settembre 2025 |
| **[!UICONTROL Context menu on links to model and plans]** | Abilitazione del menu di scelta rapida del browser sui collegamenti a modelli e piani. È ora possibile utilizzare il menu di scelta rapida del browser per aprire un piano o un modello specifico in una nuova scheda o finestra. | mercoledì 9 settembre 2025 | mercoledì 9 settembre 2025 |
| **Correzioni** | Correzioni per i seguenti biglietti: <ul><li>AMM-3101: è stata corretta la creazione di mapping non corretta per le regole: `event_date` è stato passato come nome di campo invece di `timestamp`.</li><li>AMM-3092: Corretto impossibile modificare il valore del vincolo massimo del canale su un piano basato su budget duplicato.</li><li>AM3130: sono state corrette le informazioni **[!UICONTROL Run frequency]** errate in una finestra popup di dettaglio di un modello.</li><li>AMM3158: etichette aggiornate per le opzioni **[!UICONTROL Select target metric]** come parte del riquadro **[!UICONTROL Optimize]** nell&#39;interfaccia [Plans create](/help/plans/build.md).</li><li>AMM 3176: è stato corretto un errore che impediva la visualizzazione di [Suddivisione per canale](/help/models/insights.md#breakdown) nella scheda **[!UICONTROL Attribution]** in **[!UICONTROL Model Insights]**.</li></ul> | mercoledì 9 settembre 2025 | mercoledì 9 settembre 2025 |
| **Correzioni** | Correzioni per i seguenti biglietti: <ul><li>AMM-3174: esperienza migliore quando non sono disponibili piani esistenti.</li><li>AMM-3216: convalida migliorata per intervalli di date personalizzati.</li><li>AMM-3240: visualizzazione della frequenza del modello a esecuzione fissa.</ul> | 23 settembre 2025 | 23 settembre 2025 |

## Luglio - Agosto 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Compare plans update]** | Nell&#39;interfaccia utente [Confronta piani](/help/plans/compare.md) sono ora visualizzati ulteriori dettagli per il marketing a pagamento: ROI o CPA e ricavi. | 20 agosto 2025 | 20 agosto 2025 |
| **Aggiornamenti per l&#39;armonizzazione** | Tutte le regole dei set di dati ora utilizzano una mappa [generica simile all&#39;esperienza dei campi armonizzati](/help/harmonize-data/dataset-rules.md), indipendentemente dal tipo di set di dati. Quando mappi un campo armonizzato standard da un set di dati di riepilogo, Mix Modeler tenta di dedurre automaticamente il campo set di dati Experience Platform corrispondente. | mercoledì 29 luglio 2025 | mercoledì 29 luglio 2025 |
| **Ottimizzazione del ROI marginale del piano migliorata/CPA** | Consente di migliorare il modo in cui i budget di marketing vengono distribuiti nel tempo. Invece di far convergere il ROI/CPA marginale nell&#39;intero periodo di pianificazione, puoi [ottimizzare in mesi](/help/plans/build.md) mantenendo al contempo i pattern di spesa mensili. | mercoledì 8 luglio 2025 | mercoledì 8 luglio 2025 |


## Maggio - giugno 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **Piani basati sugli obiettivi** | Accanto ai budget, puoi definire un obiettivo (target) quando [crei](/help/plans/build.md) o [modifichi](/help/plans/insights.md#edit-plan) un piano. Esempi di metriche target sono i ricavi, la conversione, il CPA o il ROI. | 18 giugno 2025 | mercoledì 8 luglio 2025 |
| **Configurazione pattern di spesa** | Quando crei un piano, ora puoi utilizzare [dati di riferimento cronologico](/help/plans/build.md) (come dati e approfondimenti sulle spese di marketing passate) durante la definizione del modello di spesa per ogni intervallo di date di budget. | 14 maggio 2025 | 14 maggio 2025 |
| **Configurazioni avanzate del piano** | Puoi definire [configurazioni avanzate](/help/plans/build.md) per il piano, come ricavi medi per conversione e costi di canale. | 14 maggio 2025 | 14 maggio 2025 |

## Marzo - aprile 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **Rilevamento deriva modello** | Quando apri un modello, viene [richiesto di riaddestrare il modello quando viene rilevata la deriva del modello](/help/models/insights.md#model-drift). | 3 aprile 2025 | 7 maggio 2025 |
| **Restituzione canale marginale in approfondimenti piano** | Una visualizzazione [ritorno al canale marginale](/help/plans/insights.md#marginal-channel-return) è stata aggiunta al piano approfondimenti, che mostra il punto di pareggio marginale e il ritorno al piano per tutti i canali selezionati. | 3 aprile 2025 | 24 aprile 2025 |


## Gennaio - Febbraio 2025

| Funzione | Descrizione | [Inizio rollout](#release-strategy) | [Disponibilità generale](#release-strategy) |
|---|---|---|---|
| **Condizioni nidificate** | Puoi creare condizioni nidificate utilizzando AND e OR quando definisci una popolazione di dati idonea come parte della [configurazione di un modello](/help/models/build.md#configure). | 15 gennaio 2025 | 18 febbraio 2025 |
| **Visualizza report** | Puoi visualizzare un rapporto su un [punto di conversione](/help/harmonize-data/conversions.md#view-report) o un [punto di contatto marketing](/help/harmonize-data/marketing-touchpoints.md#view-report) definito come parte dell&#39;armonizzazione dei dati. | 15 gennaio 2025 | 18 febbraio 2025 |
| **Conferme eliminazione** | Viene richiesto di confermare l&#39;eliminazione di un [piano](/help/plans/overview.md#delete-plans) o di un [modello](/help/models/overview.md#delete-models). | 15 gennaio 2025 | 18 febbraio 2025 |
| **Miglioramento dell&#39;interfaccia utente dei fattori** | Puoi selezionare i [fattori](/help/models/insights.md#factors-beta) da visualizzare in Approfondimenti modello. | 15 gennaio 2025 | 18 febbraio 2025 |
| **Gestione errori** | Messaggi di errore di facile utilizzo e migliore esperienza utente per scenari di errore nell’armonizzazione dei dati e nei piani. | 18 febbraio 2025 | 18 febbraio 2025 |
| **Stato modello** | Ridefinizione di [stati del modello](/help/models/overview.md#manage-models) nel ciclo di vita del modello. | 18 febbraio 2025 | 18 febbraio 2025 |


## Strategia di rilascio

[!UICONTROL Mix Modeler] utilizza i flag di funzionalità (noti anche come &quot;interruttori&quot;) per controllare la visibilità delle nuove funzionalità, consentendo test su scala controllati prima del rilascio completo. Questa strategia di rilascio include le seguenti fasi:

* **Test limitati**: un rilascio graduale inizia con il test da parte degli utenti interni di Adobe. Viene quindi reso disponibile a un piccolo gruppo di clienti per garantire che la funzione soddisfi le esigenze e le aspettative dei clienti.

* **Inizio rollout**: il rollout di una versione graduale inizia con la fase Test limitato. La versione viene quindi scalata dallo 0% al 100% di disponibilità ai clienti nel corso di un paio di mesi. Il rollout graduale avviene a livello di organizzazione Experience Cloud, in modo che tutti gli utenti autorizzati in un’organizzazione ricevano la stessa esperienza.
