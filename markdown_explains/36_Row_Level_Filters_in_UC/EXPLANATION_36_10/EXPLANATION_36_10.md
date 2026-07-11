# EXPLANATION 36 10

**Question 10**

**Which statement correctly compares Dynamic Views and Row-Level Filters?**

**Correct Answer:** **B. Dynamic Views require users to query the view, while Row-Level Filters automatically enforce security on all queries against the table.**

**Explanation**

**Dynamic Views**

- Users query the **view**.

- Security logic is implemented in the view definition.

- Useful for presenting filtered or transformed data.

**Row-Level Filters**

- Applied directly to the **table**.

- Automatically enforced on every query.

- No separate view is required.

- Recommended when you want the original table name to remain unchanged.

**Why the Correct Answer is Correct**

The key difference is **where the security is enforced**:

- Dynamic Views protect the **view**.

- Row-Level Filters protect the **table itself**.

**Why the Other Answers Are Wrong**

The incorrect options confuse the scope of enforcement or incorrectly claim the two features behave identically.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Dynamic+Views+vs+Row+Level+Filters

# [README](./../../../README.md)
