# EXPLANATION 14 9

**Question 9**

**Which statement correctly describes a Shallow Clone?**

**Correct Answer:**\
✅ **It copies metadata while initially referencing the original table's data files.**

**Explanation**

Shallow Clone creates a lightweight copy.

Instead of copying all data files:

Original Table\
\
↓\
\
Data Files\
\
↑\
\
Shallow Clone

The clone references the original files.

Benefits:

- Very fast

- Minimal storage

- Lower cost

Limitation:

If the original files are removed, the clone can be affected.

Databricks documents that shallow clones copy metadata only and reference the source data files.

**YouTube**

**Shallow Clone Explained**

https://www.youtube.com/results?search_query=Databricks+Shallow+Clone

# [README](./../../../README.md)
