---
title: Use the Viva Glint Employee Attribute Template
description: Learn how Viva Glint uses the attributes and hierarchies you provide about the people in your organization to surface meaningful and actionable insights. The template is the row of column headers; all the data you provide.
ms.author: aweixelman
author: AliciaWeixelman
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: HRIS planning tool, upload data, data file, header row, required attributes, custom attributes
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/08/2025
---

# Use the Viva Glint Employee Attribute Template

The Employee Attribute Template is a planning tool Viva Glint Administrators use to document an organization’s file format and attribute selections, before uploading employee data to the Microsoft Viva Glint platform. Use the template to document decisions that you and other data stakeholders make as you [meet and prepare to upload employee data](upload-employee-data.md).

> [!div class="nextstepaction"]
> [Download the Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533) 

## Why use the Employee Attribute Template? 

Every report, recommendation, and action plan that Viva Glint presents for your organization relies on the foundation of employee data that you provide. The collection of detailed information about the people in your organization is essential to highlight meaningful insights from survey results and determine what you're doing right and where your opportunities lie.

## Fill in the template

The first page of the attribute template contains instructions for documenting information in the file and Viva Glint data requirements. Follow the guidance on the instruction page and in the [terminology table](#employee-attribute-template-terminology) to structure your data and make data decisions.

Viva Glint supports these file formats for data your organization uploads to the platform:

- .csv for files with a comma delimiter and UTF-8 encoding
  - Viva Glint accepts UTF-8 and UTF-8 with BOM encoding
- .xlsx for files in Microsoft Excel format with a single tab of data

### Employee Attribute Template terminology

| Term | Definition |
|---|---|
| **Employee Attribute Template** | Guidance in the form of a downloadable workbook for documenting your organization’s file format and data selections, before setting up attributes in Viva Glint. |
| **Attributes** | Demographic details about employees that become report filters in the platform. |
| **Attribute Header Row** | The blueprint for columns of data and the labels for the columns. |
| **Required Attribute** | Information about each employee in your organization that Viva Glint requires:<li>Status: ACTIVE or INACTIVE <li>First name <li>Last name <li>Email address <li>Employee ID |
| **Custom Attribute** | Any employee information collected in addition to required attributes. <br>Your organization can send up to 100 custom attributes. Examples: gender, work location, department. |
| **Flat Attribute** | A category that can't be broken down further, such as age group or gender. |
| **Optional System Attribute** | A value that indicates how and when Viva Glint sends communications to an employee, such as language* and time zone. |
| **Hierarchy** | Filtering down of an employee attribute into levels from highest to lowest, largest to smallest, to provide more precise insights.  <br>Example: Region > Country > State > City |
| **Derivation** | Fields calculated based on employee attributes. <p>Examples: Age groups based on birth year or tenure based on hire date. |
| **Schema** | The framework in our platform that stores a mapping of your organization’s attributes. |

> [!IMPORTANT]
> \* See [Recent language changes](attribute-fundamentals.md#recent-language-changes) for changes to supported languages and codes effective April 10, 2025.

## Next step
After finalizing your attribute selections, reporting hierarchies, and file and date attribute formats, review your employee data with a Viva Glint checklist.

> [!div class="nextstepaction"]
> [Review your data with a checklist](data-checklist.md)
