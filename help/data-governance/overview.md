---
title: Panoramica sulla governance dei dati
description: Scopri come utilizzare i servizi e gli strumenti di Experience Platform che ti consentono di controllare i dati sull’esperienza raccolti. In questo modo, rispetti le tue pratiche commerciali, gli obblighi legali e il processo di sviluppo.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
TQID: https://experienceleague.adobe.com/vc5z266rexOpAuR1HJCj-ltOLZmkccBDvfi8JUsuiJ4
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2: id: bf7ac0fc-effb-4f0c-b93f-658412718d3cid: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:16:50.195Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 3%

---

# Panoramica sulla governance dei dati

L’integrazione tra Mix Modeler e Experience Platform offre a Mix Modeler le funzionalità per sfruttare le funzioni di governance dei dati intrinseche di Experience Platform. Questa sezione della documentazione descrive le specifiche delle funzioni di governance dei dati disponibili in Mix Modeler.

La governance dei dati di Experience Platform consente di controllare e comprendere i dati in tutto il percorso acquisiti tramite Experience Platform. Questo percorso implica la gestione della qualità dei dati, della derivazione dei dati, della catalogazione dei dati e molto altro.

Etichette di utilizzo dei dati e criteri creati sui set di dati utilizzati dalla superficie Experience Platform in Mix Modeler, se appropriato. Ad esempio, queste etichette interrompono o avvisano gli utenti quando si eliminano set di dati che fanno parte di una regola di set di dati nei dati armonizzati. Oppure nascondi i campi dello schema limitati agli utenti durante la creazione di una regola per un set di dati.

L’integrazione della governance dei dati consente di gestire la conformità in modo più efficiente. Gli amministratori dei dati della tua organizzazione possono impostare criteri per limitare l’utilizzo. Di conseguenza, puoi utilizzare dati conformi ai criteri definiti dagli amministratori dei dati. Per ulteriori informazioni, consulta la documentazione su [Etichette e criteri](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance).

Sono disponibili le seguenti funzioni di governance dei dati:

| Funzione | Dettagli |
|---|---|
| Controlli di accesso | Sono supportati il controllo dell’accesso basato sul ruolo e il controllo dell’accesso basato su attributi (a livello di campo). Per ulteriori informazioni, vedere [Controlli di accesso](access-controls.md). |
| Registri di controllo | Quando gli utenti creano, aggiornano o eliminano specifiche categorie di Mix Modeler, la funzionalità di controllo di Experience Platform registra l’attività nei registri di controllo. Consulta [Registri di controllo](audit-logs.md) per ulteriori informazioni. |
| Criteri | Come parte del flusso di lavoro dei dati armonizzato, vengono applicati i criteri definiti da Experience Platform. Qualsiasi violazione delle etichette di utilizzo dei dati viene segnalata e visualizzata all’utente. Consulta [Criteri](policies.md) per ulteriori informazioni. |
| Crittografia | Tutti i set di dati utilizzati per l’input e l’output di modelli seguono le linee guida di Experience Platform. La crittografia dei dati di Experience Platform si applica ai dati in transito e a riposo. |
| Igiene dei dati | Tutti i set di dati utilizzati per i modelli di input e out seguono le linee guida di Experience Platform. Experience Platform fornisce una serie di strumenti per gestire il ciclo di vita dei dati del cliente, incluso il supporto di diversi tipi di scadenza dei dati. Quando elimini un set di dati di origine da Experience Platform, utilizzato come parte dei dati armonizzati, viene inviata una notifica. Per ulteriori informazioni, vedere [Regole del set di dati](/help/harmonize-data/dataset-rules.md). |
| Chiavi gestite dal cliente | Dopo aver concesso la licenza a Mix Modeler con il componente aggiuntivo Privacy Security Shield, puoi utilizzare la funzionalità Chiavi gestite dal cliente per sfruttare Azure Key Vault e inserire le tue chiavi tramite API. Hai a disposizione la gestione completa dei dati elaborati all’interno dei modelli in Mix Modeler. |
