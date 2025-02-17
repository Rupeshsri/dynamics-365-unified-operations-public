---
# required metadata

title: Workforce metrics Power BI content
description: This topic describes the Workforce metrics Power BI content.
author: jcart1106 
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

ms.search.form: HcmWorkforceWorkspace
# ROBOTS: 
audience: Application User, IT Pro
# ms.devlang: 
ms.reviewer: kfend
# ms.tgt_pltfrm: 
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
# ms.search.industry: 
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611

---

# Workforce metrics Power BI content

[!include [banner](../includes/banner.md)]

This topic describes the **Workforce metrics** Microsoft Power BI content. It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.

## Accessing the Power BI content
The **Workforce metrics** Power BI content appears in the **Personnel management** workspace if you use one of these products:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## Metrics that are included in the Power BI content
The following table lists the metrics that are shown on each report.

| Report                                           | Metrics |
|--------------------------------------------------|---------|
| People Metrics                                   | Summary of other reports |
| Headcount Analysis Company, Department, Location | Headcount by company, headcount by department, headcount by location, and total headcount |
| Headcount Analysis Job, Step, Manager            | Headcount by job, headcount by step, headcount by manager, and total headcount |
| Headcount Trend Analysis                         | Headcount this year versus last year by company and rolling headcount for the last 12 months |
| FTE Analysis                                     | Total full-time equivalent (FTE), total assigned FTE, FTE by department, FTE for the last 12 months, and FTE by job |
| Workforce Demographics                           | Headcount by age and gender, headcount by ethnic origin, headcount by veteran status, headcount by marital status, number of full-time students, average tenure, average age, ratio of female to male employees, and languages spoken by employees |
| Position Analysis                                | Open positions by department, open-to-filled positions, active-to-inactive positions, and positions by department |
| Attrition Analysis                               | Attrition this year versus last year, attrition, exiting employees by age and gender, average tenure of employees leaving, employees exiting this month, and employees leaving by reason |
| People by department                             | Employees with a personnel number by department, position, and assignment start and end dates |
| Seniority Analysis                               | Average tenure, average years of service by company, and seniority list |
| Employee Anniversaries                           | Anniversaries this month, anniversaries next month, employees by years of service, and anniversaries, years of service by department |
| Employee Birthdays                               | Birthdays this month, birthdays next month, employee birthdays, and birthdays by month and department |
| Mass Hire Projects                               | Total mass hire projects, mass hire projects by status, mass hire projects by department and owner, mass hire projects by job, and mass hire projects |

You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard. For more information about how to filter and pin in Power BI, see [Create and configure a dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Be sure to download the **Workforce metrics** Power BI content that applies to the version of Microsoft Dynamics 365 that you're using.

> [!NOTE]
> The .pbix files available in Lifecycle Services apply to Finance and Operations apps only.

## Understanding the data model and entities
The following table shows the entities that the content was based on.

| Entity                   | Contents                                                                            | Relationships with other entities |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Calendar Offset          | Calendar offsets to slice reports                                                   | Past Position Assignment, Position Trend, Employee Trend, Terminated Employee |
| Company                  | Companies to filter reports by                                                      | Current Employee, Terminated Employee, Employee Trend |
| Current Position         | Positions as of the current date, FTE, open positions, and open-to-filled positions | Job, Position |
| Current Employee         | Workers as of the current date, age, and headcount                                  | Company, Geographic Location, Employee Name, Reports To, Employee Title, Demographics, Job, Employment, Position |
| Date                     | Days, weeks, months, and years                                                      | Past Position Assignment, Position Trend, Terminated Employee, Employee Trend |
| Demographics             | Date of birth, gender, ethnic origin, and marital status                            | Current Employee, Terminated Employee, Employee Trend |
| Employment               | Start date, end date, and transition date                                           | Current Employee, Terminated Employee, Employee Trend |
| Geographic Location      | City, county, postal code, and state or province                                    | Current Employee, Terminated Employee, Employee Trend |
| Job                      | Function, type, and title                                                           | Current Position, Current Employee |
| Past Position Assignment | Assignment reason, start date, end date, and job                                    | Calendar Offset, Date, Job, Position |
| Position                 | Department, FTE, position, position type, and title                                 | Current Position, Current Employee |
| Position Trend           | Positions over time, FTE, and job                                                   | Calendar Offset, Date, Job, Position |
| Reports To               | First name, last name, and full name                                                | Current Employee, Terminated Employee, Employee Trend |
| Terminated Employee      | Terminated workers, termination date, title, position, and job                      | Company, Geographic Location, Employee Name, Reports To, Calendar Offset, Date, Employee Title, Demographics, Employment, Job, Position |
| Employee Name            | First name, last name, and full name                                                | Current Worker, Terminated Employee, Employee Trend |
| Employee Title           | Title and seniority date                                                            | Current Employee, Terminated Employee, Employee Trend |
| Employee Trend           | Workers over time, headcount, company, and position                                 | Company, Geographic Location, Employee Name, Reports To, Calendar Offset, Date, Employee Title, Demographics, Employment, Job |
| Mass Hire Project        | Number of mass hire projects, project owner, and project status                     | Company, Mass Hire Line |
| Mass Hire Line           | Department, employment type, and position                                           | Date, Job, Mass Hire Project |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]