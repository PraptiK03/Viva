---
title: Complete Program Setup for a Viva Glint survey
description: Program Setup page is the first section of a Microsoft Viva Glint survey that lets Viva Glint Administrators define the basic settings for a survey program. Choose items like a survey name and what languages are needed, along with confidentiality directives.
ms.author: JudithWeiner
author: JudyWeiner
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: confidentiality setup, basics setup, survey comment expansion, create Viva Glint survey
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/19/2025
---

# Complete Program Setup for a Viva Glint survey

Program Setup page is the first section of a Microsoft Viva Glint survey that lets Viva Glint Administrators define the basic settings for a survey program. Choose items like a survey name and what languages are needed, along with confidentiality directives. 

## Define the basics for your Viva Glint program

Use the information in the table to guide you through each field in Program Setup.

> [!IMPORTANT]
> Not all fields are available for each survey type. For more information, see the **Survey types** column.

:::image type="content" source="../../media/glint/setup/glint-program-setup.png" alt-text="Screenshot of Viva Glint survey Program Setup, which lists features and settings an admin can set up for a survey.":::

|Field|Description|Examples/Tips|Survey types|
|:-------|:------------|:-----------|:-----------|
|**Program Name**|Used in survey and email communications, reporting, and is visible to survey respondents|Engagement, Manager Effectiveness, 30-day Onboarding| All |
|**Administrators**| This role can set up, manage, edit, and report on all surveys in the entire program|*Manage Programs* must be enabled for the name to appear in the search box.| All | 
|**Default Language**| The default language for survey participants | Dropdown menu selections are based on survey languages set up in General Settings| All |
|**Additional Languages**| Populated with languages set up for your organization in General Settings.| Be sure survey items are available in all languages chosen. To remove languages, select the **X** next to the language name.| All |
| **Admin Notifications to** |These admins are notified of upcoming surveys and are determined in General Settings.|Each survey should have at least one admin in this role who is notified before the survey goes Live. Use the **Search** add names.| Recurring and Ad Hoc |
|**Suggested Action Available** |Enables Users to create goals.|Toggle to enable or disable| All |
|**Response Window** | The number of days a user has to submit a survey once it generates.| Enter a number of days. Viva Glint defaults to 14.| Lifecycle and Always-On |
|**Waiting Period Between Surveys** or **Next Survey Available**| The number of days before a user is eligible to take the survey again.| Enter a number of days. Viva Glint defaults to 365 days for Lifecycle and one day for Always-On.| Lifecycle and Always-On|
|**Eligible for Nudges** |Timely messages designed to help managers take action| Toggle to enable or disable. | Recurring and Ad Hoc  |
|**Allow Survey Resubmission** |Allow survey takers to retake their surveys. All previous responses are deleted|  Toggle to enable or disable.| Recurring, Ad Hoc, and Lifecycle |
|**Enable [Team Conversations](/../../viva/glint/reports/team-conversations-administrator-setup)**|Helps managers and survey takers feel like their feedback is heard and acted upon.|Managers receive a personalized summary presentation of survey results. Helps your managers share results, pick Focus Areas, and identify next steps through a guided interactive conversation.| Recurring |
|**Auto-expand comments input**|With this enabled, a comment box shows after each survey item posed to a survey taker. Disabled, the survey automatically moves to the next item.|Disabled by default. Toggle to enable. This feature prompts more detailed and actionable insights by survey takers, increasing survey engagement.| All |
|**Enable Team Conversations Sharing**|Allows managers to share a read-only version of their feedback summary presentation before or after meetings with their team.| Enabled by default when Team Conversations is enabled. | Recurring |

## Confidentiality in Viva Glint programs

:::image type="content" source="../../media/glint/setup/program-setup-confidentiality-2.png" alt-text="Screenshot that shows the Confidentiality setup within Program Setup.":::

|Field|Description|Examples/Tips|
|-------|------------|-----------|
|**Confidential responses** | Promotes accurate feedback| Enabled to **Custom Confidential** by default|
|**Enable Export of Raw Survey Responses** | Enabling this functionality allows admins to export ungrouped, identifiable survey responses. Disabling this function permanently disallows access to or export of those responses, including the ability to transfer the data to a third party.| [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export)|
|**Company Message to Survey Participants** |Allows organizations to add more details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries  or concerns related to the survey. You can also add guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title "Message from [<Client_Name>]," directly following Glint's confidentiality statement. Use the following format to add a link to information: `[Display text](link)`. For example: `[Contoso handbook](http://www.contoso.com)`.|<li>Translations for the Company Message must be done manually.</li><li>The character limit for the Company Message to Survey Participants is 1,024</li><li>**Survey level custom messaging takes precedence**. Custom messaging set up in General Settings but edited at the survey level, overrides the initial messaging.</li><li>Employee Lifecycle surveys often target only a few individuals. For this reason, reducing your confidentiality threshold helps protect their privacy.</li>|

Select **Save Changes** or the **right-facing arrow symbol** to save and continue.

