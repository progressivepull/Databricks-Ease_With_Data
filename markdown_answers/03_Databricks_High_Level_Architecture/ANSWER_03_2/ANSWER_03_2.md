# ANSWER 03 2

**What is the first entity that must be created before creating Databricks workspaces?**

A. Metastore\
B. Catalog\
C. Workspace\
**D. Databricks Account**\
E. Schema

**Correct Answer: D**

**Understanding the Databricks Hierarchy**

The key concept is that Databricks follows a hierarchy:

Databricks Account\
│\
├── Workspace A\
├── Workspace B\
├── Workspace C\
│\
└── Metastore\
└── Catalog\
└── Schema\
└── Tables

You cannot create workspaces until a **Databricks Account** exists because workspaces live inside an account.

Think of it like building a house:

- Account = Land

- Workspace = House

- Catalog = Rooms

- Schema = Closets

You must own the land before building the house.

**Why D is Correct**

**D. Databricks Account ✅**

From the architecture notes:

"You first create a Databricks Account."

The Databricks Account is the top-level administrative boundary.

The account is responsible for:

- Creating workspaces

- Managing users

- Managing groups

- Managing service principals

- Managing metastores

- Assigning metastores to workspaces

Example:

Databricks Account\
│\
├── Workspace A (Dev)\
├── Workspace B (UAT)\
└── Workspace C (Prod)

Without an account, there is nowhere to create a workspace.

**Why A is Wrong**

**A. Metastore ❌**

A metastore stores Unity Catalog metadata and governance information.

It contains:

- Catalogs

- Schemas

- Tables

- Permissions

Example:

Metastore\
│\
├── Catalog\
│ ├── Schema\
│ │ └── Tables

The metastore is created and managed at the account level.

You need an account before you can manage metastores.

Therefore:

Account → Metastore

not

Metastore → Account

**Why B is Wrong**

**B. Catalog ❌**

A catalog is part of Unity Catalog.

Hierarchy:

Metastore\
└── Catalog\
└── Schema\
└── Table

A catalog exists inside a metastore.

Since a metastore requires an account, a catalog definitely cannot be the first object created.

This would be like trying to create a folder before creating the drive that stores it.

**Why C is Wrong**

**C. Workspace ❌**

This is a common exam trap.

The question asks:

What must be created before creating workspaces?

Answering "Workspace" creates a logical contradiction.

It's similar to asking:

What must exist before creating a house?

And answering:

The house.

A workspace is something created under an account.

Therefore:

Account → Workspace

not

Workspace → Account

**Why E is Wrong**

**E. Schema ❌**

A schema is even lower in the Unity Catalog hierarchy.

Hierarchy:

Metastore\
└── Catalog\
└── Schema\
└── Table

To create a schema, you first need:

1.  Account

2.  Metastore

3.  Catalog

4.  Schema

So schema is one of the last objects in the chain, not the first.

**Visualizing the Creation Order**

For exam purposes, remember this order:

1\. Databricks Account\
↓\
2. Workspace(s)\
↓\
3. Metastore\
↓\
4. Catalog\
↓\
5. Schema\
↓\
6. Tables

Even if some objects can be configured at different stages, the **Databricks Account is always the top-level entity** and must exist before workspaces can be created.

**Certification-Level Takeaway**

When you see:

"What must be created first?"

Think:

Databricks Account\
↓\
Workspaces\
↓\
Unity Catalog Objects

The **Databricks Account** is the foundation of the entire environment because it manages:

- Workspaces

- Metastores

- Users

- Groups

- Service Principals

- Permissions

That's why **D. Databricks Account** is the only correct answer. ✅

# [README](./../../../README.md)
