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

As an admin, you can set privacy and visibility controls for users, groups, or the entire tenant to meet your organization's needs. People Skills provides access controls using Feature Access Management to ensure you comply with user privacy and local regulations.

## Manage if skills are suggested 

Skills inferencing controls are enabled by default, but you can let users opt in or out after setting up People Skills in your tenant. 

- Admins can turn skills inferencing auto-on. Individual users can opt out. 
- Admins can turn skills inferencing auto-off. Individual users can opt in.  
- Admins can disable skills inferencing for their tenant.

## Manage if skills are shared 

Skills visibility controls whether users can see their colleagues’ skills on surfaces like the people card or in Copilot. All skills in a user's profile is shared and visible by default once you set up People Skills in your tenant. 

- Admins can turn skills visibility auto-on. Individual users can opt out. 
- Admins can turn skills visibility auto-off. Individual users can opt in.
- Admins can disable skills visibility for their tenant.  

:::image type="content" source="../media/skills/skills-user-privacy-settings.png" alt-text="A screenshot of the different ways a user can set privacy options for sharing People Skills." lightbox="../media/skills/skills-user-privacy-settings.png":::

> [!NOTE]
> We'll share instructions on managing skills inferencing and visibility controls before People Skills general availability.  

## Manage where skills are shared and skills suggestions 

Navigate to the People Skills setup page and select **Settings** to manage where skills are shared.

### Manage skills data sharing with Viva Insights  

When checked, Skills in Viva is passed on to Viva Insights. Skills in Insights allow organizations and leaders to discover skills within their workforce and assess skill distribution across groups. [Learn more about Skills in Viva Insights.]()

You can stop skills data from being shared with Viva Insights by unchecking this setting.

### Manage skills AI suggestions  

Select **Skill inferencing by AI** under **Settings** to see details about the AI inferencing settings.  

Users receive skill suggestions relevant to their role when inferencing is enabled. When skill suggestions are turned off, users don't see any suggested skills and can only manually confirm skills from a list.

Create an access control policy if you need to disable skill suggestions for specific users, groups, or your entire tenant.  

> [!NOTE]
> You can only create policies for People Skills using PowerShell at this time. You can’t create or manage policies through the interface in Admin Center.

#### Create access policy for People Skills using PowerShell

You have the following options while creating an access control policy:  

- Enable skills inferencing (Default): When inferencing is enabled, users receive skill suggestions relevant to their role. Users have the option to turn it off for themselves in their skill settings. 

- Turn off the default for skills inferencing: Skills inferencing is available in your tenant, but users in this access policy will be "opted-out," and won't receive inferencing suggestions. Users have the option to turn it on for themselves in their skill settings. 

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsInferencing -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

