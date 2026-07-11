# EXPLANATION 40 3

**Question 3**

**How does the Serverless Compute architecture differ from Classic Compute?**

**Correct Answer:**

**B. Serverless uses a Databricks-managed compute plane that securely accesses customer data.**

------------------------------------------------------------------------

**Why B is Correct**

Classic Compute:

Customer cloud account owns compute.

Serverless:

Databricks owns the compute plane.

It securely connects to customer data while Databricks manages the infrastructure.

------------------------------------------------------------------------

**Why the others are wrong**

Serverless:

- still reads customer data

- still uses Spark

- still uses Delta Lake

Only **who manages compute** changes.

------------------------------------------------------------------------

**Memory Tip**

Classic = Customer Compute

Serverless = Databricks Compute

------------------------------------------------------------------------

**Individual Video**

[https://www.youtube.com/watch?v=hqqAJlQaTCQ](https://www.youtube.com/watch?v=hqqAJlQaTCQ&utm_source=chatgpt.com)

**Search**

https://www.youtube.com/results?search_query=Databricks+Serverless+architecture

------------------------------------------------------------------------

# [README](./../../../README.md)
