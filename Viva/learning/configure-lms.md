---
title: Add learning management systems for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 04/06/2025
audience: admin
ms.topic: how-to
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - highpri
ms.localizationpriority: medium
description: Learn how to configure learning management systems as a learning content source for Microsoft Viva Learning.
---

# Add learning management systems for Microsoft Viva Learning

Use Viva Learning to integrate with learning management systems (LMS) and enhance the learning experience of users in your organization. We offer a growing set of LMS and content sources, which change as more providers join or update their status with the program.

You can also use [AI and Copilot content](ai-and-copilot-resources.md) for all Viva Learning users in your org who have Microsoft Copilot licenses. It's enabled by default and can be managed in the Manage Providers section of Viva Learning Admin tab.

This article covers:

- The current LMS offerings
- A summary of the dataflow process
- The data extracted from the LMS as part of the content catalog, assignment records, and completion status. 
- The way users in your org interact with learning content.

For more information on permissions and processes you perform as an admin, read about [managing content sources](content-sources-365-admin-center.md) and [managing providers](use-tabs.md).

> [!NOTE]
> A Viva Learning or Viva Suite license is required to access this feature. [Learn more about licensing](https://www.microsoft.com/microsoft-viva/learning).

> [!NOTE]
> Sources you enable in the Viva Learning admin portal can take 24 to 48 hours before becoming visible to users.

## Learning management systems


Learning management systems aren't enabled by default. To enable these sources, add them to the Viva Learning Admin tab and follow the specific instructions outlined in the accompanying table. 

|Learning management system  |Configuration instructions  |
|---------|---------|
|Cornerstone OnDemand |[Configure Cornerstone OnDemand as a content source](configure-cornerstone-content-source.md)         |
|Saba    |[Configure Saba as a content source](configure-saba-content-source.md)         |
|SAP SuccessFactors   |[Configure SAP SuccessFactors as a content source](sfsf-introduction.md)         |
|Workday | [Configure Workday as a content source](workday-intro.md)|

> [!NOTE]
> Available learning management systems are subject to change. Depending on your organization, you can have access to different learning management systems than are listed here.

You can also learn about [other content sources](configure-other-content-sources.md) we currently offer.

## Dataflow architecture

The dataflow diagram illustrates how Viva Learning uses the LMS connector to ingest the learning content catalog and learner records (assignments and completion status). The learning management system (LMS) is the ultimate source of content and learner records for their customers. Viva Learning extracts the content and learner records from the LMS by the LMS Connector as depicted in the following diagram.

:::image type="content" alt-text="Flow chart depicting the content ingestion process, which is explained in the following paragraph." source="../media/learning/lms-dataflow.png" lightbox="../media/learning/lms-dataflow.png":::

1. **LMS** <br> Viva Learning requires two types of data from every LMS.
   - **Content catalog**: Fields that are extracted as part of the Content Catalog package or API from the LMS. [View the content catalog table](#content-catalog).
   - **Assignment and completion records (learner records sync)**: Fields that are extracted as part of the Assignment & Completion package or API from the LMS. [View the assignment table](#assignment-records). [View the completion table](#completion-status).

1. **LMS Connector** <br> The LMS Connector pulls content from the LMS using both API and SFTP mechanisms. The first time you sync, the LMS extractor pulls the full data. Afterward, a scheduler triggers once every 24 hours to refresh the data and pull any changes. The extract is then validated and processed.
 <br> If you encounter any error in processing, the error code displays on the admin portal. User records received from the extract are mapped with Microsoft Entra ID records to ensure the correct assignment and completion status for every user. Once all the records are processed, the data is synchronized to Viva Learning and displayed in Viva Learning.

1. **Viva Learning** <br> Content details, such as content provider logo, thumbnail, title, and description, display on the **Home** and **Learning** tabs in Viva Learning. <br> The **My learning** tab shows the users' assigned and completed courses fetched from the LMS.

### Content catalog

The following table outlines the data extracted from the LMS as part of the Content Catalog package.

|Metadata field name |Field details |Priority |
|:-------------------|:-------------|:--------|
|Content provider (LMS) name | LMS's name. Can be provided separately and appended. |Required |
|Content provider (LMS) logo URL | URL to the LMS's logo for display purposes. |Required |
|Title of learning content |Title of learning content |Required |
|Content module's thumbnail URL |URL to the learning content thumbnail image for display purposes |Required |
|Content module's URL (deep link to consume content) |URL to learning content. This is the link that the user selects to consume content. |Required |
|Content module description/summary |Description or summary of learning content |Required |
|Content language/locale |Language in which content is available. Metadata should be provided in all available languages. |Required |
|Content module duration |Time duration of learning content |Required |
|Last modified date of content module/content creation date |Date the learning content was last modified |Required |
|Content format |Content format, such as article or video |Required |
|Assigned user role |Roles or groups that have permissions to the content  |Required for role-based access |
|Content source name |Name of the course content provider |Recommended |
|Content source logo URL |Logo of the course content provider |Recommended |
|Content ID |Unique identifier for learning content |Recommended |
|Content module author/creator/contributor |The author, creator, or contributor of learning content |Recommended |
|Content module length/size |Size of content, not based on time. For example, it could be the number of pages. |Recommended |
|Tags and keywords |Keywords, topics, and other tags associated with the learning content |Recommended |
|Difficulty level |Difficulty level of the course (such as beginner, intermediate, or advanced) |Recommended |
|Content module thumbnail alt text |Alternative text to support accessible design for images. Text describes images read by screen readers for users with assistive technology. |Recommended |
|Popularity score |Rating or popularity score for learning content |Recommended |
|Skills associated |Skills tags associated with the learning content |Recommended |

### Assignment records

The following table outlines the data extracted from the LMS for assignment records.

|Metadata field name |Field details |Priority |
|:-------------------|:-------------|:--------|
|Tenant ID | Tenant ID |Required |
|Configuration ID |LMS configuration ID. This is the equivalent to the learning source ID of the LAS. |Required |
|ID |Object unique key (configid+externalAssignmentId). |Required |
|Learning object ID |Unique identifier for the assigned learning object. |Required |
|Learner ID |ID of the learner or user assigned the learning object. |Required |
|External assignment ID |Unique assignment ID on each LMS side. |Required |
|Assignment due date |Date the assigned course is due for completion. |Required |
|Assignment completion status |Current completion status of the assigned learning object. This can be **Not started**, **In progress**, or **Completed**. |Required |
|Assignment date |Date the learning object was assigned. |Required |
|Assigner ID |ID of the user who assigned the learning object. |Recommended |
|Assignment completion date |Date the assignee completed the learning object. |Recommended |
|Assignment title |Title that an assigner maintains. |Recommended |
|Notes |Notes or comments on the assignment. |Recommended |

### Completion status

The following table outlines the data extracted from the LMS for completion status.

|Metadata field name |Field details |Priority |
|:-------------------|:-------------|:--------|
|Tenant ID | Tenant ID |Required |
|Configuration ID |LMS configuration ID. The equivalent to the learning source ID of the LAS. |Required |
|ID |Object unique key (configid+externalAssignmentId). |Required |
|User ID |Unique identifier for the user or employee. |Required |
|Learning object ID |Unique identifier for the assigned learning object. |Required |
|Completion status of learning object |The current completion status of the learning object. Completion status can be either **In progress** or **Completed**. |Required |
|Date of completion |Date the user completed the learning object. |Recommended |
|Start date |Date the user started the learning object. |Recommended |
|Course completion ID |Unique identifier for the course completion record. |Recommended |
|Current time |How far the user has progressed in the course (time).  |Recommended |
|Current page number |How far the user progressed in the course (page number). |Recommended |


## Content consumption for end users

Once you've added a learning management system as a content source, content from the LMS flows to Viva Learning and will be visible to end users.

Once a user chooses to play a course in Viva Learning, they'll be directed to the LMS webpage and need to enter the login credentials on the LMS sign-in page. [Learn more about how to consume content with Viva Learning](https://support.microsoft.com/office/01bfed12-c327-41e0-a68f-7fa527dcc98a).
