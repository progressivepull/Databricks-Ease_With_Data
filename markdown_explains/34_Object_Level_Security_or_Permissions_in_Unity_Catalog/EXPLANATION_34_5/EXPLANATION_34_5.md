# EXPLANATION 34 5

**Question 5**

**Which combination of privileges is required for a user to successfully query a Unity Catalog table?**

**Correct Answer:** **D. USE CATALOG, USE SCHEMA, and SELECT**

**Explanation**

To query a table, a user must have:

- **USE CATALOG** – Access the catalog.

- **USE SCHEMA** – Access the schema.

- **SELECT** – Read data from the table.

Without any one of these privileges, the query will fail.

**Why the Correct Answer is Correct**

All three privileges are required because users must navigate the hierarchy before reading table data.

**Why the Other Answers Are Wrong**

Each missing privilege prevents successful table access.

**YouTube Video**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**Direct YouTube Link**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+USE+CATALOG+USE+SCHEMA+SELECT

------------------------------------------------------------------------

# [README](./../../../README.md)
