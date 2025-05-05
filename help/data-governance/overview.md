---
title: Panoramica sulla governance dei dati
description: Scopri come utilizzare i servizi e gli strumenti di Experience Platform che ti consentono di controllare i dati sull’esperienza raccolti. In questo modo, rispetti le tue pratiche commerciali, gli obblighi legali e il processo di sviluppo.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 1%

---

# Panoramica sulla governance dei dati

L’integrazione tra Mix Modeler e Experience Platform offre a Mix Modeler le funzionalità per sfruttare le funzioni di governance dei dati intrinseche di Experience Platform. Questa sezione della documentazione descrive le specifiche delle funzioni di governance dei dati disponibili in Mix Modeler.

La governance dei dati di Experience Platform consente di controllare e comprendere i dati in tutto il percorso acquisiti tramite Experience Platform. Questo percorso implica la gestione della qualità dei dati, della derivazione dei dati, della catalogazione dei dati e molto altro.

Etichette di utilizzo dei dati e criteri creati sui set di dati utilizzati dalla superficie Experience Platform in Mix Modeler, se appropriato. Ad esempio, queste etichette interrompono o avvisano gli utenti quando si eliminano set di dati che fanno parte di una regola di set di dati nei dati armonizzati. Oppure nascondi i campi dello schema limitati agli utenti durante la creazione di una regola per un set di dati.

L’integrazione della governance dei dati consente di gestire la conformità in modo più efficiente. Gli amministratori dei dati della tua organizzazione possono impostare criteri per limitare l’utilizzo. Di conseguenza, puoi utilizzare dati conformi ai criteri definiti dagli amministratori dei dati. Per ulteriori informazioni, consulta la documentazione su [Etichette e criteri](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-dataviews/data-governance).

Sono disponibili le seguenti funzioni di governance dei dati:

| Funzione | Dettagli |
|---|---|
| Controlli di accesso | Sono supportati il controllo dell’accesso basato sul ruolo e il controllo dell’accesso basato su attributi (a livello di campo). Per ulteriori informazioni, vedere [Controlli di accesso](access-controls.md). |
| Registri di audit | Quando gli utenti creano, aggiornano o eliminano specifiche categorie di Mix Modeler, la funzionalità di controllo di Experience Platform registra l’attività nei registri di controllo. Consulta [Registri di controllo](audit-logs.md) per ulteriori informazioni. |
| Criteri | Come parte del flusso di lavoro dei dati armonizzato, vengono applicati i criteri definiti da Experience Platform. Qualsiasi violazione delle etichette di utilizzo dei dati viene segnalata e visualizzata all’utente. Consulta [Criteri](policies.md) per ulteriori informazioni. |
| Crittografia | Tutti i set di dati utilizzati per l’input e l’output di modelli seguono le linee guida di Experience Platform. La crittografia dei dati di Experience Platform si applica ai dati in transito e a riposo. |
| Igiene dei dati | Tutti i set di dati utilizzati per i modelli di input e out seguono le linee guida di Experience Platform. Experience Platform fornisce una serie di strumenti per gestire il ciclo di vita dei dati del cliente, incluso il supporto di diversi tipi di scadenza dei dati. Quando elimini un set di dati di origine da Experience Platform, utilizzato come parte dei dati armonizzati, viene inviata una notifica. Per ulteriori informazioni, vedere [Regole del set di dati](/help/harmonize-data/dataset-rules.md). |
| Chiavi gestite dal cliente | Dopo aver concesso la licenza a Mix Modeler con il componente aggiuntivo Privacy Security Shield o Healthcare Shield, puoi utilizzare la funzionalità Chiavi gestite dal cliente per sfruttare Azure Key Vault per inserire le chiavi personalizzate tramite API. Hai a disposizione la gestione completa dei dati elaborati all’interno dei modelli in Mix Modeler. |
