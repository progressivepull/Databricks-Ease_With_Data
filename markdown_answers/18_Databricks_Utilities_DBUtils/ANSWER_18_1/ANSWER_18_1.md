# ANSWER 18 1

**Question 1**

**Which notebook languages support DBUtils?**

**A. Python, Java, and SQL** ❌ Incorrect

- Python supports DBUtils.

- Java notebooks do **not** support DBUtils.

- SQL notebooks do not directly use the DBUtils API (although SQL can call some notebook features indirectly).

- Because Java is included, this answer is incorrect.

**B. Python, Scala, and R** ✅ Correct

DBUtils is officially supported in:

- Python

- Scala

- R

Examples:

Python

dbutils.fs.ls("/Volumes/main/default/files")

Scala

dbutils.fs.ls("/Volumes/main/default/files")

R

dbutils.fs.ls("/Volumes/main/default/files")

These languages can directly call DBUtils.

**C. SQL, Scala, and JavaScript** ❌ Incorrect

- Scala is correct.

- SQL is not a DBUtils language.

- JavaScript notebooks do not exist in Databricks.

**D. Python, SQL, and Java** ❌ Incorrect

- SQL and Java are incorrect.

**E. R, JavaScript, and SQL** ❌ Incorrect

- JavaScript and SQL are incorrect.

**Memory Trick**

DBUtils works in:

Python\
\
Scala\
\
R

Not SQL.

# [README](./../../../README.md)
