# EXPLANATION 08 4

**Question 4**

**Where is Unity Catalog metadata stored?**

**Correct Answer:**\
✅ **Databricks Control Plane**

**Explanation**

Unity Catalog stores metadata—not customer data.

Examples of metadata:

- Catalog names

- Schema names

- Table definitions

- Permissions

- Ownership

- Data lineage

- Comments

All of this is stored in the **Databricks Control Plane**.

Customer data remains in the customer's cloud storage (such as ADLS Gen2, Amazon S3, or Google Cloud Storage).

**Architecture**

Control Plane\
\
Metadata\
\
Permissions\
\
Lineage\
\
-------------------\
\
Data Plane\
\
Customer Data\
\
Delta Files\
\
Parquet Files

Databricks separates governance metadata from customer data for security and management purposes.

**YouTube**

**Control Plane vs Data Plane**

https://www.youtube.com/results?search_query=Databricks+Control+Plane+Data+Plane

# [README](./../../../README.md)
