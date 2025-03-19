---
title: "All Company now works like other Viva Engage communities"
f1.keywords:
- NOCSH
ms.author: donnabouldin
ms.reviewer: laurene
author: v-rgrace
manager: elizapo
ms.date: 01/14/2025
audience: Admin
ms.topic: faq
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Learn how All Company now works like other communities in Viva Engage."
---

# All Company community configuration

The All Company group uses the Viva Engage community architecture in Native Mode so that you can get all the new community experiences and features as they roll out. With this integration, All Company offers community customization options, like cover photos and naming.

## What are All Company community's capabilities?

Because All Company works like other communities, these features are available to network admins:

- You can edit the name, description, avatar, and cover photo for All Company.
  >[!IMPORTANT]
  > Since you can fully customize it, the default All Company name is set in the network’s locale. When the admin changes the name, the name persists for that network. The name doesn't adjust to the language of the user's locale if it differs from the network.
- Only network admins can execute pinned resources actions such as add, delete, and reposition.
- You can [restrict posts to All Company](https://support.office.com/article/3219d2ae-db15-4c9f-9dd2-28559ae39a97) to control the types of conversations that take place in the All Company feed. When you enable this setting, only admins can post in All Company. Employees can reply to a conversation starter or react to it.
- Previous All Company Resources appear in Pinned resources.
- You can search for All Company communities by name (even if the community was renamed).
- Community insights are reserved for the All Company community.
  >[!NOTE]
  >If you need access to previous insights for All Company, access them through the following URL: https://engage.cloud.microsoft/domain-name/#/groups/company/insights. Substitute your organization’s domain name in the address.
- You can promote other users from the Viva Engage experience as admins of All Company. 
- All Company is sorted like all other communities. Users can favorite the All Company community to move it to the top of their communities list. 

Network admins can't use the following settings:

- Related communities
- Post to this community by email
- Deletion of All Company from the Viva Engage UI
- Changes to All Company privacy and data classification through Viva Engage settings

### Is my All Company community Microsoft 365-connected, and what does being connected mean?

Viva Engage networks can have communities that are all connected, all unconnected, or a mix of connected and unconnected.

A connected All Company community always has a Microsoft 365 Group ("Group") associated with it. In Native Mode, All Company is always a connected community.

### What is the benefit of All Company backed by a Microsoft 365 Group?

The key differences between an All Company group connected to a Microsoft 365 Group and an unconnected All Company group are:

- A connected All Company community can create a Group.
- A connected All Company can host Live Events.
- A connected All Company has [Microsoft 365 Resources](./viva-engage-and-office-365-groups.md).

The process for confirming that All Company is connected is the same as any other community.

In the **Network Admins** settings, selecting **Enforce Office 365 Identity** associates your network with an All Company community that connects to a Microsoft 365 Group.

If the **Enforce Office 365 Identity** option isn't selected, All Company doesn't connect to a Group.

### If the All Company community is connected, what should I be aware of?

- You can delete All Company in Microsoft Entra ID, which takes it through a soft-delete and then a hard-delete process.
- The All Company community uses the Office 365 Expiration policy when it connects to the Microsoft 365 group.
- You can change the Privacy and Data Classification for All Company in Microsoft Entra ID. **If you set privacy to Private for All Company, users can't post or view the All Company group.**

### How do these changes to All Company affect my existing SharePoint web part and embed scenarios? 

If you use All Company in a SharePoint web part or embed scenario, your All Company feed is empty. To see your All Company feed, add the All Company community.  

For more information about the various SharePoint web parts and embed features, see Related articles.

## Related articles

[Viva Engage and Microsoft 365 Groups](viva-engage-and-office-365-groups.md)

[Use a Viva Engage web part in SharePoint](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da)
