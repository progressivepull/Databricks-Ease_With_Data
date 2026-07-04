# EXPLANATION 23 9

**Question 8**

**What happens when a new source file is added to the landing folder and COPY INTO is executed again?**

**Correct Answer: B. Only the new file is processed while previously loaded files are skipped.**

**Explanation**

Example:

First day:

orders1.csv\
orders2.csv

Run COPY INTO:

Both files are loaded.

Later:

orders1.csv\
orders2.csv\
orders3.csv

Run COPY INTO again:

Only orders3.csv is loaded.

This incremental loading makes COPY INTO ideal for scheduled batch ingestion.

**YouTube**

- **Incremental Loads with COPY INTO**\
  https://www.youtube.com/results?search_query=Databricks+COPY+INTO+incremental

# [README](./../../../README.md)
