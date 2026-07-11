# EXPLANATION 25 5

**Question 5**

**Which Auto Loader option specifies where inferred schemas are stored?**

**Correct Answer**

✅ **C. cloudFiles.schemaLocation**

**Explanation**

Auto Loader automatically infers schemas.

It needs somewhere to save them.

That location is specified by:

.option("cloudFiles.schemaLocation", "/schemas/")

This allows schema evolution over time without rediscovering the schema each run.

**Easy Memory Trick**

Schema Location stores the evolving schema.

**YouTube**

https://www.youtube.com/results?search_query=Databricks+cloudFiles.schemaLocation

------------------------------------------------------------------------

# [README](./../../../README.md)
