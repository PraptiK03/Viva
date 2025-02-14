---
title: Color coding in Viva Glint reports
description: Color coding logic differs in various Viva Glint reports. Learn why here.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: strengths, opportunities, team summary, executive summary
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/04/2025
---

# Color coding in Viva Glint reports

Color coding logic differs between the manager Team Summary report and other executive summary report options. 

## Color coding for Strengths & Opportunities in the Team Summary report

In a manager's Team Summary report, a color is assigned to item scores which are considered Strengths or Opportunities (S&Os). An impact analysis is conducted for each driver item to determine its impact on the outcome (typically, Engagement).
-	Items with High or Very High impact are considered potential Strengths or Opportunities.
-	Items with Low or Medium Impact aren’t considered either a Strength or an Opportunity. These items are colored **gray.**
-	The outcome items - typically the items that comprise the Engagement Score - are colored **gray.**

Items with High or Very High Impact on the outcome (for example, Engagement) are first compared to the benchmark selected. Then, the difference for each item from the benchmark is ranked to determine which are Strengths or Opportunities.

**Blue:** Half of the items with scores highest above the benchmark are considered **Strengths.** 
> [!NOTE]
> It’s possible that some items are both below the benchmark *and* displayed as Strengths. Not all items considered Strengths may score above the benchmark. 

**Red:** Half of the items with scores furthest below the benchmark are considered **Opportunities.** 
> [!NOTE]
> It’s possible that some items are both above the benchmark *and* displayed as Opportunities. Not all items considered Opportunities may score below the benchmark.
> 
> [!TIP]
> To decrease confusion, there is an account setting called **Exclude Negative Strengths & Positive Weaknesses** which can be enabled at the account level. 

> [!NOTE]
> If the respondent size of the report is too small, impact is calculated based on the overall company level. [See this guidance to learn more](/../../viva/glint/reports/driver-impact-report#small-teams-can-use-the-driver-impact-report). 


## Color coding for Strengths & Opportunities sections in Executive Summary reports

The processes to determine which items are Strengths or Opportunities are identical to the process described for the manager’s Team Summary Report. **There is an exception related to color coding.** 
- In these report tables, a blue or red dot is displayed next to each strength and opportunity.
  - Blue dots represent items above the benchmark.
  - Red dots represent items below the benchmark. 

**If most items are below the benchmark:**
- Strengths may have a red dot indicating the item is below the benchmark. 
- Opportunities may have a blue dot, if most of the items are above the benchmark, 

## Color coding for the Favorability Scale

Favorability is calculated from responses that fall within a specific range along the rating scale.

Glint’s best practice is to use a 5-point rating scale. The color representation looks like this:
-	**Blue** represents the percentage of respondents who scored a question 4 or 5. 
-	**Red** represents the percentage of respondents who scored a question 1 or 2.
-	**Gray** represents the percentage of respondents who scored a question 3.

## Color coding for the Heat Map report

The colors in the Heat Map allow quick identification of systemic patterns and outliers. Color coding is relative and not absolute. To determine the relative coloring in a Heat Map, Glint looks at the range of scores displayed:

- Maximum and minimum scores are always displayed as dark blue and dark red.
- Scores between the maximum and minimum are evenly bucketed in up to seven differently colored buckets. The median score shows in gray.

For example: If the minimum and maximum scores are 52 and 80, then Glint creates seven evenly spaced buckets between 52 and 80.
- Dark red indicates scores from 52-55, inclusive
- Dark blue indicates scores 77-80, inclusive
- Gray indicates scores from 64-68, inclusive. The other shades show scores in between:
- To read the changes and differences:
  - The middle gray is used for 0 change or difference
  - Dark red shows the biggest negative difference/change
  - Dark blue shows the biggest positive change
  - The other color buckets are evenly spaced between the maximum/minimum values, with zero on either side.

