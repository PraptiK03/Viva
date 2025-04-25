---
title: Understand Viva Glint programs and cycles 
description: Use survey program settings to define basics for all survey cycles, like supported language or survey questions. Editing a specific survey cycle unlinks it from the overall survey program.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: survey program, survey cycle, unlinked cycle, cycle edits
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/25/2025
---

# Understand Viva Glint programs and cycles  

Microsoft Viva Glint Recurring survey programs contain multiple survey cycles that let your organization trend scores over time. Use survey program settings to define basics for all survey cycles, like supported language or survey questions. Editing a specific survey cycle unlinks it from the overall survey program.

## Survey terminology 

**Survey program**: A container that houses survey configuration settings (like available languages, confidentiality thresholds, or distribution) for its survey cycles.

**Survey cycle**: A single survey within a program tied to a specific point in time. By default, survey cycles include the month and year that they launch in their names.

**Linked**: By default, all surveys cycles are linked to the overall survey program, meaning that any changes made at the program level automatically apply to all survey cycles in the program.  

**Unlinked**: A single survey can be edited in ways that don't affect future surveys in the same program. When edits are made to a single survey, it becomes unlinked. Edits made to an unlinked survey only affect that survey. Future surveys in the same program aren't affected. Trend data is unaffected. 

## Edit a program versus a cycle

Once a survey program is set up, Viva Glint Admins can edit future surveys at the program level. Set up a series of surveys and avoid major adjustments to each survey cycle by editing at the overall program level. If untouched, the same survey emails, text, and questions are repeated with each survey cycle in the program. 

> [!IMPORTANT]
> - Edits Viva Glint Admins make at the survey cycle level only apply to the cycle and not any other survey cycles in the program.
> - Edits made at the cycle level **unlink** the cycle from the overall survey program and program updates no longer flow to the unlinked, edited survey cycle.
> - Viva Glint doesn't currently support relinking survey cycles to their overall survey program.

To edit settings for a specific survey cycle whithout affecting other future survey cycles:

1. Go to **Configuration** and select **Survey programs** in **Surveys**.
2. Select a survey and confirm that it's **Approved**.
3. In the **Upcoming and Live** section, select the survey cycle to edit. An **Edit Survey** dialog appears letting you know that any edits unlink the survey cycle from the overall survey program:

   :::image type="content" source="../../media/glint/setup/unlink-cycle-warning.png" alt-text="Screenshot of the Viva Glint confirmation dialog for editing a survey cycle and unlinking it from a survey program.":::

4. Select **Yes, edit the survey** to enter the survey cycle details page:

   :::image type="content" source="../../media/glint/setup/cycle-edit-view.png" alt-text="Screenshot of the Viva Glint survey cycle details page.":::

5. For this specific survey cycle, edit the [Distribution](distribution-program-summary.md), [Questions](questions-setup.md), or [Communications](program-summary-communications.md) and select **Save Changes**.
6. Edited survey cycles have an "Unlinked from Program" label in the survey program:

   :::image type="content" source="../../media/glint/setup/unlinked-cycle.png" alt-text="Screenshot of the Viva Glint survey cycle showing as unlinked at the survey program level.":::

   > [!NOTE]
   > Unlinked survey cycles only impact survey settings and don't affect reporting.

## Edits that require cycle-level updates

If a survey is live, and you want to adjust survey reminder send dates or add reminders, you need to [make edits at the cycle level](change-live-survey.md#communications). For other changes needed to a live survey, read [Make changes to a live Viva Glint survey](change-live-survey.md). 


