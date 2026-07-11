# ANSWER 44 10

**Question 10**

**What is the difference between a Query Schedule and an Alert Schedule?**

**A. They are the same schedule managed together.** ❌ Incorrect

- They serve different purposes.

**B. The Query Schedule refreshes dashboards, while the Alert Schedule refreshes Materialized Views.** ❌ Incorrect

- Neither schedule refreshes Materialized Views.

**C. The Query Schedule executes the saved query, while the Alert Schedule determines when the alert condition is evaluated.** ✅ Correct

Think of them as two independent schedules.

**Query Schedule**

Runs SQL

Every Hour

│

Execute Query

**Alert Schedule**

Checks condition

Every 15 Minutes

│

Evaluate:

Sales \< Target?

The schedules can be configured separately depending on monitoring needs.

**D. The Query Schedule only works with notebooks, while the Alert Schedule only works with SQL Warehouses.** ❌ Incorrect

- Query schedules are associated with saved SQL queries, not notebooks.

**E. The Query Schedule creates notifications, while the Alert Schedule creates SQL queries.** ❌ Incorrect

- Notifications are generated only after the alert evaluates the query results against its condition.

**Key Concept**

- **Query Schedule** = Runs the SQL query.

- **Alert Schedule** = Evaluates the alert condition and determines whether to notify.

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **SQL Alerts** | Monitor SQL query results and send notifications when conditions are met. |
| **Common Uses** | Business KPIs, pending orders, inventory, ETL monitoring, and data quality checks. |
| **Foundation** | Every SQL Alert is built on a **saved SQL query**. |
| **Execution Engine** | The attached **SQL Warehouse** executes the query. |
| **Alert Conditions** | Use comparison operators such as \>, \<, =, \>=, and \<=. |
| **Triggered Status** | If the condition evaluates to **TRUE**, the alert becomes **Triggered** and can send a notification. |
| **Alert Fatigue Prevention** | Alerts typically **trigger once until the condition returns to normal**, avoiding repeated notifications while the issue persists. |
| **Supported Destinations** | Email, Slack, Microsoft Teams, and PagerDuty are supported; GitHub Issues is not a built-in destination. |
| **Who Configures Destinations?** | **Workspace Administrators** create and manage notification destinations. |
| **Schedules** | **Query Schedule** runs the SQL query; **Alert Schedule** determines when the query results are evaluated against the alert condition. |

# [README](./../../../README.md)
