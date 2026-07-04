# EXPLANATION 22 10

**Question 9**

**What does the Maximum Concurrent Runs setting control?**

**Correct Answer: C. The maximum number of simultaneous executions of the same workflow job**

**Explanation**

Maximum Concurrent Runs limits how many copies of the same workflow can run at once.

Example:

Maximum Concurrent Runs = 2\
\
Run \#1 Running\
\
Run \#2 Running\
\
Run \#3 Waiting

This prevents:

- Resource contention.

- Duplicate processing.

- Excessive cloud costs.

- Conflicts over the same data.

Choosing an appropriate limit helps balance throughput and resource usage.

**YouTube**

- **Databricks Workflow Settings**\
  https://www.youtube.com/results?search_query=Databricks+Workflow+Maximum+Concurrent+Runs

------------------------------------------------------------------------

# [README](./../../../README.md)
