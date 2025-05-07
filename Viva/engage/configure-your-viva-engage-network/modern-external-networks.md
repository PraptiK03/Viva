---
title: "Set up modern external Viva Engage networks"
description: "How to set up an External network for collaborating with your partners."
ms.reviewer: rajjain
ms.author: donnabouldin
author: v-rgrace
manager: donnabouldin
ms.date: 04/10/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: install-set-up-deploy
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up modern external Viva Engage networks (Preview)

>[!IMPORTANT]
>External network is currently in Preview. It's a redesigned external Viva Engage network type that requires and fully supports Microsoft Entra authentication and identity.

Microsoft designs modern external Viva Engage networks to promote collaboration between organizations. Modern networks allow users and teams from different companies, known as *external participants*, to communicate and share information in an industry-standard secure environment. Enterprise admins allocate these special external networks to partners, consultants, and other outside companies to conduct team discussions, share files, and collaborate on projects.

All Viva Engage networks support a format called M365 Native Mode, which uses Microsoft Entra identities and policies. Native mode operation is **required** for all Viva Engage networks in the enterprise. It enables users, groups, and content to map directly to their accounts in Microsoft Entra and in Microsoft 365. All parent Engage networks and external Engage networks observe this standard. Native Mode also supports eDiscovery through the [Microsoft Purview portal](https://ms.web.purview.azure.com/) to promote safe and secure collaboration in your Engage networks.

## Supported features for the modern external network

**External Participants**: Users can add external participants to public and private Viva Engage communities.

**Create and Connect**: Users can browse existing external networks or create new networks to connect with external collaborators.

**Management**: Administrators can manage external networks, set permissions, monitor activity, and ensure compliance with organizational policies.

> [!NOTE]
> Modern Viva Engage external networks support the Communities feature, with future expansions to include Campaigns, Events, and Knowledge.

## Requirements

Modern external networks must use the following Microsoft 365 requirements:

- Global Administrator privileges
- Microsoft 365 E5 license for at least one user
- Permissions to create new Workforce tenant.

Viva Engage also has the following requirements:

- The active [Global Administrator](/viva/engage/eac-key-admin-roles-permissions#microsoft-365-global-administrator) account

## Set up a modern external network

Take the following steps to perform a modern external network configuration. Complete these tasks in the order shown. Since the role requirements vary by each task, they're called out in each section.

### Set up a new Microsoft Entra workforce tenant

> [!NOTE]
> Consult the Microsoft Entra documentation [QuickStart - Access and create new tenant](/entra/fundamentals/create-new-tenant#create-a-new-tenant-for-your-organization) for the information and steps to set up your [new workforce tenant](/entra/external-id/tenant-configurations#workforce-tenants) for the modern external network.

After you create the tenant, copy the new Entra Tenant ID to a safe location for later use.

### Assign the required license to the tenant admin

The new tenant automatically embeds the creating user as a B2B Guest user and assigns them the Global Administrator role and privileges.

You also use the Microsoft Entra admin center to assign the correct license to the B2B Guest user. You assign a Microsoft 365 E5 license to the Global Administrator of the new tenant. Doing so allows the Global Administrator to sign into Viva Engage as the Engage Network Admin.

> [!NOTE]
> Enable the *Engage Core Service plan* for the user in the assigned Microsoft 365 E5 license. The admin should then confirm that the B2B Guest user account owns the global admin role and the correct Microsoft 365 E5 license.

### Connect the new Entra tenant to the parent network

Because the legacy external network doesn't yet have a Microsoft Entra tenant that backs it, the legacy network can't communicate with the parent Viva Engage network.

The new Entra tenant also needs to connect to the parent network. The next step is to connect the new Microsoft Entra tenant with the parent Viva Engage network so the parent network knows about its existence.

This process requires two steps:

- Generate a tenant association token.
- Redeem the tenant association token in the parent network. This step connects and links the new Microsoft Entra tenant to the parent Viva Engage network.

#### Generate the association token

Do the following to create the association token:

1. As the Viva Engage Global Administrator, go to engage.cloud.microsoft and sign into Viva Engage *on the new Microsoft Entra tenant*.
2. In Viva Engage, select the settings icon, and go to Admin center.
3. In the Admin center, on the **Setup and Configuration** tab, select **External Networks**.
4. Select **Setup External Network**.

    :::image type="content" source="../../media/engage/admin/admin-center-ext-networks-1.png" alt-text="Obtain the code to associate the new network":::

5. Select the **Generate Code** tab to generate a one-time tenant association code, and select **Generate**. You use the code to associate the new Entra tenant with the *parent Engage network*.

    :::image type="content" source="../../media/engage/admin/admin-center-ext-networks-2.png" alt-text="Generate the code":::

Make a note of the association code, because you use it in later steps.

#### Redeem the Token to associate the new external network/tenant with the parent Viva Engage network

This process uses the association token to establish the new Entra tenant with the enterprise parent Viva Engage network.

1. Sign out of the new Engage external network. (If you use In-Private, or Saved Profiles, you don't need to sign out.)
2. Sign in to the parent Viva Engage network on engage.cloud.microsoft. (The user must be the same Global Administrator that sets up the new Entra tenant.)
3. To access External Networks Setup in the parent network, select the settings icon, and go to the admin center.
4. In the admin center **Setup and Configuration** tab, select **External Networks**.
5. Select **Set up external network**.
6. Select the **Redeem code** tab to redeem the association code. Add the association token and the Entra tenant ID you saved from the prior steps.

After the redemption of the association code, you see the following result:

:::image type="content" source="../../media/engage/admin/external-network-confirmation.png" alt-text="Token redemption in the new network":::

The parent network now connects to the new tenant.

#### Connect the legacy external network to the new external network

After the new Microsoft Entra tenant associates to the parent network, you set the *legacy external network* to connect to the *new external network*. To do so, you use the same association token and Tenant ID that you used in the previous sections.

1. From the parent Engage network, network switch to the legacy external network.
2. To open the external network settings, select the **Settings Icon** on the external network and choose **Network Admin**.
3. To associate the legacy external network to your new external network, select **External Network Upgrade** from the menu.
4. Use the same tenant ID and tenant association token from the previous steps to enter the information in the appropriate fields and select **Redeem token.**

:::image type="content" source="../../media/engage/admin/external-network-upgrade-on-parent.png" alt-text="Token redemption":::

The legacy Viva Engage external network binds to the new external network and is backed by the new Entra tenant.

> [!NOTE]
> The system signs the user out from the legacy network to allow immediate sign in with Entra as the identity provider.

## Data Migration from legacy network to new external network

The next phase establishes the legacy network's user database in the new external network. For consistency, always use the user accounts database from your legacy external network. You do so with a CSV file that you export from your legacy external network.

### Export users from the legacy external network

1. Sign in (or network switch) to the legacy external network.
2. In Viva Engage, select the Settings icon, and go to Admin center.
3. In the Admin center, select the **Governance and Compliance** tab, and select **Data export**.
4. Under **Export user list**, enter the **Start date* and select the **End date**, then select *Download CSV file**.

:::image type="content" source="../../media/engage/admin/external-network-export-from-legacy.png" alt-text="Admin menu for the external network":::

Viva Engage uploads the new CSV file in a folder to your designated download location.

### Add exported user accounts as guest users in the external network

In the Microsoft Entra admin center, you import the current user accounts CSV from the legacy external network.

:::image type="content" source="../../media/engage/admin/external-network-entra-data-import.png" alt-text="Importing the legacy network data to the parent network's tenant":::

1. Sign in to the Microsoft Entra admin center as the Global Admin for the Entra tenant in your parent deployment.

2. Use the exported users CSV file [to bulk-invite the users from the legacy external network as guests in the new network](/entra/external-id/tutorial-bulk-invite).

### Run the Native Mode data alignment for the external network

After the legacy external network associates with the new external network, you can run the data move/data alignment process. Doing so aligns the legacy network's resources with Microsoft 365 Entra resources.

After you successfully connect the external network to the parent, the **M365 Native Mode** feature appears in the Viva Engage admin settings. To complete the Native Mode alignment, select this tab and follow the instructions.

:::image type="content" source="../../media/engage/admin/external-network-native-mode-setting.png" alt-text="Setting the external network to M365 Native Mode":::

When Native Mode alignment runs, the Native Mode configuration page shows progress and identifies failed steps for which you can take action.

:::image type="content" source="../../media/engage/admin/external-network-native-mode-screen.png" alt-text="Native Mode admin page for new network":::

## Launch the modern external network

>[!IMPORTANT]
>Update the policies of the Entra tenant that hosts your new external network based on your security posture. Pay particular attention to policies that identify, respond to, and recover from security threats.

After the data move completes, the network administrators can take the following steps:

- Confirm that the communities are configured as they were in the legacy Network.
- Notify users of their membership in the new network.

> [!NOTE]
> When you bring user accounts to the updated external network, it offers a feature to notify users of the new URL/domain. We recommend that you include the tenant ID of the new External Network in the invite URL. Format it as `https://engage.cloud.microsoft/main/org/<Tenant ID>`.

## FAQ

### What happens to my users from the legacy external network?

You can export the list of existing users in your legacy external network in a CSV file from the Native Mode setup flow. You can use the CSV file to bulk invite the users to your new external network via the Microsoft Entra admin center.

### Can I use external networks for consumer identities in modern external networks?

External networks provide full support for the Consumer Identities use case.

### What's the process for members to join the migrated external network?

The Converted external network continues support for the invitation flow to add members. Additionally, Admins can use Cross-Tenant sync to join users directly into Entra, and those users have access to the external network.
