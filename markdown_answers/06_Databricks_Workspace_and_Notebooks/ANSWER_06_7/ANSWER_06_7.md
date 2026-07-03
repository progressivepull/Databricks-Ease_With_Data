# ANSWER 06 7

**Question 7**

**Which feature allows multiple programming languages to be used within the same Databricks notebook?**

**A. Unity Catalog** ❌ Incorrect

- Unity Catalog manages data governance.

- It has nothing to do with notebook languages.

**B. Delta Lake** ❌ Incorrect

- Delta Lake manages data storage and transactions.

- It does not switch programming languages.

**C. Magic Commands (such as %sql and %sh)** ✅ **Correct**

- Magic Commands change the language for a notebook cell.

Examples:

%python

%sql

%scala

%r

%sh

This allows one notebook to combine Python, SQL, Scala, R, and shell commands.

**D. MLflow Experiments** ❌ Incorrect

- MLflow tracks machine learning experiments.

- It does not control notebook languages.

**E. Variable Explorer** ❌ Incorrect

- Variable Explorer displays variables during debugging.

- It does not change languages.

**Key Concept**

Magic Commands let you choose the language **one cell at a time**, making Databricks notebooks highly flexible.

------------------------------------------------------------------------

# [README](./../../../README.md)
