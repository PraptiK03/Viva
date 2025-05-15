---
title: Set up a Microsoft Viva Glint Always-On survey
description: Microsoft Viva Glint Always-On Feedback surveys provide insight on any topic, at any time, from any group of people in your organization.
ms.author: JudithWeiner
author: JudyWeiner
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/07/2025
---

# Set up a Microsoft Viva Glint Always-On survey

Microsoft Viva Glint Always-On feedback surveys provide insight on any topic, at any time, from any group of people in your organization. Different than scheduled or recurring programs, Always-On surveys are always open and ready for users to provide insights in real time. Ideally, Always-On surveys are quick and easy to complete in a few minutes. [Learn about survey types](/viva/glint/start/program-types-templates#types-of-surveys).

## Potential use cases

Always-On surveys should pair with the timing of an event, initiative, or situation that your organization wants continuous feedback on:

- Determine engagement confidence levels before and after a major event.
- Get suggestions for improving policies and procedures.
- Ask people during a tough time, "What can leaders do to support you right now?" 
- Determine whether recent expats feel supported in their new countries.
- Ask how confident employees are in a new product strategy.

> [!NOTE]
> Always-On surveys don't include a Communications section or send any notifications to users. Viva Glint admins need to handle Always-On survey notifications outside of the platform.

## Survey access methods

Always-On surveys don't include a Communications section or any notifications from the platform. Personalized survey links can only be delivered in Viva Glint emails, but Viva Glint admins can choose from two other access methods for Always-On surveys:

1. [Attribute-based access](attribute-based-survey-access.md)
2. [Authentication with Microsoft Entra ID](understand-survey-access-methods.md#authentication-with-microsoft-entra-id)
   
## How to set up an Always-On survey

To create a new Always-On survey:

1. From the admin dashboard, select **Configuration.**
2. In the **Surveys** section, select **Survey Programs.**
3. Select **+ New Program.**
4. Choose from the **Distress Survey Always-On template** or the **Blank Always-On template** in the **Always-On Feedback** section.

   :::image type="content" source="../../media/glint/setup/always-on-survey-templates.png" alt-text="Screenshot of Viva Glint Always-On survey templates which can be preloaded with questions or blank.":::
   
5. Hover over a template and select **Create Program.**
6. After creating a new program from a template, follow the guidance listed for each section of your Always-On survey setup.

   |:::image type="icon" source="/office/media/icons/administrator.png" :::  |Setup section |Description|
   |:----------|:-----------|:------------|
   | :::image type="icon" source="/office/media/icons/settings.png" :::  |[Program Setup](program-set-up.md)        |Define basics like languages, optional features, and confidentiality settings.  <br> ***See Important callout.**      |
   | :::image type="icon" source="/office/media/icons/users-people.png" :::   |[Distribution](distribution-program-summary.md)        |Select Distribution Lists or User Roles to include in or exclude from the survey invite list.        |
   | :::image type="icon" source="/office/media/icons/help.png" :::  |[Questions](questions-setup.md)       | Add survey introduction text, select questions, and add a survey thank you message.      |
   | :::image type="icon" source="/office/media/icons/usage-report-blue.png" :::  |[Reporting](reporting-setup.md)       |  Define which roles have access to this survey's results and determine key reporting views.      |
   | :::image type="icon" source="/office/media/icons/chat-room-conversation-blue.png" ::: |[Coaching](program-summary-coaching.md)       | Confirm or customize content that helps users interpret results on their dashboards.    |

> [!IMPORTANT]
> **For Always-On surveys**, if the **Waiting period between surveys** field is edited after a survey generates for an employee, the change only impacts new surveys generated for that employee. The original waiting period is enforced for surveys scheduled and generated.


7. [Preview your survey](preview-filter-lifecycle-programs.md#preview-your-survey) after completing each setup section.
   
8. [Review survey setup](survey-qa.md) before enabling for your organization.

9. [Customize this email template to introduce your organization to Viva Glint programs and this Always-On survey](/viva/glint/start/introductory-emails?branch=pr-en-us-10011#email-template-7---announce-survey-launch-to-entire-organization).
    
10. Enable your Always-On survey when you're ready to make it available to your organization.
   1. Use the toggle at the top of the page to switch the survey to **Approved**.
   2. Hover over the survey card on the left and select **Enable Survey**.
   3. Select **Yes, enable the survey** in the **Enable Survey** dialog. The survey tile changes from gray to blue and displays response rate as users submit surveys.
  


> [!IMPORTANT]
> After an Always-On survey is enabled for the first time, Viva Glint admins can make edits by switching the Approved toggle to **Off**. When an admin reapproves the survey in the future, the survey **auto-enables**.

## Understand how response numbers show in Always-On reporting

The default report timing for Always-On surveys is 90 days. Sometimes people in your organization may take the survey frequently - the waiting period is less than 90 days. How is this data counted?
 - The responses number shows for unique users only. Repeat survey takers count only once.
 - Multiple responses submitted by a single user are counted in the aggregate and the multiple choice report.

> **Example**
> Your organization has a survey with waiting period of one (1) day and the survey includes multiple-choice questions where only one option can be selected. The 90-day default report shows the number of unique user responses, but the multiple choice for a demographic, hierarchy, or a team adds up to more than 100%. 
