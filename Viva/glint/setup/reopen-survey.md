---
title: Reopen or extend a Viva Glint survey cycle
description: To increase participation rates, a recently closed survey cycle can be reopened or a survey close date can be extended.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: extend survey window, reopen closed window
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/23/2025
---

# Reopen or extend a Viva Glint survey cycle

Sometimes survey takers need extra time to complete a survey or your response rate may not be as high as you hoped. Admins can reopen a survey cycle as long as a new cycle isn't started. The survey cycle can also be extended. 

>[!TIP]
>For best results, reopen a recently closed survey within a day or two of the survey cycle ending.

## Reopen a closed survey 

> [!IMPORTANT]
> Survey close notifications aren't automatically regenerated once the original closing notification is sent. 

When a survey cycle is closed **and** the survey end notification email is sent, no further survey end notification email is sent.

Also consider:

- The Team Conversations for this survey is deleted and regenerated after the survey closes on the new date. Team Conversations isn't available while the survey is reopened.
- The **Phased Access** user role can't access the results of this survey until the role is regranted access. 
- Review and reschedule any Nudges already set. They also aren't rescheduled automatically. 

## Reopening a survey 

1. Select the **Configuration** symbol on your admin dashboard (landing page).
2. Select **Survey Programs**.
3. In the **Survey Cycles** section, select the **Completed** tab and select the cycle to reopen or extend.
4. From the **Actions dropdown** menu, select **Reopen Survey**.
5. A **Reopen Survey Cycle** window opens.

   :::image type="content" source="../../media/glint/setup/reopen-survey-cycle.png" alt-text="Screenshot of the Reopen survey cycle window.":::
   
To reopen this survey cycle, select a new close date. To avoid duplicating work for managers, reopen the cycle within one day of the previous cycle end date. Consider this guidance, then review and adjust as needed:

- **Team Conversations:** The Team Conversations for this survey are deleted and regenerated after the survey closes on the new end date. Any actions previously taken with this Team Conversations are lost and need to be restarted.
- **Nudges:** The Nudges schedule doesn't automatically update.
- **Reporting level access:** User Roles with Phased access - who were granted Live access before the survey cycle was reopened - automatically return to Phased access.
- **Alerts report:** Existing alerts are removed and regenerated after the new survey close date. No action required.
- **Survey emails:** Upcoming communications are automatically rescheduled based on the survey close date.
  
6. Select a new **Close date** for your survey.

> [!NOTE]
> A survey extension can't close *past the start date of the next scheduled survey.* If you choose an invalid date, you see a message directing you to choose a different date.

7. Select **Save.** The survey is immediately reopened and closes at midnight (11:59 PM) on the selected date in the client's time zone. The survey status is now **Live**.

## Extend a live survey cycle window

When a survey cycle is extended *before* its original close date, notification generation automatically updates to reflect the new close date. The default for the survey end notification email is always three days post survey cycle close.

Admins can extend a survey under these conditions:
- The survey is live
- It isn't the last day of the survey. In this case, let the survey close and then follow the process to extend a live survey cycle window.

>Example:
> - The survey end date is March 10. The Survey End notification email is set to send on March 13.
> - On March 8, you decide to extend the Close Date to March 15. The survey close notification automatically moves to March 18.

## Process to extend a live survey cycle window

1. From your admin dashboard, select **Configuration** and then **Survey programs**.
2. From the **Upcoming and Live** tab, select the **Live survey cycle** and then select the **horizontal ellipses** that display.
   
   :::image type="content" source="../../media/glint/setup/extend-live-survey.png" alt-text="Screenshot of starting point to extend a live survey.":::
   
1. Select **Manage Schedule & Invites** from the dropdown menu. The **Manage Schedule** panel opens.
1. Use the up arrow in the **Response window** field to add days onto the survey. In this example, the survey date has been extended to 18 days, from the original 14 days.
1. Select **Save Changes**.

   :::image type="content" source="../../media/glint/setup/extend-manage-schedule.png" alt-text="Screenshot of Manage Schedule panel to extend a live survey.":::

1. Confirm that the new **End date** of your survey is correct. 

  :::image type="content" source="../../media/glint/setup/extend-confirm.png" alt-text="Screenshot of confirmation of survey extension.":::

Now, choose whether to resend your survey invites.

### Resend survey invites 

Select **Resend Invites Now.**

### Reschedule survey invites

You can reschedule all invites to be resent at a new date and time. This time must be after the Survey Start date and before the first Reminder date.

:::image type="content" source="../../media/glint/setup/extend-resend.png" alt-text="Screenshot of resending and rescheduling survey invites.":::









   



   
