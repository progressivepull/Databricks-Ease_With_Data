# EXPLANATION 08 3

**Question 3**

**Which object is the top-level container in the Unity Catalog hierarchy?**

**Correct Answer:**\
✅ **Metastore**

**Explanation**

The Unity Catalog hierarchy is:

Metastore\
│\
▼\
Catalog\
│\
▼\
Schema\
│\
▼\
Table\
View\
Function\
Volume

The **Metastore** sits at the very top.

It stores:

- Metadata

- Permissions

- Catalog definitions

- Governance information

A common best practice is to have **one metastore per cloud region**.

**Think of it like a company**

Company\
\
↓\
\
Building\
\
↓\
\
Department\
\
↓\
\
Office\
\
↓\
\
Desk

Equivalent:

Metastore\
\
↓\
\
Catalog\
\
↓\
\
Schema\
\
↓\
\
Table

**YouTube**

**Unity Catalog Architecture**

https://www.youtube.com/results?search_query=Unity+Catalog+Architecture

# [README](./../../../README.md)
