# EXPLANATION 42 10

**Question 10**

**According to best practices, what is the correct refresh order when using both Streaming Tables and Materialized Views?**

**Correct Answer:**\
**C. Refresh the Streaming Table first, then refresh the Materialized View.**

**Why C is Correct**

A Materialized View often depends on data stored in a Streaming Table.

The correct workflow is:

1.  Refresh the Streaming Table to ingest the latest source data.

2.  Refresh the Materialized View so it reads the updated Streaming Table.

Refreshing the Materialized View first could leave it based on stale data.

**Why the other choices are wrong**

Refreshing in the reverse order or independently risks reporting outdated information.

**Memory Tip**

Think of it as a pipeline:

**Source → Streaming Table → Materialized View → Dashboard**

Refresh in that same order.

**Individual YouTube Video**

Streaming Tables and Materialized Views Pipeline

https://www.youtube.com/watch?v=lR1Q3F2M4qI

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Streaming+Tables+Materialized+Views+refresh+order

**Note on YouTube links:** Databricks periodically updates or replaces videos on its official channel. If an individual direct link is unavailable or changes over time, the accompanying YouTube search link will help you locate the current version of the topic.

Below is a detailed explanation of each question, why the correct answer is correct, why the other concepts are incorrect, and recommended YouTube resources. The explanations are based on current Databricks SQL, Streaming Tables, Materialized Views, and Lakeflow Declarative Pipelines (formerly Delta Live Tables) documentation.

**Recommended overall video**

**Databricks SQL: Materialized Views & Streaming Tables**

YouTube Search:

https://www.youtube.com/results?search_query=Databricks+Streaming+Tables+Materialized+Views

Official Documentation:

https://docs.databricks.com/sql/

# [README](./../../../README.md)
