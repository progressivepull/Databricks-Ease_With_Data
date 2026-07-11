# 41 Data Warehousing using DBSQL

**Data Warehousing using Databricks SQL (DBSQL)**

This lesson introduces **Databricks SQL (DBSQL)** and **SQL Warehouses**, the analytics layer of the Databricks Lakehouse Platform. While previous lessons focused on Data Engineering, this lesson shifts to the **Data Analyst** persona, showing how SQL Warehouses provide a high-performance, scalable environment for running analytical (OLAP) queries, integrating with BI tools, monitoring query performance, and creating visualizations.

------------------------------------------------------------------------

**1. What is Databricks SQL (DBSQL)?**

Databricks SQL (DBSQL) is the SQL analytics service built on the Databricks Lakehouse.

It enables users to:

- Run ANSI SQL queries

- Analyze Delta tables

- Build reports

- Create dashboards

- Connect BI tools

- Perform OLAP analytics

Because Databricks uses ANSI-compliant SQL throughout the platform, the same SQL language is used for permissions, DLT, Auto Loader, Unity Catalog, and analytics.

------------------------------------------------------------------------

**2. SQL Warehouses**

A **SQL Warehouse** is the compute engine that executes SQL queries.

Workflow:

SQL Query\
\
↓\
\
SQL Warehouse\
\
↓\
\
Lakehouse\
\
↓\
\
Results

SQL Warehouses are optimized for analytics, concurrency, and BI workloads.

------------------------------------------------------------------------

**3. Lakehouse Architecture**

Databricks combines:

Data Lake\
\
+\
\
Data Warehouse\
\
↓\
\
Lakehouse

Because Delta Lake provides warehouse capabilities on top of cloud storage, organizations can perform data engineering and business intelligence on the same platform.

------------------------------------------------------------------------

**4. Types of SQL Warehouses**

Databricks provides three warehouse types.

**Serverless**

Features:

- Photon Engine

- Predictive I/O

- Intelligent Workload Management

- Fully managed compute

Recommended for most workloads.

**Pro**

Features:

- Dedicated clusters

- More manual management

- Fewer optimizations

------------------------------------------------------------------------

**Classic**

Legacy option with the fewest optimization features.

------------------------------------------------------------------------

**5. Why Serverless Warehouses?**

Serverless SQL Warehouses provide:

- Automatic infrastructure management

- Fast startup

- Intelligent scaling

- Better query performance

- Lower operational overhead

Databricks manages the compute automatically, allowing users to focus on SQL and analytics.

------------------------------------------------------------------------

**6. Photon Engine**

Serverless warehouses use the **Photon Engine**.

Benefits include:

- Vectorized query execution

- Faster SQL processing

- Improved DataFrame performance

- Reduced execution time

In query profiles, Photon execution appears as highlighted execution stages.

------------------------------------------------------------------------

**7. Predictive I/O**

Predictive I/O improves data scanning efficiency.

Benefits:

- Faster reads

- Better storage access

- Reduced query latency

This optimization is available with Serverless Warehouses.

------------------------------------------------------------------------

**8. Intelligent Workload Management**

Serverless Warehouses automatically manage concurrent SQL workloads.

Features include:

- Resource balancing

- Query scheduling

- Automatic optimization

- Reduced queue times

This allows many users to execute queries simultaneously with minimal manual tuning.

------------------------------------------------------------------------

**9. SQL Editor**

DBSQL provides a dedicated SQL Editor.

Capabilities include:

- Write SQL queries

- Save queries

- Schedule queries

- Create visualizations

Compared to notebooks, the SQL Editor is designed specifically for analytics and reporting workflows.

------------------------------------------------------------------------

**10. Creating a SQL Warehouse**

When creating a warehouse, users configure:

- Warehouse name

- Cluster size

- Auto Stop

- Scaling

- Warehouse type

- Tags

After creation, the warehouse is immediately available for SQL workloads.

------------------------------------------------------------------------

**11. Cluster Size**

Warehouse size determines available compute resources.

Example:

2X-Small\
\
↓\
\
4 DBUs/hour

Larger warehouses support heavier analytical workloads and more concurrent users.

------------------------------------------------------------------------

**12. Scaling**

SQL Warehouses support multiple clusters.

Example:

Warehouse\
\
↓\
\
Cluster 1\
\
Cluster 2\
\
Cluster 3

Increasing the number of clusters enables higher query concurrency by distributing workloads.

