# ANSWER 17 8

**Question 8**

**What additional component is required when creating an External Volume?**

**A. A Spark Session** ❌ Incorrect

- Spark executes code.

- It isn't part of the volume definition.

**B. A Delta Table** ❌ Incorrect

- Volumes are independent of tables.

**C. A LOCATION pointing to external cloud storage** ✅ Correct

Example:

CREATE EXTERNAL VOLUME images\
LOCATION\
'abfss://media@storage.dfs.core.windows.net/images/';

The LOCATION tells Unity Catalog where the files already live.

**D. A SQL Warehouse** ❌ Incorrect

- SQL Warehouses execute SQL.

**E. A Photon-enabled cluster** ❌ Incorrect

- Photon is unrelated.

------------------------------------------------------------------------

**Key Concept**

External Volume

↓

Needs

LOCATION

------------------------------------------------------------------------

# [README](./../../../README.md)
