# 44 Databricks SQL Alerts

**Databricks SQL Alerts**

This lesson explains **Databricks SQL Alerts**, a feature that automatically monitors SQL query results and sends notifications when specified conditions are met. SQL Alerts are useful for monitoring operational metrics, business KPIs, system health, and data quality by evaluating SQL query results on a schedule and notifying users through supported destinations such as email, Slack, Microsoft Teams, PagerDuty, or webhooks.

------------------------------------------------------------------------

**1. What are Databricks SQL Alerts?**

SQL Alerts automatically monitor SQL query results.

Workflow:

SQL Query\
\
↓\
\
Evaluate Result\
\
↓\
\
Condition Met?\
\
↓\
\
Send Notification

Instead of constantly checking dashboards manually, Databricks automatically informs users when important conditions occur.

------------------------------------------------------------------------

**2. Why Use SQL Alerts?**

SQL Alerts are useful whenever data must be monitored continuously.

Example use cases:

- Sensor failures

- High pending order counts

- Data quality issues

- Missing records

- Threshold violations

- Business KPI monitoring

Alerts help detect problems immediately instead of waiting for someone to manually review reports.

------------------------------------------------------------------------

**3. Query-Driven Alerts**

Every SQL Alert is based on a SQL query.

Example workflow:

Orders Table\
\
↓\
\
SQL Query\
\
↓\
\
Pending Order Count\
\
↓\
\
Alert

The query produces a result, and the alert evaluates that result against a condition.

------------------------------------------------------------------------

**4. Example Query**

The lesson creates a query that counts pending orders.

Logic:

Orders\
\
↓\
\
Filter Status = Pending\
\
↓\
\
COUNT()\
\
↓\
\
Pending Orders Count

This single numeric result becomes the value monitored by the alert.

------------------------------------------------------------------------

**5. SQL Warehouse**

Alerts execute queries using the **SQL Warehouse** attached to the saved query.

Workflow:

Saved Query\
\
↓\
\
SQL Warehouse\
\
↓\
\
Query Result\
\
↓\
\
Alert Evaluation

The warehouse runs automatically whenever the alert schedule triggers.

------------------------------------------------------------------------

**6. Saving the Query**

Before an alert can be created:

1.  Create SQL query

2.  Test query

3.  Save query

The saved query becomes the data source for the SQL Alert.

------------------------------------------------------------------------

**7. Creating an Alert**

Creating an alert requires:

- Alert name

- Saved SQL query

- Trigger condition

- Notification settings

- Schedule

- Destination

Once configured, Databricks evaluates the query automatically.

------------------------------------------------------------------------

**8. Trigger Conditions**

Alerts compare query results against a condition.

Supported operators include:

- Greater than

- Less than

- Equal

- Not equal

- Is NULL

Example:

Pending Orders\
\
↓\
\
Greater Than\
\
↓\
\
10,000

If the condition evaluates to **TRUE**, the alert is triggered.

------------------------------------------------------------------------

**9. Example Threshold**

The lesson configures:

Pending Orders\
\
\>\
\
10,000

Current result:

191,189

Because the result exceeds the threshold, the alert status becomes **Triggered**.

------------------------------------------------------------------------

**10. Handling Empty Results**

Alerts allow configuration of what happens when the query returns no rows.

Example:

No Results\
\
↓\
\
Treat as OK

This prevents unnecessary alerts when the absence of data is considered normal.

------------------------------------------------------------------------

**11. Notification Frequency**

Several notification behaviors are available.

Examples:

- Notify once

- Notify every evaluation

- Notify when returning to normal

The lesson chooses:

Trigger Once\
\
↓\
\
Wait Until Normal\
\
↓\
\
Allow Next Alert

This prevents repeated notifications while the condition remains unchanged.

------------------------------------------------------------------------

**12. Custom Alert Templates**

Alerts support custom notification messages.

Example:

Pending Orders Alert\
\
Pending Orders Count:\
191189

