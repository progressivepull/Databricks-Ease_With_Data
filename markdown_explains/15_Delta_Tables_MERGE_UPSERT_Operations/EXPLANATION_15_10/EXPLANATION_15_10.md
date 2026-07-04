# EXPLANATION 15 10

**Question 10**

**What capability allows Delta Lake to add a new column such as IS_ACTIVE without rewriting existing data?**

**Correct Answer:**\
✅ **Schema Evolution**

**Explanation**

Schema Evolution allows Delta Lake tables to grow over time.

Original schema:

EMP_ID\
\
NAME\
\
SALARY

New schema:

EMP_ID\
\
NAME\
\
SALARY\
\
IS_ACTIVE

Instead of rewriting every existing file, Delta Lake updates the table metadata and incorporates the new column. Existing rows use NULL (or another appropriate default) until updated, while new rows include the new column.

Benefits:

- Faster schema changes

- Lower storage costs

- No full table rewrite

- Easier evolution of production tables

Schema Evolution is one of Delta Lake's core features for handling changing data structures.

**YouTube**

**Delta Lake Schema Evolution**

https://www.youtube.com/results?search_query=Delta+Lake+Schema+Evolution

**Recommended YouTube Playlists**

These playlists cover all of the MERGE, UPSERT, and Schema Evolution topics:

1.  **Official Databricks – Delta Lake**

    - https://www.youtube.com/results?search_query=Databricks+Delta+Lake

2.  **Delta Lake MERGE Tutorial**

    - https://www.youtube.com/results?search_query=Delta+Lake+MERGE+Tutorial

3.  **Schema Evolution in Delta Lake**

    - https://www.youtube.com/results?search_query=Delta+Lake+Schema+Evolution

4.  **Slowly Changing Dimensions (SCD Type 1 & Type 2)**

    - https://www.youtube.com/results?search_query=Databricks+SCD+Type+1+Type+2

5.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

# [README](./../../../README.md)
