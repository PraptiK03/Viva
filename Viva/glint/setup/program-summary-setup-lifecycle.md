---
title: Set up a Viva Glint Employee Lifecycle program
description: Viva Glint Employee Lifecycle programs measure the employee experience during key moments in the employment journey.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: onboarding, exit surveys
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 2/10/2025
---

# Set up a Viva Glint Employee Lifecycle program

Lifecycle surveys are a comprehensive approach to understanding the employee experience from onboarding to exit. They allow organizations to get a holistic understanding of the employee experience from beginning to end. Employee Lifecycle surveys are considered "trigger events" because they use the hire or termination date to automatically send. The insights from these surveys help organizations address issues that may cause turnover and help improve the overall employee experience. 

**Onboarding surveys** are crucial for gauging new hires’ early experiences and ensuring they have the resources and support needed to succeed. They typically occur within the first few weeks of employment and Glint suggests they continue at intervals to track the new employee’s integration into your company. These surveys can cover aspects like the effectiveness of your orientation process, clarity of job expectations, and the supportiveness of the environment. 

**Exit surveys** help to understand the reason that an employee voluntarily leaves your organization. They uncover the reasons behind their departure, which could range from career advancement opportunities elsewhere to dissatisfaction with the work environment. 



## Recommended cadence and tips for Employee Lifecycle surveys

Glint recommends this cadence:

- **Onboarding surveys for new hires:** within the first week of employment, then again at 30 days *and* at 90 days
- **Exit surveys for voluntary terminations:** as soon as possible

### Onboarding tips

- Onboarding survey Distribution List date ranges are relative to Hire Date.
- If the users should receive the survey 30 days after their hire date, set the first value to **after 30 days.** For the end value, provide enough of a window so that if someone has their hire date updated late in your user data, they still trigger the survey.
- Don't make the survey taker window too short. Delayed data file imports to Glint might cause people to miss being included.

### Exit survey tips

- Exit survey Distribution List date ranges are relative to the Termination Date.
- Choose to have Exit Surveys go to a company email or a personal email or both.
- If you're using **Company Email Address**, we recommend setting the date range from **14 days before the Termination Date to 1 day after.**
- If you're using **Company email + Personal email**, we recommend setting the date range from **14 days before termination date to 30 days after.**

## Program Summary setup for Employee Lifecycle survey templates

Select **My Surveys** on the admin dashboard. Choose an **Onboarding** or **Exit** survey template and then **Program Summary** pages. There are six pages to set up. Begin with **Program Setup**.

### Program Setup page

In the first box, define the basics for your program. 

|Field|Description|Tip|
|----------|------------|-------|
|**Program Name**|Used in survey and email communications, reporting, and is visible to survey respondents|30-day Onboarding, Exit|
|**Administrators**|This role can set up, manage, edit, and report on all surveys in the entire program|*Manage Programs* must be enabled for the name to appear in the search box.|
|**Default Language**|Manage Programs must be enabled for the name to appear in the search box.|
|**Additional Languages**|Manage Programs must be enabled for the name to appear in the search box.|Be sure survey items are available in all languages chosen. To remove languages, select the **X** next to the language name.|
|**Suggested Actions Available**|Enables Users to create goals.|	Toggle to enable or disable|
|**Response Window**|The number of days the employee has to complete the survey once it's Live|Glint suggests 14 days, but you can raise or lower this window.|
|**Waiting Period Between Surveys** |The number of days before an employee is eligible to take the survey again after the previous survey closes.|Our system constantly checks for changes in the trigger date so if a survey is already generated for this timeframe, it doesn't generate a new one. In many Employee Lifecycle programs, Glint recommends 30, 60, 90, or even 365 days (one full year).|
|**Allow Survey Resubmission**|Allow survey takers to retake their surveys. All previous responses are deleted.|Toggle to enable or disable.|
|**Auto-expand comments input** - *Note: this functionality begins on 2/15/2025* | With this functionality enabled, a comment box shows after each survey item posed to a survey taker. Disabled, the survey automatically moves to the next item.	Disabled by default.| Toggle to enable. This feature prompts more detailed and actionable insights by survey takers, increasing survey engagement.|
|**Enable Viva Pulse Integration**| Enabling this feature sends Glint data for every closed program cycle and future cycles.|	See the Reporting page to specify which roles have access to this integration.|

### Distribution List page

Before configuring an Employee Lifecycle program, create employee lists based on hire date for Onboarding surveys and termination date for Exit surveys.

**Process to create an Employee Lifecycle Distribution List:**

1. Select the **Configuration** symbol on the admin dashboard and then select **Distribution Lists**.
2. Select **New Distribution List**.
3. Name your new list.
4. Select **Add/Edit Employees**.
5. Select the **Attribute Rules** tile.
6. Select **I want to filter all active employees by these populations.**
7. Select **+ New Population** and find the respective attribute value from your user data, such as "Hire Date" for Onboarding or "Termination Date" for an Exit survey.
8. Set the date range for your Distribution List window.
9. Add filters if the distribution should only go to a select population.
10. If the survey should include Inactive employees (Exit surveys), be sure the **Include Inactive Employees** box is marked.
11. Select **Save Changes**.

>[!CAUTION]
>You can't use the same number of days for the beginning and end value in the Distribution List. For example: "45 days after to 45 days after" - the query would be unable to find any users.
>
### Finish setting up the Program Summary pages

The other pages required for setup in Program Summary work the same way as for a recurring-type survey program. Follow the guidance on these pages:

|Program Summary page|Tips|
|-------|----------|
| **[Questions](/viva/glint/setup/questions-setup)** ||
|**[Reporting](/viva/glint/setup/reporting-setup)**|<li>The [Overall Results report](/viva/glint/reports/overall-results) is recommended for viewing Employee Lifecycle surveys. Within this report, data can be set up and customized to surface useful insights. Filters are dependent on the attributes sent to Glint in your Employee Attribute File and must meet confidentiality requirements.</li><li>Understanding [how to interpret the trend graph](/viva/glint/reports/trend-graph-lifecycle-survey) is essential to gaining the best insights from Employee Lifecycle data.</li><li>**The default** for Employee Lifecycle reports is a 90-day look-back period.|
|**[Communication](/viva/glint/setup/program-summary-communications)**||
|**[Coaching](/viva/glint/setup/program-summary-coaching)**||






## Related resource

[Preview and filter Employee Lifecycle programs](/viva/glint/setup/preview-filter-lifecycle-programs)
