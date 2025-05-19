---
title: Enable Microsoft 365 Copilot in Viva Glint
description: Viva Glint Administrators enable Copilot in the Viva Glint app when the feature is enabled in the Microsoft 365 admin center.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Microsoft 365 Copilot in Viva Glint, Copilot, comment summarization
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/19/2025
---

# Enable Microsoft 365 Copilot in Viva Glint

Viva Glint Administrators enable Copilot in the Viva Glint app when the feature is enabled in the Microsoft 365 admin center. Microsoft privacy policies prohibit Copilot in Viva Glint from being enabled by default for any User Roles. 

Prerequisites to enabling Microsoft 365 Copilot in Viva Glint:

- Copilot in Viva Glint is enabled in the Microsoft 365 admin center. This feature can be managed by:
  - [Microsoft 365 Global Administrators](/entra/identity/role-based-access-control/permissions-reference#global-administrator)
  - [Viva Glint Tenant Administrators](/entra/identity/role-based-access-control/permissions-reference#viva-glint-tenant-administrator)
  - [AI Administrators](/entra/identity/role-based-access-control/permissions-reference#ai-administrator)
- You have at least one Recurring or Ad hoc survey administered or closed on the Viva Glint platform
- Your dashboard default language is set to English

Assign yourself and other leaders using Copilot in Viva Glint to a new [User Role](/viva/glint/setup/set-up-user-roles). The new User Role must have access to the Comments Report. Add that User Role to the survey [**Reporting** page](/viva/glint/setup/reporting-setup) in **Program Summary**.

## Control access in the Microsoft 365 admin center

Microsoft 365 global admins, Viva Glint Tenant Admins, and AI Admins can control the availability of Copilot in Viva Glint with [Feature access management](/viva/feature-access-management) in the Microsoft 365 admin center. Use organization-wide settings to enable or disable for your company or set up custom policies to control access for certain users or groups. When Copilot in Viva Glint is enabled in the Microsoft 365 admin center, Viva Glint Admins can [control access at the User Role level in the Viva Glint app](#enable-copilot-in-viva-glint-for-a-user-role). 

### Manage access for your organization

Manage organization-wide access in the Microsoft 365 admin center from Copilot Settings, Feature access management, or Viva Glint pages. To control access for Copilot in Viva Glint using PowerShell, see: [Control access to features in Viva using PowerShell](/viva/manage-access-policies). 

To manage access for your entire organization in the Microsoft 365 admin center from the Viva Glint page:

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home?#/homepage).
2. Select **Settings** in the menu on the left and select **Viva**.
3. Select **Viva Glint** and choose **Manage settings for Microsoft Copilot in Viva Glint**.
4. In the **Manage Microsoft Copilot in Viva Glint** pane that appears, select **Manage** in the **Org-wide setting** section.
5. Choose **On** to enable or **Off** to disable for your organization.
6. Select **Save**.

### Use custom policies to manage access for people or groups

To create a custom policy for certain people or groups in your organization:

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home?#/homepage).
2. Select **Settings** in the menu on the left and select **Viva**.
3. Select **Viva Glint** and choose **Manage settings for Microsoft Copilot in Viva Glint**.
4. Select **Create policy** in the **Custom policies for people or groups** section in the pane that appears.
5. Enter a name in the **Policy name** field.
   - To disable for certain users, select **Off for specific people** and add users or groups to the **Add the people or groups this policy applies to** field.
   - To enable for certain users, select **On for specific people** and add users or groups to the **Add the people or groups this policy applies to** field.
6. Select **Save**.

### Viva Glint app experiences based on Copilot status in the Microsoft 365 admin center

Use this table to determine different Copilot in Viva Glint user experiences depending on how and where admins enable Copilot in Viva Glint.

| Copilot in Viva Glint status in the Microsoft 365 admin center | Viva Glint Admin experience in app   | Viva Glint dashboard user experience in app |
|:----------|:-----------|:------------|
| Disabled for org | Copilot toggle in User Roles is gray/view-only  | Copilot entry points in reports are hidden, regardless of User Role Copilot toggle status|
| Enabled for org | Copilot toggle in User Roles is editable for all non-Company Admin roles | Copilot entry points visible when a user is in a role with Copilot enabled|  
| Disabled for people or groups | Copilot toggle in User Roles is editable for all non-Company Admin roles | Copilot entry points in reports are hidden, regardless of User Role Copilot toggle status, for specified people or groups |
| Enabled for people or groups  | Copilot toggle in User Roles is editable for all non-Company Admin roles | Copilot entry points in reports are visible for specified people or groups when they're in a User Role with Copilot enabled |

## Grant access in the Viva Glint app

When enabled in the Microsoft 365 admin center, Viva Glint Admins can manage access to Copilot in Viva Glint at the User Role level in the Viva Glint app.

> [!IMPORTANT]
> Users without access to the Comments Report and a role that gives permission to view comments can't access Copilot in Viva Glint.

### Ramp up to full utilization

Copilot in Viva Glint gives you the flexibility to roll out to one or many user roles. Consider what approach is right for your organization. Viva Glint suggests this best practice for ramping to a full rollout:

1. **Admin release:** By default, Copilot in Viva Glint is available to the Admin User Role. You may decide that for the first deployment you don't want to provide access beyond this group. This initial release can be a way to first test and better understand the functionality. Admins can also use this time to test the Copilot functionality for previously closed surveys before using it for an upcoming cycle. 
1.  **Selective deployment:** You may decide to deploy to a group beyond the admins but still not your entire eligible population. Consider which groups make sense for you. Perhaps these groups are your extended HRBP team or senior leaders who have large amounts of comments. As long as the group you're granting access to is part of a set User Role group, they can have access.
1.  **Full deployment:** Deploying to all eligible users is the highest level of deployment. These users include all roles who have results access. Even with this deployment, some leaders may not be able to use Copilot if their comments and respondents don't meet your set thresholds. For those teams that have fewer comments, Copilot may be less critical, as often these leaders can read through verbatims quickly.

### Grant a User Role permission to view comments

From your admin dashboard, follow this process:

1. Select **Configuration**.
2. In the **Employees** section, select **User Roles**.
3. Select the User Role to provide Comments Report access.

    > [!NOTE]
    > The Manager role has the **View Comments** permission enabled as a default setting.

4. Select **Permissions**.
  
   :::image type="content" source="../../media/glint/setup/copilot-permissions.png" alt-text="Screenshot of the Permissions access row in **Role Settings**." lightbox="../../media/glint/setup/copilot-permissions.png":::

5. In the **Reporting** section of the Permissions and Access page, enable **View Comments**.

    :::image type="content" source="../../media/glint/setup/copilot-view-comments-toggle.png" alt-text="Screenshot of the View Comments checkbox.":::

### Enable Copilot in Viva Glint for a User Role

The second step to enabling Copilot in Viva Glint for User Roles happens in the program's **Reporting** section. 

From your admin dashboard, follow this process:

1. Select **Configuration**.
2. In the **Surveys** section, select **Survey Programs**.
3. **Select the closed Recurring or Ad hoc program** for which you want to grant access.
4. In **Program Summary**, select **Reporting**.

     :::image type="content" source="../../media/glint/setup/copilot-reporting.png" alt-text="Screenshot of the Reporting section in Program Summary." lightbox="../../media/glint/setup/copilot-reporting.png":::

5. In **Program Roles**, select the User Role to enable with Copilot in Viva Glint. *In this example, the customized role is 'VI.'*

    :::image type="content" source="../../media/glint/setup/copilot-program-roles.png" alt-text="Screenshot of an example User Role." lightbox="../../media/glint/setup/copilot-program-roles.png":::

6. Toggle **Copilot in Viva Glint** to **On** and confirm that the role has **Comments** selected in the **Report Template Access** section.

    :::image type="content" source="../../media/glint/setup/copilot-enabled2.png" alt-text="Screenshot of the Role Permissions sections within the Reporting section." lightbox="../../media/glint/setup/copilot-enabled2.png":::

7. Select **Save Changes** in the top right of the **Reporting** page.

## Ensure Copilot in Viva Glint is enabled

From your admin dashboard, follow this process:

1. Select **Configuration**.
2. Select **User Roles** in the **Employees** section to see the list of all users assigned to a particular role.
3. Select any employee in a User Role in which you expect Copilot to be enabled.
4. Once you are on that user's profile, select **View As** to validate the user's reporting experience.

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

Use these guidelines to maximize what Copilot can summarize: 

### Enable comments

Enabling comments on quantitative items allows for more detailed feedback and context, enhancing the data's richness and usefulness for summarization. This approach provides a more comprehensive view of feedback, even on single-item indices. This practice, in turn, allows Copilot to generate more accurate and insightful summaries.

### Bring in relevant filter attributes

Copilot in Viva Glint uses HRIS or demographic attributes that are imported to Viva Glint to filter data. The use of attributes allows for targeted insights based on specific and impactful employee filters. Enable filter attributes that are important for the user roles interacting with Copilot. 

### Use these quick tips

- [Use these tips to understand and act on employee feedback quickly](/viva/glint/setup/copilot-managers?branch=main#copilot-in-viva-glint-quick-tips-for-managers).

- Need help with writing prompts? [Use these tips to get started writing prompts for Copilot in Viva Glint](/viva/glint/setup/copilot-manager-quick-guide?branch=main#quick-tips-for-copilot-prompts).

### Ask open-ended questions

Open-ended survey items are valuable for capturing a wide range of feedback. Open-ended items allow respondents to freely express their thoughts on topics that aren't covered by the survey items. Comment boxes provide a space for any top-of-mind concerns or suggestions. Comments are typically detailed and offer rich data  for Copilot to generate comprehensive summaries. Comment summarization may reveal insights not apparent from quantitative data alone.

### Use Recurring and Ad Hoc programs

At this time, Copilot in Viva Glint is unable to tap into Always-On and Employee Lifecycle programs. To maximize your ability to use Copilot in Viva Glint, use Recurring program setup for ongoing topics (for example, Engagement) and Ad Hoc for one-off topics (for example, Change Management).

## More Resources

[**Learn how managers can use Copilot in Viva Glint**](/viva/glint/setup/copilot-managers)<br>
[**Manager Guide for Copilot in Viva Glint**](/viva/glint/setup/copilot-manager-quick-guide)<br>
[**Find answers to technical FAQs for Copilot in Viva Glint**](/viva/glint/setup/copilot-faqs)<br>
[**Copilot for Microsoft 365**](https://adoption.microsoft.com/copilot/)
