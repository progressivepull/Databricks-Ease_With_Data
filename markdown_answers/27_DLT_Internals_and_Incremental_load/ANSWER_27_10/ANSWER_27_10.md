# ANSWER 27 10

**Question 10**

**Which statement about Unity Catalog Lineage is correct?**

**A. It is available only for Delta Live Tables pipelines. ❌ Incorrect**

- Unity Catalog Lineage works across many Unity Catalog-managed assets, not just DLT.

------------------------------------------------------------------------

**B. It tracks only table names and ignores columns. ❌ Incorrect**

- Unity Catalog provides **column-level lineage** in addition to table-level lineage.

------------------------------------------------------------------------

**C. It provides end-to-end table and column-level lineage for DLT pipelines and other Unity Catalog-managed assets. ✅ Correct**

Unity Catalog Lineage can show:

Raw Orders

↓

Bronze Orders

↓

Silver Orders

↓

Gold Sales Report

It also tracks individual columns, showing how a column is transformed as it moves through the pipeline. This helps with:

- impact analysis

- troubleshooting

- compliance

- auditing

- understanding data flow

------------------------------------------------------------------------

**D. It works only for Streaming Tables. ❌ Incorrect**

- Lineage works with Streaming Tables, Materialized Views, standard Delta tables, views, and other Unity Catalog-managed objects.

------------------------------------------------------------------------

**E. It requires developers to manually document every transformation. ❌ Incorrect**

- One of Unity Catalog Lineage's major benefits is that it **automatically captures lineage** from supported workloads.

- Developers do not need to manually maintain documentation for every transformation.

------------------------------------------------------------------------

**Why C is correct**

Unity Catalog Lineage provides **end-to-end visibility** into how data flows through your platform. It automatically tracks both **table-level** and **column-level** lineage across DLT pipelines and other Unity Catalog-managed assets, making it easier to understand dependencies, assess the impact of changes, and satisfy governance and auditing requirements.

# [README](./../../../README.md)
