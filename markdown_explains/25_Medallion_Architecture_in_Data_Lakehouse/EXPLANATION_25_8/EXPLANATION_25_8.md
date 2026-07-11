# EXPLANATION 25 8

**Question 8**

**Which option enables event-based file detection?**

**Correct Answer**

✅ **B. cloudFiles.useNotifications=true**

**Explanation**

Instead of repeatedly scanning folders:

Auto Loader can receive cloud storage notifications.

Enable with:

.option("cloudFiles.useNotifications","true")

Benefits:

- faster

- fewer API calls

- lower cloud costs

- near real-time ingestion

**Easy Memory Trick**

Notifications = Cloud Events

**YouTube**

https://www.youtube.com/results?search_query=Databricks+Auto+Loader+useNotifications

------------------------------------------------------------------------

# [README](./../../../README.md)
