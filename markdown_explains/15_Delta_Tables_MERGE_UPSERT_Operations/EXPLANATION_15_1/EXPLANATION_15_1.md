# EXPLANATION 15 1

**Question 1**

**What is the primary purpose of the Delta Lake MERGE command?**

**Correct Answer:**\
✅ **To combine INSERT, UPDATE, and optional DELETE operations into a single atomic transaction**

**Explanation**

The **MERGE** command synchronizes data between a **source** table and a **target** Delta table.

Instead of running separate commands:

UPDATE ...\
\
INSERT ...\
\
DELETE ...

you can perform all three operations in one statement.

**Example**

MERGE INTO employees AS target\
USING updates AS source\
ON target.emp_id = source.emp_id\
\
WHEN MATCHED THEN\
UPDATE SET \*\
\
WHEN NOT MATCHED THEN\
INSERT \*\
\
WHEN NOT MATCHED BY SOURCE THEN\
DELETE;

MERGE is **atomic**, meaning either:

- All changes succeed, or

- None of the changes are committed.

This guarantees data consistency and is one of Delta Lake's major advantages.

**MERGE Flow**

Source\
\
↓\
\
Compare Keys\
\
↓\
\
Match?\
\
Yes → UPDATE\
\
No → INSERT\
\
Missing in Source?\
\
↓\
\
DELETE (optional)

**YouTube**

**Delta Lake MERGE (Official Databricks)**

https://www.youtube.com/results?search_query=Databricks+MERGE+Delta+Lake

# [README](./../../../README.md)
