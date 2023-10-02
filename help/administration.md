---
title: Amministrazione
description: Scopri come amministrare Adobe Mix Modeler.
source-git-commit: b5b277e3476bdf6c0c0da85425bba19bea00c594
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---


# Amministrazione

Utilizza il [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html) per gestire prodotti e utenti Adobe Mix Modeler.

Per il corretto funzionamento di Adobe Mix Modeler, è necessario impostare le autorizzazioni corrette.

Nell’interfaccia utente di Adobe Experience Cloud,

1. Seleziona **[!UICONTROL Permissions]** dalla barra a sinistra, sotto **[!UICONTROL ADMINISTRATION]**.

1. Seleziona ![Persona](assets/icons/User.svg) **[!UICONTROL Roles]** dal pannello a sinistra.

1. Seleziona un ruolo esistente o creane uno esistente utilizzando **[!UICONTROL Create role]**. Se si seleziona un ruolo esistente, selezionare ![Modifica](assets/icons/Edit.svg) **[!UICONTROL Edit]** per modificare le autorizzazioni per il ruolo. Consulta [Gestisci ruoli](https://helpx.adobe.com/it/enterprise/using/admin-console.html) per ulteriori informazioni.

1. Accertati di selezionare le seguenti autorizzazioni per il ruolo:

   * **[!UICONTROL Sandboxes]**: seleziona almeno una sandbox.

   * **[!UICONTROL Data Management]**: accertati di selezionare le opzioni **[!UICONTROL View Datasets]** e **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: accertati di selezionare le opzioni **[!UICONTROL Manage Schemas]** e **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: assicurati di selezionare **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** e **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: assicurati di selezionare **[!UICONTROL View Sources]** e **[!UICONTROL Manage Sources]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   Le autorizzazioni impostate per il ruolo devono essere simili a quelle riportate di seguito.

   ![Autorizzazioni](assets/permissions.png)

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Seleziona **[!UICONTROL Save]** per salvare le autorizzazioni.

1. In entrata **[!UICONTROL Details]** entro **[!UICONTROL Role]**, aggiungi il **[!UICONTROL Users]** e/o **[!UICONTROL User groups]** per fornire agli utenti l’accesso all’Adobe Mix Modeler.
