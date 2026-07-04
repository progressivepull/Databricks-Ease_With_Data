# EXPLANATION 11 9

**Question 9**

**What happens when a catalog is created with its own managed location?**

**Correct Answer:**\
✅ **Managed tables are stored under the catalog's managed storage path.**

**Explanation**

Suppose:

Catalog\
\
Finance\
\
↓\
\
Managed Location\
\
/company/finance/

Creating a managed table inside that catalog stores data under:

/company/finance/

unless the schema itself defines a managed location, which has higher priority.

Storage precedence:

Schema\
\
↓\
\
Catalog\
\
↓\
\
Metastore

This allows storage organization by business domain.

**YouTube**

**Unity Catalog Managed Locations**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Location

------------------------------------------------------------------------

# [README](./../../../README.md)
