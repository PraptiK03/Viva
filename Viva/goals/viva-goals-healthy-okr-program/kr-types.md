---
ms.date: 12/06/2024
title: Define KR Types in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:
  - m365initiative-viva-goals
  - vg-bestpractice
search.appverid:
- MET150
description: "Learn how to set key result types while creating Objectives and Key Results (OKRs)."
---

# Use key result types in Viva Goals

Using Objectives and Key Results (OKRs) in Viva Goals provides a foundation for setting and tracking progress toward your organization's goals. The objectives are the overarching goals, while key results are the particular outcomes you need to achieve to reach those goals. There are three categories of key results, including:

 - Quantity-type or *regular* key results, which measure progress from one point to another.
 - Quality-type or *control* key results, which act as guardrails to help you monitor consistency and efficiency.
 - *Baseline* key results, which establish the standard by which you measure progress.

## Regular key result types

Use regular key result types when you're trying to achieve a specific metric. There are three categories:

1. *Reach:* Use this metric when you're starting at zero and have a specific target that you want to *reach* or achieve. An example is "Conduct five internal surveys" or "Gain 500 users for our new community site."
1. *Increase from:* Use this metric when an OKR requires tracking a metric that's already reached a specific number or level and must increase. An example is “Increase revenue from $20 million to $40 million this year.” In this example, *from* is the starting value of $20 million and *to* indicates the target value of $40 million.  
1. *Decrease from:* Use this metric when the OKR requires tracking a metric that's already at a certain number but which needs to be reduced even further. An example is “Reduce P0 bugs from 50 to 10 this quarter.” In this example, the starting value is higher than 50, while 10 is the target value.  

## Control key result types 

Use control key result types when you must maintain key results above or below a specified threshold value to preserve a metric's quality and establish guardrails for accepted results. There are two control metrics:  

1. *Stay below:* Use when a metric must remain *below* a certain threshold. An example is “Keep customer churn below $100,000.” The only input is the target value, which acts as a threshold for success.
1. *Stay above:* Use when a metric must remain above a certain threshold. An example is “Keep the customer net promoter score above nine.” The only input is the target value, which acts as a threshold for success.

#### Add risk thresholds to control metrics

You can optionally add a risk threshold value to control metrics, which specifies above or below which values you'll address or accept risks. You can configure: 

1. *Behind* status: Any check-ins that fall between the risk threshold value and the final target value receive a *Behind* designation. 
1. Accepted risk threshold value: For *stay above* key results, the risk threshold must always be less than the key result's final target value. Conversely, for *stay below* key results, the risk threshold must always be larger than the key result's final target value.

## Baseline key result types

Use baseline key result types when you want to establish a standard or criteria with which to measure progress. The *find a baseline* key result type is useful when you want to measure a goal that you're tracking with other key results, but for which you don't know the value. 

An example is "Measure baseline customer retention rate" that you want to track during a specific period, even though you don't know the starting or target metric because you haven't previously tracked it or can't be certain what to set it at. 

## Set key result types in Viva Goals

To configure key result types, select **More options** (the ellipsis) next to an OKR and:  

1. Select **Add child items**, and then select **Add key result**. The **New Key Result** window opens, in which you must provide a title for your new key result.
1. Select:
   - **Progress and Status** to configure whether you want to manually update progress and status or configure it to occur automatically.
   - **Add Metric** or **Remove Metric** to configure metrics and phased targets or remove existing ones. If you want to implement a new metric, enter a name for it and then select the appropriate option from the **Target is to** drop-down menu.
   - **Details** to modify data about a key result, including the owner, it's applicable time period, the team to which it applies, view and edit permissions for it, and add tags.
 
    :::image type="content" source="../../media/goals/add-key-result.png" alt-text="Screenshot that shows how to add a key result." lightbox="../../media/goals/add-key-result.png":::

2. In the 'Create Key Results' quick view page that appears, enter the title of the key result.
3. Select **Add metric** that appears below the title.

    :::image type="content" source="../../media/goals/add-metric-button.png" alt-text="Screenshot that shows where to find the add metric button." lightbox="../../media/goals/add-metric-button.png":::    
    
4. Enter the target name and choose the appropriate KR type using the **Target should** dropdown.

    :::image type="content" source="../../media/goals/target-should-dropdown.png" alt-text="Screenshot that shows the various KR types under the target should dropdown." lightbox="../../media/goals/target-should-dropdown.png":::
    
5. Depending on the KR type, enter the target values and select **Create**.

    :::image type="content" source="../../media/goals/create-kr-button.png" alt-text="Screenshot that shows the create button to save your changes and create your Key Result." lightbox="../../media/goals/create-kr-button.png":::

> [!NOTE]
> You can also edit or set a type for an existing key result by selecting **More options** (the ellipsis) next to a key result, and then selecting **Edit**. The **Edit Key Result** window opens, in which you can modify the existing data and add metrics and targets, among other information. 

## Progress and Status Calculation

Progress and status calculations in Viva Goals vary depending on the key result categories—regular KR types and control KR types.  

### Progress status calculation for regular KR types

Progress and status for the regular KR types are determined by two types of progress:

