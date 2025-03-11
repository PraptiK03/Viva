---
title: Set up a Viva Glint Exit survey
description: Viva Glint Exit surveys help to understand why a person voluntarily left your organization.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: onboarding, exit surveys, employee lifecycle surveys, hiring manager surveys
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/11/2025
---

# Set up a Viva Glint Exit survey

**Exit surveys** help to understand the reason that an employee voluntarily leaves your organization. They uncover the reasons behind their departure, which could range from career advancement opportunities elsewhere to dissatisfaction with the work environment. Onboarding and Exit feedback is helpful to your organization's Hiring Managers. Together, Viva Glint refers to Onboarding and Exit surveys as Employee Lifecycle surveys.

### Recommended cadence and tips for Exit surveys

Send Exit surveys for voluntary terminations as soon as possible.

**Exit survey tips**

- Exit survey Distribution List date ranges are relative to the Termination Date.
- Choose to have Exit Surveys go to a company email or a personal email or both.
  - If you're using **Company Email Address**, set the date range from **14 days before the Termination Date to 1 day after.**
  - If you're using **Company email + Personal email**, set the date range from **14 days before termination date to 30 days after.**

## Create an Exit survey

1. From your admin dashboard, select **Survey Programs.**
2. Under **Lifecycle** on the Create a Program page, select the **Exit** tile, and then **Create Program.**

   :::image type="content" source="../../media/glint/setup/elc-exit-card.png" alt-text="Screenshot of the Exit card for a Lifecycle survey.":::

## Name your program

The program title reads **Exit**. You can use the **pencil symbol** to give it a different name. For example, you can add the name of your company.


## Program Summary setup

There are six pages to set up. To set up each page, hover over each row and select it. 

:::image type="content" source="../../media/glint/setup/elc-exit-program-setup.png" alt-text="Screenshot of Program Summary for an Exit Lifecycle survey.":::

### Program Setup page

In the first box, define the basics for your program. 

|Field|Description|Tip|
|----------|------------|-------|
|**Program Name**|Used in survey and email communications, reporting, and is visible to survey respondents|Exit, [Company Name] Exit Survey|
|**Administrators**|This role can set up, manage, edit, and report on all surveys in the entire program|*Manage Programs* must be enabled for the name to appear in the search box.|
|**Default Language**|Manage Programs must be enabled for the name to appear in the search box.|
|**Additional Languages**|Manage Programs must be enabled for the name to appear in the search box.|Be sure survey items are available in all languages chosen. To remove languages, select the **X** next to the language name.|
|**Suggested Actions Available**|Enables Users to create goals.|	Toggle to enable or disable|
|**Response Window**|The number of days the employee has to complete the survey once it's live|Viva Glint suggests 14 days, but you can raise or lower this window.|
|**Waiting Period Between Surveys** |For an Exit survey, the default is set at 365 days.|If someone returns to your organization and leaves again, they can take the survey at the time of their exit.|
|**Allow Survey Resubmission**|Allow survey takers to retake their surveys. All previous responses are deleted.|Toggle to enable or disable.|
|**Auto-expand comments input** | With this functionality enabled, a comment box shows after each survey item posed to a survey taker. Disabled, the survey automatically moves to the next item.	Disabled by default.| Toggle to enable. This feature prompts more detailed and actionable insights by survey takers, increasing survey engagement.|
|**Enable Viva Pulse Integration**| Enabling this feature sends Viva Glint data for every closed program cycle and future cycles.|	See the Reporting page to specify which roles have access to this integration.|

### Confidentiality section in Program Setup

:::image type="content" source="../../media/glint/setup/program-setup-confidentiality-2.png" alt-text="Screenshot that shows the Confidentiality setup within Program Setup.":::

|Field|Description|Examples/Tips|
|-------|------------|-----------|
|**Confidential responses** | Promotes accurate feedback| Enabled to **Custom Confidential** by default|
|**Enable Export of Raw Survey Responses** | Enabling this functionality allows admins to export ungrouped, identifiable survey responses. Disabling this function permanently disallows access to or export of those responses, including the ability to transfer the data to a third party.| [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export)|
|**Company Message to Survey Participants** |Allows organizations to add more details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries  or concerns related to the survey. You can also add guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title "Message from [<Client_Name>]," directly following Viva Glint's confidentiality statement.|<li>Translations for the Company Message must be done manually.</li><li>The character limit for the Company Message to Survey Participants is 1,024.</li><li>**Survey level custom messaging takes precedence**. Custom messaging is set up in General Settings but edited at the survey level. Custom messaging overrides initial messaging.</li><li>Exit surveys often target only a few people. For this reason, a reduction of the confidentiality threshold helps protect privacy.</li>|

Select **Save Changes** when all edits are complete.

### Distribution page

Your Employee Attribute File contains a Termination Date attribute for each employee. This date is used for sending Exit surveys. You may not use the same terminology that Viva Glint uses in guidance. In this example, your Employee Attribute File column header might read **End Date**. Find the *Termination Date* in the Employee Attribute dropdown menu and select it. 

:::image type="content" source="../../media/glint/setup/elc-attribute.png" alt-text="Screenshot of the Employee Attribute dropdown menu in Employee Lifecycle Distribution setup.":::

### Create an Exit Distribution List:**

Now you need to create a custom Distribution List.

1. Select the **Configuration** symbol on your admin dashboard and then select **Distribution Lists**.
2. Select **+ New Distribution List**.
3. Name your new list by using the **pencil symbol** to delete the *Untitled* content. Let's follow an example that creates an Exit survey named **Why I Left.** 
4. Select **Add/Edit Employees**.

   :::image type="content" source="../../media/glint/setup/elc-why-left.png" alt-text="Screenshot of creating an Exit survey Distribution List setup.":::
   
5. From the **Chose a way to add employee** dialog box which opens, select the **Attribute Rules** tile. 

   :::image type="content" source="../../media/glint/setup/elc-attribute-rules.png" alt-text="Screenshot of the Attribute Rules tile in Distribution setup.":::
    
6. The **Add Attribute Rules** slider panel opens. Select **I want to include all active employees by these populations** and **Include Inactive Employees.** Use the Search bar to manually find the employee names who left your employ and should receive the Exit survey.
7. Select **Save Changes.**

   :::image type="content" source="../../media/glint/setup/elc-attribute-rules-exit.png" alt-text="Screenshot of the Attribute Rules slider panel in Distribution setup.":::

### Questions page

Viva Glint suggests using the six core questions populated on the Exit template. [View the core questions here](/../../viva/glint/setup/exit.survey).

[Learn more about Questions setup and editing in Program Summary](/../../viva/glint/setup/questions-setup?branch=pr-9461)

### Reporting page

[Set up the Report page as described in this guidance](/../../viva/glint/setup/reporting-setup)

Report recommendations:
- The **Overall Results** report is recommended for viewing Exit surveys. Data can be set up and customized to surface useful insights. Filters are dependent on the attributes sent to Viva Glint in your Employee Attribute File and must meet confidentiality requirements.
- Understanding how to interpret [trending](/viva/glint/reports/trend-graph-lifecycle-survey) is essential to gaining the best insights from Exit feedback.

### Communications page

[Set up the Communications page as described in this guidance](/../../viva/glint/setup/program-summary-communications)

### Coaching page

[Set up the Coaches page as described in this guidance](/../../viva/glint/setup/program-summary-coaching)

## Related resource

[Preview and filter Employee Lifecycle programs](/viva/glint/setup/preview-filter-lifecycle-programs)


