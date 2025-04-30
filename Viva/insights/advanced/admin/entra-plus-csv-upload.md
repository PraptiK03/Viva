---
ms.date: 04/30/2025
title: Use Microsoft Entra plus .csv files for parallel data uploads
description: This article discusses how to upload your organizational data to Viva Insights using both Microsoft Entra and .csv files simultaneously.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium
ms.collection: 
- viva-insights-advanced
- essentials-manage
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Use Microsoft Entra plus .csv files for parallel data uploads

Viva Insights typically ingests data from either Microsoft Entra ID (the default source) *or* through a manual .csv file upload. For added flexibility, Viva Insights Administrators can also set up **both** of those ingestion methods simultaneously.

Using this simultaneous or "parallel" data ingestion method ensures that critical data such as the **ManagerId** and **Organization** attributes can be retrieved from Entra, while additional data fields can be fetched from .csv files or automated connectors. This method can also improve reporting accuracy by combining other attributes from Entra and .csv uploads.

This feature can be used by tenants whose current data source is uploaded data, either in the form of manual .csv files or through connectors.

## Key benefits

* There's no loss of data when switching between data sources. 

* Having flexibility in data sources can improve the accuracy of insights in the Microsoft Copilot Dashboard, leader reports, and the analyst workbench.

## Prerequisites

1. You must be assigned the role of **Viva Insights Administrator**. 

2. If Entra is currently your default data source, you must first manually upload data using a .csv file in order to use this feature. The .csv file upload could include only fake or imaginary data, such as in the examples below.

### Example 1

For instance, your initial upload might look like this:

| PersonId | ManagerId | Organization | FunctionType |
|---|---|---|---|
| a@b.com | Dummy001@dummy.com | DummyOrg001 | Analyst |
| b@b.com | Dummy002@dummy.com | DummyOrg002 | HR |
| c@b.com | Dummy003@dummy.com | DummyOrg003 | Finance |
| d@b.com | Dummy004@dummy.com | DummyOrg004 | Marketing |
| e@b.com | Dummy005@dummy.com | DummyOrg005 | Engineering |

Then, your subsequent upload might look like this:

| PersonId | FunctionType |
|---|---|
| a@b.com | Analyst |
| b@b.com | HR |
| c@b.com | Finance |
| d@b.com | Marketing |
| e@b.com | Engineering |

### Example 2

Or, your initial upload might look like this: 

| PersonId | ManagerId | Organization | FunctionType |
|----|----|----|----|
| a@b.com | Dummy001@dummy.com | DummyOrg001 | Analyst |

Then, your subsequent update might look like this:

| PersonId | FunctionType |
|---|---|
| a@b.com | Analyst |
| b@b.com | HR |
| c@b.com | Finance |
| d@b.com | Marketing |
| e@b.com | Engineering |

## How to enable parallel data uploads

1. Log in to the advanced insights app. 

2. On the left, select **Organizational data**.  

3. Select **Configure Entra connection**.

    1. Select which attributes you want to be sourced from Entra. Only **ManagerId** and **Organization** are currently available. 

    2. It'll take approximately 24 hours for the change to go into effect. 

    3. Once the parallel data source is in effect, Entra will automatically become the default source for the attributes you've chosen, and those fields will no longer be sourced from uploaded data, even if those fields are included in your uploaded files. 

    4. You can continue uploading other data fields via manual .csv files, or through connectors, which will provide the remaining dataset for your insights.

## FAQs

**Q1. I've set up parallel data ingestion, but I want to switch back to only uploaded data. How do I do that?**

If you no longer want to use any attribute from Entra and would like to use only uploaded data going forward such as .csv files,  select **Configure Entra connection** on the **Organizational data** page. Then clear your selections for the **ManagerId** and **Organization** attributes. The change will go into effect in about 24 hours.

:::image type="content" source="../images/configure-entra-connection.png" alt-text="Screenshot that shows how to configure the Entra connection.":::

**Q2. I've set up parallel data ingestion, but I want to switch back to only using Entra and remove my uploaded data. How do I do that?**

First, make sure you've configured Entra sync for the **ManagerId** and **Organization** attributes.

Then, to remove uploaded data, follow [these instructions](./upload-org-data-subsequent.md#delete-optional-fields-from-existing-organizational-data) to delete optional attributes. Use this process to remove attributes you no longer need. You can remove all attributes except **ManagerId** and **Organization**. Then, as long as the Entra configuration is active, Entra will be your default source for the **ManagerId** and **Organization** attributes. 