------------------------------------------------------------------------

**13. Auto Stop**

Warehouses automatically stop after a configurable idle period.

Benefits:

- Reduced cost

- No manual shutdown

- Efficient resource utilization

------------------------------------------------------------------------

**14. BI Tool Integration**

SQL Warehouses integrate directly with BI tools.

Examples:

- Power BI

- Tableau

Connection information includes:

- Hostname

- HTTP Path

- JDBC URL

These details allow external analytics tools to query the Lakehouse through the SQL Warehouse.

------------------------------------------------------------------------

**15. Monitoring**

Each warehouse includes a monitoring interface.

Users can monitor:

- Running queries

- Queued queries

- Cluster usage

- Query history

This helps administrators understand workload patterns and diagnose performance issues.

------------------------------------------------------------------------

**16. Query Example**

The lesson demonstrates a SQL query that:

- Joins Orders and Customer tables

- Filters active SCD Type 2 customer records

- Groups by Market Segment

- Counts total orders

Result:

Market Segment\
\
↓\
\
Total Orders

This illustrates a typical OLAP aggregation query.

------------------------------------------------------------------------

**17. Query Profile**

After execution, users can inspect the **Query Profile**.

It displays:

- Query execution plan

- Time spent in each stage

- Memory usage

- Rows processed

- Data scanned

This provides valuable information for SQL tuning and optimization.

------------------------------------------------------------------------

**18. Spark UI Integration**

For deeper analysis, Query Profiles link directly to the Spark UI.

Spark UI provides:

- DAG visualization

- Stage details

- Task execution

- Shuffle information

- Photon execution

- Resource usage

This enables detailed performance troubleshooting.

------------------------------------------------------------------------

**19. Query History**

Every executed query is stored.

History includes:

- SQL text

- Execution time

- User

- Warehouse

- Performance details

This makes it easy to review and troubleshoot previous executions.

------------------------------------------------------------------------

**20. Saved Queries**

Queries can be saved for future use.

Benefits:

- Reusable SQL

- Easier collaboration

- Centralized query management

Saved queries can also be scheduled.

------------------------------------------------------------------------

**21. Scheduling Queries**

Saved queries support scheduled execution.

Example:

Saved Query\
\
↓\
\
Schedule\
\
↓\
\
Automatic Refresh

This is useful for recurring reports and dashboards that need fresh data.

------------------------------------------------------------------------

**22. Visualizations**

The SQL Editor can generate charts directly from query results.

Supported visualizations include:

- Bar charts

- Line charts

- Other chart types

These visualizations can be saved alongside the query and reused in dashboards.

------------------------------------------------------------------------

**23. SQL in Notebooks**

SQL Warehouses can also power notebooks.

Workflow:

Notebook\
\
↓\
\
SQL Warehouse\
\
↓\
\
Lakehouse\
\
↓\
\
Results

When a notebook is connected to a SQL Warehouse:

- Only SQL cells are supported.

- Performance and monitoring are the same as in the SQL Editor.

------------------------------------------------------------------------

**24. SQL Warehouses vs All-Purpose Clusters**

| **Feature**          | **SQL Warehouse**      | **All-Purpose Cluster**   |
|----------------------|------------------------|---------------------------|
| Primary Use          | Analytics (OLAP)       | Engineering & Development |
| SQL Optimization     | Yes                    | General-purpose           |
| BI Tool Connectivity | Yes                    | Limited                   |
| Concurrent Queries   | Optimized              | Less optimized            |
| Photon Engine        | Supported (Serverless) | Depends on configuration  |
| Visualizations       | Built in               | Notebook-based            |

------------------------------------------------------------------------

**Best Practices**

- Use **Serverless SQL Warehouses** whenever available to benefit from Photon Engine, Predictive I/O, Intelligent Workload Management, and automatic infrastructure management.

- Select an appropriate **warehouse size** and **cluster scaling configuration** based on expected concurrency and workload volume.

- Connect BI tools such as **Power BI** and **Tableau** through SQL Warehouses instead of querying data directly.

- Regularly review the **Query Profile** and **Spark UI** to identify bottlenecks, monitor memory usage, and optimize SQL performance.

- Save frequently used SQL queries and schedule them to automate recurring reports and dashboards.

- Use the SQL Editor for dedicated analytics workflows, while continuing to use notebooks when combining SQL with other languages or data engineering tasks.

# [README](./../../../README.md)
