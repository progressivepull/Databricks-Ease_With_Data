# ANSWER 24 9

**Question 9**

**Which trigger should be used when Auto Loader needs to process all currently available files and then stop automatically?**

**A. .trigger(processingTime="30 seconds")** ❌ Incorrect

Runs continuously every 30 seconds.

Does not stop automatically.

------------------------------------------------------------------------

**B. .trigger(continuous=True)** ❌ Incorrect

Continuous processing mode.

Keeps running.

------------------------------------------------------------------------

**C. .trigger(availableNow=True)** ✅ Correct

Behavior:

Read all existing files

↓

Finish processing

↓

Stop

Ideal for scheduled batch ingestion using streaming.

------------------------------------------------------------------------

**D. .trigger(batchMode=True)** ❌ Incorrect

No such trigger.

------------------------------------------------------------------------

**E. .trigger(once=False)** ❌ Incorrect

Not a valid trigger.

------------------------------------------------------------------------

**Why C is correct**

availableNow=True processes all currently available data and then terminates automatically.

# [README](./../../../README.md)
