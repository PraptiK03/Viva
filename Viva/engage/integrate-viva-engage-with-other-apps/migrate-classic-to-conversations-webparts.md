---
title: "Migrate classic feeds in SharePoint to the Viva Engage Conversations web part"
f1.keywords:
- NOCSH
ms.author: donnabouldin
ms.reviewer: spuranik
author: v-rgrace
manager: elizapo
ms.date: 05/06/2025
audience: Admin
ms.topic: upgrade-and-migration-article
ms.localizationpriority: medium
ms.service: viva-engage
ms.custom: Adm_Yammer
ms.collection: SPO_Content
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 4817d2fa-50f6-4f25-88a0-a312745768d4
description: "Migrate feeds that use the classic Highlights web part to Viva Engage Conversations web parts on your modern SharePoint pages."
---

# Migrate your classic feed on SharePoint to the Viva Engage Conversations web part

>[!NOTE]
>On June 1, 2025, Microsoft no longer supports the classic Highlights web part for Viva Engage feeds in SharePoint. To avoid a broken feed experience, we recommend that you migrate your SharePoint site to the Viva Engage Conversations web part using the instructions given in this article.

Modern SharePoint sites use the [Viva Engage Conversations web part](https://support.microsoft.com/en-us/office/use-a-viva-engage-web-part-in-sharepoint-a53cfa0c-3d09-42c8-a286-1038a81c59da?ui=en-us&rs=en-us&ad=us) to allow people to directly interact in SharePoint.

The Conversations web part is available only for the online SharePoint experience available in Microsoft 365. Learn more about [Viva Engage web parts](https://support.microsoft.com/en-us/office/use-a-viva-engage-web-part-in-sharepoint-a53cfa0c-3d09-42c8-a286-1038a81c59da?ui=en-us&rs=en-us&ad=us).

## Which web part version are you using?

SharePoint site owners can take the following steps to verify if they need to migrate their site:

1. Go to the SharePoint page that contains your Viva Engage feed.
2. If the feed includes a note stating that you’re using the classic version of Viva Engage, see the section [Migrate a classic Highlights web part to the Conversations web part](#migrate-a-classic-highlights-web-part-to-the-conversations-web-part) to migrate your feed.

If the feed doesn't include the classic version note, no action is required.

## Identify the SharePoint sites with the deprecated web part

Tenant admins can use a [downloadable script](https://www.microsoft.com/download/details.aspx?id=108154) to identify the SharePoint sites in your tenant that need to be migrated.

>[!NOTE]
>To run the script, the user must have the correct permissions to access the SharePoint admin site.

## Migrate a classic Highlights web part to the Conversations web part

Use this procedure to migrate all instances of the classic Highlights web part in SharePoint pages that you own or have permissions to. The migration process doesn’t affect Viva Engage data in any way.

1. **Open the existing classic feed on SharePoint**

    1. In SharePoint, select **Edit** at the top of the page.
    1. Select the classic Highlights web part that you want to replace and record the type of feed it's delivering to users (for example, user feed, community feed).

2. **Create a new feed using the Conversations web part**

    1. Hover above the classic Highlights web part where you want to create a new feed, and select the plus (+) icon.

        :::image type="content" source="../../media/engage/admin/hover-for-web-part-menu.png" alt-text="Screenshot shows how to access the web part menu.":::

    2. In the web part menu, select **Conversations**.

        :::image type="content" source="../../media/engage/admin/hover-menu-conversations-web-part.png" alt-text="Screenshot shows the option for creating a Conversations web part.":::

    3. Set up the Conversations web part to include settings you want to keep from your previous Highlights web part. Add new layout and background options from the right panel. For **Number of conversations to show**, select the number based on the allotted space you have for the feed.

        :::image type="content" source="../../media/engage/admin/web-parts-old-and-new.png" alt-text="Screenshot shows the Conversations menu where you specify the feed type, source, and other options.":::

    >[!NOTE]
    >For **Home** and **Community** feeds, turn off the **Publisher** option if you don't want users in your organization to publish new Engage posts from the web part.

    - **Home Feed** displays the most recent conversations that appear on the **Home** page in Viva Engage. Select if the classic Highlights web part displays the Viva Engage home feed.

    - **Community** displays the most recent conversations posted in the selected community. Select this option if the classic Highlights web part displayed a **group feed**, and enter the community name. Choose the appropriate filter for the conversations you want to display in the web part.

    - **User** displays the most recent conversations in which the user participated. If the classic Highlights web part displays a specific person’s user feed, select this option and enter the user name.

    - **Topic** displays the most recent conversations tagged with this topic. Select this option if the classic Highlights web part displays the feed for a topic. Enter the topic name.

3. **Delete the old feed and publish the new one**
    1. To delete your previous classic feed, use the trash can icon at the top left edge of the feed.

    2. To publish your changes, select **Republish** in the top right corner.
