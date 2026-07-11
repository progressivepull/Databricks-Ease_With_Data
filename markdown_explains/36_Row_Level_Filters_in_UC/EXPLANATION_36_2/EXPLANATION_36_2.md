# EXPLANATION 36 2

**Question 2**

**Why are Row-Level Filters preferred over maintaining multiple copies of the same table?**

**Correct Answer:** **B. They dynamically restrict access based on security rules while allowing all users to query a single physical table.**

**Explanation**

Instead of creating separate tables such as:

- sales_us

- sales_europe

- sales_asia

Unity Catalog keeps **one table** and filters rows dynamically according to the current user's permissions. This greatly simplifies maintenance and ensures consistent data.

**Why the Correct Answer is Correct**

Benefits include:

- One source of truth.

- Lower storage costs.

- Easier maintenance.

- Centralized security policies.

- No duplicated ETL pipelines.

**Why the Other Answers Are Wrong**

The other options require maintaining multiple copies of the same data, increasing complexity.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+Row+Filters

------------------------------------------------------------------------

# [README](./../../../README.md)
