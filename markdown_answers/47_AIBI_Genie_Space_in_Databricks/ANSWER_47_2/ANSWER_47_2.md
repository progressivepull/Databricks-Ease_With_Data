# ANSWER 47 2

**Question 2**

**When a user asks a question in plain English, what sequence of actions does Genie perform?**

**A. Creates a Delta table, refreshes a Materialized View, and publishes a dashboard** ❌ Incorrect

- Genie doesn't create database objects.

**B. Generates SQL, executes it on a SQL Warehouse, and returns results with tables and visualizations** ✅ Correct

Genie's workflow is:

Ask Question

│

Understand Meaning

│

Generate SQL

│

Run SQL Warehouse

│

Display Results

│

Optional Charts

Everything happens automatically.

**C. Converts the question into Python code and runs it on a cluster** ❌ Incorrect

- Genie generates **SQL**, not Python.

**D. Exports the data to Excel before displaying results** ❌ Incorrect

- Results are displayed directly in Genie.

**E. Creates a new Unity Catalog schema automatically** ❌ Incorrect

- Genie never creates schemas.

**Key Concept**

**English → SQL → SQL Warehouse → Results**

# [README](./../../../README.md)
