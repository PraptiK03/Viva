---
title: Choose your benchmark comparison data for Viva Glint reporting
description: Choosing the right comparison data when setting up feedback reporting sets the right context for understanding strengths and opportunities.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Benchmarks, global benchmark, internal benchmark, external benchmark, survey comparators, My Teams, Average Question
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 1/14/2025
---

# Choose your benchmark comparison data for Viva Glint reporting

Choosing the right benchmark comparison when considering Microsoft Viva Glint survey results sets the right context for understanding strengths and opportunities and makes the difference between effective progress and misdirected actions. Good comparison choices are crucial. Managers need to find the right comparison for understanding their engagement feedback.

Comparisons come from these sources:

- **Internal:** Compared to your organization's overall scores or another internal group
- **Historical:** Compared to previous survey results
- **External:** Compared to external benchmarks, comprised of scores across Glint customers

Use a combination of comparative data to reveal the most comprehensive information for your managers.

> [!NOTE]
> Your company may use custom terms for the Viva Glint terminology used in this guidance.

## How to change the comparison in a report

The company admin chooses the default comparison for survey data. Managers can choose to view a different comparison group to provide more context for your survey scores from any report they have access to.

1. From the **Reports** tab, choose the report and then select the **Settings** button. The **Report Settings** slider window opens.
2. Under **Comparison**, use the down-facing arrow next to change the  comparator.
3. Select **Done**.

## Understand the four comparison settings

Viva Glint provides four default options for comparison reporting. In addition to the following four settings, your company may have one or more internal comparisons configured (for example, Division or Business Unit).

|Comparator|Description|When to use|
|-------|--------|-----------|
|**Benchmark**|Provides a comparison point for feedback based on survey data compiled from all Viva Glint customers, not just within your organization.| Helpful for admins and first-time survey results analysis|
|**Company**  | Displays team scores in comparison to company-wide scores for the same questions.| Helpful for users with more than one area of responsibility|
|**My Teams** | Compares a manager's team score to an overall score derived from a filter.| This setting is the superset of access and is best used with custom access or managers with large organizations|
|**Average Question** |Presents a single, overall score for all questions and respondents within your access.| Helpful for users looking for some level of variance in their score|

## Why are comparison choices beneficial?

**Comparison scores within the platform enable you to make sense of your results.** Without meaningful comparison data, inaccurate conclusions may cause you to focus on the wrong areas for improvement.

**Algorithms built into the platform take comparative data sets into consideration**. The Glint platform intelligently highlights Strengths and Opportunities. The platform considers a combination of survey results, their impact on the outcomes you care about, and where you stand on available comparisons.

**Comparisons between groups within an organization may be helpful to score interpretation.** For groups that typically score higher relative to other groups on a set of priority questions, it may be useful to source best practices from that group. Then share them with other groups to support broad scale improvement.

## Determine which comparison data to use

Decide which comparison data can be most useful. Consider your company's overall business and measurement strategy. Consider where you are in your survey cycle - first survey, subsequent surveys, etc. In general, external benchmarks provide useful level-setting comparisons during an initial survey, but aren't as useful to your organization as internal and trend (historical) comparisons in subsequent surveys.

### When is the **internal benchmark** comparison useful?

Managers are best served by using an internal comparison, which for a team's first survey is typically the organization's **Company** scores. Internal comparisons provide a more relevant comparison for managers than an external benchmark. After an initial survey, the manager gets the most useful information by comparing team scores from one survey to the next survey. This comparison is referred to as *trend.*

**Important:**
- The internal benchmark attribute must be turned on in a User Role for that person to see this comparison in reporting.
- The internal comparison available to a user is their *current* value, which is populated in the selected attribute.

 **Example:**
  - The attribute selected for the internal benchmark is **Country,** and the user's *current* Country value is USA.
  - The user sees **USA** as an available benchmark to select in their dropdown menu.
  - The score used for comparison is calculated from the survey responses of other users whose current Country value is USA.
  - Summary for this example: comparison data is aggregated from the responses of users whose current value for the selected attribute is the same as the user's - USA. 

  **Now, let's say the user moves and their new Country value is Mexico.**
  - The internal benchmark now available in the dropdown menu is Mexico
  - The comparison score is calculated from response data of users also currently showing Mexico as their Country value in your employee data attribute file.

