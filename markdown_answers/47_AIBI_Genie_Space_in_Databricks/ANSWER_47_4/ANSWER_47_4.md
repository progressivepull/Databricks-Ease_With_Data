# ANSWER 47 4

**Question 4**

**Which type of information does Genie primarily use to understand the meaning of user questions?**

**A. Delta transaction logs only** ❌ Incorrect

- Transaction logs track changes to Delta tables.

- They don't explain business meaning.

**B. Notebook source code** ❌ Incorrect

- Genie doesn't learn from notebook code.

**C. Metadata such as table descriptions, column comments, dataset names, and relationships** ✅ Correct

Metadata gives AI context.

Example

Table

orders

Column

cust_id

Without description

AI doesn't know what "cust_id" means.

With description

Customer Identifier

Now Genie understands.

Good metadata dramatically improves accuracy.

**D. Spark executor logs** ❌ Incorrect

- Logs are for troubleshooting.

**E. Git repository history** ❌ Incorrect

- Source control isn't used for question interpretation.

**Key Concept**

**Better metadata = Better AI answers**

# [README](./../../../README.md)
