# EXPLANATION 37 1

**Question 1**

**What is the primary purpose of Column-Level Masking in Unity Catalog?**

**Correct Answer:** **C. To dynamically hide or mask sensitive column values while keeping the column visible**

**Explanation**

Column-Level Masking (also called **column masks**) protects sensitive information such as Social Security numbers, phone numbers, email addresses, or credit card numbers by replacing the original values with masked values at query time. Users can still see the column itself, but the returned values depend on their permissions.

**Why the Correct Answer is Correct**

Column masking:

- Keeps the column available in query results.

- Dynamically returns either the original value or a masked value.

- Is evaluated automatically during query execution.

- Protects sensitive data without duplicating tables.

**Why the Other Answers Are Wrong**

- They describe hiding entire rows (Row-Level Security).

- They describe removing columns entirely rather than masking values.

- They confuse object permissions with data masking.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Column+Masking+Unity+Catalog

------------------------------------------------------------------------

# [README](./../../../README.md)
