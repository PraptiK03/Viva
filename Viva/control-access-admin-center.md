---
title: "Microsoft Viva - Control who can access features in Microsoft Viva using the Microsoft 365 admin center"
ms.reviewer: loreenl
ms.author: loreenl
author: lizap
manager: elizapo
ms.date: 01/24/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Control who can access features in Microsoft Viva using the Microsoft 365 admin center"
---

# Control who can access features in Microsoft 365 using the Microsoft 365 admin center

To control who has access to specific Microsoft 365 features and tailor your deployments to meet your local regulatory or business requirements, you can create and update policies in the Microsoft 365 admin center.

Policies are used to enable or disable specific features or types of data processing for users or groups in your tenant. [Learn more about policies](/viva/feature-access-management).

> [!NOTE]
> - You can override your org-wide setting by using custom policies to apply only to specific users or groups. 
> - Custom policies take precedence over your org-wide settings. For example, if you have organization-wide access turned off, a custom policy could still allow access for specific users or groups. If there are no custom policies set for a user or group, the organizational setting will apply. For more details, see [Which policy takes precedence](/viva/feature-access-management?#which-policy-takes-precedence).
> - Policies for People Skills can only be created via PowerShell at this time. You cannot use the interface in Microsoft 365 admin center to create policies for People Skills features.

## Create a policy
1.	From the Microsoft 365 admin center, select **Viva** from the settings menu. 
2.	Select the **Settings** tab and select **Manage feature access**. 
3.	Select **Create a policy**. 
4.	Name the policy and select the app and feature for which you'd like to set the policy. 
5.	Select the **Access setting** option and choose **On** or **Off** to enable or disable the feature. Some features also allow the option for users to opt out.
6.	Select **Everyone** or **Specific people and groups** under **Apply access settings to**. If you didn't select Everyone, add the specific people and groups you want to apply the policy to.
7.	Select **Save**. 
8.	Select **Next** to review.
9.	Once you've reviewed your policy, select **Create policy**.

    :::image type="content" source="media\viva-create-policy.png" alt-text="Create policy pane" lightbox="media\viva-create-policy.png":::

    After saving, you'll see that your policy was created.

    :::image type="content" source="media\viva-policy-created.png" alt-text="Policy created pane" lightbox="media\viva-policy-created.png":::

    > [!NOTE]
    > - You can assign a maximum of 10 policies per feature to users and groups. Each policy can be assigned to a maximum of 20 users or groups. 
    > - Policy names must be unique.
 
## View policy details
1.	From the Microsoft 365 admin center, select **Viva** from the settings menu. 
2.	Select the Settings tab and select **Manage feature access**. 
3.	Select the policy name to view the details.

    :::image type="content" source="media\viva-policy-edit.png" alt-text="View details policy pane" lightbox="media\viva-policy-edit.png":::

## Edit an existing policy 
1.	From the Microsoft 365 admin center, select **Viva** from the settings menu. 
2.	Select the Settings tab and select **Manage feature access**. 
3.	Select the vertical ellipses (More actions) and choose **Edit policy**. 
4.	Edit the desired fields.
5.	Select **Next** to review and then select **Save**. 

## Delete an existing policy 
1.	From the Microsoft 365 admin center, select **Viva** from the settings menu. 
2.	Select the **Settings** tab and select **Manage feature access**. 
3.	Select the policy you'd like to delete. 
4.	Select **Delete policy**. 
5.	Confirm you'd like to delete the policy. 

## Additional information and best practices
- Changes to access policies take effect for the user within 24 hours, unless noted for a specific feature. Changes for Copilot in Viva Engage might take up to 48 hours. 
- When you add users to or remove them from a Microsoft Entra ID or Microsoft 365 group, it can take up to 24 hours before changes to their feature access take effect. 
- When you have a policy enabled with the option for users to opt out of a feature, and then you change the Access setting to on or off, the ability for users to opt out is removed. In this case, a user's opt out preference is not preserved and is reset to the default state. If the option to opt-out is re-enabled, users would need to opt out of the feature again. However, it is important to know that if there are multiple changes to access settings within a 24-hour period, the user's preference may not reset to the default state.
- For a history of policy creation, updates, and deletions, see the Viva Feature Access Management (VFAM) change logs for your organization in  Microsoft Purview. 
- When user identities in Microsoft Entra ID are deleted, user data is deleted from Viva feature access management. If user identities are re-enabled during the soft-deleted period, the admin needs to reassign policies to the user. 
- When groups in Microsoft Entra ID and Microsoft 365 are deleted, they're deleted from the stored policies. If groups are re-enabled during the soft-deleted period, the admin needs to reassign policies to the groups.

## More resources

[Learn more about policies](/Viva/feature-access-management)

[Manage feature access using PowerShell](/viva/manage-access-policies)

[Microsoft Viva Privacy](/viva/viva-privacy)

[Microsoft Viva Security](/viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)

