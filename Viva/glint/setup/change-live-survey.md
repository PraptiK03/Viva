---
title: Admins editing a live Viva Glint survey
description: Viva Glint suggests changing a live survey only when necessary.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Edit live survey items, edit live survey questions, edit program summary
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 4/21/2025
---

# Admins editing a live Viva Glint survey

Some elements of a Live recurring or Ad Hoc survey can be adjusted, but only make Live edits when necessary.

> [!IMPORTANT]
> The term "item" refers to any question or statement posed in a Viva Glint survey.

Preview your survey before launching. Then follow these practices:

|   Best Practice   |   Considerations   |
| --- | --- | 
|**Don't stop the survey**|Unless you need to completely replace a survey cycle, never *stop* a survey. Some edits can be made while the survey is enabled.|
|**Make email and reminder edits only at the cycle level**| Program level changes don't apply to a Live survey.|
|**Keep the meaning of an item intact**| If you need to fix spelling, grammatical, or translation errors:<ul><li>The adjusted item meaning should remain the same after edits. </li><li> To ensure the integrity of the survey results, don't adjust any rating scale or multiple-choice options.</li></ul>|
|**Make text changes uniformly**| Text changes need to be made across all languages included in the survey.|
|**Always Save and re-approve**| When making Live edits, save changes and **reapprove** the survey before ending your session. [Use this guidance for approving, previewing, enabling, and disabling a survey](/viva/glint/setup/preview-manage-enable-engage-programs).|

**Watch for this alert in Program Summary when editing a Live survey:**

:::image type="content" source="../../media/glint/setup/live-survey-alert.png" alt-text="Screenshot of alert in Program Summary." lightbox="../../media/glint/setup/live-survey-alert.png":::

## Scenarios and considerations for Live survey changes 

Sometimes changing a Live survey may be beneficial. 

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| The text at the beginning (top) and end (bottom) of the survey | The *Intro* or *Thank You* text needs adjustments or corrections. | Newly edited text is featured immediately and *only* if a survey taker hasn't begun the survey. |
| Item text | The phrasing of an item needs to be edited. | Decide whether to change the item while the survey is live or if it can wait until the next cycle. Follow Live survey edits guideline.|
| Adding or removing an item | You want to add a new item or remove an item from a Live survey. | An item *can't* be added or removed from a Live survey except in an Always-On or Employee Lifecycle program. |
| Item order | The survey items need to be reordered. | The newly edited order is featured immediately but *only* on surveys that aren't started. |

## Fields which can be edited 
Only these fields can be edited when a survey is Live.

|Field|Need-to-knows|
|--------|--------------|
|**Question Text** | Wording shows verbatim.<ul><li> The **+ button** allows you to edit the question.  </li><li> Try not to edit our standard survey items. Item edits may impact language translations and the item's intention to accurately tie to its designated benchmark.</li><li>Changes to the item apply to all survey programs and Live survey questionnaires in Recurring and Ad Hoc programs using this item. This change includes the survey where the admin initialized the change.</li><li> Changes can also be made from the Question Library.</li><li> **Be aware if the item is used in multiple programs, emails send for each of those surveys in Recurring Ad Hoc programs..** |
|**Instruction Text** |Use this space to provide survey takers with helpful information about how to answer this item.</li></ul>|
|**Comment Placeholder Text** | **Leave your comments here** appears by default. This text can be customized |
|**Benchmark** | |

> [!IMPORTANT]
> Edits to a question apply only to live and upcoming survey cycles. The edited question is not reflected in past reports.

## Edit a Live survey

The information is broken out across **Program Summary** setup pages.

### Program Setup 

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **Various** | You want to edit the **Program Name**. | Edits are visible only to users with unstarted surveys |
| **Additional languages** | You want to add a new language as a survey option. | If custom translation text isn't provided, Viva Glint's standard text translations are used. |

### Distribution

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **Add users** | Employees not included in your *Employee Attribute File* need to participate in the survey. | From the admin dashboard, select the **People** section and then **Send Survey**. Each new user is sent the email invitation immediately. From then on, new users receive reminders according to the same schedule as all other users. |
| **Edit a Distribution List** | The Distribution List (DL) of employees included or excluded in the survey needs adjustment. | A DL can be adjusted at any time but doesn't automatically send a survey invitation to new users. These invites must be sent manually. |

