---
title: Administrator enablement for Microsoft 365 Copilot in Viva Glint
description: Administrators enable Microsoft 365 Copilot in Viva Glint. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/21/2025
---

# Administrator enablement for Microsoft 365 Copilot in Viva Glint

Prerequisites to enabling Microsoft 365 Copilot in Viva Glint:
- You have at least one Recurring or Ad hoc survey administered or closed on the Viva Glint platform
- Your dashboard default language is set to English

Admins enable Copilot in Viva Glint. Microsoft privacy policies prohibit Copilot in Viva Glint from being enabled by default for any User Roles. 

Assign yourself and others using Copilot in Viva Glint to a new User Role. Create the new User Role with access to the Comments Report enabled. Add that User Role to the survey [**Reporting** page](/viva/glint/setup/reporting-setup) in **Program Summary**.

>[!IMPORTANT]
>Users without access to the Comment Report can't access Viva Glint in Copilot.

## Grant Comment Report permission

From your admin dashboard, follow this process:

1.	Select the **configuration (cogwheel)** symbol.
2.	In the **Employees** section, select **User Roles**.
3.	Select the User Role to provide Comment Report access. In this example, Company Admin is chosen.
   
    :::image type="content" source="../../media/glint/setup/copilot-select-user.png" alt-text="Screenshot of how to give a User Role Copilot in Viva Glint permissions." lightbox="../../media/glint/setup/copilot-select-user.png":::

    > [!NOTE]
    > The Manager role has Comment Report permission enabled as a default setting.

4. Select **Permissions**.
  
   :::image type="content" source="../../media/glint/setup/copilot-permissions.png" alt-text="Screenshot of the Permissions access row in **Role Settings**." lightbox="../../media/glint/setup/copilot-permissions.png":::

5.	In the **Reporting** section of the Permissions and Access page, enable **View Comments**.

    :::image type="content" source="../../media/glint/setup/copilot-view-comments-toggle.png" alt-text="Screenshot of the View Comments checkbox.":::

## Grant Comment Reports access

The second step to enabling Copilot in Viva Glint for User Roles happens in the program's **Reporting** section. This step allows users enabled for the Comment Reports to access the report.

### Ramp up to full utilization

Copilot in Viva Glint gives you the flexibility to roll out to one or many user roles. Consider what approach is right for your organization. Viva Glint suggests this best practice for ramping to a full rollout:

1. **Admin release:** By default, Copilot in Viva Glint is available to the Admin User Role. You may decide that for the first deployment you don't want to provide access beyond this group. This can be a way to first test and better understand the functionality. Admins can also use this time to test the Copilot functionality for previously closed surveys before using it for an upcoming cycle. 
1.  **Selective deployment:** You may decide to deploy to a group beyond the admins but still not your entire eligible population. Consider which groups makes sense for you. Perhaps this is your extended HRBP team or senior leaders who have large amounts of comments. As long as the group you want to grant access to is in a set User Role group within Viva Glint, you can provide them access.
1.  **Full deployment:** Deploying to all eligible users is the highest level of deployment. This would include all roles who have results access. Even with this deployment, some leaders may not be able to use Copilot if their comments and respondents don't meet your set thresholds. For those teams that have fewer comments, Copilot may be less critical, as often these leaders can read through verbatims quickly.

From your admin dashboard, follow this process for deployment:

1.	Select the **Configuration** symbol.
2.	In the **Surveys** section, select **Survey Programs**.
3.	**Select the closed Recurring or Ad hoc program** for which you want to grant access.
4.	In **Program Summary**, select **Reporting**.

     :::image type="content" source="../../media/glint/setup/copilot-reporting.png" alt-text="Screenshot of the Reporting section in Program Summary." lightbox="../../media/glint/setup/copilot-reporting.png":::

5. In **Program Roles**, select the User Role to enable with Copilot in Viva Glint. *In this example, the customized role is 'VI'.*

    :::image type="content" source="../../media/glint/setup/copilot-program-roles.png" alt-text="Screenshot of an example User Role." lightbox="../../media/glint/setup/copilot-program-roles.png":::

6. Toggle **Copilot in Viva Glint** to **On** and then **Save Changes**.

    :::image type="content" source="../../media/glint/setup/admin-enable.jpg" alt-text="Screenshot of the Role Permissions sections within the Reporting section." lightbox="../../media/glint/setup/admin-enable.jpg":::

