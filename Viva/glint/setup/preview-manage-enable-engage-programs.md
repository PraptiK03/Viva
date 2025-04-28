---
title: Preview, enable, and prepare to launch Viva Glint surveys
description: After all the sections in Program Summary are set up, use the following guidance to approve, preview, edit, and launch your Microsoft Viva Glint program.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: preview survey, approve survey, enable survey, monitor survey emails, launch
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/28/2025
---

# Preview, enable, and prepare to launch Viva Glint surveys

After all the sections in Program Summary are set up, use the following guidance to approve, preview, edit, and launch your Microsoft Viva Glint program. 

## Approve a program 

When each section of a survey is set up successfully, a blue checkmark displays to the right of the section name on the Program Summary page. These checkmarks indicate that the survey can be approved and enabled. Approving the program takes it out of draft state and displays scheduled survey cycles on the Upcoming and Live section of the page. 

After a Viva Glint Administrator approves a program, all programs except for Employee Lifecycle and Always-On surveys must also be enabled to go Live on the scheduled date. Surveys go into Live status at midnight on the day they're scheduled to go out, in your default time zone. 

   > [!NOTE]
   > When Employee Lifecycle and Always-On surveys are updated, admins are prompted to reapprove them. Reapproval automatically re-enables the cycle. This feature helps admins ensure live surveys are always active.

### Procedure 

To approve a program, change Approved to **Yes**. 

   > [!NOTE]
   > After Viva Glint Admins approve a survey, they also need to enable a survey to make it live.

## Preview the survey

When your survey is approved, you can preview how survey invites and reminder emails appear to end users. 

### Procedure

1. [Send preview emails](email-content-customization.md#preview-emails).
6. Review the email content and then select **Provide Feedback**.  

   > [!TIP]
   > Share the preview questionnaire with your team for approval.

7. The introductory page of the program opens in a new tab, in the default language of the user you preview. 

   When reviewing the introduction and summary for each item, ensure that: 

   - Rating scale is as expected 
   - Rating scale labels are written as expected (Strongly Disagree - Strongly Agree) 
   - Comments are available 
   - Items aren't skippable unless intended
   - Macros appear as values 
   - More language options are available as expected

## Edit a cycle schedule 

To make edits to a survey after seeing a preview:

1. Select the **ellipsis** next to the cycle to be previewed.  
2. Select **Edit**. Once a survey is live, the edit option isn't available. 
3. Make the necessary changes. 

## Manage a cycle schedule 

To reschedule the survey: 

1. Select the **ellipsis** next to the cycle you want to edit.  
2. Select **Manage Schedule**. 
3. In the **Reschedule Survey** dialog box, make the necessary changes. If the survey is Live, the **Schedule** section is disabled.  
4. Select **Save Changes**. 

## Announce the upcoming survey

Now it's time to let survey takers know that the survey is just days away. Customize our email templates and share them with the people on your survey Distribution Lists. Use the tips for customizing templates found on the page with the template.

### Send this email 1-2 days before your survey launches

[Announce survey launch to entire organization](/../../viva/glint/start/introductory-emails?branch=pr-en-us-9977#email-template-7---announce-survey-launch-to-entire-organization): Announce the imminent survey release and build excitement!

### Send this email when the survey is live

Set a calendar alert to send this email (customized) to your full distribution list 72 hours before the survey is set to close.

[Reminder to submit survey](/../../viva/glint/start/introductory-emails?branch=pr-en-us-9977#email-template-8-reminder-to-submit-survey)

## Enable a program 

Once enabled, surveys go live at midnight on the day they're scheduled to go out, in your company’s default time zone. Survey invitations are sent according to your delivery window set up on the Communications page.  

1. Select the **ellipsis** next to the cycle to be enabled.  
2. Select **Enable Survey**.  
3. The **Status indicator** changes to blue. If the survey is Live, the Status indicator shows green. 

Once the program is enabled and live, the following changes can't be made: 

- Survey name can't be changed 
- Removing or adding items on a live survey 
- Adding or editing distribution lists on a live survey  
- Removing items from the dashboard 
- Removing comments 
- Reopening a closed survey 

## Verify a launch 

Check your email and the email of at least one other survey recipient when your program is scheduled to be live. If your survey is missing, check to confirm that the dates are correct and that the survey was enabled.

## Monitor email activity

Microsoft 365 Global Administrators and Exchange Administrators can use email activity reports to monitor  activity and address delivery issues after a Viva Glint survey launches. For more information, see:

- [Microsoft 365 admin center](/microsoft-365/admin/activity-reports/email-activity-ww)
- [Exchange admin center](/exchange/exchange-admin-center)
