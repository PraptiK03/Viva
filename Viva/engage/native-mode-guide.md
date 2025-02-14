---
ms.date: 12/26/2024
title: "Viva Engage Native Mode: Step-by-step guide"
description: "Learn about the process of migrating to Native Mode with this in-depth step-by-step guide."
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

# Viva Engage Native Mode: Step-by-step guide

Organizations that want to use Viva Engage compliance features need to make sure their network supports Native Mode. For greater security and compliance, Native Mode fully backs Viva Engage through Microsoft 365. Native Mode also supports the following features:

- Host a live event in every Viva Engage community
- Simplify file administration through SharePoint
- Apply Microsoft 365 Group management policies

Any Viva Engage network created after January 16, 2020 supports Native Mode and its full feature set. 

If you support older Viva Engage networks in your Microsoft tenant, you can use the Native Mode Alignment Tool to integrate your network with Microsoft 365.

The following steps describe how to transition your network to Native Mode. For more information about what Native Mode means for your Viva Engage Network, see [Overview of Native Mode](overview-native-mode.md).

## 1. Initial steps to access the Native Mode Alignment Tool

To align your network to Native Mode, your Microsoft tenant must have a single Viva Engage Network associated with it. If you have more than one Viva Engage Network in your tenant, you need to consolidate them. To do so, complete the steps in [Consolidate multiple Viva Engage networks](./configure-your-viva-engage-network/consolidate-multiple-networks.md).

After consolidating the Viva Engage network, make sure that it enforces Microsoft 365 identity. For more information, see [Enforce Microsoft 365 Identity](./configure-your-viva-engage-network/enforce-office-365-identity.md).

## 2. Access the Native Mode Alignment Tool

You must be an Engage admin to use the Native Mode Alignment Tool. If your account temporarily receives these admin privileges, it can take a few hours for Viva Engage to reflect them. Once granted, temporary privileges are required only to initiate the alignment process; they aren't required while the tool is running. Privileged Identity Management (PIM) doesn't affect the alignment process.

To access the Native Mode Alignment Tool after Viva Engage recognizes your admin account: 

1. Sign in to Viva Engage.
2. Open the Network Admin section and select **Native Mode for Microsoft 365**.

## 3. Prepare to run the Native Mode Alignment Tool

> [!IMPORTANT] 
> The Alignment Tool can take a long time for processing. Most customers can run the tool over one to two weeks, but it can take up to 90 days in extreme circumstances.

Before you run the Native Mode Alignment Tool, generate and review the Alignment Report for your network. To run the report from within the tool, select the **Generate Report** button in the middle of the screen. The report produces a list of all users and communities in your Viva Engage Network. This step doesn't change your network and doesn't start the alignment process.

This report is in YML format. If you want to review the report as a CSV file, we provide a tool available in GitHub that converts the file.

The report provides the following information:

- **Which users are currently unmapped**

  The Alignment Tool tries to map all unmapped users to an existing Microsoft Entra account. Any users who don't have a Microsoft Entra account are deleted from the network.

- **How many files each user has stored in Private Messages**

  The Alignment Tool hard-deletes all files that are attached to private messages. These files are unrecoverable after alignment completes.

- **Which communities in your network are Private and Unlisted**

  Unlisted communities become standard private communities through the Microsoft Entra B2B Guest framework alignment. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have Microsoft Entra B2B guests in your Viva Engage network, you can reinvite them as Microsoft Entra B2B guests as part of the migration.

- **Which communities in your network allow external guests**

  Native mode doesn't allow external groups. Guest access to networks in Native Mode takes place through the Microsoft Entra B2B Guest framework. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have Microsoft Entra B2B Guests in your Viva Engage network, you can reinvite your guests as Microsoft Entra B2B guests as part of the migration.

- **Which communities in your network don't have any owners or have owners who lack Microsoft 365 Group creation rights**

  The Native Mode Alignment Tool creates a new Microsoft 365 Group, which is authorized by using the credentials of the existing owners of the Viva Engage community. If the community has no owner&#8212;or if no owners are authorized to create Microsoft 365 Groups&#8212;the tool creates the group using the credentials of the admin who started the Alignment Tool.

> [!NOTE] 
> Before you run the Alignment Tool, notify all users who have files stored in private messages, owners of any groups that are marked as unlisted, and owners of any external groups.

## 4. Export the content in your Viva Engage network

