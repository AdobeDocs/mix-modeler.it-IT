---
title: Controlli di accesso
description: Scopri come configurare i controlli di accesso in Mix Modeler.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Controlli di accesso

Il controllo degli accessi per Mix Modeler viene fornito tramite Experience Platform in [Adobe Admin Console](https://adminconsole.adobe.com/) e tramite [Autorizzazioni](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) in Experience Platform. Questa funzionalità sfrutta i profili di prodotto nell’Admin Console, che collegano gli utenti con autorizzazioni e sandbox.

Per ulteriori informazioni sul controllo degli accessi, vedere [Panoramica sul controllo degli accessi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Controllo degli accessi basato sul ruolo

Consulta [Amministrazione](../main-guide/administration.md) su come configurare le autorizzazioni di accesso basate sul ruolo per gli utenti e i gruppi di utenti di Mix Modeler in Experience Platform.

## Controllo degli accessi basato su attributi

[Il controllo dell&#39;accesso basato su attributi](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) è una funzionalità di Experience Platform che consente agli amministratori di controllare l&#39;accesso a oggetti specifici e/o funzionalità basate su attributi. Gli attributi possono essere metadati aggiunti a un oggetto, ad esempio un’etichetta aggiunta a un campo o a un segmento dello schema. Un amministratore definisce i criteri di accesso che includono attributi per gestire le autorizzazioni di accesso degli utenti.

Questa funzionalità consente di etichettare i campi dello schema Experience Data Model (XDM) con etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. In parallelo, gli amministratori possono utilizzare l’interfaccia di amministrazione di utenti e ruoli per definire i criteri di accesso sui campi dello schema XDM. E gestisci meglio l’accesso dato a utenti o gruppi di utenti (utenti interni, esterni o di terze parti). Inoltre, il controllo dell’accesso basato su attributi consente agli amministratori di gestire l’accesso a segmenti specifici.

Tramite il controllo degli accessi basato su attributi, gli amministratori possono controllare l’accesso degli utenti sia ai dati personali sensibili (SPD) che alle informazioni personali (PII) in tutti i flussi di lavoro e le risorse di Platform. Gli amministratori possono definire ruoli utente con accesso solo a campi e dati specifici che corrispondono a tali campi.

Durante la configurazione delle regole del set di dati per i set di dati armonizzati, il controllo dell&#39;accesso basato sull&#39;attributo [di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) viene applicato a livello di campo. Un campo è limitato quando un’etichetta è associata a un campo schema. Inoltre, è abilitata una policy attiva che nega l’accesso a quel campo. Di conseguenza:

* quando crei una regola di set di dati, non vengono visualizzati i campi dello schema con restrizioni,
* non puoi visualizzare o modificare la mappatura di uno o più campi dello schema per i quali esistono restrizioni. Quando modifichi o visualizzi una regola del set di dati contenente tali campi con restrizioni, viene visualizzata la schermata seguente.
  ![Azione non consentita](/help/assets//action-not-permitted.png)

