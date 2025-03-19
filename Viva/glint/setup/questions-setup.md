---
title: Questions setup in Program Summary of Viva Glint
description: On the Questions page admins add or modify items for Viva Glint surveys.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: edit questions, survey items, question targeting, item targeting, add logo
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/14/2025
---

# Questions set up in Program Summary

> [!IMPORTANT]
> The term **item** refers to any *question or statement* posed to a survey taker.

Admins can add, modify, or delete template items on the Questions page. Standard templates provide prepopulated survey items, along with customizable introductory and concluding text. The Viva People Science Team researches and substantiates prepopulated survey items.

:::image type="content" source="../../media/glint/setup/program-summary-questions.png" alt-text="Screenshot of where to access Questions setup from Program Summary." lightbox="../../media/glint/setup/program-summary-questions.png":::

 Refer to the [Learn about Viva Glint program design](/training/modules/viva-glint-learn-about-viva-glint-program-design) module to learn how to implement your organization's listening strategy in your survey program question setup.

## Use Viva Glint's survey templates

Standard templates provide prepopulated survey items, along with customizable introductory and concluding text. The Viva Glint People Science Team researches and substantiates prepopulated survey items.

## Edit the survey introduction message

Customize the introduction message for the survey by hovering over and selecting the box with the **Hello** message. In the **Edit Survey Intro** slider panel:

1. If multiple languages were set up in General Settings for this program, the option to select languages shows. Choose an alternate language from the **Language** dropdown menu. 
2. Edit **Greeting** - "Hello" is prepopulated but can be customized.
3. Edit **Text** - Default text shows in the **Text** box. All default text can be edited. Delete macros or add macros by selecting the **+ symbol**.
4. Select **Save Changes**.

   :::image type="content" source="../../media/glint/setup/questions-hello-text.png" alt-text="Screenshot of where to customize introductory text." lightbox="../../media/glint/setup/questions-hello-text.png":::

### Add a hyperlink to the survey introduction

To add a link to an employee resource or other information in your survey introduction:

1. Select the **Questions** section of your survey program and select the survey introduction section.
2. In the **Text** field, add `[Display text](link)`, replacing "Display text" with the text that should become a link. Replace "link" with the URL.
   1. Example: `[Contoso handbook](http://www.contoso.com)`
3. If your survey has multiple languages, select each language from the **Language** dropdown menu to add the hyperlink to the **Text** field in all languages.
4. Select **Save Changes**.
5. [Preview your survey](/viva/glint/setup/preview-manage-enable-engage-programs) to confirm that the hyperlink works as expected.

### Add a logo to the survey introduction

> [!TIP]
> Ensure that logos are horizontally oriented, have a transparent background, and 16 MB or smaller in file size.

1. From the admin dashboard, select **Configuration**. In the **Action Taking** section, select **Content Resources**.
1. Select **+ New** to add a new resource and **OK** in the languages message that appears.

1. Add a title in the **Untitled Resource** and **Title** fields. Survey intro logos can be unique to each survey program. Include the survey name in the title if desired.
1. In **Type**, select **Image**.
1. Optionally, add a **Description**.
1. In **File**, select **Choose File**. Choose the image file from your device. If the image is as you'd like, select **Save**.
1. Select **Publish** and then select **Publish** again in the **Publish Resource** dialog box.
1. On the **Resources** page, filter to **Image** and copy the text of the recently added image from the **Name** column.
1. Replace "logo-name" in this text with the name of your uploaded logo: `![logo-name](logo-name "logo-name")`
1. Copy the `![logo-name](logo-name "logo-name")` text (with your logo name added) and paste it into the end of the Text field.
1. Select **Save Changes**.
1. [Preview your survey](/viva/glint/setup/preview-manage-enable-engage-programs) to confirm that the logo appears as expected.

## Edit survey items

Survey items can be edited during the initial survey configuration *and* sometimes during a live survey. [Read about editing live survey items](/viva/glint/setup/question-edit).

