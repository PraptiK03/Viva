---
ms.date: 01/31/2025
title: Tips for uploading organizational data for Microsoft 365 Copilot in Viva Insights
description: Explains to Viva Insights admins which specific attributes to upload and how to use them to generate actionable insights with Microsoft 365 Copilot.
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

# Tips for uploading organizational data for Microsoft 365 Copilot in Viva Insights

>[!IMPORTANT]
> Microsoft 365 Copilot in Viva Insights is rolling out gradually and isn't yet available to all customers.


Microsoft 365 Copilot in Viva Insights is most effective when you upload as much data as possible for each employee attribute in Viva Insights. You should upload as many attributes as your company finds useful, because most questions leaders ask will depend on a combination of multiple attributes. [Learn more about the attributes Copilot in Viva Insights supports](./prepare-org-data.md).

Here's a list of specific attributes and the questions you can ask Copilot, whose responses would be informed by those attributes.

| Attribute | Sample questions related to the attribute |
|---|---|
| ManagerId | <li>How many senior engineers in the U.K. manage teams? <li>How many managers have less than 1 hour of manager 1:1 time with their teams each week? <li>Who are my managers in New York? <li>How many employees in the Product organization have a team size of more than three, grouped by level? |
| LevelDesignation | <li>How many principal engineers work across two different time zones? <li>How many senior employees work mostly in the office? <li>Who are the new hires at the executive level? |
|FunctionType | <li>Which HR employees are new hires who work mostly from the office? <li>How many Sales employees with the Sales function have more than 10 hours of external meeting hours each week? <li>How many Finance employees worked after hours last month? |
| HireDate | <li>Who got hired in October, grouped by teams? <li>Who are the employees hired in the last 12 months, grouped by department? <li>Who was hired more than 20 years ago and is still with the company? <li>Who were the new hires in the leadership team over the past three years? <li> Which employees hired in 2018 are engineers? <li>How many employees have their work anniversaries this quarter? <li>Who are the tenured employees in the Finance department, grouped by level and region? | 
| Supervisor Indicator | <li>How does after hours collaboration vary between managers and managers of managers? <li>How much 1:1 time is there in the sales organization between individual contributors and managers?  <li> What is the ratio between managers and individual contributors in the engineering team?  |
| WeeklyBadgeOnsiteDays | <li>How does average network sizes of employees vary between hybrid, on-site, and mostly remote? <li>What is the distribution of work modes for my finance team in Chicago?  <li>Who are my employees that work on-site on Tim’s team? |
| CountryOrRegion | <li>What is the after hours collaboration of employees across different countries?  <li>Who are the newly hired data scientists in the U.S.? <li>How many managers in Eastern Europe have less than two hours of manager 1:1 time? |
| Timezone (Not an uploaded value, automatically derived from user settings) | <li>How many employees work in EST?  <li>What is the distribution of employees across time zones?  |

## Other best practices to keep in mind

* **Align the data types for each column**. Each attribute above has a required data type format. For example, HireDate is a DateTime data type while Function Type is a String. [Learn more about data types and their example values](./prepare-org-data.md#attribute-reference).

* **Choose your population for every attribute**. Upload each attribute with the entire analyzed population, but exclude employees for an attribute that your company considers sensitive, and for employees whose data you don't want to appear for leaders. The only way to exclude data from appearing in Copilot responses is to abstain from uploading data for those employees. This allows you to take control of the data that appears in Copilot for these organizational context attributes. If in doubt, consult the appropriate internal teams at your company.

    >[!Note]
    > For questions regarding HR data, Copilot's answers are based only on employees with a Viva Insights license.

* **Refreshed data is good data**. If you're using a .csv upload as the data source, you should periodically refresh attributes that change often in your organization. You should refresh the following attributes with the frequencies below:

    * Monthly refreshes: ManagerId, WeeklyBadgeOnsiteDays 
    * Quarterly refreshes: SupervisorIndicator, Layer, HourlyRate, LevelDesignation, Organization 
    * Six-month refreshes: NewHireDate, Location, CountryOrRegion, FunctionType

* **Establish unique values for different attributes**. Copilot associates leaders' questions with uploaded attributes. If there's a large overlap in the values across multiple attributes, the system might incorrectly associate a question with the wrong attribute. This is most likely to happen for the Location, CountryOrRegion, Organization, and FunctionType attributes.

### Related topics

[Learn more about how to use Copilot in Viva Insights](..//..//org-team-insights/org-insights-copilot.md)