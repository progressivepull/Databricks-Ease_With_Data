# EXPLANATION 16 4

**Question 4**

**Which table property controls whether Deletion Vectors are enabled?**

**Correct Answer:**\
✅ **delta.enableDeletionVectors**

**Explanation**

Enable Deletion Vectors with:

ALTER TABLE employees\
\
SET TBLPROPERTIES (\
\
'delta.enableDeletionVectors'='true'\
\
);

Once enabled, supported operations like DELETE, UPDATE, and MERGE can use Deletion Vectors instead of immediately rewriting files.

**YouTube**

**Delta Table Properties**

https://www.youtube.com/results?search_query=Databricks+Table+Properties

# [README](./../../../README.md)
