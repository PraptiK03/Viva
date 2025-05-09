---
ms.date: 04/23/2025
title: Upload and maintain data through the Microsoft 365 admin center
description: Learn how to upload organizational data using the Microsoft 365 Admin Center instead of Viva Insights.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Upload and maintain data through the Microsoft 365 admin center

Viva Insights is transitioning tenants to upload organizational data through the Microsoft 365 admin center. This move is being completed in phases, and your tenant admin will receive a notification prior to your scheduled transition. Until you receive such notification, please continue uploading your organizational data as you currently do.

Organizational data in Microsoft 365 centralizes organizational data uploads across Viva and Microsoft 365 apps, making it faster to reuse your organizational data across multiple apps without needing to upload data for each app separately.

[Learn more about organizational data in the Microsoft 365 admin center](/viva/organizational-data).

[Learn more about the Microsoft 365 admin center](/microsoft-365/admin/admin-overview/admin-center-overview).

>[!Important]
>Viva Insights admins have a six-month transition period to migrate to the new platform. The transition will occur in three waves, with all Viva Insights tenants assigned to one of the waves.
>
>Once your tenant(s) migrate to Organizational data in Microsoft 365, only Global admins can upload and manage data through the Microsoft 365 admin center, [here](https://go.microsoft.com/fwlink/?linkid=2298902). Managing data uploads through the Viva Insights Analyst Workbench will no longer be available.

## 1. Prepare your organizational data

Work with the person responsible for preparing your data, such as your data source admin, to prepare your organizational data.

To use organizational data in Microsoft 365, you need to use the same column headers provided in the template through the data upload wizard.  

Ensure your file is updated with the correct attribute name headers as specified in the template, which must be prefixed with Microsoft_*attribute-name* such as Microsoft_*Organization*. This is different from how you currently prepare your data file for upload within Viva Insights. The headers should now be prefixed with Microsoft_. Keep this formatting in mind as you prepare your data file to prevent data upload errors.

[Learn more about the public attributes you can upload through Organizational data in the Microsoft 365 admin center](/viva/organizational-data).

[Learn more about how to prepare your data](..//admin/prepare-org-data.md).

>[!Note]
>Microsoft Entra data is the default data source until you upload an organizational data file. [Learn more](/viva/organizational-data).

## 2. Upload and manage your data in the Microsoft 365 admin center

After preparing your data, Global admins must now work with your organization’s data source admin to prepare organizational data using the .csv template in the Microsoft 365 admin center.

To upload data, follow the Organizational data in Microsoft 365 wizard to complete the data upload. After successfully uploading data, Global admins can: 

* View the data upload progress
* Download data validation error logs to help correct the data if needed
* Check organizational data import history
* View the data quality of past uploads

>[!Note]
>Uploading files larger than 25 MB using Organizational data in Microsoft 365 requires the use of SharePoint. [Learn how to upload data through SharePoint](/viva/import-orgdata#upload-the-file-to-sharepoint).

## Other capabilities remaining in the Advanced Analytics app

While uploading and managing organizational data must now be done in the Microsoft 365 admin center, all other tasks must still be done in the Advanced Analytics app such as creating [data partitions](../admin/partitions.md), uploading all other types of data such as [sentiment data](../../org-team-insights/copilot-dashboard.md#upload-group-level-survey-results-with-the-advanced-insights-app), business outcome data, and managing your Viva Insights [admin settings](../admin/admin-center.md).

## Use Viva Insights for data uploads after transition

If you've transitioned to the Microsoft 365 admin center for organizational data uploads, you can switch back to using Viva Insights if you'd like. You'll be able to switch back until all tenants have been migrated to the Microsoft 365 admin center. To do so, use the process below.

1. In the advanced insights app, select **Organizational data** on the left.

2. Select **Undo migration**.

    :::image type="content" source="../images/modis-upload-rollback-01.png" alt-text="Screenshot that shows the button to transition back to Viva Insights upload.":::

3. Select a reason for why you're switching back, then select **Submit**.

4. Your tenant will be reverted immediately back to Viva Insights for organizational data uploads.

## FAQ

**Why am I in wave 1?**

Current product usage and geographical location were the main factors to determine which customers to migrate first. Reach out to us if you have any questions about the wave to which you're assigned.

**Will this affect my organization’s existing data?**

There's no impact on your organization’s existing data in Viva Insights. Every new upload from organizational data in Microsoft 365 is an incremental upload to your existing data.

**Will there be any downtime associated with this move?**

No delays are expected, and you shouldn't experience any break in Viva Insights seeded, Copilot dashboard, or premium Viva Insights capabilities. The usual time to process your data uploads will still apply. While no system downtime is expected, you might need some time to get familiar with the Microsoft 365 admin center platform.

**Will I still be able to use the Viva Insights Advanced Analytics app to upload data?**

No, you won’t have access to the organizational data upload feature in the Viva Insights app. All other features you use in Viva Insights will still be available.

**I have more questions that haven’t been answered, or I need to make a request to the Viva Insights team.**

Please reach out to us through your Viva Insights support team.