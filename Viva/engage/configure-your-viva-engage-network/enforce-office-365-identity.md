---
title: "Enforce Microsoft 365 identity for Viva Engage users"
description: "When you enforce Microsoft 365 identity in Viva Engage, all Viva Engage users use their Microsoft 365 credentials to sign in to Viva Engage."
f1.keywords:
- CSH
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/23/2025
audience: Admin
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: 
- Adm_Yammer
- fwlink from UI
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 008f940b-6bec-47fc-bcc6-9c6133467562
---

# Enforce Microsoft 365 identity for Viva Engage users

When Viva Engage becomes a core service for your organization, users need to sign in seamlessly like any other Microsoft 365 service.

To streamline user management, enforce Microsoft 365 identity in Viva Engage to maintain a single identity for all your users. It's easy to implement single sign-on (SSO) capabilities for Microsoft 365, including Viva Engage. Doing so also simplifies your users' experience signing in to Viva Engage.

SSO requires that Viva Engage admins configure the following capabilities:

   - Password hash sync
   - Pass-through authentication or [Microsoft Entra ID](https://support.office.com/article/06a189e7-5ec6-4af2-94bf-a22ea225a7a9#BK_Federated).
  
## How it works

The following flowchart shows what happens when a user signs in to Viva Engage.
  
:::image type="content" source="../../media/engage/admin/enforce-o365-id.png" alt-text="Flowchart shows what happens when user signs in when Microsoft 365 identity is enforced, they sign in with their Microsoft 365 identity.":::
  
Here's an account of the user's sign-in experience:
  
1. The user tries to sign in to Viva Engage, and gets a sign-in dialog box.
    
2. The user enters their email address.

   - **When you enforce Microsoft 365 identity**, the user just signs in with their Microsoft 365 identity. If your Microsoft 365 tenant implements the *federated identity model*, the user uses SSO as they do for all other Microsoft 365 apps.
    
   - **When Microsoft 365 identity isn't enforced**, user sign-in is more complicated, because they don't use SSO: 
   
      - If their email address corresponds to a Microsoft 365 account, they can sign in with their Microsoft 365 identity;

      - If their email address doesn't correspond to a Microsoft 365 account, they sign in with their Viva Engage identity.
    
The following table compares the user sign-in behavior when you enforce Microsoft 365 identity, or when it isn't enforced. Microsoft 365 identity isn't enforced by default.
  
| Is Microsoft 365 identity enforced? | Is the user's email address tied to a Microsoft 365 account? | What happens when the user signs in |
|:-----|:-----|:-----|
|Yes |Yes |The user is prompted to sign in with their Microsoft 365 identity. |
|No |Yes |The user is prompted to sign in with their Microsoft 365 identity. |
|No |No |The user is prompted to sign in with their Viva Engage identity (email and password). |
   
<a name="StartEnforcing"> </a>

## Start enforcing Microsoft 365 identity in Viva Engage

It's easy to start enforcing Microsoft 365 identities in Viva Engage. However, enabling it logs off all current users' sessions in Viva Engage. Before you take action, do the following to make sure your Viva Engage users can continue working smoothly:
  
- **All current Viva Engage users must have a corresponding Microsoft 365 identity.** When you enforce Microsoft 365 identities for Viva Engage, any user without that identity is locked out of Viva Engage. Ensure that all of your current Viva Engage users have their Microsoft 365 identities. To do so, go to the data export page in the Viva Engage admin center and export all users. Compare that list to the list of users in Microsoft 365 and make any needed changes.
- **Tell your users about this change.** Inform all your users that you're switching to Microsoft 365 identities, because it can disrupt their day-to-day usage of Viva Engage. See the following sample email for suggested text.
  
### To start enforcing Microsoft 365 identity in Viva Engage

You must have Microsoft 365 Global administrator privileges and be synchronized to Viva Engage on Microsoft 365.
  
1. In the Yammer admin center, select **Settings -> Edit network admin settings**, and choose **Security Settings**.

2. In the Security Settings page, go to the **Microsoft 365 Identity Enforcement** section and select **Enforce Microsoft 365 identity**.

    :::image type="content" source="../../media/engage/admin/enforce-o365-settings.png" lightbox="../../media/engage/admin/enforce-o365-settings.png" alt-text="Screenshot that shows the Enforce Microsoft 365 identity in Viva Engage checkbox in the Viva Engage Security Setting page.":::
  
3. A confirmation message asks you to select the level of enforcement:

   - **Committed Enforcement**: This option applies if all of your Viva Engage users have an account in Microsoft Entra ID.

     :::image type="content" source="../../media/a0927cc2-eafa-4ace-a939-a3fa27be943b.png" alt-text="Screenshot of confirmation dialog box that shows the Enforcement level for Microsoft 365 sign-in.":::

     > [!IMPORTANT] 
     > You can't undo this change, which means your users can't use their original Viva Engage usernames and passwords to sign in.
  
   - **Temporary 7-Day Enforcement**: Choose this option if you're testing enforcement of Microsoft 365 identity on your network, and might need to revert the change. A temporary enforcement period of seven days begins, and your users can't sign in with Viva Engage usernames and passwords. After seven days, your network automatically commits to Microsoft 365 identity enforcement. [This setting supports an Undo feature](enforce-office-365-identity.md#stop-enforcing-microsoft-365-identity-in-viva-engage), so you can reset your network to its previous enforcement.

     :::image type="content" source="../../media/a0927cc2-eafa-4ace-a939-a3fa27be943b.png" alt-text="Screenshot of confirmation dialog box that shows the Enforcement level for Microsoft 365 sign-in.":::
  
4. If necessary, you can sign out all current users to ensure that everyone using the Viva Engage service signs in with their Microsoft 365 identities. To sign out all current users, select the **Log out all users** checkbox. If you decide to do so, we recommend that you communicate this change using the following sample email.

   *Subject Line: [Action Required] upcoming automatic sign out from Viva Engage*

   *Hello,*

   *This email is to inform you that [ORGANIZATION'S NAME] is changing the way that our users access Viva Engage. If you're currently working on Viva Engage, you may experience an automatic sign out. This event is due to security configuration of Microsoft 365 single sign-on for Viva Engage. This change improves your experience by allowing you to use the same sign-on that you use for all of your other Microsoft 365 applications.*

   *You can immediately resume your work by signing in to Viva Engage again with your Microsoft 365 username and password.*

   *We made this change so that you can access all of Microsoft 365 with a single identity. If you can't sign in using your Microsoft 365 username and password, let your network administrator know.*

   *Thank You.*

   *[SIGNATURE]*
    
5. If you're ready to start enforcing this setting, select **Okay**.

6. Go to the Security Settings page where the **Enforce Microsoft 365 identity in Viva Engage** checkbox is now selected.

   > [!NOTE]
   > You can also select **Block Microsoft 365 users who don't have Viva Engage licenses** to ensure that only users with Viva Engage licenses sign in to Viva Engage.
  
6. Choose **Save** to save all your settings on the page.

## Stop enforcing Microsoft 365 identity in Viva Engage

<a name="StopEnforcing"> </a>

> [!IMPORTANT]
> You can end enforcement of Microsoft 365 identities in Viva Engage when you're in the temporary seven day enforcement period. 
  
When you stop enforcing Microsoft 365 identities in Viva Engage, the following changes occur:
 
- Other users can join your network by signing up with their work email and verifying it.
- Any users already signed into Viva Engage with their Microsoft 365 identities remain unaffected by this change.
  
**Stop enforcing Microsoft 365 identity in Viva Engage**

You must be a global administrator to perform these steps.
  
1. In Viva Engage, go to the **Network Admin** section, and select **Security Settings**.

2. In the Security Settings page, go to the **Microsoft 365 Identity Enforcement** section and clear the **Enforce Microsoft 365 identity** checkbox.

   A confirmation message asks you to verify that you're ready to stop enforcing Microsoft 365 identity.

   :::image type="content" source="../../media/09162001-6581-41f9-b558-27673366c2a8.png" alt-text="Screenshot of confirmation dialog box to stop enforcing Microsoft 365 identities in Viva Engage. If previously configured, Viva Engage SSO restarts. The change doesn't affect users who sign into Viva Engage with Microsoft 365 identities.":::
  
3. Select **Okay** to confirm your choice. 

   The Security Settings page shows the **Enforce Microsoft 365 identity in Yammer** checkbox cleared.

4. Choose **Save** to save your settings.
    
## Frequently asked questions

<a name="FAQ"> </a>

#### Once Microsoft 365 Identity Enforcement is set to **Committed Enforcement**, can I revert it?

> [!IMPORTANT]
> At this point, reverting the **Enforce Microsoft 365 Identity** setting disrupts the user experience, because users who sign in with their user names and passwords can't access their connected resources. **We do not recommend reverting this setting**.

When an organization commits to Microsoft 365 identity enforcement, with one Microsoft 365 tenant tied to a single Viva Engage tenant, the network enables *connected communities*. This configuration creates a Viva Engage community associated with a connected Microsoft 365 community. People in the tenant can take advantage of community software tools such as SharePoint, Planner, and OneNote. 
  
#### How does this change affect guest and external users?

The identity enforcement doesn't affect guests and external users, who continue to follow the sign-in settings and requirements of their home network.

#### How long does it take for this setting to be applied?

Enforcement of Microsoft 365 identity applies immediately after you enable the setting.

#### We use the same Active Directory Federated Services (ADFS) configuration in Viva Engage and Microsoft 365. Should we sign out users during the transition?

Yes. The collective sign out ensures all users who sign back on after the transition just reconnect to their Microsoft 365 identity. Microsoft 365 identity connects users to lifecycle management from Microsoft 365. Users get a consistent experience, with more tools like Microsoft 365 suite navigation.

#### What is the user sign out experience when I enforce Microsoft 365 identities?

Users receive an immediate sign out of their web and mobile sessions. All users just sign back in again with their Microsoft 365 identity credentials. They also get restored access to all their apps, devices, and browser sessions.
  
#### How do I audit and clean up Viva Engage users when compared to Microsoft 365 and Microsoft Entra ID?

You can audit Viva Engage users in any of your Microsoft 365-connected networks and take appropriate action. See more information and examples in [How to audit Viva Engage users in networks connected to Microsoft 365](../manage-viva-engage-users/audit-users-connected-to-office-365.md).
