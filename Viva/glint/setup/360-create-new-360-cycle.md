---
title: Create a new 360 program or cycle
description: 360 programs contain cycles that can be cloned to use on a set schedule.
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: duplicating 360 cycle, copying 360 cycle, cloning 360 cycle, name new 360 cycle
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 2/11/2025
---

# Create a new 360 program or cycle

360 programs contain cycles that can be cloned to use on a set schedule. Follow this process:

1. From your manager dashboard, select **360 Feedback Programs**.

1. Select the **+ New 360 Program** button from the All 360 Programs page.

1. Now choose the **Glint Manager 360 Program template** or the blank template. Hover over the card and select **New Program**. 

1. An untitled program page opens with a new card which displays the current month and date. In the row above the card, name the program by selecting the **pencil symbol**. Navigate back to the **All 360 Programs** page and you see your new program listed.

## Use the Actions dropdown menu

:::image type="content" source="../../media/glint/setup/360-actions-menu.png" alt-text="Screenshot of the 360 Actions menu.":::

Open the **Actions** dropdown menu to:

### Duplicate your program
Only the most recent cycle settings copy. No program history, schedules, or participants are included.

### Add or edit admin access 
Easily add a group of admins included in a pre-existing role.

### Update language settings
Select **Language Settings** to confirm:
- Additional Survey Languages: Options available to feedback providers
- Default Survey Language: The default survey language
- Dashboard Languages: Options available to subjects when selecting feedback providers and focus areas

:::image type="content" source="../../media/glint/setup/360-language-settings.png" alt-text="Screenshot of the 360 *Language Settings* window.":::

Now it's time to set up an individual cycle.

## Create a new 360 cycle

1. Select **Create New Cycle**.
1. In the **Choose a past cycle to copy from** window, select a cycle to clone. All settings copy except for Schedule & Communication, reminders and subjects.
2. Use the **pencil symbol** to name your copied template. Give cycles unique names in order to differentiate between them. Only admins see cycle names. Cycle names don't appear on the user interface or on reports.
3. The new cycle displays in the **Cycle Name** column.

## Set up cycle settings 

> [!TIP]
> Although **Manage Subjects** appears first on the cycle page, set up **Cycle Settings** first. There are five areas to set up. As you move through them, a filled blue circle confirms their completion. Circles will appear complete if the cycle is cloned. Review for editing, as needed.

:::image type="content" source="../../media/glint/setup/360-cycle-settings-first.png" alt-text="Screenshot of the five sections to configure in Cycle Settings.":::

### The Basics

There are three sections to configure:
- The Basics
- Feedback provider category settings and confidentiality
- Feedback provider response information

:::image type="content" source="../../media/glint/setup/360-the-basics-2.png" alt-text="Screenshot of the first section to configure in Cycle Settings.":::

### Feedback Provider Category Settings and Confidentiality

:::image type="content" source="../../media/glint/setup/360-categories-confidentiality-2.png" alt-text="Screenshot of the second section to configure in Cycle Settings.":::

Select up to six feedback provider categories. 
- Standard categories automatically prepopulate feedback providers based on Manager Hierarchy.
- Remove the Direct Reports category for individual contributor (IC) subjects.
- **Or** ask IC subjects to skip adding feedback providers for the Direct Reports category for cycles with both managers and ICs.

>[!TIP]
> To ensure a true 360 view, choose at least three feedback provider categories, in addition to Self.

|Feedback provider category|Minimum confidentiality threshold|Can subject or admin edit prepopulated feedback providers?|How assigned|
|----------|:-------------:|:-------------:|-------------|
|Self| 1|No|Required - All 360 subjects require a subject self assessment|
|Manager|1|Yes|Prepopulates with the subject's direct manager|
|Skip Manager|1|Yes|Prepopulates with the subject's direct manager's manager|
|Direct reports|3*|Yes|Prepopulates with the subject's direct reports|
|Peers|3*|Yes|Prepopulates with people who have the same direct manager as the subject|
|Custom|1|N/A|Not commonly used, but could be used for a *dotted line manager* or *mentor* feedback|
|Custom|3*|N/A|Commonly used for *Collaborators*|

> [!IMPORTANT]
> *At least three feedback providers must respond at the *survey level* to show feedback in a subject's report. This requirement isn't applicable at the *question* level.

#### Edit a feedback provider category

**Hover over and choose a category** to open the **Edit window** for that category, which looks like this example:

:::image type="content" source="../../media/glint/setup/360-edit-provider-category-2.png" alt-text="Screenshot of an example of a window that opens to edit a feedback provider category.":::

Edit each field as you’d like. When editing in another language that's available in the dropdown menu, that language saves so you can come back to it later if further edits are needed.

#### Confidentiality Statements

You can increase the confidentiality threshold for some feedback provider categories, but you can’t decrease the threshold less than the default values.

Dependent on the provider category, provider response information settings, and whether your organization included a privacy policy link in General Settings, the 360 confidentiality statement users see varies. [Learn more about Viva Glint 360 privacy and confidentiality](https://go.microsoft.com/fwlink/?linkid=2230922).

### Feedback Provider Response Information

This setting can’t be edited once a cycle is live. Choose between:
- **On** (default): Subjects see feedback providers and if they've responded. In reports, subjects see which feedback providers responded per category, but responses aren't tied to individual names.
- **Off**: Subjects see feedback providers but not whether they've responded. In reports, they see only the number of feedback providers who responded.

:::image type="content" source="../../media/glint/setup/360-provider-response-info-2.png" alt-text="Screenshot of the Feedback Provider Response Information window.":::

Select **Save** when you're done configuring the page.


## Delete a program
All settings and cycles associated with this program are deleted. This step can't be undone.


