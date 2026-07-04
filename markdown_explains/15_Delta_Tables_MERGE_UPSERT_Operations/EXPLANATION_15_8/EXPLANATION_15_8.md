# EXPLANATION 15 8

**Question 8**

**Which new column is added to support the soft delete implementation?**

**Correct Answer:**\
✅ **IS_ACTIVE**

**Explanation**

Instead of deleting a row:

DELETE

The lesson changes:

IS_ACTIVE = FALSE

Active rows:

TRUE

Inactive rows:

FALSE

Queries simply filter:

WHERE IS_ACTIVE = TRUE

This preserves the data while hiding inactive records from normal queries.

**YouTube**

**Soft Delete Implementation**

https://www.youtube.com/results?search_query=Delta+Lake+Soft+Delete

# [README](./../../../README.md)
