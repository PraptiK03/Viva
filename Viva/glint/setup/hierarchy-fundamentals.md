---
title: Viva Glint organizational hierarchy fundamentals
description: Learn how Viva Glint uses managerial hierarchy as the primary hierarchy ranking and processes the levels automatically, with a capacity of up to 10 levels.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: managerial hierarchy, locational hierarchy, departmental hierarchy, matrix hierarchies
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 01/10/2025
---

# Viva Glint organizational hierarchy fundamentals

A reporting hierarchy in Microsoft Viva Glint filters data into levels from highest to lowest, or largest to smallest, to provide precise insights into employee feedback. 

Glint allows for up to 10 reporting hierarchies, including a manager hierarchy. Each reporting hierarchy can have up to 10 levels, except for the manager hierarchy. The manager hierarchy can be calculated up to 25 levels.

## CEO and Manager hierarchy

Manager hierarchy is typically used as the primary reporting hierarchy. Glint generates this hierarchy automatically with file uploads. Every employee in your organization should have a Manager ID except your organization's CEO or top-level leader. No other hierarchy's are automatically generated.

> [!IMPORTANT]
> The Glint column label for your managerial hierarchy is **Manager.** Ensure that no other attribute columns in your employee data file are labeled *Manager.* 

### Example

Glint generates the employee's Manager ID column from your data file. 

|Employee|Manager|Glint generated Manager ID|Glint generated hierarchy level|
|-----|------|-------|------|
|Leonie| Marcio|Marcio's ID|Level 4|
|Marcio |Archie|Archie's ID|Level 3|
|Archie| Angel|Angel's ID|Level 2|
|Angel|None, Angel is the CEO. Leave the cell blank.|The hierarchy ends with Angel, who doesn't report to anyone.|Level 1|

:::image type="content" source="../../media/glint/setup/mgr-hierarchy-filter.png" alt-text="Screenshot of manager hierarchy filters in Glint reporting, drilling down from level 1 to level 3.":::

> [!CAUTION]
> Matrix manager hierarchies aren't recommended to be included in employee data. Glint only calculates levels for one manager hierarchy. 

## Update your CEO

When the CEO changes in your organization, the data file hierarchy must be updated. If not updated, your hierarchy is broken and may not show results or reflect your survey population the way it exists.

Process to update your data file for a new CEO:
1. Upload a file with the new CEO. Leave the Manager cell blank.
2. Update the CEO -referred to as **Top-Level Manager**- in the [General Settings](/../../viva/glint/setup/manage-general-settings) feature. 
3. To update this change for a current or past survey, implement a [**retroactive update**](/../../viva/glint/setup/glint-data-apps#retroactive_pulse_update). 

### Multiple CEOs

**Glint's best practice is to select a single user in your employee data as the top level/CEO whose Manager ID value is blank.** If your organization has multiple leaders that should sit at the top of your manager hierarchy, your organization can add a placeholder "CEO." All top-level users can then report to this placeholder CEO and appear as level 2 managers in Glint reporting and filters:

:::image type="content" source="../../media/glint/setup/placeholder-ceo-filter.png" alt-text="Screenshot of manager hierarchy filters in Glint reporting, with a placeholder CEO as the top-level user and multiple CEOs as level 2 managers.":::

#### Considerations

Before adding a placeholder CEO to your employee data:

- Determine whether your organization can manually insert a placeholder CEO in employee data files each time they're uploaded to Glint.
- Ensure that the Top-Level Manager selection in [General Settings](manage-general-settings.md) aligns with your placeholder CEO user or is left blank.

## Hierarchy groups

Depending on the size of your organization and reporting needs, Glint admins can set up other nonmanager reporting hierarchies. Include attributes in employee data for each level of these hierarchies, which commonly include location or department information.

### Example: location hierarchy

**NAMER > USA > Chicago**

:::image type="content" source="../../media/glint/setup/location-hierarchy-filter.png" alt-text="Screenshot of location hierarchy filters in Glint reporting, drilling down from level 1 to level 3.":::

In this example, three columns are needed in employee data to create a location hierarchy in Glint:

- Level 1 – Region
- Level 2 – Country
- Level 3 – City

This example includes three levels, but Glint admins can customize the location hierarchies for your organization to include up to 10 levels.

### Example: department hierarchy

**Department > Division**

:::image type="content" source="../../media/glint/setup/dept-hierarchy-filter.png" alt-text="Screenshot of department hierarchy filters in Glint reporting, drilling down from level 1 to level 2.":::

Two columns are needed in employee data to create a department hierarchy in Viva Glint:

- Level 1 – Department
- Level 2 – Division

## Next step
Use Glint attribute and hierarchy information to populate your Glint Employee Attribute Template. This template serves as a planning tool for your employee data file attributes, layout, and format.

> [!div class="nextstepaction"]
> [Viva Glint Employee Attribute Template](create-employee-attribute-template.md)
