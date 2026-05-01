---
title: Amministrazione
description: Scopri come amministrare Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# Amministrazione

Utilizza [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html) per gestire prodotti e utenti Mix Modeler.

Per il corretto funzionamento di Mix Modeler, è necessario impostare le autorizzazioni corrette.

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

     ![RBAC Mix Modeler](/help/assets/mix-modeler-rbac.png)


1. Accertati di selezionare le autorizzazioni aggiuntive per il ruolo. Ad esempio, per visualizzare o gestire set di dati e schemi, seleziona:

   - **[!UICONTROL Data Management]**: selezionare le opzioni rilevanti: **[!UICONTROL View Datasets]** o **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: selezionare le opzioni rilevanti: **[!UICONTROL Manage Schemas]** o **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Selezionare **[!UICONTROL Save]** per salvare le autorizzazioni.

1. In **[!UICONTROL Details]** entro **[!UICONTROL Role]**, aggiungere **[!UICONTROL Users]** o **[!UICONTROL User groups]** appropriati per consentire agli utenti di accedere a Mix Modeler.
