# EXPLANATION 45 10

**Question 10**

**What permissions are typically granted to users with Consumer Access?**

**Correct Answer:**\
**C. Dashboard and Genie access without development or cluster management privileges**

**Why C is Correct**

Consumer users are business users who consume analytics rather than build data pipelines.

Typical capabilities include:

- View AI/BI Dashboards

- Use Genie

- Query published semantic models (as permitted)

They typically do **not**:

- create clusters

- manage compute

- develop notebooks

- administer Unity Catalog

This supports a least-privilege security model while giving users access to trusted business metrics.

**Why the other choices are wrong**

Consumer Access is designed for using governed analytics, not for platform administration or engineering tasks.

**Memory Tip**

**Consumer = Consume Analytics**

**Developer = Build Analytics**

**Individual YouTube Video**

https://www.youtube.com/watch?v=qhNohS4Lj24

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Genie+Metric+Views+Unity+Catalog

# [README](./../../../README.md)
