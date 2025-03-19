---
title: Review and test Viva Glint surveys before launch
description: To prepare for a smooth launch for your Microsoft Viva Glint survey programs, use the guidance and checklists available here to confirm that all of your platform and survey settings are correct.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: QA, quality assurance, quality check, QC, UAT, user acceptance testing
ms.collection:
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/13/2025
---

# Review and test Viva Glint surveys before launch

To prepare for a smooth launch for your Microsoft Viva Glint survey programs, use the guidance and checklists available here to confirm that all of your platform and survey settings are correct.

## Confirm selections in General Settings

Selections that admins make in [General Settings](manage-general-settings.md) lay the groundwork for users' survey-taking and reporting experiences. Verify that your choices for important fields here appear as expected.

> [!NOTE]
> Not all General Settings fields are included here, but settings that have the biggest impact to survey takers are included.

|Section  |Item  |Confirm that...|
|:----------|:-----------|:------------|
|Company Information     |Client Name       |The organization name is correct; it appears in surveys and email invites and reminders.        |
|      |Client Time Zone       |The correct default time zone that Viva Glint uses to send communications is selected.        |
|      |Company Privacy Policy (optional)        |If configured, the correct link to your company policy is included. [Learn more](add-privacy-policy.md)        |
|      |Company Message to Survey Participants (optional)      |If configured, the message and translations here are accurate. To customize for each survey, add in Program Setup.        |
|Communications     |Send Surveys in Users' Time Zones       |This setting is switched to Yes or No to enable or disable [sending communications in user's time zones](time-zones.md).         |
|Reporting     |Attributes for Alerts       |Attributes are selected to use for populations in the [Alerts Report](/viva/glint/reports/alerts-report-attrition-risk). **When blank, no alerts are generated**.        |
|      |Primary Hierarchy      |The correct primary hierarchy is selected for default reporting views and sections (usually Manager Hierarchy).        |
|      |Secondary Hierarchy       |The correct secondary hierarchy is selected for default reporting views and sections.        |
|Engage Survey Details     |Require Azure AD for links in survey emails       |This setting is switched to:<br><br> Yes to require survey participants to authenticate with Entra ID to access surveys. <br> No to allow survey participants to access surveys with personalized links.<br>[Learn more](understand-survey-access-methods.md).        |
|      |Attribute-based Survey Access       |If needed, attributes are selected for an alternate survey access method for deskless workers. [Learn more](attribute-based-survey-access.md)        |
|Features     |Employee Post-Survey Action Taking       |This setting is set to Yes or No to determine if survey participants see recommended LinkedIn Learning videos on their survey Thank you page. This setting applies to all surveys.        |
|Technical Configuration     |SFTP Setup       |Secure File Transfer Protocol (SFTP) setup is complete if your organization imports employee data with this method. [Learn more](set-up-sftp.md).        |
|Localization     |Comments Analytics Languages       |Languages that should be translated to English for comment analysis are selected. **Languages must be selected before a survey launches to successfully analyze non-English comments.**       |
|      |Default Survey Language       |The correct default language is selected for survey participants.        |
|      |Supported Survey Languages       |Correct languages for survey participants are selected.        |
|      |Default Dashboard Language       |The correct default language is selected for dashboard users.        |
|      |Supported Dashboard Languages       |Correct languages for dashboard users are selected.         |

## Review survey setup

Review each section of your survey program setup before launching a test survey to an internal team. For information on settings that Viva Glint Admins can edit while a survey is live, see: [Make changes to a live Viva Glint survey](change-live-survey.md).

> [!IMPORTANT]
> Not all fields and survey setup sections are available for all survey types. For more information, see the **Survey types** column.

### Program Setup

|Item   | Confirm that...  | Impact| Survey type |
|:----------|:-----------|:------------|:------------|
|Program Name    |The correct value is entered and there are no spelling errors.       |Low        | All |
|Administrators|The correct User Roles are selected as program admins.   |Low| All |
|Default Language|The correct default language is selected.  |Medium| All |
|Additional Languages|Correct survey languages are selected. Languages available are based on Supported Survey Languages selected in General Settings  |Medium| All |
|Admin Notifications To|The correct user is selected for admin notification emails for this program.    |Medium| Recurring and Ad Hoc |
|Suggested Actions Available|This setting is set to Yes or No correctly to allow or disallow users to create Focus Areas based on suggestion action templates.  |High| All |
|Response Window | The number of days the survey is open for responses is correct.  | High  | Lifecycle and Always-On |
|Waiting Period Between Surveys or Next Survey Available | The number of days a survey taker waits to submit a survey again is correct.  | Medium | Lifecycle and Always-On |
|Eligible for Nudges|This setting is set to Yes or No correctly to enable or disable Nudges for managers to act on survey results.   |High| Recurring and Ad Hoc  |
|Allow Survey Resubmission|This setting is set to Yes or No correctly to allow or disallow users to reset their own surveys and resubmit during live surveys.   |High| Recurring, Ad Hoc, and Lifecycle |
|Enable Team Conversations|This setting is set to Yes or No correctly to enable or disable Team Conversations for managers to act on results with a guided, in-platform experience.  |High| Recurring |
|Auto-expand comments input   |This setting is set to Yes to automatically expand comment boxes after a response is entered or No to let users select "+ comment."  |Medium      | All |
|Enable Team Conversations Sharing | This setting is set to Yes or No correctly to enable or disable Team Conversations sharing by managers.  | Medium | Recurring |
|Confidential Responses|This setting is set to Yes or No correctly. This setting can only be switched to No for Employee Lifecycle surveys.  |High| All |
|Enable Export of Raw Survey Responses|This setting is set to Yes or No correctly to allow or disallow the export of raw respondent data for this program.   |High| All |
|Company Message to Survey Participants|Any optional custom messaging to survey participants and accompanying translations are entered correctly.  |High| All |

