---
title: Controlli di accesso
description: Scopri come configurare i controlli di accesso in Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
TQID: https://experienceleague.adobe.com/EoiF5ui2Bqq0Oxuv-s5E5pQclj9gnjoKgZ1bOzRK-vY
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-05-01T09:20:37.287Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 1%

---

# Controlli di accesso

Il controllo degli accessi per Mix Modeler viene fornito tramite Experience Platform in [Adobe Admin Console](https://adminconsole.adobe.com/) e tramite [Autorizzazioni](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) in Experience Platform. Questa funzionalità sfrutta i profili di prodotto in Admin Console, che collegano gli utenti con autorizzazioni e sandbox.

Per ulteriori informazioni sul controllo degli accessi, vedere [Panoramica sul controllo degli accessi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Controllo degli accessi basato sul ruolo

Consulta [Amministrazione](../main-guide/administration.md) su come configurare le autorizzazioni di accesso basate sul ruolo per gli utenti e i gruppi di utenti di Mix Modeler in Experience Platform.

## Controllo degli accessi basato su attributi

[Il controllo dell&#39;accesso basato su attributi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) è una funzionalità di Experience Platform che consente agli amministratori di controllare l&#39;accesso a oggetti specifici e/o funzionalità basate su attributi. Gli attributi possono essere metadati aggiunti a un oggetto, ad esempio un’etichetta aggiunta a un campo o a un segmento dello schema. Un amministratore definisce i criteri di accesso che includono attributi per gestire le autorizzazioni di accesso degli utenti.

Questa funzionalità consente di etichettare i campi dello schema Experience Data Model (XDM) con etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. In parallelo, gli amministratori possono utilizzare l’interfaccia di amministrazione di utenti e ruoli per definire i criteri di accesso sui campi dello schema XDM. E gestisci meglio l’accesso dato a utenti o gruppi di utenti (utenti interni, esterni o di terze parti). Inoltre, il controllo dell’accesso basato su attributi consente agli amministratori di gestire l’accesso a segmenti specifici.

Tramite il controllo degli accessi basato su attributi, gli amministratori possono controllare l’accesso degli utenti sia ai dati personali sensibili (SPD) che alle informazioni personali (PII) in tutti i flussi di lavoro e le risorse di Platform. Gli amministratori possono definire ruoli utente con accesso solo a campi e dati specifici che corrispondono a tali campi.

Durante la configurazione delle regole del set di dati per i set di dati armonizzati, il controllo dell&#39;accesso basato su [attributi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) di Experience Platform viene applicato a livello di campo. Un campo è limitato quando un’etichetta è associata a un campo schema. Inoltre, è abilitata una policy attiva che nega l’accesso a quel campo. Di conseguenza:

* quando crei una regola di set di dati, non vengono visualizzati i campi dello schema con restrizioni,
* non puoi visualizzare o modificare la mappatura di uno o più campi dello schema per i quali esistono restrizioni. Quando modifichi o visualizzi una regola del set di dati contenente tali campi con restrizioni, viene visualizzata la schermata seguente.
  ![Azione non consentita](/help/assets/action-not-permitted.png)
