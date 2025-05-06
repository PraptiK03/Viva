---
title: Support participants during a live Microsoft Viva Glint survey
description: During a live Viva Glint survey, participants can use online support content to answer many of their questions. Take other steps listed here to set up users for success to submit their valuable feedback.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: survey taker, survey participant, live survey, support, resend survey, survey eligibility
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/06/2025
---

# Support survey participants during a live Microsoft Viva Glint survey

Introduce Microsoft Viva Glint surveys and [communicate proactively](/../../viva/glint/communicate/prelaunch-live-email-templates) with your organization about upcoming surveys. During a live Viva Glint survey, participants can use [online support content](https://support.microsoft.com/en-us/topic/viva-glint-overview-87374186-feec-4256-962a-563f99992f08) to answer many of their questions. Take other steps listed here to set up users for success to submit their valuable feedback.

## Create an FAQ document

Use the [Viva Glint FAQ template](survey-taker-faq.md) to create your own internal document to address commonly asked questions in your organization. Include: 

- How users are eligible to participate
- What to do if users run into login issues
- The survey start and end dates
- The sending email address for survey emails
- The [resend survey link](#use-the-viva-glint-survey-invite-link), filled in with your company ID.

## Allow survey resubmission

Use the "Allow Survey Resubmission" feature during survey [program setup](/../../viva/glint/setup/program-set-up) so that participants can resubmit their responses by selecting a link on the survey Thank You page.

:::image type="content" source="../../media/glint/setup/vg-survey-resubmit.png" alt-text="Screenshot of the Thank You page with survey resubmission enabled.":::

## Manage authentication issues

Your organization may require that you authenticate with Microsoft Entra to access surveys in Viva Glint. If users encounter any issues when logging in, the following articles help with common troubleshooting topics related to multifactor authentication. Route Microsoft Entra login issues to your IT help desk.

- [Common problems with two-step verification for a work or school account](https://support.microsoft.com/account-billing/common-problems-with-two-step-verification-for-a-work-or-school-account-63acbb9b-16a1-47b9-8619-6a865e8071a5)
- [Troubleshoot problems using Microsoft Authenticator](https://support.microsoft.com/account-billing/troubleshoot-problems-with-microsoft-authenticator-a3a74493-566b-4c2e-b949-a2789bac0fd3)

## Confirm eligibility

If a user reaches out because they weren't included in a survey, use Viva Glint to confirm whether they're eligible.

### Recurring and Ad Hoc surveys

1. From the admin dashboard, select **Configuration**. In the **Survey Programs** section, select **Surveys**.
2. Select the live survey.
3. In the list of **Upcoming and Live** surveys, hover over the right side of the live survey and select the ellipsis.
4. In the dropdown menu, select **Export Recipients** and enable the **Include all use attributes?** setting to see the user's attribute values as they were when the survey launched.
5. Search for the user in the exported recipient file to confirm if they were included in the survey.

### Lifecycle and Always-On surveys

> [!NOTE]
> Viva Glint Admins need [access to Advanced Configuration](/viva/glint/setup/understand-advanced-configuration#grant-user-access-to-advanced-configuration) to export recipients for Lifecycle and Always-On surveys.

1. Go to **Configuration** and in **Service Configuration**, select **Advanced Configuration**.
2. In the **Advanced Configuration** menu, select **Data Apps** and choose **Export Users from Survey Cycle**.
1. To export recipients, select the parameters:
   1. **surveyName:** Select **Load Values** and choose a survey from the dropdown list.
   1. **cycleName:** Select **Load Values** and choose a cycle from the dropdown list.
   1. **includeAttributes:** Select **yes** to include all attributes. Select **no** to include required attributes only.
   1. **includeAllCycles:** Select **yes** to include all cycles (this option is recommended for Lifecycle and Always-On survey eligibility troubleshooting). Select **no** to include the selected cycle only.
   1. **includePersonalEmail:** Select **yes** to include the personal email attribute (if applicable). Select **no** to exclude. 
1. Select **Save as ZIP** to download a compressed file of recipients.
1. Search for the user in the exported recipient file to confirm if they were included in the survey.

## Validate credentials for attribute-based survey access

Your organization may use [attribute-based access](/../../viva/glint/setup/attribute-based-survey-access), which is often set up for access with a QR code or shortened link. If a user sees a **could not validate credentials** message, they reach out to confirm their details. To confirm a user’s credentials, go to Viva Glint Advanced Configuration. Export their information as it was when the survey launched with the [Export Users from a Survey Cycle Data App](/../../viva/glint/setup/glint-data-apps).

## Resend survey invites

### Use the "Resend Survey" option to send invites to individual employees

If a user is eligible for a survey but wasn’t included at the time of launch, use the Viva Glint [Send Survey](/../../viva/glint/setup/people-page) option to send an invite during a live survey. In the configuration section, select **People** and search for a user. After selecting their profile, select **Actions** and choose **Send Survey**, which sends in invite email.

### Resend all invites in bulk

To reschedule all invites to be resent - in bulk - use the **Resend Survey Invites** option. The date and time must be after the Survey Start date and before the first Reminder date.

:::image type="content" source="../../media/glint/setup/extend-resend.png" alt-text="Screenshot of resending and rescheduling survey invites.":::

### Use the Viva Glint survey invite link

Any user in your organization can use these links to resend invites for all of a user’s active surveys. Replace the **‘companyID’ with your own in the URL** (as an admin, go to General Settings and confirm the Client UUID value as your company ID). Enter a user’s email address and select **Email Survey Invite** to resend emails. The **Provide Feedback** button in the new emails uses the same [access method](/viva/glint/setup/understand-survey-access-methods) as the original invites (authentication with Microsoft Entra ID or a personalized link).

- US server: https://app.us1.glint.cloud.microsoft/companyID/q2/resend-pulse
- EU server: https://app.eu1.glint.cloud.microsoft/companyID/q2/resend-pulse

For example, if Contoso (whose tenant is US-based) wants to update the link for their organization, it looks like this:

> [https://app.us1.glint.cloud.microsoft/**contoso**/q2/resend-pulse](https://app.us1.glint.cloud.microsoft/contoso/q2/resend-pulse)

:::image type="content" source="../../media/glint/setup/vg-resend-url-page.png" alt-text="Screenshot of the Viva Glint resend survey landing page.":::

Users receive a notification email after using the link if they have no active surveys.

:::image type="content" source="../../media/glint/setup/email-no-active-surveys.png" alt-text="Screenshot of the email a user receives when they use the link to resend survey invites but have no active surveys.":::



