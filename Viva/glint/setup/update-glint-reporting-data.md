---
title: How to update reporting data in closed Viva Glint surveys
description: Microsoft Viva Glint Advanced Configuration Uploads and Data Apps allow you to perform complex data updates. Use this guidance to determine which retroactive update option best meets your needs.
ms.author: aweixelman
author: AliciaWeixelman
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: advanced configuration, uploads, retroactive update
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/05/2025
---

# How to update reporting data in closed Viva Glint surveys

Microsoft Viva Glint Advanced Configuration Uploads and Data Apps allow you to perform retroactive updates to survey data. Use this guidance to determine which retroactive update option best meets your needs.

> [!CAUTION]
> - Don't perform a retroactive update while a Viva Glint survey is live.
> - Deleted user data can't be retroactively updated.

## Attributes that don't require retroactive updates

Some attributes in Viva Glint always reference the most current information and don't require retroactive updates. These attributes include:

- First Name
- Last Name
- Email Address
- Employee ID
- Time Zone
- Survey Language
- Dashboard Language
- Personal Email

## Factor in Survey Program type

Recurring and Ad Hoc survey programs represent a point in time for all respondents, and updates for multiple users for one time period can be applied in bulk with retroactive update options. Employee Lifecycle and Always-On survey programs, however, are ongoing. Surveys generate for individual users at many points throughout the lifetime of these surveys, making it difficult to pinpoint users' data in the past and apply updates, especially for Manager Hierarchy data.

### Employee Lifecycle and Always-On surveys

Ongoing survey types like Lifecycle and Always-On can have the same user respond multiple times in a survey cycle that may need a retroactive update. Viva Glint retroactive updates don't currently support attribute value updates to multiple records for the same user during a retroactive update. An admin can remove users who have multiple records when preparing a file of corrected user data.

If duplicated users aren't removed, admins see a:

- "Failed to run the data app RETROACTIVE_PULSE_UPDATE" error message when using the RETROACTIVE_PULSE_UPDATE Data App.
- "FAILED" State for the Retroactive User Updates upload, with the following File error in the Upload Job Details:
  - System error: Failed to find user_staging_record with externalUserId=[user@contoso.com], which is not supposed to happen at all because User object with the same ID was previously loaded."

## Data update options

There are two options to update reporting data for closed survey cycles in Viva Glint. For updates to nonmanager hierarchy information, use the Advanced Configuration > Uploads > Retroactive User Updates option. For manager hierarchy updates, use the Advanced Configuration > Data Apps > RETROACTIVE_PULSE_UPDATE option. See the following descriptions of each option and select "Learn more" to see how to complete each update.

### Uploads: Retroactive User Updates

To retain current employee information, upload a file of all or some users in your closed survey to apply new values to past versions of data. This option is the simplest and can be used for most retroactive updates, including nonmanagerial reporting hierarchy updates. [Learn more](advanced-config-uploads.md#to-perform-a-retroactive-user-updates-upload).

> [!IMPORTANT]
> To retroactively update a Manager Hierarchy, always use the RETROACTIVE_PULSE_UPDATE Data App and not the Retroactive USERS_UPLOAD option. [Learn more](glint-data-apps.md).

### Data Apps: RETROACTIVE_PULSE_UPDATE

Update Manager Hierarchy information for closed surveys by uploading corrected users to Viva Glint, running the RETROACTIVE_PULSE_UPDATE Data App, and reverting user data to current information after the update. [Learn more](glint-data-apps.md#to-perform-a-retroactive-update-to-manager-hierarchy).
