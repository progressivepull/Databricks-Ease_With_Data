# ANSWER 24 8

**Question 8**

**Which Auto Loader option enables event-based file detection using cloud notification services?**

**A. cloudFiles.enableStreaming=true** ❌ Incorrect

No such option.

------------------------------------------------------------------------

**B. cloudFiles.useNotifications=true** ✅ Correct

Example:

.option(

"cloudFiles.useNotifications",

"true"

)

Uses:

- Azure Event Grid

- AWS SQS

- Google Pub/Sub

instead of directory listing.

------------------------------------------------------------------------

**C. cloudFiles.eventMode=true** ❌ Incorrect

No such option.

------------------------------------------------------------------------

**D. cloudFiles.notificationService=eventGrid** ❌ Incorrect

Not a valid Auto Loader option.

------------------------------------------------------------------------

**E. cloudFiles.incremental=true** ❌ Incorrect

Auto Loader is already incremental.

------------------------------------------------------------------------

**Why B is correct**

cloudFiles.useNotifications=true enables cloud notification–based file discovery.

------------------------------------------------------------------------

# [README](./../../../README.md)
