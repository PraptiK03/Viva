---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 05/21/2025
title: Skills landscape report
description: Navigate the skills landscape report in Viva Insights
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: ablubetk
audience: Admin
---
# Skills landscape report (preview)

>[!Important]
>This feature is in private preview. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

The Skills landscape report helps you explore top skills people in your company might have and identify potential skill gaps. These insights are powered by [People Skills](https://go.microsoft.com/fwlink/?linkid=2313228&clcid=0x409).

With this report, you can:

* Understand People Skills data and how it's used
* Browse commonly used skills and areas of skills specialization 
* See how groups of skills are distributed in your organization 
* Explore skills hierarchy 

Before we get started, there are a few things you should know:

* People need to have eligible licenses for **Viva Insights** and valid **People Skills** data to be included in this report.
* The skills data is imported from People Skills to Viva Insights through APIs. Your Microsoft 365 admin or knowledge admin needs to enable the connection in the Microsoft 365 admin center.
* Only people with the **Viva Insights Analyst** role can run and set up this report. Your Microsoft 365 admin needs to assign the analyst role to enable their access.
* The skills names displayed in the report are only available in English.
* The report can include up to three months of skills insights.  

To populate the report in Power BI, you need to set up, and successfully run the predefined **Skills landscape** query in Viva Insights.

:::image type="content" source="../../images/skills-pbi-setup.png" lightbox="../../images/skills-pbi-setup.png" alt-text="Screenshot of run analysis to populate report.":::

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiZDlmOTY4NTctYmVhYi00ZWM5LTlkYmQtYWZhZDIwNjEwMGYzIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]
 
## Prerequisites
Before you can run the queries and populate the report in Power BI, you need to:

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the December 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.

## Report setup
### Run query
1.	In the Viva Insights analyst experience, select **Analysis.**
2.	Under Power BI templates, navigate to **Skills landscape** and select **Set up analysis.**
3.	Under **Query setup**:

    1. Type a **Query name.**

    2. Type a **Description** (optional).
    
    3. Select a **time period** of up to three months.

    >[!Note]
    > This Power BI query is set to **Group by Month**, and you can't edit this field.

4. Set **Auto-refresh** (optional). You can set the query to automatically update by selecting **Auto-refresh**. When you select **Auto-refresh**, your query automatically runs and computes a new result every month.

    >[!Note]
    > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing. 

5.	In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. For more details about filter and metric options, refer to [Filters.](../filters.md)

    >[!Important]
    > Only people with valid **Viva Insights** licenses and People Skills data are included in this report. The population count in **Employees with People Skills** data shows the number of employees the query will measure. The query won't run if the population count is zero.

6.	Under **Select which employee attributes you want to include in the query**, add up to 20 organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    > This Power BI query needs some specific attributes to run, including some required attributes to indicate employee skills, and we've preselected them for you. These attributes appear in gray and you can't 
      remove them.
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is 
      missing that attribute.
      Learn more about attributes and data quality in [Data quality in the analyst experience.](../data-quality-analyst-experience.md)

7.	Select **Run** on the upper right side of the screen. The query might take a few minutes to run.
8.	When your query results are ready, go to the **Query results page** and select the **Power BI icon**. Download the Power BI template and get the partition and query identifiers. You need these identifiers later.

### Link report to query

1. Open the downloaded template.
1. If you're prompted to select a program, select **Power BI**.
1. When you're prompted by Power BI:
   1. Paste in the partition and query identifiers.
   1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
   1. Select **Load** to import the query results into Power BI.
1. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.
   > [!IMPORTANT]
   > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
   > :::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab." :::

## Report settings
View and set the following parameters in **Report settings**. You can find this section on the right panel of the report's pages.

| Setting | Description |
| ------- | ------------------|
| Time period for the report | This shows the time period of the insights in the report. The report includes up to three months of the skills data based on your selection when you set up the query. |
| Group by | Set the primary group-by attribute for all report pages. You can change this attribute at any time and all report pages will group values by the new attribute. |
| Filter | Select an organizational attribute, and then filter by any of the values for the selected attribute. For example, if you selected "Organization" as the attribute, you could set "Engineering" as the filter value. You'll only see data from the Engineering organization, so setting filters lowers the **People included in this report** count. |
|Skill customization | Exclude AI-inferred skills: Choose whether to exclude AI-inferred skills in the distribution insights. AI-inferred skills are powered by People Skills based on people's job titles and recent Microsoft 365 activities. If you select this option, the report will only include confirmed skills in the distribution insights. |

## About the report
The report provides insights about the skills landscape in your organization to help you identify distribution of top skills, connections between skills, and potential skill gaps.


