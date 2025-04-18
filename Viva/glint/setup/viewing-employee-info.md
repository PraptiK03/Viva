---
title: Use Viva Glint's People page to view employee information
description: Use the People functionality to view and manage specific access for people in your organization.
author: JudyWeiner
ms.author: JudithWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/25/2025
---

# Use Viva Glint's People page to view employee information

To find and view information about a specific person, from the admin dashboard, select the **People** tile. 

Use one of the two following methods: 

- Begin to type the name of the employee in the search bar. When the name appears as a dropdown, select the name.   
- Scroll down the alphabetized list of names. With hundreds or thousands of employees, this method isn't as efficient! 

For each employee, the following information is visible: 

- **Employee Name**: Editable by admin by selecting the pencil symbol. 
- **Email**: Editable by admin by selecting the pencil symbol.
- **Manager Reports**
- **Team**

This example is a small snapshot of a fictitious employee's People page:

:::image type="content" source="../../media/glint/setup/people-header-row.png" alt-text="Screenshot of fictitious employee People page.":::

## Manage other employee information available

For employees with extended roles, other sections are visible. They may include:

### User Roles

View and manage what data and people a user has access to. This section is editable by selecting the **pencil symbol**. The **Customize User Role** dialog box opens. To add a User Role to a profile, select from the list that appears in the dialog box. Changes made override any previous role exclusions. Select **Save.**

**KRISTI - I DON'T KNOW THE ANSWER TO WHY OME ROLES ARE NOT SELECTABLE. WHAT ARE YOU TRYING TO GET AT?**

:::image type="content" source="../../media/glint/setup/people-customize-role.png" alt-text="Screenshot of the Customize User Role dialog box in the People feature.":::

### Company Admin: Advanced Configuration Access

[Advanced Configuration settings] (/../../viva/glint/setup/understand-advanced-configuration)are used to help manage your account. They're available for company admins and support roles. This setting must be on for Advanced Support users. This section is editable by selecting the **pencil symbol**. The **Advanced Configuration access** dialog box opens. Toggle to enable. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-advanced-config-access.png" alt-text="Screenshot of the Advanced Configuration Access dialog box in the People feature.":::

### Admin Access

Defines which people the user can manage. This section is editable by selecting the **pencil symbol**. The **Customize Admin Access** dialog box opens. Select **+ New Population** to add new groups and filters for this user. Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-customize-admin.png" alt-text="Screenshot of the Customize Admin Access dialog box in the People feature.":::

### Focus Area Access

Defines which people's data this use can see in Focus Area reports. This section is editable by selecting the **pencil symbol**. The **Customize Focus Area Access** dialog box opens. Select **+ New Population** to add new groups and filters for this user.  Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-custom-focus-area.png" alt-text="Screenshot of the Customize Focus Area Access dialog box in the People feature.":::

### Survey Access

This person's survey access appears by individual survey cycle name. This section is editable by selecting the **pencil symbol**. The **Customize Survey Data Access** dialog box opens. Select **+ New Population** to add new groups and filters for this user.  Changes made override defaults. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-survey-access.png" alt-text="Screenshot of the Customize Survey Data Access dialog box in the People feature.":::

>[!CAUTION]
> Microsoft rules govern viewing and exporting raw data to protecting employee confidentiality. Review [raw data exports](https://go.microsoft.com/fwlink/?linkid=2239587) within our Security and Privacy documents.

## View attributes

In the Attributes section, attributes show for this user as defined in your latest Employee Attribute File upload.

### Hierarchy attributes

- **Location hierarchy**
- **Manager hierarchy:** The organization’s highest-ranking employee (generally the CEO) is listed first. The hierarchy progresses downward, following the organizational chart flow, ending with the employee’s immediate manager. Not editable. 
- **Old Manager hierarchy**, if it exists

### Standard attributes

Your organization may not use all of these attributes and may also refer to the attributes using other terminology. Whichever attributes you sent to Glint show here. These attributes are common examples of Standards attributes:
- **Manager email**
- **Employee ID**: Editable. [Learn how here](/../../viva/glint/setup/people-page).
- **Sub-Department**
- **Department**
- **Start Date**
- **Hire Date**
- **Level**
- **Tenures** 

## Use the View As function 

The **View As** functionality allows you to open your Glint program as if you were another employee. You can view another user’s dashboard based on their User Role and data access.

**To view as another person**: 
1. Locate the person you want to View As using the Search box. To open their page, select their name. 
1. Select **View As**. 
1. The dashboard indicates **You are seeing `<name>`'s Viva Glint experience.**

To return to your own account, select **Return to your account**. 

:::image type="content" source="../../media/glint/setup/people-view-as.png" alt-text="Screenshot of the View As functionality in the People feature.":::

## Use the Actions menu

The Actions button dropdown menu allows you to send surveys, send user data, and delete users. 

### Send Survey 

Send a survey to one employee (manually) from the People page. In the Actions button, select **Send Survey**. Enabled and live surveys are displayed. Select the survey to send from the surveys available in the dropdown menu. Select **Send**. 

>[!IMPORTANT]
>Send a survey manually when an employee wasn't part of the Distribution List for that survey during the initial send.
>
>A Distribution List continually updates when you send an Employee Attribute File to Glint. Any employee who becomes eligible for a survey after its initial send requires a manual invite. Add them to the Distribution List after, and upload the new Employee Attribute File to Glint.

> [!NOTE]
> Surveys only show when enabled or live. Go back into the program to re-enable or change the date of the survey. It takes a few minutes for a survey to become live.

### Send User Data

In the Actions button, select **Send User Data**. To fulfill a Data Send Request (DSR) request from an employee, enter their personal email address. Choose the attributes to export and then select **Send.** An encrypted data export is generated and downloaded to your chosen location. If the provided email address is valid, a one-time password is emailed to the requestor, granting access to the encrypted data file. After downloading the data file, securely share it with the requestor through your preferred secure communication channel.

:::image type="content" source="../../media/glint/setup/people-send-user-data.png" alt-text="Screenshot of the Send User Data dialog box in the People feature.":::

### Delete User

When an admin deletes an employee, their data is removed from Viva Glint. This deletion excludes essential account information associated with your organization’s Microsoft 365 subscription.

By deleting this user, you also remove:
- Their role definitions and ability to manage your client
- Their ability to sign in to your company’s Viva Glint client
  
:::image type="content" source="../../media/glint/setup/people-delete-user.png" alt-text="Screenshot of the Delete Support User dialog box in the People feature.":::



