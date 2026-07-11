# EXPLANATION 36 9

**Question 9**

**How can an administrator grant a user access to an additional market segment without modifying the row filter function?**

**Correct Answer:** **C. Update the metadata table with the new authorization rule.**

**Explanation**

If the row filter uses a metadata (mapping) table, administrators simply insert or update an authorization record.

Example:

| **User** | **Market** |
|----------|------------|
| Alice    | Healthcare |

No code changes are required because the row filter automatically evaluates the updated authorization data.

**Why the Correct Answer is Correct**

Updating data is simpler and safer than changing security code.

**Why the Other Answers Are Wrong**

The other options require unnecessary modifications to the row filter function or the protected table.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+row+filter+mapping+table

------------------------------------------------------------------------

# [README](./../../../README.md)
