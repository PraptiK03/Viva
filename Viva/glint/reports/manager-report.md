---
title: The Viva Glint Manager Report
description: "The Manager Report displays a Directs or Roll-up Hierarchy view for survey items within a specific organizational hierarchy. It is intended for use by senior leaders to see how their managers are doing"
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: senior leader report,
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/17/2025
---

# The Viva Glint Manager report in Viva Glint

The Microsoft Viva Glint Manager Report displays a **Directs** or **Roll-up Hierarchy** view of comparisons for two different survey items. These preset items are assigned during survey setup and are the default settings. To change the items, select the **question label**. Similar to other reports, column headers are static and can be used as a sorting feature. 

This report is for admins and senior leaders so they can evaluate manager engagement.

:::image type="content" source="../../media/glint/reports/manager-report.png" alt-text="Screenshot of the Manager Report access card in the admin Reports tab.":::

> [!IMPORTANT]
> To make the Manager Report available in Reports for users, their **User Role** must have your organization's Manager ID attribute selected for **Report Sections** in the role's **Report Attributes**.
>
> :::image type="content" source="../../media/glint/reports/manager-id-report-attribute.png" alt-text="Screenshot of Manager ID selected in a role's Report Attributes.":::

## Manager Report terminology

|Hierarchy|Definition|
|---------|---------|
|Directs|Displays data for all *managers* within a specific managerial roll-up hierarchy. It only displays data for employees that report directly to that manager.|  
|Roll-up|Displays data for all *employees* within a manager's hierarchy. This data includes any employees that fall below a manager in the org chart, even if they don't report directly to that manager. In other words, more levels of the organizational chart. |

## Use the Manager Report filter 

The Manager Report has a unique filter option, which isn't present in other reports. 

1. From the *Manager Report* page, select **Add a filter**.

   :::image type="content" source="../../media/glint/reports/manager-report-add-a-filter-button.png" alt-text="Screenshot of the Manager Report Add a filter button.":::

2. In the **Filter By** box, select **+ Add Filters** to open the **Select Filter Type** dropdown menu.
3. From the dropdown box, select either **Managers** or **Respondents**. 
   1. The **Managers** filter looks at your employee data attribute file for values for the manager themselves. **Manager** refers to a 
   leader with people reporting up to them at the time of the survey launch and is therefore qualified to receive survey results.
   1. The **Respondents** filter looks at all attribute values for individual employees who report into that manager.
  
   :::image type="content" source="../../media/glint/reports/manager-report-select-filter.png" alt-text="Screenshot of the Select Filter Type button.":::

4. After a user selects **Managers** or **Respondents**, a new dropdown menu displays all attributes sent to Viva Glint in your employee attribute data file. Choose the attribute you want to study. As appropriate, more dropdown menus become available to drill down the desired attribute even further.

5. Use the **Close Filter X** to remove the top section from your screen.

## Choose your report settings

1. Select the **Settings** button to open the **Report Settings** panel.
2. Viva Glint provides four default options for comparison reporting. In addition to the following four settings, your company may have one or more internal comparisons configured (for example, Division or Business Unit).

   |Comparator|Description|When to use|
   |-------|--------|-----------|
   |**Benchmark**|Provides a comparison point for feedback based on survey data compiled from all Viva Glint customers, not just within your organization.| Helpful for admins and first-time survey results analysis|
   |**Company**  | Displays team scores in comparison to company-wide scores for the same questions.| Helpful for users with more than one area of responsibility|
   |**My Teams** | Compares a manager's team score to an overall score derived from a filter.| This setting is the superset of access and is best used with custom access or managers with large organizations|
   |**Average Question** |Presents a single, overall score for all questions and respondents within your access.| Helpful for users looking for some level of variance in their score|

3. Use the **Group by** dropdown menu to choose **None, Manager,** or **Location Hierarchy**.
4. Use the **Key Metric** dropdown menu to show the report in terms of **Scores** or **Favorability**.

## Export and Share

Share your results with leaders and stakeholders in the way that works best for you. Select the **Export and Share** button for access to these options:

:::image type="content" source="../../media/glint/reports/overall-export-share.png" alt-text="Screenshot of exporting and sharing options.":::

   



