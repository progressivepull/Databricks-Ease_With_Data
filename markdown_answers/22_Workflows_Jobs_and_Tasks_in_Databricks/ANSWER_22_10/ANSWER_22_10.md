# ANSWER 22 10

**Question 10**

**In the example workflow from the lesson, what happens if the current day is not Sunday?**

**A. Employee data is processed for every department.** ❌ Incorrect

- That would happen only when the condition is satisfied.

**B. The workflow automatically retries.** ❌ Incorrect

- Retry behavior depends on failures, not the day of the week.

**C. The workflow ends without processing employee data.** ✅ Correct

The lesson included conditional logic similar to:

Is Today Sunday?\
\
│\
Yes │ No\
│\
Process Data\
\
End

If today is not Sunday:

- No employee processing occurs.

- The workflow exits normally.

This is a common scheduling pattern used to prevent unnecessary processing.

**D. A Delta Live Table is created.** ❌ Incorrect

- The condition does not trigger DLT creation.

**E. The workflow creates a new Job Cluster and waits.** ❌ Incorrect

- Waiting is unrelated to the Sunday condition.

------------------------------------------------------------------------

**Memory Trick**

Sunday?

↓

Yes

↓

Process

No

↓

End

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Databricks Workflows | Orchestrate, schedule, and automate multi-step pipelines |
| Job vs. Task | A **Job** is the overall workflow; it contains one or more **Tasks** |
| Supported task type | **Delta Live Tables (DLT)** is one of several supported Workflow task types |
| Notebook source | Stored in either the **Databricks Workspace** or a **Git repository** |
| Job Compute | Automatically created when a workflow starts and terminated when it completes or fails |
| Workflow parameters | Typically populate notebook **dbutils.widgets** |
| Job Parameters vs. Task Parameters | **Job Parameters** are available to every task; **Task Parameters** apply only to a specific task |
| Queueing | Jobs wait for compute resources (up to **48 hours**) instead of failing immediately |
| Maximum Concurrent Runs | Limits how many instances of the **same workflow job** can run simultaneously |
| Lesson example | If the current day is **not Sunday**, the workflow ends without processing employee data |

# [README](./../../../README.md)
