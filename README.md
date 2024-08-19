
**Project Overview:**

We extracted data from various sources using Azure Data Studio, Azure SQL DB, and CosmosDB, storing the raw data in Data Lake storage under "srcsqlserver," "srccosmos," and "srcazuresql." We then cleaned and organized the data into an Operational Data Store (ODS), creating six key tables: Cases, Deaths, Recoveries, Policies, Geography, and Date.

**Schema Design:**

Initially, we used a star schema but later transitioned to a snowflake schema due to expanded data. The Policy table serves as the centralized fact table, with all others as dimension tables.

**Data Analysis:**

We standardized the Date/Time format across all tables, connected them by creating new columns, and calculated a 30-day rolling average and growth rate for cases and deaths. We analyzed the impact of different policies on these metrics and identified four optimal policies based on their effectiveness and stringency.

Here's a condensed version of your second report section for the README:


**Policy Analysis and Recommendations:**

Balancing policy effectiveness with nonrestrictiveness is essential for policy task forces. We compared policy stringency indices with cases per capita to optimize our recommendations. While PowerBI visualizations provided valuable insights, we exercised caution in their interpretation. For example, PowerBI suggested reopening schools to lower death rates—an unexpected result likely due to unaccounted factors.

PowerBI's tools were useful starting points, especially the key insights visual, which highlighted four key policies—[C1] School Closures, [E2] Debt Contract Relief, [H2] Testing, and [H6] Stay-at-Home Orders. We focused on policies with strong negative correlations with death and new case growth rates. Our analysis of global Covid-19 data identified school closings [C1] and debt contract relief [E2] as the most effective nonrestrictive policies. Although Germany’s testing policy [H2] showed high effectiveness, it was excluded due to its restrictive nature.

Our final recommendation aims to keep the 30-day rolling average growth rates of deaths below 1% and new cases below 3% while minimizing restrictions.
