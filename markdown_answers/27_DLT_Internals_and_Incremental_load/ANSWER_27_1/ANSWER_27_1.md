# ANSWER 27 1

**Question 1**

**What is one of the biggest advantages of Delta Live Tables (DLT) regarding pipeline datasets?**

**A. Developers must manually create and delete every Delta table. ❌ Incorrect**

- This describes a traditional ETL approach, not DLT.

- Without DLT, developers often have to:

  - Create tables

  - Delete obsolete tables

  - Manage table versions

- DLT automates these tasks.

------------------------------------------------------------------------

**B. DLT automatically manages the lifecycle of datasets created within a pipeline. ✅ Correct**

One of DLT's biggest advantages is **dataset lifecycle management**.

DLT automatically:

- Creates datasets.

- Updates datasets when the pipeline runs.

- Removes datasets that are no longer defined.

- Tracks dependencies between datasets.

- Maintains metadata.

Example:

Pipeline Code

↓

DLT

├── Create tables

├── Update tables

├── Delete obsolete tables

└── Maintain metadata

Developers focus on transformation logic, not table management.

------------------------------------------------------------------------

**C. DLT stores all datasets only in local notebook memory. ❌ Incorrect**

- Notebook memory is temporary.

- DLT stores data as **Delta tables**, not in notebook memory.

- Data persists after the notebook finishes.

------------------------------------------------------------------------

**D. Developers must manually register every table in Unity Catalog. ❌ Incorrect**

- DLT integrates with Unity Catalog.

- When configured, DLT automatically manages registered datasets.

- Manual registration is generally unnecessary.

------------------------------------------------------------------------

**E. DLT automatically converts all tables into streaming tables. ❌ Incorrect**

DLT supports multiple dataset types:

- Streaming Tables

- Materialized Views

- Views

Not every dataset is streaming.

------------------------------------------------------------------------

**Why B is correct**

DLT automatically manages the **entire lifecycle** of pipeline datasets, reducing operational work and simplifying pipeline maintenance.

------------------------------------------------------------------------

# [README](./../../../README.md)
