# EXPLANATION 43 10

**Question 10**

**Which pair of SQL statements can be used to automate the setup of Lakehouse Federation?**

**Correct Answer:**\
**C. CREATE CONNECTION and CREATE FOREIGN CATALOG**

**Why C is Correct**

The standard setup sequence is:

CREATE CONNECTION postgres_connection

...

CREATE FOREIGN CATALOG sales_db

USING CONNECTION postgres_connection;

These two SQL statements automate the configuration of a federated external database inside Unity Catalog.

**Why the other choices are wrong**

Other SQL statements create tables, schemas, or views but do not establish the federation infrastructure.

**Memory Tip**

Remember the two-step setup:

1.  **CREATE CONNECTION**

2.  **CREATE FOREIGN CATALOG**

**Individual YouTube Video**

https://www.youtube.com/watch?v=mdw5j0l7K2Y

**YouTube Search**

https://www.youtube.com/results?search_query=CREATE+FOREIGN+CATALOG+Databricks+Lakehouse+Federation

Below is a detailed explanation of each question, why the correct answer is correct, why the other concepts are incorrect, and recommended YouTube resources. The explanations are based on the current Databricks Lakehouse Federation and Unity Catalog documentation.

**Recommended Overall Video**

**Lakehouse Federation Overview (Databricks)**

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Lakehouse+Federation

**Official Documentation**

https://docs.databricks.com/query-federation/

# [README](./../../../README.md)
