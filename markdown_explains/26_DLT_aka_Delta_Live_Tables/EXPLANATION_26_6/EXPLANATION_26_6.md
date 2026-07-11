# EXPLANATION 26 6

**Question 6**

**Which keyword is used to reference datasets created earlier within the same Delta Live Tables pipeline?**

**Correct Answer:** **C. LIVE**

**Explanation**

The LIVE keyword allows one dataset inside the pipeline to reference another.

Example:

SELECT \*

FROM LIVE.bronze_orders

**Why the Correct Answer is Correct**

LIVE tells DLT to use another dataset defined within the same pipeline rather than an external table.

**Why the Other Answers Are Wrong**

They are not valid DLT pipeline reference keywords.

**YouTube Video**

**Direct Link**\
[<u>https://www.youtube.com/watch?v=iqf_QHC7tgQ</u>](https://www.youtube.com/watch?v=iqf_QHC7tgQ)

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+LIVE+keyword+DLT

# [README](./../../../README.md)
