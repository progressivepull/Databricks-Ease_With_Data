# ANSWER 26 2

**Question 2**

**Which of the following operational tasks is automatically managed by Delta Live Tables?**

**A. Writing SQL queries ❌ Incorrect**

DLT cannot write your SQL.

You still create the transformation logic.

Example:

SELECT \*

FROM customers

WHERE active = true

You write that.

DLT executes it.

**B. Creating business logic ❌ Incorrect**

Business rules are always written by developers.

For example:

- filter inactive customers

- calculate sales tax

- join customer tables

DLT does not invent these rules.

**C. Pipeline orchestration, cluster management, and dependency tracking ✅ Correct**

DLT automatically manages:

- cluster lifecycle

- scheduling

- execution order

- retries

- dependency graph

- monitoring

Example:

Bronze

↓

Silver

↓

Gold

DLT figures out the execution order automatically.

**D. Designing Power BI reports ❌ Incorrect**

Power BI is a reporting tool.

DLT prepares the data.

**E. Creating cloud storage accounts ❌ Incorrect**

Storage accounts are cloud infrastructure.

DLT does not provision cloud resources.

**Why C is correct**

DLT automates the operational aspects of ETL pipelines so developers can focus on transforming data.

# [README](./../../../README.md)
