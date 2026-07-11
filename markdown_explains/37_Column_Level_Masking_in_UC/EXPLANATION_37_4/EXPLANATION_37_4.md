# EXPLANATION 37 4

**Question 4**

**In the metadata-driven masking approach, what is the primary purpose of the metadata table?**

**Correct Answer:** **B. To maintain mappings between users and their authorization groups or roles**

**Explanation**

Rather than embedding authorization rules directly in the masking function, a metadata table stores mappings such as:

| **User** | **Role** |
|----------|----------|
| Alice    | HR       |
| Bob      | Finance  |
| Carol    | Manager  |

The masking function references this table to determine whether a user should receive the original value or a masked version.

**Why the Correct Answer is Correct**

A metadata table centralizes authorization and allows administrators to update permissions by changing data instead of code.

**Why the Other Answers Are Wrong**

The incorrect options suggest storing actual masked values or application logic in the metadata table.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+metadata+table+column+masking

------------------------------------------------------------------------

# [README](./../../../README.md)
