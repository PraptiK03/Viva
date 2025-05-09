---
title: Use the Viva Glint Driver Impact report
description: An engagement driver—a key driver—is a factor that directly correlates to an organization's employees' happiness at work. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: driver impact report, broader team insights, strengths, opportunities, key drivers, graph view, table view, executive summary report
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 3/28/2025
---

# Use the Viva Glint Driver Impact report

Drivers are factors that affect employee engagement. A driver's *impact* is its correlation with employee engagement in the world of work. Team and organizational **Strengths** and **Opportunities** (S&Os) are derived from Driver Impact data.

There can be a significant difference in how important a specific driver of engagement is to one team compared to another team, or to the rest of the company. For example, the engineering team's engagement level might be highly impacted by a lack of growth opportunities, whereas the overworked finance team rates work-life balance as having the highest impact. Key drivers vary within organizations and populations.

[Watch this video about using the Driver Impact Report.](https://learn-video.azurefd.net/vod/player?id=a2adbcf1-8cf0-43e5-9036-80a28ee1c5cd)

## Settings on the Driver Impact report

The default Driver Impact Report is set at the client level. Choose between an internal benchmark or an external benchmark comparison. The comparison dictates what appears on the dashboard for all reports, across all programs. Comparison groups can be changed, but report views revert to the default setting upon logging off.

## Understand the four comparison settings

One or more internal benchmark comparisons may be available to view feedback, based on how benchmarks are configured in the Reporting section of your [General Settings](/../../viva/glint/reports/survey-reports-overview) feature. 

|Viva Glint benchmark comparison option| Description| 
|---------|-----------------|
|**Benchmark** | Provides a comparison point for feedback based on survey data compiled from all Viva Glint customers. The comparison points aren't just within your organization. This comparison is helpful for admins and first-time survey results analysis.|
|**Company** |Displays team scores in comparison to company-wide scores for the same survey items. This comparison is helpful for users with more than one area of responsibility.|
|**My Teams** |Compares a team's score to an overall score derived from a user’s data access. This comparison is helpful for users with more than one area of responsibility.|
| **Average Question**| Presents a single, overall score for all items and respondents within your access. This comparison is helpful for users looking for some level of overall variance in their score.|

[Learn more about comparison data](/../../viva/glint/setup/survey-comparison-data?branch=pr-en-us-9179).

## Derive Strengths and Opportunities (S&Os) from the Driver Impact report

The algorithm used to identify S&Os is composed of item scores, impact on engagement, and relativity of the score to a benchmark comparison. 

**Strengths** are areas that the team should celebrate. 
>
**Opportunities** are areas the team should work on to improve overall engagement (or the survey's intended key outcome).

[Watch this video for a quick summary of Strengths and Opportunities](/viva/glint/reports/act-strengths-opportunities).

To determine a driver's impact, individual survey responses are analyzed to determine how closely aligned scores are to each driver and to the outcome variable, typically engagement. 

**A driver's impact is classified as *high* when this is true:**
- Employees who rate a driver high, also rate engagement high
- Employees who rate a driver low, also rate engagement low

If a driver's score isn't related to engagement, then it has *low* or *zero* impact. Knowing which drivers have a high impact allow managers to focus on improving the scores of drivers which matter most.

## View Strengths & Opportunities versus Company

Managers should look at the Strength & Opportunity report before looking at the *Company* or another internal comparison. While *Benchmark* is a valuable comparison, most often *Company* is more informative, as the comparison is internal.

>[!TIP]
>- A manager with scores **below** company average should focus on the items with the biggest gaps. These items reflect the greatest opportunity for improvement. For this reason, the **Take Action** button defaults to the Opportunities section of the S&O report.
>
>- To gain a sense of what areas need attention, a manager with scores **above** the company average can change to view S&Os versus *Benchmark.*

If you're looking at *Company* results* and the default comparison is also *Company*, the driver analysis shows *Average Question* as the comparison - otherwise there would be no comparison ratio.

### Apply filters

Applying filters allows leaders to look at Strengths and Opportunities for specific groups. To apply a filter:

1. Select the filter symbol at the top of the page.
2. Select **+ Add Filters.**
3. From the dropdown menu, choose a filter from the **People** or **Question Responses** section.

## Driver Impact graph view

When a user navigates to the Driver Impact Report, the default view is graph format. The graph plots each driver's impact on the x-axis and the selected comparison on the y-axis. The comparison can include an internal benchmark or an external benchmark.

Items on the right side of the graph have a high statistical correlation with the selected outcome, typically engagement or eSat, across all respondents in a group. Often a person rates a driver and its corresponding outcome the same. For this reason, acting on those items likely has the biggest impact on engagement or the selected outcome.

In determining S&Os, the platform considers the distance to the comparison point and the impact on the key outcome. Only items with a **High** or **Very High** impact are considered when determining S&Os. The items highest in relation to the comparison are marked as Strengths. The items that are lowest in relation to the comparison are marked as Opportunities. Based on this analysis, a rank ordered list of items is displayed:

- Relative Strengths are indicated by points with a **bold white dot**.
- Relative Opportunities are indicated by a **red dot**.

> [!IMPORTANT]
> - The S&Os section is hidden on a user's dashboard if there are less than two eligible items ranked. This instance happens when:
>   - There are insufficient results
>   - All items have low or medium impact
>   - A user is on a report filtered to only one item

## Driver Impact table view

The Driver Impact table view displays the top three S&Os exactly as managers see them on their S&O report. Select **Show more** to display all S&Os. Select **Show less** to hide them.

The circle next to each driver's name indicates the impact level and score in relation to the comparison:

- A filled circle indicates the highest impact.
- A partially filled circle indicates relatively lower impact.
- Blue indicates that the item scored above the comparison.
- Red indicates that the item scored below the comparison.

 Table view example:

 :::image type="content" source="../../media/glint/reports/driver-impact-example.png" alt-text="Screenshot of a table view of the Driver Impact report.":::

## How small teams can use the Driver Impact report

The algorithm used to determine Driver Impact scores includes a statistical test to determine if enough data exists to establish a significant correlation. 

**A minimum number of 20 respondents is the default threshold to determine whether impact scores show for a team.** Managers of teams that don't meet the minimum number of respondents see their S&Os based on the impact calculated at the *Company* level. This method provides the most statistically sound results.

Key points for managers with fewer than 20 respondents:

- S&Os on the dashboard are the areas a manager's team scored relatively high or low on, in relation to the comparison. These areas have the strongest impact on engagement at the larger company level. The impact isn't reflective of your team specifically. The dashboard doesn't show impact scores at the team level if there are fewer than 20 respondents.
- One manager's S&Os may be different from other leaders within their organization.
- If enabled, include [Broader Team Insights (BTI)](/viva/glint/reports/broader-team-insights) into conversations to promote an understanding of what drives engagement.

