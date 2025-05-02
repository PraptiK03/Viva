---
title: Manage Viva Glint Advanced Configuration settings and tasks
description: Microsoft Viva Glint offers Advanced Configuration options which allow users to view and modify advanced platform settings and perform complex data updates.
ms.author: aweixelman
author: AliciaWeixelman
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Advanced configuration, advanced settings, retroactive user updates, retro updates
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/02/2025
---

# Manage Viva Glint Advanced Configuration settings and tasks

Microsoft Viva Glint offers Advanced Configuration options which allow users to view and modify advanced platform settings and perform complex data updates. Use Advanced Configuration to:

- [Review and edit reporting thresholds](manage-confidentiality-thresholds.md) in the Details or Surveys section.
- Manage advanced survey settings, [like Sensitive Comments](glint-sensitive-comments.md).
- [Import external, historical data](import-historical-response-data.md) from a previous employee survey vendor.
- Export a detailed [snapshot of employee data](glint-data-apps.md) at the time of a past survey launch.
- [Update employee data that is tied to a closed survey](update-glint-reporting-data.md) to correct reporting.
- Perform uploads to [update custom access](advanced-config-uploads.md#perform-a-managers_upload).
- Monitor Advanced Configuration tasks that are still running in the Running Jobs section.

:::image type="content" source="../../media/glint/setup/glint-service-config.png" alt-text="Screenshot that displays the Advanced configuration option icon in Viva Glint tenant.":::

> [!CAUTION]
> Changing certain settings in Advanced Configuration may be irreversible. These options should only be modified by trained Viva Glint users.

## Grant user access to Advanced Configuration

To access, a Viva Glint Admin must enable Advanced Configuration access on an admin user's profile in Viva Glint.

### Grant access to an existing admin user

> [!NOTE]
> Viva Glint Admins can update their own access to Advanced Configuration.

1. Select the **Configuration** symbol, then in **Employees,** choose **People.**
2. In the **Search People** field, enter the user's first and last name or email address.
3. Select the user when they appear as a search result.
4. On the user's detail page, in **Company Admin: Advanced Configuration Access,** select the **pencil symbol** to edit.
5. In the dialog, **turn on Advanced Configuration access** and select **Save**.

After enabling access, when a user selects the **Configuration** symbol, then goes to **Service Configuration**, they see **Advanced Configuration.**

> [!NOTE]
> A user may need to refresh or sign in to Viva Glint again to see Advanced Configuration.

### Grant access to a Support user

To manage Support users' access to Viva Glint and Advanced Configuration, follow the guidance in this article: [Manage Support users in Viva Glint](add-external-user.md).

## Advanced Configuration: Details

View specifics about how information displays in Viva Glint reporting and which features are enabled. For more information on reviewing and editing reporting thresholds in the Details or Surveys section, see [Manage confidentiality thresholds](manage-confidentiality-thresholds.md).

| Setting | Description |
| --- | --- |
| **Auto Action Plans** | Enable autogeneration of action plans for eligible users |
| **Custom Surveys Enabled** | Advanced survey customization, no action required |
| **Rated Confidentiality Threshold** | Scores don't display for fewer responses than this threshold. Viva Glint standard: 5 |
| **Suppression Threshold** | To prevent guessing the scores of respondent groups with insufficient data, the next biggest group is suppressed until the total insufficient + suppressed = or exceeds this number. Viva Glint standard: 2 |
| **Parent Team Suppression Threshold** | Access results for teams that would have been suppressed for parent team respondents greater than or equal to this threshold. Viva Glint standard: 400 |
| **Industry average eSat score** | Industry average for eSat |
| **Industry average response rate** | Industry average for response rate |
| **Response Rate Threshold** | Response rates don't display for groups smaller than this value. Viva Glint standard: 5 |
| **Default Rating Scale** | Number of responses available on rating questions. Viva Glint standard: 5 |
| **Minimum Threshold for Alerts Report** | In the Alerts report, minimum number of respondents for a group to be considered. Viva Glint standard: 20 |
| **Minimum Score Difference for the Alerts Report** | In the Alerts report, minimum difference from benchmark score for a group. Viva Glint standard: 8 |
| **Maximum number of Alerts** | In the Alerts report, the maximum number of alerts to display. Viva Glint standard: 2000 |
| **Maximum number of Alerts for a population** | In the Alerts report, the maximum number of attributes to combine for a group. Viva Glint standard: 2 |
| **Alert and Insight Hierarchy Limitation** | In the Alerts report, when hierarchies are selected, the maximum number of levels considered. Viva Glint standard: 3 |
| **Attribute Cardinality Management** | In the Alerts report, when values for an attribute exceed this number, the attribute isn't included in the report. Viva Glint standard: 100 |
| **Insight Probability Threshold** | In the Alerts report, the statistical likelihood that results aren't by chance and are significant. Viva Glint standard: 0.05 |
| **Comments Search Threshold** | Comments don't display for fewer question responses than this threshold. Viva Glint standard: 10 |
| **Comments Confidentiality Threshold** | Comments don't display by topics for fewer responses than this threshold. Viva Glint standard: 10 |
| **Minimum Difference for Driver Impact Report** | In the Driver Impact report, the minimum difference from the item score for the entire company. Viva Glint standard: 5 |
| **Driver Impact Report Threshold** | In the Driver Impact report, the minimum number of respondents to display results. Viva Glint standard: 20 |
| **Exclude negative strengths and positive weaknesses** | Exclude negative strengths and positive weaknesses for Driver Impact calculation. |
| **Enable Kiosk Page** | Allow users to [access attribute-based surveys](attribute-based-survey-access.md) without a registered kiosk. |
| **Self-Serve Mode** | EDIT_AND_CREATE allows admins to edit and create survey programs |
| **Support Users for Survey Notifications** | No action needed, leave blank. Admins can add users in the Support role to surveys in the Distribution section.  |
| **Action Plans to Goals enabled?** | No action needed, leave as true |
| **Enable Cross Program Filtering** | Filter results across multiple surveys programs. Viva Glint standard: true |
| **Percentage Probability of following up on marked question** | To encourage open-ended comments, percentage of users that are prompted with follow-up questions in surveys. Viva Glint standard: 15 |
| **Frequency of in-product feedback shown MLE Dashboard** | Percentage of users that see in-product feedback questions in their Team Summary dashboard. Viva Glint standard: 100 |
| **Frequency of in-product feedback shown on non-MLE Dashboard** | Percentage of users that see in-product feedback questions in their non-Team Summary dashboard. Viva Glint standard: 10 |
| **Enable Filter Suppression on Scores** | Disable users' ability to filter to teams whose scores are suppressed |

## Advanced Configuration: Surveys

For a simpler view of existing survey programs, go to **Configuration** symbol and select **Survey Programs**. Use the **Advanced Configuration Surveys** option to view advanced technical details related to your survey programs. The main page for Surveys includes:

- Name
- Type
- State
- Program
- Start Date
- Frequency
- Recurrence Rule
- Show Last Modified (when enabled)

Select a survey program to view more details and options. For more information on reviewing and editing reporting thresholds in the Details or Surveys section, see [Manage confidentiality thresholds](manage-confidentiality-thresholds.md).

| Survey setting | Description |
| --- | --- |
| **State** | ACTIVE (ready to be enabled) or DRAFT (edit mode) |
| **Domain** | No action needed, leave blank |
| **Survey Trigger Type** | How surveys generate: Schedule, Event (example: Hire Date), User Initiated |
| **Event Trigger Survey Questionnaire Shelf Life** | Days to complete survey |
| **Generate DISABLED survey cycle in Self Serve** | True. Recurring/upcoming surveys don't enable until an admin enables them |
| **Resubmit Submit Enabled** | Allow users to resubmit their own surveys |
| **Survey Type** | Recurring, On demand, Employee Lifecycle (ELC), or Always-On |
| **Event Trigger Survey Minimum Pulsing Interval (Days)** | Minimum days before a user can be surveyed again |
| **Icon Name (css class)** | No action needed, leave blank |
| **Contact Method** | Company Email or Company and Personal Email |
| **Minimum Sample Size** | Blank. Refer to platform-level settings in Details |
| **Minimum Group Size** | Blank. Refer to platform-level settings in Details |
| **No Suppression Parent Team Size** | Blank. Refer to platform-level settings in Details |
| **Minimum sample Size Survey Stats** | Blank. Refer to platform-level settings in Details |
| **Minimum Respondent size for Driver Impact Report** | Blank. Refer to platform-level settings in Details |
| **Minimum Respondent Size for Comments** | Blank. Refer to platform-level settings in Details |
| **Minimum Group Size for Comments** | Blank. Refer to platform-level settings in Details |
| **Run action plans** | True. Generate action plans for eligible users |
| **Default survey locale** | Displays selection from Survey Programs: Survey: Program Setup |
| **Additional Survey Locales** | Displays selection from Survey Programs: Survey: Program Setup |
| **Enable Follow Up** | Enable follow up questions that encourage more open-ended comments in surveys |
| **Sensitive Comments** | [Enable sensitive comment flagging](glint-sensitive-comments.md) in the admin view of the Comments report for personally identifiable information (PII), sensitive topics, and profanity. |

## Advanced Configuration: Users

To export Viva Glint users select the **Configuration** symbol, choose **People,** and then **Export**.

## Advanced Configuration: External Import

[Import external survey results](import-historical-response-data.md) to see trend for past items that continue to be asked in Viva Glint survey programs.

## Advanced Configuration: Data Apps

Use [Viva Glint Data Apps](glint-data-apps.md) to export recipients or update attribute values for users in closed surveys.

| App UUID | Description |
| --- | --- |
| **EXPORT_USERS_FROM_SURVEY_CYCLE** | Export survey recipients, attributes, and hierarchies as they existed when a survey launched |
| **RETROACTIVE_PULSE_UPDATE** | Update employee attributes associated with a closed survey cycle |

## Advanced Configuration: Uploads

Use the Uploads option to:

- View file upload details.
- Update users' custom data access in bulk.
- Perform retroactive data updates to correct employee attributes in reporting.

### Upload types:

- **MANAGERS_UPLOAD:** [Upload custom results data access](advanced-config-uploads.md#perform-a-managers_upload) for dashboard users in bulk.
- **Retroactive User Updates:** [Update user data in closed surveys](advanced-config-uploads.md#perform-retroactive-user-updates) to correct reporting.
- **ROLE_UPLOAD:** To upload users to a Viva Glint User Role, follow the guidance in this article: [Import and export Viva Glint User Roles](export-user-roles.md).

## Advanced Configuration: Running Jobs

Review details, statuses, and start times for Advanced Configuration tasks performed within the last 15 minutes to 48 hours, depending on the selected timeframe.
