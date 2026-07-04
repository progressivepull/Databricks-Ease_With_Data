# EXPLANATION 20 9

**Question 8**

**What does Auto Scaling do for a Databricks cluster?**

**Correct Answer: B. Automatically adjusts the number of worker nodes based on workload demand.**

**Explanation**

Auto Scaling automatically increases or decreases the number of worker nodes based on the workload.

Example:

Morning\
2 Workers\
\
Large ETL Job\
⬇\
\
8 Workers\
\
Job Finishes\
⬇\
\
2 Workers

Benefits:

- Better performance during peak workloads.

- Reduced cloud costs during idle periods.

- No manual resizing required.

The Driver Node remains constant; Auto Scaling changes only the number of Worker Nodes.

**YouTube**

- **Databricks Autoscaling Explained**\
  https://www.youtube.com/results?search_query=Databricks+Autoscaling

# [README](./../../../README.md)
