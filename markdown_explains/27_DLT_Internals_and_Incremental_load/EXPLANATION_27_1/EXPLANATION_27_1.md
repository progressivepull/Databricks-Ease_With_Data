# EXPLANATION 27 1

**Question 1**

**What is one of the biggest advantages of Delta Live Tables (DLT) regarding pipeline datasets?**

**Correct Answer:** **B. DLT automatically manages the lifecycle of datasets created within a pipeline.**

**Explanation**

One of the major benefits of Delta Live Tables (now called **Lakeflow Declarative Pipelines**) is that developers only define the datasets and transformations. Databricks automatically manages the creation, updating, refreshing, optimization, and overall lifecycle of the datasets produced by the pipeline.

**Why the Correct Answer is Correct**

DLT automatically:

- Creates Streaming Tables and Materialized Views.

- Refreshes datasets when upstream data changes.

- Tracks dependencies.

- Manages metadata and pipeline state.

Developers focus on business logic instead of infrastructure.

**Why the Other Answers Are Wrong**

The incorrect options generally imply that developers must manually create, refresh, or manage datasets, which defeats the purpose of DLT.

**YouTube Video**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**YouTube Search**\
https://www.youtube.com/results?search_query=Delta+Live+Tables+dataset+lifecycle

------------------------------------------------------------------------

# [README](./../../../README.md)
