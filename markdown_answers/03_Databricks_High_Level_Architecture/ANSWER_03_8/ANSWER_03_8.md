# ANSWER 03 8

**Which role is responsible for creating workspaces, managing users, and assigning permissions across workspaces?**

A. Workspace Administrator\
B. Owner\
C. Data Engineer\
D. Metastore Administrator\
**E. Account Administrator**

**Correct Answer: E**

**The Core Concept: Scope of Responsibility**

The easiest way to answer Databricks role questions is to ask:

**What level does this role operate at?**

Databricks roles operate at different levels:

Databricks Account\
│\
├── Account Administrator\
│\
├── Workspace A\
│ └── Workspace Administrator\
│\
├── Workspace B\
│ └── Workspace Administrator\
│\
└── Metastore\
└── Metastore Administrator

The bigger the scope, the more authority the role has.

**Why E is Correct**

**E. Account Administrator ✅**

Your notes explicitly state:

**Account Administrator is responsible for:**

- Creating workspaces

- Managing users

- Managing metastores

- Assigning permissions across workspaces

Example:

Databricks Account\
│\
├── Dev Workspace\
├── UAT Workspace\
└── Prod Workspace

The Account Administrator can:

✓ Create Dev Workspace\
✓ Create UAT Workspace\
✓ Create Prod Workspace\
✓ Add Users\
✓ Create Groups\
✓ Create Service Principals\
✓ Assign Workspace Access\
✓ Attach Metastores

This is the highest administrative role discussed in your notes.

**Memory Trick**

Think:

Account Administrator\
=\
Everything Above Workspaces

If the question mentions:

- Multiple workspaces

- Users across workspaces

- Workspace creation

The answer is usually:

✅ Account Administrator

**Why A is Wrong**

**A. Workspace Administrator ❌**

This is the most common exam trap.

A Workspace Administrator only manages **one workspace**.

Your notes state:

Workspace Administrator is responsible for:

- Managing a specific workspace

- Managing workspace users

- Managing workspace assets and permissions

Example:

Workspace A\
│\
├── Notebooks\
├── Jobs\
├── Clusters\
└── Users

The Workspace Administrator can manage Workspace A.

They cannot:

❌ Create new workspaces\
❌ Manage all workspaces in the account\
❌ Perform account-level administration

**Easy Comparison**

**Workspace Administrator**

Controls:\
One Workspace

**Account Administrator**

Controls:\
All Workspaces

**Why B is Wrong**

**B. Owner ❌**

Owner refers to the creator of an object.

Your notes say:

Examples:

Notebook Owner\
Table Owner\
Schema Owner

Owners can:

✓ Grant permissions\
✓ Delegate access\
✓ Manage their object

But only for the object they own.

Example:

Notebook A\
│\
└── Owner

The owner cannot:

❌ Create workspaces\
❌ Manage users across workspaces\
❌ Manage metastores at the account level

**Exam Shortcut**

If the question talks about:

Table\
Notebook\
Schema

Think:

Owner

If it talks about:

Workspaces\
Users\
Accounts

Think:

Account Administrator

**Why C is Wrong**

**C. Data Engineer ❌**

This option is included to test whether you can distinguish between a **job role** and an **administrative role**.

A Data Engineer typically:

Builds pipelines\
Creates ETL jobs\
Writes Spark code\
Transforms data

Example:

df.read.table("sales")\
df.transform(...)\
df.write.save(...)

A Data Engineer is not automatically an administrator.

The role does not inherently include authority to:

❌ Create workspaces\
❌ Manage account users\
❌ Assign workspace permissions

**Think of It This Way**

A Data Engineer uses the platform.

An Account Administrator manages the platform.

**Why D is Wrong**

**D. Metastore Administrator ❌**

Your notes state:

**Metastore Administrator is responsible for:**

- Creating catalogs

- Managing data objects

- Delegating privileges

Example:

Metastore\
│\
├── Catalog A\
├── Catalog B\
└── Catalog C

The Metastore Administrator manages governance and metadata.

They can:

✓ Create catalogs\
✓ Manage schemas\
✓ Manage permissions

They cannot:

✗ Create workspaces\
✗ Manage all account users\
✗ Manage workspace assignments

**Common Exam Trap**

Students often see:

"Administrator"

and assume it's the highest role.

But Databricks has different administrative scopes.

| **Role**                | **Scope**                |
|-------------------------|--------------------------|
| Account Administrator   | Entire Account           |
| Workspace Administrator | One Workspace            |
| Metastore Administrator | Unity Catalog Governance |
| Owner                   | Specific Object          |

**The Fastest Way to Solve Role Questions**

Ask:

**Does it involve multiple workspaces?**

Example:

Create Workspaces\
Assign Workspace Access\
Manage Users Across Workspaces

Answer:

✅ Account Administrator

**Does it involve one workspace?**

Example:

Manage Clusters\
Manage Workspace Users\
Manage Workspace Assets

Answer:

✅ Workspace Administrator

**Does it involve catalogs and schemas?**

Example:

Catalog Creation\
Governance\
Privileges

Answer:

✅ Metastore Administrator

**Does it involve a single notebook/table/schema?**

Example:

Grant Access to a Table\
Manage Notebook Permissions

Answer:

✅ Owner

**Certification-Level Takeaway**

Memorize this table:

| **Role** | **Main Responsibility** |
|----|----|
| **Account Administrator** | Workspaces, users, groups, metastores, account-level permissions |
| **Workspace Administrator** | One workspace and its assets |
| **Metastore Administrator** | Catalogs, schemas, governance |
| **Owner** | Specific object (table, schema, notebook) |
| **Data Engineer** | Builds and manages data pipelines |

When you see:

**Creating workspaces, managing users, and assigning permissions across workspaces**

those are **account-level responsibilities**, making **E. Account Administrator** the only correct answer. ✅

# [README](./../../../README.md)
