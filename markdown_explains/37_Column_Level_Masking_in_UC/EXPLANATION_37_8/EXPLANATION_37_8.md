# EXPLANATION 37 8

**Question 8**

**What is the purpose of the built-in is_member() function?**

**Correct Answer:** **B. To check whether the current user belongs to a specified group**

**Explanation**

is_member() evaluates whether the current user belongs to a specified Databricks or identity-provider group. It allows masking rules to be based on group membership rather than maintaining separate mapping tables.

Example:

CASE

WHEN is_member('HR')

THEN salary

ELSE NULL

END

**Why the Correct Answer is Correct**

It simplifies authorization by leveraging existing group memberships.

**Why the Other Answers Are Wrong**

The incorrect options suggest it validates passwords, checks table ownership, or performs unrelated tasks.

**YouTube Video**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**Direct YouTube Link**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+is_member+function

------------------------------------------------------------------------

# [README](./../../../README.md)
