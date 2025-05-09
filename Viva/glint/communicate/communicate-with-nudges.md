---
title: Communicate with Viva Glint Nudges
description: Nudges are personalized email notifications designed to meet managers where they are in their flow of work. Nudges encourage managers to take simple steps to drive their team’s engagement and performance.
ms.author: Judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: managers using nudges, Nudge triggers, manager action, nudges
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/24/2025
---

# Communicate with Viva Glint Nudges

Microsoft Viva Glint Nudges are personalized notifications designed to meet managers where they are in their flow of work. Nudges encourage managers to take simple steps to drive their team’s engagement and performance. 

**Nudges are sent on a set schedule.** Managers receive unique messages with each Nudge to keep the experience fresh, focused, and relevant as it unfolds. Nudges simplify key behaviors into small steps and make action taking collaborative. Nudges aren't sent to managers who didn’t receive enough feedback to meet confidentiality thresholds. 

> [!NOTE]
> Nudge communications might not send exactly between the two hour window specified during platform configuration. The send time is dependent upon the number of communications being sent.

## Understand Nudge terminology

| Term | Definition | 
|---|---|
| **Recipient group** | Defines who receives Nudges and at what frequency |
| **Teammates** | This term has a different meaning dependent upon the employee role: <br><br> <ul><li> Individual contributors: Managers + peers </li><li> Frontline manager: Manager + directs </li><li> Manager of Managers: Manager + direct </li></ul>|

## How managers benefit from Nudges

Nudges differ from other Viva Glint notifications. Nudges are sent only for high priority messages, such as:

- Concierge-like Nudges to interpret and share results and commit to a Focus Area.
- Reminders and suggestions for taking action on Focus Areas.

This table shows the conditions, messages, and actions for Nudge notifications:

| Condition | Message | Action |
|--------|--------|---------|
|When a survey is Live| [Survey Name] is live! Invite your teammates to respond! <br> *If a manager has multiple live surveys running, a consolidated message is sent, listing each survey*.|No action required|
|Manager hasn't viewed survey results|**Heading** - Your survey results are ready.<br>**Body** - Review your [Survey Name] results and prepare to share with your team.|Interpret results from the manager dashboard.|
|Manager viewed results but hasn't decided on a Focus Area|**Heading** - It’s time to check in with your team. <br>**Body** - Talk with your team about results, celebrate wins, and collaborate on what next steps to take to build trust, transparency, and shared ownership of action. | [Use the Team Conversations Presentation Kit](/../../viva/glint/reports/managers-sharing-team-conversations)|
|Manager received the previous Nudge but hasn't created a Focus Area.|**Heading** - Take one small step to build your team's engagement.<br> **Body** - Small steps have a large impact. You discussed results with your team, it's time to choose a Focus Area. We support you with action items, best practices, and ongoing reminders.|Choose a Focus Area.|
|Manager has an active Focus Area created. <br> *The Focus Area may or may not have an active action item associated with it. The Nudge is sent accordingly.* |**Heading** - How are you and your team progressing on your goal? <br><br> **Body** - <br> **If the goal has an active action item:** <br> **Next up on [Driver]:[Action Item]** <br> *For example: Next up on Opinions Count: Listening Tips for Leaders* <br><br> **If the goal has no active action items:** <br> **Next up on [Driver]:[Recommendation]** <br> *For example, Next up on Opinions Count: Work on Listening Tips for Leaders*|Take action on a Focus Area|
|Survey is live and manager hasn't viewed results. <br> Or, the survey is closed, an action item is created, and action is taken.|**Heading Variants** - How are you progressing on your Focus Area? Let's check-in.<br> **Body Variant** - Now is a good time to reflect, celebrate the progress you've made with your team, and decide if you'd like to keep working on this goal. If you're done, remember to mark the goal "Complete" to get credit for your work!|Reflect on action|

> [!NOTE]
> - If a user repeatedly doesn't open or interact with Nudge messages, they're automatically unsubscribed. 
> - If a user is in multiple recipient groups, they may receive emails from either group. Users never receive more than one Nudge per week. 

## How admins set up Nudges 

To set up Nudges, recipient groups must be created and enabled. Only one User Role can be selected per recipient group. You can create multiple groups to reach more User Roles or send Nudges at a different frequency for each group.

From the Viva Glint admin dashboard, select **Configuration**, then **Nudges** in the  **Notifications** section. 

### Add a new recipient group

On the Nudges landing page, select **+ New recipient group**.

#### Set up recipients 

1. Choose who receives the Nudge: 
    1. **User Role**: Select a role from the dropdown menu. Add only one User Role per group. If you have one User Role that includes all managers, it reduces the number of recipient groups you need to create.
    2. **Exclude**: Select individual users, Distribution Lists, or User Roles from the search bar.
    3. **Recipient List**: Download the list of recipients to a *.csv* file to have it for reference.  
    
#### Set up timing

Defines when and how frequently users receive Nudges. From the dropdown menu, choose to send Nudges from every one to eight weeks. Viva Glint Admins can adjust frequency after a survey launches.

- **Frequency:** Send Nudges every two to four weeks.
- **Send Day:** Choose a business day of the week for Nudges to send.
- **Window:** Select the number of days Nudge messages send after a survey closes.

> [!TIP]
> Align Nudges to your survey cadence. For example, 90 days for quarterly surveys or 180 days for biannual survey.
      
#### Enable, disable, and preview content 

Select the **Nudge #** to enable, disable, or preview Nudge messages. The corresponding preview pane opens.

- Enable or disable by using the **On** and **Off** toggle. 
- Preview what your Nudge looks like: It includes your company logo, the survey name, highlight where the user is in the results process, and a link to view results.
- Results process: 
  - Nudge #1: Interpret results 
  - Nudge #2: Share with your team 
  - Nudge #3: Choose a Focus Area (or whatever term your organization uses) 
  - Nudge #4: Focus Area reminder 

#### View enabled programs 

When Viva Glint Admins enable Nudges for Recurring and Ad Hoc surveys in Program Setup, they appear in the **Enabled programs** list. 

To enable **Nudges** for a survey program:

1. Go to **Configuration** and select **Survey Programs**.
2. Choose a survey and go to **Program Setup**.
3. Enable the **Eligible for Nudges** setting by switching the toggle to **Yes**.
4. Select **Save Changes**.

## Edit Nudge details 

Once Nudge details are saved, Viva Glint Admins can enable or disable Nudge messages for survey programs.

To make changes to a recipient group: 

1. Go to **Configuration** and select **Nudges**.
2. Select **Disable**. In the dialog that appears, select **Disable Recipient Group**.
3. Select Edit details on the group to edit. 
1. Make changes and select **Save Changes**.  
1. Select **Enable** and then **Enable Recipient Group** on the Configuration section of the Nudges landing page to enable the group for survey programs that have Nudges enabled.

## Nudge FAQs

**Q: How long do Nudges continue to send?** <br>
A: Nudges send within 90 days of the survey closing, regardless of the date Nudges are enabled. For example, if a program is on a quarterly cadence, Nudges stop when the next cycle starts.

**Q: How can I include or exclude programs from receiving Nudges?** <br>
A: Switch the **Eligible for Nudges** feature to **YES** or **NO** on the **Program Setup** page in **Program Summary**. **Suggested Action Plans** must be switched to **ON**, to enable Nudges.

**Q: Where do I view programs enabled for roles in Nudges?** <br>
A: From the admin dashboard select **Nudges**, then **View Details** (for an enabled User Role within the Configuration section). The Recipient Group Setup page opens for that User Role. Review the **Enabled Programs** section.


