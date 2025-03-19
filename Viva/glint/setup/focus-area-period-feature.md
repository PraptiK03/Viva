---
title: Set up Focus Area periods for a Viva Glint survey
description: Viva Glint admins can manage Focus Area periods directly from the platform. A Focus Area period is the timeframe (or window) from Focus Area creation through expected action taking completion. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: focus area periods
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: install-set-up-deploy
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 12/12/2024
---

# Set up Focus Area periods for a Viva Glint survey

Viva Glint admins can manage Focus Area periods directly from the platform. A Focus Area period is the timeframe (or window) from when the Focus Area is created until action taking should be completed.

Managing Focus Area periods allow admins to determine how often to survey. From the Configuration page, select **Periods** from the **Focus Areas** section. 

:::image type="content" source="../../media/glint/reports/focus-area-periods-access.png" alt-text="Screenshot of how to access Focus Area Periods from the admin dashboard.":::

> [!NOTE]
> Glint Admins need **Manage Focus Area Periods** permission to configure them. Set that up in **User Roles** from your Glint dashboard.

## Add a Focus Area Period

1. Select **+ New Period** to open the **Create Period** slider panel.

   :::image type="content" source="../../media/glint/reports/focus-areas-create-period.png" alt-text="Screenshot of the Create Period slider window.":::

2. Select a language. Each language saves as it is selected.
1. Select a cadence: monthly, quarterly, semi-annually, annually, weekly.
1. Name the period.
1. Choose a start date. 
1. Choose an end date. The end date is the date of expected completion. Managers see this date on their action plan.
1. **Enable** the Focus Area period.
1. Select **Save Changes.**

## Focus Area Periods have built-in 90-day logic

When a manager creates a Focus Area period, the system checks to find if another Focus Area period conflicts with this timeframe. If a conflict exists, the system creates a new Focus Area period to allow users enough time to complete all actions.

> [!TIP]
> When configuring this window, realize that action plan strategies are built around a 90-day completion plan. Create the time period to allow 90 days from the day the manager establishes their action to its expected due date.
