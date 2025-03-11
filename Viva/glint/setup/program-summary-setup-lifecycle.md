---
title: Set up a Viva Glint Onboarding survey
description: Viva Glint Employee Onboarding surveys measure the employee experience during key moments based on a person's Hire Date.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: onboarding, Hire Date, surveys for Hiring Managers, lifecycle feedback, lifecycle surveys
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 3/11/2025
---

# Set up a Viva Glint Onboarding survey

**Onboarding surveys** are crucial for gauging new hires’ early experiences and ensuring they have the resources and support needed to succeed. They typically occur within the first few weeks of employment and Microsoft Viva Glint suggests they continue at intervals to track the new employee’s integration into your company. These surveys can cover aspects like the effectiveness of your orientation process, clarity of job expectations, and the supportiveness of the environment. Onboarding and Exit feedback is helpful to your organization's Hiring Managers. Together, Viva Glint refers to Onboarding and Exit surveys as Employee Lifecycle surveys.

### Recommended cadence and tips 

The first Onboarding survey for new hires is recommended at 30 days. Consider sending another Onboarding survey at 60 and at 90 days of employment.

**Onboarding tips:**

- Onboarding survey Distribution List date ranges are relative to Hire Date.
- If a person receives the survey 30 days after their Hire Date, set the first value to **after 30 days.** For the end value, provide enough of a window so that if a Hire Date updated late into your Employee Attribute File, they still trigger the survey.
- Don't make the survey taker window too short. Delayed data imports to Viva Glint might cause people to miss an intended Onboarding survey.

## Create an Onboarding Survey

1. From your admin dashboard, select **Survey Programs.**
2. Under **Lifecycle** on the Create a Program page, select the **Onboarding** tile, and then **Create Program.**

   :::image type="content" source="../../media/glint/setup/onboarding-card.png" alt-text="Screenshot of the Onboarding card for a Lifecycle survey.":::

## Name your program

The program title reads **Onboarding**. You can use the **pencil symbol** to give it a different name. For example, you can add the name of your company.

## Program Summary setup 

There are six pages to set up. To set up each page, hover over each row and select it. 

:::image type="content" source="../../media/glint/setup/lifecycle-program-summary.png" alt-text="Screenshot of the Program Summary setup for an Onboarding survey.":::

### Program Setup page

In the first box, define the basics for your program. 

:::image type="content" source="../../media/glint/setup/onboarding-basics.png" alt-text="Screenshot of the Basics setup for an Onboarding survey.":::

|Field|Description|Tip|
|----------|------------|-------|
|**Program Name**|Used in survey and email communications, reporting. The name is visible to survey respondents|30-day Onboarding, 60-day Onboarding|
|**Administrators**|This role can set up, manage, edit, and report on all surveys in the program|*Manage Programs* must be enabled for the name to appear in the search box.|
|**Default Language**|Manage Programs must be enabled for the name to appear in the search box.|
|**Additional Languages**|All languages set up in General Settings display. **X** any language to delete it for this program.|Be sure survey items are available in all languages chosen.|
|**Suggested Actions Available**|Enables Users to create goals.|	Toggle to enable or disable|
|**Response Window**|The number of days the employee has to complete the survey once it's live|Glint suggests 14 days, but you can raise or lower this window.|
|**Waiting Period Between Surveys** |The number of days before an employee is eligible to take the survey again after the previous survey closes.|Our system constantly checks for changes in the trigger date so if a survey is already generated for this timeframe, it doesn't generate a new one. In many Employee Lifecycle programs, Glint recommends 30, 60, 90, or even 365 days (one full year).|
|**Allow Survey Resubmission**|Allow survey takers to retake their surveys. All previous responses are deleted.|Toggle to enable or disable.|
|**Auto-expand comments input** | With this functionality enabled, a comment box shows after each survey item posed to a survey taker. Disabled, the survey automatically moves to the next item.	Disabled by default.| Toggle to enable. This feature prompts more detailed and actionable insights by survey takers, increasing survey engagement.|
|**Enable Viva Pulse Integration**| Enabling this feature sends Glint data for every closed program cycle and future cycles.|	See the Reporting page to specify which roles have access to this integration.|

### Confidentiality section in Program Setup

:::image type="content" source="../../media/glint/setup/program-setup-confidentiality-2.png" alt-text="Screenshot that shows the Confidentiality setup within Program Setup.":::

