---
title: Registri di audit
description: Scopri come accedere ai registri di audit da Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 85f9b42a775006cd3566447b2bb9d0a806fa3e73
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 5%

---

# Registri di audit

Per aumentare la trasparenza e la visibilità delle attività eseguite nel sistema, l’attività dell’utente all’interno del flusso di lavoro di Mix Modeler viene acquisita nei registri di audit di Experience Platform per comprendere eventuali modifiche guidate dall’utente alle categorie Mix Modeler. Questi registri costituiscono un audit trail che può essere utile per la risoluzione dei problemi e può aiutare la tua azienda a rispettare in modo efficace le politiche aziendali di gestione dei dati e i requisiti normativi.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Un registro di audit informa chi ha eseguito quale azione e quando. Ogni azione registrata contiene metadati che indicano il tipo di azione, la data e l’ora, l’ID e-mail dell’utente che l’ha eseguita e altri attributi relativi al tipo di azione. Tiene traccia delle azioni di creazione, aggiornamento ed eliminazione eseguite dagli utenti in Mix Modeler.

Per esaminare il registro di controllo, nell’interfaccia di Mix Modeler:

1. Selezionare ![Elenco attività](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** da **[!UICONTROL PRIVACY]**.

1. In **[!UICONTROL Audits]**, è possibile trovare **[!UICONTROL Activity log]**. Il registro attività mostra le voci per le categorie, le azioni e lo stato di Mix Modeler seguenti.

   | Categoria | Azione | Stato |
   |---|---|---|
   | Regola set di dati Mix Modeler | Creare | Consenti o nega |
   | Regola set di dati Mix Modeler | Aggiornamento | Consenti o nega |
   | Regola set di dati Mix Modeler | Elimina | Consenti o nega |
   | Campo Mix Modeler | Creare | Consenti o nega |
   | Campo Mix Modeler | Aggiornamento | Consenti o nega |
   | Campo Mix Modeler | Elimina | Consenti o nega |
   | Punto di contatto marketing Mix Modeler | Creare | Consenti o nega |
   | Punto di contatto marketing Mix Modeler | Aggiornamento | Consenti o nega |
   | Punto di contatto marketing Mix Modeler | Elimina | Consenti o nega |
   | Conversione Mix Modeler | Creare | Consenti o nega |
   | Conversione Mix Modeler | Aggiornamento | Consenti o nega |
   | Conversione Mix Modeler | Elimina | Consenti o nega |
   | Modello Mix Modeler | Creare | Consenti o nega |
   | Modello Mix Modeler | Aggiornamento | Consenti o nega |
   | Modello Mix Modeler | Elimina | Consenti o nega |
   | Modello Mix Modeler | Riscore | Consenti o nega |
   | Modello Mix Modeler | Clona | Consenti o nega |
   | Modello Mix Modeler | Addestra/Ritira | Consenti o nega |
   | Modello Mix Modeler | Download/salvataggio dei metadati | Consenti o nega |
   | Piano Mix Modeler | Creare | Consenti o nega |
   | Piano Mix Modeler | Aggiornamento | Consenti o nega |
   | Piano Mix Modeler | Modifica modello associato | Consenti o nega |
   | Armonizzazione dei dati Mix Modeler | Attiva sincronizzazione | Consenti o nega |


1. Seleziona una voce nel registro attività per aprire un pannello e ottenere ulteriori dettagli.

   ![Controllo Mix Modeler](/help/assets/mix-modeler-audit.png)

1. Per filtrare in base all&#39;intervallo **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** o **[!UICONTROL Date]**, selezionare ![Filtro](/help/assets/icons/Filter.svg).

1. Per modificare le colonne visualizzate nel registro attività, selezionare ![Colonne](/help/assets/icons/ColumnSetting.svg) e nella finestra di dialogo **[!UICONTROL Customize table]** selezionare le colonne da visualizzare. Selezionare **[!UICONTROL Apply]** per applicare la selezione, **[!UICONTROL Cancel]** per annullarla.

1. Per scaricare il registro di controllo, selezionare ![Scarica](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Nella finestra di dialogo **[!UICONTROL Download log]**, selezionare **[!UICONTROL CSV]** o **[!UICONTROL JSON]** come formato e selezionare **[!UICONTROL Download]**.

## Accesso ai registri di audit

Quando la funzione è abilitata per la tua organizzazione, i registri di audit vengono raccolti automaticamente quando si verifica un’attività. Non è necessario abilitare manualmente la raccolta dei registri di controllo.

Per visualizzare ed esportare i registri di audit, è necessario disporre dell&#39;autorizzazione di controllo dell&#39;accesso per i registri di audit. Per informazioni su come gestire le singole autorizzazioni per le funzionalità di Mix Modeler, consulta la [documentazione sul controllo degli accessi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).
