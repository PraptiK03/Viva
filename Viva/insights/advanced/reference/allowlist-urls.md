---
ms.date: 4/11/2025
title: Viva Insights allowlist URLs
description: Learn about the required URLs that must be allowed for Viva Insights to operate correctly.
author: zachminers
ms.author: v-zachminers
ms.topic: concept-article
ms.collection: 
- viva-insights-advanced
- viva-insights-leader
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anriduhbajaj
audience: Admin
---

# Viva Insights allowlist URLs

Viva Insights requires access to specific URLs to function properly. Network or Microsoft Entra ID administrators, therefore, must ensure these URLs are allowed through firewalls, proxies, and other network security measures.

The table below identifies the required URLs that must be allowed for Viva Insights to operate correctly. Blocking any of these endpoints might lead to an inability to access the service, missing data, degraded performance, or limited feature availability.

## Required allowlist URLs

Wildcards (*) represent all levels under the root domain.

| URL | Purpose |
|---|---|
| login.microsoftonline.com | Authentication and authorization |
| api.orginsights.viva.office.com | Viva Insights API services |
| *.cloud.microsoft | Analytical processing for Viva Insights |
| substrate.office.com | Data processing and integration |
| graph.microsoft.com | Microsoft Graph API for retrieving organizational data |

## Recommended allowlist URLs

While not required, allowing the following URLs can improve performance and ensure a seamless experience with Viva Insights.

| URL | Purpose |
|---|---|
| webshell.suite.office.com | Microsoft Office 365 Web Shell services |
| clients.config.office.net | Office client configuration and updates |
| res-1.cdn.office.net | Office 365 content delivery network |
| ecs.office.com | Office 365 cloud services |
| r4.res.office365.com | Office 365 resource services |
| amcdn.msftauth.net | Microsoft authentication services |
| config.fp.measure.office.com | Office telemetry and performance monitoring |
| js.monitor.azure.com | Azure monitoring and telemetry |
| browser.events.data.microsoft.com | Microsoft browser event data collection |

## Related topics

* [Supported languages](./supported-languages.md)
* [Set up advanced insights](../setup-maint/setup-overview.md)