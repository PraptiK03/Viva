---
title: Use Viva Glint's People feature 
description: The People page on the dashboard allows admins to view employee attributes, manage permissions, roles, and status."
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Employee Attribute File, data file, derived attributes, optional attributes, hierarchy groups, All People functionality, User Roles functionality
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/25/2025
---

# Use Viva Glint's People feature 

The People page functionality allows admins to view employee attributes, manage permissions and roles, and deactivate employees. 

The  **People** section is accessed from the **Employees** section on the admin dashboard and allows admins to: 

- View individual employee data  
- Manage positions by assigning User Roles 
- Manage employment status 
- Import an employee file 
- Export a file of active employees

 :::image type="content" source="../../media/glint/setup/people-tile.png" alt-text="Screenshot of the People tile on the admin dashboard.":::

## Use the All People functionality

A count of present and past employees, listed by: 

- **Active:** People working within your organization presently. 
- **Inactive:** People no longer in your organization. They may also be on leave.
- **Support Users:** Outside users added by your organization to provide assistance.
- **Advanced Configuration Access:** Company Admin users with access to Advanced Configuration

## Use the User Roles functionality

A count of company admins, managers, Human Resource Business Partners (HRBPs), and HR business partners listed by User Roles. Select the role to view only employees in that position.

:::image type="content" source="../../media/glint/setup/people-functionality.png" alt-text="Screenshot of the All People and User Roles column on the People feature.":::

## Other functionality

:::image type="content" source="../../media/glint/setup/people-additional-functionality.png" alt-text="Screenshot of the import, export, and actions buttons on the People feature.":::

### Use the Import feature

To import into Glint, choose the attribute dataset. Follow the in-platform guidance for one of these three options to complete your report:
- Attribute update
- Edit employee list and details
- Employee ID updates

:::image type="content" source="../../media/glint/setup/people-import.png" alt-text="Screenshot of the import functionality on the People feature.":::

#### Attribute updates

Choose the **Attribute update** tile to update your existing schema with new attributes. Follow the in-platform 5-step guidance.

:::image type="content" source="../../media/glint/setup/people-5-step-import.png" alt-text="Screenshot of the 5-step data import process.":::

#### Edit employee list and details

To add new users or to modify employee records in bulk, upload full or incremental employee data files. Use CSV or XLSX format. Employee information isn't altered during a live survey.

:::image type="content" source="../../media/glint/setup/people-import-bulk.png" alt-text="Screenshot of the Import employee list and details dialog box.":::

#### Import employee ID updates

Upload your data file in a CSV or XLSx format. Follow the guidelines for column headers.

:::image type="content" source="../../media/glint/setup/people-id-updates.png" alt-text="Screenshot of the Import employee ID updates dialog box.":::

### Use the Export feature

Select the employee list to export from the **All People** or **User Roles** column. In this example, we chose **Company Admin.** A dialog box opens, allowing you to chose how you would like your export formatted. Toggle as desired and then select **Export.**

:::image type="content" source="../../media/glint/setup/people-export.png" alt-text="Screenshot of the Export Company Admin dialog box.":::

### Use the Actions menu

The dropdown menu makes these two features available:

- Manager user attributes
- Add a support user

#### Manage user attributes

Your **Employee data file** opens, showing the current attributes that Glint expects in your Employee Attribute File. Rename as needed. You can also view derived attributes, optional system attributes, and hierarchy groups.

To add new attributes, upload a new data file by navigating to **Settings** > **People** > **Import** > **Attribute updates**

:::image type="content" source="../../media/glint/setup/people-data-file.png" alt-text="Screenshot of the Employee Data File window.":::

##### Manage Active Attributes

Derived attributes are fields calculated from specific attributes shared with Glint. They appear as available filters in your reports.

Use the ellipses in the **User Attribute** row to select **Edit attribute**. In the **Edit Attribute** dialog box, update the attribute name and manage who can see reporting for this attribute. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-edit-attribute.png" alt-text="Screenshot of the Edit Attribute dialog box.":::

##### Manage Derived Attributes

Select the **Manage derived attributes** button to select which derived attributes are available as filters in your reports. **Save changes.**

:::image type="content" source="../../media/glint/setup/people-derived-attributes.png" alt-text="Screenshot of the live Derived Attributes window.":::

##### Manage Optional System Attributes

Optional system attributes are fields which can be mapped to a time zone, language, or personal email shared with Glint.

Select the **Manage optional system attributes** button to select which optional attributes are available as filters in your reports. **Save changes.**

###### Manage Hierarchy Groups

A hierarchy filters an employee's attributes into levels from highest to lowest, or largest to smallest. The filter provides precise insights into a survey. Define a location hierarchy, such as Region > Country > City, or a department hierarchy, such as Business unit > Department > Team. You can also create a custom hierarchy. 

**Hierarchy groups can only be created during initial schema setup.**

## Other resource

[Find information on a specific person using the People feature](/viva/glint/setup/viewing-employee-info).








