---
title: Use Viva Glint cross-program intelligence to filter results across survey programs
description: Microsoft Viva Glint cross-program intelligence surfaces patterns across separate survey programs, giving HR and leaders a holistic understanding of the employee journey.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: advanced filtering, cross-program intelligence, cross-program filter, cross-program analysis
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/10/2025
---

# Use Viva Glint cross-program intelligence to filter results across survey programs

Microsoft Viva Glint cross-program intelligence is an advanced filtering option in Viva Glint that allows users to filter across multiple surveys' results to answer your organization's complex employee sentiment questions. This feature can surface patterns across separate survey programs, giving HR and other leaders a holistic understanding of employee feedback. For a given survey program, users can filter by another survey program's:

- attribute values
- question responses
- comment topics and sentiment

> [!NOTE]
> To use cross-program intelligence, users need to be in a role with **Cross-Program Advanced Filtering** enabled in the role's **Permissions and Access** section.

## Confidentiality

Viva Glint’s cross-Program intelligence always honors the stricter confidentiality threshold between two survey programs to always meet data protection expectations set with participants when they took the survey. 

With cross-program filtering, users can filter by attributes and demographics but also by question responses and comment sentiment and topics. To protect confidentiality in these analyses, there's 'always a baseline threshold of 10 respondents for scores and 20 for comments. 

## Example use cases

Your organization can use cross-program intelligence to explore topics like: 

- How engaged employees are who onboarded in the last 90 days.
- Which manager qualities might explain employee exit reasons.
- Whether employees rate engagement higher depending on their Microsoft 365 Copilot usage.

> [!TIP]
> - **Survey results and filtering**: Ensure that you select the appropriate surveys to view results for and surveys to filter by. For example, to view exiting employees' reasons for leaving when their engagement scores are high, go to reports for an Exit survey and use Engagement question responses as filters.
> - **Timeframes**: Select timeframes for surveys that are close enough to give good results. For example, if you select Exit survey results for July 2024, make sure that the survey that you use as a filter is for the same timeframe.

## How to filter with cross-program intelligence

Learn how a user can filter by another survey program's question responses using engagement ratings compared to Microsoft 365 Copilot usage as an example.

1. From the **Dashboard**, select **Reports**.
1. In the menu on the left, select the survey that you want to see results for. In this case, choose the Microsoft 365 Copilot Impact Survey to find out if more engaged employees have higher Copilot usage.  
1. Select the **Executive Summary Report** and select the filter pane at the top to expand it.
1. Select **Advanced** in the top right of the filter pane and choose **Yes, enable advanced filtering** in the dialog that appears.
  
   :::image type="content" source="../../media/glint/reports/enable-advanced-filtering.png" alt-text="Screenshot of the enable advanced filtering dialog.":::

1. On the left side of the filter panel, the November 2022 Copilot survey is selected. On the right side of the filter panel, select the **plus (+)** icon and choose the December 2022 Engagement program (the most recent Engagement survey).
  
   :::image type="content" source="../../media/glint/reports/cross-program-filter-applied.png" alt-text="Screenshot of cross-program filtering with the Engagement Dec 2022 survey selected as a filter.":::

1. To filter Microsoft 365 Copilot Impact Survey results by Engagement survey responses, select **+Add Filters** and choose **Question Responses**.

   :::image type="content" source="../../media/glint/reports/cross-program-intelligence-question-filter.png" alt-text="Screenshot of cross-program filtering by question response with the Engagement Dec 2022 survey.":::

1. In the **Question Responses** filter, choose **eSat**, select **Favorable**, and select **Done**.
  
   :::image type="content" source="../../media/glint/reports/cross-program-esat-filter-applied.png" alt-text="Screenshot of cross-program filtering with the Engagement Dec 2022 survey and eSat favorable responses selected as filters.":::

1. After applying filters, select **Close Filters x** to collapse the filter pane.
1. Go to the Questions section in the **Executive Summary Report** and note the Copilot Usage breakdown for Engagement survey takers who responded favorably. High percentages of engaged users report that they use Microsoft 365 Copilot "Daily" (42%) or "A few times per week" (46%).
   
    :::image type="content" source="../../media/glint/reports/copilot-usage-fav.png" alt-text="Screenshot of Copilot usage response breakdown filtered by Engagement Dec 2022 favorable eSat responses.":::

1. To view Copilot usage for respondents that scored negatively or neutrally for engagement, in the **Question Responses** filter, choose **eSat**, select **Favorable** and **Neutral**, and select **Done**.

   :::image type="content" source="../../media/glint/reports/cross-program-esat-filter-applied2.png" alt-text="Screenshot of cross-program filtering with the Engagement Dec 2022 survey and eSat negative and neutral responses selected as filters.":::
  
1. Go to the Questions section in the **Executive Summary Report** and note the Copilot Usage breakdown for Engagement survey takers who responded negatively or neutrally. High percentages of engaged users report that they use Microsoft 365 Copilot "Less than monthly" (45%) or "Never" (55%).
   
    :::image type="content" source="../../media/glint/reports/copilot-usage-unfav.png" alt-text="Screenshot of Copilot usage response breakdown filtered by Engagement Dec 2022 negative and neutral eSat responses.":::   


