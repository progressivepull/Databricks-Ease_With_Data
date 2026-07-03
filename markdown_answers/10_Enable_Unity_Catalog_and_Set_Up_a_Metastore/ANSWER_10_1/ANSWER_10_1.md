# ANSWER 10 1

**Question 1**

**What is the first component that must be created before Unity Catalog can be enabled?**

**A. Catalog** ❌ Incorrect

- A catalog stores data assets such as schemas and tables.

- However, a catalog **cannot exist without a metastore**.

- The metastore is the parent object that manages all catalogs.

**B. Schema** ❌ Incorrect

- Schemas organize tables, views, functions, and volumes.

- A schema must exist **inside a catalog**, so it cannot be created first.

**C. Volume** ❌ Incorrect

- Volumes store files such as images, PDFs, CSVs, machine learning models, and other unstructured data.

- Volumes exist inside a schema, so they are created much later.

**D. Metastore** ✅ Correct

The metastore is the **foundation of Unity Catalog**.

It stores:

- Catalog metadata

- Permissions

- Ownership

- Governance policies

- Data lineage

Hierarchy:

Metastore\
└── Catalog\
└── Schema\
├── Tables\
├── Views\
├── Functions\
└── Volumes

Without a metastore, Unity Catalog cannot function.

**E. Storage Credential** ❌ Incorrect

- Storage Credentials are used later to securely connect Unity Catalog to cloud storage.

- They do not replace the need for a metastore.

**Key Concept**

Always remember:

First Step\
↓\
Create Metastore

# [README](./../../../README.md)
