---
title: Flusso di lavoro di Mix Modeler
description: Scopri il flusso di lavoro tipico di Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Flusso di lavoro di Mix Modeler

Guarda questo video per un’introduzione al flusso di lavoro degli utenti in Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Un flusso di lavoro tipico in Mix Modeler è costituito dalle seguenti attività:

![Testo alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Attività | Descrizione |
|---|---|---|
| ![Dati](/help/assets/icons/Data.svg){width="100"} | [**Acquisire dati**](../ingest-data/overview.md) | Acquisisci dati evento da Experience Platform (ad esempio Adobe Analytics, Web SDK, altre origini), dati aggregati dai canali di marketing (ad esempio TV, giardini murati, e-mail, attività possedute e gestite), dati di fattori esterni dai clienti (ad esempio le variazioni di prezzo nel servizio di abbonamento) e dati di fattori interni (ad esempio i piani delle vacanze). |
| ![ControlloDati](/help/assets/icons/DataCheck.svg){width="100"} | [**Armonizzare i dati**](../harmonize-data/overview.md) | Configura le regole di mappatura e di risoluzione dei conflitti per unire i vari set di dati di marketing necessari per misurare e pianificare le prestazioni della campagna in Mix Modeler. |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**Configura modelli**](../models/create.md) | Configura le istanze del modello con i punti di contatto di marketing (ad esempio i canali), le definizioni di conversione e i fattori interni ed esterni. |
| ![DatiFile](/help/assets/icons/FileData.svg){width="100"} | [**Formazione e valutazione dei modelli**](../models/overview.md) | Crea punteggi aggregati e a livello di evento utilizzando l’apprendimento automatico e il punteggio. |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**Crea piani**](../plans/overview.md) | Determinare la migliore allocazione di fondi di marketing per raggiungere un obiettivo aziendale utilizzando l’output dei modelli Mix Modeler. |
| ![Dashboard](/help/assets/icons/Dashboard.svg){width="100"} | [**Dashboard panoramica**](../dashboard/overview.md) | Ottieni informazioni su dati, modelli e piani armonizzati utilizzando varie visualizzazioni configurabili. |

{style="table-layout:auto"}

Il diagramma di flusso dettagliato orientato ai dati riportato di seguito illustra come:

* I dati armonizzati si basano su:

   * dati sull’evento esperienza (provenienti dal connettore di origine di Analytics, raccolti tramite SDK e API Experience Platform, acquisiti tramite i connettori di origine o mediante acquisizione in streaming),
   * dati aggregati o di riepilogo provenienti da giardini murati (come Facebook, YouTube), da origini del traffico o da dati pubblicitari offline e
   * definizioni di campi armonizzati e regole in materia di serie di dati.

* un modello è basato su:

   * le definizioni dei punti di contatto di conversione e marketing risultanti dai dati armonizzati e
   * dati aggregati o di riepilogo non di marketing contenenti fattori interni o esterni.

* I punteggi degli eventi di attribuzione multi-touch possono potenzialmente essere inseriti in un data lake Experience Platform per essere utilizzati nella configurazione del modello, nell’apprendimento e nel punteggio successivi.

![Flusso di lavoro completo](/help/assets/comprehensive-workflow.svg)
