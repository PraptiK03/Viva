---
title: Viva Glint Questions setup
description: As a Microsoft Viva Glint Administrator, use the Questions section to manage survey items, modify introduction and thank you messages, and add optional features like targeting, display logic, and sections.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: edit questions, survey items, question targeting, item targeting, add logo, survey instructions, survey thank you message, add sections, custom question
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/06/2025
---

# Viva Glint Questions setup

As a Microsoft Viva Glint Administrator, use the Questions section to manage survey items, modify introduction and thank you messages, and add optional features like targeting, display logic, and sections. To set up survey items, use information from your [Holistic Vision and Strategy Discovery Workbook](customize-program.md#use-the-holistic-listening-vision-and-strategy-discovery-workbook) and your [Deployment guide survey tab](/viva/glint/introduction-viva-glint#deploy-viva-glint-and-launch-a-survey) as a guide.

> [!NOTE]
> Not all items in the Viva Glint Question Library are posed in question format. Library items also include statements to rate on a given scale. For this reason, the term "item" on the Viva Glint platform and in Learn and training guidance refers to any content in the Question Library. The term "item" includes questions and statements.

## Edit the survey introduction message

Customize the introduction message for the survey by hovering over and selecting the **Hello** message. In the **Edit Survey Intro** pane:

1. Edit **Greeting**: "Hello" is prepopulated but can be customized.
1. Edit **Text**: Default text shows in the **Text** box. All default text can be edited. Delete macros or add macros by selecting the **+ symbol**.
1. If the survey uses multiple languages, choose each language from the **Language** dropdown menu to edit translations. Changes autosave when a new language is selected from the dropdown menu.
1. Select **Save Changes** when all edits are complete.

   :::image type="content" source="../../media/glint/setup/questions-hello-text.png" alt-text="Screenshot of where to customize introductory text." lightbox="../../media/glint/setup/questions-hello-text.png":::

### Add a hyperlink to the survey introduction

To add a link to an employee resource or other information in your survey introduction:

1. Select the **Questions** section of your survey program and select the survey introduction section.
2. In the **Text** field, add `[Display text](link)`, replacing "Display text" with the text that should become a link. Replace "link" with a link to the employee resource.
   1. Example: `[Contoso handbook](http://www.contoso.com)`
3. If your survey uses multiple languages, select each language from the **Language** dropdown menu to add the hyperlink to the **Text** field in all languages. Changes autosave when a new language is selected from the dropdown menu.
4. Select **Save Changes**.
5. Preview your survey to confirm that the hyperlink works as expected.
   1. [Recurring or Ad Hoc survey preview process](preview-manage-enable-engage-programs.md)
   1. [Lifecycle and Always-On survey preview process](preview-filter-lifecycle-programs.md#preview-the-survey)

### Add a logo to the survey introduction

> [!TIP]
> Ensure that logos are horizontally oriented, have a transparent background, and 16 MB or smaller in file size.

1. From the admin dashboard, select **Configuration**. In the **Action Taking** section, select **Content Resources**.
1. Select **+ New** to add a new resource and **OK** in the languages message that appears.
1. Add a title in the **Untitled Resource** and **Title** fields. Survey intro logos can be unique to each survey program. Include the survey name in the title if desired.
1. In **Type**, select **Image**.
1. Optionally, add a **Description**.
1. In **File**, select **Choose File**. Choose the image file from your device. If the image is as you'd like, select **Save**.
   
   :::image type="content" source="../../media/glint/setup/logo-content-resource.png" alt-text="Screenshot of fields completed to add a logo as a Viva Glint Content Resource.":::
   
1. Select **Publish** and then select **Publish** again in the **Publish Resource** dialog box.
1. On the **Resources** page, filter to **Image** and copy the text of the recently added image from the **Name** column.
1. Replace "logo-name" in this text with the name of your uploaded logo: `![logo-name](logo-name "logo-name")`
1. Go to **Configuration,** choose **Survey Programs,** and select a survey whose introduction should have a logo.
2. Go to the **Questions** section, select the introduction, and copy the `![logo-name](logo-name "logo-name")` text (with your logo name added) and paste it into the end of the Text field.

   :::image type="content" source="../../media/glint/setup/logo-text-intro.png" alt-text="Screenshot of logo text copied into a Viva Glint survey introduction text field.":::
   
1. If your survey uses multiple languages, select each language from the **Language** dropdown menu to add the logo to the **Text** field in all languages. Changes autosave when a new language is selected from the dropdown menu.
1. Select **Save Changes**.
1. Preview your survey to confirm that the logo appears as expected.
   1. [Recurring or Ad Hoc survey preview process](preview-manage-enable-engage-programs.md)
   1. [Lifecycle and Always-On survey preview process](preview-filter-lifecycle-programs.md#preview-the-survey)

## Add survey questions

In programs that use survey templates, like Quarterly Engagement, the Questions section is prepopulated with survey items. There are two ways to access the Question library pane to add questions to a survey:

1. Select the **+** symbol that appears above the Thank you message after the last survey question, or
2. Select the **+** symbol next to the Thank you message and select the **Browse Questions** menu option.
   1. To prefilter questions based on type, choose Add Rating Question, Add Multiple Choice Question, or Add Open-Ended Question from the menu.
3. Use the **Search for a question** field to enter keywords to search for an item in the Question library edit pane.
4. Use the Sources, Type, Benchmark, and the More Filters options to filter to items based on your survey needs.
5. To add an item to the survey, hover over it and select the **+** symbol.

> [!TIP]
> For open-ended questions, consider whether [**Auto-expand comments input**](/../../viva/glint/setup/program-summary-overview) is enabled in **Program Setup**.

> [!NOTE]
> For Recurring surveys: 
> - Choose survey items for each cycle by selecting the cycle number next to the item. Cycle one (1) is the upcoming survey that launches on the date selected in the **Send the next survey on** field in the survey **Schedule**.
> - To be able to save the Questions section, every cycle needs to have at least one question selected.

## Create a custom question

When creating **new custom questions**, keep in mind that:

- There are no preloaded translations.
- There are no external benchmarks. [Learn more about mapping custom questions to benchmarks](custom-question-benchmark.md).
- Custom questions aren't included in the [Attrition Risk Index](/viva/glint/reports/alerts-report-attrition-risk#attrition-risk-index).
- Custom questions aren't mapped to standard [Action Plan Templates](/viva/glint/setup/customize-action-plans#understand-terminology-associated-with-content-resources-and-action-plans) or recommended [Focus Areas](/viva/glint/people-science/people-science-explains-focus-areas).
   
> [!CAUTION]
> Your organization may have policies governing appropriate survey items for employees. Ensure you consult any such policies before proceeding. Rather than create a new item, search the Question Library for existing questions that could be reused or repurposed. Viva Glint standard questions are validated and typically come with benchmarks and action plans. 

1. Select the **+** symbol at before the Thank you message to open the **Question library** edit pane.
2. Select the **+ Create** button. A **Create Question** window opens.
   1. You can also select an existing question to access the **Edit Question** pane and choose **Duplicate question** create a custom copy of a Viva Glint item.
1. For your new item, enter information in [editable fields](#editable-question-fields).              
1. If your survey uses multiple languages, select each language from the **Language** dropdown menu to update translations. Changes autosave when a new language is selected from the dropdown menu.
1. Select **Save and Add**.

## Edit survey questions

Before **editing** an item:

- Select the item and check whether it exists in other surveys in the Associated Programs tab.
- [Review the impact of editing Viva Glint standard items](question-library.md#the-implication-of-customizing-editing-question-library-items).

To edit a survey item in the Questions section:

1. Hover over the item to display the horizontal ellipsis.

   :::image type="content" source="../../media/glint/setup/questions-dropdown.png" alt-text="Screenshot of the dropdown menu next to survey items.":::

1. Select **Edit Question** from the ellipsis dropdown menu.
1. In the **Edit Question** pane, change information in [editable fields](#editable-question-fields).               
1. If your survey uses multiple languages, select each language from the **Language** dropdown menu to update translations. Changes autosave when a new language is selected from the dropdown menu.
1. Select **Save changes**.

> [!IMPORTANT]
> - Open-Ended questions are always optional and don't include an "Optional question" setting.
> - To add a new response option to Multiple Choice/Multi-Select questions, always use the "+ Add new choice" feature. Switch the "Show" toggle to "Hide" to retire an option. Overwriting an existing option with a different/new label causes trend issues in reports and confusion in raw data exports.

## Editable question fields

Viva Glint survey questions have some fields that are view only and fields can vary by question type. For more information, see the following table.

| Field  | Description and use | Question type | Editable or view only |
|:----------|:-----------|:------------|:------------|
| Question ID               | Unique question ID.     | All             | View only   |
| Language                  | Dropdown field that lists all translations for the question. This field also appears for English-only surveys. select languages from the dropdown menu to update translations.       | All        | Editable    |
| Question Type             | The question type: Rating, Open-Ended, or Multiple Choice/Multi-Select      | All             | View only   |
| Reporting label           | The shortened label for a question that appears in reports.       | All             | Editable    |
| Question text             | The full question text that survey takers see. This text also appears in some report areas.       | All             | Editable    |
| Benchmark                 | The Viva Glint [standard question that this item is linked to for benchmarking](custom-question-benchmark.md).    | Rating          | Editable    |
| Instruction text          | Help text for survey takers to answer the question.       | All             | Editable    |
| Comment placeholder text  | Help text for survey takers to provide comments.       | All             | Editable    |
| Rating scale              | The number of responses for rated questions.        | Rating          | View only   |
| Label for all options     | Enable this toggle to display a label for all responses instead of only high and low values.      | Rating          | Editable    |
| Low value                 | The label for the lowest response for rated questions ("Strongly Disagree").       | Rating          | Editable    |
| High value                | The label for the highest response for rated questions ("Strongly Agree").        | Rating          | Editable    |
| Option description        | Enable this toggle to show descriptions for each multiple choice response option.       | Multiple Choice | Editable    | 
| Option fields             | Labels for each multiple choice response option.       | Multiple Choice | Editable    | 
| Select as least           | The minimum number of responses a user needs to select for a multi-select question.       | Multiple Choice | Editable    |
| Select at most            | The maximum number of responses a user can select for a multi-select question.        | Multiple Choice | Editable    |
| Allows comments           | Enable or disable to allow or disallow comments that supplement responses.       | Rating and Multiple Choice  | Editable   |
| Optional question         | Enable or disable to allow or disallow users to skip the question.      | Rating and Multiple Choice  | Editable   |
| Suggested action template | Confirm the default or select a different template from the dropdown menu for managers to have suggested action items when choosing this item as a Focus Area.        | Rating                      | Editable   |

## Add a Section Break or Survey Section 

To alert survey takers to a change in topic or keep in mind certain information as they answer part of a survey, Viva Glint Admins can add Section Breaks or Survey Sections.

- **Section Break**: A message that appears once for a survey taker and disappears as they scroll through a survey. 
- **Survey Section**: A header with questions tied to it that remains at the top of the screen as the user responds.

### Add a Section Break 

1. Select the circular **+** button on the Questions page.
2. Select **Add Section Break** to reveal an edit pane.
3. Add text to the **Title** and **Text** fields.
4. Use the **+** symbol to add macros, if needed.
5. If your survey uses multiple languages, select each language from the **Language** dropdown menu to update translations. Changes autosave when a new language is selected from the dropdown menu.
6. Select **Save Changes.** Now the Section Break title appears as a row after survey questions, with a quotation mark.

   :::image type="content" source="../../media/glint/setup/add-section-break.png" alt-text="Screenshot of a Section Break row.":::

7. Move the Section Break by dragging it into place where you want to alert survey takers of a new section.

   :::image type="content" source="../../media/glint/setup/section-break-moved.png" alt-text="Screenshot of a Section Break row moved between chosen survey item sections.":::

8. To edit or delete the Section Break, use the ellipsis on the Section Break to select **Edit Section** or **Delete** from the dropdown menu.

### Add a Survey Section

1. Select the **+** button on the Questions page.
2. Select **Add Section Section** to reveal an edit pane.
3. Add text to the **Title** and **Text** fields.
4. If your survey uses multiple languages, select each language from the **Language** dropdown menu to update translations. Changes autosave when a new language is selected from the dropdown menu.
5. Select **Save Changes.** Now the Survey Section appears as a row beneath your survey items, with brackets calling it out.

   :::image type="content" source="../../media/glint/setup/add-survey-section.png" alt-text="Screenshot of a Survey Section row.":::

6. Move the Survey Section by dragging it into place where you want to alert survey takers of a new section.

   :::image type="content" source="../../media/glint/setup/section-break-moved-2.png" alt-text="Screenshot of a Survey Section row moved before chosen survey item sections.":::

7. To add questions to the Survey Section, use the ellipsis on the Survey Section to select **+ Add Question** from the dropdown menu.
  
   :::image type="content" source="../../media/glint/setup/section-add-question.png" alt-text="Screenshot of the ellipsis dropdown menu next to Survey Section.":::

8. Choose questions in the **Question Library** edit panel opens. Hover over a question and select the **+** symbol to add to the Survey Section.

    > [!NOTE]
   > If questions already exist in the survey, delete them and readd to the Survey Section.

   :::image type="content" source="../../media/glint/setup/section-question-added.png" alt-text="Screenshot which shows a new item added under a Survey Section.":::

3. The new survey item shows under the Survey Section.

## Add question targeting

Microsoft Viva Glint Administrators can use Distribution Lists or User Roles to target survey items or exclude items for specific groups of users. [Learn how to target items to certain users](targeted-survey-items.md).

## Add Display Logic

Display logic rules allow Viva Glint Admins to show or hide survey items depending on the survey taker’s responses to previous questions in a survey. [Learn more about tailoring survey experiences with Viva Glint Display Logic](viva-glint-display-logic.md).

## Delete survey questions

To delete an item from a survey program:

1. Hover over a question and select the ellipsis that appears.
1. In the dropdown menu, select **Delete**.
1. Select **Yes, delete it** in the dialog that appears.

> [!NOTE]
> This action only removes the item from the survey program. The item still exists in the Question Library and Viva Glint Admins can add it to other surveys.

## Edit the "Thank You!" message 

Customize the **Thank You** message by hovering over and selecting the message at the bottom of the Questions section. In the edit pane that opens:

1. Edit **Greeting**: Customize the default "Thank you!" text or leave as is.
1. Edit **Text**: 
   1. Customize the default message or leave as is.
   1. Delete macros or add macros by selecting the **+ symbol** in the **Text** box. 
   1. Macros pull in values from Viva Glint (like survey frequency) or from your employee data (like Department). 
1. If your survey uses multiple languages, select each language from the **Language** dropdown menu to edit translations. Changes autosave when a new language is selected from the dropdown menu.
1. Select **Save Changes**.

> [!NOTE]
> To add a hyperlink to the survey Thank You message, follow [these steps](#add-a-hyperlink-to-the-survey-introduction).


## Next Step
> [!div class="nextstepaction"]
> [Reporting setup in Program Summary](/../../viva/glint/setup/reporting-setup).

## More resources

Many items are prohibited from being edited once a survey is live. [Read what items can't be edited during a live survey](/viva/glint/setup/change-live-survey)
