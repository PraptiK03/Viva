---
title: Viva Glint organizational hierarchy fundamentals
description: A reporting hierarchy in Microsoft Viva Glint filters data into levels from highest to lowest, or largest to smallest, to provide precise insights into employee feedback.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: manager hierarchy, locational hierarchy, departmental hierarchy, hierarchy group, reporting hierarchy
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/28/2025
---

# Viva Glint organizational hierarchy fundamentals

A reporting hierarchy in Microsoft Viva Glint filters data into levels from highest to lowest, or largest to smallest, to provide precise insights into employee feedback. 

Viva Glint allows for up to 10 reporting hierarchies, including a manager hierarchy. Each reporting hierarchy can have up to 10 levels, except for the manager hierarchy. The manager hierarchy can be calculated up to 25 levels.

## CEO and Manager hierarchy

Manager hierarchy is typically used as the primary reporting hierarchy. Viva Glint generates this hierarchy automatically with file uploads. Every employee in your organization should have a Manager ID except your organization's CEO or top-level leader. No other hierarchies are automatically generated.

> [!IMPORTANT]
> The Viva Glint column label for your managerial hierarchy is **Manager.** Ensure that no other attribute columns in your employee data file are labeled *Manager.* 

### Example

Viva Glint generates manager hierarchy levels based on the relationship between Employee and Manager IDs in your employee data files.

|Employee|Manager|Manager ID|Viva Glint generated hierarchy level|
|:-----|:------|:-------|:------|
|Leonie| Mario|Mario's ID|Level 4|
|Mario |Archie|Archie's ID|Level 3|
|Archie| Angel|Angel's ID|Level 2|
|Angel|None, Angel is the CEO. Leave the cell blank.|The hierarchy ends with Angel, who doesn't report to anyone.|Level 1|

:::image type="content" source="../../media/glint/setup/mgr-hierarchy-filter.png" alt-text="Screenshot of manager hierarchy filters in Glint reporting, drilling down from level 1 to level 3.":::

> [!CAUTION]
> Viva Glint only calculates levels for one manager hierarchy and doesn't support other matrix manager hierarchies.

## Update your CEO

When the CEO changes in your organization, update your employee data file and selections in Viva Glint. If not updated, your hierarchy is broken and may not show results or reflect your survey population the way it exists.

To update a CEO in Viva Glint:

1. Upload a file with the new CEO. Leave the Manager cell blank.
2. Update the CEO -referred to as **Top-Level Manager**- in the [General Settings](/../../viva/glint/setup/manage-general-settings) feature.
3. If the new CEO doesn't appear as a user to select from the dropdown menu in **General Settings**:
   1. Go to **Configuration** and choose **People**.
   2. Search for the new CEO and on their user profile, update their email address (to their Employee ID, for example).
   1. Return to **General Settings** and search for and select the new CEO.
   1. On the new CEO user's profile, revert their email address to the correct value.
4. Reload employee data, including the CEO with a blank Manager ID, to recalculate your manager hierarchy.
5. To update this change for a current or past survey, implement a [**retroactive update**](/../../viva/glint/setup/glint-data-apps#retroactive_pulse_update). 

### Multiple CEOs

**Viva Glint's best practice is to select a single user in your employee data as the top level/CEO whose Manager ID value is blank.** If your organization has multiple leaders that should sit at the top of your manager hierarchy, your organization can add a placeholder "CEO." All top-level users can then report to this placeholder CEO and appear as level 2 managers in Viva Glint reporting and filters:

:::image type="content" source="../../media/glint/setup/placeholder-ceo-filter.png" alt-text="Screenshot of manager hierarchy filters in Viva Glint reporting with a placeholder CEO as the top-level user.":::

#### Considerations

Before adding a placeholder CEO to your employee data:

- Determine whether your organization can manually insert a placeholder CEO in employee data files each time they're uploaded to Viva Glint.
- Ensure that the Top-Level Manager selection in [General Settings](manage-general-settings.md) aligns with your placeholder CEO user or is left blank.

## Hierarchy groups

Depending on the size of your organization and reporting needs, Viva Glint Admins can set up other nonmanager reporting hierarchies. Include attributes in employee data for each level of these hierarchies, which commonly include location or department information.

### Example: location hierarchy

**NAMER > USA > Chicago**

:::image type="content" source="../../media/glint/setup/location-hierarchy-filter.png" alt-text="Screenshot of location hierarchy filters in Viva Glint reporting, drilling down from level 1 to level 3.":::

In this example, three columns are needed in employee data to create a location hierarchy in Viva Glint:

- Level 1 – Region
- Level 2 – Country
- Level 3 – City

This example includes three levels, but Viva Glint admins can customize the location hierarchies for your organization to include up to 10 levels.

### Example: department hierarchy

**Department > Division**

:::image type="content" source="../../media/glint/setup/dept-hierarchy-filter.png" alt-text="Screenshot of department hierarchy filters in Viva Glint reporting, drilling down from level 1 to level 2.":::

Two columns are needed in employee data to create a department hierarchy in Viva Glint:

- Level 1 – Department
- Level 2 – Division

## Next step
Use Viva Glint attribute and hierarchy information to populate your Viva Glint Employee Attribute Template. This template serves as a planning tool for your employee data file attributes, layout, and format.

> [!div class="nextstepaction"]
> [Viva Glint Employee Attribute Template](create-employee-attribute-template.md)
