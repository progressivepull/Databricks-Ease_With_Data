# ANSWER 22 8

**Question 8**

**What happens when Queueing is enabled and compute resources are unavailable?**

**A. The job immediately fails.** ❌ Incorrect

- Queueing prevents immediate failure.

**B. The workflow automatically switches to Serverless Compute.** ❌ Incorrect

- Databricks does not automatically switch compute types.

**C. The job waits for resources and can remain queued for up to 48 hours.** ✅ Correct

Example:

No Compute Available\
\
↓\
\
Queue\
\
↓\
\
Resources Become Available\
\
↓\
\
Run Job

This helps prevent failures caused by temporary resource shortages.

**D. The job skips all dependent tasks.** ❌ Incorrect

- Tasks wait.

**E. The job is automatically deleted.** ❌ Incorrect

- Jobs remain queued.

------------------------------------------------------------------------

**Memory Trick**

Queue Enabled

↓

Wait

Not Fail

------------------------------------------------------------------------

# [README](./../../../README.md)
