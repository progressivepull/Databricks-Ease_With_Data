# EXPLANATION 23 8

**Question 7**

**How can COPY INTO perform simple transformations while loading data?**

**Correct Answer: B. By wrapping the source data in a SELECT statement that performs transformations**

**Explanation**

Instead of loading the source directly, you can transform it first.

Example:

COPY INTO sales\
FROM (\
SELECT\
upper(customer_name) AS customer_name,\
amount \* 1.10 AS amount\
FROM '/Volumes/raw/sales'\
)\
FILEFORMAT = CSV;

Common transformations include:

- Renaming columns.

- Changing letter case.

- Calculating derived values.

- Filtering rows.

- Casting data types.

This is useful for lightweight data cleansing during ingestion.

**YouTube**

- **Databricks COPY INTO Transformations**\
  https://www.youtube.com/results?search_query=Databricks+COPY+INTO+SELECT

# [README](./../../../README.md)
