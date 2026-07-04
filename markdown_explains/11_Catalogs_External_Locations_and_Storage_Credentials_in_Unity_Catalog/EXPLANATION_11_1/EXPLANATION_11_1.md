# EXPLANATION 11 1

**Question 1**

**When a managed table is created in Unity Catalog, which managed location has the highest priority for storing its data?**

**Correct Answer:**\
✅ **Schema Managed Location**

**Explanation**

Unity Catalog allows **managed storage locations** to be configured at three levels:

1.  **Schema**

2.  **Catalog**

3.  **Metastore**

When a managed table is created, Unity Catalog checks for a storage location in this order:

Schema Managed Location\
↓\
Catalog Managed Location\
↓\
Metastore Managed Location

If a managed location exists on the **schema**, it takes precedence over all others.

**Example**

Suppose you have:

Metastore\
Managed Location:\
/company/\
\
Catalog: Finance\
Managed Location:\
/company/finance/\
\
Schema: Payroll\
Managed Location:\
/company/payroll/

Creating a managed table inside the **Payroll** schema stores its data in:

/company/payroll/

because the schema-level location has the highest priority.

This hierarchy allows organizations to control storage at different levels of granularity. Databricks documents this precedence for managed storage locations.

**YouTube**

**Unity Catalog Managed Storage**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Storage

------------------------------------------------------------------------

# [README](./../../../README.md)
