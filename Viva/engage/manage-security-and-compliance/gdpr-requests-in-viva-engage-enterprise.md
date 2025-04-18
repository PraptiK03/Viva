---
title: "Manage GDPR data subject requests in Viva Engage Enterprise"
f1.keywords:
- NOCSH
ms.author: dmillerdyson
ms.reviewer: jobacus
author: v-rgrace
manager: elizapo
ms.date: 04/02/2025
audience: Admin
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection: essentials-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: eae49f12-4661-4ba5-aa72-01248f0709bf
description: "Erase all information about a Viva Engage user to comply with GDPR data subject requests."
---

# Manage GDPR data subject requests in Viva Engage Enterprise

As a verified admin, you can erase a user from Viva Engage to comply with a [General Data Protection Regulation (GDPR) data subject request](/compliance/regulatory/gdpr-dsr-Office365). When you erase a user, the action removes their personally identifying information, but their messages and files remain. You can review a user's messages and files to decide which ones to delete. An ID ties to remaining content, but not with the user's name.

Choose the approach that applies for your case, and **follow the steps in the order listed**. The order matters: after you erase a user, you can't find their data to delete it.

| Approach | Steps |
| :----- | :----- |
|Keep all messages and files created by the user| Select **Erase the user** to remove the user from the home tenant and from any external tenants. The Erase action doesn't delete messages or files. |
|Delete all messages created by the user and decide which files to delete| 1. Do one per-user export of the user's data for the home tenant, and one for each of their external tenants.<br>2. To remove the user from each tenant, select **Permanently remove this user, and remove their messages**.<br>3. In the home tenant, use the **Erase the user** option.<br>4. Within 14 days, remove any files stored in Viva Engage in the home tenant. Delete any information that the per user export doesn't include. |
|Review files and messages created by the user and decide which to keep and which to delete|1. Do one per-user export of the user's data for the home tenant, and one for each external tenant if any. <br>2. In the home tenant, use the **Erase this user** option. <br>3. Within 14 days, remove any files or messages as necessary from the home tenant, and any information missing from the per user export.*|

> [!NOTE]
> If you prefer to have more than 14 days to review and delete files and messages, you can do so before erasing the user.
 
> [!IMPORTANT]
> Closing a Microsoft Entra ID account doesn't delete the user and their information. To delete user information, go to the Viva Engage admin center and complete the following instructions.

<a name="DeleteMessagesFiles"> </a>

## Delete specific messages or files

Use the Viva Engage file ID from the export's **messages.csv** file to go directly to the file in Viva Engage and delete it.

> [!IMPORTANT]
> For Viva Engage files stored in SharePoint, delete the files from Viva Engage in order to remove the Viva Engage metadata and the file.
  
**To locate and delete a specific message:**

1. In the data export's **messages.csv** file, find the URL for the message in the `gdpr_delete_url` column. The URL has this syntax: `https://www.yammer.com/messages/thread_id/hard_delete_confirmation`.
  
2. Copy the `gdpr_delete_url` for the message you want to delete. Paste it into a browser window that's logged in to the network from which you want to delete the message.

3. After verifying that the displayed message is the one to delete, click the link to permanently delete the message from Viva Engage and associated data exports.

**To locate and delete a specific Viva Engage file stored in Viva Engage or SharePoint:**

  1. Use the **Search** box in Viva Engage. For example, for a file named 12345678.pptx in the export, search for 1235678.pptx. In the search results, select **Go to File**, and then select **Delete this File**.

  1. You can also build the URL for the file. Use **https//www.yammer.com**/*network_name*/**#**/**files**/*file_number*, for example `https://www.yammer.com/contosomkt.onmicrosoft.com/#/files/12345678`. On the Viva Engage page for the file, select **Delete this File**.

**To delete the cover images for a user:**

 1. By API: Engage Admins or verified admins can delete cover images for any user in their tenant via an API call. The URL has this syntax: `www.yammer.com/api/public/v1/user-profiles/*user_id*/cover-image`.

      For example, to delete the cover images of a user with ID 1234567890, the URL would look like: `www.yammer.com/api/public/v1/user-profiles/1234567890/cover-image`.

 2. By UI: Engage Admins with premium Viva licenses can upload or delete cover photos for any user who has the premium Viva license and has storyline enabled by:

     1. Visiting the profile page of the user.
     2. Hovering your mouse over the profile header and selecting **"Upload cover photo"**.
     3. Deleting or uploading a new cover image, as needed.

