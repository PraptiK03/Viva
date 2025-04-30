---
title: Create a new Viva Glint 360 program and cycle
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
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 4/30/2025
---

# Create a new Viva Glint 360 program and cycle

360 programs contain cycles which can be cloned to use for other groups. 

## Create a new 360 program

1. From your admin dashboard, select **360 Feedback Programs**.
1. Select the **+ New 360 Program** button on the All 360 Programs page.
1. Now choose the **Glint Manager 360 Program template** or the **blank template.** Hover over the card and select **New Program**. 
1. An untitled program page opens.
   -  A card displays the current month and date. **This automatically generated and populated card represents the first cycle of your program.**
   -  In the title row, name the program by selecting the **pencil symbol**. Delete the dummy information to name your program.
   -  In this example, we created a **360 for Small Team Managers** program. It automatically populates the first cycle, in this case "February 2025." The cycle shows as both a card and in the row under the Cycle Name column.
   
      :::image type="content" source="../../media/glint/setup/360-small-teams-program.png" alt-text="Screenshot of the Create a 360 program and cycle page.":::

1. Navigate back to the **All 360 Programs** page to confirm that your new program is listed.
   
   :::image type="content" source="../../media/glint/setup/360-all-programs.png" alt-text="Screenshot of the 360 All Programs page confirming your new program is created.":::

### Use the Actions menu

:::image type="content" source="../../media/glint/setup/360-action-menu-2.png" alt-text="Screenshot of the 360 program action menu-2360-action-menu-2.":::

Open the program **Actions** dropdown menu to:

- **Duplicate your program:** Only the most recent cycle settings copy. No program history, schedules, or participants are included. Select **Duplicate Program.** Select **Save Changes**.
- **Add or edit admin access:** Easily add a group of admins included in a preexisting User Role. These are defined in User Roles on your admin dashboard. Select **Save Changes**.

- **Update language settings:** Set your default language and other languages for this program:
  - **Additional Survey Languages:** Options available to feedback providers
  - **Default Survey Language:** The default survey language
  - **Dashboard Languages:** Options available to 360 participants when the log in to Viva Glint. Languages are preset in General Setting from your admin dashboard.
  Select **Save Changes**.

  :::image type="content" source="../../media/glint/setup/360-language-settings.png" alt-text="Screenshot of the 360 *Language Settings* window.":::

- **Delete:** All settings and cycles associated with this program are deleted. This action can't be undone. Select **Delete Program** to confirm.

### Create a 360 cycle

Your first cycle is automatically added to the page. Now select **+ New Cycle.**

:::image type="content" source="../../media/glint/setup/360-new-cycle.png" alt-text="Screenshot of the 360 New Cycle button.":::

1. From the dialog box that opens, use the dropdown menu to select the cycle to copy. Select **Create New Cycle**. In this example, only the first cycle is available as no others are created.

   :::image type="content" source="../../media/glint/setup/360-february.png" alt-text="Screenshot of the Choose a past cycle to copy from window.":::

1. Now, on the **Cycle** page you see the **Copy title.** Use the **pencil symbol** to rename your new cycle. Let's rename this cycle **May 2025:**

   :::image type="content" source="../../media/glint/setup/360-may.png" alt-text="Screenshot of renaming a program cycle.":::

1. Use the left-facing arrow to navigate back to the **Program** page to confirm that your new cycle is created. The cycle also shows in the **Cycle Name** column.

   :::image type="content" source="../../media/glint/setup/360-confirm-new-cycle.png" alt-text="Screenshot of the 360 Program page with the original cycle and a new cycle.":::

#### Edit cycle settings 
 
> [!TIP]
> Although **Manage Subjects** appears first on the cycle page, set up **Cycle Settings** first.

Select the new cycle to configure. All settings from the copied schedule populate, except the Schedule & Communication page, reminders, and 360 subjects. There are five pages to set up. As you move through each page, a filled blue circle confirms their completion. The first four rows appear complete in a cloned cycle. 

:::image type="content" source="../../media/glint/setup/360-cycle-settings-first.png" alt-text="Screenshot of the five sections to configure in Cycle Settings.":::

