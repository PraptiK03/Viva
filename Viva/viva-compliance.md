---
title: "Microsoft Viva compliance"
ms.reviewer: loreenl
ms.author: loreenl
author: loreenla
manager: elizapo
ms.date: 05/07/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: solution-overview
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- essentials-compliance
search.appverid:
- MET150
description: "Find Microsoft Viva compliance information."
---

# Microsoft Viva - Compliance

Microsoft offers a [comprehensive set of compliance offerings](/compliance) to help your organization comply with national, regional, and industry-specific requirements governing the collection and use and data. 
Microsoft Viva is also covered under the [Microsoft Product Terms](https://www.microsoft.com/licensing/docs/view/Product-Terms) and [Data Protection Agreement (DPA)](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA?year=2021#:~:text=Microsoft%20Products%20and%20Services%20Data%20Protection%20Addendum%20%28DPA%29,to%20the%20Product%20Terms%20site%20%28and%20formerly%20OST%29).

For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trustcenter).

This article covers the following information:

- [Shared responsibility model](#shared-responsibility-model)

- [Inheritance of compliance features and settings](#inheritance-of-compliance-features-and-settings)

- [System and Organization Controls (SOC) 2](#system-and-organization-controls-soc-2)

- [General Data Protection Regulation (GDPR)](#general-data-protection-regulation-gdpr)

- [Data residency](#data-residency)

- [Microsoft Purview](#microsoft-purview)


## Shared responsibility model
Microsoft works to ensure that we are compliant with industry and international standards, and customers are responsible for ensuring their data within the [Microsoft Cloud](https://www.microsoft.com/en-us/trust-center/compliance/compliance-overview#compliance) is protected in a manner that is compliant with the standards and regulations imposed on the customer.

![Image depicting shared responsibility model](./media/viva-compliance.png)

## Inheritance of compliance features and settings
Microsoft Viva apps are built on your existing infrastructure and, depending on the app, inherit compliance features and settings from Microsoft Teams, Exchange Online, SharePoint, Azure, and Viva Engage. In addition, all Viva modules are built on the [Microsoft Graph API](/graph/overview).

![Image depicting simple architecture model](./media/viva-architecture.png)

For detailed information on each service, see:

**Microsoft 365** [Plan for security and compliance](/microsoft-365/compliance/plan-for-security-and-compliance)

**Microsoft Teams** [Overview of security and compliance in Microsoft Teams](/microsoftteams/security-compliance-overview)

**Microsoft SharePoint** [Plan compliance requirements for SharePoint and OneDrive](/SharePoint/compliant-environment)

**Microsoft Graph** [Use the Microsoft Graph compliance and privacy APIs](/graph/api/resources/complianceapioverview)
 
**Viva Engage** [Overview of security and compliance in Viva Engage](/viva/engage/manage-security-and-compliance/security-and-compliance)

**Microsoft Entra ID** [Microsoft Entra security baseline for Microsoft Entra ID](/security/benchmark/azure/baselines/aad-security-baseline)

**Azure** [Azure, Dynamics 365, Microsoft 365, and Power Platform compliance offerings](/azure/compliance/offerings/)

## System and Organization Controls (SOC) 2

A [SOC 2 report](/compliance/regulatory/offering-soc-2) is an independent assessment of a service organization's systems and processes that are relevant to the trust services criteria. The report is conducted by a third-party auditor and evaluates the effectiveness of the controls in place to meet these criteria. Following is the SOC 2 audit report status for each Viva app:

| Viva app | SOC 2 report |
|----------|-----------|
| Viva Connections | Covered within scope of [Microsoft 365 - Central Services - SOC 2 report](https://servicetrust.microsoft.com/DocumentPage/b369c903-12a0-406d-8a25-ea7c61b3a42e). Excludes third-party content.
| Viva Glint, Insights, Learning, Pulse | Covered by [Microsoft 365 - Microservices Type 2 SOC 1 Report](https://servicetrust.microsoft.com/DocumentPage/432fa0dd-f656-4be3-ac40-5dbb6a249cb7)
| Viva Engage | Covered by [Microsoft 365 - Viva Engage - SOC 2 Type 2 (2024)](https://servicetrust.microsoft.com/DocumentPage/abcf5178-cd02-45ab-a226-6b278bb2aa09)

## General Data Protection Regulation (GDPR)
All Viva apps built on your Microsoft 365 infrastructure support compliance with EU General Data Protection Regulation (GDPR) requirements.
For detailed information, see [Microsoft Viva privacy](/Viva/viva-privacy).

## Data residency
Data residency refers to the geographic location where data is stored at rest. Many customers, particularly in the public sector and regulated industries, have distinct requirements around protecting personal or sensitive information.  In addition, in certain countries, customers are expected to comply with laws and regulations that explicitly govern data storage location.

For information about data residency for Viva apps, see [Microsoft Viva privacy](/Viva/viva-privacy).

## Microsoft Purview 
[Microsoft Purview](/purview/purview) is a family of data governance, risk, and compliance solutions that can help your organization govern, protect, and manage your entire data estate.

Currently, certain features in Viva Engage and Viva Connections (through SharePoint) are supported by Microsoft Purview.

The Viva Engage features [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery) and [Data Retention](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview) are supported by Microsoft Purview; sensitivity labels and data loss prevention aren't supported. Native Mode is required to take advantage of eDiscovery and the Microsoft Purview portal. This functionality is unavailable for networks in non-Native mode. For more information, see [Overview of Native Mode](engage/native-mode-guide.md).

Viva Connections inherits eDiscovery and [Data Retention](/microsoft-365/compliance/retention-policies-sharepoint) support from [SharePoint](/SharePoint/compliant-environment) for files involved in each service.

## More resources

[Microsoft Viva privacy](/Viva/viva-privacy)

[Microsoft Viva security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
