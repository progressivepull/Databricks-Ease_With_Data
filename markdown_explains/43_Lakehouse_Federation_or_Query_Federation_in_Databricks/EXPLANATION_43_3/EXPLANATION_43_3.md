# EXPLANATION 43 3

**Question 3**

**What Unity Catalog object represents external data accessed through a live connection?**

**Correct Answer:**\
**C. Foreign Catalog**

**Why C is Correct**

A **Foreign Catalog** is a Unity Catalog object that represents an external database.

Example:

PostgreSQL Database

↓

Connection

↓

Foreign Catalog

↓

Schemas

↓

Foreign Tables

It makes external tables appear inside Unity Catalog while the data remains in the external system.

**Why the other choices are wrong**

- Catalog = native Unity Catalog storage

- Schema = organizational container

- Delta table = stored in Delta Lake

**Memory Tip**

**Foreign Catalog = External Database**

**Individual YouTube Video**

https://www.youtube.com/watch?v=mdw5j0l7K2Y

**YouTube Search**

https://www.youtube.com/results?search_query=Foreign+Catalog+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
