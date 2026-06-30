# ANSWER 03 3

**Which statement about Databricks workspaces is correct?**

A. A workspace can contain multiple accounts.\
B. A metastore can contain multiple accounts.\
**C. An account can contain multiple workspaces.**\
D. A workspace can contain multiple metastores only.\
E. Users must create a new account for every workspace.

**Correct Answer: C**

**First Understand the Architecture**

The architecture described in your notes looks like this:

Databricks Account\
│\
├── Workspace A (Dev)\
├── Workspace B (UAT)\
├── Workspace C (Prod)\
│\
├── Users\
├── Groups\
├── Service Principals\
└── Metastore

The most important relationship is:

One Account\
↓\
Many Workspaces

Think of the Databricks Account as the parent and Workspaces as children.

------------------------------------------------------------------------

**Why C is Correct**

**C. An account can contain multiple workspaces. ✅**

This is exactly how Databricks is designed.

Example:

Databricks Account\
│\
├── Dev Workspace\
├── Test Workspace\
├── UAT Workspace\
└── Production Workspace

Organizations commonly separate environments using multiple workspaces.

For example:

| **Workspace** | **Purpose**             |
|---------------|-------------------------|
| Dev           | Development             |
| UAT           | User Acceptance Testing |
| Prod          | Production              |

The Account Administrator manages all these workspaces from a single Databricks Account.

This is directly stated in the notes:

"An account can contain multiple workspaces."

------------------------------------------------------------------------

**Why A is Wrong**

**A. A workspace can contain multiple accounts. ❌**

This reverses the hierarchy.

Actual hierarchy:

Account\
↓\
Workspace

Option A incorrectly says:

Workspace\
↓\
Accounts

A workspace is a child object that exists inside an account.

Think of it like:

Company Account\
├── Office A\
├── Office B

An office does not contain companies.

Similarly:

Workspace ≠ Parent of Account

------------------------------------------------------------------------

**Why B is Wrong**

**B. A metastore can contain multiple accounts. ❌**

A metastore stores governance and metadata information.

It contains:

Metastore\
│\
├── Catalogs\
├── Schemas\
└── Tables

It does **not** contain Databricks Accounts.

The relationship is actually:

Account\
↓\
Creates/Manages\
Metastore

A metastore is a governance object.

An account is an administrative object.

They are completely different levels of the architecture.

------------------------------------------------------------------------

**Why D is Wrong**

**D. A workspace can contain multiple metastores only. ❌**

Several problems exist here.

**Problem 1**

The word **"only"** is a major red flag on exams.

Workspaces contain many things:

- Notebooks

- Jobs

- Clusters

- Dashboards

- Libraries

- Users

Not just metastores.

------------------------------------------------------------------------

**Problem 2**

Your notes specifically state:

The same metastore can be attached to multiple workspaces.

Example:

Metastore\
│\
┌───┼─────┐\
▼ ▼ ▼\
Dev UAT Prod

This means:

- One metastore

- Multiple workspaces

Not:

- One workspace

- Multiple metastores

Therefore the relationship is backwards.

------------------------------------------------------------------------

**Why E is Wrong**

**E. Users must create a new account for every workspace. ❌**

This directly contradicts the architecture.

Your notes show:

Databricks Account\
│\
├── Workspace A\
├── Workspace B\
└── Workspace C

One account can support many workspaces.

Creating separate accounts for every workspace would defeat the purpose of centralized administration.

The Account Administrator is specifically responsible for:

- Managing multiple workspaces

- Managing users

- Managing groups

- Managing metastores

All from one account.

------------------------------------------------------------------------

**Common Exam Trap**

Databricks exams often test whether you understand the hierarchy.

Many wrong answers reverse parent-child relationships.

Remember:

Account\
↓\
Workspace

NOT

Workspace\
↓\
Account

and

Metastore\
↓\
Catalog\
↓\
Schema\
↓\
Table

NOT

Table\
↓\
Schema\
↓\
Metastore

When an option reverses the hierarchy, it's usually wrong.

------------------------------------------------------------------------

**Certification-Level Takeaway**

Memorize this structure:

Databricks Account\
│\
├── Workspace A\
├── Workspace B\
├── Workspace C\
│\
└── Metastore\
└── Catalog\
└── Schema\
└── Table

Key rule:

**One Databricks Account can manage multiple Workspaces.**

That's why **C. An account can contain multiple workspaces** is the correct answer. ✅

# [README](./../../../README.md)
