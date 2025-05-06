---
title: Release Microsoft Viva Glint feedback results to User Roles
description: Grant live or phased access to determine when managers have access to survey results.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: report access
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/06/2025
---

# Release Microsoft Viva Glint feedback results to User Roles

To determine when leaders get access to Recurring or Ad Hoc survey results, grant Live or Phased access to User Roles. Access status can't be switched while a survey is live.

- **Live access**: Reporting access is readily available, in real time, as surveys are completed. Admins always have *Live* access and can't be included in *Phased* access rollout.
  
- **Phased access**:  Recommended for managers and Human Resources Business Partners (HRBPs) for action planning, tracking, and reviewing feedback results for completed surveys.
  - Excludes this role group from real-time, live survey results
  - Is configured at the program level but occurs at the cycle level
  - Allows users access to historical cycles
  - Prohibits reporting access during that cycle until the survey ends and the admin grants access 

> [!TIP]
> Keep survey results classified while the survey is *Live*, among just a small group of leaders. Incomplete results may lead to unintended and inaccurate conclusions. Feedback results aren't final until all results are considered.

## Enable or switch between Live and Phased access

From the **Reporting** tab of your admin dashboard, choose the User Role. In this example, let's use Managers. The down-facing arrow is selected and the permissions for employees in the Manager User Role are displayed.

:::image type="content" source="../../media/glint/reports/choose-access-1.png" alt-text="Screenshot of the Program Roles permissions section in Reporting.":::

The permissions for the chosen role display. The default **Reporting view** is **Live.**  Use the menu box in that row to switch from Live View to Phased Access.
 
:::image type="content" source="../../media/glint/reports/switch-view.png" alt-text="Screenshot of the switching from Live View to Phased Access.":::
 
## Grant user access for a completed cycle

- After a cycle is competed, the admin needs to release the survey results to those users with Phased access. 

   1. Switch to the **Completed** view and hover over the survey cycle. 
   1. In the **Reporting view** column for the desired survey, view reporting access. In this example, the **Reporting view** shows that **7 of 8 Roles** currently see reports. Hover over the hyperlink to reveal the User Roles. 

       :::image type="content" source="../../media/glint/setup/access-view.png" alt-text="Screenshot of the Reporting view access display.":::

  1. Now select that hyperlink in the **Reporting view** column and then select **Grant Access**.
   
       :::image type="content" source="../../media/glint/setup/grant-access.png" alt-text="Screenshot of the Grant Access button to release results.":::

  1. In the **Grant Report Access**, check the box of any role that requires access. **Important: Once access is granted, it can't be revoked.**
   
  1. Select **Provide Access**.
   
      :::image type="content" source="../../media/glint/setup/grant-report-access-2.png" alt-text="Screenshot of the Grant Report Access dialog box.":::

  1. Now the **Reporting view** column for this survey reads **Fully Released** and is visible to all roles with permissions. 

      :::image type="content" source="../../media/glint/setup/fully-released.png" alt-text="Screenshot of the Fully Released reporting view.":::

- The hyperlink may indicate **Fully Released** (rather than the "7 of 8 Roles" in the example). This means that all roles already have report permissions available to them.

> [!IMPORTANT]
> When a new program cycle begins, reporting from the previous cycle is automatically released to all users with permissions to see the results. This release occurs even when the admin hasn't updated all roles to **Live** status.

## Change from Live access to Phased access
 
