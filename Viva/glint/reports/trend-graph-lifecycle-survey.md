---
title: Trend scores for Viva Glint Employee Lifecycle and Always-On programs
description: Microsoft Viva Glint recurring surveys happen at definite points in time and trend based on each survey launch. But scores for  Viva Glint Employee Lifecycle (ELC) and Always-On surveys trend differently because of their ongoing nature.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: lifecycle trend, trend line, trend scores, ELC, exit trend, onboarding trend, always-on trend
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/06/2025
---

# Trend scores for Viva Glint Employee Lifecycle and Always-On programs

Microsoft Viva Glint recurring surveys happen at definite points in time and trend based on each survey launch. But scores for  Viva Glint Employee Lifecycle (ELC) and Always-On surveys trend differently because of their ongoing nature.

- ELC and Always-On surveys, by default, display scores filtered to surveys delivered in the last 90 days. 
- ELC and Always-On surveys are always active so reports group based on the date range selected and not a specific survey date, like with recurring surveys.  
- ELC and Always-On results appear in dashboards in real time and follow program confidentiality thresholds for displaying results to users who have access.

> [!NOTE]
> If program settings allow users to submit multiple surveys for an ELC or Always-On survey, they may have multiple response records in raw survey response exports. **However, aggregated reports in the platform count them only once**. [Learn more about how responses are counted in reports](#understand-how-response-numbers-show-in-elc-and-always-on-reporting).

## Date filters for reports

Users have access to multiple preset date range filters and can apply custom date ranges in ELC and Always-On survey reports. Keep in mind that:

- Survey reports use **survey delivery date** as the date type for filtering in reports.
- Dates are based on calendar year (not fiscal year) in survey reports.

:::image type="content" source="../../media/glint/reports/elc-date-filter-options.png" alt-text="Screenshot of date filter options for lifecycle surveys.":::

### Monthly versus Last 30 Days

The Survey Date section in Heat Map reports uses the start month used to calculate a score as the label for the column.

- When users select a [Monthly](#monthly) date range, the most recent month column in the **Survey Date** section shows the current month. The score date range starts and ends in the current month. In the following example, when a user filters to Monthly in March 2025, an Onboarding survey's Heat Map report shows the most recent score as "Mar 2025":

  :::image type="content" source="../../media/glint/reports/heat-map-elc-monthly.png" alt-text="Screenshot of a Viva Glint Heat Map report, filtered to a monthly view.":::
  
- When users select the [Last 30 days](#last-30-days) date range, the most recent month column in the **Survey Date** section shows the previous month. The score is using a 30-day lookback from today's date, which makes the start date for the score in the previous month. In the following example, when a user filters to the last 30 days in March 2025, an Onboarding survey's Heat Map report shows the most recent score as "Feb 2025":

  :::image type="content" source="../../media/glint/reports/heat-map-elc-last-30-days.png" alt-text="Screenshot of a Viva Glint Heat Map report, filtered to a view based on the last 30 days.":::

### Default date range

Reports for ELC and Always-On surveys default to a view of results for surveys delivered in the past 90 days. The date displayed when you hover over data points is the first day of that range - meaning that **the most recent** data point is 90 days before today's date and previous data points in trend lines display data with ranges whose start dates are 90-day increments in the past. For more information, see the following table.

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | 90 days before today's date   | 90 days before today - today                   |
| Second most recent | 180 days before today's date  | 180 days before today - 90 days before today   |  
| Third most recent  | 270 days before today's date  | 270 days before today - 180 days before today  |

### Other date ranges

Aside from the default range, users can select the following preset date ranges or enter custom dates when viewing survey results. Use these tables to determine the date ranges that are used to display scores for each timeframe.

#### Last 30 days

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | 30 days before today's date   | 30 days before today - today                   |
| Second most recent | 60 days before today's date  | 60 days before today - 30 days before today   |  
| Third most recent  | 90 days before today's date  | 90 days before today - 60 days before today  |

#### Monthly

Monthly views are based on calendar year, not fiscal year.

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | First day of current month   | First day of current month - today                 |
| Second most recent | First day of previous month  | First day of previous month - end of previous month  | 
| Third most recent  | First day of previous month  | First day of previous month - end of previous month  |

#### Quarterly

Quarterly views are based on calendar year, not fiscal year.

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | First day of current quarter   | First day of current quarter - today                 |
| Second most recent | First day of previous quarter  | First day of previous quarter - end of previous quarter  |  
| Third most recent  | First day of previous quarter  | First day of previous quarter - end of previous quarter  |

#### Custom date range

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | Start date of custom date range  | Start date - end date of custom date range              |
| Second most recent | Custom range days before start date | Custom range days before start date - custom range start date |  
| Third most recent  | Custom range days x2 before start date  | Custom range days x2 before start date - custom range days before start date |

**Example**

A user at Contoso wants to view Exit scores over time, based on six month periods. They need to select a custom date range because no preset date ranges show scores based on six month timeframes. They select July 1, 2024 through December 31, 2024.

:::image type="content" source="../../media/glint/reports/elc-custom-date-range.png" alt-text="Screenshot of a custom date range applied for a lifecycle report.":::

The previous data points on the trend line show six month scores going back in time:

| Data point  | "Surveyed on" date displayed   | Score date range|
|:----------|:-----------|:------------|
| Most recent        | Jul 1, 2024  | Jul 1, 2024 - Dec 31, 2024 |
| Second most recent | Dec 31, 2023 | Dec 31, 2023 - Jul 1, 2024 |  
| Third most recent  | Jul 1, 2023  | Jul 1, 2023 - Dec 31, 2023 |
| Fourth most recent | Dec 31, 2022 | Dec 31, 2022 - Jul 1, 2023 | 
| Fifth most recent  | Jul 1, 2022  | Jul 1, 2022 - Dec 31, 2022 |  
| Sixth most recent  | Dec 31, 2021 | Dec 31, 2021 - Jul 1, 2022 |  

The trend line in the Executive Summary Report shows data points going back in time by six month increments.

:::image type="content" source="../../media/glint/reports/elc-trend-example.png" alt-text="Screenshot of an Executive Summary Report for an ELC survey with a custom six month date range applied.":::

## Understand how response numbers show in ELC and Always-On reporting

The default report date range for ELC and Always-On surveys is 90 days. It's possible for some users in your organization to submit multiple surveys in that timeframe - the waiting period between surveys is less than 90 days. How is this data counted?

 - The response number shows for **unique users** only. Repeat survey takers count only once.
 - Multiple responses submitted by a single user are counted in the aggregate and the multiple choice report.

### Example 1

A unique user at Contoso submits an Exit survey on November 14, 2024 with a rating of 50. The same unique user submits another Exit survey on November 25, 2024 with a rating of 75.

**Reporting:**

- When isolating the results date range to include only one (1) submission for the unique user, the experience is as expected.
- When viewing only for November 14 or only for November 25, reporting reflects only one (1) respondent with scores of 50 or 75 on the separate days, as expected. 
- When expanding the results date range to include November 14-25, the "All" score is calculated as 63 (average of the unique user's two (2) submissions) and reflects one (1) respondent. 

### Example 2

A unique user at Contoso submits surveys and has a different department value for each submission:

  - November 14, 2024: Department = Software Engineering
  - November 25, 2024: Department = Customer Service
  
**Reporting:**

When users view results from November 14-25, 2024:

- Reporting reflects one (1) response but two departments.
- Each department shows their respective scores.
- "All" is reported as the average of both submissions.