## Ensure Copilot in Viva Glint is enabled

From your admin dashboard, follow this process:

1.	Select the **Configuration** symbol.
2.	Select **User Roles** in the **Employees** section to see the list of all users assigned to a particular role.
3.	Select any employee in a User Role in which you expect Copilot to be enabled.
4.	Once you are on that user's profile, select **View As** to validate the user's reporting experience.

    :::image type="content" source="../../media/glint/setup/copilot-view-as.png" alt-text="Screenshot of the View As button in User Roles.":::

5. Be sure you see the **Copilot** button on the user's Viva Glint dashboard.

   :::image type="content" source="../../media/glint/setup/copilot-access-button.png" alt-text="Screenshot of the Copilot capability on the manager dashboard." lightbox="../../media/glint/setup/copilot-access-button.png":::

## Reporting steps before using Copilot in Viva Glint

Follow these steps on the [Manager Guide for reviewing feedback results](/viva/glint/setup/copilot-manager-quick-guide?branch=main#manager-process-for-reviewing-feedback-results): 

1. Review your scores on the Viva Glint Team Summary dashboard before jumping directly into Copilot.
   :::image type="content" source="../../media/glint/setup/copilot-team-summary-1.png" alt-text="Screenshot of the Manager Team Summary dashboard.":::
   
1. Review the Strengths & Opportunities section on the Viva Glint Team Summary dashboard. This dashboard shows you strengths to celebrate and opportunity areas to improve upon.
   :::image type="content" source="../../media/glint/setup/copilot-strengths-opps.png" alt-text="Screenshot of Strengths & Opportunities on the Manager Team Summary dashboard.":::
   
1. Now, ask Copilot in Viva Glint to dive deeper to uncover insights around your areas of interest.
   :::image type="content" source="../../media/glint/setup/copilot-button-1.png" alt-text="Screenshot of the Copilot button on the Manager Team Summary dashboard.":::

## Get the most from Copilot in Viva Glint

Use thee best practices to get the most from Copilot in Viva Glint. Maximize what Copilot can summarize by using these guidelines: 

### Enable comments

Enabling comments on quantitative items allows for more detailed feedback and context, enhancing the data's richness and usefulness for summarization. This approach provides a more comprehensive view of feedback, even on single-item indices. This practice, in turn, allows Copilot to generate more accurate and insightful summaries.

### Bring in relevant filter attributes

Copilot in Viva Glint uses HRIS or demographic attributes that are imported to Viva Glint to filter data. The use of attributes allows for targeted insights based on specific and impactful employee filters. Enable filter attributes that are important for the user roles interacting with Copilot. 

### Use these quick tips

[Use these tips to understand and act on employee feedback quickly](/viva/glint/setup/copilot-managers?branch=main#copilot-in-viva-glint-quick-tips-for-managers).
[Use these tips to write prompts for Copilot in Viva Glint](/viva/glint/setup/copilot-manager-quick-guide?branch=main#quick-tips-for-copilot-prompts).

### Ask open-ended questions

Open-ended survey items are valuable for capturing a wide range of feedback. Open-ended items allow respondents to freely express their thoughts on topics that may not be covered by the survey items. Comment boxes provide a space for any top-of-mind concerns or suggestions. Comments are typically detailed and offer rich data  for Copilot to generate comprehensive summaries. Comment summarization may reveal insights not apparent from quantitative data alone.

### Use Recurring and Ad Hoc programs

Where it makes sense, use Recurring and Ad Hoc programs.At this time, Copilot in Viva Glint is unable to tap into Always-On and Employee Lifecycle programs. To maximize your ability to use Copilot in Viva Glint, use Recurring program setup for ongoing topics (for example, Engagement) and Ad Hoc for one-off topics (for example, Change Management). 

## More Resources

[**Learn how managers can use Copilot in Viva Glint**](/viva/glint/setup/copilot-managers)

[**Manager Guide for Copilot in Viva Glint**](/viva/glint/setup/copilot-manager-quick-guide)

[**Find answers to technical FAQs for Copilot in Viva Glint**](/viva/glint/setup/copilot-faqs)

[**Copilot for Microsoft 365**](https://adoption.microsoft.com/copilot/)
