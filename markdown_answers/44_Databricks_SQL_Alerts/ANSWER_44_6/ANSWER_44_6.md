# ANSWER 44 6

**Question 6**

**If a SQL Alert is configured with the condition Pending Orders \> 10,000 and the query returns 191,189, what will happen?**

**A. The alert status becomes Unknown.** ❌ Incorrect

- The result clearly satisfies the condition.

**B. The alert is automatically deleted.** ❌ Incorrect

- Alerts are never deleted because a condition is met.

**C. The alert status becomes Triggered because the condition evaluates to TRUE.** ✅ Correct

Let's evaluate it:

191,189 \> 10,000

TRUE

Result:

Status = Triggered

Notification Sent

**D. The query execution is canceled.** ❌ Incorrect

- The query already completed.

**E. The SQL Warehouse is stopped automatically.** ❌ Incorrect

- Alerts don't stop compute resources.

**Key Concept**

**Alert = Boolean evaluation (TRUE or FALSE).**

# [README](./../../../README.md)
