# ANSWER 45 10

**Question 10**

**What permissions are typically granted to users with Consumer Access?**

**A. Full workspace development and cluster creation privileges** ❌ Incorrect

- Consumer users don't develop code.

**B. SQL development and notebook editing permissions** ❌ Incorrect

- Developers receive these permissions.

**C. Dashboard and Genie access without development or cluster management privileges** ✅ Correct

Consumer Access is designed for business users.

Typical capabilities:

✅ View dashboards

✅ Use AI/BI Genie

✅ Consume reports

They generally cannot:

❌ Create clusters

❌ Edit notebooks

❌ Develop pipelines

**D. Metastore Administrator permissions** ❌ Incorrect

- Metastore Admins manage Unity Catalog.

**E. Unity Catalog ownership of all Metric Views** ❌ Incorrect

- Consumers are not owners.

**Key Concept**

Think:

Developer

- Build

Consumer

- View

------------------------------------------------------------------------

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **Metric View** | A centralized, governed semantic layer that defines reusable business metrics and dimensions. |
| **Core Components** | **Dimensions** (grouping fields such as Customer, Region, Year) and **Measures** (calculations such as Revenue, Total Orders). |
| **Definition Format** | Metric Views are created using **YAML** definitions. |
| **Main Benefit** | Define business logic once and reuse it everywhere, ensuring consistent KPI calculations and reducing duplicate SQL. |
| **Referencing Measures** | Use the syntax **measure(metric_name)**, for example measure(total_orders). |
| **Query Limitation** | SELECT \* is **not supported** because Metric Views expose measures and dimensions rather than acting like standard tables. |
| **Advanced Analytics** | **Window-based measures** enable calculations such as Current Year vs. Previous Year, running totals, and moving averages. |
| **Built-in Joins** | Metric Views can include joins so dashboard developers don't have to write complex join logic themselves. |
| **AI/BI Dashboard Benefit** | Dashboards reuse predefined business logic instead of redefining complex SQL calculations in every report. |
| **Consumer Access** | Business users can access dashboards and AI/BI Genie without notebook editing, cluster management, or development privileges. |

# [README](./../../../README.md)
