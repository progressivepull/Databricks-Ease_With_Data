# EXPLANATION 49 2

**Question 2**

**The Databricks CLI is built on top of which underlying technology?**

**Correct Answer:**\
**B. Databricks REST API**

**Why B is Correct**

The Databricks CLI is essentially a command-line wrapper around the Databricks REST API.

For example:

databricks catalogs list

internally calls the appropriate Databricks REST API endpoint and formats the response for terminal use.

Because of this, nearly everything you can do with the CLI can also be done through the REST API. ([docs.databricks.com](https://docs.databricks.com/aws/en/dev-tools/cli/))

**Why the other choices are wrong**

The CLI is not built directly on:

- Spark

- Photon

- Delta Lake

- Unity Catalog

**Memory Tip**

**CLI = REST API + Friendly Commands**

**Individual YouTube Video**

https://www.youtube.com/watch?v=5s8N4vV5m9M

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+REST+API+CLI

------------------------------------------------------------------------

# [README](./../../../README.md)
