# ANSWER 42 7

**Question 7**

**Which SQL command performs a full reload of all source data for a Streaming Table?**

**A. REFRESH MATERIALIZED VIEW** ❌ Incorrect

- Refreshes Materialized Views only.

**B. REFRESH STREAMING TABLE** ❌ Incorrect

- Performs the standard incremental refresh.

- Only new data is processed.

**C. REFRESH STREAMING TABLE FULL** ✅ Correct

- Reprocesses **all source data**.

- Useful when:

  - Logic changes

  - Source corrections occur

  - A complete rebuild is needed

**D. REBUILD STREAMING TABLE** ❌ Incorrect

- Not a valid SQL command.

**E. ALTER STREAMING TABLE REFRESH** ❌ Incorrect

- Not valid syntax.

**Key Concept**

| **Command**                  | **Action**                          |
|------------------------------|-------------------------------------|
| REFRESH STREAMING TABLE      | Incremental refresh (new data only) |
| REFRESH STREAMING TABLE FULL | Full reload of all source data      |

# [README](./../../../README.md)
