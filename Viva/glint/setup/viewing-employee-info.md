---
title: Use Viva Glint's People page to view employee information
description: Use the People functionality to view and manage specific access for people in your organization.
author: JudyWeiner
ms.author: JudithWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: user profile, view roles, edit ID
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/23/2025
---

# Use Viva Glint's People page to view employee information

To find and view information about a specific person in Microsoft Viva Glint, from the admin dashboard, select the **People** tile. 

To search for a user, type the name, email address, or ID of the employee in the search bar. When the name appears, select the name to view their profile.   

For each employee, the following information is visible: 

- **Employee Name**: Editable by admin by selecting the pencil symbol. 
- **Email**: Editable by admin by selecting the pencil symbol.
- **Employee ID**: Editable by admin by selecting the pencil symbol.
- **Current Manager Hierarchy**

This example is a snapshot of an employee's detail page:

:::image type="content" source="../../media/glint/setup/people-header-row2.png" alt-text="Screenshot of fictitious employee People page.":::

## Use the View As function 

The **View As** functionality allows you to open Viva Glint dashboard and reports as if you were another user based on their User Role and data access.

**To view as another person**: 

1. Locate the person you want to View As using the Search box. To open their page, select their name. 
1. Select **View As**. 
1. The dashboard indicates **You are seeing `<name>`'s Viva Glint experience.**

To return to your own account, select **Return to your account**. 

:::image type="content" source="../../media/glint/setup/people-view-as.png" alt-text="Screenshot of the View As functionality in the People feature.":::

## Use the Actions menu

The Actions button dropdown menu allows you to send surveys, send user data, and delete users. 

### Send Survey 

Send a survey to an employee (manually) from their profile. In the Actions menu, select **Send Survey**. Enabled and live surveys are displayed. Select the survey to send from the surveys available in the dropdown menu. Select **Send**. 

> [!IMPORTANT]
> Send a survey manually when an employee wasn't part of the Distribution List for that survey during the initial send.
>
> Distribution Lists continually update as you send new employee data to Viva Glint. Any employee who becomes eligible for a survey after its initial send requires a manual invite.

> [!NOTE]
> Surveys only show when enabled or live.

### Send User Data

In the Actions menu, select **Send User Data**. To fulfill a Data Send Request (DSR) request from an employee, enter their personal email address. Choose the attributes to export and then select **Send.** [Learn more about sending data to users](raw-data-request-response.md#use-the-people-feature-to-export-responses).

:::image type="content" source="../../media/glint/setup/people-send-user-data.png" alt-text="Screenshot of the Send User Data dialog box in the People feature.":::

### Delete User

When an admin [deletes an employee](raw-data-request-response.md#delete-user-data), their data is removed from Viva Glint. This deletion excludes essential account information associated with your organization’s Microsoft 365 subscription.

By deleting this user, you also remove:

- Their role definitions and ability to manage your client
- Their ability to sign in to your company’s Viva Glint client
  
:::image type="content" source="../../media/glint/setup/people-delete-user.png" alt-text="Screenshot of the Delete Support User dialog box in the People feature.":::

## User Roles

View and manage what data and people a user has access to. This section is editable by selecting the **pencil symbol**. The **Customize User Role** dialog opens. To add a User Role to a profile, select from the list that appears in the dialog. Changes made override any previous role exclusions. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-customize-role2.png" alt-text="Screenshot of the Customize User Role dialog box in the People feature.":::

## Company Admin: Advanced Configuration Access

[Advanced Configuration settings](/../../viva/glint/setup/understand-advanced-configuration) are used to help manage your account and are available for users in the Company Admin role. This setting must be on for Advanced Support users. This section is editable by selecting the **pencil symbol**. The **Advanced Configuration access** dialog opens. Toggle to enable. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-advanced-config-access.png" alt-text="Screenshot of the Advanced Configuration Access dialog box in the People feature.":::

## Admin Access

Admin access defines which people the user can manage. This section is editable by selecting the **pencil symbol**. The **Customize Admin Access** dialog opens. Select **+ New Population** to add new groups and filters for this user. Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-customize-admin2.png" alt-text="Screenshot of the Customize Admin Access dialog box in the People feature.":::

## Focus Area Access

Focus Area access defines which people's data this user can see in Focus Area reports. This section is editable by selecting the **pencil symbol**. The **Customize Focus Area Access** dialog opens. Select **+ New Population** to add new groups and filters for this user. Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-custom-focus-area.png" alt-text="Screenshot of the Customize Focus Area Access dialog box in the People feature.":::

## Survey Access

This person's survey access appears by individual survey name. This section is editable by selecting the **pencil symbol**. The **Customize Survey Data Access** dialog opens. Select **+ New Population** to add new groups and filters for this user. Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-survey-access.png" alt-text="Screenshot of the Customize Survey Data Access dialog box in the People feature.":::

> [!CAUTION]
> Microsoft rules govern viewing and exporting raw data to protect employee confidentiality. Review [raw data exports](employee-raw-data-export.md) within our Security and Privacy documents.

> [!NOTE]
> For more information on granting custom access or granting custom access in bulk, see:
> - [User Roles with custom data access in Viva Glint](custom-user-role.md)
> - [Custom data access in Viva Glint](custom-access.md)

## Attributes

In the Attributes section, attributes show for this user as defined in your latest employee data upload. This section includes:

- **Hierarchies**: A list of each hierarchy group and the values for each hierarchy level for this user.
- **Standard attributes**: A list of visible custom attributes for this user, like Hire Date or Department.

> [!NOTE]
> When custom attributes have [their Visibility set to Off](update-attributes.md#update-custom-attribute-visibility), data doesn't appear on a user's profile.

## Survey programs

This section lists all of a user's current and past survey programs that they're invited to. To view a list of specific survey cycles, expand each survey program with the right-facing arrow.