Dynamic placeholders can insert values from the SQL query into the notification.

------------------------------------------------------------------------

**13. Preview**

Before saving the template, Databricks provides a preview showing exactly what recipients will receive.

This helps verify formatting and variable substitution before enabling the alert.

------------------------------------------------------------------------

**14. Alert Status**

Possible statuses include:

- Unknown

- Triggered

- Normal

Initially:

Unknown

After refreshing:

Triggered

because the query result satisfies the configured condition.

------------------------------------------------------------------------

**15. Notification Destinations**

Databricks currently supports five destination types:

- Email

- Slack

- Webhook

- PagerDuty

- Microsoft Teams

These integrations allow alerts to reach operational teams through their preferred communication platforms.

------------------------------------------------------------------------

**16. Creating Destinations**

Notification destinations are created separately.

Navigation:

Workspace Settings\
\
↓\
\
Notifications\
\
↓\
\
Destinations

Only **Workspace Administrators** can create notification destinations.

------------------------------------------------------------------------

**17. Email Destination**

The lesson demonstrates an email destination.

Workflow:

SQL Alert\
\
↓\
\
Email Destination\
\
↓\
\
Recipient\
\
↓\
\
Notification

Once associated with an alert, Databricks automatically sends email notifications whenever the trigger condition is met.

------------------------------------------------------------------------

**18. Alert Schedule**

Each alert has its own independent schedule.

Workflow:

Schedule\
\
↓\
\
Run Query\
\
↓\
\
Evaluate Condition\
\
↓\
\
Send Alert

The alert schedule determines how often the SQL query is evaluated.

------------------------------------------------------------------------

**19. Alert Schedule vs Query Schedule**

An important distinction:

**Query Schedule**

Schedules execution of the saved SQL query.

**Alert Schedule**

Schedules evaluation of the alert condition.

These schedules are independent and managed separately.

------------------------------------------------------------------------

**20. End-to-End Architecture**

SQL Warehouse\
\
↓\
\
Saved Query\
\
↓\
\
Query Result\
\
↓\
\
Alert Condition\
\
↓\
\
Triggered?\
\
↓\
\
Notification Destination\
\
↓\
\
Email / Slack / Teams

The SQL Warehouse executes the query, Databricks evaluates the condition, and notifications are sent only when appropriate.

------------------------------------------------------------------------

**SQL Alerts Workflow**

| **Step**              | **Description**                       |
|-----------------------|---------------------------------------|
| Create SQL Query      | Produce a measurable result           |
| Save Query            | Store the query                       |
| Create Alert          | Associate query with an alert         |
| Configure Condition   | Define the threshold or rule          |
| Configure Destination | Select email, Slack, Teams, etc.      |
| Schedule Evaluation   | Define how often to check             |
| Trigger Notification  | Send alerts when the condition is met |

------------------------------------------------------------------------

**Supported Notification Destinations**

| **Destination** | **Purpose**                          |
|-----------------|--------------------------------------|
| Email           | Send alert emails                    |
| Slack           | Notify Slack channels                |
| Microsoft Teams | Send Teams messages                  |
| PagerDuty       | Incident management                  |
| Webhook         | Integrate with external applications |

------------------------------------------------------------------------

**Best Practices**

- Build alerts on **saved SQL queries** that return a clear metric or KPI to evaluate.

- Run alerts using a **SQL Warehouse** appropriate for the workload, since the warehouse executes the underlying query.

- Choose notification thresholds carefully to minimize false positives and alert fatigue.

- Use **custom alert templates** to include meaningful information, such as the metric value or query result, in notifications.

- Configure notification frequency thoughtfully—for example, notify **once until the condition returns to normal** to avoid repeated alerts for the same issue.

- Send alerts to the communication channel that best fits the operational workflow, such as **Email**, **Slack**, **Microsoft Teams**, **PagerDuty**, or a **Webhook** integration.

# [README](./../../../README.md)
