# EXPLANATION 08 5

**Question 5**

**Which of the following is the highest-level data securable object in Unity Catalog?**

**Correct Answer:**\
✅ **Catalog**

**Explanation**

A **Catalog** is the highest-level **data securable** object.

Hierarchy:

Catalog\
\
↓\
\
Schema\
\
↓\
\
Table

Permissions can be assigned at the catalog level.

Example:

GRANT SELECT\
ON CATALOG finance\
TO analysts;

Everything inside the catalog inherits permissions where appropriate.

**Memory Trick**

Security starts at:

Catalog

**YouTube**

**Unity Catalog Security**

https://www.youtube.com/results?search_query=Unity+Catalog+Security

# [README](./../../../README.md)
