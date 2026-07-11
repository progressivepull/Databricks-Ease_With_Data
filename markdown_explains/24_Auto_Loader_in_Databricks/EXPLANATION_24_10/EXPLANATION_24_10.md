# EXPLANATION 24 10

**Question 10**

**Which schema evolution mode stores unexpected columns in the \_rescued_data column without failing the stream?**

**Correct Answer:** **E. rescue**

**Explanation**

When Auto Loader encounters unexpected columns, **rescue mode** keeps the stream running.

Instead of failing:

New Column

↓

Stream Stops

it stores the unexpected data in the special \_rescued_data column:

Name

John

\_rescued_data

Salary=50000

This preserves the data for later review while avoiding pipeline failures.

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+\_rescued_data+Auto+Loader

- https://www.youtube.com/results?search_query=Databricks+Auto+Loader+schema+evolution+rescue

------------------------------------------------------------------------

**Best Overall Auto Loader Videos**

If you only have time to watch a few videos, these are excellent starting points:

1.  **Databricks Official – How Databricks Leverages Auto Loader to Ingest Millions of Files an Hour**\
    https://www.youtube.com/results?search_query=How+Databricks+Leverages+Auto+Loader+to+Ingest+Millions+of+Files+an+Hour

2.  **Databricks Auto Loader Tutorial**\
    https://www.youtube.com/results?search_query=Databricks+Auto+Loader+Tutorial

3.  **CloudFiles + Structured Streaming**\
    https://www.youtube.com/results?search_query=CloudFiles+Structured+Streaming+Databricks

These videos complement the official Databricks documentation and provide visual demonstrations of the concepts covered in your quiz.

# [README](./../../../README.md)
