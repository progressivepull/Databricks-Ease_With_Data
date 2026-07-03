# ANSWER 10 8

**Question 8**

**What additional step is required after creating a Metastore to enable Unity Catalog?**

**A. Restart all compute clusters** ❌ Incorrect

- Restarting clusters is not required.

**B. Create a Delta table** ❌ Incorrect

- Tables are created after Unity Catalog is enabled.

**C. Assign the Metastore to a Databricks workspace** ✅ Correct

Creating a metastore alone is not enough.

You must attach it to one or more workspaces.

Flow:

Create Metastore\
↓\
Assign Workspace\
↓\
Unity Catalog Enabled

**D. Configure Auto Loader** ❌ Incorrect

- Auto Loader is unrelated.

**E. Create an MLflow experiment** ❌ Incorrect

- MLflow is unrelated to Unity Catalog setup.

**Memory Trick**

Metastore alone does nothing until:

Workspace\
↓\
Attached

# [README](./../../../README.md)
