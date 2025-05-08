---
title: "Microsoft Viva - Feature access management using PowerShell"
ms.reviewer: elizapo
ms.author: loreenl
author: loreenl
manager: elizapo
ms.date: 02/18/2025
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
description: "Control who can access features in Microsoft Viva using PowerShell"
---

# Control access to features in Microsoft 365 using PowerShell

You can use access policies to manage which users can access specific features in Microsoft 365 apps with PowerShell. Feature access management lets you enable or disable specific features for specific groups or users in your tenant and so tailor your deployments to meet your local regulatory and business requirements.

An authorized admin in your tenant can create, assign, and manage access policies from PowerShell. When a user signs in to Microsoft 365, the policy settings are applied, and they only see the features that haven't been disabled.

> [!IMPORTANT]
> You can have multiple access policies for a feature active in your organization. That means that a user or group could be impacted by multiple policies. In that case, the most restrictive policy assigned directly to a user or group takes precedence. For more information, see [How access policies work](/Viva/feature-access-management).

## Requirements

Before you can create an access policy, you need:

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)
- Access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later. If you need to use non-mail-enabled groups you must have access to Exchange PowerShell version 3.5.1 or later. If you need to setup policies with the user opted-out by default (soft-disable), you must have access to Exchange PowerShell version 3.8.0 or later.

- User accounts created in or synchronized to Microsoft Entra ID
- Microsoft 365 groups, Microsoft Entra security groups created in or synchronized to Microsoft Entra ID, or distribution groups.
- The [role required for the specific app and feature](/viva/feature-access-management#features-available-to-manage).


> [!IMPORTANT]
> These features are not yet available in GCC High or DoD. For GCC, refer to the documentation for your specific app for availability.

## Create and manage access policies for Microsoft 365 features

Policies can be created and managed by an admin who has permissions to do so in the Microsoft 365 admin center or by using PowerShell. [Get all the details about creating and managing policies](/viva/feature-access-management#creating-and-managing-policies). For detailed instructions on how to construct a command in PowerShell, please refer to the [PowerShell documentation](/powershell/module/exchange/?view=exchange-ps&branch=main). 

### Get the featureID for the feature
Before you can create an access policy, use the **ModuleID** to get the **featureID** for the specific feature you want to control access to.

**Module IDs**

|App|ModuleID|
|-|-|
|Engage|VivaEngage|
|Glint|VivaGlint|
|Goals|VivaGoals|
|Insights|VivaInsights|
|Pulse|VivaPulse|
|Skills*|PeopleSkills*|

*Policies for People Skills can only be created via PowerShell at this time. You cannot use the interface in Microsoft 365 admin center to create policies for People Skills features.

Use the **[Get-VivaModuleFeature](/powershell/module/exchange/get-vivamodulefeature)** PowerShell cmdlet to get a list of all of the features available in a specific Microsoft 365 app and their associated IDs.

1. Install Exchange Online PowerShell Version 3.2.0 or later:

   ```PowerShell
   Install-Module -Name ExchangeOnlineManagement
   ```

2. Connect to Exchange Online with admin credentials:

   ```PowerShell
   Connect-ExchangeOnline
   ```

   Complete the authentication as the role required for the specific feature you're creating the policy for.

3. Run the [Get-VivaModuleFeature](/powershell/module/exchange/get-vivamodulefeature) cmdlet to see the features that you can manage by using an access policy.  

   For example, to see which features are supported in Viva Insights, run the following cmdlet:

   ```PowerShell
   Get-VivaModuleFeature -ModuleId VivaInsights
   ```
4. Find the feature that you'd like to create an access policy for and make note of its **featureID**.

### Create an access policy

> [!TIP]
> We recommend admins refer to [PowerShell documentation](/powershell/module/exchange/?view=exchange-ps&branch=main) for a complete list of available commands to create and manage policies. This includes advanced policies for features with user opt-in controls, soft-disabling features, and detailed instructions on PowerShell command syntax.

Now that you have the **featureID**, use the [**Add-VivaModuleFeaturePolicy**](/powershell/module/exchange/add-vivamodulefeaturepolicy) PowerShell cmdlet to create an access policy for the feature.

You can assign a maximum of 10 policies per feature to users and groups. Each policy can be assigned to a maximum of 20 users or groups. You can assign one additional policy per feature to the entire tenant by using the *-Everyone* parameter, which will function as a global default state for that feature across your organization.

Run the [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy) cmdlet to create a new access policy.

> [!NOTE]
> If your feature supports user controls for opt out, make sure you set the *IsUserControlEnabled* parameter when you create the policy. If you don't, user controls for the policy uses the default state for the feature.

For example, run the following to create an access policy, called *UsersAndGroups*, to restrict access to the Reflection feature in Viva Insights.

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso.com    
   ```
This example adds a policy for the Reflection feature in Viva Insights. The policy disables the feature for the specified users and group members. If you want to disable the feature for all users, use the *-Everyone* parameter instead.


### Manage access policies

You can update an access policy to change whether a feature is enabled or disabled, as well as to change who the policy applies to (everyone, a user, or a group).

For example, building on our last example, to update who the policy applies to, run the following cmdlet:

```powershell
Update-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx -GroupIds group1@contoso.com,group2@contoso.com
```

Just like when you create the policy, if your policy supports user controls, include the *IsUserControlEnabled* parameter when you change the policy.

> [!IMPORTANT]
> Values that you specify for the *-UserIds* and *-GroupIds* parameters or the *-Everyone* parameter overwrite any existing users or groups. To preserve the existing users and groups, you need to specify those existing users or groups *and* any additional users or groups that you want to add. Not including existing users or groups in the command effectively removes those specific users or groups from the policy. You can't update a policy for a particular user or group to include the entire tenant if a policy for the entire tenant already exists for the feature - only one tenant-wide policy is supported.

To check what features are disabled for a specific user or group, run the [Get-VivaModuleFeatureEnablement](/powershell/module/exchange/get-vivamodulefeatureenablement) cmdlet. This cmdlet returns what's called the *enablement status* for the user or group.

For example:

```powershell
Get-VivaModuleFeatureEnablement -ModuleId VivaInsights -FeatureId Reflection -Identity user@contoso.com
```

### Delete an access policy

Use the [Remove-VivaModuleFeaturePolicy](/powershell/module/exchange/remove-vivamodulefeaturepolicy) cmdlet to delete an access policy.

For example, to delete the Reflection feature access policy, start by getting the specific UID for the access policy - you can get that by running [Get-VivaModuleFeaturePolicy](/powershell/module/exchange/get-vivamodulefeaturepolicy). Then, run the following cmdlet:

```powershell
Remove-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```
### Troubleshooting

- If you have issues creating or using access policies for Viva app features, confirm the feature you're trying to set a policy for is listed in the [feature table](/Viva/feature-access-management#features-available-to-manage) and is available to your tenant.
- If you see the error message "Requester was not authorized to complete the request" while you're running a PowerShell cmdlet, check if you have any conditional access policy set that blocks specific IP addresses. If so, either remove your IP address from that policy or create a new policy to allowlist your IP address. Learn more about [Microsoft Entra Conditional Access](/entra/identity/conditional-access/) and [Troubleshooting Conditional Access using the What If tool](/entra/identity/conditional-access/troubleshoot-conditional-access-what-if).



## More resources

[Learn more about creating and managing policies](/Viva/feature-access-management)

[Control who can access features in Microsoft Viva using the Microsoft 365 admin center](/viva/control-access-admin-center)

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
