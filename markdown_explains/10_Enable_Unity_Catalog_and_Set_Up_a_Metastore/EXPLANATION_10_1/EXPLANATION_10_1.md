# EXPLANATION 10 1

**Question 1**

**What is the first component that must be created before Unity Catalog can be enabled?**

**Correct Answer:**\
✅ **Metastore**

**Explanation**

The **Metastore** is the foundation of Unity Catalog.

Before you can create:

- Catalogs

- Schemas

- Tables

- Views

- Volumes

- Functions

you must first create a **Metastore**.

Think of the Metastore as the **master container** for Unity Catalog metadata.

**Unity Catalog Hierarchy**

Metastore\
│\
▼\
Catalog\
│\
▼\
Schema\
│\
├── Tables\
├── Views\
├── Functions\
└── Volumes

The Metastore stores:

- Metadata

- Permissions

- Ownership

- Governance

- Catalog definitions

- Data lineage

Without a Metastore, Unity Catalog cannot function. Databricks documents the Metastore as the top-level governance object for Unity Catalog.

**YouTube**

**Unity Catalog Setup (Official Databricks)**

https://www.youtube.com/results?search_query=Databricks+Unity+Catalog+Setup

# [README](./../../../README.md)
