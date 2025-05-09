---
title: "Files in Native Mode"
description: "How to prepare your Viva Engage network for Native Mode in Microsoft 365."
f1.keywords:
- NOCSH
ms.reviewer: auhosford
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/10/2025
audience: Admin
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
---

# Viva Engage files in Native Mode for Microsoft 365

All Viva Engage networks must be converted to operate in Native Mode for Microsoft 365. In Native Mode, Sharepoint automatically stores all Viva Engage files for your network. It's easier for users and admins to access and manage files when you have a single location for file storage. While Viva Engage automatically converts legacy group networks to Native Mode, some networks might need to be manually converted. The Native Mode Alignment Tool makes it easy to convert a huge Viva Engage network's complement of files.

The Native Mode Alignment Tool uses the following file handling rules for Viva Engage groups:

- The Alignment tool renames all existing Viva Engage files that don't align with SharePoint naming standards to meet requirements.
- Group files that reside in Microsoft Azure get copied to a new SharePoint Document Library (SDL) for the group. After the file copy and migration complete, we delete the non-SharePoint version of all files.
- Previously deleted group files are permanently deleted.
- New files always upload to the SDL.
- After migration completes, non-SharePoint group files are deleted *within 30 days*.
- Viva Engage files that don't align with SharePoint naming standards are renamed to meet requirements.

## File renaming rules

The Native Mode Alignment Tool also follows a set of file naming conventions when it begins the migration: 

- Filenames with unsupported characters in SharePoint replace those characters with an underscore (`_`).
- Duplicate files, or files with names that already exist in SharePoint, are renamed using the format `filename_yammerFileID_extension`.
- Filenames with a blank space as the first or last character, or that end with a period, are edited to remove those characters.
- Unnamed files are named according to the following format: `Viva Engage File`, `Viva Engage File (1)`, `Viva Engage File (2)` and so on.
- Filenames starting with `\~$` are renamed to remove the leading tilde, for example: `~$Viva Engage File` is renamed to `$Viva Engage File`.
- Filenames containing `_vti_` anywhere in the name are replaced with `-vti-`. For example: `Viva_Engage_vti_File` is renamed to `Viva-Engage-vti-File`.
- Filenames that contain `.lock`, CON, PRN, AUX, NUL, COM0 - COM9, LPTO - LPT9, or desktop.ini are renamed to append `_file` to the name. For example, `COM0` gets renamed to `COM0_file`. 
- For groups that have multiple files with the same name, the tool appends duplicate filenames with `_X`, where X is an increasing number for each duplicate file (for example, `file_1`, `file_2`, `file_3`, and so on).

## Before you run the Alignment Tool

Because migration deletes files from your network and the process is irreversible, admins need to take the following actions before using the Native Mode Alignment Tool:

- In case anyone asks for them, export any necessary files before running the Alignment Tool. Learn more about how to [Export Viva Engage data](../manage-security-and-compliance/export-viva-engage-enterprise-data.md#find-and-delete-specific-messages-or-files).
- Ensure that your mobile and desktop users update to the latest version of Viva Engage Android, Viva Engage iOS, and Viva Engage Desktop apps. Older app versions have issues uploading files to SharePoint.
- If you use non-Microsoft or partner APIs to upload files, use the current REST API call for [Upload files into Viva Engage groups](/rest/api/yammer/upload-files-into-yammer-groups). Previous API versions are blocked. Individual upload file sizes are limited to 4 MB.
- Notify users that the migration deletes files from Viva Engage private messages. The latest version of the file migrates to SharePoint, and no previous versions get copied.

The Alignment Tool doesn't copy the follower count. Users also can't mark files as official.

## Admin step-by-step experience

Take the following steps to use the Native Mode Alignment Tool:

1. Export all files.

2. Start the **Native Mode Alignment Tool**.

3. Download the **Alignment Report**, which provides details on the files for each user and group.

   - Each user has a count for the total number of private message files. The Alignment tool deletes all private message files when the job completes.
   - Each group has a count of Viva Engage and SharePoint files. The Alignment tool migrates all Viva Engage files to SharePoint, with the exceptions noted in this article. Existing SharePoint files aren't affected.

4. Authorize and run the tool. You can expect the following time frames for networks with significant file counts:

   - SLA - up to 30 days for networks with < 100,000 files
   - SLA - up to 45 days for networks with > 100,000 files

5. After the Native Mode Alignment Tool job completes, review the automatically produced Error Report and determine if other steps are necessary before your network operates in Native Mode.

### End user experience

This table explains the expected end user experience for files while the Tool is running:

|Tasks|Microsoft 365 Viva Engage Groups|Unconnected Viva Engage Groups|Private Messages|
|-----|------------------------|-------------------------|----------------|
|Delete files|User can delete files|File isn't migrated to SharePoint.|Files are deleted and users have no access.|
|Edit file|Edited files are stored in SharePoint|Only the latest file migrates to SharePoint. **If a user edits a file during migration, they risk losing data**. Old versions are no longer accessible in SharePoint.|N/A|
|New file|New files are stored in SharePoint|File is in Microsoft Azure, but migrates to SharePoint by the time the Tool completes its work.|N/A|


If a group is deleted during the tool job, all the files from that group are deleted and don't migrate over.

## After successful entry to Native Mode

You can expect to see the following results after a network migration to Native Mode:

- All group files are [stored in SharePoint](https://go.microsoft.com/fwlink/?linkid=2111253), which provides a consistent file management experience.

- You can run file searches from SharePoint and from Viva Engage. Viva Engage searches the first 5,000 characters of files in Microsoft Azure cloud storage and the title and author, and searches only the title and author of files stored in SharePoint.

> [!NOTE]
> If you receive an error code during the alignment process for Native Mode, refer to the [Error Codes section in the Troubleshooting Native Mode article](../troubleshoot-problems/troubleshoot-native-mode.md#error-codes).

## What happens to files in private messages when you run the Native Mode Alignment Tool?

Users can't upload files to Private messages. Link sharing is still available. All files in Private messages are deleted.

## Related articles

[Overview of Native Mode](../overview-native-mode.md)

[Troubleshoot problems with Native Mode for Microsoft 365](../troubleshoot-problems/troubleshoot-native-mode.md)
