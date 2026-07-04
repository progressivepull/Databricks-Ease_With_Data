# EXPLANATION 23 5

**Question 4**

**Why does the lesson create a placeholder Delta table before using COPY INTO?**

**Correct Answer: B. To create an empty table without a predefined schema so COPY INTO can infer it automatically**

**Explanation**

Instead of manually defining every column, you can create an empty Delta table and allow COPY INTO to infer the schema.

Example:

CREATE TABLE employees;

Then:

COPY INTO employees\
FROM '/Volumes/raw/employees'\
FILEFORMAT = CSV\
FORMAT_OPTIONS ('header'='true');

Databricks inspects the source files and automatically creates the table schema.

Benefits:

- Less manual work.

- Faster development.

- Fewer schema definition errors.

**YouTube**

- **Databricks Schema Inference**\
  https://www.youtube.com/results?search_query=Databricks+Schema+Inference

# [README](./../../../README.md)
