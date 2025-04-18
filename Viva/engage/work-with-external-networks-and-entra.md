---
title: "Work with external networks in Viva Engage"
description: "Describes integration of external networks for partners and consultants."
ms.reviewer: blyttle
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 04/15/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: high
ms.collection: 
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Work with external networks in Viva Engage

>[!NOTE]
> The modern Viva Engage user experience is coming to external networks starting June 1, 2025. This document provides high-level procedures to migrate your existing external networks to the new experience. For details, [see the Message Center notification about this feature set](https://iridias.microsoft.com/messagecenter?id=1036575).

Viva Engage networks support a format called M365 Native Mode which uses Microsoft Entra identities and policies. Native mode operation is **required** for all Viva Engage networks in the enterprise. It enables users, groups, and content to map to their counterparts in Microsoft Entra and Microsoft 365. Native Mode also supports eDiscovery through the Microsoft Purview portal, so your organizations safely and securely collaborates in your Engage network.

Viva Engage legacy external networks require alignment to Microsoft Entra to operate in M365 Native Mode. Customers benefit from the full suite of Microsoft Security and Compliance features.

As of April 2025, nearly all customer organizations with significant Viva Engage networks observe the Native mode standard. Any remaining customers have until June 1, 2025 to complete the alignment of their external networks to Microsoft Entra. Use the following procedures to develop your new external network and to migrate data from the existing external network.

>[!NOTE]
> Also see [Viva Engage Native Mode: Step-by-step guide](native-mode-guide.md) for more information about how M365 Native Mode works and the advantages it offers. All Viva Engage networks of all types must observe this standard.

## Three-Phase external networks configuration

The updated external network process has three phases:

:::image type="content" source="../media/engage/admin/config-and-connect-1.png" alt-text="High-level steps for external network conversion.":::

The following terms are used in this document:

- **Parent network**: Your current Viva Engage network
- **New Entra tenant**: The new Microsoft Entra tenant that hosts the new external Viva Engage network
- **Legacy external network**: Your current external network
- **New external network**: The new native-on-Microsoft 365 external network

### Set Up a new Microsoft Entra tenant

:::image type="content" source="../media/engage/admin/config-and-connect-2.png" alt-text="First high-level step for network preparation":::

New Viva Engage networks always map to a new Microsoft Entra tenant. Every new external network requires its own Microsoft Entra tenant.

You need specific permissions and licenses:

- Viva Engage external network v2 configuration requires Global Administrator privileges.

- Because the external network uses Microsoft 365 Groups, Entra B2B, and SharePoint Online storage, at least one user in the tenant requires a Microsoft SharePoint license.

- **Recommended license requirement:** Assigning a Microsoft 365 E5 license automatically supports the full Compliance Purview experience.

>[!NOTE]
> During tenant creation, select **Microsoft Entra ID** for the tenant. Avoid use of other values such as *Microsoft Entra ID (B2C)*.

The Global Administrator needs to follow the steps in the following **Create a New Tenant** link from Microsoft Entra.

[QuickStart - Access and create new tenant - Microsoft Entra | Microsoft Learn](/entra/fundamentals/create-new-tenant#create-a-new-tenant-for-your-organization).

After you finish configuring the new tenant, keep its tenant ID handy, because you'll need it for later steps.

>[!NOTE]
> The creation of the new tenant automatically projects the creating user as a B2B Guest user and assigns the Global Administrator role and privileges.

### Connect Engage in the new Microsoft Entra tenant with the parent Engage network

You apply two important procedures in this step:

- Generate a tenant association token

- Redeem the tenant association token to connect the two Viva Engage networks (the Parent network and the new external network).

#### Generate the tenant association token

In Engage, as a Global Administrator, sign in to the New Engage Network in the new Microsoft Entra tenant by going to engage.cloud.microsoft.

Do the following to access external networks setup:

1. In Engage, select the settings icon, and go to Admin center.

2. In the Admin center, on the Setup and Configuration tab, select the external network.

3. Select **Setup external network**.

    :::image type="content" source="../media/engage/admin/config-and-connect-3.png" alt-text="Setting up the external network.":::

4. Select the **Generate Code** tab to generate a one-time code to associate the new external network with the parent Engage network. After you generate the association code, take note as it's used in later steps.

:::image type="content" source="../media/engage/admin/config-and-connect-4.png" alt-text="Generate the Code step.":::

#### Associate the new network with the parent Engage network

In this section, you redeem your generated token to associate the new external network with the parent network.

1. Network switch to the parent Engage network. (Ensure that you're using the same Global Administrator account that's responsible for the new Microsoft Entra tenant.) You now access external networks setup.

2. In Engage, select the settings icon and go to the admin center.

3. In the **Setup and configuration** tab, select **External networks**.

4. Select **Setup external network** to redeem the association code. Select the **Redeem code** tab, and add the association token and Entra tenant ID saved from the previous steps.

    :::image type="content" source="../media/engage/admin/config-and-connect-5.png" alt-text="Select Redeem Code to establish the association.":::

5. After the association, an *External network has been successfully setup* message appears.

    :::image type="content" source="../media/engage/admin/config-and-connect-6.png" alt-text="A message appears to confirm the setup.":::

### Connect the legacy Engage network to the new Engage network

You need to run this procedure to move data from the current external network to your new one.

1. From the parent Engage network, switch to the legacy external network.

2. To open the external network settings, select its Settings icon and select **Network admin** from the menu.

3. To associate the legacy external network to the new network, select **External network upgrade** from the menu.

    :::image type="content" source="../media/engage/admin/config-and-connect-7.png" alt-text="Select the External Network Upgrade option from the Admin menu.":::

4. Using the same Tenant ID and tenant association token from the previous steps, enter the information in the appropriate fields and select **Redeem Token**.

    :::image type="content" source="../media/engage/admin/config-and-connect-8.png" alt-text="Select the Redeem Token option.":::

After the token redemption, the legacy Engage external network is now associated with the new external network. The software signs the user out at this point to allow signing in with Microsoft Entra as your identity provider. You're ready to begin data migration to the new network.

## Data Migration from a legacy network to the new external network

The next process starts the data migration of the legacy network's content to the new external network. You must export or configure your user accounts for use in the new deployment.

:::image type="content" source="../media/engage/admin/config-and-connect-9.png" alt-text="Migrating the existing network's content to the new network.":::

1. Sign in to the legacy external network using admin privileges.

2. In the Admin experience, select **Export users** to export the set of user accounts in the legacy external network. Entra produces a .CSV file that contains your user account information.

3. As the Global Admin for the new Entra tenant, sign in to the Entra Portal. To bulk-add the users from the legacy external network, provide the exported users' CSV file to bulk-invite them as guests in the new network.

:::image type="content" source="../media/engage/admin/config-and-connect-10.png" alt-text="The Entra console provides the bulk-invite feature.":::

>[!NOTE]
> For more information, see [Bulk invite B2B users - Microsoft Entra External ID | Microsoft Learn](/entra/fundamentals/create-new-tenant#create-a-new-tenant-for-your-organization).

### Move the network data

With the legacy external network now associated with the new external network, you can start the data move/data alignment.

:::image type="content" source="../media/engage/admin/config-and-connect-11.png" alt-text="Select the M365 Native Mode tab.":::

After signing in to the external network, after you execute the external network upgrade process, you see the **M365 Native Mode** option in admin settings. To complete the M365 Native Mode alignment, select this tab and follow its instructions.

:::image type="content" source="../media/engage/admin/config-and-connect-12.png" alt-text="Instructions for M365 Native Mode configuration.":::

## Launch the new external network

:::image type="content" source="../media/engage/admin/config-and-connect-13.png" alt-text="The last stage of external network migration.":::

>[!IMPORTANT]
> Update the policies of the Entra tenant that hosts your new external network. Base them on your security requirements, including the policies to identify, respond to, and recover from security threats.

After completing the data move to the new external network, administrators must take the following actions:

- Confirm that all Communities are configured and operating as they did in the legacy network;

- Notify users of the new network through a communication channel applicable to your organization.

>[!NOTE]
> When you replace your guest accounts in the new network, it offers a feature to notify users of the new URL/domain.

## FAQ

**Where can I find more information about M365 Native mode?**

See [Viva Engage Native Mode: Step-by-step guide](native-mode-guide.md) for more details about how it works and its advantages. All Viva Engage networks must observe this standard.

**What happens to my users from the legacy external network?**

You can export the list of existing users in your legacy external network in a CSV file from the Native Mode setup flow. You can also use the CSV file to bulk invite the users to your new external network via the Microsoft Entra portal.

**I use external networks for Consumer Identities, are these still supported in modern external networks?**

Yes. Engage continues to support consumer identities in both external and parent Engage networks.

**What is the process for members joining the migrated external network?**

The updated external network supports adding members by using the invitation flow.

Admins can also use Cross-Tenant Sync to move users directly into Entra. Those users have access to the new external network.
