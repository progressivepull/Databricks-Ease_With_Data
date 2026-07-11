# EXPLANATION 44 7

**Question 7**

**What notification behavior helps prevent repeated alerts while the monitored condition remains true?**

**Correct Answer:**\
**B. Trigger once until the condition returns to normal**

**Why B is Correct**

Imagine a dashboard is above the threshold for three hours.

Without suppression:

Email

Email

Email

Email

Email

With **Trigger once until OK**:

Email

(wait)

Condition returns to normal

Future trigger allowed

This reduces notification fatigue and prevents users from receiving duplicate alerts for the same ongoing issue.

**Why the other choices are wrong**

Repeated notifications without control can overwhelm users.

**Memory Tip**

**One alert per incident.**

**Individual YouTube Video**

https://www.youtube.com/watch?v=Itz0b6kQK9A

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+SQL+Alert+notification+frequency

------------------------------------------------------------------------

# [README](./../../../README.md)