|Field|Description|Examples/Tips|
|-------|------------|-----------|
|**Confidential responses** | Promotes accurate feedback| Enabled to **Custom Confidential** by default|
|**Enable Export of Raw Survey Responses** | Enabling this functionality allows admins to export ungrouped, identifiable survey responses. Disabling this function permanently disallows access to or export of those responses, including the ability to transfer the data to a third party.| [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export)|
|**Company Message to Survey Participants** |Allows organizations to add more details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries  or concerns related to the survey. You can also add guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title "Message from [<Client_Name>]," directly following Glint's confidentiality statement.|<li>Translations for the Company Message must be done manually.</li><li>The character limit for the Company Message to Survey Participants is 1,024.</li><li>**Survey level custom messaging takes precedence**. Custom messaging is set up in General Settings but edited at the survey level. Custom messaging overrides initial messaging.</li><li>Onboarding surveys often target only a few people. For this reason, a reduction of the confidentiality threshold helps protect privacy.</li>|

Select **Save Changes** when all edits are complete.

### Distribution page

Your Employee Attribute File contains a Hire Date attribute for each employee. This list is used for sending Onboarding surveys. You may not use the same terminology that Viva Glint uses in guidance. In this example, the Employee Attribute File column header is **Start Date**:

:::image type="content" source="../../media/glint/setup/elc-distribution-attribute.png" alt-text="Screenshot of the Employee Attribute dropdown menu in Employee Lifecycle Distribution setup.":::

#### Create an Onboarding Distribution List

Now you need to create a custom Distribution List.

1. Select the **Configuration** symbol on your admin dashboard and then select **Distribution Lists**.
2. Select **+ New Distribution List**.
3. Name your new list by using the **pencil symbol** to delete the *Untitled* content. Let's follow an example that creates a program titled **30-day Onboarding Distribution List**.
4. Select **Add/Edit Employees**.

   :::image type="content" source="../../media/glint/setup/elc-30-day.png" alt-text="Screenshot of creating a 30-day Onboarding Distribution List setup.":::
   
5. From the **Chose a way to add employee** dialog box which opens, select the **Attribute Rules** tile. 

   :::image type="content" source="../../media/glint/setup/elc-attribute-rules.png" alt-text="Screenshot of the Attribute Rules tile in Distribution setup.":::
    
6. The **Add Attribute Rules** slider panel opens. Select **I want to filter all active employees by these populations.**
7. Select **+ New Population** and then **Add Filters.** Find the respective attribute value from your User data, such as "Hire Date" for Onboarding.

   :::image type="content" source="../../media/glint/setup/elc-add-attributes-panel.png" alt-text="Screenshot of the Add Attribute Rules slider panel in Distribution setup.":::
    
8. Select a date and then select **Done.**
9. Select **Save Changes**. Your completed Distribution List for Hire Date looks like this:

   :::image type="content" source="../../media/glint/setup/elc-hire-date-list.png" alt-text="Screenshot of a Hire Date Distribution List created.":::
   
### Questions page

Viva Glint suggests using the 14 core questions populated on the Onboarding template. You can replace them with others suggested by the Microsoft People Science research team. [View the core questions and alternates here](/../../viva/glint/setup/create-onboarding-exit-surveys).

[Learn more about Questions setup and editing in Program Summary](/../../viva/glint/setup/questions-setup)

### Reporting page

[Set up the Report page as described in this guidance](/../../viva/glint/setup/reporting-setup)

The default for interpreting Onboarding reports is a 90-day look-back period. Report recommendations:
- The **Overall Results** report is recommended for viewing Onboarding surveys. Data can be set up and customized to surface useful insights. Filters are dependent on the attributes sent to Viva Glint in your Employee Attribute File and must meet confidentiality requirements.
- Understanding how to interpret [**trending](/../../viva/glint/reports/aggregate-trending) is essential to gaining the best insights from Onboarding feedback.

### Communications page

[Set up the Communications page as described in this guidance](/../../viva/glint/setup/program-summary-communications)

### Coaching page

[Set up the Coaches page as described in this guidance](/../../viva/glint/setup/program-summary-coaching)


## Related resource

[Preview and filter Employee Lifecycle programs](/viva/glint/setup/preview-filter-lifecycle-programs)
