# ANSWER 13 1

**Question 1**

**Before creating an external table in Unity Catalog, what must first be created in Azure Data Lake Storage (ADLS)?**

**A. A SQL Warehouse** ❌ Incorrect

- A SQL Warehouse is a compute resource used to execute SQL queries.

- It does **not** provide a storage location for an external table.

**B. A dedicated storage folder for external table data** ✅ Correct

An external table stores its data in a location that **you manage**.

Example:

ADLS Gen2\
└── external-tables/\
└── sales/

When creating the table, Unity Catalog references this folder.

Example:

CREATE TABLE sales\
LOCATION 'abfss://external-tables@storageaccount.dfs.core.windows.net/sales/'

Unlike managed tables, Unity Catalog **does not create this storage location for you**.

**C. A Delta Live Table pipeline** ❌ Incorrect

- Delta Live Tables automate data pipelines.

- They are unrelated to creating external storage locations.

**D. A Unity Catalog metastore** ❌ Incorrect

- A metastore is required to use Unity Catalog overall, but the question asks specifically what must first exist **in ADLS**.

- The required ADLS resource is the storage folder.

**E. A Databricks notebook** ❌ Incorrect

- Notebooks are one way to execute SQL, but they are not a storage requirement.

**Key Concept**

External Table:

You create storage folder\
↓\
Unity Catalog references it

------------------------------------------------------------------------

# [README](./../../../README.md)
