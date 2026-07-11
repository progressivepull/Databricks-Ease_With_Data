# EXPLANATION 36 4

**Question 4**

**What is the purpose of the metadata table used in the lesson?**

**Correct Answer:** **C. To centrally maintain user authorization rules, such as which market segments each user may access**

**Explanation**

A metadata (or mapping) table stores authorization rules instead of hardcoding them inside the row filter function.

Example:

| **User** | **Market** |
|----------|------------|
| Alice    | Retail     |
| Bob      | Government |
| Carol    | Healthcare |

The row filter consults this table to determine whether the current user can access a given row. Databricks recommends mapping tables for many row-level security scenarios.

**Why the Correct Answer is Correct**

A metadata table allows administrators to update permissions by modifying data instead of changing code.

**Why the Other Answers Are Wrong**

They incorrectly suggest storing security logic in notebooks or rewriting the row filter function.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+row+level+security+mapping+table

------------------------------------------------------------------------

# [README](./../../../README.md)
