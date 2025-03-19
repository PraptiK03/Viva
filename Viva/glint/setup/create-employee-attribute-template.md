---
title: Create your Viva Glint Employee Attribute Template
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
ms.date: 03/10/2025
---

# Create your Viva Glint Employee Attribute Template

The Employee Attribute Template is a planning tool Viva Glint Administrators use to document an organization’s file format and attribute selections, before uploading your employee data to the Microsoft Viva Glint system.

Ensure that attribute labels that you set up initially stay consistent over time in the data files transferred to Viva Glint. For example, if your organization sets up **Employee ID**, it can't later be recognized as the same column renamed as **Employee Number**.

> Use Viva Glint's **[Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533)** as guidance to ensure that data is uploaded in the correct format, incorporating our recommendations and requirements.

> [!IMPORTANT]
> See [Upcoming language changes](attribute-fundamentals.md#upcoming-language-changes) for changes to supported languages and codes effective April 10, 2025.

## Why is creating an employee data template important? 

Every report, recommendation, and action plan that Viva Glint presents for your organization relies on the foundation of employee data that you provide. The collection of detailed information about the people in your organization is essential, so we can use cuts of that data to highlight meaningful insights from survey results. In doing that, Viva Glint helps you to determine what you're doing right and where your opportunities lie.

A successful process means that you first need to: 

- Understand the definitions and why we ask for attributes and hierarchies
- Use the Employee Attribute Template to format and create your data file
- Understand how to set up and upload your data to Viva Glint

### Use your IT department for support

Many companies rely on their IT department to stage and maintain the backend processes that power Viva Glint programs. Your IT department may be the best internal expert when it comes to certain data preparation tasks.

## Create the template

Viva Glint supports these file formats for data your organization uploads to the platform:

- .csv for files with a comma delimiter and UTF-8 encoding
  - Viva Glint accepts UTF-8 and UTF-8 with BOM encoding
- .xlsx for files in Microsoft Excel format with a single tab of data

The first page of the template contains instructions for building your own template. Follow the guidance on the instruction page and in the following table to set up your template.

### Definitions for Employee Attribute Template

| Term | Definition |
|---|---|
| **Employee Attribute Template** | Guidance in the form of a downloadable workbook for documenting your organization’s file format and data selections, before setting up attributes in Viva Glint. |
| **Attributes** | Demographic details about employees that become report filters in the platform. |
| **Attribute Header Row** | The blueprint for the the columns of data and the labels for the columns. |
| **Required Attribute** | Information about each employee in your organization that Viva Glint requires:<li>Status: ACTIVE or INACTIVE <li>First name <li>Last name <li>Email address <li>Employee ID |
| **Custom Attribute** | Any employee information collected in addition to required attributes. <br>Your organization can send up to 100 custom attributes. Examples: gender, work location, department. |
| **Flat Attribute** | A category that can't be broken down further, such as age group or gender. |
| **Optional System Attribute** | A value that indicates how and when Viva Glint sends communications to an employee, such as language and time zone. |
| **Hierarchy** | Filtering down of an employee attribute into levels from highest to lowest, largest to smallest, to provide more precise insights.  <br>Example: Region > Country > State > City |
| **Derivation** | Fields calculated based on employee attributes. <p>Examples: Age groups based on birth year or tenure based on hire date. |
| **Schema** | The framework in our platform that stores a mapping of your organization’s attributes. |

## Next step
After finalizing your attribute selections, reporting hierarchies, and file and date attribute formats, review your employee data with a Viva Glint checklist.

> [!div class="nextstepaction"]
> [Review your data with a checklist](data-checklist.md)
