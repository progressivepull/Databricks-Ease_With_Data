# EXPLANATION 09 1

**Question 1**

**Before Unity Catalog was introduced, what was the default catalog used by Databricks?**

**Correct Answer:**\
✅ **Hive Metastore**

**Explanation**

Before Unity Catalog, Databricks used the **Hive Metastore** as its default metadata repository.

The Hive Metastore stored information about:

- Databases (schemas)

- Tables

- Views

- Columns

- Data types

- Table locations

It **did not store the actual data**. Instead, it stored metadata that described where the data was located.

**Traditional Architecture**

Databricks Workspace\
│\
▼\
Hive Metastore\
│\
▼\
Metadata\
\
(Table Names)\
\
(Column Names)\
\
(Storage Location)\
\
│\
▼\
Cloud Storage\
\
(ADLS)\
\
(S3)\
\
(GCS)

One important limitation was that each workspace typically had its own Hive Metastore, making governance across multiple workspaces difficult.

Unity Catalog was introduced to solve these governance challenges by providing centralized management across workspaces.

**YouTube**

**Hive Metastore vs Unity Catalog**

https://www.youtube.com/results?search_query=Hive+Metastore+vs+Unity+Catalog

**Unity Catalog Overview**

https://www.youtube.com/results?search_query=Unity+Catalog+Databricks

# [README](./../../../README.md)
