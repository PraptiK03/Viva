---
title: Sign in to and switch between Viva Glint experiences in the app 
description: Viva Glint Administrators and dashboard users can access multiple Microsoft Viva Glint experiences in one tenant.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: multiple apps, multiple Viva Glint experiences, switch experiences
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/11/2025
---

# Sign in to and switch between Viva Glint experiences in the app

Viva Glint Administrators and dashboard users can access multiple Microsoft Viva Glint experiences in one tenant. To successfully sign in, users need: 

- A profile uploaded in each Viva Glint experience with the same email address that matches the email address in Microsoft Entra.
  - Example: If kat@contoso.com should access three separate Viva Glint experiences (Contoso, Fabrikam, and Relecloud), they need to be uploaded to all three Viva Glint experiences with the same email address: kat@contoso.com.
- A license for each Viva Glint experience that they need to access. 

> [!IMPORTANT]
> Single tenants with multiple Viva Glint experiences are currently supported for customers migrating from LinkedIn Glint only.

To access and switch between Viva Glint experiences: 

1. Select a link based on the region that your organization's Viva Glint tenant sits in.
  - US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
  - EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)
1. Follow login prompts and select a Viva Glint experience.

   > [!NOTE]
   > When a user accessed their dashboard from an organization-specific link (for example: http://app.us1.glint.cloud.microsoft/relecloud), they aren’t presented with Viva Glint experience selections and go to the dashboard for the organization referenced in the link.
   
   :::image type="content" source="../../media/glint/setup/ms-login.png" alt-text="Screenshot of the Microsoft login page.":::

   :::image type="content" source="../../media/glint/setup/vg-sami-first-login.png" alt-text="Screenshot of the Viva Glint experience selection page.":::

1. After logging in, switch between Viva Glint experiences with the dropdown menu in the app.
   > [!NOTE]
   > After initial login, users see a **Select your Glint experience** prompt. For future logins, the last Viva Glint experience that a user selected displays on their dashboard. 

   :::image type="content" source="../../media/glint/setup/select-glint-exp-dash.png" alt-text="Screenshot of the dashboard message that appears when first logging into one of multiple Viva Glint experiences.":::

   :::image type="content" source="../../media/glint/setup/vg-experience-switcher-dash.png" alt-text="Screenshot of the Viva Glint dashboard with the experience dropdown menu.":::