### About skill distribution and related concepts
This is the total number or percentage of people in your organization who have either confirmed they have a skill or are presumed to have a skill based on AI reasoning and analysis. Distribution can be filtered to include only confirmed skills in **Report settings**.

* **Skill confirmed by user**: A skill that a person confirmed they have in People Skills experiences.
* **Skill inferred by AI**: A skill that an AI system predicts a person has but hasn’t been confirmed by the person. AI inferences are based on job titles and recent Microsoft 365 activities.


### People Skills introduction

This page introduces the basics of People Skills and provides a summary of your organization's skills data. This page can help you:

* Understand how People Skills infers and provides data 

* Identify how many people are included in this report. If the number doesn't look correct, contact your admin for more information 

* Discover how many people have confirmed their skills. As more people confirm their skills, the data's relevance improves

### Top skills at a glance

This page provides a top-level overview of the skills being used across the measured population in the organization.

This page can help you:

* Understand commonly used skills in your organization, which are normally used across a large population. 

* Discover top used skills in Artificial Intelligence. Use this information to identify talent in this area for your AI initiatives. 

* Identify skills that are highly concentrated in small pockets of the population. These insights help you discover areas of skills specialization in specific groups.

There are two definitions of concentration skills you can toggle between in the report:

* By count of employees: A skill is concentrated if it's held by many employees in just a few groups. This information can be useful for your project assignments or resource allocation.

* By percentage of employees: A skill is concentrated if it's held by a high percentage of employees in just a few groups. This information can help you identify expert groups for your initiatives.

### Skills deep dive 

This page provides insights on how specific skills are distributed between groups (determined by organizational attributes). You can use these insights to understand the skill profile for a group, compare differences across groups, and identify potential skill gaps. 

Specifically, you can:​ 

* Select a primary skill of interest to quickly form a group of related skills, including its subskills and adjacent skills.​

* Define your own group of skills for distribution analysis by adding or removing skills.​

* Identify the distribution of skills across your organization based on available attributes in the report.

### AI-generated skills hierarchy (beta) 

Powered by People Skills and currently in beta, this page shows how skills are clustered and connected to each other to help you: 

* Identify skills distribution from the categories that matter to your organization

* Maximize learning and career advancement programs​ 

* Better allocate resources by understanding how skills complement each other 

In the interactive visuals on this page, you can explore the skills hierarchy in your organization. Start by selecting a skill category to view the top skills for that category. Select one of these skills to show its subskills. If the Computer science skill is in the top layer, and the Artificial intelligence (AI) skill is in the drilldown, this means AI is a subskill of Computer science. There are up to five layers in the skills hierarchy, powered by People Skills.

### Glossary
Get definitions for key concepts introduced in this report. [Learn more about People Skills](https://go.microsoft.com/fwlink/?linkid=2313228&clcid=0x409).

## FAQ 

**Q1. I see the Skills landscape report template in Advanced Insights, but I can't run the query. And, employees with People Skills data is zero in the query setup. Why?**

There are two prerequisites to use skills data for this report: 

1. People Skills services need to be onboarded and active in your organization.  
2. The data sharing option needs to be turned on for Viva Insights to process People Skills data.  

Please contact your Microsoft 365 admin for more details.

**Q2. Why are there fewer people than expected in this report?**

There can be multiple reasons: 

1. Some employees might not have the required Viva Insights licenses or People Skills service plan. Contact your Microsoft 365 admin for information on the Viva licenses and People Skills service plan in your organization. 
2. Some employees might not have their organizational data successfully uploaded or connected to Viva Insights. Contact your Insights admin for details about organizational data. 
3. Some employees might decide not to share their skills with the organization in their skills settings. Their skills will no longer show up in this report.

**Q3. The total number of people is correct in the report, but some groups don't appear in the breakdown view. Why?**

This report has a minimum group size threshold, which is set to 10 people by default. Any group that does not meet this minimum size will not be displayed in the report breakdown view.

**Q4. I have other questions about setting up or sharing the Power BI report.**

For details about how to share the report and other Power BI tips, troubleshooting, and frequently asked questions, see [Power BI tips, FAQ, and troubleshooting.](./power-bi-faq-troubleshoot.md)

**Q5. What is People Skills and how can I learn more about it?**

People Skills is a service in Microsoft 365 to help employees and organizations identify skills, manage skills, and discover opportunities. [Learn more](https://go.microsoft.com/fwlink/?linkid=2313228&clcid=0x409).

## Related topics
[Access query results and modify existing queries](../query-results.md)

[Filters](../filters.md)