### Distribution

|Item   |Confirm that...  | Impact| Survey type|
|:----------|:-----------|:------------|:------------|
|Distribution For This Program    |The correct Distribution Lists are selected to include users.       |High        |All      |
|Exclude Groups|The correct Distribution lists are selected to exclude users.   |High|All|

> [!NOTE]
> For Lifecycle surveys, the **Download Recipients** option isn't available. To get a list of recipients for a Lifecycle survey, follow [these steps](/viva/glint/communicate/support-survey-participants#lifecycle-and-always-on-surveys).

### Schedule

|Item   |Confirm that...  | Impact | Survey type|
|:----------|:-----------|:------------|:------------|
|The surveys go out every    |The survey frequency is correct (for example, every three months).       |Low        | Recurring        |
|Send the next survey on|The survey start date is accurate.   | High| Recurring and Ad Hoc|
|Schedule Preview|Upcoming survey dates are accurate based on frequency and survey start date.   |Low| Recurring|
|Response Window|The number of days the survey is open for responses is correct.   |High| Recurring and Ad Hoc|
|Team Conversation Window| The number of days the conversation is open is correct.  |High| Recurring |


### Questions

|Item   |Confirm that...  |Impact| Survey type|
|:----------|:-----------|:------------|:------------|
|Welcome text and translations    |Welcome text and translations are accurate.       |High        |All        |
|Questions|All questions are part of the survey and that the upcoming cycle number is selected for the right questions.   |High|All|
|Questions: Order|Questions are in the correct order.   |High|All|
|Questions: Text and translations|Customized question text and translations are accurate.   |High|All|
|Questions: Targeting|Distribution lists selected to target questions are accurate.   |High|All|
|Questions: Display Logic|Questions that should only appear based on certain responses to other questions are set up correctly.   |High|All|
|Sections and translations|Section break/header text and translations are correct.   |Medium|All|
|Thank you text and translations|Thank you text and translations are accurate.    |High|All|

> [!NOTE]
> - Section break: User scrolls and it disappears as you take the survey. 
> - Survey section: A persistent header with questions tied to it that remains at the top of the screen as the user responds.

### Reporting

|Item   |Confirm that...  |Impact| Survey type|
|:----------|:-----------|:------------|:------------|
|Program Roles    |Roles who should be added to the program are present and that they're granted live or phased access correctly.      |High        |All        |
|Reporting View |Live View or Phased Access is selected appropriately, depending on whether the role should have access to live survey data.   |Medium|Recurring and Ad Hoc|
|Concierge Visibility |This setting is set to On or Off correctly to give managers a concierge experience in dashboards.   |Medium|Recurring and Ad Hoc|
|Broader Team Insights |This setting is set to On or Off to allow direct reports visibility to a summary report of users' scores in this role.   |Medium|Recurring and Ad Hoc|
|Copilot in Viva Glint |This setting is set to On or Off to allow users to access Copilot comment summarization.   |Medium|Recurring and Ad Hoc|
|Team Conversations |This setting is set to On or Off correctly to allow managers to use in-platform Team Conversations.   |Medium|Recurring|
|Dashboard Default |The correct report, typically Team Summary, is selected for the dashboard view.   |Medium|All|
|Report Template Access |Report templates are selected correctly to grant users access to specific reports.  |High|All|
|Question Reporting Access |Users in the role have access to the correct questions.   |Medium|All|
|Aggregate Indices|Question aggregates are set up and labeled correctly.   |Medium|All|
|Key Outcome|The correct item or aggregate is selected.   |Medium|All|
|Driver Impact Outcomes|The correct items or aggregates are selected.  |Medium|All|
|Manager Report Defaults|The correct items are selected to appear on the Manager report.   |Medium|All|
|PowerPoint Export Template|The correct template is selected.   |Low|All|
|Broader Team Insights PowerPoint Export Template|The correct template is selected.   |Low|All|