**Expected progress:** Viva Goals calculates expected progress based on the start and end date of an OKR. At the beginning of the time period, the expected progress is 0% and at the end of the time period the expected progress will be 100% 

**Actual Progress:** Actual progress is calculated based on the check-ins made on the OKR. There are three ways check-ins can be made:

1. Manually
1. From a data source (Integration)
1. Roll up from Key results

### Status calculation for regular KR types

There are two ways in which status can be determined.

1. **Derive Status based on Actual Progress:** Status of the OKR is set based on the actual progress made via automatic progress updates.
2. **Manually Update Status:** Users can manually update the status of the OKRs by making check-ins. This overrides the status set automatically by Viva Goals based on progress updated via roll-up from key results or via a data source.

[Learn in detail how the progress and status are calculated for regular KR types](/viva/goals/track-okr-progress-status).

## Progress status calculation for control KR types

Progress and status for the control KR types Stay below and Stay above are calculated as follows: 

**Stay below:** 

If the current metric value is less than the threshold or target value, then the progress of the OKR is set to 100%, and the status is set to “On Track”. 

Let's take the example key result "Keep churn below 100k" as shown in the image below. The progress graph includes a point in the graph that represents a check-in. Each check-in made will be represented as a point in the graph.

:::image type="content" source="../../media/goals/on-track-stay-below-kr.png" alt-text="Screenshot that shows the progress graph for a stay below KR that's on track." lightbox="../../media/goals/on-track-stay-below-kr.png":::

The red dotted line indicates the border value below which the progress points must be in order to be "On Track."

Similarly, if the value is greater than or equal to the threshold or target value, then the progress of the OKR is 0% and the status is set to “At Risk.”

Let's take the example key result "Maintain page response time below 2 seconds." As shown in the image, the current progress or check-in made is depicted as a point in the graph.

:::image type="content" source="../../media/goals/at-risk-stay-below-kr.png" alt-text="Screenshot that shows the progress graph for a stay below KR that's at risk." lightbox="../../media/goals/at-risk-stay-below-kr.png":::

Since it's greater than the border value of 2, it lies above the red dotted line and in the shaded area that represents "At Risk." This indicates that the status of the key result is "At Risk."

> [!NOTE]
> Any check-in or progress point that lies on the red line or in the shaded grey area is "At Risk" while those that lie in the white area are **On Track.**

**Stay above:**

If the value is greater than the threshold value, then the progress is set to 100% and the status is “On Track.”

Let's consider the key result "Ensure NPS stays above 9." where 9 is the border value represented by the red dotted line as shown in the image below. Each point in the graph represents a check-in. Since the point lies in the white area above the dotted line, the progress status is "On Track" as the white area represents "On Track."

:::image type="content" source="../../media/goals/on-track-stay-above-kr.png" alt-text="Screenshot that shows the progress graph for a stay above KR that's on track." lightbox="../../media/goals/on-track-stay-above-kr.png":::

If the value is equal to or less than the threshold value, then progress of OKR is 0% and status is set to “At Risk”. 

Let's take the example of the following key result: "Maintain average FCSAT score above 8." Here, 8 is the border value represented by the red line. Since the current progress value is 7.8, which is less than the border value, the progress point is shown to be present in the shaded grey area. This area represents "At Risk" and so, the status of the key result is "At Risk."

:::image type="content" source="../../media/goals/at-risk-stay-above-kr.png" alt-text="Screenshot that shows the progress graph for a stay above KR that's at risk." lightbox="../../media/goals/at-risk-stay-above-kr.png":::

For control KR types, there's no notion of “Behind” since we consider these KR types as met or unmet. 

## How does roll up happen for control KR types?

Based on the progress of the control metric-type key result (either of 0% or 100%), the value is rolled up from the child KR to the parent objective.

If you want to turn off roll-up, this can be done by making the contribution of each key result to 0%. Here's how:

1. Right-click on or select the parent objective and select **Manage contributions**. 

    :::image type="content" source="../../media/goals/manage-contributions-button.png" alt-text="Screenshot that shows where to find manage contributions." lightbox="../../media/goals/manage-contributions-button.png":::
    
2. Changing the corresponding KRs to 0% and select **Save**.  

     :::image type="content" source="../../media/goals/manage-contributions.png" alt-text="Screenshot that shows roll-up being disabled for a few Key Results." lightbox="../../media/goals/manage-contributions.png":::   
    
## Status calculation for baseline key results  

Baseline key results don't have a notion of progress associated with it, but have statuses, which are different from the other types of key results. 

The statuses for baseline key results are: **Not started, In-progress, Closed, Postponed.** Whenever there's a check-in value associated with a baseline type of key result, the status is automatically updated to ‘in-progress’. The user must manually update the status of the Key result to any other state such as closed or postponed. 

**Roll up:** If the parent key result created and the children key result created under the parent are all of type baseline, then the sum of values from the children is rolled up to the parent.

## FAQ (Frequently Asked Questions)

**Q: After adding risk threshold to an existing control metric the status will automatically change to Behind?**
**A:** No, only the next time when you make a check-in or edit the values, will the status get updated to **Behind** until then it will continue to stay **At-risk** or **On-track** only whatever the status was before the risk threshold was added.
