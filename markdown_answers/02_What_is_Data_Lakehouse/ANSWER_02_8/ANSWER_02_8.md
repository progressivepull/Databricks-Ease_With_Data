# ANSWER 02 8

What problem results from maintaining separate Data Lakes and Data Warehouses in traditional architectures?

A. Increased data quality\
B. Faster analytics performance\
C. Reduced storage costs\
**D. Multiple copies of the same data and synchronization issues**\
E. Better AI/ML integration

**Correct Answer: D**

**Understand the Core Concept First**

**Traditional Architecture**

Historically, organizations often maintained:

**Data Lake**

Used for:

- Raw data storage

- ETL processing

- Data engineering

- AI/ML workloads

**Data Warehouse**

Used for:

- Reporting

- Dashboards

- Business Intelligence (BI)

- Analytics

Architecture:

Source Systems\
↓\
Data Lake\
↓\
ETL Process\
↓\
Data Warehouse\
↓\
BI Reports

Notice the same data exists in multiple places.

This leads to:

- Duplicate data copies

- Synchronization issues

- Higher costs

- Multiple data owners

Databricks solves this by combining both into a **Lakehouse**.

------------------------------------------------------------------------

**A. Increased Data Quality ❌**

**Why it's wrong**

Having separate Data Lakes and Data Warehouses does not automatically improve data quality.

In fact, multiple copies often create quality problems.

**Example**

Customer data in the Data Lake:

John Smith

Customer data in the Warehouse:

Jon Smith

Which one is correct?

Now teams have conflicting versions.

**Real Problem**

More copies often mean:

- More inconsistencies

- More confusion

- More reconciliation work

**Exam Tip**

Multiple copies usually decrease consistency rather than improve quality.

------------------------------------------------------------------------

**B. Faster Analytics Performance ❌**

**Why it's wrong**

This is generally considered a benefit, not a problem.

The question asks:

"What problem results?"

Faster analytics is not a problem.

Also, moving data between systems can actually slow overall processes.

**Example**

Lake\
↓\
ETL\
↓\
Warehouse\
↓\
Dashboard

Each transfer adds time and complexity.

**Exam Tip**

If an option sounds like an advantage, it is probably not the answer.

------------------------------------------------------------------------

**C. Reduced Storage Costs ❌**

**Why it's wrong**

Separate systems usually increase storage costs.

Why?

Because data gets copied.

Example:

10 TB in Data Lake\
10 TB in Data Warehouse

Total:

20 TB stored

You pay for both copies.

**Databricks Goal**

Lakehouse aims to reduce duplication:

One Data Copy\
↓\
Used by BI and AI/ML

**Exam Tip**

Duplicate data = Higher storage costs, not lower.

------------------------------------------------------------------------

**D. Multiple Copies of the Same Data and Synchronization Issues ✅**

**Why it's correct**

This is one of the biggest problems Databricks highlights.

**Problem 1: Duplicate Data**

The same dataset may exist in:

Data Lake\
Warehouse\
Reporting Database\
ML Environment

Now there are several copies.

------------------------------------------------------------------------

**Problem 2: Synchronization**

Whenever data changes:

Update Data Lake\
↓\
Update Warehouse\
↓\
Update Reports

If one update fails:

Lake = New Data\
Warehouse = Old Data

Reports become inaccurate.

------------------------------------------------------------------------

**Problem 3: Multiple Owners**

Different teams manage different copies.

Example:

| **Team**         | **System**      |
|------------------|-----------------|
| Data Engineering | Data Lake       |
| Analytics        | Warehouse       |
| BI Team          | Reporting Layer |

Everyone may see different numbers.

------------------------------------------------------------------------

**Databricks Lakehouse Solution**

Instead of:

Data Lake\
+\
Warehouse

Databricks uses:

Data Lakehouse

Benefits:

✅ Single copy of data\
✅ AI/ML and BI use same data\
✅ Less synchronization effort\
✅ Lower storage costs

**Exam Tip**

When you see:

- Separate Lake + Warehouse

- Traditional architecture

Think:

Duplicate data + synchronization problems

------------------------------------------------------------------------

**E. Better AI/ML Integration ❌**

**Why it's wrong**

Separate systems typically make AI/ML integration harder.

Data scientists often need data from:

- Data Lake

- Warehouse

- Reporting systems

This creates extra work.

**Traditional Architecture**

AI Team ← Data Lake\
BI Team ← Warehouse

Different teams, different data.

**Lakehouse Architecture**

Single Data Source\
↓\
AI + BI + Analytics

This improves AI/ML integration.

**Exam Tip**

"Better AI/ML integration" is one of the benefits of a Lakehouse, not a problem of traditional systems.

------------------------------------------------------------------------

**Quick Elimination Strategy**

| **Option** | **Correct?** | **Why** |
|----|----|----|
| A. Increased data quality | ❌ | Multiple copies often reduce consistency |
| B. Faster analytics performance | ❌ | Benefit, not a problem |
| C. Reduced storage costs | ❌ | Duplicate copies increase costs |
| D. Multiple copies and synchronization issues | ✅ | Core problem of separate Lake and Warehouse systems |
| E. Better AI/ML integration | ❌ | Lakehouse improves integration, not traditional architecture |

------------------------------------------------------------------------

**Memory Trick**

**Traditional Architecture**

Data Lake\
↓\
Copy Data\
↓\
Warehouse

Problems:

❌ Duplicate data\
❌ Multiple owners\
❌ Sync failures\
❌ Higher costs

**Databricks Lakehouse**

One Data Copy\
↓\
AI + BI + Analytics

Benefits:

✅ Shared data source\
✅ No synchronization headaches\
✅ Lower storage costs

That's why the correct answer is:

✅ **D. Multiple copies of the same data and synchronization issues**.

# [README](./../../../README.md)