There are three entry points where survey items can be edited:
-	In the **Question Library** in Admin Configuration. This entry point doesn't require that the survey is changed to an unapproved state.
-	In **Survey Programs, Live** 
-	In **Upcoming Surveys**

> [!IMPORTANT]
> **Allow Survey Resubmission** in the **Program Setup** must be toggled to **Yes.** If not, an alert informs you that the change to **Yes** happens automatically when edits are saved. To continue, select **Edit**.

### Edit a survey item from the Questions page in Program Summary

Hover over the item to display the horizontal ellipses. Select **Edit Question** from the dropdown menu.
   
:::image type="content" source="../../media/glint/setup/questions-dropdown.png" alt-text="Screenshot of the dropdown menu next to survey items." lightbox="../../media/glint/setup/questions-dropdown.png":::

In the **Edit Question** panel, there are two tabs to consider:
   - Question configuration
   - Associated Programs

#### Question Configuration tab 

:::image type="content" source="../../media/glint/setup/question-panel.png" alt-text="Screenshot of the Edit Question panel." lightbox="../../media/glint/setup/question-panel.png":::

Follow the in-platform guidance for edits to your chosen item. Select **Save Changes** when you're finished.

> [!IMPORTANT]
> For comment setup, consider whether [**Auto-expand comments input**](/../../viva/glint/setup/program-summary-overview) is enabled in **Program Setup**.

#### Associated Programs tab 

A list of each program your edited survey item appears in displays. The example image shows a portion of the list of 161 associated programs for the chosen item. Be sure the change works for each associated program!

:::image type="content" source="../../media/glint/setup/questions-associated-programs.png" alt-text="Screenshot of the Associated Programs tab." 

:::image type="content" source="../../media/glint/setup/questions-program-list.png" alt-text="Screenshot of a portion of an Associated Program list." 

## Survey item targeting

Add a target to a specific item to ensure that only the population selected sees it in the survey. 
Using the search box, select one or more **User Roles** to include or exclude. 
Select **Save Changes**.

## Delete survey items

Remove an item from the program by selecting **Yes, delete it** in the box that displays. If you don't want to delete, select **No, I changed my mind.**

## Edit the "Thank You!" message 

Customize the **Thank You** concluding survey message by hovering over the box and selecting it. In the window that opens:

1. Select languages from the **Language** dropdown menu. Languages permissioned for your organization in General Settings are available. If only English is available, this field won't show.
1. Edit **Greeting** - "Thank you!" is prepopulated but customize the greeting in a way that's comfortable for you. 
1. Edit **Text** - You see dummy text in the **Text** box.
   - All dummy text can be edited.
   - The Text field also includes placeholders, called macros, that pull in values based on your employee data or Glint-generated items. Delete macros or add new macros by selecting the **+ symbol** in the Text box.
1. Select **Save Changes**.

> [!NOTE]
> To add a hyperlink to the survey Thank You message, follow [these steps](#add-a-hyperlink-to-the-survey-introduction).

## Edit Question cycles

You don't have to use all of the items selected for a survey in each cycle. Choose survey items per cycle by selecting the corresponding cycle number next to the item. For example, if you only want a certain item asked on the first survey, deselect all numbers except for the number 1.

## Add new items and section breaks

To add rating questions, multiple choice questions, open-ended questions, or section breaks (to give your people time to take a natural pause), follow this guidance: [Adding items to a prepopulated survey](/../../viva/glint/setup/add-new-questions).

## Edit Display Logic

>[!TIP]
> Wait to add display logic until after your sections and items are in the order you want.

1. In the Display Logic window, set the **Overall logic for conditions** and **Conditions** or **Subconditions**. 
1. Select **+ Add new condition** to add more.

**[Use this guidance to manage display logic](/../../viva/glint/setup/viva-glint-display-logic)**

## Next Step
> [!div class="nextstepaction"]
> [Reporting setup in Program Summary](/../../viva/glint/setup/reporting-setup).



