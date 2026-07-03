# ANSWER 10 10

**Question 10**

**Which new capability becomes available after Unity Catalog is successfully enabled and the workspace is refreshed?**

**A. Automatic cluster scaling** ❌ Incorrect

- Autoscaling is a cluster feature, not a Unity Catalog feature.

**B. Azure DevOps integration** ❌ Incorrect

- Azure DevOps integration is independent of Unity Catalog.

**C. Catalog creation and centralized workspace permissions** ✅ Correct

Once Unity Catalog is enabled, you can:

- Create catalogs

- Apply centralized permissions

- Share data across workspaces

- Use fine-grained access control

- Govern data consistently

This is the primary capability unlocked by Unity Catalog.

**D. Automatic Delta Live Tables deployment** ❌ Incorrect

- Delta Live Tables are configured separately.

**E. Built-in Auto Loader pipelines** ❌ Incorrect

- Auto Loader is an ingestion feature, not part of Unity Catalog enablement.

**Key Concept**

After enabling Unity Catalog:

Centralized Governance\
+\
Catalog Creation\
+\
Cross-Workspace Security

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| First Unity Catalog component | **Metastore** |
| Best practice | **One metastore per cloud region** |
| Azure Storage Account | Stores managed Unity Catalog table data |
| Required ADLS Gen2 feature | **Hierarchical Namespace (HNS)** |
| Access Connector | Uses a **Managed Identity** to authenticate Databricks to Azure Storage |
| Required RBAC role | **Storage Blob Data Contributor** |
| Metastore configuration requires | **ADLS Gen2 storage path + Access Connector Resource ID** |
| Final setup step | Assign the metastore to one or more workspaces |
| First Metastore Administrator | The user who creates the metastore |
| Main capability after enablement | Centralized governance, catalog creation, and consistent permissions across workspaces |

# [README](./../../../README.md)
