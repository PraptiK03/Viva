---
title: Set up Viva Glint for a multitenant organization
description: Multitenant organization (MTO) is a Microsoft 365 feature that enables you to form a tenant group within your organization.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: MTO, multitenant organization, B2B collaboration, cross-tenant sync, FAQ
ms.collection:  
- Microsoft 365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/14/2025
---

# Set up Viva Glint for a multitenant organization

Multitenant organization (MTO) is a Microsoft 365 feature that enables your company to form a tenant group in your organization. MTO allows users in a tenant group to access an instance of Microsoft Viva Glint installed in only one tenant. Viva Glint Administrators can survey and grant report access to employees across the tenant group for an organization-wide view of employee sentiment. Use the guidance in this article to learn more about multitenant organization setup, syncing users between tenants, and ensuring all users exist in the Viva Glint application. [Learn more about MTO](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview).

#### Terminology

- **Target tenant:** The tenant where Viva Glint is installed and where the Microsoft 365 global admin sets up an MTO policy. 
- **Source tenant:** Any other tenants with users that access Viva Glint in the target tenant.

> [!NOTE]
> [Allowlist updates](allowed-list.md) only need to be made to target tenants where the Viva Glint app is installed.

### Get started

Select a step to jump to instructions for a specific part of multitenant organization setup for Viva Glint. 

