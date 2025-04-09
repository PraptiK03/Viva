---
title: "Manage Viva Engage with Microsoft Intune"
f1.keywords:
- NOCSH
ms.reviewer: jobacus
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 03/01/2025
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
ms.collection: essentials-security
search.appverid:
- MET150
- MOE150
- MED150
ms.assetid: 76f5c4c9-6a4e-43d1-87dc-2848a90686be
description: "Subscribe to Microsoft Intune to add mobile application management to Viva Engage"
---

# Manage Viva Engage on mobile devices with Microsoft Intune

When you subscribe to [Microsoft Intune](https://www.microsoft.com/en-us/security/business/endpoint-management/microsoft-intune?rtc=1), you can use mobile application management (MAM) with Viva Engage along with other apps. Through MAM, you can manage and protect app data on devices even when they're not enrolled in mobile device management (MDM).
  
## Manage Viva Engage with MAM

Microsoft Intune provides mobile application management (MAM) capabilities for Viva Engage, Outlook, and other Microsoft mobile apps for iOS and Android.
  
MAM helps you manage bring-your-own-devices (BYOD) users, and apps for work and personal use, for devices that aren't enrolled in MDM. When you use Intune with Viva Engage, you can set up policies covering Viva Engage instances on Android and iOS devices to help protect your corporate data. The following table describes Intune policies for mobile clients:
  
| Intune policy you can enforce on the app | Available for Android? | Available for iOS? |
|:-----|:-----|:-----|
|Allow apps to transfer data to other apps  |Yes  |Yes  |
|Allow apps to receive data from other apps  |Yes  |Yes  |
|Prevent "Save As"  |Yes  |Yes  |
|Prevent iTunes and iCloud backups  | -- |Yes  |
|Prevent Android backups  |Yes  | -- |
|Restrict cut, copy, and paste with other apps  |Yes  |Yes  |
|Restrict web content to display in the Intune Managed Browser  |Yes  |Yes  |
|Encrypt app data  |Yes  |Yes  |
|Disable contacts sync  |Yes  |Yes  |
|Require PIN for access, and set specific requirements such as PIN length and number of allowed tries  |Yes  |Yes  |
|Allow use of fingerprint instead of PIN  |Yes  |Yes  |
|Require corporate credentials for access  |Yes  |Yes  |
|Block managed apps from running on jailbroken or rooted devices  |Yes  |Yes  |
|The frequency of how often the access requirements are checked  |Yes  |Yes  |
|Block screen capture and Android Assistant  |Yes  | -- |
|When you retire or unenroll a device with the Viva Engage app, the application's corporate data is deleted  |Yes  |Yes  |

> [!IMPORTANT]
> Intune enforces MAM policies when users authenticate to Viva Engage through Microsoft Entra ID accounts. They're not enforced when users authenticate to Viva Engage with Viva Engage-specific passwords or Viva Engage temporary passwords.
