# EXPLANATION 13 6

**Question 6**

**Which SQL command lists recently dropped tables that are still eligible for recovery?**

**Correct Answer:**\
✅ **SHOW TABLES DROPPED IN schema_name**

**Explanation**

Example:

SHOW TABLES DROPPED IN sales;

This displays dropped tables that are still within the recovery window.

Typical information includes:

- Table name

- Drop timestamp

- Recovery eligibility

This helps administrators identify tables that can still be restored.

**YouTube**

**Unity Catalog SQL Administration**

https://www.youtube.com/results?search_query=Unity+Catalog+SQL+Administration

# [README](./../../../README.md)
