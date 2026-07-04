# EXPLANATION 22 9

**Question 8**

**What happens when Queueing is enabled and compute resources are unavailable?**

**Correct Answer: C. The job waits for resources and can remain queued for up to 48 hours.**

**Explanation**

Sometimes a workflow cannot start immediately because:

- Cluster capacity has been reached.

- Cloud resources are temporarily unavailable.

- Maximum concurrent runs have been reached.

When Queueing is enabled:

Workflow Requested\
│\
Resources Busy\
│\
Job Queued\
│\
Resources Become Available\
│\
Workflow Starts

A queued job can remain waiting for up to **48 hours** before it is dropped.

This prevents jobs from failing immediately due to temporary resource shortages.

**YouTube**

- **Databricks Job Queueing**\
  https://www.youtube.com/results?search_query=Databricks+Job+Queueing

------------------------------------------------------------------------

# [README](./../../../README.md)
