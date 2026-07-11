# ANSWER 43 7

**Question 7**

**How are tables inside a Foreign Catalog identified?**

**A. Type = Delta** ❌ Incorrect

- Delta tables are Databricks-native tables.

**B. Type = Managed** ❌ Incorrect

- Managed tables are owned by Databricks.

**C. Type = External Volume** ❌ Incorrect

- Volumes contain files, not database tables.

**D. Type = Foreign** ✅ Correct

- Foreign tables indicate:

  - The table exists externally.

  - Databricks accesses it through Federation.

  - Data remains outside the Lakehouse.

**E. Type = Streaming** ❌ Incorrect

- Streaming Tables are another object entirely.

**Key Concept**

**Foreign Catalog → Foreign Tables**

# [README](./../../../README.md)
