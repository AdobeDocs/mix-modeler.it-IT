---
title: Amministrazione
description: Scopri come amministrare Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 4d84c93121fc476cc6610ad572bab161bbacfc23
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# Amministrazione

Utilizza [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html) per gestire prodotti e utenti Mix Modeler.

Affinché Mix Modeler funzioni correttamente, devi impostare le autorizzazioni corrette.

Nell’interfaccia utente di Adobe Experience Cloud:

1. Seleziona **[!UICONTROL Permissions]** dalla barra a sinistra, sotto **[!UICONTROL ADMINISTRATION]**.

1. Seleziona ![Utente](/help/assets/icons/User.svg) **[!UICONTROL Roles]** dal pannello a sinistra.

1. Selezionare un ruolo esistente o creare un ruolo utilizzando **[!UICONTROL Create role]** (ad esempio, **Mix Modeler**). Se si seleziona un ruolo esistente, selezionare ![Modifica](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** per modificare le autorizzazioni per il ruolo. Per ulteriori informazioni, vedere [Gestione ruoli](https://helpx.adobe.com/it/enterprise/using/admin-console.html).

1. Verifica di aver selezionato una o più sandbox per il ruolo.

1. Aggiungi la risorsa **Adobe Mix Modeler** all&#39;elenco delle risorse per il ruolo.

1. Assicurarsi di selezionare le autorizzazioni **[!UICONTROL Adobe Mix Modeler]** corrette per il ruolo che si sta configurando. Puoi selezionare uno o più dei seguenti ruoli:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. Accertati di selezionare le autorizzazioni aggiuntive per il ruolo. Ad esempio, per visualizzare o gestire set di dati e schemi, seleziona:

   - **[!UICONTROL Data Management]**: selezionare le opzioni rilevanti: **[!UICONTROL View Datasets]** o **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: selezionare le opzioni rilevanti: **[!UICONTROL Manage Schemas]** o **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Selezionare **[!UICONTROL Save]** per salvare le autorizzazioni.

1. In **[!UICONTROL Details]** entro **[!UICONTROL Role]**, aggiungere l&#39;elemento **[!UICONTROL Users]** o **[!UICONTROL User groups]** appropriato per consentire agli utenti di accedere a Mix Modeler.
