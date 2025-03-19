---
title: Use Viva Glint's Focus Area Overview report
description: "Provides a status of the completion of Focus Areas across teams, at-a-glance critical insights, and access to other details."
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: goal overview, goal report, export focus area permissions, export focus areas, roles with focus area permissions, focus areas for 360 feedback programs, development focus areas, people goals, percentage of focus area participation for managers
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 2/10/2025
---

# Use Viva Glint's Focus Area Overview report

The Microsoft Viva Glint Focus Areas Overview report provides a completion status for Focus Areas across teams. The report provides critical insights and easy access to other details. Leaders and admins use this report to connect managers working on similar Focus Areas and to view feedback comments to read context about what their managers are working on. 

>[!IMPORTANT]
>Your organization may use the word "goals," rather than our standard term "Focus Areas." For this reason, the verbiage and images on guidance may not match exactly with your dashboard.


## Grant permission for managers to view the Focus Area Overview report 

1. Open **User Roles** on your Microsoft Viva Glint admin dashboard. 
1. Approve **View Focus Areas Reports** in the **Reporting** section of **Managers Permissions and Access**. 

The report respects access at a per-person level. 

:::image type="content" source="../../media/glint/reports/reporting-view-focus-area-reports.png" alt-text="Screenshot of where to grant permissions for roles to see Focus Area reports.":::

## Access the Focus Area Overview report 

From the admin dashboard, select the **Reports** tab. From the Focus Areas column, select **Focus Area Overview**.  

   :::image type="content" source="../../media/glint/reports/focus-areas-from-reports.png" alt-text="Screenshot showing the Reports tab in the admin dashboard, highlighting the Focus Area Overview option.":::

## Report section summary 

Use this table to understand report sections and descriptions.

| Term | Description | 
|---|---|
| **Summary** | - How close are we to Focus Area completion?<br>- What’s the status of the Focus Areas? <br>- What percent of the population makes up each status?<br>- How many managers created Focus Areas?|
| **Overall Focus Area Completion** | Shows progress toward 100% Focus Area completion. View the count of Focus Areas completed and the number of employees who completed them. |
| **Focus Area Status** | Illustrates each Focus Area status and the populations they cover. Hover over each status for a deeper dive into the information.|
| **% of Employees with Focus Areas** | Shows the overall percent of managers and others with Focus Areas. Hover over the number for a deeper dive into the information. | 
| **% of Employees without Focus Areas** | Displays the percentage of employees who don't have Focus Areas. |
| **Goal Status by Type** | The breakdown of Focus Areas by type. Sections of the report are dynamic, displaying more details when you select them. |
| **Column Headers** | Select column headers, sortable by status in ascending or descending order |
| **Status Bars** | Select any status bar to include that data in the **Summary** section. This data provides other insights about the Focus Area type, specifically: <br>- Overall completion status <br>- % of  employees that don't have the Focus Area| 
| **Percentages** | To see detailed information, hover over the percentage score.|
| **Filter** | Located in the header menu at the top of the page and indicated by an arrow and any selected filters, when collapsed. <br> The selections chosen are automatically added to the filter. To view past reports or modify filters, select the arrow to expand the menu. The current Focus Area period appears by default, but you can look back at previous periods.|

## Focus Area Status by Type

People Goals and Development are terms Viva Glint uses to distinguish between two different types of Focus Area related goals:
- **Development** goals refer to 360 feedback program Focus Areas.
- **People** goals refer to Focus Areas for all other types of surveys.

:::image type="content" source="../../media/glint/setup/focus-area-overview-status-type.png" alt-text="Screenshot of Focus Area status by type.":::

### How is the percentage of Focus Area participation calculated?

The percentage calculation for the Focus Area Overview Report is based on how many users have access to the **Create Focus Areas** permission in **User Roles**. 

If a manager has one Focus Area for the Engagement Survey and one Focus Area for their 360 program, the Focus Area Overview report shows two Focus Areas created for that user. However, the manager only counts once towards the total users eligible to create Focus Areas. 

## Exporting Focus Area report data  

Export Focus Area data in two different ways: 
- From the Focus Area Overview report,
- From the admin dashboard.

### Export data from the Focus Area Overview report 

Use the **Export** menu to choose your export option. 
- **Export Focus Areas Usage to Spreadsheet**, or
- **Export All Action Items to Spreadsheet**.

   :::image type="content" source="../../media/glint/reports/focus-areas-overview-export.png" alt-text="Screenshot of the download options or exporting the Focus Area report.":::

### Export data from the admin dashboard 

1. In the **Action Taking** section, select **All Action Items Report**.
1. The report automatically generates a CSV file.

   :::image type="content" source="../../media/glint/reports/focus-area-export-csv.png" alt-text="Screenshot of the verification dialog box indicating that your csv report downloaded.":::

### What does the Focus Area Overview report include?

- Employee email 
- Employee first and family name 
- Employee Focus Area 
- Employee Focus Area period 
- Focus Area windows and due dates 
- Action item and description 
- Action item and status 
- Whether the items are a Viva Glint suggested item 
- Focus Area comments: Following the Suggested Action Item column, admins with permissions can see:
   - The number of comments supporting a Focus Area.
   - The comment, each in its own row.
 
## Learn from Viva People Science methodology

Initiating and managing action after a survey can be an unclear process. Focused and streamlined action planning is essential. An action plan is a written commitment to make incremental improvements to the employee experience. 

> [!div class="nextstepaction"]
> [Viva People Science explains focus areas and action planning](../people-science/people-science-explains-focus-areas.md)

