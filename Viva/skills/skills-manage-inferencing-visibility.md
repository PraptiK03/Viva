---
title: Manage skills inferencing and visibility 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 04/29/2025
audience: admin
ms.topic: overview
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
ms.localizationpriority: medium
description: This article describes how to manage skill suggestions and skill visibility.
---

# Manage skills inferencing and visibility 

As an admin, you can set privacy and visibility controls for users, groups, or the entire tenant to meet your organization's needs. People Skills provides access controls using [Feature Access Management](/viva/feature-access-management) to ensure you comply with user privacy and local regulations.

## Manage if skills are suggested

Skills inferencing controls are enabled by default, but you can let users opt in or out or disable inferencing entirely either before or after setting up People Skills.

- Admins can turn skills inferencing auto-on. Individual users can opt out. 
- Admins can turn skills inferencing auto-off. Individual users can opt in.  
- Admins can disable skills inferencing for their tenant.

## Manage if skills are shared 

Skills visibility controls whether users can see their colleagues’ skills on surfaces like the people card or in Copilot. All skills in a user's profile are shared and visible by default once you set up People Skills in your tenant. You can also change these visibility controls before or after setting up People Skills.

- Admins can turn skills visibility auto-on. Individual users can opt out. 
- Admins can turn skills visibility auto-off. Individual users can opt in.
- Admins can disable skills visibility of some skills (AI suggested or Org added skills) for their tenant. *

* We offer granular visibility controls so you can control sharing of an entire skills profile, or for types of skills such as AI-suggested skills or Org added skills. Admins cannot completely disable skills profile visibility, as a user can always opt in to sharing their skills profile from their personal skills settings in Profile Editor. However, admins can disable sharing of some skills such as AI-suggested, or org. added skills.

:::image type="content" source="../media/skills/skills-user-privacy-settings.png" alt-text="A screenshot of the different ways a user can set privacy options for sharing People Skills." lightbox="../media/skills/skills-user-privacy-settings.png":::  

## Manage skill suggestions and where skills are shared 

Navigate to the People Skills setup page and select **Settings** to manage where skills are shared.

### Manage skills data sharing with Viva Insights  

