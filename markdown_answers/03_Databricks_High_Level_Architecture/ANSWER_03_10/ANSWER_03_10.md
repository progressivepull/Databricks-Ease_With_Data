# ANSWER 03 10

**What is a Service Principal in Databricks?**

A. A special type of workspace administrator\
B. A backup metastore for disaster recovery\
**C. A non-human identity used by applications, automation, CI/CD pipelines, and jobs**\
D. A cluster used for automated processing\
E. A user group for developers

**Correct Answer: C**

**Core Concept**

A **Service Principal** is a **non-human identity**.

Instead of a person logging in, an application or automation process uses the Service Principal to authenticate and access Databricks resources securely.

Think:

**Human Identity**

John Smith\
↓\
Username + MFA\
↓\
Databricks

Non-Human Identity

CI/CD Pipeline\
↓\
Service Principal\
↓\
Databricks

This allows automation without using a real person's credentials.

**Option A: A special type of workspace administrator ❌ Wrong**

A Workspace Administrator is a human role that manages a workspace.

Responsibilities:

- Manage workspace users

- Manage workspace permissions

- Manage workspace assets

Example:

Workspace Admin\
↓\
Adds users\
Manages notebooks\
Controls permissions

**Why Wrong?**

A Service Principal is:

- Not a human user

- Not an administrator role

- Not responsible for managing workspaces

The question asks:

What is a Service Principal?

A Service Principal is an **identity**, not an **administrator**.

**Option B: A backup metastore for disaster recovery ❌ Wrong**

A Metastore is part of Unity Catalog.

Responsibilities:

- Store metadata

- Manage catalogs

- Manage schemas

- Govern tables

Example:

Metastore\
│\
├── Catalog\
├── Schema\
└── Table

**Why Wrong?**

A Service Principal has nothing to do with:

- Metadata storage

- Catalogs

- Disaster recovery

- Metastores

This option mixes two completely different concepts.

**Option C: A non-human identity used by applications, automation, CI/CD pipelines, and jobs ✅ Correct**

This is the official definition.

A Service Principal is created so automated systems can securely access Databricks.

Common use cases:

**CI/CD Pipelines**

GitHub Actions\
↓\
Service Principal\
↓\
Deploy notebooks

**Scheduled Jobs**

Nightly ETL Job\
↓\
Service Principal\
↓\
Run Databricks workflow

**Applications**

Web Application\
↓\
Service Principal\
↓\
Access Databricks APIs

**Why Correct?**

Service Principals are:

✔ Non-human identities\
✔ Used for automation\
✔ Used by applications\
✔ Used by CI/CD pipelines\
✔ Used by scheduled jobs

Everything in Option C matches the definition exactly.

**Option D: A cluster used for automated processing ❌ Wrong**

A cluster is a compute resource.

Example:

Spark Cluster\
│\
├── Driver\
├── Executor 1\
├── Executor 2\
└── Executor 3

Clusters perform:

- ETL processing

- Machine learning

- SQL workloads

**Why Wrong?**

A Service Principal:

- Does not process data

- Is not compute

- Is not infrastructure

Instead:

Service Principal\
↓\
Authenticates\
↓\
Uses Cluster

The Service Principal accesses the cluster but is not the cluster itself.

**Option E: A user group for developers ❌ Wrong**

A group is a collection of users.

Example:

Data Engineers\
│\
├── John\
├── Sarah\
└── Mike

Groups help manage permissions.

Example:

Group: Data Engineers\
↓\
Granted access to Workspace A

**Why Wrong?**

A Service Principal is:

- One identity

- Used by automation

A group is:

- Multiple users

- Used for permission management

These are completely different concepts.

**Real-World Example**

Imagine your company runs a nightly ETL job.

**Bad Practice**

Nightly Job\
↓\
Uses John's username/password

Problems:

- John leaves the company

- Password changes

- Security risk

**Best Practice**

Nightly Job\
↓\
Service Principal\
↓\
Databricks

Benefits:

- No human dependency

- Easier auditing

- More secure

- Recommended by Databricks

This is why Service Principals exist.

**Exam Trap**

Many certification questions try to confuse:

| **Concept**       | **Purpose**         |
|-------------------|---------------------|
| User              | Human identity      |
| Group             | Collection of users |
| Service Principal | Non-human identity  |
| Workspace Admin   | Administrative role |
| Cluster           | Compute resource    |

If you see:

- Application

- Automation

- Script

- Workflow

- CI/CD

- API access

The answer is usually:

✅ **Service Principal**

**Memory Trick**

Think:

**"Users are for people. Service Principals are for software."**

People → User Accounts\
Software → Service Principals

That's why **Option C** is correct.

# [README](./../../../README.md)
