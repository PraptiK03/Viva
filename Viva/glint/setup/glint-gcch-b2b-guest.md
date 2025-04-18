---
title: Invite Government Cloud users to your Viva Glint tenant
description: For organizations with Viva Glint installed to a commercial tenant, admins can invite users that need dashboard access from GCC or GCC High cloud tenants as B2B collaboration users.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: b2b guest, gcc high cloud, invite users, cross-cloud settings, viva glint
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/04/2025
---

# Invite Government Cloud users to your Viva Glint tenant

Microsoft Viva Glint is available for commercial tenants but isn't available for Government Community Cloud (GCC) or Government Community Cloud High (GCC High) entities. For organizations with Viva Glint installed to a commercial tenant, admins can invite users that need dashboard access from GCC or GCC High cloud tenants as B2B collaboration users. Consider Viva Glint survey access methods, Microsoft Entra configuration steps, data upload requirements in the Viva Glint app, and the B2B guest sign-in experience described in this article when inviting GCC or GCC High users to your commercial tenant.

> [!NOTE]
> Cross-tenant synchronization and multitenant organization don't currently support cross-cloud setups.

## Survey access methods

Limit the number of users you need to invite to a commercial tenant by using a survey access method that doesn't require authentication for survey takers. Choose from personalized links or attribute-based access:

- [Personalized survey link](understand-survey-access-methods.md#personalized-survey-link)
- [Attribute-based access](attribute-based-survey-access.md)

Only users that require dashboard access need to be invited as B2B collaboration users.

## Configuration in the Microsoft Entra admin center

To invite GCC or GCC High users to your commercial tenant where Viva Glint is installed:

1. [Update cross-cloud access settings](#update-cross-cloud-access-settings)
2. [Invite B2B guests](#invite-b2b-guests-in-bulk)
3. Optionally, [limit users that appear in Microsoft Teams searches](#limit-users-that-appear-in-microsoft-teams-searches)

### Update cross-cloud access settings

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) with a role that has at least [Security Administrator](/entra/identity/role-based-access-control/permissions-reference#security-administrator) permissions.
2. [Enable cross-cloud access settings](/entra/external-id/cross-cloud-settings#enable-the-cloud-in-your-microsoft-cloud-settings).
3. [Add the tenant to your organizational settings](/entra/external-id/cross-cloud-settings#add-the-tenant-to-your-organizational-settings).

### Invite B2B guests in bulk

1. Sign in to the [Microsoft Entra admin center](https://entra.microsoft.com) with a role that has at least [User Administrator](/entra/identity/role-based-access-control/permissions-reference#user-administrator) permissions.
2. [Follow steps to invite guests in bulk](/entra/external-id/tutorial-bulk-invite#invite-guest-users-in-bulk).

### Limit users that appear in Microsoft Teams searches

1. Sign in to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).
2. Select **Teams** and go to **Teams settings.**
3. Under **Search by name,** enable **Scope directory search using an Exchange address book policy** by switching the toggle to **On**.
4. Users that are marked as hidden in Exchange don't show in Teams searches.

More information:

- [Limit who users can see when searching the directory in Teams](/microsoftteams/teams-scoped-directory-search)
- [Information barriers in Microsoft Teams](/purview/information-barriers-teams)
- [Address book policies in Exchange Online](/exchange/address-books/address-book-policies/address-book-policies)

## Upload users to the Viva Glint app

Viva Glint Admins need to upload all users from the GCC or GCC High tenant, including survey takers and dashboard users, to the Viva Glint app. To upload employee data to Viva Glint:

- [Choose a Viva Glint data upload method](choose-upload-method.md)

> [!IMPORTANT]
> Email addresses uploaded to Viva Glint must match what's on file in the GCC or GCC High tenant.

## Sign-in experience as a guest

Invited guests from GCC or GCC High tenants need to take these steps to access Viva Glint on a commercial tenant.

> [!TIP]
> To prevent sign-in issues, access Viva Glint in a new InPrivate or Incognito window.

1. Select the appropriate link for the organization's region:
   - US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
   - EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)
2. Select **Sign-in options** in the **Sign in** dialog.
   
   :::image type="content" source="../../media/glint/setup/sign-in-options.png" alt-text="Screenshot of the sign-in options selection for guest sign in.":::

5. Select **Sign in to an organization.**

   :::image type="content" source="../../media/glint/setup/sign-in-to-an-org.png" alt-text="Screenshot of the Sign in to an organization selection for sign in options.":::
   
7. Enter the **domain name** of the organization you'd like to sign in to (for example: `contoso.com`) and select **Next**.
   
   :::image type="content" source="../../media/glint/setup/gcch-enter-domain.png" alt-text="Screenshot of a guest sign in prompt for an organization's domain.":::
   
9. Enter the email address connected to your GCC or GCC High account, for example: `user@contoso.us`, and enter your password.
    
    :::image type="content" source="../../media/glint/setup/gcch-sign-in.png" alt-text="Screenshot of email and password entry for sign in.":::
   
12. Complete multifactor authentication steps to sign in.

    :::image type="content" source="../../media/glint/setup/gcch-mfa.png" alt-text="Screenshot of a sign in approval request for Microsoft Authenticator.":::

