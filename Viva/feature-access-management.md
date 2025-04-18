---
title: "Microsoft Viva - Feature access management"
ms.reviewer: loreenl
ms.author: loreenl
author: lizap
manager: elizapo
ms.date: 03/26/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: solution-overview
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
search.appverid:
- MET150
description: "Control who can access features in Microsoft Viva"
---
# Control access to features in Viva

To control who has access to specific Viva features you can create and update policies in the [Microsoft 365 admin center](/Viva/control-access-admin-center) or in [PowerShell](/Viva/manage-access-policies).

Policies are used to enable or disable specific features or types of data processing for users or groups in your tenant.

> [!NOTE]
> These features aren't available yet in GCC High or DoD. For GCC, see the documentation for your specific app for availability.

## Creating and managing policies  

Policies can be created and managed by a Viva admin who has permissions to do so in the [Microsoft 365 admin center](/Viva/control-access-admin-center) or in [PowerShell](/Viva/manage-access-policies). For more information, see the **Who can manage access** column in the following feature table.

Policies for copilots in Viva can also be [managed through the Copilot settings page in the Microsoft 365 admin center](/viva/copilot/copilot-access-management). These policies remain in sync with policies managed through Viva admin page.  

### Requirements
Before you can create a policy, you need:  

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing).
- User accounts created in or synchronized to Microsoft Entra ID.
- Microsoft 365 groups, Microsoft Entra security groups created in or synchronized to Microsoft Entra ID, or distribution groups.<br>
- For [PowerShell](/Viva/feature-access-management) access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later. If you need to use non-mail-enabled groups, you must have access to Exchange PowerShell version 3.5.1 or later.

## Features available to manage

You can use feature access management to manage access to the following features:

> [!NOTE]
> - Some features may not support user/group policies. In addition, policies for one app can have an impact on the entire tenant or users in your tenant. For more information, see the feature documentation by using the link in the table.
> - Only some features have the controls available for admins to provide users with the option to opt out.

