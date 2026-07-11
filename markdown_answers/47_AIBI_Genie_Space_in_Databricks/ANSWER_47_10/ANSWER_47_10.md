# ANSWER 47 10

**Question 10**

**Which permissions are required for business users to successfully use a shared Genie Space?**

**A. Only Can Run permission on the Genie Space** ❌ Incorrect

- Access to the Genie Space alone isn't enough.

- Users also need permission to access the underlying data and compute.

**B. Only Workspace Administrator privileges** ❌ Incorrect

- Business users do not need to be administrators.

**C. Genie Space access, dataset permissions (USE CATALOG, USE SCHEMA, SELECT), and Can Use permission on the SQL Warehouse** ✅ Correct

Users need **three categories of permissions**:

**1. Genie Space**

Can access the shared Genie Space.

**2. Data Permissions**

Must be able to read data.

Example:

USE CATALOG

USE SCHEMA

SELECT

**3. SQL Warehouse**

Need **Can Use** permission so the generated SQL can execute.

Without **any one** of these, Genie cannot return results.

**D. Cluster creation permission and notebook editing access** ❌ Incorrect

- Genie users don't need development permissions.

**E. Metastore Administrator privileges only** ❌ Incorrect

- Metastore Admin is an administrative role and is unnecessary for typical Genie users.

**Key Concept**

Think of Genie access as requiring **three doors** to be unlocked:

Door 1

Genie Space Access

│

Door 2

Data Permissions

(USE CATALOG

USE SCHEMA

SELECT)

│

Door 3

SQL Warehouse

(Can Use)

│

User Gets Results

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **AI/BI Genie** | Lets business users ask questions in natural language instead of writing SQL. |
| **Workflow** | English question → AI interprets → SQL generated → SQL Warehouse executes → Results and visualizations returned. |
| **Supported Compute** | SQL Warehouse **Pro** and **Serverless**. |
| **AI Understanding** | Genie relies heavily on high-quality metadata such as table descriptions, column comments, dataset names, and relationships. |
| **Example Values** | Help Genie understand real business values and abbreviations found in your data. |
| **Custom Instructions** | Teach Genie organization-specific terminology, acronyms, and business rules. |
| **Show Code** | Displays the generated SQL so users can inspect filters, joins, aggregations, and other query logic. |
| **Visualizations** | Genie can automatically produce charts (bar, pie, trend, etc.) in addition to tabular query results. |
| **Monitoring** | Administrators can review user questions, generated SQL, users, and query history to improve Genie Spaces. |
| **Required Permissions** | Users need **Genie Space access**, **Unity Catalog permissions** (USE CATALOG, USE SCHEMA, SELECT), and **Can Use** permission on the associated SQL Warehouse. |

# [README](./../../../README.md)
