# ANSWER 25 7

**Question 7**

**What happens when Auto Loader uses the Available Now trigger?**

**A. The stream runs forever until manually stopped. ❌ Incorrect**

That's continuous streaming.

------------------------------------------------------------------------

**B. Only one file is processed each time the stream runs. ❌ Incorrect**

Auto Loader processes **all** available files.

------------------------------------------------------------------------

**C. All currently available files are processed, and then the stream stops automatically. ✅ Correct**

Workflow:

Start

↓

Read every available file

↓

Write to Delta

↓

Stop automatically

This is excellent for scheduled jobs.

------------------------------------------------------------------------

**D. Files are processed only when a user manually approves them. ❌ Incorrect**

No manual approval is required.

------------------------------------------------------------------------

**E. Processing occurs only when new notifications arrive. ❌ Incorrect**

That's notification mode, not Available Now.

------------------------------------------------------------------------

**Why C is correct**

availableNow=True combines streaming reliability with batch-style execution.

------------------------------------------------------------------------

# [README](./../../../README.md)