- Completely disable skills inferencing: Skills inferencing is disabled for your tenant and users can't opt in to receiving skill inferencing suggestions.

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsInferencing -Name HardDisable -IsFeatureEnabled $false 
   ```

For more information on how to create and manage policies, see [control access to features in Viva](../feature-access-management.md). 

### Manage skills visibility

Select **Skills profile visibility** under **Settings** to see details about the sharing settings.  

An individual’s skills profile, consisting of AI-suggested, confirmed, and third-party imported skills, will be visible to other people in your organization by default.  

Admins can manage which skills will be seen across the various skills-related experiences in Microsoft 365, such as the profile card, other Microsoft Viva products, and other connected applications, by using skills visibility controls.  

We offer granular visibility controls so you can control sharing of an entire skills profile, or for types of skills such as AI-suggested skills or third party skills.  

Types of skills sharing controls offered:  

- Visibility of entire user skills profile (Parent Control): An individual’s skills profile  consists of AI-suggested skills, user confirmed skills and third-party imported skills. If sharing is disabled, all user skills will be private and won't be shown to other users or shared with any Microsoft 365 experiences.  

- Visibility of AI suggested skills: AI-suggested skills are skills suggestions based on AI inferencing that are relevant to a user’s role. These skills will only be shown if the skills profile (parent) is also set to visible.  

- Visibility of third party skills: Third party skills were imported by your organization and may have been previously confirmed by a user in a third-party product. These skills will only be shown if the skills profile (parent) is also set to visible.  

#### Control visibility of entire user skills profile (Parent Control)

An individual’s skills profile consists of AI-suggested skills, user confirmed skills and third-party imported skills. By default, a user’s skills profile is shown to others in their organizations and shared with other Microsoft 365 experience. If sharing is disabled, all user skills will be private and won't be shown to other users or shared with any Microsoft 365 experiences.  

If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy. For more information, see control access to features in Viva.  

> [!NOTE]
> Policies for People Skills can only be created by PowerShell at this time and can't be created or managed through the Admin Center.  

#### Create access policy for Visibility using PowerShell 

You have the following options while creating an access control policy:  

- Enable profile visibility (Default): When visibility is enabled, users skills profile is shared across Microsoft 365. Users have the option to turn it off for themselves in their skill settings. 

- Turn off the default for profile visibility: Users in this access policy will be "opted-out,” and their skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings. 
   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId SkillsProfileVisibility -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

   > [!NOTE] 
   > We don't offer the option to completely disable Skills profile visibility, a user can always opt in to sharing their skills from their personal skills stings in Profile Editor.  

For more information on how to create and manage policies, see control access to features in Viva.  

### Control Visibility of AI suggested skills  

AI-inferred skills are suggested to users based on their role and Microsoft 365 activity.  

By default, a user’s AI suggested skills are shown to others in their organizations and shared with other Microsoft 365 experiences. 

> [!NOTE]
> These skills are only shared if the parent control (Skills Profile visibility) is also enabled/shared. If sharing is disabled, AI suggested skills won't be shown to other users or shared with any Microsoft 365 experiences. 

If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy. For more information, see control access to features in Viva.  

> [!NOTE]
> Policies for People Skills can only be created by PowerShell at this time and can't be created or managed through the Admin Center.  

#### Create access policy for AI-suggested skill visibility using PowerShell 

You have the following options while creating an access control policy:  

- Enable AI-suggested skill visibility (Default): When visibility is enabled, AI-suggested skills are shared across Microsoft 365. Note: These skills are only shared if parent control (Skills Profile visibility) is also enabled/shared. Users have the option to turn it off for themselves in their settings.

- Turn off the default for AI-suggested skill sharing: Users in this access policy will be "opted-out,” and their AI-suggested skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings.

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowAISkills -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

- Completely AI-suggested skill sharing: AI-suggested skills aren't shared with Microsoft 365 experience in your tenant and users can't opt in to sharing their AI skill suggestions.  

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowAISkills -Name  HardDisable -IsFeatureEnabled $false 
   ```

Read more about control access to features in Viva.  

### Control visibility of third-party skills imported by your organization  

Third-party skills imported from a third-party system and added by your organization display in a user’s skills profile alongside other AI-suggested skills.

By default, third-party skills display to others in their organizations and shared with other Microsoft 365 experiences.

> [!NOTE]
> These skills are only shared if Skills Profile visibility is also enabled or shared. If sharing is disabled, third-party skills won’t display to other users or get shared with any Microsoft 365 experiences. 

If you need to disable sharing for specific users, groups, or your entire tenant, create an access control policy. Read more about controlling access to features in Viva.  

> [!NOTE]
> Policies for People Skills can only be created by PowerShell at this time and can't be created or managed through the Admin Center.  

### Create access policy visibility of third-party skills using PowerShell 

You can create an access control policy with the following options:  

- Enable third-party skill visibility (Default): When visibility is enabled, third-party skills are shared across Microsoft 365. Note: These skills are only shared if parent control (if Skills Profile visibility) is also enabled/or shared. Users have the option to turn it off for themselves in their settings. 

- Turn off the default for third-party skill sharing : Users in this access policy will be "opted-out,” and their third-party skills won't be shared across Microsoft 365. Users have the option to turn it on for themselves in their skill settings. 

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowOrgAddedSkills -Name SoftDisable -IsFeatureEnabled $true -IsUserControlEnabled $true -IsUserOptedInByDefault $false 
   ```

- Completely third-party skill sharing: Third-party skills aren't shared with Microsoft 365 experience in your tenant and users can't opt in to sharing their third-party skills. 

   To create this policy, run the following PowerShell command:

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId PeopleSkills -FeatureId ShowOrgAddedSkills -Name  HardDisable -IsFeatureEnabled $false 
   ```

For more information on how to create and manage policies, see control access to features in Viva.  

 