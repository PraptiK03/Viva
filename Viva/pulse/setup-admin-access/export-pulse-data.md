---
title: Export pulse data
description: "Export all tenant and report data as a pulse admin"
ms.reviewer: 
ms.author: zaidjiwani
author: zaidjiwani
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 4/22/2025
ms.topic: how-to
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
---

# Export data

As a Pulse admin, you can choose to either export out all Pulse data or specific report data. To access the Viva Pulse admin export feature, you must have one of the following admin roles assigned to you: Microsoft 365 Global admin, Pulse admin. Reports will get data only for reports created after enabling e-Discovery for Forms Responses. Otherwise, it is empty.

To open the **Export** tab, go to Viva Pulse on the app or on the web, and select **Manage** and then **Data export**. Your tenant can only have one export job active at a time.

### Export all tenant data

To export out all data from a tenant, select **Create an export request** and then select all data. You must input a date range that can be no longer than one year. After inputting your desired dates, select **Export to .csv**.

You get an email notification letting you know when your export job is complete.

### Export report data

To export out report data from a tenant, select **Create an export request** and then select **Report data**. You must input a specific author and you can filter by Pulse name and template type. After selecting your desired reports, select **Export to .csv**.

You get an email notification letting you know when your export job is complete.
 
### Column definitions  

The Status column in your exported data displays one of the following values to indicate the current state of each feedback request:

- Open (0): The feedback request is active and still open.  
- Closed (1): The feedback request is completed.  
- Canceled (2): The feedback request is canceled.  

The Question Type column in your exported data shows one of the following values to describe the format of each question:

- Rating (0): The question uses a rating scale.  
- Multiple Choice (1): The question allows the user to select one or more options from a list.  
- Open-Ended (2): The question allows the user to type in an open-ended response.  
- Matrix (3): The question is a matrix question.  
- Ranking (4): The question asks the user to rank options.  

The Category column in your exported data shows one of the following values to indicate the type of question:

- Focus (0)  
- Resource (1)  
