# EXPLANATION 06 3

**Question 3**

**Which programming languages are natively supported in Databricks notebooks?**

**Correct Answer:**\
✅ **Python, SQL, Scala, and R**

**Explanation**

Databricks notebooks support **four native programming languages**:

| **Language** | **Common Uses**                  |
|--------------|----------------------------------|
| Python       | Data engineering, ML, automation |
| SQL          | Analytics and reporting          |
| Scala        | Native Apache Spark development  |
| R            | Statistics and data science      |

One of the platform's strengths is the ability to use multiple languages in the same notebook.

Example:

\# Python\
df = spark.table("sales")

%sql\
SELECT \* FROM sales

%scala\
println("Hello Spark")

%r\
summary(df)

**YouTube**

**Databricks Notebook Languages**

https://www.youtube.com/results?search_query=Databricks+Notebook+Python+SQL+Scala+R

------------------------------------------------------------------------

# [README](./../../../README.md)
