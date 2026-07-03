# ANSWER 09 7

**Question 7**

**What happens when a managed table is dropped?**

**A. Only the metadata is removed.** ❌ Incorrect

- Physical files are also removed.

**B. Only the physical data is removed.** ❌ Incorrect

- Metadata is also deleted.

**C. Both the metadata and physical data files are deleted.** ✅ Correct

Dropping a managed table removes:

- Metadata

- Data files

Everything disappears.

Example:

DROP TABLE sales;

Result:

Table deleted\
Data deleted

**D. The table becomes an external table.** ❌ Incorrect

- Dropping a table never converts its type.

**E. The table is converted into a view.** ❌ Incorrect

- Tables and views are unrelated object types.

**Memory Trick**

Managed Table:

DROP TABLE\
│\
▼\
Everything deleted

------------------------------------------------------------------------

# [README](./../../../README.md)
