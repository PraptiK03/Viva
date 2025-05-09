---
title: Communicate with Viva Glint users based on time zone
description: Microsoft Viva Glint offers the ability to send survey invites, reminders, and other notifications in users’ preferred time zones. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: optional system attributes, time zones, time zone delivery
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/08/2025
---

# Communicate with Viva Glint users based on time zone

Microsoft Viva Glint offers the ability to send survey invites, reminders, and other notifications in users’ preferred time zones. 

> [!NOTE]
> This feature sends emails on a time-zone-based schedule but doesn’t include activation/deactivation of each user’s survey by time zone.

## Set up a time zone attribute

To ensure employees receive survey communications in their unique time zones, your time zone attribute must be appropriately [configured as an optional system attribute](send-employee-attributes.md#optional-system-attributes). Once configured, include this time zone attribute in your employee data to trigger survey emails in employees' time zones.
 
Use [Viva Glint supported time zones](supported-time-zones.md) to find valid time zone values. Before a survey launches, ensure that all employees have a valid value attached to their records.

> [!NOTE]
> When a user has a blank or invalid time zone value in employee data, notifications send in the default time zone selected in General Settings.

## Manage time zone options in General Settings

As a Viva Glint admin, select a default time zone and enable sending in users’ time zones in General Settings.

### Set a default time zone

Set the default time zone in the **Company Information** section of **General Settings**, found on the admin dashboard from the configuration page, in the **Service Configuration** section. Use the dropdown menu to find your organization’s default time zone and then select **Save Changes**.

> [!NOTE]
> Employee Lifecycle survey invitations are triggered by events. These events send platform notifications at your Viva Glint default time zone.

## Enable notification in user time zone

Set notifications to **send in users’ time zones** in the **Communication section** of **General Settings**, found on the admin dashboard from the configuration page, in the **Service Configuration** section. Toggle to **YES** to activate and then select **Save Changes**.

This setting applies to all survey and results notification emails and can’t be disabled or enabled at the survey program level. When enabled, a 24-hour buffer is added to survey start and end times in the default time zone to allow for users to access and submit surveys across the globe.

> [!IMPORTANT]
> If this feature is enabled or disabled during a live survey, the update won't apply to emails and reminders that are already scheduled, and it won't affect the activation date/deactivation dates on existing surveys.

### Example
> Contoso, with a default time zone/headquarters in New York, wants to ensure that their Sydney, Australia employees receive and access their surveys at the same time in their day as the rest of their employee population. For survey invites to send to Sydney employees at 9:00 AM on March 28 in Australia/Sydney time, the survey needs to be active no later than 12:00 AM, March 27, New York time because New York is 14 hours behind Sydney.

> Enabling sending in user time zone allows for invites to send to users at the appropriate time and adds a 24-hour cushion before launch and after survey close in Contoso's default time zone.

> | Event in default time zone: |Survey activation|Survey launch|Survey close|Survey deactivation|
> |:----------------  |:----------------|:------------|:-----------|-------------------|
> | **Activity:** |Surveys generate/activate|Invites send|Survey ends |Surveys inactivated|
> | **Time:** |March 27, 12:00 AM|March 28, 9:00 AM|April 11, 12:00 AM|April 12, 12:00 AM|

> [!NOTE]
> Users in any time zone can access a survey before receiving an email invite after the Survey Activation time if they have access to My Surveys in Viva Glint or attribute-based survey access. Any results submitted appear in the dashboard at 12:00 AM on the survey launch day.
