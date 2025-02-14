---
ms.date: 01/31/2025
title: Discover organizational insights quickly with Microsoft 365 Copilot in Viva Insights
description: Explains how to use Microsoft 365 Copilot in Viva Insights to access organizational insights about your company, and use Copilot to answer questions about your organization.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.collection: 
- essentials-manage
- viva-copilot
- magic-ai-copilot
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: user
---

# Discover organizational insights quickly with Microsoft 365 Copilot in Viva Insights

>[!IMPORTANT]
> Microsoft 365 Copilot in Viva Insights is rolling out gradually and is not yet available to all customers.

Microsoft 365 Copilot in Viva Insights offers leaders and their assigned delegates an easy way to explore organizational and behavioral data. With Copilot, you can obtain actionable insights quickly and efficiently by asking questions in natural language, transforming how you interact with organizational data.

:::image type="content" source="images/copilot-leader-home.png" alt-text="Screenshot showing the organization insights Home page using Copilot.":::

## Prerequisites

To use Copilot, no additional license is needed; however, you must meet at least one of the following conditions:

* Be assigned a premium Viva Insights license and the Group Manager (GM) role in Viva Insights for a team that meets the minimum size requirements. [Learn more](../advanced/setup-maint/manager-settings.md).

* You can also view organization insights if you're given "delegate access" by a group manager. [See how delegate access works](../org-team-insights/delegate-access.md).

## How it works

Copilot in Viva Insights enables leaders to ask targeted or broad questions about their organization and receive instant, data-driven answers. Along with direct responses, Copilot provides access to detailed reports with visualizations, making it easy for leaders to dive deeper into the insights.

### Example questions

#### Specific questions related to workforce management

*"How many new hires joined my team last month?"*

Copilot generates a response based on the latest data, such as a count of new hires and detailed reports showing employee attributes like location, manager, or function.

#### Broader questions to get the general pulse of the team

*"How is my team doing?"*

Copilot summarizes data insights using people science research and behavioral observations, enabling leaders and delegates to make data-informed decisions.

#### Employee engagement topics

*"How much time does my team spend in after-hours collaboration across countries?"*

Copilot summarizes data insights using behavioral data capturing signals from collaboration tools like Outlook, Teams calls, and Teams chats, enabling leaders and delegates to make data-informed decisions.

#### Prompt recommendations

Users can explore recommended prompts using the Home page or Prompt Library. These prompts, with customizable fields, make it easier to get started and access the most relevant insights.

## Where to find it

As a leader or delegate, you can access Copilot using the Viva Insights Teams app or the web version of the app. A Copilot chat window will open on the right where you can ask questions. The Home page also provides prompts you can use to open Copilot. [Learn more](../org-team-insights/org-insights.md).

## Use deep-dive reports

As you use Copilot, you'll also find deep-dive visualization reports to help you perform further analysis and gain actionable insights. [Learn more](./copilot-deep-dive-reports.md).

## Use Organizational Behavioral Reports

Existing Organizational Behavior Reports remain available in Viva Insights. On the Home page, select **Organizational Behavior Reports** to access them. [Learn more](./leader-reports.md).

## How does it work on the backend?

Copilot in Viva Insights is powered by Large Language Models (LLMs), a technology that processes language-based tasks in a conversational format. The system combines enterprise data with AI-generated insights to provide accurate, actionable, and context-aware responses. [Learn more](../copilot-data-privacy-security.md).

## How to prepare your organization

As a Viva Insights admin, the quality of Copilot’s responses is determined by the quality of the HR data you upload. For best results:

* Upload new HR data at least once a month to keep insights accurate and up to date. 

* Maintain high coverage of HR data attributes by uploading data for everyone in your organization for each attribute. Exclude employees with sensitive attribute data.

* If you don't include users in an HR upload, organizational context data for those employees won't appear in Copilot in the Viva Insights app.  

* To remove Copilot access for a leader, [disable their Group Manager (GM) role](../advanced/setup-maint/manager-settings.md). To remove Copilot access for a delegate, remove their delegate role. [Learn more about delegate access](../org-team-insights/delegate-access.md).

[Learn more about how to optimize your use of attributes for Copilot](./../advanced/admin/upload-org-data-copilot.md).

### HR data attributes

Copilot uses the following customer uploaded HR data attributes: 

* **LevelDesignation**
* **HireDate**
* **FunctionType**
* **CountryOrRegion**
* **PersonIsManager**
* **WeeklyBadgeOnsiteDays**

[Learn more about Viva Insights attributes and their descriptions](../advanced/admin/prepare-org-data.md#attribute-reference).

## FAQs

### Q1. Can I still access existing reports in Viva Insights? 
Yes, these are available under the **Organizational Behavior Reports** section on the Home page. 

### Q2. What controls do admins have? 
Admins can: 

* Remove GM roles for users who shouldn't access Copilot. 
* Exclude specific HR attributes or users from data uploads.

### Related topics

* [View organization insights](../org-team-insights/org-insights.md)
* [Optimize how you use attributes with Copilot](./../advanced/admin/upload-org-data-copilot.md)