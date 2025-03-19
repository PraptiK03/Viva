---
title: "Non-Native Mode and hybrid Viva Engage networks upgrades"
description: Details on non-native and hybrid Viva Engage networks.
f1.keywords:
- NOCSH
ms.reviewer: auhosford
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/10/2025
audience: Admin
ms.topic: upgrade-and-migration-article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MET150
- YAE150
---

# Non-Native Mode and hybrid Viva Engage Network upgrades

Non-Native Mode and hybrid Viva Engage Networks must upgrade to [Native Mode](../overview-native-mode.md) to allow users, groups, and content to map to their counterparts in Microsoft Entra ID and Microsoft 365. Native Mode also provides other benefits, such as the ability to host live events in every Viva Engage community and simplify file administration through SharePoint. Native Mode also supports eDiscovery through the Microsoft Purview compliance portal, so your organization can collaborate safely and securely within your Viva Engage network.

## When does this change happen?

Conversion to Native Mode is complete for all Viva Engage networks, with rare exceptions. You can initiate the upgrade process on your own by visiting the Microsoft 365 Native Mode page within the Network Admin pages of Viva Engage.

## How does this change affect your organization?

After conversion to Native Mode, you can no longer access these features:
-	Network-level guests 
-	Email blocked lists
-	Secret groups

If your organization has active guests, you can use Microsoft Entra B2B guest functionality for guests who reside in the same geographic area as the Viva Engage network, such as US guests for US networks, and EU guests for EU networks. After Native Mode conversion of your network, guests must be reinvited.

If your organization currently uses an email blocked list to control access to your Viva Engage network, you can continue to do so from Microsoft Entra ID. For more information, see [Manage Viva Engage licenses in Microsoft 365](../manage-engage-licenses-microsoft-365.md).

These features are only available to networks in Native Mode. Microsoft 365 doesn't support a secret groups feature. All groups must be public or private.

 As part of the migration process, the Viva Engage administrator account is added to all groups in the network. Files also are sometimes renamed.

 ## What do you need to do to prepare?

 **If you would like to self-initiate your migration:**

 See the [step-by-step guide](../native-mode-guide.md) to Native Mode migration. You can run an alignment report that identifies gaps in your current network alignment with Native Mode. Because the migration process deletes some data, ensure that you back up your network’s data and communicate the migration to your users before running the Native Mode Alignment Tool.

 **If you would like Microsoft to initiate your migration:**

 No action is required from you. You can run an alignment report to identify gaps in your current network alignment with Native Mode. **We recommend that you back up your data and communicate the migration to your users before your scheduled migration start date.** If your alignment report reveals any blockers to migration, you can log an exception with support.

 **When you need to postpone or schedule your migration around blackout dates:**

 Contact support to log an exception.
