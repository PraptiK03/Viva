---
title:  Manage Support users in Viva Glint
description: Grant access to Viva Glint Support users to help in deployment, advanced insights analysis, and complex Support tasks.
ms.author: aweixelman
author: AliciaWeixelman
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: External user, partner, support, add user
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/04/2025
---

# Manage Support users in Viva Glint

The Support User role is designed to grant the right permissions to guests, like Microsoft Partners, and allow Microsoft Viva Glint Administrators to quickly audit how many Support users have access to their Viva Glint application. Support users can help with deployment, advanced insights analysis, and complex support tasks. 

> [!IMPORTANT]
> - Support users can exist in Microsoft Entra ID with a member type of Guest or Member with a company email address for your organization that matches the email for their profile in the Viva Glint platform. [Learn more about how Support users sign in to Viva Glint](#sign-in-as-a-support-user)
> - Support users require an Entra license but don't count toward your organization's Viva Glint licenses.
> - Support users shouldn't be included in your employee data file uploaded to Viva Glint.

## Add a Support user

> [!CAUTION]
> Don't add support users to the Viva Glint Company Admin role by [assigning them in the Microsoft 365 admin center](post-provisioning-next-steps.md). Users aren't able to successfully log in to Viva Glint.

To add a user:

1. From the admin dashboard, select the **Configuration** symbol, then in **Employees**, choose **People**.
2. In the **Actions** dropdown menu, select **Add a Support User**.
3. Enter the First Name, Last Name, and Email on file in Microsoft Entra ID for this user.  
4. The **Company Admin User Role** is selected by default and grants Support users the required level of access to help in your Viva Glint account.

    > [!IMPORTANT]
    > Support users in Viva Glint don't have all export/import abilities.

5. Switch the **External user** toggle to **Yes** to flag guests in Viva Glint.
6. Switch the **Grant user advanced configuration access** setting to **Yes** to allow Support users access to **Advanced Configuration** features.
  
   > [!IMPORTANT]
   > Users with access to Advanced Configuration settings can make changes to potentially sensitive areas of
   > your Viva Glint configuration. For an Advanced Configuration overview, see [Understand Advanced
   > Configuration options in Viva Glint.](understand-advanced-configuration.md)

7. Select **Add support user.**

## Sign in as a Support user

Support users need to take these steps to access Viva Glint with member types of "Guest" in Entra.

1. Select the appropriate link for the organization's region:
   - US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
   - EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)
2. Select **Sign-in options** in the **Sign in** dialog.
3. Select **Sign in to an organization.**
4. Enter the **domain name**, for example: `contoso.onmicrosoft.com`, of the organization you'd like to sign in to and select **Next**.
5. Enter your email and password, select **Sign in**, and follow other sign-on prompts (for example: multifactor authentication).

> [!TIP]
> To prevent sign-in issues, try accessing Viva Glint in a new InPrivate or Incognito window.

## Remove a Support user

When a Support user no longer needs access to your Viva Glint account:

1. From the admin dashboard, select the **Configuration** symbol, then in **Employees**, choose **People**.
2. In the **Search People** field, enter the first and last name or email address of the user.
3. In the search results, select the desired user.
4. On the user's profile, select **Actions** and then **Delete User**.
5. In the dialog, select **Delete User.**

   > [!IMPORTANT]
   > This action is irreversible.
