---
ms.date: 1/03/2025
title: "Automatic Native Mode migration and network consolidation"
description: "Frequently asked questions about Native Mode for Viva Engage"
ms.reviewer: auhosford
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Automatic Native Mode migration and network consolidation

Non-native and hybrid Viva Engage networks receive automatic upgrades to Native Mode. Native mode operation allows users, groups, and content to map to their counterparts in Microsoft Entra ID and Microsoft 365. Native Mode also enables networks to host Live Events in every Viva Engage community, and simplify file administration through SharePoint. 

Native Mode also supports eDiscovery through the Microsoft Purview compliance portal, which allows your organization to collaborate safely and securely in your Viva Engage network.

## Frequently asked questions

### How does automatic migration work?

Unlike manual migration, automatic migration requires little advance preparation. It uses the following timeline:

**10 days before migration starts:** You receive a Microsoft 365 Message Center post to notify you that your network is chosen for automatic migration.

**Day of migration start:** You receive a Microsoft 365 Message Center post to notify you that migration has started.

**During migration:** In most cases, migration takes between 1 and 30 days to complete.

**Once migration is complete:** You receive a Microsoft 365 Message Center post notifying you that the migration is complete. You have 90 days to perform a post-migration audit and to export data that isn't supported in Native Mode.

### I don’t want to be automatically migrated. What can I do?

Native mode is fundamental to the integration of Viva Engage within Microsoft 365 and all networks are being upgraded. Previously, admins had to initiate the migration, but an improved automatic migration performs the task.  

If you wish to control the migration, it may still be possible. Start the migration immediately by following the [step-by-step guide](/Viva/engage/native-mode-guide).  

### I received a Microsoft 365 Message Center post that says I’m selected for automatic migration. When does it start and end?

Your migration begins 10 days after the date of the first Message Center post. You receive another Message Center post when your migration begins. No admin action is needed to complete the migration. Information about the migration is provided when it completes.

Migration time depends on the volume of files which need to be migrated from legacy Viva Engage file storage to SharePoint storage. It isn't possible to provide an estimate ahead of time due to the number of factors involved.

### I was planning to migrate manually, but the alignment report button is grayed out. How do I export the alignment report?

The alignment report is part of the manual alignment process. Automatic migrations don't produce an alignment report. Doing so avoids inconsistencies between the report and the state of objects in the network during the migration.

### I want to manually migrate on my own schedule. Is it still possible to receive exemptions?

Exemptions were temporarily available to help customers plan their migrations in the early stages of the automated migration rollout. Now that the automated process is rolling out to all customers and the manual process isn't supported, it's no longer possible to offer exemptions.  

### What information will be provided after the migration?

To ensure completeness of post-migration data, all content from your previous network remains available for 90 days to allow administrator data audits. Administrators can get various reports on the migration, which cover deleted unmapped users, deleted files, deleted messages, copied files, and guests.

### What is the impact to end users during the migration?

Community guests need to be reinvited after migration completes, but most end users aren't impacted during migration. Microsoft Entra B2B replaces the legacy Viva Engage external communities feature when a network is in native mode. See [Work with Microsoft Entra B2B guests in Viva Engage communities](/viva/engage/get-started-with-viva-engage/azure-ad-b2b-guests-viva-engage).

### The migration page says the migration is still in process, but we received a Message Center post stating the migration was complete. What is happening?

The Native Mode migration page states that the migration is in process until the end of the 90-day data retention period.

### I have more than one network associated with my Microsoft 365 tenant. Will you automatically migrate all of those networks into native mode?

No. Networks are automatically consolidated. You'll receive a Message Center post indicating which network will remain after consolidation. The remaining network will then be migrated to Native Mode. The best way to ensure appropriate network consolidation is to perform it on your own. For more information, see [Consolidate multiple Viva Engage networks](/Viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).
