---
title: Assign Viva Glint Tenant and Service Administrators
description: After setting up a Microsoft Viva Glint tenant as a Microsoft 365 Global Administrator, assign Viva Glint Tenant Administrators.
ms.author: judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: assign viva glint admins, viva glint tenant admin, viva glint admin, microsoft 365 global admin
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/11/2025
---

# Assign Viva Glint Tenant and Service Administrators

After setting up a [Microsoft Viva Glint tenant](viva-glint-tenant-provision.md) as a Microsoft 365 Global Administrator, assign Viva Glint Tenant Administrators. Tenant admins manage Viva Glint settings in the Microsoft 365 admin center and assign Viva Glint Administrators who manage the Viva Glint app. [Learn more about key Viva Glint roles](/viva/glint/start/role-definitions).

## Assign Viva Glint Tenant Admins

To assign Viva Glint Tenant Admins as the Microsoft 365 Global Admin:

1. Log in to the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/?linkid=2264234) with your admin credentials. 
2. Go to the **Users** section and select **Roles** in the menu on the left.
3. Search for "Viva Glint Tenant Administrator" in the list of available roles. 
4. Select the role and choose **Assign.** Choose the users or groups you want to assign the role to and confirm your selection. 

## Assign Viva Glint Service Admins

To assign Viva Glint Service Admins as the Viva Glint Tenant Admin:

> [!IMPORTANT]
> If your organization migrates from LinkedIn Glint, your Viva Glint Tenant admin doesn’t need to assign Viva Glint service admins in the admin center. Admin users are migrated as part of your technical migration to Microsoft Viva Glint.

1. Ensure that all Viva Glint Service Admin users have their First Name, Last Name, Employee ID, and Email populated in Microsoft Entra. [Manage Entra user profile information](/entra/fundamentals/how-to-manage-user-profile-info).

   > [!IMPORTANT]
   > To prevent duplication errors with future file uploads, ensure that the Employee ID values for these users match the Employee ID from the HR Information System (HRIS) that's used to transfer data to Viva Glint.

1. Sign in to the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/?linkid=2264234). 
1. Go to **Settings** and select **Viva**.
2. In the list of applications, select **Viva Glint**.
3. Select **Assign Glint service admin** and choose **Add users**.
4. Search for and select service admin users.
5. Select **Add** to assign users.
6. Newly assigned users appear in the Viva Glint application in the Company Admin role within minutes.
7. Newly assigned users receive an email notification:

   :::image type="content" source="../../media/glint/setup/service-admin-email.png" alt-text="Screenshot of the email notification that Viva Glint service admins receive when they're added to the admin role.":::
   

> [!CAUTION]
> Don't assign Support users to the Company Admin role in the Microsoft 365 admin center. To add Support users, see: [Manage Support users in Viva Glint](add-external-user.md).

## Manage Viva Glint service admins in the Viva Glint app

Viva Glint service admins can assign and unassign users to the Company Admin role in the Viva Glint application. 

In the Viva Glint app:

1. Go to **Configuration** and select **People**.
2. Search for and select a user.
3. On the user's profile, select the pencil icon to edit **User Roles**.
4. Select or deselect **Company Admin** to add or remove a user from the role.
5. Select **Save**.

## What do I do if I need help?

[Get support from Microsoft 365](/viva/troubleshoot/glint/contact-support/get-support-viva-glint?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)