### Schedule

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **Survey launch date** | You need to postpone the launch date of the survey. | To avoid potential challenges, make this update a minimum of 24 hours before the survey is scheduled to go Live. |
| **Response window** | You want to decrease or increase the number of days for the survey window. | Adjust a minimum of 48 hours before the original survey end date.<br>Be sure your *Communications* email send dates align with the updated survey window.<br><br>**Note** that Live schedule edits apply at the cycle level. |
| **Resend Survey Invites** | You want to resend the survey invite email to users who yet to respond |The email doesn't send to survey takers with completed surveys.  Viva Glint admins can only make this change between the invite send date and the first reminder date.<br><br> This functionality isn't available after the first reminder sends.|
| **Reschedule Survey Invites** | You want to reschedule the survey invite email due to issues with the first invite. | Viva Glint admins can only make this change between the invite send date and the first reminder date.<br><br> This functionality isn't available after the first reminder sends. |

#### Manage the schedule for a live survey

1. Navigate to **Configuration** and choose **Survey Programs** in the **Surveys** section.
2. Select the Live survey to edit from the **Survey Programs** list.
3. In the list of **Upcoming and Live** surveys, go the Live survey and select the ellipses.
4. In the dropdown menu, select **Manage Schedule & Invites** and choose from the **Schedule**, **Resend Survey Invites**, or **Reschedule Survey Invites** options.

   :::image type="content" source="../../media/glint/setup/live-manage-schedule-2.png" alt-text="Screenshot of the Manage Schedule & Invites feature for a live Viva Glint survey.":::

### Items (survey questions or statements)

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **The text at the beginning and end of the survey** | The **Intro** or **Thank You** text needs adjustments or corrections. | Newly edited text is featured immediately on unopened surveys. |
| **Add or remove a survey item** | You want to add a new item or remove an item from a Live survey. | An item *can't* be added or removed from a Live survey except in an Always-On or an Employee Lifecycle program. You can't add, remove, or reorder rating items and multiple-choice questions during a live survey.|
| **Item order** | The items need to be reordered. | Newly edited item order is featured immediately on opened surveys. |
|**Survey sections and survey breaks**| You want to change the formatting of the survey.| Survey section and break additions can't occur during a Live cycle. Section and break changes apply to upcoming cycles only.|
| **Question text** | The phrasing or benchmark status of an item needs to be edited. | <ul><li> Once confirmed and saved, the edited item is pushed to all Live and future surveys that use it.</li><li> All programs with the changed item are automatically set to allow survey resubmission.</li><li> If your organization uses Entra ID or personalized links for survey access, notify participants who started or completed the survey via email. Select the checkbox.</li><li>If your organization uses attribute-based survey access, manual notification of the change is required.</ul> |
|**Question targeting**| You want to target or exclude specific populations for a survey item | Question targeting is not available once a survey is live. 

### Question mapping

Mapping to a Viva Glint standard item needs to be updated.

| Scenario | Considerations |
| -------- | --------| 
|**#1 - You need to change text for an item associated with a benchmark but without a benchmark change**.|Existing external benchmark associations remain the same in the Question Library and in your survey reports. |
|**#2 - You need to change text for an item not associated with a benchmark.** | The considerations stated in **Question text** apply.|
|**#3 - You need to change benchmark mapping but aren't changing item text**.|  <ul><li> External benchmarks are updated in the Question Library.</li><li> No updates are made to survey items, so Live and future surveys aren't impacted.</ul> |
|**#4 - You need to change benchmark mapping and change item text.** | <ul><li>The considerations stated in **Question text** apply.</li><li>Existing external benchmark associations are updated in the Question Library. </li><li> To accurately update reports, re-approve the survey program which includes the changed item.</ul>|

:::image type="content" source="../../media/glint/setup/confirm-before-changing-1.png" alt-text="Screenshot of the Confirm before saving dialog box for item change without benchmark change.":::

