# IT Ticket Analysis using Excel

## Project Overview

This project analyzes IT support ticket data to understand ticket demand, resolution efficiency, employee satisfaction, and IT agent performance.

The analysis was carried out in Microsoft Excel using data cleaning, formulas, PivotTables, charts, and an interactive dashboard. The main objective was to identify operational bottlenecks and determine where process, technology, training, or staffing improvements could have the greatest impact.

The dataset contains **97,498 IT support tickets** handled by **50 IT agents** between 2016 and 2020.

---

## Business Problem

As IT support demand increases, an organization needs to ensure that tickets continue to be resolved efficiently without affecting service quality.

This analysis focuses on answering questions such as:

- How has IT ticket demand changed over time?
- Which types of requests generate the most workload?
- How quickly are tickets being resolved?
- Are high-severity tickets taking longer to resolve?
- How satisfied are employees with IT support?
- Is workload distributed evenly among IT agents?
- Are there noticeable differences in agent performance?
- Should future investment focus on hiring, training, or improving ticket-management processes?

---

## Dataset

The project uses two source tables:

### Tickets

- **97,498 records**
- **11 original attributes**
- Contains information about ticket dates, request categories, issue types, severity, priority, resolution time, satisfaction ratings, and assigned agents.

### IT Agents

- **50 agent records**
- **6 attributes**
- Contains agent information such as Agent ID, name, email, and date-of-birth fields.

Additional fields were created during the analysis where required.

---

## Tools and Excel Skills Used

**Tool:** Microsoft Excel

Techniques used throughout the project include:

- Data cleaning and validation
- Excel Tables
- PivotTables
- PivotCharts
- Slicers
- `COUNTIF`
- `SUMIF`
- `INDEX` / `MATCH`
- Lookup operations
- `AVERAGE`
- `CORREL`
- `DATEDIF`
- `MID` and `FIND`
- Date-based analysis
- Conditional aggregation
- Sorting and filtering
- Data-type validation
- Duplicate and missing-value checks
- Interactive dashboard creation

---

## Data Preparation

Before performing the analysis, the dataset was checked for data-quality issues.

The preparation process included:

1. Reviewing missing values
2. Checking for duplicate records
3. Validating data types
4. Reviewing categorical values for inconsistencies
5. Correcting inconsistent category labels
6. Creating additional fields required for analysis
7. Linking ticket records with agent information

Some of the derived fields included:

- Agent Name
- Year
- Month
- Age
- Age Group
- Email Domain
- Severity Score

The cleaned data was then used to create PivotTables, charts, KPIs, and the final dashboard.

---

## Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Tickets | 97,498 |
| Total IT Agents | 50 |
| Average Resolution Time | 4.55 days |
| Average Satisfaction | ~4.1 / 5 |
| Average Severity Score | 2.05 |
| Average Priority Score | 1.59 |
| Average Agent Age | 41.06 years |

These KPIs provide a high-level view of IT support demand, service quality, and workforce performance.

---

## Analysis and Findings

### 1. Ticket Demand Increased Significantly

Annual ticket volume increased throughout the five-year period:

| Year | Tickets |
|---|---:|
| 2016 | 13,051 |
| 2017 | 14,915 |
| 2018 | 18,954 |
| 2019 | 21,490 |
| 2020 | 29,088 |

Ticket volume increased by approximately **123% between 2016 and 2020**.

This indicates growing pressure on IT support operations and suggests that support capacity, automation, and processes should be reviewed as demand continues to increase.

---

### 2. System Requests Generate the Highest Workload

Ticket distribution by request category:

| Request Category | Tickets |
|---|---:|
| System | 39,002 |
| Login Access | 29,193 |
| Software | 19,570 |
| Hardware | 9,733 |

**System** requests represent the largest category, followed by **Login Access**.

These high-volume categories may provide opportunities for standardized workflows, automation, FAQs, or self-service solutions.

---

### 3. Most Tickets Are IT Requests

The dataset contains:

- **73,220 IT Requests**
- **24,278 IT Errors**

IT Requests account for approximately **75% of all tickets**.

Repeated service requests may therefore be a useful area to investigate for automation or self-service support.

---

### 4. Resolution Performance

The overall average resolution time is:

**4.55 days**

Resolution times were also analyzed across request categories.

Hardware requests consistently showed higher average resolution times than the other request categories, making hardware support a potential operational bottleneck.

Possible areas for further investigation include:

