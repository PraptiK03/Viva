---
title: Preview reporting data in Viva Glint before launch
description: Use Microsoft Viva Glint's Report Preview option to confirm that your employee attributes and survey questions appear as expected in reporting before launching a survey.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva glint reports, preview demo reports, reporting preview window
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/17/2025
---

# Preview reporting data in Viva Glint before launch

Use Microsoft Viva Glint's Report Preview option to confirm that your employee attributes and survey questions appear as expected in reporting before launching a survey. Viva Glint Administrators can familiarize themselves with the Viva Glint dashboard and preview how data file attributes display scores and work as report filters. If employee data or questions don't appear as expected, make data or survey setup adjustments to finetune before survey launch.

> [!NOTE]
> Demo surveys are only available for Recurring and Ad-Hoc surveys and only visible to users in the Company Admin User Role.

## Generate a Report preview

Use the following steps to generate a preview based on your employee data, survey questions, and randomized responses. An email lets you know when the report is available; the report may take up to 24 hours to generate. Once generated, your report remains visible for seven days. 

> [!NOTE]
> Report generation requests queue up in the order that they’re requested across all surveys and users. Coordinate with other Viva Glint Admins when generating report previews.

> [!IMPORTANT]
> To ensure no unintended notifications are sent, temporarily disable Nudges or Team Conversations before proceeding.

1. Select the **Configuration symbol** and then **Survey Programs.** 
2. Select a Recurring or Ad Hoc survey and switch the survey to **Approved**.
3. In the **Upcoming and Live** tab, hover on the far right of the next scheduled survey cycle and select the ellipsis.
4. In the dropdown menu that appears, select **Preview**. 

   :::image type="content" source="../../media/glint/setup/preview-dropdown.png" alt-text="Screenshot of the preview dropdown menu within the ellipses next to a survey cycle.":::
 
5. In the **Survey Preview** dialog that appears, select **Generate Report Preview** to create a report preview based on your employee data, survey questions, and randomized responses.
   
   :::image type="content" source="../../media/glint/setup/generate-report-preview.png" alt-text="Screenshot of the *Survey Preview for Engagement* dialog box from which to select **Generate Report Preview**.":::

   :::image type="content" source="../../media/glint/setup/report-preview-generated.png" alt-text="Screenshot of the *Report Preview Generated* dialog box.":::

6. When report generation is complete, you receive an email; the report may take up to 24 hours to generate.

   > [!CAUTION]]
   > Until you receive an email, ensure that your survey program remains in an **Approved** status. Preview data doesn't generate successfully if the survey program isn't **Approved**.
   
7. To replace the reporting preview with newly uploaded employee data or survey questions during the seven-day window, return to the survey's **Survey Preview** dialog and select **Generate Report Preview** again.

## How do I see my preview data after it's generated?

Your demo data is viewable from the program listing on your admin dashboard. It shows in the list of your programs with the name of the program preceded by "Demo Data." To leave that program - and remove the demo banner from the top of your screen - use **Switch Program.**

:::image type="content" source="../../media/glint/setup/switch-programs.png" alt-text="Screenshot of how the Demo Data for Engagement program shows on the admin dashboard.":::

To view filterable reports:

1. Select **Reports.**
2. Choose **Demo Data for `<survey name>`** in the **Survey programs** list.
3. [Select a report](/viva/glint/reports/survey-reports-overview) to review.

   :::image type="content" source="../../media/glint/setup/demo-data-for-engagement.png" alt-text="Screenshot of the Viva Glint Reports tab and a Demo Data for Engagement survey to select for previewing.":::

   :::image type="content" source="../../media/glint/setup/demo-data-expiration.png" alt-text="Screenshot of a Viva Glint Executive Summary report preview with the expiration date posted at the top.":::

## Commonly asked questions

### Does the demo preview show Strengths and Opportunities? 

No. Demo data previews rely on fake response data with little variation in scores that doesn’t produce Strengths and Opportunities. 

### Does the demo preview use items selected for the upcoming cycle or all items that exist at the program level? 

The preview uses all items that are part of the next scheduled survey cycle.

### Should I create Focus Areas from demo preview dashboards? 

Any test Focus Areas show with other real Focus Areas in the platform and in exported Focus Area reports. If you do create them as a training exercise, delete them afterward.
