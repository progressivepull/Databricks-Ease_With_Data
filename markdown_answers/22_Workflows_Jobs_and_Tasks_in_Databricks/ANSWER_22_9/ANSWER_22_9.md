# ANSWER 22 9

**Question 9**

**What does the Maximum Concurrent Runs setting control?**

**A. The number of worker nodes in a cluster** ❌ Incorrect

- Worker count is controlled by cluster settings.

**B. The number of notebooks that can be edited simultaneously** ❌ Incorrect

- Editing notebooks isn't limited by this setting.

**C. The maximum number of simultaneous executions of the same workflow job** ✅ Correct

Example:

Maximum Concurrent Runs:

2

Timeline:

Run 1\
\
Run 2\
\
Run 3\
\
↓\
\
Waits

The third execution waits until one finishes.

This prevents overlapping executions that could compete for the same data or resources.

**D. The number of SQL queries executed per second** ❌ Incorrect

- SQL throughput isn't controlled here.

**E. The number of clusters created per workspace** ❌ Incorrect

- Cluster limits are separate.

------------------------------------------------------------------------

**Memory Trick**

Concurrent Runs

↓

Same Job

Running Together

------------------------------------------------------------------------

# [README](./../../../README.md)
