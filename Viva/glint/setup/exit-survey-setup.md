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
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/30/2025
---

# Set up a Viva Glint Exit survey

Together, Microsoft Viva Glint refers to Onboarding and Exit surveys as Employee Lifecycle surveys. Viva Glint **Exit surveys** help organizations understand the reasons that employees voluntarily leave. These reasons can range from career advancement opportunities elsewhere to dissatisfaction with their work environment.

## Recommended cadence and tips for Exit surveys

Send Exit surveys for voluntary terminations as soon as possible so that users can access survey invites from their work email address. 

- Exit survey Distribution List date ranges are relative to the termination date that your organization includes in data uploaded to Viva Glint.
- Choose to have Exit Surveys go to a company email or both a company and personal email.
  - If you use **Company Email Address**, set the date range from **14 days before the Termination Date to 1 day after.**
  - If you use **Company email + Personal email**, set the date range from **14 days before termination date to 30 days after.**
 
Learn more about using [date-based Distribution Lists](set-up-distribution-lists.md#use-date-based-lists).

### Survey access methods

If your organization plans to [include inactive users](set-up-distribution-lists.md#use-attribute-rules-to-add-users) in Exit Distribution Lists, use survey access methods that allow inactive users to respond to surveys:

1. [Attribute-based access](attribute-based-survey-access.md)
2. [Personalized link](understand-survey-access-methods.md#personalized-survey-link)

## How to set up an Exit survey

1. From the admin dashboard, select **Configuration**.
2. In the **Surveys** section, select **Survey Programs**.
3. Select **+ New Program**.
4. Choose a survey template or start with a blank template in the **Lifecycle** section.

   :::image type="content" source="../../media/glint/setup/elc-exit-card.png" alt-text="Screenshot of the Exit card for a Lifecycle survey.":::

5. Hover over a template and select **Create Program**.
6. After creating a new survey program from a template, follow the guidance listed for each section of your Exit survey setup.

   |:::image type="icon" source="/office/media/icons/administrator.png" :::  |Setup section |Description|
   |:----------|:-----------|:------------|
   | :::image type="icon" source="/office/media/icons/settings.png" :::  |[Program Setup](program-set-up.md)        |Define basics like languages, optional features, and confidentiality settings.        |
   | :::image type="icon" source="/office/media/icons/users-people.png" :::   |[Distribution](distribution-program-summary.md)        |Select Distribution Lists or User Roles to include in or exclude from the survey invite list.        |
   | :::image type="icon" source="/office/media/icons/help.png" :::  |[Questions](questions-setup.md)       | Add survey introduction text, select questions, and add a survey thank you message.      |
   | :::image type="icon" source="/office/media/icons/usage-report-blue.png" :::  |[Reporting](reporting-setup.md)       |  Define which roles have access to this survey's results and determine key reporting views.      |
   | :::image type="icon" source="/office/media/icons/whats-new-megaphone-blue.png" ::: |[Communications](program-summary-communications.md)       | Customize and set a schedule to send survey communications.     
   | :::image type="icon" source="/office/media/icons/chat-room-conversation-blue.png" ::: |[Coaching](program-summary-coaching.md)       | Confirm or customize content that helps users interpret results on their dashboards.       |

   > [!NOTE]
   > The attribute that your organization includes as a termination date in uploaded data may have a different label, like "Leave Date." Select the date that should trigger Exit surveys in the Distribution section of your survey.

7. [Preview your survey](preview-filter-lifecycle-programs.md#preview-your-survey) after completing each setup section.
   
8. Build excitement and remind your people about the survey.
   - 1-2 days before your survey launch, [customize this email template and send it to your Distribution Lists.]( /../../viva/glint/start/introductory-emails?branch=pr-en-us-9977#email-template-7---announce-survey-launch-to-entire-organization)
   - [Set a calendar alert to send this survey reminder email to your full Distribution List 72 hours before the survey is set to close](/../../viva/glint/start/introductory-emails?branch=pr-en-us-9977#email-template-8-reminder-to-submit-survey).
     
9. [Review survey setup](survey-qa.md) before survey launch.
   
10. [Enable and launch your survey](preview-filter-lifecycle-programs.md#enable-an-employee-lifecycle-program).

11. **Set a calender alert** to customize and send post-survey email communications:
    - **To your entire organization:**
       - 1 day after survey close: [Announce that the survey is closed and explain what's next](/../../viva/glint/communicate/results-rollout-templates?branch=main#email-template-1-survey-close-and-whats-next-for-all-employees)
       - 3-4 days after survey close: [Share survey results and what to expect from feedback](/../../viva/glint/communicate/results-rollout-templates?branch=main#email-template-2---survey-results-and-next-steps-for-all-employees)

    - **To your managers:**
      - 1 day after survey close: [Survey results and confidentiality standard](/../../viva/glint/communicate/results-rollout-templates?branch=main#email-template-5---survey-results-and-confidentiality-standards-for-managers)
      - 5-7 days after survey closes: [How to have effective conversations](/../../viva/glint/communicate/results-rollout-templates?branch=main#email-template-6---how-to-have-effective-conversations-managers-and-hrbps)


