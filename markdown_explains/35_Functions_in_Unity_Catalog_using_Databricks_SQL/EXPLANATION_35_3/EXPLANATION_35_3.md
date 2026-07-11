# EXPLANATION 35 3

**Question 3**

**What is the primary advantage of a Unity Catalog User-Defined Function (UDF) over a PySpark session UDF?**

**Correct Answer:** **C. It is permanently registered, shared across users, and governed by Unity Catalog permissions.**

**Explanation**

A standard PySpark UDF exists only for the lifetime of the current Spark session. A Unity Catalog UDF is stored permanently in Unity Catalog, where it can be reused by different users and governed with permissions.

**Why the Correct Answer is Correct**

Unity Catalog UDFs:

- Persist after the session ends.

- Can be shared across teams.

- Support centralized governance.

- Are reusable from SQL and notebooks.

**Why the Other Answers Are Wrong**

They incorrectly describe temporary session UDF behavior.

**YouTube Video**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**Direct YouTube Link**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+Python+UDF

------------------------------------------------------------------------

# [README](./../../../README.md)
