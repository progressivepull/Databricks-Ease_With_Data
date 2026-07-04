# EXPLANATION 17 3

**Question 3**

**Where do Volumes fit within the Unity Catalog object hierarchy?**

**Correct Answer:**\
✅ **As siblings of Tables within a Schema**

**Explanation**

Volumes live inside a schema.

Hierarchy:

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
├── Tables\
\
├── Views\
\
├── Functions\
\
└── Volumes

Notice that Volumes exist alongside tables—they are not inside tables.

**Think of a Schema like a Folder**

Sales Schema\
\
├── Orders Table\
\
├── Customers Table\
\
├── Sales View\
\
└── Files Volume

**YouTube**

**Unity Catalog Hierarchy**

https://www.youtube.com/results?search_query=Unity+Catalog+Hierarchy

# [README](./../../../README.md)
