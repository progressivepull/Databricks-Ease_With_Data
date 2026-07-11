# ANSWER 44 7

**Question 7**

**What notification behavior helps prevent repeated alerts while the monitored condition remains true?**

**A. Notify every evaluation** ❌ Incorrect

- This would generate excessive notifications.

Example:

Every minute...

Still TRUE

Still TRUE

Still TRUE

Still TRUE

Hundreds of notifications could be sent.

**B. Trigger once until the condition returns to normal** ✅ Correct

- Databricks avoids alert fatigue.

- Once triggered:

  - No additional notifications are sent while the condition remains true.

  - A new notification is sent only after:

    - Condition becomes false

    - Then becomes true again

Timeline:

False

↓

True

↓

Notification

↓

Still True

↓

No Notification

↓

False

↓

True Again

↓

New Notification

**C. Run the SQL query continuously without evaluation** ❌ Incorrect

- Alerts always evaluate conditions.

**D. Disable notifications after the first query execution** ❌ Incorrect

- Alerts continue monitoring.

**E. Execute a full refresh before every evaluation** ❌ Incorrect

- Refreshes have nothing to do with notification behavior.

**Key Concept**

**Trigger once until recovery = prevents alert spam.**

# [README](./../../../README.md)
