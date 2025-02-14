---
title: "Viva Engage file storage overview"
description: "Where files are stored in Viva Engage depends on whether the network uses Microsoft 365 connected groups."
f1.keywords:
- NOCSH
ms.reviewer: rociov
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 02/10/2025
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
---

# Viva Engage file storage overview

Files attached to posts in Viva Engage networks connected to Microsoft 365 are stored in SharePoint. Files in community posts are stored in the document library that backs up the community. Storyline posts are stored in a hidden library in the creator's OneDrive.

**Exception**: When the Viva Engage network doesn't connect to Microsoft 365 groups, files uploaded to posts are stored directly in Viva Engage cloud storage. It includes files from the following entities:  

- Multiple Viva Engage networks owned by a single Microsoft 365 tenant.
- Viva Engage networks that don't enforce Office 365 identity.
- Viva Engage basic networks.

Learn more about file storage in communities that connect to Microsoft 365 groups:

- Learn about [File Storage for storyline posts](../eac-storyline.md#file-storage-for-storyline).
- Learn about [Viva Engage and Microsoft 365 groups](../engage-microsoft-365-groups.md).
- Learn how to [Enable or Disable the Community Resources Module and Files Tab](https://support.microsoft.com/en-gb/topic/manage-viva-engage-community-resources-08fc99bf-c36c-425b-9a98-079e62510135).

> [!NOTE]
> Policies in SharePoint's document libraries take precedence over settings for files, images, and videos in Viva Engage.

## Benefits of Sharepoint Storage

For network and tenant administrators, SharePoint has a rich set of security and compliance features that apply to uploaded files in Viva Engage, for Microsoft 365-connected Viva Engage groups. Features include eDiscovery, data loss protection, and in-geo residence for files at rest.

End users work with the familiar SharePoint user interface for file navigation and management, with the following capabilities:

- Use Microsoft Search for greater discoverability and easier access.
- Browse or search features in SharePoint and Delve to find and access files through Viva Engage, SharePoint, and other Microsoft 365 resources.
- Enable offline access to files by syncing a SharePoint folders to a folder on their computer.

<!-- Links in the short bulleted list to be hidden but keep for possible future use per request-->
<!--
For information about using Viva Engage files stored in SharePoint, see the following articles:

- [Where are my Viva Engage files stored?](https://support.microsoft.com/office/how-do-i-tell-where-my-viva-engage-files-are-being-stored-fadfdefa-e00d-40b6-94cb-a9ddb171a443)

- [Edit a previously uploaded file when your Viva Engage connected group now stores files in SharePoint](https://support.microsoft.com/office/edit-a-previously-uploaded-file-when-your-viva-engage-connected-group-now-stores-files-in-sharepoint-4b2cfde2-871e-4f0d-9936-db5a57ef5f87) 
-->

## Storage locations of community and storyline files

**Community**
Files uploaded to community posts are stored in the SharePoint document library that backs up the community. You can access the library from two places: 

- **Files tab**: When the community admin enables the **Files** tab, you can access the document library by selecting it. 
- **Community resources**: When the community admin enables the Community resources widget, you can access the document library from the path **SharePoint library > Apps > Viva Engage**.  

> [!NOTE]
> For communities residing in Yammer before it became Viva Engage, folders that store attachments to community posts are labeled **Yammer** instead of **Viva Engage**.

**Storyline**
Files uploaded to storyline posts are stored in a hidden library in the storyline's owner OneDrive. The Microsoft 365 user experience doesn't provide an entry point to this location, but you can access it through a URL resembling the following example:  

`https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage/Attachments/Storyline` 

To determine the precise URL for a user's storyline page, follow these steps: 

1. Open the user's OneDrive in a browser and note its URL. 

2. Locate the user identifier, which is the part of the URL immediately that follows `my.sharepoint.com/personal/`.

3. Replace everything after the profile identifier and the backslash plus VivaEngage, without a space, case insensitive. The resulting URL resembles this example:

    `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage` 

4. Press **Enter**. The library appears.

[See this page to find out how to enable and disable the Community Resources Module and Files Tab](https://support.microsoft.com/en-gb/topic/manage-viva-engage-community-resources-08fc99bf-c36c-425b-9a98-079e62510135).

> [!Important]
> **Avoid using SharePoint to modify, replace, delete, move, or rename** the folder structure (**Documents > Apps > Viva Engage**), documents, and rich media for your Viva Engage network. Changing these elements in SharePoint will break the front-end experience of posts, in communities, and in your storyline.

## Troubleshoot attachment issues 

### 1. Restore a Microsoft 365 group or document library that backs a connected community

Community posts can lose attached files and rich media when the Microsoft 365 group that backs up a connected community is deleted, when the group's SharePoint library is deleted, or if the folder structure (**Documents > Apps > Viva Engage**) is deleted or moved from their location. 

To restore a deleted group, contact your administrator, Help desk, IT or technical support department. For more information, see [Restore a deleted Microsoft 365 group](/microsoft-365/admin/create-groups/restore-deleted-group?view=o365-worldwide&preserve-view=true). 

To restore a document library, follow the instructions in [Restore items in the recycle bin that were deleted from SharePoint or Teams](https://support.microsoft.com/office/restore-items-in-the-recycle-bin-that-were-deleted-from-sharepoint-or-teams-6df466b6-55f2-4898-8d6e-c0dff851a0be).

### 2. Delete attached files that belong to deleted community or storyline posts 

If a file or rich media gets removed from a post, it isn't removed from SharePoint or OneDrive. They remain shared and accessible to anyone with access to that community or storyline.  

To fully delete the file, ensure the attachment is removed from the post or from the reply. If the post or reply is already published, the author or a community admin can select the overflow menu (...) and then choose **Edit**. You can also delete the entire post or reply. Then, perform one of the following deletion tasks in SharePoint: 

#### 2.1 Delete files removed from a post or a reply in a community

1. Open the SharePoint library backing the community. You can do this one of two ways, depending on your environment:
    - Select the **Files** tab on the community;
    - Select **SharePoint Library** from the **Community resources** module in the community's right navigation. 
2. Open the **Documents > Apps > Viva Engage** folder. 
3. Locate the file previously attached to the post and select **Delete**. 

#### 2.2 Permanently delete files removed from a post or a reply on a storyline 

Files attached to storyline posts are stored in a hidden library in the author's OneDrive. There's no entry point to this location in the Microsoft 365 user experience, but you can access it through a URL resembling the following example:

1. Open the user's OneDrive in a browser. 

2. Note the URL to the user's OneDrive. 

3. Locate the user identifier, which is the part of the URL immediately that follows `my.sharepoint.com/personal/`.

4. Replace everything after the profile identifier and the backslash plus VivaEngage, without a space, case insensitive. The resulting URL resembles this example:

    `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage` 

5. Press **Enter**. The library appears.

6. Open the **Attachments > Storyline** folder. The URL to the folder where storyline files are saved resembles this example:

    `https://<tenantname>-my.sharepoint.com/personal/<user identifier>/VivaEngage/Attachments/Storyline`

7. Locate the previously attached file and select **Delete**.

    Files that users upload in Microsoft 365 connected groups are saved in the **Apps > Viva Engage** subfolder of the SharePoint document library for the group. Users can access the SharePoint document library from Viva Engage under **Microsoft 365 Resources** or **Office 365 Resources** on the right side of a Viva Engage group, or through SharePoint itself. The Viva Engage group must be Microsoft 365 connected.

 > [!NOTE]
 > Avoid deleting, moving, or renaming files in the **Apps > Viva Engage** subfolder.

### 3. Resolve images that appear blank in Viva Engage conversation threads

Files attached to community posts are stored in the SharePoint document library that backs up the community. Files are stored in the path **Documents > Apps > Viva Engage**.  

If the library location changes, files and images attached to community posts could appear blank. To solve this issue, take the following steps: 

1. Move the contents of the duplicated folders into the official **Apps/Viva Engage** folder.

2. Once they're empty, delete all duplicated folders.

3. Ensure the permissions on the official **Apps/Viva Engage** folder are the default ones. 

To find the document library that backs up the community, use the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) API `https://graph.microsoft.com/v1.0/groups/{office_365_group_id}/drive/special/approot/` and change the `office_365_group_id` attribute in the API call to the community ID. The following example illustrates:

`https://graph.microsoft.com/v1.0/groups/contoso_program_managers_group/drive/special/approot/`

- Learn [How do I find a community's group feed ID in Viva Engage](https://support.microsoft.com/office/how-do-i-find-a-community-s-group-feed-id-in-viva-engage-9372ab6f-bcc2-4283-bb6a-abf42dec970f#:~:text=To%20find%20the%20group%20ID%20for%20a%20Viva,an%20online%20tool%20to%20decode%20base%2064.%20).

- Learn [How Yammer evolved to Viva Engage](https://techcommunity.microsoft.com/blog/viva_engage_blog/yammer-is-evolving-to-viva-engage/3738825).

> [!Important]
> In legacy communities created before March 2023, the SharePoint document libraries are named **Yammer** instead of **Viva Engage**.

### 4. Prevent deletion of files from Viva Engage communities

Engage community members can access the SharePoint library, and open or delete chosen folders and files. The permissions that enable file access are by design but can risk accidental or unintentional deletion. This section describes how to prevent this issue by removing navigation to the library from Engage communities.  

Viva Engage stores communities' attachments to posts in the community's SharePoint document library. It stores files in a subfolder named `Apps\Yammer` or `Apps\Viva Engage`. Members can open the community library in the Files tab, or select **Community resources > SharePoint library** on the Viva Engage right pane. From there, members can delete folders or files. 

Community admins can remove the navigation entry points to the library. Take the following steps to remove the **Files** tab and the **Community resources** link:

1. Select the **...** option in the bottom-right corner of the community header. 

2. Select **Settings** and turn off the **Community resources** toggle.

3. Turn off the **Enable Files tab** toggle.

## Guest access to files

The following table shows how different guests can access uploaded files in Viva Engage and SharePoint-stored files.

| Type of user | Access to group files in Viva Engage | Access to group files in SharePoint |
|----------|----------|----------|
|**Conversation-level guest that is in your network**|**Private group**: Can view files shared in the conversation, but can't upload files.<br/>**Public group**: Can view, edit, and upload files.|Conversation level guests can't access any files saved in SharePoint nor upload any files. If you want to enable access to specific files in the conversation, add them as an Azure B2B guest on the Office 365 tenant. File upload isn't permitted.|
|**Network-level guest that is also an Azure B2B guest, and a member of the group in Microsoft 365**|Can view, edit, and upload files.|These Azure B2B guests can view, upload, or edit files from the SharePoint Document library only. File access from Viva Engage isn't permitted.|
|**Azure B2B guest, but not a member of the group<br/>Network-level guest<br/>Conversation-level guest that isn't in your network**|Automatic file access isn't allowed. These users can request access to specific files.<br/>Can't upload files.|Automatic file access isn't permitted. Guests can request access to specific files. File upload isn't permitted.|
|**Network-level guest, but not Azure B2B guest**|Automatic file access isn't allowed. A guest must become an Azure B2B guest and a member of the group in Microsoft 365. Alternatively, other group members can grant access to specific files or the entire document library through one of many SharePoint external sharing methods.|No automatic access for network level guests to Viva Engage files saved in SharePoint. If you want to enable access to specific files, add them as an Azure B2B guest on the Office 365 tenant. For more information, see [Microsoft Entra B2B documentation](/azure/active-directory/b2b/). If guests need to upload files to a specific group from SharePoint or have automatic access to files uploaded to SharePoint, add them as a group member in SharePoint.|

> [!NOTE]
> Guest memberships are separate for Microsoft Entra ID and Viva Engage. Deleting a network-level guest from a Microsoft 365 connected Viva Engage group, or from the tenant in Microsoft Entra ID, doesn't remove the user in Viva Engage. Deleting a user from Viva Engage doesn't delete the user from a Microsoft 365 group or from Microsoft Entra ID.

For more information about Microsoft Entra B2B guests, see [Guest access in a Microsoft Entra B2B](/azure/active-directory/b2b/what-is-b2b).

## Requirements

- Viva Engage version requirements

    Ensure your users are using the most recent Viva Engage versions. At a minimum, users should be using the following or newer versions:

    - Viva Engage on iOS - 7.33.0  

    - Viva Engage on Android - 5.5.84

    - Viva Engage desktop on Windows or Mac - 3.4.2

- Cookie and browser requirements

    To store Viva Engage files in SharePoint, we use the Microsoft Authentication Library (MSAL) library with Microsoft Entra ID tokens for authentication. If you don't enable third-party cookies in your browser, or if security zone settings are incorrect, refresh processing for Microsoft Entra tokens can't send necessary information to Microsoft Entra ID.

    When a token refresh call fails, users see:

    - On the Viva Engage page for a connected group, Microsoft 365 Resources are dimmed

    - File operations fail

    - Viva Engage live events can't be created.

     For more information, see [A silent sign-in request was sent but no user is signed in](https://github.com/AzureAD/azure-activedirectory-library-for-js/wiki/FAQs#q6-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in).

    To avoid problems, take the following steps:

    - Ensure that no extensions (such as Ghostery) block or prevent reading of cookies.

    - In Microsoft Edge, ensure protected mode is disabled for the trusted zone.

        Include **engage.cloud.microsoft** and related URLs as a part of trusted zone. For more information, see [Microsoft 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges)

    - In complex environments, especially those using wildcard configurations such as *.fabrikam.com, more effort may be required to find the right configuration. URLs may need to be moved between zones, or replaced with the absolute versions in some cases.

    - Users shouldn’t access Viva Engage using incognito or InPrivate mode or equivalent modes in other browsers.
