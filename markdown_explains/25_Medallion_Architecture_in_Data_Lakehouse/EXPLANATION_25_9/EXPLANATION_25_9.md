# EXPLANATION 25 9

**Question 9**

**Which trigger processes all current files and then stops automatically?**

**Correct Answer**

✅ **C. .trigger(availableNow=True)**

**Explanation**

Normally:

.writeStream.start()

runs forever.

Sometimes you want:

- process everything currently available

- stop automatically

Use:

.trigger(availableNow=True)

This is commonly used for scheduled ingestion jobs.

**Easy Memory Trick**

Available Now = Process Everything, Then Exit

**YouTube**

https://www.youtube.com/results?search_query=Databricks+availableNow+trigger

------------------------------------------------------------------------

# [README](./../../../README.md)