When checked in the Settings, skills in Viva is passed on to Viva Insights. Skills in Insights allow organizations and leaders to discover skills within their workforce and assess skill distribution across groups. [Learn more about skills in Viva Insights.](https://go.microsoft.com/fwlink/?linkid=2320729)

You can stop skills data from being shared with Viva Insights by unchecking this setting.

### Manage AI skill suggestions

Select **Skill inferencing by AI** under **Settings** to see details about the AI inferencing settings.  People Skills provides access controls using [Feature Access Management](/viva/feature-access-management) to ensure you comply with user privacy and local regulations.

Users receive skill suggestions relevant to their role when inferencing is enabled. When skill suggestions are turned off, users don't see any suggested skills and can only manually confirm skills from a list.

Create an access control policy if you need to disable skill suggestions for specific users, groups, or your entire tenant. For more information on how to create and manage policies, see [control access to features](../feature-access-management.md). 

> [!NOTE]
> Policies for People Skills can only be created in PowerShell at this time. You can’t create or manage policies through the interface in Admin center.

You have the following options for creating an access control policy in PowerShell to manage skills inferencing:  

- **Enable skills inferencing (Default):** When inferencing is enabled, users receive skill suggestions relevant to their role. Users have the option to turn it off for themselves in their skill settings. 

- Keep skills inferencing enabled but default off: Skills inferencing is available in your tenant, but users in this access policy will be "opted-out," and won't receive inferencing suggestions. Users have the option to turn it on for themselves in their skill settings.

   To create this policy, run the following PowerShell cmdlet. 

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsInferencing -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *SkillsInferencing*.

- **Completely disable skills inferencing:** With this policy, skills inferencing is disabled for your tenant and users can't opt in to receiving skill inferencing suggestions.

   To create this policy, run the following PowerShell cmdlet:

     ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsInferencing -Name HardDisable -IsFeatureEnabled $false 
   ```
   
     For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *SkillsInferencing*.

### Manage skills visibility

Select **Skills profile visibility** under **Settings** to see details about the sharing settings.  People Skills provides access controls using [Feature Access Management](/viva/feature-access-management) to ensure you comply with user privacy and local regulations.

An individual’s skills profile, consisting of AI-suggested, confirmed, and third-party imported skills, will be visible to other people in your organization by default.  

Admins can manage which skills will be seen across the various skills-related experiences in Microsoft 365, such as the profile card, other Microsoft Viva products, and other connected applications, by using skills visibility controls.

> [!NOTE]
> Policies for skills visibility controls can only be created in PowerShell at this time. You can’t create or manage policies through the interface in Admin center.

We offer granular visibility controls so you can control sharing of an entire skills profile, or specific types of skills such as AI-suggested skills or org-added skills.  

Types of skills sharing controls offered:  

- Visibility of entire user skills profile (Parent control): An individual’s skills profile consists of AI-suggested skills, user confirmed skills and third-party imported skills.

- Visibility of AI-suggested skills: AI-suggested skills are skill suggestions based on AI inferencing that are relevant to a user’s role and their Microsoft 365 activity. 

- Visibility of org added skills: Third-party skills, imported by your organization or may have been previously confirmed by a user in a third-party product, appear in a user’s skills profile alongside other AI-suggested skills.

#### Control visibility of entire user skills profile (Parent control)

By default, a user’s skills profile is shown to others in their organizations and shared with other Microsoft 365 experience. If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy.

> [!NOTE]
> If sharing is disabled or "opted-out" by a user, all user skills will be private and won't be shown to other users or shared with any Microsoft 365 experiences.

You have the following options for creating an access control policy in PowerShell to manage visibility of entire user skills profile:  

- Enable profile visibility (Default): When visibility is enabled, users skills profile is shared across Microsoft 365. Users have the option to turn it off for themselves in their skill settings. 

- Keep the default off for profile visibility: Users in this access policy will be "opted-out,” and their skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings.

   To create this policy, run the following PowerShell cmdlet:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsProfileVisibility -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *SkillsProfileVisibility*.

> [!NOTE]
> We don't offer the option to completely disable skills profile visibility. A user can always opt in to sharing their skills profile from their personal skills settings in Profile Editor. Admins can disable sharing of some skills such as AI-suggested, or org. added skills 

#### Control visibility of AI-suggested skills (child control) 

By default, a user’s AI-suggested skills are shown to others in their organizations and shared with other Microsoft 365 experiences. People Skills provides access controls using [Feature Access Management](/viva/feature-access-management) to ensure you comply with user privacy and local regulations.

> [!NOTE]
> These skills are only shared if Skills Profile visibility is also enabled or shared. If sharing is disabled, AI-suggested skills won't be shown to other users or shared with any Microsoft 365 experiences. 

If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy.

You have the following options for creating an access control policy in PowerShell to manage the visibility of AI-suggested skill:  

- Enable AI-suggested skills visibility (Default): When visibility is enabled, AI-suggested skills are shared across Microsoft 365. Users have the option to turn it off for themselves in their settings.

- Keep the default off for AI-suggested skill sharing: Users in this access policy will be "opted-out," and their AI-suggested skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings.

   To create this policy, run the following PowerShell cmdlet:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowAISkills -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *ShowAISkills*.

- Complete AI-suggested skill sharing: With this policy, AI-suggested skills aren't shared with Microsoft 365 experience in your tenant and users can't opt in to sharing their AI skill suggestions.  

   To create this policy, run the following PowerShell cmdlet:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowAISkills -Name  HardDisable -IsFeatureEnabled $false 
   ```

   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *ShowAISkills*.

#### Control visibility of third-party skills imported by your organization (child control)

By default, third-party skills are displayed to others in their organizations and shared with other Microsoft 365 experiences. People Skills provides access controls using [Feature Access Management](/viva/feature-access-management) to ensure you comply with user privacy and local regulations.

> [!NOTE]
> These skills are only shared if Skills Profile visibility is also enabled or shared. If sharing is disabled, third-party skills won’t display to other users or get shared with any Microsoft 365 experiences. 

If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy. 

You have the following options for creating an access control policy in PowerShell to manage third-party skills visibility imported by your organization:  

- Enable third-party skills visibility (Default): When visibility is enabled, third-party skills are shared across Microsoft 365. Users have the option to turn it off for themselves in their settings. 

- Keep the default off for third-party skill sharing: Users in this access policy will be "opted-out,” and their third-party skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings.

   To create this policy, run the following PowerShell cmdlet:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowOrgAddedSkills -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *ShowOrgAddedSkills*.

- Complete third-party skill sharing: With this policy, third-party skills aren't shared with Microsoft 365 experience in your tenant and users can't opt in to sharing their third-party skills. 

   To create this policy, run the following PowerShell cmdlet:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowOrgAddedSkills -Name HardDisable -IsFeatureEnabled $false 
   ```
  
   For this example, the **ModuleId** is *PeopleSkills*, and the **featureId** is *ShowOrgAddedSkills*.

For more information on how to create and manage policies, see [control access to features](../feature-access-management.md).  