> [!NOTE]
> In cases where the admin or the user aren't premium licensed, or the user no longer has their own storyline, previously uploaded photos need to be deleted via API.

<a name="OtherData"> </a>
<a name="EditProfile"></a>

## Find and delete user data not included in per-user export

Some user data doesn't get included in an export.

To find this data for a user, go to Viva Engage settings :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false"::: \> **People**, and select the name of the user.
  
The following table shows how to change or delete this data when needed.

| Type of data | How to change or delete data |
|:-----|:-----|
|Bookmarked messages, group membership, followed or following users, and followed articles | When you [erase a user from the Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), this information is deleted after the 14-day suspension period.<br><br>Users can change or delete their own information. For steps, see [Change my Viva Engage profile and settings (Web and Desktop)](https://support.microsoft.com/office/change-my-viva-engage-profile-and-settings-web-and-desktop-ab813bce-5312-4688-94ee-70018545cd3c). |
|User settings, including notification, application, and language settings | When you [erase a user from your Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), this information is deleted after the 14-day suspension period. As an admin, you can't change this information for a user.<br><br>Users can change their own settings. For steps, see [Change my Viva Engage profile and settings (Web and Desktop)](https://support.microsoft.com/office/change-my-viva-engage-profile-and-settings-web-and-desktop-ab813bce-5312-4688-94ee-70018545cd3c). |
|User profile | If the user has a Viva Engage identity, there are two options to remove the user: <ul><li>[Erase a user from your Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), Viva Engage deletes this information after the 14-day suspension period.</li><li>[Allow the user to edit their own profile and settings](gdpr-requests-in-viva-engage-enterprise.md#EditProfile).</li></ul> If the user has a Microsoft 365 identity, Viva Engage pulls the user profile from Microsoft 365. That information originates from Microsoft Entra ID. Viva Engage users can temporarily change their profiles in Viva Engage. If a change occurs in the Microsoft Entra ID, *their changes are overwritten*. **To permanently change or delete a user's profile, you must change or delete directory data in Microsoft 365 and in Microsoft Entra ID**. See [Manage Viva Engage users across their lifecycle from Microsoft 365](/viva/engage/manage-viva-engage-users/manage-users-across-their-lifecycle) and [Add or change profile information for a user in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal). |

<a name="RemoveGroup"> </a>

## Remove a user from a group including an external group

1. In the group, click on the count in the **Members** module. A panel of community members opens.

2. Select Settings :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false"::: next to the user's name.

3. Select **Remove from community**.

<a name="RemoveThread"> </a>

## Remove a noncommunity participant from a conversation in a private community

- If a noncommunity member is added to a conversation, a reply appears in the conversation to note who was added. The reply contains a link to **Remove** the noncommunity member participant.

<a name="RemoveUser"> </a>

## Erase a user from your Viva Engage home tenant and external tenants

> [!IMPORTANT]
> When you erase a user, a 14-day window opens to decide which files and messages to save or delete in the home tenant. Be sure to export all necessary user data. After the 14 day period elapses, Viva Engage erases all user-identifying data. Delete user messages and files *within 14 days* after selecting **Erase this user**. After the 14-day window, files and messages remain, but are **marked as belonging to a former user**.<br><br>After the user account transitions from Deactivated to Removed, you can't associate user data with that user, which means you can't export and review their data.

Before you erase a user, see [Delete specific messages or Viva Engage files stored in Viva Engage or SharePoint](gdpr-requests-in-viva-engage-enterprise.md#DeleteMessagesFiles). The article describes how to review and delete a user's messages and files in external groups, external threads, and tenants. After you select **Erase this user**, the user isn't associated with those messages and files.

Removing a user from their home Viva Engage tenant removes them from all external tenants. You must separately remove guests from each of their external tenants.
  
When you erase a user, the action deletes the following user data:
  
- Who the person follows, connections to followed conversations and articles, and connections to their followers

- Bookmarks, language preferences, notification settings, and account activity

- The user's profile

- Community memberships

- The list of tenants of which they were a member

As an admin, you can erase a user from their home tenant and from their external tenants.
  
## See also

[Manage Viva Engage data compliance](manage-data-compliance.md)
  
[Export data from the Viva Engage admin center](/viva/engage/eac-as-manage-data)
