---
ms.date: 03/05/2025
title: Enable or disable advanced insights with PowerShell 
description: Learn how to turn advanced insights for Viva Insights on or off with PowerShell cmdlets
author: zachminers
ms.author: v-zachminers
ms.topic: install-set-up-deploy
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Enable or disable advanced insights with PowerShell

*Applies to: Microsoft 365 global admin*

Advanced insights is on by default, but users can't access advanced insights until the Microsoft 365 global admin [assigns the roles](./assign-user-roles.md) of Insights admin and Insights analyst.

Once roles are assigned, this feature access control allows global admins to enable or disable advanced insights for Viva Insights using PowerShell cmdlets. This control supports tenant-level policies only, not user or group-level policies. If you disable advanced insights, Insights analysts can't access advanced insights, but Insights admins *can* still access certain features such as privacy settings, manager settings, and partitions.

## Steps

1. [Connect to Exchange Online](./configure-personal-insights.md#connect-to-exchange-online) and, when prompted, sign in with your admin credentials. 

2. After you've signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet: [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy).

### Example: Turn off advanced insights for your tenant

```powershell
 ModuleId : VivaInsights
 FeatureId : AdvancedInsights
 Name : DisableFeatureForAll
 IsFeatureEnabled : false
 Everyone
```

[Learn more about how to set these policies](/viva/feature-access-management).

You can also manage these features in the Microsoft 365 admin center. [Learn how](/viva/control-access-admin-center).

## Next steps

> [!div class="nextstepaction"]
> [Assign manager and leader permissions](./manager-settings.md)