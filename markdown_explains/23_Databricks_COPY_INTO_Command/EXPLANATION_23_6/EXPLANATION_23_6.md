# EXPLANATION 23 6

**Question 5**

**Which capability allows COPY INTO to automatically create columns and detect data types when loading data into a placeholder table?**

**Correct Answer: B. Schema Inference**

**Explanation**

**Schema Inference** examines the source data and determines:

- Column names

- Data types

- Column order

Example CSV:

EmployeeID,Name,Salary\
1,Alice,75000\
2,Bob,68000

Databricks infers:

| **Column** | **Data Type** |
|------------|---------------|
| EmployeeID | Integer       |
| Name       | String        |
| Salary     | Integer       |

This eliminates the need to manually define the schema for many datasets.

**YouTube**

- **Schema Inference in Databricks**\
  https://www.youtube.com/results?search_query=Databricks+Schema+Inference

# [README](./../../../README.md)
