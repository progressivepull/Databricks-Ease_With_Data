# EXPLANATION 36 7

**Question 7**

**Why does the lesson first implement the security logic as a dynamic view before applying a row filter to the table?**

**Correct Answer:** **C. They allow the security logic to be validated before applying automatic enforcement at the table level.**

**Explanation**

A Dynamic View allows developers to test and verify the filtering logic before attaching it directly to the table as a row filter.

This approach helps:

- Validate results.

- Debug authorization logic.

- Ensure users see only expected rows.

**Why the Correct Answer is Correct**

Testing with a view reduces the risk of applying incorrect security policies directly to production tables.

**Why the Other Answers Are Wrong**

The incorrect options imply Dynamic Views are required for Row-Level Security, which is not the case.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Dynamic+Views+Row+Level+Security

------------------------------------------------------------------------

# [README](./../../../README.md)