|:::image type="icon" source="/office/media/icons/task-list-planning-blue.png" ::: |[Plan for MTO](#plan-for-mto)| :::image type="icon" source="/office/media/icons/administrator.png" ::: |[Set up MTO](#set-up-mto)| :::image type="icon" source="/office/media/icons/migration-blue.png" ::: |[Sync users](#sync-users) |:::image type="icon" source="/office/media/icons/users-people.png" ::: |[Import users from all tenants to the Viva Glint app](#import-users-from-all-tenants-to-the-viva-glint-app) |
|:---|:---|:---|:---|:---|:---|:---|:---|

### Plan for MTO

Meet internally with your MTO stakeholders, review requirements, and consider Viva Glint survey access methods to plan for your MTO setup.

| :::image type="icon" source="/office/media/icons/task-list-planning-blue.png" ::: |Step<br> <br> _roles involved_| More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/meeting.png" ::: | **Meet with stakeholders** <br> <br>_Microsoft 365 global admin_ <br> <br>_Viva Glint admin_ <br> <br>_IT team members_ <br> <br>_Viva Glint project team members_| Determine:<br> <br> <ul><li>How many tenants your organization uses</li> <li>Whether employees exist in different tenants</li> <li>What your Viva Glint survey needs are across different tenants and employee populations</li> <li>How you currently use Viva Glint for organization-wide surveys</li></ul>|
| :::image type="icon" source="/office/media/icons/compliance-blue.png" ::: | **Review requirements** <br> <br>_Microsoft 365 global admin_ | <ul><li>All tenants exist in the same cloud</li><li>All tenants use Microsoft Entra ID </li><li>Viva Glint is installed in one tenant where all Viva Glint licenses used in the MTO are purchased (regardless of the home tenant of the user)</li> <li>[Target and source tenant prerequisites](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#prerequisites)</li><li>[License requirements](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview#license-requirements)<li>[Learn about MTO limitations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues)</li> </ul>|
|:::image type="icon" source="/office/media/icons/users-settings.png" ::: | **Determine survey access methods and users to sync** <br> <br>_Viva Glint admin_ <br> <br>_Viva Glint project team_ | <ul><li>**Authentication with Microsoft Entra ID**<br> _Survey takers must exist in Entra and in the Viva Glint app_ <br></li> <li>**Personalized links**<br> _Survey takers need to exist in the Viva Glint app only_ <br></li> <li>**Attribute-based survey access**<br> _Survey takers need to exist in the Viva Glint app only_</li> <li>[Learn more about Viva Glint survey access methods](/viva/glint/setup/understand-survey-access-methods)</li></ul><br> **All users that access survey results must exist in Entra**|

> [!TIP]
> See [Viva Glint for a multitenant organization FAQ](mto-faq.md) for answers to commonly asked MTO, cross-tenant sync, and B2B collaboration questions.

### Set up MTO

Microsoft 365 global admins can set up MTO in the Microsoft 365 admin center or using the Microsoft Graph API. Setup in the Microsoft 365 admin center offers a user-friendly experience with simple and quick configuration steps. Microsoft Graph API configuration gives admins more granular control and advanced customization and automation options. Consider your organization’s level of complexity across tenants when choosing an MTO setup method.

> [!TIP]
> MTO setup in the Microsoft 365 admin center is recommended and is the most commonly used setup method.

> [!IMPORTANT]
> If your organization already uses B2B collaboration or cross-tenant synchronization to sync users, an MTO setup is still required. MTO and (an included MTO policy) identifies trusted domains and tenants.

| :::image type="icon" source="/office/media/icons/administrator.png" ::: |Step <br> <br> _roles involved_ | More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/api.png" ::: | **Option 1: Set up MTO in the Microsoft 365 admin center** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>[As the target tenant admin, set up a new MTO in the Microsoft 365 admin center](/microsoft-365/enterprise/set-up-multi-tenant-org#set-up-a-new-multitenant-organization)</li> <li>[As the target tenant admin, add tenants to your MTO in the Microsoft 365 admin center](/microsoft-365/enterprise/set-up-multi-tenant-org#add-a-tenant-to-your-multitenant-organization)</li> <li>[As a source tenant admin, join an MTO](/microsoft-365/enterprise/join-leave-multi-tenant-org#join-an-existing-multitenant-organization)</li></ol>|
|:::image type="icon" source="/office/media/icons/api.png" ::: | **Option 2: Set up MTO with the Microsoft Graph API** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>As the target tenant admin, [sign in to the target tenant](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#step-1-sign-in-to-the-owner-tenant) and [create an MTO](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#step-2-create-a-multitenant-organization)</li> <li> [As the target tenant admin, add tenants to the MTO](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#step-3-add-tenants)</li><li> As the source tenant admin, [sign in to the source tenant](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#step-6-sign-in-to-a-member-tenant) and [join the MTO](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph#step-7-join-the-multitenant-organization)</li><li> As the target tenant admin, [setup a cross-tenant access policy](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-templates#cross-tenant-access-policy-partner-template) and [configure inbound user sync](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-templates#cross-tenant-synchronization-template)</li></ul>|


### Sync users

There are two options to sync users for MTO and Viva Glint: B2B collaboration or cross-tenant synchronization. Both options result in the creation of [B2B collaboration users](/entra/external-id/user-properties). Cross-tenant synchronization automatically updates users and removes them when they leave the organization. Review prerequisites for each method:

- [cross-tenant synchronization prerequisites](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#prerequisites)
- [B2B collaboration prerequisites](/entra/external-id/tutorial-bulk-invite#prerequisites)

> [!TIP]
> Cross-tenant synchronization is recommended and offers a more automated and streamlined user sync method.

> [!IMPORTANT]
> - If your organization already has cross-tenant synchronization set up for users that need to access Viva Glint in the target tenant, skip this step.
> - If your organization uses [B2B direct connect](/entra/external-id/b2b-direct-connect-overview), accounts for source tenant users aren't created in the target tenant. Cross-tenant synchronization is still needed to sync users and doesn't affect any existing B2B direct connect setups. 

| :::image type="icon" source="/office/media/icons/migration-blue.png" ::: |Sync option <br> <br> _roles involved_| More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/users-people.png" ::: | **Option 1: cross-tenant synchronization (CTS)** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>As the target tenant admin, [enable CTS in the target tenant](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-2-enable-user-synchronization-in-the-target-tenant)</li> <li>As target tenant admin, [enable autoredemption in the target tenant](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-3-automatically-redeem-invitations-in-the-target-tenant) </li><li>As the source tenant admin, [enable autoredemption in the source tenant](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-4-automatically-redeem-invitations-in-the-source-tenant)</li><li>As the source tenant admin, [set up CTS in the source tenant](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-5-create-a-configuration-in-the-source-tenant) and [test the connection to the target tenant](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-6-test-the-connection-to-the-target-tenant)</li> <li>As the source tenant admin, [define who's in scope for provisioning](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-7-define-who-is-in-scope-for-provisioning) and [test on demand provisioning](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-11-test-provision-on-demand)</li><li>As the source tenant admin, [start the provisioning job](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-12-start-the-provisioning-job) to sync users to the target tenant</li> <li>As target and source tenant admins, [verify users in the target tenant and monitor the provisioning job](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-13-monitor-provisioning)</li></ol>|
|:::image type="icon" source="/office/media/icons/upload-blue.png" ::: | **Option 2: B2B collaboration** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>**Optional:** In the target and source tenants, [confirm that autoredemption is selected in cross-tenant access settings](/entra/external-id/cross-tenant-access-overview#automatic-redemption-setting)</li><li>As the target tenant admin, [prepare a comma-separated value (.csv) file with user information](/entra/external-id/tutorial-bulk-invite#understand-the-csv-template)</li> <li>As the target tenant admin, [upload the file to Microsoft Entra ID](/entra/external-id/tutorial-bulk-invite#invite-guest-users-in-bulk)</li><li>As the target tenant admin, [confirm that users are added to the directory](/entra/external-id/tutorial-bulk-invite#verify-guest-users-in-the-directory)</li></ol>|


### Import users from all tenants to the Viva Glint app

To successfully access surveys and results, all users need to be imported to the Viva Glint application, regardless of their home tenant. Viva Glint offers two methods to import users:

| :::image type="icon" source="/office/media/icons/users-people.png" ::: |Import method <br> <br> _roles involved_| More information|
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/database.png" ::: | **Secure File Transfer Protocol (SFTP)** <br> <br>_Viva Glint admin_ <br> <br>_HR information system team_| <ul><li>[SFTP and data automation](/viva/glint/setup/sftp-data-automation)</li></ul> |
|:::image type="icon" source="/office/media/icons/files-blue.png" ::: | **People page import** <br> <br>_Viva Glint admin_ | <ul><li>[People page import in the Viva Glint platform](/viva/glint/setup/upload-employee-attributes)</li> </ul>|

### Related resources

**Cross-tenant access and multitenant organization**: 

- [Cross-tenant access overview](/entra/external-id/cross-tenant-access-overview), especially the **Important considerations** section.
- [Configure B2B collaboration cross-tenant access](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
- [Enable B2B external collaboration settings](/entra/external-id/external-collaboration-settings-configure).
- [Plan for multitenant organizations in Microsoft 365](/microsoft-365/enterprise/plan-multi-tenant-org-overview)
- [Configure a multitenant organization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph?tabs=ms-powershell)
- [What is a multitenant organization in Microsoft Entra ID?](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview)
- [Manage tenants in your Microsoft Customer Agreement billing account](/azure/cost-management-billing/microsoft-customer-agreement/manage-tenants#whats-a-tenant) 
- [Multitenant organization scenario and Microsoft Entra capabilities](/entra/identity/multi-tenant-organizations/overview)
- [Viva Glint for a multitenant organization FAQ](mto-faq.md)

**B2B collaboration**: 

- [Configure cross-tenant access settings for B2B collaboration](/entra/external-id/cross-tenant-access-settings-b2b-collaboration)
- [Bulk invite guest users for B2B collaboration](/entra/external-id/tutorial-bulk-invite)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)

**Cross-tenant synchronization**: 

- [Configure cross-tenant synchronization](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure) 
- [Configure cross-tenant synchronization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure-graph?tabs=ms-powershell)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)
- [Cross-tenant synchronization licensing](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-overview#license-requirements)
