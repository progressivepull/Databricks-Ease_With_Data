# ANSWER 26 1

**Question 1**

**What is the primary purpose of Delta Live Tables (DLT) in Databricks?**

**A. To manually configure Spark clusters for every ETL job ❌ Incorrect**

- This is the opposite of DLT's goal.

- Without DLT, engineers often need to:

  - Create clusters

  - Configure clusters

  - Schedule jobs

  - Handle retries

- DLT automates these operational tasks.

**B. To simplify ETL development by automatically managing pipeline operations while developers define transformations ✅ Correct**

This is exactly why DLT exists.

Instead of worrying about infrastructure, developers simply define:

- where data comes from

- how data is transformed

- where data goes

DLT automatically manages:

- cluster creation

- orchestration

- scheduling

- dependency tracking

- retries

- monitoring

- optimization

Think of DLT as an **autopilot for ETL pipelines**.

Instead of driving the car, you only tell it the destination.

**C. To replace Delta Lake with Parquet files ❌ Incorrect**

DLT actually **uses Delta Lake**.

Delta Lake provides:

- ACID transactions

- Time Travel

- Schema enforcement

- Schema evolution

DLT builds pipelines **on top of Delta Lake**, not instead of it.

**D. To create dashboards directly from raw data ❌ Incorrect**

Dashboards are typically created using:

- Databricks SQL

- Power BI

- Tableau

- Looker

DLT prepares the data.

Visualization happens later.

**E. To manage Azure storage accounts only ❌ Incorrect**

DLT works across cloud platforms:

- Azure

- AWS

- Google Cloud

It is not an Azure storage management tool.

**Why B is correct**

DLT allows developers to focus on **business logic**, while Databricks manages the operational complexity of running reliable ETL pipelines.

# [README](./../../../README.md)
