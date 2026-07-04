# EXPLANATION 23 4

**Question 3**

**What does it mean that COPY INTO is idempotent?**

**Correct Answer: C. Running the command multiple times does not reload previously processed files.**

**Explanation**

An **idempotent** operation produces the same result no matter how many times it is run with the same input.

Example:

Initial folder:

orders1.csv\
orders2.csv\
orders3.csv

First run:

COPY INTO orders\
FROM '/landing/orders';

All three files are loaded.

Running the same command again:

COPY INTO orders\
FROM '/landing/orders';

No duplicate rows are added because those files have already been processed.

This behavior simplifies scheduled ingestion jobs and avoids accidental duplicate loads.

**YouTube**

- **Databricks COPY INTO Idempotent Loading**\
  https://www.youtube.com/results?search_query=Databricks+COPY+INTO+idempotent

# [README](./../../../README.md)
