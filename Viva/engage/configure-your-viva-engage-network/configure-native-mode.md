---
title: "Native Mode for Microsoft 365 requirements for a Viva Engage network"
description: "Learn how to prepare your Viva Engage network for Native Mode for Microsoft 365."
f1.keywords:
- NOCSH
ms.reviewer: auhosford
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/10/2025
audience: Admin
ms.topic: install-set-up-deploy
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
---

# Setup requirements for Viva Engage in Native Mode for Microsoft 365

## Requirements 

Native Mode has the following requirements:

- There can only be one Viva Engage network on the tenant.

- All domains on the tenant are associated with the Viva Engage network, and there are no domains on the Viva Engage network that aren't on the tenant.

- All Viva Engage files must be [stored in SharePoint](https://go.microsoft.com/fwlink/?linkid=2111253).

- Retention mode in Viva Engage is set to Archive.

- All users must be in Microsoft Entra ID. Microsoft Entra ID enforces Microsoft 365 identity. You also need to delete any users who aren't mapped to the network.

- There can't be any unlisted private groups.

- All existing groups must be Microsoft 365 connected.

- External groups aren't supported.

- There can't be any network-level or thread-level guests.

> [!NOTE]
> Microsoft recommends Viva Engage Native Mode for security, compliance, and Microsoft 365 integration. See [Viva Engage Native Mode: Step-by-step guide](../native-mode-guide.md) for details about how to transition external groups and users to Viva Engage Native Mode.

## How does the Native Mode Alignment tool work with your network?

The Native Mode Alignment Tool prepares your network for Native Mode by disabling some features and mitigating previously created instances of those features. Those changes include:

- Any unlisted private groups in your network change to private listed groups. Users can't create unlisted private groups.

- External groups in Viva Engage aren't supported. All external groups are made internal only, and guests in those groups no longer have access to the group and its contents. Support for B2B-based external groups is expected at a later date.

- The Native Mode Alignment Tool adds the Microsoft 365 Global administrator to unconnected groups that have no owner, or where the owner has no permissions to create Microsoft 365 groups. It doesn't add them to unconnected groups if the owner has group creation rights.

The Alignment Tool also performs the following tasks:

- It connects all unconnected Viva Engage groups after applying the changes mentioned in the previous three bulleted items.

- It blocks file uploads in Viva Engage Private messages, and deletes all previously uploaded files in Viva Engage Private messages.

- It deletes all internal users (and their associated files and Private messages) in the network who aren't mapped to a Microsoft 365 identity in Microsoft Entra ID.

- It disables support for guests in the network, and removes existing guests from the network. It also removes their associated Private messages and files.

- It disables support for adding guests to an individual thread. Guests who were previously added to individual threads lose their access.

- It deletes all group messages and files for previously deleted groups. It also deletes group messages consistent with your network's retention policy.

- It locks your Viva Engage network into Native Mode.

- It imports your data into the Security & Microsoft Purview compliance portal to support eDiscovery.

>[!CAUTION]
> Once you start alignment through the Tool, the change is **irreversible**.
> Notify users about the preceding changes *before* you run the Alignment Tool to make sure they're prepared.

While the tool is running, unconnected groups don't receive Group updates.

## Related articles

[Overview of Native Mode](../overview-native-mode.md)

[Viva Engage files in Native Mode for Microsoft 365](files-in-native-mode.md)

[Troubleshoot problems with Native Mode for Microsoft 365](../troubleshoot-native-mode.md)
