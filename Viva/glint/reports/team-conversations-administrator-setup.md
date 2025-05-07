---
title: Set up Viva Glint Team Conversations
description: Microsoft Viva Glint Administrators can set up Team Conversations for managers. Team Conversations allow managers to meet with their teams and have meaningful discussions on their team's results and choose Focus Areas.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: set up team conversations, team conversations, conversation sharing, take action
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/18/2025
---

# Set up Viva Glint Team Conversations

Microsoft Viva Glint Administrators can set up Team Conversations for managers. Team Conversations allow [managers to meet with their teams and have meaningful discussions](take-action-team-conversations.md) on their team's results and choose Focus Areas.

> [!NOTE]
> - Team Conversations are only available for Recurring surveys.
> - [Nudges](/viva/glint/communicate/communicate-with-nudges) can coexist with Team Conversations but don't send when the Team Conversations window is open.

## Enable Team Conversations in Program Setup

To enable Team Conversations as a Viva Glint Admin:

1. Select **Configuration** and select **Survey Programs** from the Surveys section.
1. Select a survey program that should have Team Conversations enabled.
2. Enable Team Conversations by switching the toggle to **Yes**.
3. Enable or disable Team Conversations Sharing by toggling to **Yes** or **No**. This setting allows managers to  share their Team Conversations with users in roles that have **View My Surveys** permissions. 

> [!NOTE]
> Team Conversations only generate for managers with survey results that meet confidentiality threshold requirements.

> [!IMPORTANT]
> When a Viva Glint Admin enables Team Conversations for an existing survey, an "Additional configuration needed" message appears in Program Setup. Use the information in this article to set up Schedule, Reporting, and Communications survey sections for Team Conversations.

## Schedule setup

Indicate how many days the Team Conversations Window should remain open. This drives the reminder schedule for Team Conversations. Even after the Team Conversation window closes users can still access their Team Conversations via My Surveys. Once set, conversation start and end dates display after the conversation days setting. 

> [!TIP]
> The default response window is 28 days, but Viva Glint Admins can enter up to 180 days.  

## Reporting setup

There are two items to configure on the Reporting page for each User Role that should have access to Team Conversations. Select the down-facing arrow next to the User Role in the **Program Roles** section and then: 

1. Enable Team Conversations for that role by toggling Team Conversations button to **On**. 
1. Select **Team Summary** as the **Dashboard Default** from the dropdown menu. 

## Communications setup

Team Conversations messages are designed to notify managers when they can begin conversations, remind them of an upcoming conversation due date, and prompt users whose conversations are overdue. Conversation emails begin to send seven* days after survey results are released for roles that have live access. To successfully send messages, ensure that:

- Team Conversations is enabled for a survey and for roles 
- The survey cycle is closed
- User Roles moved to live access at least seven days ago
- The survey close date is within the last 45 days

\* Viva Glint defaults to seven days, but Viva Glint Admins can edit the number of days for conversation start and reminder emails.

When Team Conversations are enabled, these emails appear in the Communications section:

| Email | Default delivery timeframe | Description | 
|:----------|:----------|:----------|
| Conversation Start Notification | Seven days after survey results are released | Notification to managers that results are available to present to their team |
| Reminder 1 | For incomplete conversations, seven days before due date | Reminder to managers to meet with their team to share results and select focus areas |
| Reminder 2 | For incomplete conversations, three days before due date | Reminder to managers to meet with their team to share results and select focus areas |
| Conversation Overdue Reminder 1 | For incomplete conversations, three days after due date | Notification that conversation is overdue |
| Conversation Summary Notification | Manager-driven, unscheduled | When sharing is enabled, a summary email that managers can send before and/or after conversations with their team |

> [!NOTE]
> If you enable Team Conversations for a User Role after the conversation start date, start emails immediately send once Team Conversations is switched to **On**. 

### Edit communications 

Edit and preview by selecting **Edit**. Edits made to notifications are only for the current program. Switching from Edit to **Preview** (and languages) automatically saves changes. 

> [!TIP]
> Plan to make all edits to conversation emails and their send dates before:
> - the first User Role in your organization gets live access
> - the scheduled conversation start date for the first User Role in your organization

For start and reminder emails, Viva Glint Admins can:

- Add or delete an email
- Edit the number of days before or after the conversation due date that the email should send
- Send in any languages enabled for the survey 
- Preview emails in the platform
- Add more reminders by selecting **+ Conversation Reminder**

> [!NOTE]
> Admins can enable or disable (not delete) the Conversation Summary Email, but scheduling the number of days after the conversation due date isn't available. This email is only visible when sharing is enabled in Program Setup and sent by managers to share conversation summaries with their teams. 

### Conversation email scheduling 

Reminders schedule for users in a role when the User Role gets live access to a survey. If admins grant live access to roles at different times, their Team Conversations reminders are on different schedules. The Conversation Start email can be turned on or off until the day it sends but not after the start of the Team Conversations. 

> [!IMPORTANT]
> - Viva Glint Admins can't delete a reminder email after the first user/role scheduled to receive a reminder gets that email.
> - Viva Glint Admins can only edit reminders when there's a role in phased access or the earliest due date for any role is still in the future.

### Customize Team Conversations email content

[Learn more about customizing Team Conversations email content](team-conversations-content-cusomization.md).

## Coaching setup

When Team Conversations are enabled, admins can set up the Team Conversations presentation kit for your manager to share with their teams. See [Coaching Setup for Admins](/viva/glint/setup/program-summary-coaching#manage-team-conversations-content). 

 