>Here's an example of the **May 2025** cycle page:
>
>:::image type="content" source="../../media/glint/setup/360-may-cycle-setup.png" alt-text="Screenshot of the setup page for a new cycle." lightbox="../../media/glint/setup/360-may-cycle-setup.png":::

## Setup page

There are three sections to review. The sections are preconfigured for you.

### The Basics Setup

Define the basics and feedback provider category settings. Define these fields:
- Program name: The overall name for the program
- Cycle name: Add a date or an identifying description for each specific cycle
- Display name: The name used in all references to this 360 cycle for subjects, feedback providers, and report recipients.
- Description: An internal note with details about this program

#### Manage translations in The Basics

Select **Manage Translations** to open **The Basics Translations** slider panel. Each translation added autosaves after selecting the next language.

### Feedback Provider Category Settings and Confidentiality

To ensure a true 360 view, choose at least three feedback provider categories, in addition to Self. Edit each category as needed. When editing in another language from the dropdown menu, that language saves so you can come back to it later as needed. Hover over and select the row to open the **Edit** slider panel.

From the copied cycle, up to six feedback provider categories are preset. 
- Standard categories automatically show feedback providers based on Manager Hierarchy.
- Remove the Direct Reports category for Individual Contributor (IC) subjects.
- **For cycles with both managers and ICs,** ask subjects to skip adding feedback providers for the Direct Reports category.

|Feedback provider category|Minimum confidentiality threshold|Can subject or admin edit prepopulated feedback providers?|How assigned|
|----------|:-------------:|:-------------:|-------------|
|Self| 1|No|Required - All 360 subjects require a subject self assessment|
|Manager|1|Yes|Prepopulates with the subject's direct manager|
|Skip Manager|1|Yes|Prepopulates with the subject's direct manager's manager|
|Direct reports|3*|Yes|Prepopulates with the subject's direct reports|
|Peers|3*|Yes|Prepopulates with people who have the same direct manager as the subject|
|Custom|1|N/A|Not commonly used, but could be used for a *dotted line manager* or *mentor* feedback|
|Custom|3*|N/A|Commonly used for *Collaborators*|

***At least three feedback providers must respond at the *survey* level to show feedback in a subject's report. This requirement doesn't apply at the *question* level.**

### Confidentiality threshold

You can increase the confidentiality threshold for some feedback provider categories, but you can’t decrease the threshold to less than the default values.
The 360 confidentiality statement users see varies. The statement is dependent on the provider category, provider response information settings, and whether your organization included a privacy policy link in General Settings. [Learn about Viva Glint 360 privacy and confidentiality](/viva/glint/setup/viva-glint-survey-privacy).

>Here's an example of the **Edit Manager** slider panel, where the confidentiality statement can be edited:
>
>:::image type="content" source="../../media/glint/setup/360-edit-confidentiality.png" alt-text="Screenshot of the Edit Manager slider panel." 

### Feedback Provider Response Information

This setting can’t be edited once a cycle is live. Choose between:
- **On** (default): Subjects see responded feedback providers. In reports, subjects see which feedback providers responded per category, but responses aren't tied to individual names.
- **Off**: Subjects see feedback providers but no information about their response status. In reports, they see only the number of feedback providers who responded.

:::image type="content" source="../../media/glint/setup/360-provider-response-info-2.png" alt-text="Screenshot of the Feedback Provider Response Information window.":::

Select **Save** when you're done configuring the Setup page.

## Introduce your 360 program or cycle 

[Email to introduce 360s to senior leadership and HR leadership](/../../viva/glint/setup/360-email-templates?branch=main#1-introductory-360-email-for-senior-leaders)
[Introductory email to all employees who might be considered as a 360 subject](/../../viva/glint/setup/360-email-templates?branch=main#2--introductory-email-for-all-employees)

## Use these guidance pages to complete 360 cycle setup

There are four more pages to configure:

- [Survey Questions](/../../viva/glint/setup/360-add-edit-cycle-questions)
- [Overview & Feedback provider Selection Content](/../../viva/glint/setup/overview-feedback-provider-selection)
- [Competencies & Reporting](/../../viva/glint/setup/360-competencies)
- [Schedule & Communication](/../../viva/glint/setup/360-schedules-comms)