**For managers, using internal comparisons and their own team's trend are best practices.**

>[!NOTE]
>It is best to make attributes available for comparison that are stable over time. 

### When is the **Company** comparison useful?

Company comparisons are useful for a first survey when managers have no team trend to follow. After the first survey, managers should focus on their team's trend to see progress and where opportunities lie.

### When is an **external benchmark** comparison useful?

For an initial survey, when no historical data exists, most organizations are interested in seeing how their scores compare to an *external* benchmark. This practice is a good way to begin orient your organization to their results. Viva Glint has more than 180 survey questions with benchmark data by industry, function, or country.

As you begin to survey more frequently, trends and internal comparisons become more useful than external benchmarks. They help you make incremental improvements in areas that matter most to your teams. While the external benchmark provides a meaningful reference point in assessing overall scores, managers shouldn't focus heavily on it. 

**For Employee Lifecycle surveys**, there are external benchmarks for onboarding and exit items. Consider using internal comparisons, however, to highlight the uniqueness of your employee experience.

> [!TIP]
> Use [Viva Glint's global benchmark offerings and methodology](benchmarks.md) for external benchmarking comparisons.

### When is the **My Teams** comparison useful?

The **My Teams** comparison represents the scores for the user's total access within Viva Glint. 
- For company admins, the **My Teams** comparison is the same as the **Company** comparison since they have access to all company data.
- For a manager, **My Teams** represents the scores for everyone who reports up through them (their roll-up organization).

> [!NOTE]
> If no filter is applied to a report, the *My Teams* comparison is the same as your overall scores and will show no differences. For the *My Team*s comparison to be useful, look at filtered data (for example, subteams within the hierarchy, specific attribute groups, etc.)

The **My Teams** comparison tends to be most useful for higher level managers or those who oversee large organizations.

### When is the **Average Question** comparison useful?

Use the **Average Question** comparison under these circumstances:

- For any survey when there's no available comparisons (such as trend or external benchmark)
- For any survey where the difference between your score and others is small, such as versus **Company Overall**

In these instances, the **Average Question** score allows a comparison measurement that highlights the highest and lowest scoring items. This comparison can be used as a launching point for conversation and choosing Focus Areas.

## Tips for choosing comparisons 

- **Don't rely on external benchmarks indefinitely.** For some leaders, it's critical to understand how similar organizations are scoring. This knowledge helps them decide where to prioritize actions to deliver the same or better employee experiences. Best practice: focusing on internal comparisons over external benchmarks addresses your organization's unique strengths and opportunities.
- **Learn how to interpret differences in scores.** To determine where to take action, understand the magnitude of positive or negative differences between your scores and other comparison scores.
- **Caution small team managers on using external benchmarks as comparisons.** Benchmark data represents an average of millions of data points. External benchmarks are meant to be used for assessing organization overall scores. A better comparison for first-line managers is past survey scores (trend) for their own team or organization averages.

### Keep in mind

When comparing two groups, a group against a benchmark, or a score change over time, consider both practical and statistical significance.

- **Practical significance:** The difference in the scores between two groups that is large enough to observe unique patterns. If a score difference between two teams is too small to detect a difference, that difference doesn't carry as much practical significance.
- **Statistical significance:** The probability that the difference between the scores of two groups isn't chance or coincidence. Instead, it accurately represents the unique responses of individuals in each group. This comparison is useful with larger groups, where it can be used to surface reliable patterns in data. On your platform, Alerts and Driver Impact analysis automatically check for statistical significance and display significant results.