- Hardware availability
- Replacement procedures
- Vendor dependencies
- Escalation processes

---

### 5. Severity Does Not Strongly Predict Resolution Time

The Pearson correlation between severity score and resolution time was approximately:

**r = -0.0405**

This indicates almost no linear relationship between ticket severity and resolution time.

Interestingly, urgent tickets were resolved faster than some lower-severity categories, suggesting that critical tickets were being prioritized effectively.

---

### 6. Employee Satisfaction Remained Strong

Approximately **80.3% of tickets received satisfaction ratings of 4 or 5**.

Despite increasing ticket demand, overall satisfaction remained relatively strong.

This suggests that service quality was being maintained, although low-rated tickets should still be investigated to identify recurring service issues.

---

### 7. Priority Assignment Needs Improvement

A significant finding was the number of tickets without an assigned priority:

**29,410 tickets were classified as Unassigned.**

This represents roughly **30% of all tickets**.

Improving ticket classification and introducing automated priority-assignment or routing rules could reduce this issue and improve workflow consistency.

---

### 8. Agent Workload Is Relatively Balanced

Ticket volume was distributed fairly evenly across the 50 agents.

- Highest ticket count: **2,027**
- Lowest ticket count: **1,856**
- Difference: **171 tickets**

Ticket count alone therefore does not indicate that any individual agent is significantly overloaded.

However, agent performance varies when resolution time, satisfaction, and ticket complexity are considered together.

This means agent performance should not be evaluated using ticket volume alone.

---

## Dashboard

An interactive Excel dashboard was created to bring the major findings into a single view.

The dashboard includes:

- Overall KPIs
- Ticket-volume trends
- Resolution-time analysis
- Request-category analysis
- Issue-type distribution
- Severity and priority analysis
- Satisfaction analysis
- Agent-performance analysis
- Interactive slicers for exploring the data

### Dashboard Preview

![IT Ticket Analysis Dashboard](https://github.com/Mehwish4610/excel-it-ticket-analysis/blob/main/Screenshot%202026-08-19%20001615.png)

---

## Recommendations

Based on the analysis, the following actions were identified:

### Improve ticket routing and priority assignment

A large number of tickets have no assigned priority. Automated classification, routing, and escalation rules could improve consistency and reduce manual effort.

### Focus automation on high-volume requests

System and Login Access requests generate a large proportion of the total workload. Repetitive requests in these categories could be candidates for self-service or automated workflows.

### Investigate hardware resolution delays

Hardware requests consistently take longer to resolve. Hardware availability, replacement procedures, vendor dependencies, and escalation processes should be reviewed.

### Use targeted agent training

Rather than applying the same training to the entire team, training can be focused on agents showing relatively high resolution times or lower satisfaction scores.

### Monitor capacity before increasing headcount

Current workload is relatively evenly distributed across agents. Based on this analysis, immediate large-scale hiring is not the first priority.

However, ticket volume should continue to be monitored because demand increased considerably during the period analyzed.

---

## Project Files

```text
excel-it-ticket-analysis/
│
├── README.md
│
├── images/
│   └── dashboard.png
│
├── report/
│   └── IT_Tickets_Project_Report.pdf
│
└── presentation/
    └── IT_Tickets_Presentation.pdf
```

> **Note:** The complete Excel workbook contains 97,498 ticket records and is not included in this repository due to its file size. The repository includes the project documentation, analysis results, dashboard preview, and presentation.

---

## What I Learned

This project helped me move beyond using Excel only for calculations and understand how it can be used for an end-to-end data analysis workflow.

Through the project, I gained practical experience in:

- Cleaning and validating a large dataset
- Structuring data for analysis
- Using PivotTables to answer business questions
- Working with lookup and aggregation functions
- Analyzing trends across time
- Comparing performance using multiple metrics
- Building an interactive Excel dashboard
- Turning analysis results into business recommendations

One of my main takeaways was that a single metric rarely tells the full story. For example, agent ticket volume appeared relatively balanced, but combining workload with resolution time, satisfaction, and ticket complexity provided a much more useful view of performance.

---

## Future Improvements

If I extend this project, I would like to:

- Recreate the analysis using SQL
- Build an equivalent dashboard in Power BI
- Compare Excel, SQL, and Power BI workflows
- Perform deeper analysis of the factors affecting resolution time
- Explore automated ticket categorization and routing

---

## Author

**Mehwish**

Aspiring Data Scientist | Data Analytics | Python | SQL | Excel
