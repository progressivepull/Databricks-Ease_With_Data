# EXPLANATION 16 3

**Question 3**

**Which command is commonly used to physically remove rows that were marked by Deletion Vectors?**

**Correct Answer:**\
✅ **OPTIMIZE table_name;**

**Explanation**

Deletion Vectors only mark rows as deleted.

Eventually the files need to be rewritten.

That happens during:

OPTIMIZE employees;

Process:

Old File\
\
↓\
\
OPTIMIZE\
\
↓\
\
New File\
\
↓\
\
Deleted Rows Gone

OPTIMIZE rewrites files, compacts them, and can eliminate rows previously marked by Deletion Vectors. Depending on the table state and runtime, Databricks may also use other maintenance operations such as REORG TABLE ... APPLY (PURGE) for complete physical cleanup.

**YouTube**

**Databricks OPTIMIZE**

https://www.youtube.com/results?search_query=Databricks+OPTIMIZE

# [README](./../../../README.md)
