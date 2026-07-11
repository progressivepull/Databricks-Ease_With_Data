# 45 Metric Views in Databricks Unity Catalog

**Metric Views in Databricks Unity Catalog and AI/BI Dashboards**

This lesson introduces **Metric Views** in **Databricks Unity Catalog**, a semantic modeling feature that allows organizations to define **centralized, reusable, governed business metrics**. Instead of repeatedly writing complex SQL calculations, business logic is defined once in a Metric View and reused consistently across SQL queries, dashboards, and BI tools. This creates a single source of truth for KPIs and improves reporting accuracy.

**What is a Metric View?**

A Metric View is a semantic layer that contains:

- **Dimensions** – descriptive fields used for grouping and filtering (Order Date, Order Status, Customer Segment, Year, etc.)

- **Measures** – calculated business metrics (Total Orders, Total Sales, Profit, Average Price, etc.)

Rather than exposing raw tables, Metric Views expose meaningful business concepts that analysts can easily use.

**Why Metric Views are Important**

Metric Views solve several common reporting problems:

- Business logic is written once.

- Everyone uses identical KPI calculations.

- SQL becomes much simpler.

- Reports remain consistent across departments.

- Governance and permissions are centralized.

For example, instead of every analyst writing:

COUNT(DISTINCT o_orderkey)

they simply use:

measure(total_orders)

The calculation is already defined inside the Metric View.

**Metric View Definition**

Metric Views are created using **YAML**.

The YAML defines:

- Source table

- Dimensions

- Measures

- Joins

- Expressions

- Window calculations

Example:

Source:\
Orders_Raw\
\
Dimensions:\
Order Date\
Order Status\
Order Year\
\
Measures:\
Total Orders\
Total Price

The Metric View itself behaves like a reusable semantic table.

**Defining Dimensions**

The instructor creates several dimensions:

- Order Key

- Order Date

- Order Priority

- Order Status

- Order Year

Dimensions are used for:

- GROUP BY

- Filters

- Visualizations

Example:

Order Status

maps directly to

o_orderstatus

inside the table.

**Creating Calculated Dimensions**

Metric Views can also contain business logic.

Example:

Raw values:

O\
F\
P

become readable values:

Open\
Fulfilled\
Processing

using a CASE expression.

Instead of every report translating codes, the Metric View automatically provides readable values.

**Creating Measures**

Several reusable measures are created.

Examples include:

- Total Price

SUM(total_price)

- Total Orders

COUNT(DISTINCT order_key)

These calculations become reusable measures that users access through the measure() function.

**Querying Metric Views**

Unlike normal tables, Metric Views do **not** allow:

SELECT \*

Instead, queries explicitly request dimensions and measures.

Example:

SELECT\
measure(total_orders)\
FROM orders_metric_view

Grouping is simple:

SELECT\
order_status_readable,\
measure(total_orders)\
GROUP BY order_status_readable

Users never rewrite aggregation logic.

**Window-Based Measures**

The lesson demonstrates advanced measures using windows.

Examples include:

- Current Year Orders

- Previous Year Orders

Window properties include:

- Order by Year

- Current range

- Trailing one year

- Last value

This allows Metric Views to perform sophisticated time-based calculations without requiring analysts to write window functions manually.

**Year-over-Year (YoY) Calculations**

Additional measures include:

- Current Year Orders

- Previous Year Orders

- Year-over-Year Growth

- Year-over-Year Growth Percentage

Growth calculation:

Current Year\
-\
Previous Year

Growth Percentage:

(Current - Previous)\
/ Current\
× 100

These measures reuse existing measures rather than redefining calculations.

**Reusing Measures**

Existing measures can reference one another.

Example:

measure(Current Year Orders)\
-\
measure(Previous Year Orders)

This avoids duplicating SQL and keeps calculations consistent.

**Joining Dimension Tables**

Metric Views support joins.

Example:

Orders (Fact)\
LEFT JOIN\
Customer (Dimension)

The instructor joins:

Orders_Raw

with

Customer_Raw

using Customer Key.

This enables new dimensions such as:

- Customer Market Segment

without requiring users to perform joins themselves.

**Handling Business Rules**

Metric Views can standardize data cleaning.

Example:

NULL

becomes

Others

using a CASE expression.

Every report automatically follows this rule, improving consistency across dashboards.

**Metric Views as Semantic Models**

The lesson emphasizes that Metric Views act as a semantic model by:

- Centralizing business logic

- Standardizing KPI calculations

- Eliminating duplicated SQL

- Providing reusable metrics

- Serving as the organization's single source of truth

Anyone using the Metric View receives the same results.

**AI/BI Dashboards**

The second part demonstrates building **AI/BI Dashboards** using Metric Views.

Because business logic already exists, creating reports becomes much easier.

Examples include:

- KPI cards

- Bar charts

- Line charts

- Area charts

- Trend reports

Dashboard creators simply choose dimensions and measures without writing SQL.

**Benefits Over Raw SQL**

Without Metric Views:

Every dashboard developer must know:

- COUNT DISTINCT

- SUM

- CASE

- Window functions

- Joins

With Metric Views:

Developers simply select:

Total Orders

or

Year-on-Year Growth

The calculations are already defined.

**Interactive Dashboards**

Dashboards support:

- Filters

- Drill-down

- Cross-filtering

- Multiple visualizations

- Semantic model integration

Selecting one chart automatically filters the others.

**AI Forecasting**

Databricks AI/BI Dashboards include forecasting.

The dashboard can:

- Analyze historical trends

- Predict future values

- Display confidence intervals

- Automatically generate forecasting SQL

The instructor shows forecasting total orders by year using the built-in AI_FORECAST function, enabling predictive analytics with minimal manual effort.

**Publishing Dashboards**

Before users can access dashboards, they must be published.

Publishing options include:

- Embed creator credentials

- Use viewer permissions

- Share dashboards

- Schedule refreshes

- Enable Genie integration

Embedding credentials allows viewers to inherit the creator's data access, while viewer permissions enforce each user's own security policies.

**Consumer Access**

The lesson demonstrates configuring **Consumer Access** for business users.

Consumer users receive:

- Dashboard access

- Genie access

They do **not** receive:

- Workspace development access

- SQL development access

- Cluster creation permissions

This creates a simplified interface focused on consuming reports rather than developing them.

**Key Takeaways**

- **Metric Views** provide a governed semantic layer for business metrics.

- They centralize reusable **dimensions** and **measures**.

- Business logic is defined once and reused everywhere.

- Queries reference metrics using the **measure()** function instead of rewriting SQL.

- Metric Views support **joins**, **window functions**, **calculated fields**, and **data cleansing**.

- They ensure consistent KPI calculations across dashboards and BI tools.

- **AI/BI Dashboards** integrate directly with Metric Views for rapid visualization.

- Built-in **AI Forecasting** enables predictive analytics with automatically generated SQL.

- **Consumer Access** allows business users to securely view dashboards without development privileges.

# [README](./../../../README.md)
