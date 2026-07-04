# EXPLANATION 08 1

**Question 1**

**What is the primary purpose of Unity Catalog in Databricks?**

**Correct Answer:**\
✅ **To provide centralized governance, security, and metadata management across Databricks workspaces**

**Explanation**

**Unity Catalog** is Databricks' centralized governance solution.

Before Unity Catalog, organizations often managed permissions separately in each workspace, making administration difficult and inconsistent.

Unity Catalog provides one place to manage:

- Data permissions

- User access

- Groups

- Catalogs

- Schemas

- Tables

- Views

- Volumes

- Functions

- Data lineage

- Auditing

One Unity Catalog can govern **multiple Databricks workspaces**.

**Architecture**

Databricks Account\
│\
▼\
Unity Catalog\
│\
┌────────┼────────┐\
▼ ▼ ▼\
Workspace A Workspace B Workspace C

Instead of configuring permissions three separate times, administrators configure them once in Unity Catalog.

Databricks documentation describes Unity Catalog as the unified governance solution for data and AI assets across workspaces.

**YouTube**

**Official Databricks – Unity Catalog**

https://www.youtube.com/results?search_query=Databricks+Unity+Catalog

**Unity Catalog Tutorial**

https://www.youtube.com/results?search_query=Unity+Catalog+Databricks+Tutorial

# [README](./../../../README.md)