:::image type="content" source="../../media/glint/setup/questions-confirm-text-no-association-2.png" alt-text="Screenshot of Confirm before saving dialog box for text edit for item with no associated benchmark.":::

:::image type="content" source="../../media/glint/setup/questions-confirm-benchmark-change.png" alt-text="Screenshot of Confirm before saving dialog box for a benchmark mapping change only.":::

:::image type="content" source="../../media/glint/setup/questions-confirm-text-benchmark-changes-4.png" alt-text="Screenshot of the Confirm before saving dialog box for benchmark and item text changes.":::


#### Admin process for editing an item during a Live survey

There are three entry points for editing an item:
-	From the **Question Library**, on your admin dashboard. This entry point doesn't require survey to go into unapproved state.
-	From the **Survey Programs, Live** section
-	From the **Survey Programs, Upcoming** section

**Allow Survey Resubmission** in the **Program Setup** section of **Program Summary** must be toggled to **Yes.** If not, an alert informs you that the change to **Yes** is made automatically when your edits are saved.

Hover over the **horizontal ellipsis** next to any survey item to select **Edit Question**.

The **Edit Question** slider window includes these setup tabs:
- **Question Configuration**
- **Associated Programs** - The **Before you edit this question** dialog box informs whether this question is currently used in one or more Live survey programs.

#### Associated programs

A list of program names previously used or currently in use that include this survey item are shown. You see an alert cautioning you that this item is being used in one or more Live surveys. 
- If you don't want to make this change, choose **Cancel**.
- You can edit language text, instruction text, and comment placeholder text only. Other fields are disabled and can't be edited until the survey is no longer Live.
- Make your changes and select **Save**.

:::image type="content" source="../../media/glint/setup/change-live-q-tooltips.png" alt-text="Screenshot of warning and tips about editing a question during a live survey." lightbox="../../media/glint/setup/change-live-q-tooltips.png":::

### Reporting

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **All items in the Reporting section** | Any section in the Reporting section needs adjustment. | Save all changes, then return to the **Program Summary** and adjust the Approved toggle to **Yes**. |
|**Reporting label**| You want to change the name of the reporting label to identify a survey item.| Reporting labels can't be updated during live cycles.|
| **Benchmark update** | Your external comparison benchmark was updated. | If changes are made to the benchmark in a Live program, be certain users with Live access are aware so they aren't confused by different results from a past viewing. **Read the section about benchmark status change in the **Items** guidance on this page. |
| **Aggregate Indices** | You need to edit or add an aggregate index. | If changes are made to indices in a Live program, be certain users with live access are aware so they aren't confused by results that are different from their last viewing. |
| **Driver Impact Outcomes** | You need to edit or add Driver Impact outcomes. | If changes are made to Driver Impact outcomes, be certain users with Live access are aware and aren't confused by different outcome options shown in the Driver Impact report. |

### Communications

Live Communications edits only apply when made at the cycle level.

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **Reminders** | You need to add or delete email reminders, or otherwise edit existing text. | Future reminders can be added, edited, or deleted if adjusted at least 24 hours their scheduled send time. Reminders can't be added, edited, or deleted, on the day that they're scheduled to send. |
| **Results Notification** | You want to turn this feature on or off, edit existing text, or adjust the number of days until the message is sent. | To avoid potential challenges, make changes at least 48 hours before the closing of the survey window. |

### Other Live changes 

|   Topic   |   Scenario   |   Considerations   |
| --- | --- | --- |
| **Manager hierarchies** | Your reporting displays incorrect leadership hierarchies due to errors in your Employee Attribute File. | Change only after the close of the survey window. |
| **Add bulk survey participants** | An extra group of employees needs to be added to the platform. | Identify the employees to be added. Then, manually send them the survey invite from within the **People** configuration page. |
| **Add users not in the Distribution List** | Employees outside of the Distribution List need to be included. | From the admin Configuration dashboard, select the **People** feature, then **Employee**, then **Action**, then **Send Survey**. |
| **Email timing** | You want to adjust the time emails are sent. | Adjust timing at the cycle level only and consider the user time zones. |