|App|Feature|Control for user opt-out?|Who can manage access|ModuleID|
|-|-|-|-|-|
|Engage|[Copilot in Engage](/viva/engage/configure-copilot-for-engage)|No|AI admin**|VivaEngage|
||[AI Summarization](/viva/engage/configure-copilot-for-engage)|Yes|Engage admin|VivaEngage|
|Glint|[Copilot in Viva Glint](/viva/glint/copilot/admin-enable)*|No|Global admin|VivaGlint|
|Goals|[Copilot in Viva Goals](/viva/goals/copilot-intro)|No|Goals admin|VivaGoals|
|Insights|[Advanced Insights](/viva/insights/advanced/introduction-to-advanced-insights)|No|AI admin|VivaInsights|
||[Analyst Report Publish (preview)](/viva/insights/advanced/analyst/publish-reports)|No|Viva Insights admin|VivaInsights|
||[Copilot Dashboard](/viva/insights/org-team-insights/copilot-dashboard)|No|AI admin|VivaInsights|
||[Copilot Dashboard Auto Enablement](/viva/insights/org-team-insights/copilot-dashboard#remove-access-to-the-dashboard-for-the-entire-tenant-with-powershell)|No|AI admin|VivaInsights|
||[Copilot Dashboard Delegation](/viva/insights/org-team-insights/delegate-access)|Yes|AI admin|VivaInsights|
||[Copilot Assisted Value](https://go.microsoft.com/fwlink/?linkid=2281051)|No|AI admin|VivaInsights|
||[Copilot in Viva Insights](/viva/insights/advanced/analyst/copilot-query)|No|AI admin**|VivaInsights|
||[Digest Welcome Email](/viva/insights/advanced/setup-maint/configure-personal-insights#configure-access-at-the-tenant-level)|No| Global admin|VivaInsights|
||[Meeting cost and quality](https://aka.ms/meetingcostandqualitypost)|No|Insights admin|VivaInsights|
||[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)|No|Insights admin|VivaInsights|
|Pulse|[Customization](/viva/pulse/setup-admin-access/set-up-in-app-pulse-experience#customization)|No|Viva Pulse admin|VivaPulse|
||[Team conversations in Pulse reports](/viva/pulse/setup-admin-access/granular-access-controls#conversations-in-pulse-reports)|No|Viva Pulse admin|VivaPulse|
||[Copilot in Viva Pulse](/viva/pulse/setup-admin-access/granular-access-controls)|No|Viva Pulse admin|VivaPulse|
||[Viva Pulse experience with Microsoft 365 Copilot](/viva/pulse/setup-admin-access/granular-access-controls)|No|Viva Pulse admin|VivaPulse|
|Skills|Default Skills visibility*|Yes|Knowledge admin|VivaSkills|
||Skill suggestions*|Yes|Knowledge admin|VivaSkills|

\* The feature or feature control might not yet be available for all tenants. Support will be added soon.

\** The AI admin controls all Copilot features in Viva Engage, Viva Goals, and Viva Insights. Individual app admins can control the Copilot features they have access to.
> [!NOTE]
>
> - For information on the impact of policies on your tenant or the users in your tenant or on the functionality of other features in your tenant, see the table above for documentation on the specific feature.  
> - You can control only the access to features that support access policies and that are available in your tenant. For example, if you have an EDU-based tenant, you can't use policies to gain access to features that are not otherwise available to EDU tenants. See the table above for documentation on the specific feature.
> - You can have multiple access policies for an active feature in your organization, which means a user could be impacted by multiple policies. In that case, the most restrictive policy assigned to the user or group takes precedence. For more information, see **Which policy takes precedence** below.
> - Changes to access policies take effect for the user within 24 hours, unless noted for a specific feature. Changes for Copilot in Viva Engage might take up to 48 hours.
> - Features support org-wide and user/group policies, unless otherwise noted in that app's feature documentation.

## Which policy takes precedence?  

A user has one effective policy for each feature. It's possible, or even likely, that a user is assigned a policy and is also a member of one or more groups that's assigned a policy for the same feature. In these kinds of scenarios, a user's effective policy is determined according to the rules of precedence, as follows:  

If a user is directly assigned a policy as an individual or as a member of a group, that policy takes precedence. If a user has multiple of these policies assigned, then the most restrictive policy they're assigned applies: 

- Feature is disabled
- Feature is enabled with option for user to opt out (if available for a given feature) 
- Feature is enabled 

If a user isn't assigned a policy as an individual or member of a group, the org-wide policy applies. This is either the default setting for the feature or the tenant-wide/org-wide policy created by the admin.

> [!NOTE]
> - Changes to policies can take up to 24 hours to go into effect for most features. 
> - Changes to policies for the Copilot in Engage feature may take up to 48 hours to go into effect.
> - If users are in nested groups and you apply access policies to the parent group, the users in the nested groups receive the policies. The nested groups and the users in those nested groups must be created in or synchronized to Microsoft Entra ID.
> - When you add users to or remove them from a Microsoft Entra ID or Microsoft 365 Group, it can take 24 hours before changes to their feature access take effect.
> - When an admin removes the option for users to opt out by fully enabling or disabling the feature, the user's opt in/out preference isn't preserved and is reset to the default state. If an admin re-enables the option allowing a user to opt out of a feature, users will need to select to opt out of the feature again.
> - Quick changes to the enablement state for a feature in less than 24 hours after making the change may not result in the resetting of user opt in/out preferences.
> - For a history of policy creation, updates, and deletions, see the Viva Feature Access Management (VFAM) change logs for your organization in [Microsoft Purview](/purview/tutorial-purview-audit-logs-diagnostics).

## Additional information and best practices

- Policies are evaluated on a per-user basis.
- Only one policy per feature can be assigned to *'everyone'.* This policy serves as the global default state for that feature in your organization.
- When user identities in Microsoft Entra ID are deleted, user data is deleted from Viva feature access management. If user identities are re-enabled during the soft-deleted period, the admin needs to reassign policies to the user.
- When groups in Microsoft Entra ID and Microsoft 365 are deleted, they're deleted from the stored policies. If groups are re-enabled during the soft-deleted period, the admin needs to reassign policies to the groups.

## More

[Learn how to manage access to features in the Microsoft 365 admin center](/viva/control-access-admin-center)

[Learn how to manage access to features using PowerShell](/Viva/manage-access-policies)
