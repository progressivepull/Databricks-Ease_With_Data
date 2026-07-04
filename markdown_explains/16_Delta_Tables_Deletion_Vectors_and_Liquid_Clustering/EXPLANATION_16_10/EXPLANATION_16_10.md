# EXPLANATION 16 10

**Question 10**

**What is one limitation when selecting clustering columns for Liquid Clustering?**

**Correct Answer:**\
✅ **Clustering columns must appear within the first 32 columns of the table.**

**Explanation**

Liquid Clustering has an implementation constraint:

The clustering column must be located within the **first 32 columns** of the table schema.

Example:

1 CustomerID\
\
2 Name\
\
3 Address\
\
...\
\
32 Region\
\
33 InvoiceNumber

Here, InvoiceNumber (column 33) cannot be chosen as a clustering column unless the schema is reordered.

This is a technical limitation to be aware of when designing table schemas for Liquid Clustering.

**YouTube**

**Liquid Clustering Tutorial**

https://www.youtube.com/results?search_query=Databricks+Liquid+Clustering+Tutorial

**Recommended YouTube Playlists**

If you're learning modern Delta Lake optimization features, these playlists are excellent:

1.  **Official Databricks – Delta Lake**

    - https://www.youtube.com/results?search_query=Databricks+Delta+Lake

2.  **Deletion Vectors in Databricks**

    - https://www.youtube.com/results?search_query=Databricks+Deletion+Vectors

3.  **Liquid Clustering Tutorial**

    - https://www.youtube.com/results?search_query=Databricks+Liquid+Clustering

4.  **Delta Lake Performance Optimization**

    - https://www.youtube.com/results?search_query=Delta+Lake+Performance+Optimization

5.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

# [README](./../../../README.md)