Immediately before you run the Alignment Tool, export any content from your Viva Engage Network that isn't already backed up. The best practice is to regularly export this content. We also suggest regularly scheduled automated backups. When you use regular backups, it's easier to export any other data as needed.

If you don't make regular data backups, export all the data in the home network that you want to keep. You can ignore external networks, because the Native Mode Alignment Tool doesn't affect them. You can export data from the beginning of your network, or export data going back a certain period of time. 

The Native Mode Alignment Tool deletes certain data from your network, including files attached to private messages, and messages posted in previously deleted groups. Any data that isn't backed up might be nonrecoverable after the Alignment Tool runs.

Take the following steps to export a large volume of content from your network:

  1. **Export message data** 
     - Export message data by using the [Network Data Export feature](eac-as-manage-data.md#export-tenant-data-by-date-range) in the Viva Engage admin panel.
     - Limit your export to a maximum date range of two months at a time and exclude attachments. If you include attachments, you may need to limit your date ranges to avoid time-out errors (to one week at a time, for example).

  2. **Export files**
     - Export files separately from messages with the [Viva Engage file export API](/rest/api/yammer/yammer-files-export-api).
     - Run API requests to export all files from a specified date range. The API supports up to six concurrent requests. Each request should be limited to a two-month period. You can use this method to simultaneously export a full year of files in a single API call.

## 5. Run the Alignment Tool for the first time

After you review the Alignment Report, make sure to do the following tasks:

- Communicate upcoming changes to the users in your network
- Export your data
- Possess full knowledge of the changes the tool makes in your network. 

You're ready to run the Native Mode Alignment Tool.

The tool runs in the background of your Viva Engage network and has no effect on end users. When the tool starts, it makes changes to your network to prevent new unmapped users, unconnected groups, and other new entities.

> [!IMPORTANT] 
> In most cases, you'll need to run the Alignment Tool more than once.

To run the tool, scroll to the bottom of the page and select the **Continue** button. 

You receive a prompt to confirm that you've read and understand the changes that the tool makes to your network. Check through the form, and ensure you fully understand the implications of running the tool.

> [!IMPORTANT]
> The Native Mode Alignment Tool makes permanent and irreversible changes in your network. Data deleted through this process can't be recovered.

When you're ready, complete the authorization form and start the Alignment Tool. You need to keep the window open for up to five minutes while the initial phase of the tool finishes. If you try to navigate away from the page during the setup phase, the tool sends a warning to prevent you from accidentally leaving too soon.

## 6.	Track Alignment Tool progress

The Alignment Tool runs in the background and doesn't affect end users. Small networks may be able to complete the process in one to two weeks. For large networks, the first run can take up to 90 days. If your network needs to run the tool multiple times, each run takes less time than the previous run, as the tool only needs to process content that wasn't processed in previous runs.

To check on the progress of the Alignment Tool, go back to the page where you started the tool. At the top of the page, a banner reports the current status of the tool, next steps, and whether the tool is ready for you to take next steps.

Near the bottom of the screen, details about the status appear every 30 minutes. Details include the number of migrated users, groups, and files.

## 7. Resolve the error report

When the tool finishes, the banner at the top of the page gives a report. When the banner says that your network is successfully aligned to Native Mode, the alignment process is complete and no further action is required. If the banner says that the alignment failed and provides a link to an error report, you must download the error report and fix the errors. Most errors are easy to resolve and require that you rename a file that has characters that aren't allowed in SharePoint files.

> [!NOTE]
> The error report appears at the bottom of the page. The error report differs from the Alignment Report that you reviewed earlier.

This CSV error report remains available until the next time the Alignment Tool is run. On a second run, the tool generates a new error report.

The report contains a list of files that failed to migrate from Microsoft Entra ID to SharePoint, with error codes. For a list of common error codes and remediation steps, see the [error codes section of this article](troubleshoot-native-mode.md#error-codes). You also can enlist our Premier Support Team to help resolve errors. If you have a high volume of errors, the Support Team can provide scripts to bulk-update the files in your network for faster remediation.

It's possible that your error report contains errors that aren't covered in the documentation cited earlier or that don't appear to be actionable. Often these errors are duplicates of other errors that are actionable. Work through all the errors that you can and then rerun the Alignment Tool. Most of these errors get resolved when you run the tool after fixing actionable errors.

> [!IMPORTANT]
> After a network is successfully aligned to Native Mode, the system automatically prevents any action that would break this alignment. Once this process runs successfully, you don't have to go through it again.
