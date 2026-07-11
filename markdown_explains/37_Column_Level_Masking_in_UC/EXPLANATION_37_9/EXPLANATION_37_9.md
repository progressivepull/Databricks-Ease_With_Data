# EXPLANATION 37 9

**Question 9**

**What is an advantage of using is_member() instead of a metadata table for column masking?**

**Correct Answer:** **C. It simplifies authorization by using existing Databricks or identity-provider groups without maintaining custom mappings.**

**Explanation**

Using is_member() removes the need to create and maintain a custom authorization table. Instead, authorization is determined directly from existing Databricks account groups or synchronized identity-provider groups.

**Why the Correct Answer is Correct**

Benefits include:

- Less administration.

- No custom mapping tables.

- Automatic use of existing enterprise groups.

- Easier long-term maintenance.

**Why the Other Answers Are Wrong**

The incorrect options assume is_member() provides additional security beyond group membership or replaces object-level permissions.

**YouTube Video**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**Direct YouTube Link**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+is_member+column+masking

------------------------------------------------------------------------

# [README](./../../../README.md)
