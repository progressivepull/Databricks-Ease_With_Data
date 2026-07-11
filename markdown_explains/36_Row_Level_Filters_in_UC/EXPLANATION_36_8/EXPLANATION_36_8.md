# EXPLANATION 36 8

**Question 8**

**What happens after a row filter is attached directly to a Unity Catalog table?**

**Correct Answer:** **C. Unity Catalog automatically applies the filter to every query against the table.**

**Explanation**

Once a row filter is attached using ALTER TABLE ... SET ROW FILTER, Unity Catalog automatically evaluates the filter whenever the table is queried. Users do not need to remember to query a special view or include additional WHERE clauses.

**Why the Correct Answer is Correct**

The enforcement is automatic and transparent, ensuring consistent row-level security.

**Why the Other Answers Are Wrong**

They incorrectly state that users must manually invoke the filter or use a separate object.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=ALTER+TABLE+SET+ROW+FILTER+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
