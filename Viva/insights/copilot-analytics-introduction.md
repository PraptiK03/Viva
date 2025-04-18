---
ms.date: 04/21/2025
title: Copilot Analytics introduction
description: Explains how to set up and use Copilot Analytics in Viva Insights, including the Microsoft Copilot Dashboard and Advanced Reporting.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.collection: 
- essentials-manage
- essentials-overview
- essentials-navigation
- viva-copilot
- magic-ai-copilot
- highpri
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: user
---

# Copilot Analytics introduction

Microsoft 365 Copilot Analytics provides organizations with deep insights about how their employees are using Copilot. With these insights, companies can make better-informed decisions about how to deploy Copilot, and how to more broadly improve employee productivity.

Copilot Analytics encompasses three areas:  

* Readiness and adoption report in the Microsoft 365 admin center. [Learn more](/microsoft-365/admin/activity-reports).

* Microsoft Copilot Dashboard in Teams and the Teams web app for leaders and their selected delegates. [Learn more](./org-team-insights/copilot-dashboard.md).

* Advanced Reporting through the Viva Insight web app and pre-configured Power BI dashboards. [Learn more](./advanced/introduction-to-advanced-insights.md).

## Which tool should I use when?

| Tool | Scenario |
|---|---|
| Readiness and adoption report | This report, available in the Microsoft 365 admin center, provides a starting point to help inform your Copilot license deployment and rollout strategy and to monitor adoption. It includes reports on: <br><br /><li>[Readiness](/microsoft-365/admin/activity-reports/microsoft-365-copilot-readiness)<li>[Usage](/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage)<li>[Copilot chat](/microsoft-365/admin/activity-reports/microsoft-copilot-usage)<li>[AI Adoption score](/microsoft-365/admin/adoption/ai-adoption-score)<li>Agents<li>Message consumption |
| Copilot Dashboard | Once you've deployed Copilot, the Copilot Dashboard provides insights and metrics that help you understand usage and evaluate the impact across your organization. The report includes details of Copilot actions taken across each Microsoft 365 app, estimated financial savings, and learning resources. [Learn more](./org-team-insights/copilot-dashboard.md). |
| Advanced Reporting | Advanced Reporting enables organizations to dive deeper into Copilot usage and impact through both pre-configured Power BI report templates and fully customizable queries. You can select from more than 100 Copilot metrics and customize filters to answer granular and specific questions. You can also upload business impact data to measure Copilot's impact using the metrics that matter most to your organization. [See the list of pre-configured templates](#copilot-analytics-pbi-reports). |

All employees with Microsoft 365 Copilot licenses are automatically assigned a Viva Insights service plan, which makes them part of the measured population for the Copilot Dashboard as well as Advanced Reporting. [Learn how to modify these settings](./advanced/privacy/privacy.md#remove-employees-from-the-measured-population).

## How to access and set up the Copilot Dashboard

1. The Copilot Dashboard is available in the Teams app for any customer with a Microsoft 365 or Office 365 subscription for business or enterprise, who has an active Exchange Online account. The dashboard's availability of features and metrics, however, depend on the number of assigned Copilot and Viva Insights licenses. [Learn more](./org-team-insights/copilot-dashboard.md#feature-availability-based-on-licenses). Data is typically available within seven days after licenses have been assigned.

2. Users who are senior leaders as determined by their Microsoft Entra ID data have automatic access to the dashboard. Users with access to the dashboard can "delegate" their access to other people in the company so they also can view the dashboard. [Learn more](./org-team-insights/delegate-access.md).

3. There are a number of other settings you can customize for the Copilot Dashboard, such as controlling who can access it, or setting a minimum group size for insights. [Learn more](./advanced/admin/manage-settings-copilot-dashboard.md).

4. Uploading organizational data is optional but a step you can take to view more granular details. [Learn more](./advanced/admin/upload-org-data-copilot.md).

### How to upload organizational data

By default, the Copilot Dashboard uses your organization's Microsoft Entra ID data as well as user settings and SMTP addresses. This data source automatically ingests the **PersonId**, **ManagerId**, **Organization**, **Domain**, and **TimeZone** attributes. [Learn more about attributes](./advanced/admin/org-data-overview.md).

If you want to keep using Microsoft Entra ID as the data source, you don't need to do anything else to upload organizational data. But if you want to incorporate more attributes into the dashboard's insights, then use one of the methods described below.

* Upload data through the advanced insights app using [these steps](./advanced/admin/org-data-overview.md). This is the recommended way to upload data if you have Viva Insights licenses deployed.

* Import organizational data using an automated API-based import. [Learn more](./advanced/admin/import-org-data-first.md). 

* Import organizational data using an automated Azure blob import. [Learn more](./advanced/admin/import-org-data-azure.md). 

* Upload data through the Microsoft 365 admin center using [these steps](/viva/organizational-data).

## How to set up Advanced Reporting

1. Only users with the **Insights Analyst** role can set up and run queries. Assign roles using [these steps](./advanced/setup-maint/assign-user-roles.md). 

2. If you'd like, you can customize privacy settings such as the minimum group size for insights, or remove sensitive keywords from insights. [Learn how](./advanced/setup-maint/privacy-settings.md).

    > [!VIDEO 34102e25-f316-432c-974b-b20d7f8f7ff0]

### How to use preconfigured templates for Advanced Reporting

There are several preconfigured Power BI templates you can use to analyze the usage and impact of Copilot within your organization. You can also customize each template using filters and metrics based on the specific question you're looking to answer.  

To find these templates, in the Viva Insights analyst experience, select **Create analysis**. Under the **Copilot** section, select **Set up analysis** for the template you want to run.

:::image type="content" source="images/analyst-copilot-pbis.png" alt-text="Screenshot that shows where to find PBI templates.":::

> [!VIDEO 7623c86c-43e1-4684-995d-1cf22f15399d]

### Copilot Analytics PBI reports

Learn more about how to set up and use each report with the links below.

* [Copilot adoption report](./advanced/analyst/templates/microsoft-365-copilot-adoption.md)
* [Copilot impact report](./advanced/analyst/templates/microsoft-365-copilot-impact.md)
* [Copilot for Sales adoption report](./advanced/analyst/templates/copilot-for-sales-adoption.md)
* [Copilot business impact report](./advanced/analyst/templates/copilot-business-impact.md)