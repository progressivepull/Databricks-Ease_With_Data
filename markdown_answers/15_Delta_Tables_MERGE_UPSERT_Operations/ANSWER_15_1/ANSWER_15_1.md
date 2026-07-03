# ANSWER 15 1

**Question 1**

**What is the primary purpose of the Delta Lake MERGE command?**

**A. To permanently delete all records from a table** ❌ Incorrect

- MERGE **can** delete records, but deleting everything is **not** its purpose.

- To delete all rows, you would typically use:

DELETE FROM table_name;

or

TRUNCATE TABLE table_name;

- MERGE is designed to compare two datasets and apply changes intelligently.

**B. To optimize Delta table storage** ❌ Incorrect

- Storage optimization is performed using:

OPTIMIZE table_name;

- MERGE modifies data, not storage layout.

**C. To combine INSERT, UPDATE, and optional DELETE operations into a single atomic transaction** ✅ Correct

MERGE is one of Delta Lake's most powerful commands.

It can perform all three operations at once:

Source Record\
↓\
Exists in Target?\
│\
Yes │ No\
│\
UPDATE │ INSERT\
│\
Missing from Source?\
│\
DELETE (optional)

This entire operation is **atomic**, meaning either:

- everything succeeds, or

- nothing changes.

This guarantees data consistency.

**D. To create Delta table backups** ❌ Incorrect

- MERGE is not a backup tool.

- Delta Lake provides Time Travel and cloning features for recovery.

**E. To convert CSV files into Delta format** ❌ Incorrect

- Converting CSV files involves reading the CSV and writing it as Delta.

- MERGE assumes the data is already available.

**Memory Trick**

MERGE =

UPDATE\
+\
INSERT\
+\
(optional DELETE)\
\
All in one transaction

------------------------------------------------------------------------

# [README](./../../../README.md)
