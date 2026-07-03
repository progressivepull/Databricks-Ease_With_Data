# ANSWER 08 10

**Question 10**

**Why is centralized governance with Unity Catalog beneficial for organizations?**

**A. It eliminates the need for cloud storage.** ❌ Incorrect

- Cloud storage is still required.

- Unity Catalog governs access to it.

**B. It automatically creates Spark clusters.** ❌ Incorrect

- Cluster creation is separate from governance.

**C. It provides consistent security, simplified administration, auditing, and governance across multiple workspaces.** ✅ Correct

Benefits include:

- One permission model

- Easier administration

- Consistent access control

- Central auditing

- Data lineage

- Better compliance

- Shared governance across multiple workspaces

This is the primary reason organizations adopt Unity Catalog.

**D. It replaces Databricks Runtime with Photon.** ❌ Incorrect

- Photon is a query execution engine.

- Unity Catalog is a governance service.

**E. It stores all customer data in the Control Plane.** ❌ Incorrect

- Customer data remains in the customer's cloud storage (Data Plane).

- Only metadata and governance information are stored in the Control Plane.

------------------------------------------------------------------------

**Overall Concepts to Remember**

| **Concept** | **Remember This** |
|----|----|
| **Unity Catalog** | Centralized governance, security, metadata, lineage, and auditing |
| **Core Principle** | Define security once, enforce it everywhere |
| **Hierarchy** | Metastore → Catalog → Schema → Table/View/Volume |
| **Metadata Location** | Databricks Control Plane |
| **Customer Data Location** | Customer Data Plane (cloud storage) |
| **Highest Data Securable** | Catalog |
| **Schema Contains** | Tables, Views, Functions, Volumes |
| **Volumes Store** | Structured, semi-structured, and unstructured files |
| **Non-Data Securables** | Storage Credentials, External Locations, Connections |
| **Table Naming** | catalog.schema.table |
| **Main Organizational Benefit** | Centralized security, governance, auditing, and simplified administration across multiple workspaces |

# [README](./../../../README.md)