> [!NOTE]
> - The Team Conversations setting only appears in a Program Role when Team Conversations are enabled in Program Setup.
> - Aggregate Indices can't be deleted after they're set up.

### Communications

|Item   |Confirm that...  |Impact|Survey type|
|:----------|:-----------|:------------|:------------|
|Notification Timing    |The correct timeframe is selected to deliver emails.       |High        |Recurring, Ad Hoc, and Lifecycle        |
|Email Settings*|The correct email types are selected to deliver emails.   |Medium|Recurring, Ad Hoc, and Lifecycle |
|Configure Notifications|Survey start, reminder, and results emails follow the correct schedule.   |High|Recurring, Ad Hoc, and Lifecycle |
|Team Conversations** notification schedule | The conversation start, reminder, and overdue emails follow the correct schedule.  |High|Recurring |
|Translations|Survey, conversation (if enabled), and results emails have accurate translations.   |High|Recurring, Ad Hoc, and Lifecycle |

> [!NOTE]
> - *This setting only appears when your organization has a Personal Email Optional System Attribute set up. Personal emails are recommended for contacting exiting employees.
> - **Team Conversations emails only appear when Team Conversations are enabled in Program Setup.


### Coaching 

|Item   |Confirm that...  |Impact|Survey type|
|:----------|:-----------|:------------|:------------|
|Interpretation    |The correct content is selected for the Interpretation Guide.       |Medium        |All        |
|Top Strengths|The correct content is selected for Top Strengths.    |Medium        |All        |
|Top Opportunities|The correct content is selected for Top Opportunities.   |Medium        |All        |
|Team Conversation Presentation Guidance| The correct content is selected for the conversation presentation. |Medium        |Recurring        |
|Team Conversation Resource Guidance| The correct content is selected for the conversation resources.  |Medium        |Recurring        |

> [!NOTE]
> - Team Conversations items only appear when Team Conversations are enabled in Program Setup.

## Preview data in reporting

After reviewing your survey setup and confirming that employee data is imported to Viva Glint, use the [Generate Report Preview](preview-demo-reporting.md) option to preview how attributes and questions look in reports.

> [!IMPORTANT]
> The Generate Report Preview option is only available for Recurring and Ad Hoc survey types.

## Launch a test survey

To verify that your Viva Glint survey setup, launch a test survey to a group of users, collect feedback, make updates, and delete the test survey after testing is complete. 

### Select a group of survey testers

At least two to three weeks before launching your first Viva Glint survey, conduct testing with a group of users on your project team. Include your Viva Glint core project team and any stakeholders who should provide approval for the survey. For complex setups and surveys with multiple translations, involve testers who can validate all languages selected.

Each test user can review the survey experience with this checklist: [Review a Viva Glint test survey](survey-testing.md).

Provide instructions for users on items that you want them to focus on, including:

- email invite and reminder delivery days and times
- attribute-based access survey link experience (provide link, if applicable)
- languages they should review (if applicable)
- question targeting they should confirm (if applicable)
- question display logic (if applicable)

### Set up a test survey

Launch a test survey to your project team to confirm that emails arrive and the survey-taking experience appears as expected. To set up a test survey:

> [!IMPORTANT]
> To launch a test survey, always create a copy of your survey program. Viva Glint Admins can delete test survey programs, but not test survey cycles in a survey program.

1. From the admin dashboard, select **Configuration** and then choose **Survey Programs**.
1. On the far right of your completed survey program, select the ellipses and choose **Duplicate** from the menu that appears.
1. A new survey program appears titled **"survey name" Copy**.
1. Select the copied survey and go to **Distribution**.
   1. Select a Distribution List that includes test users in the **Distribution For This Program** field.
1. Select **Save & Continue** to go to **Schedule**.
   1. Select a date to launch your test survey in the **Send the next survey on** field.
   1. Select a number of days for the test survey to be open in the **Response Window** field.
1. Go to the **Communications** section to confirm timing and invites/reminders are selected for your test survey's **Response Window**.
1. [Approve and Enable](preview-manage-enable-engage-programs.md) your test survey.
2. Collect feedback from survey testers and update your survey setup based on feedback.

### Capture survey tester feedback

Use this template to create a log to track and resolve survey tester feedback. The first row is populated with an example.

| Issue category |Issue | Description | Tester | Date logged | Status | Resolution |
|:----------|:-----------|:------------|:----------|:-----------|:------------|:------------|
| Email | Email went to junk | Viva Glint survey invite went to Junk folder instead of inbox | Test User | January 13, 2025 | Resolved | Worked with IT to update allowlist |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |

### Delete a test survey

When survey testing is complete, [delete your test survey](delete-survey-data.md) from **Survey Programs**.

## Approve and enable a survey for launch

After all testing and review are complete, [Approve and Enable](preview-manage-enable-engage-programs.md) your survey for launch.
