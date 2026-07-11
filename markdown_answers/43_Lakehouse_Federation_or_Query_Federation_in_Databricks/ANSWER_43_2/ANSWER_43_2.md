# ANSWER 43 2

**Question 2**

**Which of the following is a key benefit of using Lakehouse Federation?**

**A. It requires all external data to be converted to Delta format first.** ❌ Incorrect

- One major advantage is that **no conversion is required**.

- Databricks can query supported external databases directly.

**B. It eliminates the need for Unity Catalog.** ❌ Incorrect

- Unity Catalog is actually required.

- It manages:

  - Connections

  - Foreign Catalogs

  - Permissions

**C. It reduces storage duplication by querying data where it already resides.** ✅ Correct

- Since data is not copied:

  - Less storage is consumed.

  - ETL pipelines can often be reduced.

  - Data remains synchronized because it is queried live.

**D. It only supports Azure Data Lake Storage.** ❌ Incorrect

- Federation supports multiple external databases, not just Azure storage.

**E. It automatically creates ETL pipelines for every external database.** ❌ Incorrect

- Federation aims to **avoid** ETL whenever possible.

**Key Concept**

**Benefit = No duplicate copies of data.**

# [README](./../../../README.md)
